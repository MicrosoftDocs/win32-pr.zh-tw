---
description: 說明 CryptoAPI 系統架構。
ms.assetid: 244329bb-fc71-4ab9-8831-a9478108ffa3
title: CryptoAPI 系統架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 791ed0ebfc82df1dc7b6e9600d4e0455ae60df3da35cfe3f8fd613f7b230ebd7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768802"
---
# <a name="cryptoapi-system-architecture"></a>CryptoAPI 系統架構

CryptoAPI 系統架構由五個主要功能區域組成：

-   [基底加密函式](#base-cryptographic-functions)
-   [憑證編碼/解碼函數](#certificate-encodedecode-functions)
-   [憑證存放區功能](#certificate-store-functions)
-   [簡化的訊息函數](#simplified-message-functions)
-   [低層級訊息函數](#low-level-message-functions)

## <a name="base-cryptographic-functions"></a>基底加密函式

-   用來連接到 CSP 的 *內容* 函式。 這些函式可讓應用程式依名稱選擇特定的 CSP，或選擇可提供所需功能類別的特定 CSP。
-   用來產生及儲存 [*密碼編譯金鑰*](../secgloss/c-gly.md)的 [*金鑰產生函數*](../secgloss/k-gly.md)。 包含變更 [*連結模式*](../secgloss/c-gly.md)、 [*初始化向量*](../secgloss/i-gly.md)和其他加密功能的完整支援。 如需詳細資訊，請參閱[金鑰產生和 Exchange](cryptography-functions.md)函式。
-   用來交換或傳輸金鑰的 *金鑰交換函數*。 如需詳細資訊，請參閱[密碼編譯金鑰儲存體以及 Exchange](cryptographic-key-storage-and-exchange.md)和[金鑰產生和 Exchange 功能](cryptography-functions.md)。

## <a name="certificate-encodedecode-functions"></a>憑證編碼/解碼函數

-   用來加密或解密資料的函數。 [*雜湊*](../secgloss/h-gly.md)資料也包含支援。 如需詳細資訊，請參閱 [資料加密和解密功能](cryptography-functions.md) 以及 [資料加密和解密](data-encryption-and-decryption.md)。

## <a name="certificate-store-functions"></a>憑證存放區功能

-   用來管理數位憑證集合的函式。 如需詳細資訊，請參閱 [數位憑證](digital-certificates.md) 和 [憑證存放區功能](cryptography-functions.md)。

## <a name="simplified-message-functions"></a>簡化的訊息函數

-   用來加密和解密訊息和資料的函式。
-   用來簽署訊息和資料的函式。
-   用來確認收到的訊息和相關資料之簽章真實性的函數。

如需詳細資訊，請參閱 [簡化的訊息](simplified-messages.md) 和 [簡化的訊息函數](cryptography-functions.md)。

## <a name="low-level-message-functions"></a>低層級訊息函數

-   用來執行簡化訊息函數所執行之所有工作的函數。 低層級的訊息函式比簡化的訊息函式提供更大的彈性，但需要更多函式呼叫。 如需詳細資訊，請參閱 [低層級訊息](low-level-messages.md) 和 [低層級訊息函數](cryptography-functions.md)。

![cryptoapi 架構](images/cryparch.png)

每個功能區域的函式名稱中都有一個關鍵字，指出其功能區域。



| 功能區域              | 函數名稱慣例 |
|------------------------------|--------------------------|
| 基底加密函式 | 地穴                    |
| 編碼/解碼函數  | 地穴                    |
| 憑證存放區功能  | 儲存                    |
| 簡化的訊息函數 | 訊息                  |
| 低層級訊息函數  | Msg                      |



 

應用程式會在所有這些區域中使用函數。 這些函式會結合在一起，以執行 CryptoAPI。 [*基底加密*](../secgloss/b-gly.md)函式會使用 csp 來取得必要的密碼編譯演算法，以及 [加密金鑰](cryptographic-keys.md)的產生和安全儲存。

使用兩種不同的密碼編譯金鑰： [*工作階段金鑰*](../secgloss/s-gly.md)（用於單一加密/解密）和 [*公開/私密金鑰*](../secgloss/p-gly.md)組（會以更永久的方式使用）。

> [!Note]  
> 雖然應用程式可以直接與五個功能區域中的任一個通訊，但無法與 CSP 直接通訊。 所有應用程式對 CSP 的通訊都是透過 [*基底加密*](../secgloss/b-gly.md)函式進行。 基底加密函式具有參數，可指定要使用的 CSP。 此參數可以設定為 **Null** ，以選取預設的 CSP。

 

 

 
