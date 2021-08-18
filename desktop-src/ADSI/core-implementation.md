---
title: 核心執行
description: ADSI 提供者支援下列功能
ms.assetid: 39798237-a181-43b4-8441-ac711f923d4d
ms.tgt_platform: multiple
keywords:
- core 實行 ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78487b701cac0409745ed3a7776dd882f2c37a878dec1d144c3b52a426db487
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118962087"
---
# <a name="core-implementation"></a>核心執行

ADSI 提供者支援下列功能：

-   COM 和 URL 格式的 ADsPath 字串。 根據定義，您可以使用 ADsPath 取出 Active Directory 物件。 提供者支援其目錄服務使用 **ParseDisplayName** 執行所需的語法。
-   最上層命名空間物件，支援 [**IParseDisplayName：:P arsedisplayname**](/windows/win32/api/oleidl/nf-oleidl-iparsedisplayname-parsedisplayname) 和 [**IADsOpenDSObject**](/windows/desktop/api/Iads/nn-iads-iadsopendsobject)。 此物件包含此命名空間的根節點。 **ParseDisplayName** 實作為的一部分必須包含剖析器，以檢查它自己的命名空間是否有語法錯誤。 此物件也必須支援 [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 和 **IADsOpenDSObject**。
-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)介面。 這包括透過 [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 和 [**IADs：： SetInfo**](/windows/desktop/api/Iads/nf-iads-iads-setinfo)的簡單屬性快取執行。 取得或設定物件屬性的作業會在快取模式下發生。 快取值會在 **IADs：： SetInfo** 期間寫入基礎目錄存放區。 不過，ADSI 方法不會被快取，但會立即執行。
-   [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist)、 [**IADsPropertyEntry**](/windows/desktop/api/Iads/nn-iads-iadspropertyentry)和 [**IADsPropertyValue**](/windows/desktop/api/Iads/nn-iads-iadspropertyvalue)介面，可直接存取和列舉屬性快取中的屬性。 對於不公開架構的目錄服務，此介面可讓您操作物件的屬性。
-   非自動化用戶端的 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面。 這會使用無線通訊協定來取得最大效能，並略過屬性快取。
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)介面。 每個 Active Directory 物件都有控制其存留期的父容器。 請注意，針對 ADs 容器物件， [**IADs：： GetInfo**](/windows/desktop/api/Iads/nf-iads-iads-getinfo) 只會影響容器屬性，而不會影響其內容。 SetInfo on ADs 容器物件只會影響容器屬性，而不會影響容器內已存在的新建立物件或物件。
-   [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面。 這是不使用編譯時間系結之語言的自動化介面，例如 Visual Basic 腳本版本。 與此相關的是提供者必須提供的類型程式庫資料。 如需詳細資訊，請參閱 [ADSI 提供者的執行問題](implementation-issues-for-adsi-providers.md)。
-   架構類別容器物件和適當的語法、屬性和架構類別物件，分別支援 [**IADsSyntax**](/windows/desktop/api/Iads/nn-iads-iadssyntax)、 [**IADsProperty**](/windows/desktop/api/Iads/nn-iads-iadsproperty)和 [**得到 iadsclass**](/windows/desktop/api/Iads/nn-iads-iadsclass) 。 每個根節點至少必須包含自己的架構類別容器物件。
-   [**IADsMembers**](/windows/desktop/api/Iads/nn-iads-iadsmembers)介面（如果任何支援的屬性是 ADSI 物件的集合，例如安全性群組）。
-   [**IADsCollection**](/windows/desktop/api/Iads/nn-iads-iadscollection)介面，如果任何支援的屬性是具有 [**IADsCollection：： Add**](/windows/desktop/api/Iads/nf-iads-iadscollection-add)和 [**IADsCollection：： Remove**](/windows/desktop/api/Iads/nf-iads-iadscollection-remove)功能的相同目錄元素類型集合。
-   **IEnumXXXX** 列舉支援所有特定的列舉值物件。
-   對應語法的常式，並將原生資料轉換成 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) 資料類型。
-   遵循提供者提供的 ADSI 物件的 ADSI 慣例。 包含說明檔和型別程式庫，可記錄介面屬性和方法。

如同任何 COM 執行，對 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))的呼叫必須針對未提供的介面傳回 **e \_ NOINTERFACE** 、針對未完成的介面傳回 e **\_ >notimpl** ，否則會實作為未執行的介面不支援的方法，並傳回未完成屬性 **\_ \_ \_ 不 \_ 支援的 e ADS 屬性** 如需雙重介面以及它們如何影響屬性執行的詳細資訊，請參閱 [雙重介面](dual-interfaces.md)。

 

 