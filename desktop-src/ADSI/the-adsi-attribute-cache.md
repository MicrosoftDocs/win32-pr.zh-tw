---
title: ADSI 屬性快取
description: ADSI 物件模型提供每個 ADSI 物件的用戶端屬性快取。
ms.assetid: 0d2b4117-11f2-4b39-8fe5-3b176e4256f4
ms.tgt_platform: multiple
keywords:
- ADSI 屬性快取 ADSI
- ADSI ADSI，使用，利用 ADSI、屬性快取存取及運算元據
- 屬性 ADSI，屬性快取
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5940d431fc476fdecd8397875bf06a04ed82ea30ab4ed2e98b94ccef98f0e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119930041"
---
# <a name="the-adsi-attribute-cache"></a>ADSI 屬性快取

ADSI 物件模型提供每個 ADSI 物件的用戶端屬性快取。 屬性快取相當於記憶體中的資料表，其中包含已下載的大部分物件屬性的名稱和值。 某些屬性（例如操作屬性）不會被快取。 ADSI 使用屬性快取來增強屬性操作的效能，並新增屬性讀取和寫入作業的 transactioning 功能。 這項功能對於以沒有原生批次處理機制可設定屬性的語言（例如 Microsoft Visual Basic 開發系統）所撰寫的客戶而言非常重要。 如果沒有 ADSI 屬性快取，這類用戶端就必須在每次讀取或寫入屬性時存取伺服器。

建立物件或第一次系結至時，物件的屬性快取是空的。 呼叫 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 方法時，ADSI 會將物件的要求屬性從基礎目錄服務載入至本機快取。 當特定的屬性值被讀取，且快取是空的時，ADSI 會對 **IADs：： GetInfo** 方法進行隱含呼叫。 填滿快取時，所有屬性讀取作業只適用于快取的內容。

寫入屬性值時，新的值會儲存在本機快取中，直到呼叫 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法為止。 呼叫 **IADs：： SetInfo** 方法時，快取中的屬性會認可至基礎目錄服務。 在呼叫 **IADs：： SetInfo** 方法之後，值會保留在快取中，直到以另一個對 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 方法的呼叫明確重新整理為止。

> [!IMPORTANT]
> 必須謹慎使用 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 方法，因為這個方法一律會從基礎目錄服務覆寫快取中的屬性值，即使快取的值已變更也一樣。 也就是說，它會覆寫快取中已變更的屬性值，但在呼叫 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo) 方法時，不會認可到基礎目錄服務。

 

下圖顯示用來在快取上操作的不同方法。

![adsi 屬性快取](images/ds2propc.png)

 

 




