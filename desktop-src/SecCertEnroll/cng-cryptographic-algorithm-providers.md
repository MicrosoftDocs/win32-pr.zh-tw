---
description: 不同于密碼編譯 API (CryptoAPI) ，密碼編譯 API：新一代 (CNG) 將密碼編譯提供者與金鑰儲存提供者隔開。
ms.assetid: ce29bc97-049e-4c82-979f-4c805a318ba0
title: CNG 密碼編譯演算法提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0fd98a7eb6fd159c54977cdf8b72ebffd747da48
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467075"
---
# <a name="cng-cryptographic-algorithm-providers"></a>CNG 密碼編譯演算法提供者

不同于密碼編譯 API (CryptoAPI) ，密碼編譯 API：新一代 (CNG) 將密碼編譯提供者與金鑰儲存提供者隔開。 基本密碼編譯演算法作業（例如雜湊和簽章）稱為基本作業或單純的基本作業。 CNG 包含可執行下列演算法的提供者。

-   [對稱演算法](#symmetric-algorithms)
-   [非對稱演算法](#asymmetric-algorithms)
-   [雜湊演算法](#hashing-algorithms)
-   [金鑰 Exchange 演算法](#key-exchange-algorithms)
-   [相關主題](#related-topics)

## <a name="symmetric-algorithms"></a>對稱演算法



| Name                                   | 支援的模式                                                                                                                                                                                                 | 金鑰大小（位） (預設/最小/最大)  |
|----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------|
| 進階加密標準 (AES)     | ECB、CBC、CFB8、CFB128、GCM、CCM、GMAC、CMAC、AES 金鑰包裝、XTS<br/> **Windows 8：** CFB128 和 CMAC 模式的支援開始。<br/> **Windows 10：** 支援 XTS-AES 模式開始。<br/> | 128/192/256                        |
| 資料加密標準 (DES)          | ECB、CBC、CFB8、CFB64<br/> **Windows 8：** CFB64 模式的支援開始。<br/>                                                                                                                   | 56/56/56                           |
| 資料加密標準進行 xor (DESX)    | ECB、CBC、CFB8、CFB64 <br/> **Windows 8：** CFB64 模式的支援開始。<br/>                                                                                                                  | 192/192/192                        |
| 三重資料加密標準 (3DES)  | ECB、CBC、CFB8、CFB64 <br/> **Windows 8：** CFB64 模式的支援開始。<br/>                                                                                                                  | 112/168                            |
| RSA Data Security 2 (RC2)               | 支援 ECB、CBC、CFB8、CFB64 模式。<br/> **Windows 8：** CFB64 模式的支援開始。<br/>                                                                                              | 8位遞增的16至128      |
| RSA Data Security 4 (RC4)               |                                                                                                                                                                                                                 | 8至512，以8位遞增      |



 

## <a name="asymmetric-algorithms"></a>非對稱演算法



| 名稱                              | 注意                                                                                                                                                                             | 金鑰大小（位） (預設/最小/最大)                                                                             |
|-----------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
|  (DSA) 的數位簽章演算法 | 針對1024與3072位之間的金鑰大小，執行符合 FIPS 186-3。 <br/> 執行符合 FIPS 186-2 的金鑰大小，從512到1024位。<br/> | 512至3072，以64位遞增<br/> **Windows 8：** 3072位金鑰的支援開始。<br/> |
| RSA                               | 包含使用 PKCS1 的 RSA 演算法、優化的非對稱式加密填補 (OAEP) 編碼或填補，或概率簽章配置 (PSS) 純文字填補               | 512至16384，以64位遞增                                                                            |



 

## <a name="hashing-algorithms"></a>雜湊演算法



| 名稱                               | 注意               | 金鑰大小（位） (預設/最小/最大)  |
|------------------------------------|---------------------|------------------------------------|
| 安全雜湊演算法 1 (SHA1)      | 包含 HmacSha1   | 160/160/160                        |
| 安全雜湊演算法 256 (SHA256)  | 包含 HmacSha256 | 256/256/256                        |
| 安全雜湊演算法 384 (SHA384)  | 包含 HmacSha384 | 384/384/384                        |
| 安全雜湊演算法 512 (SHA512)  | 包含 HmacSha512 | 512/512/512                        |
| 訊息摘要 2 (MD2)              | 包含 HmacMd2    | 128/128/128                        |
| 訊息摘要 4 (MD4)              | 包含 HmacMd4    | 128/128/128                        |
| 訊息摘要 5 (MD5)              | 包含 HmacMd5    | 128/128/128                        |



 

## <a name="key-exchange-algorithms"></a>金鑰 Exchange 演算法




| 演算法名稱 | 備註 | 金鑰大小（位） (預設/最小/最大)  | 
|----------------|-------|------------------------------------|
| Diffie-Hellman 金鑰 Exchange 演算法 | 512至4096，以64位遞增 | 
|  (ECDH) 的橢圓曲線 Diffie-Hellman | 包含使用256、384和521位公開金鑰的曲線（如 SP800-56A 中所指定）。 | 256/384/521 | 
|  (ECDSA) 的橢圓曲線數位簽章演算法 | 包含使用256、384和521位公開金鑰的曲線，如 FIPS 186-3 中所指定。<blockquote>[!Note]<br />若要顯示所有命名的橢圓曲線，請使用 <strong>Certutil displayEccCurve</strong>。</blockquote><br /> | 256/384/521 | 




 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**CNG 演算法識別碼**](/windows/desktop/SecCNG/cng-algorithm-identifiers)
</dt> <dt>

[CNG 密碼編譯基本函數](/windows/desktop/SecCNG/cng-cryptographic-primitive-functions)
</dt> <dt>

[瞭解密碼編譯提供者](understanding-cryptographic-providers.md)
</dt> </dl>

 

