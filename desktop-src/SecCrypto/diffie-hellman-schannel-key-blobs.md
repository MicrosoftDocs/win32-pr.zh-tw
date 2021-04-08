---
description: Blob 可搭配 Diffie-hellman/安全通道提供者使用，以在密碼編譯服務提供者 (CSP) 中匯出和匯入金鑰。
ms.assetid: ebb85b7c-204d-4b1c-86dc-5a03c8eda47b
title: Diffie-hellman/Schannel 金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 65a76869c6c6239e17a5ae14921805a076c9381c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692999"
---
# <a name="diffie-hellmanschannel-key-blobs"></a>Diffie-hellman/Schannel 金鑰 Blob

[*Blob*](../secgloss/b-gly.md)可搭配 [*diffie-hellman*](../secgloss/d-gly.md)安全通道提供者使用，以將金鑰 / [](../secgloss/s-gly.md)從 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 中匯出和匯入。

-   [公開金鑰 Blob](#public-key-blobs)
-   [私密金鑰 Blob](#private-key-blobs)

## <a name="public-key-blobs"></a>公開金鑰 Blob

Diffie-Hellman 的 [*公開金鑰 blob*](../secgloss/p-gly.md)（輸入 **PUBLICKEYBLOB**）是用來交換 Diffie-Hellman 金鑰交換中的 (G ^ X) mod P 值。 這些金鑰會以下列格式匯出並匯入為一連串的位元組。

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            y[dhpubkey.bitlen/8]; // Where y = (G^X) mod P
```

下表說明 [*金鑰 BLOB*](../secgloss/k-gly.md)的每個元件。



| 欄位          | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey)結構。 **魔術** 成員必須設為0x31484400。 此十六進位值是 DH1 的 [*ASCII*](../secgloss/a-gly.md) 編碼。                                                                                                                                                                                                                                                                                                                                                      |
| publickeystruc | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| y              | **位元組** 序列。 Y 值（ (G ^ X) mod P）位於 [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey) 結構的正上方。 順序的長度（以位元組為單位）是 **DHPUBKEY** 除以八的 **bitlen** 成員。 如果 (G ^ X) mod P 的計算所產生的資料長度是一個或多個小於 P 除以八的位元組，則資料必須以零值 (的必要位元組填補，) 才能讓資料變成所需的長度 (位元組由小到 [*小*](../secgloss/l-gly.md) 的格式) 。 |



 

## <a name="private-key-blobs"></a>私密金鑰 Blob

D-H [*私用金鑰 blob*](../secgloss/p-gly.md)（輸入 **PRI加值稅EKEYBLOB**）是用來匯出和匯入 d-h 金鑰的私用資訊。 這些金鑰會以下列格式匯出並匯入為一連串的位元組。

``` syntax
PUBLICKEYSTRUC  publickeystruc;
DHPUBKEY        dhpubkey;
BYTE            prime[dhpubkey.bitlen/8];
BYTE            generator[dhpubkey.bitlen/8];
BYTE            secret[dhpubkey.bitlen/8];
```

下表說明金鑰 BLOB 的每個元件。



| 欄位          | 描述                                                                                                                                                                                                |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dhpubkey       | [**DHPUBKEY**](/windows/win32/api/wincrypt/ns-wincrypt-dhpubkey)結構。 **魔術** 成員必須設為0x32484400。 此十六進位值是 DH2 的 [*ASCII*](../secgloss/a-gly.md) 編碼。 |
| 產生器      | **位元組** 序列。 產生器 G。                                                                                                                                                                      |
| publickeystruc | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                      |
| 主要          | **位元組** 序列。 質數模數 P。這項資料必須一律將最重要的位元組數設定為一。                                                                    |
| secret         | **位元組** 序列。 秘密指數 X。                                                                                                                                                                |



 

> [!Note]  
> 質數、產生器和秘密值的長度必須一律相同（以位元組為單位）。 如果任何值是一個或更短的值，則必須以所需的零位元組數目填補，使其相同。 質數、產生器和秘密的格式為 [*位元組*](../secgloss/l-gly.md) 由小到大。

 

 

 
