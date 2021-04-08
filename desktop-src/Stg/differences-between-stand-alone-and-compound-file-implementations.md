---
title: 獨立和複合檔案執行之間的差異
description: 屬性集介面和複合檔案執行的獨立實作為某些方式不同。
ms.assetid: 650d4759-a58a-47a4-922d-5757e356cf56
keywords:
- IPropertyStorage Strctd Stg.，實施
- IPropertyStorage Strctd Stg.，實施，差異
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 988f8a9cfdaca0a131bedf98cd8ff10ae8b89525
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839831"
---
# <a name="differences-between-stand-alone-and-compound-file-implementations"></a>獨立和複合檔案執行之間的差異

屬性集介面和複合檔案執行的獨立實作為某些方式不同。 在資料流程、儲存體、屬性集儲存區和屬性儲存物件的複合檔案中，不同的介面會彼此協調，因為它們共用一般的實值。 在獨立的執行中，介面實現是相異的。

因此，複合檔案執行會處理並行問題，並將屬性集物件與儲存體或資料流程物件同步處理。 使用獨立執行時，用戶端會負責處理儲存體或資料流程物件與屬性集之間的平行存取和同步處理問題。 用戶端可以遵循兩個簡單的規則來滿足這些需求。 首先，絕對不要在屬性儲存物件開啟時，使用其資料流程或儲存介面來操作屬性集。 其次，在上階儲存物件上呼叫 **CopyTo**、 **MoveElementTo** 或 **commit** 之前，一律在屬性儲存物件上呼叫 **commit** 。 具體而言，下列專案需要用戶端注意：

-   在複合檔案的執行中，單一機制會針對儲存物件和其相關聯的屬性集物件提供並行保護。 不過，在獨立的執行中，儲存體物件的執行與屬性集的執行是分開的，而且每個都提供自己的並行機制。 因此，在獨立的執行中，用戶端會負責透過相互排除的機制來維護兩個執行之間的並行保護。
-   在複合檔案執行中，屬性集的變更會在屬性集快取中進行緩衝處理。 然後，在儲存物件上呼叫 [**IStorage：： Commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) 方法時，複合檔案執行會在認可儲存物件之前，自動從屬性集緩衝區清除屬性集變更。 因此，屬性集的變更會在認可的交易中變成可見。

    在獨立的執行中，用戶端必須在呼叫 IPropertyStorage：： commit 方法之前，先呼叫 [**：： commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) 來明確地排清屬性集緩衝區，然後再呼叫儲存體上的 [**IStorage：： commit**](/windows/desktop/api/Objidl/nf-objidl-istorage-commit) 方法。 或者，用戶端可以在獨立的執行中使用新的 PROPSETFLAG \_ 無緩衝值，直接寫入屬性集，而不是快取屬性集內部緩衝區的變更。 如果使用 PROPSETFLAG 無 \_ 緩衝，則會自動符合用戶端的責任。 複合檔案執行不支援 PROPSETFLAG 未緩衝的 \_ 值。 如需詳細資訊，請參閱 [**PROPSETFLAG 常數**](propsetflag-constants.md)。

-   如同交易式儲存體，複合檔案執行會在執行 [**IStorage：： CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto) 或 [**IStorage：： MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)的呼叫之前，先清除其內部緩衝區來更新屬性集。 因此，屬性集的變更會反映在複製或移動的儲存元素中。

    在獨立的執行中，用戶端必須在呼叫 [**IStorage：： CopyTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-copyto)或 [**IStorage：： MoveElementTo**](/windows/desktop/api/Objidl/nf-objidl-istorage-moveelementto)之前呼叫 [**IPropertyStorage：： Commit**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-commit) ，以明確地清除屬性集緩衝區。 或者，用戶端可以使用新的 PROPSETFLAG \_ 無緩衝值直接寫入屬性集，而不是快取屬性集緩衝區的變更。 如需詳細資訊，請參閱 [**PROPSETFLAG 常數**](propsetflag-constants.md)。

 

 




