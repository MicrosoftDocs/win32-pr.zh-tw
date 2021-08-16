---
description: 基底提供者、強式提供者和增強型提供者都使用相同的金鑰 Blob。
ms.assetid: f1bd347b-33bd-40bc-9a9b-c06f264f1af4
title: 增強的提供者金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1098ec45f73183f31cb91d15e2957dcc5964591bd8c6de4e30616df0808ade6b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874438"
---
# <a name="enhanced-provider-key-blobs"></a>增強的提供者金鑰 Blob

基底提供者、強式提供者和增強型提供者都使用相同的 [*金鑰 blob*](../secgloss/k-gly.md)。

-   [公開金鑰 Blob](#public-key-blobs)
-   [私密金鑰 Blob](#private-key-blobs)
-   [簡單的金鑰 Blob](#simple-key-blobs)

## <a name="public-key-blobs"></a>公開金鑰 Blob

[*公開金鑰 blob*](../secgloss/p-gly.md)（類型 **PUBLICKEYBLOB**）是用來將 [*公開金鑰*](../secgloss/p-gly.md) 儲存在 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 之外。 擴充提供者的公開金鑰 Blob 具有下列格式。

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
```

下表描述每個公開金鑰元件。 所有值都是以 [*位元組*](../secgloss/l-gly.md) 由小到大的格式。



| 欄位          | 描述                                                                                                                                                                                                                                                                           |
|----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 模數        | 公開金鑰模數資料位於 [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey) 結構的正後方。 這項資料的大小會因公開金鑰的大小而有所不同。 您可以將 **RSAPUBKEY bitlen** 欄位的值除以八來判斷位元組數目。 |
| publickeystruc | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                                                                                                 |
| rsapubkey      | [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey)結構。 **魔術** 成員必須設為0x31415352。 此十六進位值是 RSA1 的 [*ASCII*](../secgloss/a-gly.md) 編碼。                                                                         |



 

> [!Note]  
> 公開金鑰 Blob 未加密。 它們包含 [*純文字*](../secgloss/p-gly.md) 格式的公開金鑰。

 

## <a name="private-key-blobs"></a>私密金鑰 Blob

[*私用金鑰 blob*](../secgloss/p-gly.md)（類型 **PRI加值稅EKEYBLOB**）是用來將 [*私密金鑰*](../secgloss/p-gly.md) 儲存在 CSP 外部。 擴充提供者的私密金鑰 Blob 具有下列格式。

``` syntax
PUBLICKEYSTRUC  publickeystruc;
RSAPUBKEY rsapubkey;
BYTE modulus[rsapubkey.bitlen/8];
BYTE prime1[rsapubkey.bitlen/16];
BYTE prime2[rsapubkey.bitlen/16];
BYTE exponent1[rsapubkey.bitlen/16];
BYTE exponent2[rsapubkey.bitlen/16];
BYTE coefficient[rsapubkey.bitlen/16];
BYTE privateExponent[rsapubkey.bitlen/8];
```

下表描述私密金鑰 BLOB 元件。

> [!Note]  
> 這些欄位會對應到 [*公開金鑰加密標準*](../secgloss/p-gly.md) 的7.2 章節中所述的欄位 (PKCS) \# 1，但有些許差異。

 



| 欄位           | 描述                                                                                                                                                                                                   |
|-----------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 係數     | 係數。 此值為 q) mod p (反向的數值。                                                                                                                                                |
| exponent1       | 指數1。 此值的數值為 d mod (p – 1) 。                                                                                                                                                        |
| exponent2       | 指數2。 此值的數值為 d mod (q – 1) 。                                                                                                                                                        |
| 模組         | 模數。 這具有 *Prime1*×*Prime2* 的值，通常稱為 n。                                                                                                                                   |
| prime1          | 質數1，通常稱為 p。                                                                                                                                                                             |
| prime2          | 質數2，通常稱為 q。                                                                                                                                                                             |
| privateExponent | 私用指數，通常稱為 d。                                                                                                                                                                           |
| publickeystruc  | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                         |
| rsapubkey       | [**RSAPUBKEY**](/windows/desktop/api/Wincrypt/ns-wincrypt-rsapubkey)結構。 **魔術** 成員必須設為0x32415352。 此十六進位值是 RSA2 的 [*ASCII*](../secgloss/a-gly.md) 編碼。 |



 

> [!Note]  
> 私密金鑰 Blob 未加密。 它們包含純文字格式的私密金鑰。

 

呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)時，開發人員可以選擇是否要加密金鑰。 如果 *hExpKey* 參數包含工作階段金鑰的有效控制碼，就會加密 **PRI加值稅EKEYBLOB** 。 但 BLOB 的 [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) 部分都會加密。

> [!Note]  
> 加密演算法和加密金鑰參數不會與私密金鑰 BLOB 一起儲存。 應用程式必須管理和儲存此資訊。 如果傳遞給 *hExpKey* 的值為零，將會匯出私密金鑰而不加密。

 

> [!Caution]  
> 匯出私密金鑰而不加密是很危險的，因為這些金鑰接著很容易被未經授權的實體攔截及使用。

 

## <a name="simple-key-blobs"></a>簡單的金鑰 Blob

[*簡單的金鑰 blob*](../secgloss/s-gly.md)（類型 **SIMPLEBLOB**）是用來儲存和傳輸 CSP 外部的工作階段金鑰。 擴充提供者簡單金鑰 Blob 一律會以 [*金鑰交換公開金鑰*](../secgloss/k-gly.md)加密。 **SIMPLEBLOB** 的 **>pbdata** 成員是採用下列格式的位元組序列。

``` syntax
PUBLICKEYSTRUC  publickeystruc;
ALG_ID algid;
BYTE encryptedkey[rsapubkey.bitlen/8];
```

下表說明 **SIMPLEBLOB** 之 **>pbdata** 成員的每個元件。



| 欄位          | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| algid          | [**ALG \_ 識別碼**](alg-id.md)結構，指定用來加密工作階段金鑰資料的加密演算法。 這通常是 CALG \_ RSA KEYX 的值 \_ ，這表示已使用 [*rsa 公開金鑰演算法*](../secgloss/r-gly.md)，以金鑰交換公開金鑰來加密工作階段金鑰資料。                                                                                                                           |
| encryptedkey   | **位元組** 序列，代表加密工作階段金鑰資料（格式為 PKCS \# 1），類型2加密區塊。 如需此資料格式的相關資訊，請參閱 \# RSA Data Security，inc. 發行的公開金鑰加密標準 (PKCS) 1。這項資料的大小一律與公開金鑰的模數相同。 例如，Microsoft RSA 基底提供者所產生的公開金鑰可能是512位 (64 個位元組) 長度，因此加密的工作階段金鑰資料也一律為512位 (64 位元組) 。<br/> |
| publickeystruc | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |



 

如需基底提供者和擴充的提供者金鑰 Blob 的相關資訊，請參閱 [基底提供者金鑰 blob](base-provider-key-blobs.md)。

 

 
