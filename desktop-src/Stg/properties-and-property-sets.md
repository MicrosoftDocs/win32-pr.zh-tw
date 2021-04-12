---
title: 屬性和屬性集
description: 雖然自動化和 Microsoft ActiveX 控制項提供的執行時間屬性種類很重要，但它們並不直接滿足儲存儲存在檔案系統中之物件資訊的需求。
ms.assetid: 350cfb84-2f8e-46e7-a70d-09beb14a8eee
keywords:
- 結構化儲存體 Strctd Stg.、基本概念、屬性和屬性集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fdafcbef0e92479aa628ab119b6d961abb74d82
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104372682"
---
# <a name="properties-and-property-sets"></a>屬性和屬性集

雖然自動化和 Microsoft ActiveX 控制項提供的執行時間屬性種類很重要，但它們並不直接滿足儲存儲存在檔案系統中之物件資訊的需求。 這些實體可能包含 (結構化、複合) 、目錄和摘要目錄等檔案。 COM 同時提供這些持續性屬性的標準序列化格式，以及一組可讓您建立及操作屬性集及其屬性的介面和函式。

持續性屬性會儲存為集合，且一或多個集合可能會與檔案系統實體相關聯。 這些持續性屬性集會用來儲存適合當做更精細值集合來表示的資料。 它們並不是用來做為大型的資料基底。 它們可用來儲存有關系統上物件的摘要資訊，然後可供任何其他瞭解如何解讀該屬性集的物件存取。

先前的 COM 版本指定的內容和用法非常少，但卻定義了序列化格式，可讓開發人員將屬性和屬性集儲存在 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 實例中。 也定義了單一屬性集的屬性識別碼和語義（用於檔的摘要資訊）。 屆時，必須以資料流程的形式直接建立和操作該結構。 請參閱 [結構化儲存體序列化屬性集格式](structured-storage-serialized-property-set-format.md)。

不過，現在 COM 定義了兩個主要介面來管理屬性集：

-   [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)
-   [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)

當這些介面在支援 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) 介面 (（例如複合檔案) ）的物件上執行時，不再需要直接處理序列化格式。 透過 [**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage) 和 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage) 寫入屬性會建立完全符合 COM 屬性集格式的資料，如透過 **IStorage** 方法所查看。 反之也是如此，使用 **IStorage** 寫入 COM 屬性集格式的屬性會透過 **IPropertySetStorage** 和 **IPropertyStorage** (顯示，不過您無法預期寫入 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) 並讓屬性通過 **IPropertyStorage** 立即可用，反之亦然) 。

[**IPropertySetStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertysetstorage)介面會定義建立及管理屬性集的方法。 [**IPropertyStorage**](/windows/desktop/api/Propidl/nn-propidl-ipropertystorage)介面會直接操控屬性集內的屬性。 藉由呼叫這些介面的方法，應用程式開發人員可以管理任何適用于指定檔案系統實體的屬性集。 使用這些介面可為屬性提供一個微調的讀取和寫入執行，而不是在每個應用程式中都有一個執行，例如 incessant 搜尋的效能瓶頸。 您可以執行介面以增強效能，因此可以更快速地讀取和寫入屬性，例如更有效率的快取。 此外， **IPropertyStorage** 和 **IPropertySetStorage** 可讓您在不支援 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)的實體上操作屬性，不過一般而言，大部分的應用程式都不會這麼做。

本節包含下列主題：

-   [摘要資訊屬性集](the-summary-information-property-set.md)
-   [預先定義的屬性集格式識別碼](predefined-property-set-format-identifiers.md)
-   [DocumentSummaryInformation 和使用者設定的屬性集](the-documentsummaryinformation-and-userdefined-property-sets.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 中的屬性集執行](property-set-implementations-in-com.md)
</dt> <dt>

[屬性集考慮](property-set-considerations.md)
</dt> <dt>

[管理屬性](managing-properties.md)
</dt> <dt>

[管理屬性集](managing-property-sets.md)
</dt> <dt>

[儲存屬性集](storing-property-sets.md)
</dt> <dt>

[效能特色](performance-characteristics.md)
</dt> </dl>

 

 




