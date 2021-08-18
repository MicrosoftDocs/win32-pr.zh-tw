---
description: 顯示如何傳送加密的訊息。
ms.assetid: 928b1863-7a54-4bf0-b447-85b8c2868bcd
title: 手動工作階段金鑰交換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38c9f7338b40ed1675b2186e478c8c124719b376889ce691d305e246016e0d9c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119425590"
---
# <a name="manual-session-key-exchanges"></a>手動工作階段金鑰交換

> [!Note]  
> 本節所述的程式假設使用者 (或 CryptoAPI 用戶端) 已經有自己的一組 [*公開/私密金鑰*](../secgloss/p-gly.md) 組，而且也取得彼此的 [*公開金鑰*](../secgloss/p-gly.md)。

 

下圖顯示如何使用此程式來傳送加密的訊息。

![傳送加密的訊息](images/capi04.png)

這種方法很容易受到一種常見的攻擊。 小人可以取得一或多個加密訊息和加密金鑰的複本。 然後，在稍後的時間，小人可以將其中一個訊息傳送給接收者，而接收者將無法得知訊息未直接來自原始寄件者。 您可以使用時間戳所有訊息或使用序號來降低這項風險。

將加密的訊息傳送給另一位使用者的最簡單方式，就是傳送以隨機工作階段金鑰加密的訊息，以及使用接收者的 [*金鑰交換公開金鑰*](../secgloss/k-gly.md)加密的工作階段金鑰。

以下是傳送加密工作階段金鑰的步驟。

**傳送加密的工作階段金鑰**

1.  使用 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)函式來建立隨機 [*工作階段金鑰*](../secgloss/s-gly.md)。
2.  使用工作階段金鑰來加密訊息。 這項程式會在 [資料加密和解密](data-encryption-and-decryption.md)中討論。
3.  使用 [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey)函式將工作階段金鑰匯出至 [*金鑰 BLOB*](../secgloss/k-gly.md) ，並指定使用目的地使用者的金鑰交換公開金鑰來加密金鑰。
4.  將加密的訊息和加密的金鑰 BLOB 傳送給目的地使用者。
5.  目的地使用者使用 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) 函式，將金鑰 BLOB 匯入其 CSP 中。 如果在步驟3中指定了目的地使用者的金鑰交換公開金鑰，這將會自動將工作階段金鑰解密。
6.  目的地使用者接著可以使用工作階段金鑰來解密訊息， [並遵循資料加密和解密](data-encryption-and-decryption.md)中所討論的程式。

 

 
