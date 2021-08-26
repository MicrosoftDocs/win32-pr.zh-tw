---
description: 來源安全轉換的來源必須位於套件來源的根目錄。」
ms.assetid: b5355053-9922-444f-a117-f6af461ef9e9
title: 安全來源轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f591e6f30c11ec9fa7edf2f943ef1f660a0a3b12ff87c3c1de0984328652565b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040998"
---
# <a name="secure-at-source-transforms"></a>安全來源轉換

來源安全轉換的來源必須位於套件來源的根目錄。」 安裝或公告封裝之後，安裝程式會將轉換儲存在快取中，而在安全的檔案系統上，使用者沒有寫入權限。 如果轉換的本機複本無法使用，安裝程式會搜尋來源以還原快取。 方法與搜尋 .msi 檔案的來源清單相同。 如需詳細資訊，請參閱 [來源復原](source-resiliency.md)。 由任何使用者移除產品時，會從使用者的電腦移除該產品的所有安全轉換。

若要在安裝封裝時套用安全來源轉換，請設定 [TransformsSecure 原則](transformssecure-policy.md) 或 [**TransformsSecure**](transformssecure.md) 屬性，或將 @ 轉換清單中傳遞的第一個字元。 每個轉換都必須以檔案名表示，而且必須位於封裝來源的根目錄中。 如果有任何轉換不在套件來源的根目錄中，安裝就會失敗。 如需詳細資訊，請參閱套用 [轉換](applying-transforms.md)。

 

 



