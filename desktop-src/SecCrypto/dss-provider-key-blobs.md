---
description: 與數位簽章標準 (DSS) 提供者一起使用，可在密碼編譯服務提供者 (CSP) 中匯出和匯入金鑰。
ms.assetid: a0a266ef-0830-4a3f-9bf6-6b64c95c3d03
title: DSS 提供者金鑰 Blob
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f27a73e35cccd6fad672f4c94d589d754f970c0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943334"
---
# <a name="dss-provider-key-blobs"></a>DSS 提供者金鑰 Blob

[*Blob*](../secgloss/b-gly.md) 可與 [*數位簽章標準*](../secgloss/d-gly.md) (DSS) 提供者一起使用，以在 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 中匯出和匯入金鑰。

-   [公開金鑰 Blob](#public-key-blobs)
-   [私密金鑰 Blob](#private-key-blobs)

## <a name="public-key-blobs"></a>公開金鑰 Blob

DSS [*公開金鑰*](../secgloss/p-gly.md) 會匯出並匯入為 BLOB，這是一系列結構如下的位元組。

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              y[dsspubkey.bitlen/8];
DSSSEED           seedstruct;
```

下表描述這些元件。 所有值都是以 [*位元組*](../secgloss/l-gly.md) 由小到大的格式。



| 欄位          | 描述                                                                                                                                                                                                          |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85))結構。 **魔術** 成員的值必須是0x31535344。 此十六進位數位是 DSS1 的 [*ASCII*](../secgloss/a-gly.md) 編碼。 |
| g              | **位元組** 序列。 發電機，g。 必須與 p 的長度相同。 如果與 p 的長度不同，則必須以0x00 位元組填補。                                                                      |
| p              | **位元組** 序列。 質數模數 p。 最重要的位元組中最重要的位必須設定為一個。                                                                                                 |
| publickeystruc | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                                |
| q              | **位元組** 序列。 質數、q、20位元組的長度。 最重要的位元組中最重要的位必須設定為一個。                                                                                     |
| seedstruct     | [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed)結構。 用於驗證質數的種子和計數器值。                                                                                                                                |
| y              | **位元組** 序列。 公開金鑰，y。 的長度必須與 p 相同。 如果與 p 的長度不同，則必須以0x00 位元組填補。                                                                         |



 

> [!Note]  
> [*公開金鑰 blob*](../secgloss/p-gly.md) 未加密。 它們包含 [*純文字*](../secgloss/p-gly.md) 格式的公開金鑰。

 

## <a name="private-key-blobs"></a>私密金鑰 Blob

DSS [*私密金鑰*](../secgloss/p-gly.md) 會以位元組順序匯出和匯入，如下所示。

``` syntax
PUBLICKEYSTRUC    publickeystruc;
DSSPUBKEY         dsspubkey;
BYTE              p[dsspubkey.bitlen/8];
BYTE              q[20];
BYTE              g[dsspubkey.bitlen/8];
BYTE              x[20];
DSSSEED           seedstruct;
```

下表說明每個元件。 所有值都是以 [*位元組*](../secgloss/l-gly.md) 由小到大的格式。



| 欄位          | 描述                                                                                                                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dsspubkey      | [**DSSPUBKEY**](/previous-versions/windows/desktop/legacy/aa381982(v=vs.85))結構。 **魔術** 成員必須設為0x32535344。 此十六進位數位是 DSS2 的 [*ASCII*](../secgloss/a-gly.md) 編碼。 |
| g              | **位元組** 序列。 發電機，g。 必須與 p 的長度相同。 如果與 p 的長度不同，則必須以0x00 位元組填補。                                                                |
| publickeystruc | [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc)結構。                                                                                                                                                          |
| p              | **位元組** 序列。 質數模數 p。 最重要的位元組中最重要的位必須設定為一個。                                                                                           |
| q              | **位元組** 序列。 質數、q。 q 的長度是20個位元組。 最重要的位元組中最重要的位必須設定為一個。                                                                          |
| seedstruct     | [**DSSSEED**](/windows/desktop/api/Wincrypt/ns-wincrypt-dssseed)結構。 用於驗證質數的種子和計數器值。                                                                                                                          |
| x              | **位元組** 序列。 秘密指數 x。 必須一律為20個位元組的長度。 如果 x 的長度小於20個位元組，則必須以0x00 填補。                                                     |



 

呼叫 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)時，開發人員可以選擇是否要加密金鑰。 如果 *hExpKey* 參數包含工作階段金鑰的有效控制碼，就會加密 **PRI加值稅EKEYBLOB** 。 但 BLOB 的 [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) 部分都會加密。

> [!Note]  
> 加密演算法和加密金鑰參數不會與私密金鑰 BLOB 一起儲存。 應用程式必須管理和儲存此資訊。 如果傳遞給 *hExpKey* 的值為零，將會匯出私密金鑰而不加密。

 

> [!Caution]  
> 匯出私密金鑰而不加密是很危險的，因為這些金鑰接著很容易被未經授權的實體攔截及使用。

 

 

 
