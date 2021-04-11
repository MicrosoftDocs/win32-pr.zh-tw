---
description: 摘要存取挑戰的大小必須小於2048個位元組。
ms.assetid: 16c6728a-966b-436f-902d-3e12368986b6
title: 摘要挑戰的內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97f90dd78ae28536f6e2d07882f69335975df14d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112200"
---
# <a name="contents-of-a-digest-challenge"></a>摘要挑戰的內容

摘要存取挑戰的大小必須小於2048個位元組。 下列範例顯示指派給 szChallenge 字元字串的挑戰。


```C++
szChallenge = "realm=\"Microsoft_Example_Forest\",";
algorithm = "MD5-sess\", qop=\"auth\", nonce=\"0123456789abcdef\"";
```



> [!Note]  
> 挑戰字串會以雙引號括住，且包含內嵌的雙引號。 內嵌的雙引號前面必須加上 ( () 的反斜線) \\ 。

 

摘要挑戰可以包含下列指示詞。



| 指示詞         | Description                                                                                                                                                                                                                                                                                            |
|-------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| realm             | 對用戶端所需之 [*認證*](/windows/desktop/SecGloss/c-gly) 的執行定義提示。 如果使用者提示輸入認證，用戶端應該向使用者顯示此資訊。                                                  |
| 演算法         | Microsoft Digest 支援 MD5 和 MD5 Ses 之始。 為了達到最佳效能，請使用 MD5-Ses 之始。                                                                                                                                                                                                                     |
| qop               | 這個指示詞可以設定為 auth、auth-int 或 auth。 如需詳細資訊，請參閱 [保護品質和密碼](quality-of-protection-and-ciphers.md)。                                                                                                                                       |
| nonce             | 伺服器為每個挑戰產生的唯一編碼值。 用戶端不得變更此值。                                                                                                                                                                                       |
| 不透明            | 包含正在建立之 [*安全性內容*](/windows/desktop/SecGloss/s-gly) 的參考。 如需詳細資訊，請參閱 [維護連接之間的安全性內容](maintaining-the-security-context-between-connections.md)。 |
| 只有) 的加密 (SASL | 伺服器支援的密碼清單。 只有在 qop 指示詞指定驗證人員時，此專案才可以存在於 Digest SASL 挑戰中。 如需詳細資訊，請參閱 [保護品質和密碼](quality-of-protection-and-ciphers.md)。                                              |
| 字元集           | 如果伺服器可以處理 UTF-8 編碼的使用者名稱和領域，則可以將這個指示詞設定為 utf-8。 如果用戶端瞭解字元集指示詞，則可以使用 UTF-8 編碼的值來回應。                                                                                                       |



 

Microsoft Digest 會為伺服器應用程式產生摘要挑戰字串。 如需詳細資訊，請參閱 [產生摘要挑戰](generating-the-digest-challenge.md)。

 

 
