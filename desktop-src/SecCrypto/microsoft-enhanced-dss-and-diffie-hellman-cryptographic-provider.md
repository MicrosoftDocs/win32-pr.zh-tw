---
description: Microsoft 增強的 DSS 和 Diffie-Hellman 密碼編譯提供者支援 Diffie-Hellman 的金鑰交換、SHA 雜湊、DSA 資料簽署和驗證 (FIPS 186-2) 和 RC4 對稱式加密演算法。
ms.assetid: 90eca1e0-960f-4355-aef7-6e923100a6d8
title: Microsoft 增強式 DSS & Diffie-Hellman 密碼編譯提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 70c42b4e504c1e5d4cb8ccfea7405580e37362f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970833"
---
# <a name="microsoft-enhanced-dss--diffie-hellman-cryptographic-provider"></a>Microsoft 增強式 DSS & Diffie-Hellman 密碼編譯提供者

Microsoft 增強式 DSS 和 [*Diffie-hellman*](../secgloss/d-gly.md) 密碼編譯提供者支援 *diffie-hellman* 金鑰交換、SHA 雜湊、DSA 資料簽署和驗證 (FIPS 186-2) 和 RC4 對稱式加密演算法。

<dl> 提供者類型： **>prov \_ DSS \_ DH**  
提供者名稱： **MS \_ ENH \_ DSS \_ DH \_ >prov**  
</dl>

此密碼編譯提供者支援下列演算法。

| 演算法識別碼          | 演算法類型  | 預設大小 (位)  | Description                                                                                                                                                |
|-----------------------|-----------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **CALG \_ CYLINK \_ MEK** | 資料加密 | 40                  | CYLINK 訊息加密演算法。                                                                                                                       |
| **CALG \_ RC2**         | 資料加密 | 128                 | RSA RC2。                                                                                                                                                   |
| **CALG \_ RC4**         | 資料加密 | 128                 | RSA RC4。                                                                                                                                                   |
| **CALG \_ DES**         | 資料加密 | 56                  | 資料加密標準 (DES) 。                                                                                                                            |
| **CALG \_ 3des \_ 112**   | 資料加密 | 112                 | 兩個主要的三重 DES。                                                                                                                                        |
| **CALG \_ 3des**        | 資料加密 | 168                 | 三個主要的三重 DES。                                                                                                                                      |
| **CALG \_ SHA1**        | 雜湊            | 160                 | 安全雜湊演算法 1 (SHA-1) 。                                                                                                                           |
| **CALG \_ MD5**         | 雜湊            | 128                 | 訊息摘要 5 (MD5) 。                                                                                                                                    |
| **CALG \_ DSS \_ SIGN**   | 簽名       | 1024                |  (DSA) 的數位簽章演算法。                                                                                                                         |
| **CALG \_ DH \_ SF**      | 金鑰交換    | 1024                | 儲存和轉寄 [*diffie-hellman*](../secgloss/d-gly.md) 金鑰交換演算法。 |
| **CALG \_ DH \_ EPHEM**   | 金鑰交換    | 1024                | [*Diffie-hellman*](../secgloss/d-gly.md) 暫時演算法。                      |



 

 

 
