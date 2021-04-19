---
description: 在某些情況下，金鑰必須從密碼編譯服務提供者的安全環境中匯出 (CSP) 到應用程式的資料空間。 已匯出的金鑰會儲存在加密的金鑰 BLOB 結構中。
ms.assetid: 859b1bfe-6182-4728-a721-1f34cc98f66f
title: 密碼編譯金鑰儲存和交換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: be7e789a736f0fcd5208bc16d73b43c6a9232e33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998062"
---
# <a name="cryptographic-key-storage-and-exchange"></a>密碼編譯金鑰儲存和交換

在某些情況下，金鑰必須從 [*密碼編譯服務提供者*](../secgloss/c-gly.md) 的安全環境中匯出 (CSP) 到應用程式的資料空間。 已匯出的金鑰會儲存在加密的 [*金鑰 BLOB*](../secgloss/k-gly.md) 結構中。

有兩個特定的情況需要匯出金鑰：

-   若要儲存 [*工作階段金鑰*](../secgloss/s-gly.md) 以供應用程式稍後使用，例如，應用程式只會加密資料庫檔案，稍後再進行解密。 應用程式會負責儲存加密金鑰。 這是必要的，因為 Csp 不會保留會話之間的 [*對稱金鑰*](../secgloss/s-gly.md) 。
-   將金鑰傳送給其他人。 如果個別的 Csp 可以直接通訊，但不能這麼做，就會比較容易。 因為 Csp 無法通訊，所以必須從一個 CSP 匯出金鑰，並傳輸至目的地應用程式，然後再匯入到目的地 CSP 中。 如果通訊路徑不受信任，此程式可能會變得更複雜。

無論是哪一種情況，應用程式都必須將工作階段金鑰儲存在 CSP 外一段時間。 如需詳細資訊，請參閱 [儲存工作階段金鑰](procedure-for-storing-a-session-key.md)的程式。

 

 
