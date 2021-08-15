---
description: Blob 可與 RSA/安全通道提供者搭配使用，以將金鑰從密碼編譯服務提供者匯出，並將金鑰匯入 (CSP) 。
ms.assetid: 97d5ee6d-4687-4cd2-b122-36f8ea3c93ca
title: RSA/Schannel 金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3be8bfa8b87ee901317e220583ff7b08ea110e342a2d9dd9abb477053ffdf05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118900533"
---
# <a name="rsaschannel-key-blobs"></a>RSA/Schannel 金鑰 Blob

[*Blob*](../secgloss/b-gly.md)可與 [*RSA*](../secgloss/r-gly.md)安全通道提供者搭配使用， / [](../secgloss/s-gly.md)以在 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 中匯出和匯入金鑰。

-   [公開金鑰 Blob](#public-key-blobs)
-   [私密金鑰 Blob](#private-key-blobs)
-   [簡單的金鑰 Blob](#simple-key-blobs)

## <a name="public-key-blobs"></a>公開金鑰 Blob

[*公開金鑰 blob*](../secgloss/p-gly.md)（類型 **PUBLICKEYBLOB**）是用來儲存 [*公開金鑰*](../secgloss/p-gly.md)。 這些金鑰會以下列格式匯出並匯入為一連串的位元組。

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
```

下表描述每個公開金鑰元件。 所有值都是以 [*位元組*](../secgloss/l-gly.md) 由小到大的格式。



| 欄位          | 描述                                                                                                                                                                                                                                                                                        |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 模數        | **位元組** 序列。 公開金鑰模數資料位於 **RSAPUBKEY** 結構的正後方。 這項資料的長度會隨著公開金鑰的長度而有所不同。 您可以藉由將 **RSAPUBKEY** 的 **bitlen** 成員值除以八來判斷位元組數目。 |
| publickeystruc | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                                                                                                              |
| rsapubkey      | [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey)結構。 **魔術** 成員必須設為0x31415352。 此十六進位值是 RSA1 的 [*ASCII*](../secgloss/a-gly.md) 編碼。                                                                                      |



 

> [!Note]  
> 公開金鑰 Blob 未加密。 它們包含 [*純文字*](../secgloss/p-gly.md) 格式的公開金鑰。

 

## <a name="private-key-blobs"></a>私密金鑰 Blob

[*私用金鑰 blob*](../secgloss/p-gly.md)（類型 **PRI加值稅EKEYBLOB**）是用來儲存 [*公開/私密金鑰*](../secgloss/p-gly.md)組。 這些金鑰會以下列格式匯出並匯入為一連串的位元組。

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
RSAPUBKEY       rsapubkey;
BYTE            modulus[rsapubkey.bitlen/8];
BYTE            prime1[rsapubkey.bitlen/16];
BYTE            prime2[rsapubkey.bitlen/16];
BYTE            exponent1[rsapubkey.bitlen/16];
BYTE            exponent2[rsapubkey.bitlen/16];
BYTE            coefficient[rsapubkey.bitlen/16];
BYTE            privateExponent[rsapubkey.bitlen/8];
```

如果 [*金鑰 blob*](../secgloss/k-gly.md) 已加密，則 Blob 的 [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) 部分都會加密，但不會加密。

> [!Note]  
> 加密演算法和加密金鑰參數不會與私密金鑰 BLOB 一起儲存。 應用程式必須負責管理這項資訊。

 

下表說明每個私密金鑰 BLOB 元件。

> [!Note]  
> 這些欄位會對應到 [*公開金鑰加密標準*](../secgloss/p-gly.md) 的7.2 章節中所述的欄位 (PKCS) \# 1，但有些許差異。

 



| 欄位           | 描述                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| exponent1       | **位元組** 序列。 第一個指數。 此值的數值為 d mod (p – 1) 。                                                                                                                           |
| exponent2       | **位元組** 序列。 第二個指數。 此值的數值為 d mod (q – 1) 。                                                                                                                          |
| 係數     | **位元組** 序列。 係數。 此值為 q) mod p (反向的數值。                                                                                                                           |
| 模組         | **位元組** 序列。 模數。 這包含包含 *Prime1* \* *Prime2* 的字串。 它通常稱為 n。                                                                                               |
| prime1          | **位元組** 序列。 質數1，通常稱為 p。                                                                                                                                                        |
| prime2          | **位元組** 序列。 質數2，通常稱為 q。                                                                                                                                                        |
| publickeystruc  | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                         |
| privateExponent | **位元組** 序列。 私用指數，通常稱為 d。                                                                                                                                                  |
| rsapubkey       | [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey)結構。 **魔術** 成員必須設為0x32415352。 此十六進位值是 RSA2 的 [*ASCII*](../secgloss/a-gly.md) 編碼。 |



 

> [!Note]  
> 私密金鑰 Blob 未加密。 它們包含純文字格式的私密金鑰。

 

呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)時，開發人員可以選擇是否要加密金鑰。 如果 *hExpKey* 參數包含工作階段金鑰的有效控制碼，就會加密 **PRI加值稅EKEYBLOB** 。 但 BLOB 的 [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) 部分都會加密。

> [!Note]  
> 加密演算法和加密金鑰參數不會與私密金鑰 BLOB 一起儲存。 應用程式必須管理和儲存此資訊。 如果傳遞給 *hExpKey* 的值為零，將會匯出私密金鑰而不加密。

 

> [!Caution]  
> 匯出私密金鑰而不加密是很危險的，因為這些金鑰接著很容易被未經授權的實體攔截及使用。

 

## <a name="simple-key-blobs"></a>簡單的金鑰 Blob

[*簡單的金鑰 blob*](../secgloss/s-gly.md)（類型 **SIMPLEBLOB**）是用來儲存和傳輸工作階段金鑰。 這些一律會以 [*金鑰交換公開金鑰*](../secgloss/k-gly.md)加密。 這些金鑰會以下列格式匯出並匯入為一連串的位元組。

``` syntax
PUBLICKEYSTRUC  publickeystruc ;
ALG_ID          algid;
BYTE            encryptedkey[rsapubkey.bitlen/8];
```

下表說明每個簡單的 BLOB 元件。



| 欄位          | 描述                                                                                                                                                                                                                                                                                                                   |
|----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | [**ALG \_ 識別碼**](alg-id.md)結構。 這通常會指定 CALG \_ RSA \_ KEYX 演算法，這表示使用 [*rsa 公開金鑰演算法*](../secgloss/r-gly.md)，以金鑰交換公開金鑰來加密工作階段金鑰資料。 |
| encryptedkey   | **位元組** 序列。 加密工作階段金鑰資料的格式為 PKCS \# 1，type 2 encryption block。 如需此資料格式的相關資訊，請參閱 RSA Data Security，Inc. 發行的公開金鑰加密標準 (PKCS) 。                                                                                     |
| publickeystruc | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                                                                                                                                         |



 

這項資料的大小一律與公開金鑰的模數相同。 例如，Microsoft 基礎密碼編譯提供者所產生的公開金鑰一律為512位 (64 位元組) 長度，因此加密的工作階段金鑰資料也一律為64個位元組。

 

 
