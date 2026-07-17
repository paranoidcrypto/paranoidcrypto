# Security Policy / Política de Seguridad

**ParanoidCrypto v2.0** · DNA-based text encryption  
Author: Paris Lavin · ORCID: [0000-0002-8893-526X](https://orcid.org/0000-0002-8893-526X)  
Website: [https://www.paranoidcrypto.cl](https://www.paranoidcrypto.cl)

---

## 🌐 Languages / Idiomas

- [English](#english)
- [Español](#espanol)
- [Português](#portugues)

---

<a name="english"></a>
## 🇬🇧 English

### Supported Versions

| Version | Supported          |
| ------- | ------------------ |
| 2.0.x   | ✅ Supported       |
| < 2.0   | ❌ Not supported   |

### Reporting a Vulnerability

If you discover a security vulnerability in ParanoidCrypto, please help us by reporting it responsibly.

**DO NOT open a public issue** for security vulnerabilities.

#### How to report

1. **Email**: Contact the author via ORCID: [0000-0002-8893-526X](https://orcid.org/0000-0002-8893-526X)
2. **Include**:
   - Description of the vulnerability
   - Steps to reproduce
   - Potential impact
   - Suggested fix (if any)
3. **Expected response time**: 48-72 hours
4. **What to expect**:
   - Acknowledgment of your report
   - Regular updates on progress
   - Credit in the security advisory (unless you prefer to remain anonymous)

### Security Architecture

#### Client-Side Processing

ParanoidCrypto is designed with privacy as a core principle:

- ✅ **All encryption/decryption happens in the user's browser**
- ✅ **No data is sent to external servers** (except the visitor counter)
- ✅ **No backend processing** of user content
- ✅ **Secret keys never leave the user's device**
- ✅ **No cookies or tracking** of user activity

#### Cryptographic Implementation

| Component | Implementation | Notes |
|-----------|----------------|-------|
| BWT+MTF | Burrows-Wheeler Transform + Move-to-Front | Pattern hiding and compression |
| SHA-256 | Pure JavaScript | Based on FIPS 180-4 standard |
| XOR Cipher | Symmetric stream cipher | Uses SHA-256-derived keystream |
| Key derivation | SHA-256 + counter mode | Generates pseudo-random stream |
| DNA encoding | 2-bit to nucleotide mapping | 24 dictionary permutations |

#### Nucleotide Dictionaries

The application supports 24 different nucleotide mapping dictionaries:

| # | Mapping | Binary Pattern |
|---|---------|----------------|
| 1 | A T G C | 00→A, 01→T, 10→G, 11→C |
| 2 | A T C G | 00→A, 01→T, 10→C, 11→G |
| ... | ... | ... |
| 24 | C G T A | 00→C, 01→G, 10→T, 11→A |

All 24 permutations are available for selection during encryption/decryption.

#### Firebase Integration

The visitor counter uses Firebase Realtime Database:

- Only stores anonymous visit counts and visitor IDs
- No personal data is collected
- Visitor IDs are randomly generated and stored locally
- Rules must be configured properly (see below)

### Firebase Security Rules

For production use, configure these rules in your Firebase Realtime Database:

```json
{
  "rules": {
    "site_stats": {
      "total_visits": {
        ".read": true,
        ".write": true
      },
      "visitors": {
        "$visitor_id": {
          ".read": true,
          ".write": true
        }
      }
    }
  }
}
```

---
<a name="espanol"></a>
## 🇪🇸 Español

### Versiones Soportadas

| Versión | Soportada          |
| ------- | ------------------ |
| 2.0.x   | ✅ Soportada       |
| < 2.0   | ❌ No soportada    |

### Reportar una Vulnerabilidad

Si descubres una vulnerabilidad de seguridad en ParanoidCrypto, por favor ayúdanos reportándola de manera responsable.

**NO abras un issue público** para vulnerabilidades de seguridad.

#### Cómo reportar

1. **Email**: Contacta al autor vía ORCID: [0000-0002-8893-526X](https://orcid.org/0000-0002-8893-526X)
2. **Incluye**:
   - Descripción de la vulnerabilidad
   - Pasos para reproducirla
   - Impacto potencial
   - Solución sugerida (si la tienes)
3. **Tiempo de respuesta esperado**: 48-72 horas
4. **Qué esperar**:
   - Confirmación de recepción de tu reporte
   - Actualizaciones regulares del progreso
   - Crédito en el aviso de seguridad (a menos que prefieras permanecer en el anonimato)

### Arquitectura de Seguridad

#### Procesamiento del Lado del Cliente

ParanoidCrypto está diseñado con la privacidad como principio fundamental:

- ✅ **Toda la encriptación/desencriptación ocurre en el navegador del usuario**
- ✅ **No se envían datos a servidores externos** (excepto el contador de visitas)
- ✅ **Sin procesamiento backend** del contenido del usuario
- ✅ **Las claves secretas nunca salen del dispositivo del usuario**
- ✅ **Sin cookies ni rastreo** de la actividad del usuario

#### Implementación Criptográfica

| Componente         | Implementación                        | Notas                                |
| ------------------ | ------------------------------------- | ------------------------------------ |
| BWT+MTF            | Transformada de Burrows-Wheeler + Move-to-Front | Ocultamiento de patrones y compresión |
| SHA-256            | JavaScript puro                       | Basado en el estándar FIPS 180-4     |
| Cifrado XOR        | Cifrado de flujo simétrico            | Usa flujo derivado de SHA-256        |
| Derivación de clave| SHA-256 + modo contador               | Genera un flujo pseudoaleatorio      |
| Codificación de ADN| Mapeo de 2 bits a nucleótidos         | 24 permutaciones de diccionario      |

#### Diccionarios de Nucleótidos

La aplicación soporta 24 diccionarios de mapeo de nucleótidos diferentes:

| #  | Mapeo   | Patrón Binario             |
| -- | ------- | -------------------------- |
| 1  | A T G C | 00→A, 01→T, 10→G, 11→C     |
| 2  | A T C G | 00→A, 01→T, 10→C, 11→G     |
|... | ...     | ...                        |
| 24 | C G T A | 00→C, 01→G, 10→T, 11→A     |

Las 24 permutaciones están disponibles para su selección durante la encriptación/desencriptación.

#### Integración con Firebase

El contador de visitas utiliza Firebase Realtime Database:

- Solo almacena conteos de visitas anónimas e IDs de visitantes
- No se recopilan datos personales
- Los IDs de visitantes se generan aleatoriamente y se almacenan localmente
- Las reglas deben configurarse correctamente (ver abajo)

### Reglas de Seguridad de Firebase

Para uso en producción, configura estas reglas en tu Firebase Realtime Database:

```json
{
  "rules": {
    "site_stats": {
      "total_visits": {
        ".read": true,
        ".write": true
      },
      "visitors": {
        "$visitor_id": {
          ".read": true,
          ".write": true
        }
      }
    }
  }
}
```

<a name="portugues"></a>
## 🇧🇷 Português

### Versões Suportadas

| Versão  | Suportada          |
| ------- | ------------------ |
| 2.0.x   | ✅ Suportada       |
| < 2.0   | ❌ Não suportada   |

### Reportando uma Vulnerabilidade

Se você descobrir uma vulnerabilidade de segurança no ParanoidCrypto, por favor, ajude-nos reportando-a de forma responsável.

**NÃO abra um issue público** para vulnerabilidades de segurança.

#### Como reportar

1. **Email**: Entre em contato com o autor via ORCID: [0000-0002-8893-526X](https://orcid.org/0000-0002-8893-526X)
2. **Inclua**:
   - Descrição da vulnerabilidade
   - Passos para reproduzir
   - Impacto potencial
   - Correção sugerida (se houver)
3. **Tempo de resposta esperado**: 48-72 horas
4. **O que esperar**:
   - Confirmação do recebimento do seu relatório
   - Atualizações regulares do progresso
   - Crédito no aviso de segurança (a menos que prefira permanecer anônimo)

### Arquitetura de Segurança

#### Processamento do Lado do Cliente

O ParanoidCrypto é projetado com a privacidade como princípio fundamental:

- ✅ **Toda criptografia/descriptografia ocorre no navegador do usuário**
- ✅ **Nenhum dado é enviado para servidores externos** (exceto o contador de visitas)
- ✅ **Sem processamento backend** do conteúdo do usuário
- ✅ **As chaves secretas nunca saem do dispositivo do usuário**
- ✅ **Sem cookies ou rastreamento** da atividade do usuário

#### Implementação Criptográfica

| Componente         | Implementação                        | Notas                                |
| ------------------ | ------------------------------------ | ------------------------------------ |
| BWT+MTF            | Transformada de Burrows-Wheeler + Move-to-Front | Ocultação de padrões e compressão    |
| SHA-256            | JavaScript puro                      | Baseado no padrão FIPS 180-4         |
| Cifra XOR          | Cifra de fluxo simétrico             | Usa fluxo derivado de SHA-256        |
| Derivação de chave | SHA-256 + modo contador              | Gera um fluxo pseudoaleatório        |
| Codificação de DNA | Mapeamento de 2 bits para nucleotídeos | 24 permutações de dicionário         |

#### Dicionários de Nucleotídeos

A aplicação suporta 24 dicionários de mapeamento de nucleotídeos diferentes:

| #  | Mapeamento | Padrão Binário           |
| -- | ---------- | ------------------------ |
| 1  | A T G C    | 00→A, 01→T, 10→G, 11→C   |
| 2  | A T C G    | 00→A, 01→T, 10→C, 11→G   |
|... | ...        | ...                      |
| 24 | C G T A    | 00→C, 01→G, 10→T, 11→A   |

Todas as 24 permutações estão disponíveis para seleção durante a criptografia/descriptografia.

#### Integração com Firebase

O contador de visitas utiliza o Firebase Realtime Database:

- Armazena apenas contagens de visitas anônimas e IDs de visitantes
- Nenhum dado pessoal é coletado
- Os IDs de visitantes são gerados aleatoriamente e armazenados localmente
- As regras devem ser configuradas corretamente (veja abaixo)

### Regras de Segurança do Firebase

Para uso em produção, configure estas regras no seu Firebase Realtime Database:
