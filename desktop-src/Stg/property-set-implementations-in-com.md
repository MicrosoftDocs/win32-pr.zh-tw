---
title: COM 中的屬性集執行
description: COM 中的屬性集執行
ms.assetid: 52d7b534-f81a-4cc9-b5ea-9538bfff056c
keywords:
- 結構化儲存體 Strctd Stg.，使用屬性集在 COM 中使用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8ee68fcd36958e0b7b0648e40f6e3c480f31d3
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933341"
---
# <a name="property-set-implementations-in-com"></a>COM 中的屬性集執行

雖然不會完全使用持續性屬性集的可能性，但目前有兩個主要用途：

-   使用檔等物件儲存摘要資訊
-   傳送物件之間的屬性資料

COM 屬性集的設計目的，是要將適合表示的資料儲存為較精細值的中等大小集合。 如果資料集太大而無法執行，則應該將它們分成不同的資料流程、儲存體及/或屬性集。 COM 屬性集資料格式並非用來提供許多小型物件的資料庫替代。

COM 提供各種物件的屬性集介面，以及三個 helper 函數。 下一節將說明這些執行的一些效能特性。 如需特定介面的詳細資訊，以及如何取得這些介面的指標，請參閱 COM 參考一節中的下列內容：

-   [IPropertySetStorage –複合檔案執行](ipropertysetstorage-compound-file-implementation.md)

    複合檔案的實作為提供 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 和 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 介面，也提供 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面。 由於 **IStorage** 的複合檔案執行， **IPropertySetStorage** 介面可透過呼叫 [**IUnknown：： QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))來取得。

-   [IPropertySetStorage – NTFS 檔案系統執行](ipropertysetstorage-ntfs-file-system-implementation.md)

    您也可以針對非複合檔案的 NTFS 檔案取得 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面。 因此，您可以針對 NTFS 磁片區上的所有檔案取得這些介面。

-   [IPropertySetStorage –獨立執行](ipropertysetstorage-stand-alone-implementation.md)

    當 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 的這個執行具現化時，它會獲得支援 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面之物件的指標。 然後，它會在該儲存物件內操作屬性集的儲存。 因此，可以存取和操作任何支援之物件上的屬性集。

-   [IPropertySetStorage 實行考慮](ipropertysetstorage-implementation-considerations.md)

    提供 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面的執行時，需要考慮幾個問題。 請參閱 COM 參考一節中的這些 *執行考慮* 。

此外，還有四個 helper 函式，其設計目的是為了協助處理已從屬性集中讀取的屬性， (為 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構) ：

-   [**PropVariantInit**](/windows/desktop/api/PropIdl/nf-propidl-propvariantinit)
-   [**PropVariantClear**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantclear)
-   [**FreePropVariantArray**](/windows/win32/api/combaseapi/nf-combaseapi-freepropvariantarray)
-   [**PropVariantCopy**](/windows/win32/api/combaseapi/nf-combaseapi-propvariantcopy)

下列各節會更詳細地討論 COM 中的屬性集執行：

-   [管理屬性集](managing-property-sets.md)
-   [屬性集考慮](property-set-considerations.md)
-   [儲存屬性集](storing-property-sets.md)
-   [效能特色](performance-characteristics.md)
-   [執行摘要資訊屬性集](implementing-the-summary-information-property-set.md)
-   [IPropertySetStorage 實行考慮](ipropertysetstorage-implementation-considerations.md)

 

 