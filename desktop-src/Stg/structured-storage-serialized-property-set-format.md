---
title: 結構化儲存體序列化屬性集格式
description: 持續性屬性集會提供將資料儲存在檔案系統實體內的選項。 建議您在建立和管理它們時，使用屬性和屬性集中所述的 IPropertySetStorage 和 IPropertyStorage 介面。
ms.assetid: f22abe40-535f-4178-9460-59bbe26ff178
keywords:
- 結構化儲存體 Strctd Stg.、基本、序列化屬性集格式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5acbc5300c04b4fe5a9b2a9ce2610eefc8608b3921ef52968a7165c4362ff7cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117959772"
---
# <a name="structured-storage-serialized-property-set-format"></a>結構化儲存體序列化屬性集格式

持續性屬性集會提供將資料儲存在檔案系統實體內的選項。 建議您在建立和管理它們時，使用 [屬性和屬性集中](properties-and-property-sets.md)所述的 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)介面。

屬性集是由值的標記區段所組成，而且區段是由格式識別碼 (FMTID) 來唯一識別。 每個屬性都是由屬性識別碼和代表值的類型指標所組成。 儲存在屬性集中的每個值都有唯一的屬性識別碼，可區分屬性。 類型指標描述值中的資料標記法。

當您使用 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 介面時，您不需要處理 COM 序列化的屬性集格式結構。 如需詳細資訊，請參閱下列主題：

屬性集內的所有資料元素都會儲存在 Intel 表示中， (也就是以位元組由小到大的順序) 。

COM 會定義屬性集的標準、序列化資料格式。 處理序列化格式，而不是使用介面時，屬性集會具有下列特性：

-   屬性集可讓不同的應用程式建立自己的獨立屬性集來提供應用程式。
-   屬性集可以儲存在單一 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 實例或包含多個資料流程的 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 實例中。 屬性集只是另一種資料類型，可儲存在記憶體中或磁片上儲存體的許多不同形式。 如需建立儲存物件之字串名稱的詳細資訊和建議慣例，請參閱[儲存體物件命名慣例](storage-object-naming-conventions.md)。
-   屬性集允許包含說明內容的顯示名稱字典。 建議使用一組選擇屬性名稱的慣例。 如需此選擇性字典的詳細資訊，請參閱 [保留的屬性識別碼](reserved-property-identifiers.md)，包括 [屬性識別碼 0](/windows/desktop/Stg/reserved-property-identifiers)。

屬性集資料流程分為三個主要部分：

-   標頭
-   FORMATID/位移配對
-   包含實際屬性集值的區段

屬性集資料流程的整體長度必須小於或等於256K。 下列章節、 [屬性集標頭](property-set-header.md)、 [格式識別碼/位移](format-identifier-offset-pair.md)組和 [區段](section.md) (包括 [屬性識別碼/位移](property-identifiers-offset-pairs.md) 組) ，以及支援的主題，描述構成屬性集資料格式的個別元件。

> [!Note]  
> 本檔先前的版本描述了屬性集資料流程的延伸模組，並允許一個以上的區段，但是已經修改為可提供屬性資料流程中的一個區段。 其中一個例外狀況是 [DocumentSummaryInformation 和使用者設定的屬性集](the-documentsummaryinformation-and-userdefined-property-sets.md)。

 

 

 