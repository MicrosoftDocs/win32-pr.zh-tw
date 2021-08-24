---
description: 安全-完整路徑轉換的來源必須位於 [轉換] 屬性中指定的完整路徑。
ms.assetid: 9c1cd6c5-d246-49d8-a632-991274bb4511
title: 安全-完整路徑轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f55e16f40d99deceb8b625297cf447ebf5ec7dfb14a25518554804cf35b572e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040898"
---
# <a name="secure-full-path-transforms"></a>安全-完整路徑轉換

安全-完整路徑轉換的來源必須位於 [ [**轉換**](transforms.md) ] 屬性中指定的完整路徑。 安裝或公告封裝之後，安裝程式會將轉換儲存在快取中，而在安全的檔案系統上，使用者沒有寫入權限。 如果轉換的本機複本變得無法使用，它可能只會使用指定的路徑來還原快取。 由任何使用者移除產品時，會從使用者的電腦移除該產品的所有安全轉換。

若要在安裝封裝時套用安全的完整路徑轉換，請設定 [TransformsSecure 原則](transformssecure-policy.md) 或 [**TransformsSecure**](transformssecure.md) 屬性，或將 \| 第一個字元傳遞至轉換清單。 每個轉換來源的完整路徑必須在轉換字串中傳遞。 如果清單中有任何相對路徑，安裝就會失敗。 轉換來源不需要與封裝的來源位於一起。

 

 



