---
description: Blob 可與 Diffie-Hellman 提供者一起使用，以在密碼編譯服務提供者 (CSP) 中匯出和匯入金鑰。
ms.assetid: 052f2108-d402-41a0-b4ac-e93ba6b06b49
title: Diffie-Hellman 金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e8e993daf5b9ec0509ae6fa01df4edc06bafec733bb80f7b014921026fbc35ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117767712"
---
# <a name="diffie-hellman-key-blobs"></a>Diffie-Hellman 金鑰 Blob

[*Blob*](../secgloss/b-gly.md) 可搭配 [*diffie-hellman*](../secgloss/d-gly.md) 提供者使用，以從 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 中匯出和匯入金鑰。

-   [公開金鑰 Blob](#public-key-blobs)
-   [私密金鑰 Blob](#private-key-blobs)

## <a name="public-key-blobs"></a>公開金鑰 Blob

Diffie-Hellman 的 [*公開金鑰 blob*](../secgloss/p-gly.md)（輸入 **PUBLICKEYBLOB**）是用來交換 Diffie-Hellman 金鑰交換中的 (G ^ X) mod P 值。 這些金鑰會以下列格式匯出並匯入為一連串的位元組。

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY dhpubkey;
BYTE y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

下表說明 [*金鑰 BLOB*](../secgloss/k-gly.md)的每個元件。



| 欄位          | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey)結構。 **魔術** 成員應設定為0x31484400。 此十六進位值是 "DH1" 的 [*ASCII*](../secgloss/a-gly.md) 編碼。                                                                                                                                                                                                                                                                                                                                                                 |
| publickeystruc | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          |
| y              | **位元組** 序列。 Y 值（ (G ^ X) mod P）位於 [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) 結構的正後方，而且應該一律是 **DHPUBKEY bitlen** 欄位的長度（以位元組為單位）， (位長度 P) 除以八。 如果 (G ^ X) mod P 的計算所產生的資料長度是一個或多個小於 P 除以八的位元組，則資料必須以零值 (的必要位元組填補，) 才能讓資料變成所需的長度 (位元組由小到 [*小*](../secgloss/l-gly.md) 的格式) 。 |



 

## <a name="private-key-blobs"></a>私密金鑰 Blob

Diffie-Hellman 的 [*私密金鑰 blob*](../secgloss/p-gly.md)（輸入 **PRI加值稅EKEYBLOB**）是用來儲存 Diffie-Hellman 金鑰的公開/私用資訊。 這些金鑰會以下列格式匯出並匯入為一連串的位元組。

``` syntax
PUBLICKEYSTRUC  publickeystruc; 
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

下表說明金鑰 BLOB 的每個元件。



| 欄位          | 描述                                                                                                                                                                                                  |
|----------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey)結構。 **魔術** 成員必須設為0x32484400。 此十六進位值是 "DH2" 的 [*ASCII*](../secgloss/a-gly.md) 編碼。 |
| 產生器      | **位元組** 序列。 發電機，G。                                                                                                                                                                       |
| publickeystruc | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                        |
| 主要          | **位元組** 序列。 質數模數 P。這項資料必須一律將最重要的位元組數設定為一。                                                                      |
| secret         | **位元組** 序列。 秘密指數 X。                                                                                                                                                                 |



 

> [!Note]  
> 產生器和密碼必須一律具有相同的長度（以位元組為單位）。 如果其中一個位元組比另一個位元組更短，則必須以零值位元組的數位填補，使其相同。 產生器和密碼都是以 [*位元組*](../secgloss/l-gly.md) 由小到大的格式。

 

 

 
