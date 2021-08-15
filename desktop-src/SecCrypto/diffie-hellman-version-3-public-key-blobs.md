---
description: Diffie-Hellman 第3版公開金鑰 Blob (類型 PUBLICKEYBLOB) 用來匯出和匯入 DH 公開金鑰的相關資訊。
ms.assetid: ba29a71a-7509-49c7-93d2-f0a699532706
title: Diffie-Hellman 第3版公開金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21515e370fba1c63ab3d852a88ad45b974683a3ca5ba3c3ad258733593fb6e5c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767415"
---
# <a name="diffie-hellman-version-3-public-key-blobs"></a>Diffie-Hellman 第3版公開金鑰 Blob

Diffie-Hellman 第3版 [*公開金鑰 blob*](../secgloss/p-gly.md) (類型 PUBLICKEYBLOB) 用來匯出和匯入 DH 公開金鑰的相關資訊。 它們具有下列格式：


```C++
BLOBHEADER blobheader; 
                 // As explained under "Data Structures"
DHPUBKEY_VER3 dhpubkeyver3;
BYTE p[dhpubkeyver3.bitlenP/8]; 
                 // Where P is the prime modulus
BYTE q[dhpubkeyver3.bitlenQ/8]; 
                 // Where Q is a large factor of P-1
BYTE g[dhpubkeyver3.bitlenP/8]; 
                 // Where G is the generator parameter
BYTE j[dhpubkeyver3.bitlenJ/8]; 
                 // Where J is (P-1)/Q
BYTE y[dhpubkeyver3.bitlenP/8]; 
                 // Where Y is (G^X) mod P
```



當 CRYPT \_ BLOB \_ VER3 旗標與 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)搭配使用時，會匯出此 blob 格式。 因為版本是在 BLOB 中，所以將此 [*blob*](../secgloss/b-gly.md) 與 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)搭配使用時，不需要指定旗標。

此外，當使用 *dwParam* 值 KP [](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) \_ PUB \_ 參數來設定 DH 金鑰的金鑰參數時，此 BLOB 格式會搭配 CryptSetKeyParam 函式使用。 這是在 \_ 用來產生金鑰的 CRYPT PREGEN 旗標時完成的。 在這種情況下，y 值會被忽略，因此不應該包含在 BLOB 中。

下表說明金鑰 BLOB 的每個元件。



| 欄位        | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|--------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| blobheader   | [**BLOBHEADER**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。 **BType** 成員的值必須是 PUBLICKEYBLOB。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| dhpubkeyver3 | [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3)結構。 **魔術** 成員應設定為0x33484400 的公開金鑰。 請注意，十六進位值只是 "DH3" 的 [*ASCII*](../secgloss/a-gly.md) 編碼。                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| P            | P 值是位於 [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) 結構的正後方，而且應該一律是 **DHPUBKEY \_ VER3** **bitlenP** 欄位的長度（以位元組為單位）， (位長度的 p) 除以八 ([*位元組*](../secgloss/l-gly.md) 由小到大格式) 。                                                                                                                                                                                                                                                                                                                                                                                           |
| Q            | Q 值位於 P 值的正後方，而且應該一律是 [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenQ** 欄位的長度（以位元組為單位），並以 8 (位元組由大 [*到小*](../secgloss/l-gly.md) 的格式) 。 如果 bitlenQ 值為0，則不會從 BLOB 中遺漏值。                                                                                                                                                                                                                                                                                                                                                                 |
| G            | G 值位於 Q 值的正後方，而且應該一律是 [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenP** 欄位的長度（以位元組為單位）， (位長度的 P) 除以八。 如果資料的長度是一或多個小於 P 的位元組除以8，則必須以零值的必要位元組填補資料， (零值) 讓資料變成所需的長度 (以 [*位元組*](../secgloss/l-gly.md) 由小到大格式) 。                                                                                                                                                                                                                              |
| J            | J 值會緊接在 G 值之後，且應一律為 [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenJ** 欄位的長度（以位元組為單位），並以 8 (位元組由大 [*到小*](../secgloss/l-gly.md) 的格式) 。 如果 bitlenQ 值為0，則不會從 BLOB 中遺漏值。                                                                                                                                                                                                                                                                                                                                                                 |
| Y            | Y 值（ (G ^ X) mod P）會緊接在 J 值之後，且應一律為以位元組為單位的 [**DHPUBKEY \_ VER3**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey_ver3) **bitlenP** 欄位長度（以位元組為單位）， (位長度為 P) 除以八。 如果 (G ^ X) mod P 的計算所產生的資料長度是一個或多個小於 P 除以8的位元組，則資料必須以零值 (的必要位元組填補，) 才能讓資料變成所需的長度 (位元組由小到 [*小*](../secgloss/l-gly.md) 的格式) 。 當此結構與 [**CryptSetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) 搭配使用 *dwParam* 值 KP \_ PUB 參數時 \_ ，BLOB 中不會包含此值。 |



 

> [!Note]  
> 公開金鑰 Blob 未加密，但包含純文字格式的公開金鑰。

 

 

 
