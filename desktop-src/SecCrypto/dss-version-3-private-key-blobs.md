---
description: 描述匯出的 DSS 第3版私密金鑰的格式。
ms.assetid: 650532fd-919b-495a-9fb9-981790447d3d
title: DSS 第3版私密金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a6434e411ba3268901176a5c9739ceecfa79689
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192741"
---
# <a name="dss-version-3-private-key-blobs"></a>DSS 第3版私密金鑰 Blob

匯出第3版 [*DSS*](../secgloss/d-gly.md) [*私密金鑰*](../secgloss/p-gly.md) 時，其格式如下：


```C++
BLOBHEADER        blobheader; 
DSSPRIVKEY_VER3   dssprivkeyver3;
BYTE p[dssprivkeyver3.bitlenP/8]; 
                    // Where P is the prime modulus
BYTE q[dssprivkeyver3.bitlenQ/8]; 
                    // Where Q is a large factor of P-1
BYTE g[dssprivkeyver3.bitlenP/8]; 
                    // Where G is the generator parameter
BYTE j[dssprivkeyver3.bitlenJ/8]; 
                    // Where J is (P-1)/Q
BYTE y[dssprivkeyver3.bitlenP/8]; 
                    // Where Y is (G^X) mod P
BYTE x[dssprivkeyver3.bitlenX/8]; 
                    // Where X is the private exponent
```



當 [](../secgloss/b-gly.md) CRYPT \_ BLOB \_ VER3 旗標與 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)搭配使用時，會匯出此 blob 格式。 因為版本是在 BLOB 中，所以將此 BLOB 與 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)搭配使用時，不需要指定旗標。

下表說明 [*金鑰 BLOB*](../secgloss/k-gly.md)的每個元件。



| 欄位          | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Blobheader     | [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。 **BType** 成員的值必須是 PUBLICKEYBLOB。                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Dssprivkeyver3 | **DSSPRIVKEY \_ VER3** 結構。 **魔術** 成員應設定為 "DSS4"， (0x34535344) 做為私用金鑰。 請注意，十六進位值只是 "DSS4" 的 [*ASCII*](../secgloss/a-gly.md) 編碼。<br/>                                                                                                                                                                                                                                                                     |
| P              | P 值是位於 **DSSPRIVKEY \_ VER3** 結構的正後方，而且應該一律是 **DSSPRIVKEY \_ VER3 bitlenP** 欄位的長度（以位元組為單位）， (位長度的 p) 除以八 ([*位元組由小到小*](../secgloss/l-gly.md) 的格式) 。                                                                                                                                                                                                                           |
| Q              | Q 值位於 P 值的正後方，而且應該一律是 **DSSPRIVKEY \_ VER3 bitlenQ** 欄位的長度（以位元組為單位），並以 8 (位元組由大到 [*小*](../secgloss/l-gly.md) 的格式) 。                                                                                                                                                                                                                                                                     |
| G              | G 值位於 Q 值的正後方，而且應該一律是 **DSSPRIVKEY \_ VER3 bitlenP** 欄位的長度（以位元組為單位）， (位長度的 P) 除以八。 如果資料的長度是一或多個小於 P 的位元組除以8，則必須以零值的必要位元組填補資料， (零值) 讓資料變成所需的長度 (以 [*位元組*](../secgloss/l-gly.md) 由小到大格式) 。                                                                 |
| J              | J 值會緊接在 G 值之後，且應一律為 **DSSPRIVKEY \_ VER3 bitlenJ** 欄位的長度（以位元組為單位），並以 8 (位元組由大到 [*小*](../secgloss/l-gly.md) 的格式) 。 如果 bitlenJ 值為0，則不會從 BLOB 中遺漏值。                                                                                                                                                                                                   |
| Y              | Y 值（ (G ^ X) mod P）位在 J 值的正後方，而且應該一律是 **DSSPRIVKEY \_ VER3 bitlenP** 欄位的長度（以位元組為單位）， (位長度 P) 除以八。 如果 (G ^ X) mod P 的計算所產生的資料長度是一個或多個小於 P 除以8的位元組，則資料必須以零值 (的必要位元組填補，) 才能讓資料變成所需的長度 (位元組由小到 [*小*](../secgloss/l-gly.md) 的格式) 。 |
| X              | X 值是隨機的大型整數，因此 DH 金鑰組（Y）的公開部分等於： Y = (G ^ X) mod P<br/>                                                                                                                                                                                                                                                                                                                                                                                               |



 

呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)時，開發人員可以選擇是否要加密金鑰。 如果 *hExpKey* 參數包含工作階段金鑰的有效控制碼，就會將金鑰加密。 但 BLOB 的 [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) 部分都會加密。 請注意，加密演算法和加密金鑰參數不會與 [*私密金鑰 BLOB*](../secgloss/p-gly.md)一起儲存。 應用程式必須管理和儲存此資訊。 如果傳遞給 *hExpKey* 的值為零，將會匯出私密金鑰而不加密。

> [!IMPORTANT]
> 匯出私密金鑰而不加密是很危險的，因為這些金鑰接著很容易被未經授權的實體攔截及使用。

 

 

 
