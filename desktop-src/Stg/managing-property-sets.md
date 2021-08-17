---
title: 管理屬性集
description: 持續性屬性集包含相關的資料做為屬性。
ms.assetid: 19ff2751-87f3-43d8-9307-ce2dd399f694
keywords:
- 管理屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8b6b81c466232d4fd325d53a3cfe67ebb1cbc60c757a6dfe135a021ab7892a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960882"
---
# <a name="managing-property-sets"></a>管理屬性集

持續性屬性集包含相關的資料做為屬性。 每個屬性集都是使用 FMTID 來識別，而全域唯一識別碼 (GUID) ，可讓應用程式存取屬性集來識別屬性集。 透過此識別，應用程式會解讀該集合所包含的屬性。

例如，文字處理器中的字元格式設定屬性，或繪圖程式中專案的轉譯屬性是屬性集。

COM 會定義 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 介面，以協助管理屬性集。 透過這個介面的方法，您可以建立新的屬性集，或開啟或刪除現有的屬性集。 此外，它還提供建立列舉值的方法，並提供其 [**IEnumSTATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 介面的指標。 您可以呼叫此介面的方法來列舉物件上的 [**STATPROPSETSTG**](/windows/win32/api/propidlbase/nn-propidlbase-ienumstatpropsetstg) 結構，以提供物件上所有屬性集的相關資訊。

當您建立或開啟 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)實例時，它類似于開啟支援 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 或 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)的物件，因為您需要指定開啟介面的儲存模式。 若為 **IStorage**，這些包括交易模式、讀取/寫入模式以及共用模式。

當您使用 [**IPropertySetStorage：： create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create)的呼叫來建立屬性集時，請指定屬性集是否為 simple 或簡單。 簡單的屬性集包含的型別，可以完全寫在屬性集資料流程中，它的大小會限制，而且在 Windows NT 4.0 和更早版本中，可能不會超過 256 KB，Windows 2000、Windows XP 和 Windows Server 2003 中則為 1 MB。 但是，當您需要在屬性集中儲存較大量的資訊時，可以指定要簡單的屬性集。 這可讓您使用一或多個類型，只指定儲存或資料流程物件的指標。 這些類型為 VT \_ 串流、vt 資料流程 \_ 物件、vt \_ 儲存和 vt \_ 儲存的 \_ 物件。

儲存在這些屬性中的資料不會計入 Windows NT 4.0 或更早版本的 256 KB 屬性集大小限制，或是 Windows 2000、Windows XP 和 Windows Server 2003 的 1 MB 限制。 但是，屬性的相關資料（例如其名稱）則適用。 此外，如果您需要交易更新，則必須簡單屬性集。 當然，開啟這些類型的效能會受到影響，因為它需要開啟您擁有指標的資料流程或儲存物件。

如果您的應用程式使用複合檔案，您可以使用這些介面的 COM 提供執行，這些介面是在 COM 複合檔案儲存物件上所執行。

每個屬性集都是由邏輯連接的屬性群組所組成，如 [管理屬性](managing-properties.md)中所述。

如需 COM 中屬性集的詳細資訊，請參閱：

-   [COM 中的屬性集執行](property-set-implementations-in-com.md)
-   [屬性集考慮](property-set-considerations.md)
-   [IPropertySetStorage 實行考慮](ipropertysetstorage-implementation-considerations.md)
-   [儲存屬性集](storing-property-sets.md)
-   [效能特色](performance-characteristics.md)
-   [執行摘要資訊屬性集](implementing-the-summary-information-property-set.md)

 

 