---
description: 列出 Microsoft 提供的密碼編譯服務提供者。
ms.assetid: 1461914e-5506-4f24-97da-3d2148aafd1c
title: Microsoft 密碼編譯服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 294d00660cbfa89c6113e6e9fcf2600b2f745e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000075"
---
# <a name="microsoft-cryptographic-service-providers"></a>Microsoft 密碼編譯服務提供者

下列 (CSP) 的 [*加密服務提供者*](../secgloss/c-gly.md) 目前可從 Microsoft 取得。



| 提供者                                                                                                                                 | 描述                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Microsoft 基礎密碼編譯提供者](microsoft-base-cryptographic-provider.md)                                                       | 一組廣泛的基本密碼編譯功能，可匯出至其他國家或地區。                                                                                                                                                     |
| [Microsoft 強式密碼編譯提供者](microsoft-strong-cryptographic-provider.md)                                                   | 適用于 Windows XP 及更新版本的 Microsoft 基礎密碼編譯提供者延伸模組。                                                                                                                                                           |
| [Microsoft 增強型密碼編譯提供者](microsoft-enhanced-cryptographic-provider.md)                                               | 使用較長的金鑰和其他演算法的 Microsoft 基礎密碼編譯提供者。                                                                                                                                                                |
| [Microsoft AES 密碼編譯提供者](microsoft-aes-cryptographic-provider.md)                                                         | Microsoft 增強型密碼編譯提供者，支援 AES 加密演算法。                                                                                                                                                                    |
| [Microsoft DSS 密碼編譯提供者](microsoft-dss-cryptographic-provider.md)                                                         | 使用安全雜湊演算法 ([*SHA*](../secgloss/s-gly.md)) 和數位簽章標準 (DSS) 演算法，提供雜湊、資料簽章和簽章驗證功能。 |
| [Microsoft 基底 DSS 和 Diffie-Hellman 密碼編譯提供者](microsoft-base-dss-and-diffie-hellman-cryptographic-provider.md)         | DSS 密碼編譯提供者的超集合，也支援使用安全雜湊演算法的 Diffie-Hellman 金鑰交換、雜湊、資料簽署和簽章驗證， (SHA) 和數位簽章標準 (DSS) 演算法。                    |
| [Microsoft 增強的 DSS 和 Diffie-Hellman 密碼編譯提供者](microsoft-enhanced-dss-and-diffie-hellman-cryptographic-provider.md) | 支援 Diffie-Hellman 金鑰交換 (40 位 DES 衍生) 、SHA 雜湊、DSS 資料簽署和 DSS 簽章驗證。                                                                                                                           |
| [Microsoft DSS 和 Diffie-hellman/Schannel 密碼編譯提供者](microsoft-dss-and-diffie-hellman-schannel-cryptographic-provider.md) | 支援雜湊、資料簽署與 DSS、產生 Diffie-Hellman (D-H) 金鑰、交換 D-H 金鑰，以及匯出 D-H 金鑰。 此 CSP 支援 SSL3 和 TLS1 通訊協定的金鑰衍生。                                                           |
| [Microsoft RSA/Schannel 密碼編譯提供者](microsoft-rsa-schannel-cryptographic-provider.md)                                       | 支援雜湊、資料簽章和簽章驗證。 演算法識別碼 CALG \_ SSL3 \_ SHAMD5 用於 SSL 3.0 和 TLS 1.0 用戶端驗證。 此 CSP 支援 SSL2、PCT1、SSL3 和 TLS1 通訊協定的金鑰衍生。             |
| [Microsoft RSA 簽名密碼編譯提供者](microsoft-rsa-signature-cryptographic-provider.md)                                     | 提供資料簽署和簽章驗證。                                                                                                                                                                                                        |



 

 

 
