---
title: 使用 ADSI 存取及運算元據
description: 所有物件都有屬性。
ms.assetid: 366a1fbc-3089-406a-9819-cf2ba7636c5f
ms.tgt_platform: multiple
keywords:
- ADSI ADSI，存取和運算元據
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b3291db7490c79aae6363f619582ed24339fb83d
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "106969935"
---
# <a name="accessing-and-manipulating-data-with-adsi"></a>使用 ADSI 存取及運算元據

所有物件都有屬性。 所有 Active Directory 服務介面 (ADSI) COM 物件都有一個或多個介面，其中包含可抓取 COM 物件所代表之目錄物件屬性的方法。 有幾種方式可以從物件讀取屬性：

-   依名稱取得特定屬性： [**IADs**](/windows/desktop/api/Iads/nn-iads-iads) 介面有兩個方法 [**IADs：： Get**](/windows/desktop/api/Iads/nf-iads-iads-get) 和 [**IADs：： GetEx**](/windows/desktop/api/Iads/nf-iads-iads-getex) 可讀取特定屬性。 每個 ADSI COM 物件都有一個 **IADs** 介面。
-   取得指定的屬性清單： [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 介面具有方法 [**IDirectoryObject：： GetObjectAttributes**](/windows/desktop/api/Iads/nf-iads-idirectoryobject-getobjectattributes) ，可讓您指定包含要讀取之屬性名稱的清單，並傳回包含所要求屬性值之結構的陣列。
-   列舉物件的所有屬性： [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) 介面可讓您列舉物件上的所有屬性。
-   取得特殊屬性：自動化介面 ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \*) 具有屬性方法，可讓您取得未儲存在物件中的特殊屬性。 或者，屬性方法可讓您取得與儲存的實際資料類型不同的資料格式的物件屬性。 例如， **IADs** 介面具有像是 [**IADs：： get \_ name**](iads-property-methods.md)的屬性方法，它會將物件的相對辨別名稱 (RDN) ; **IADs：： get \_類別**，它會抓取物件的類別，並使用 **IADs：： get \_ 父系**，將 ADsPath 抓取物件的父系。

ADSI 可讓您從目錄伺服器讀取屬性，在本機快取內容。 這可讓您選擇從本機屬性快取讀取屬性，或是直接從目錄伺服器抓取屬性。 ADSI 也有方法可更新快取，以及指定是否要快取物件的所有屬性，或只快取您指定的屬性。

在您抓取屬性之後，您會讀取其值。 屬性的資料類型取決於屬性的定義 (也稱為 Active Directory 架構中的屬性) 。 針對可以存在於 Active Directory 中的每個屬性類型，Active Directory 架構中都有一個 **attributeSchema** 物件。 **AttributeSchema** 物件會定義屬性的特性。 其中一個特性是屬性的語法，它會決定屬性值的資料類型。 如需詳細資訊，請參閱[Active Directory 屬性](/windows/desktop/AD/syntaxes-for-attributes-in-active-directory-domain-services)[之屬性](/windows/desktop/AD/characteristics-of-attributes)和語法的特性。

自動化介面 ([**IADs**](/windows/desktop/api/Iads/nn-iads-iads) \*) 會傳回屬性值做為 [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant)或代表屬性之 COM 物件上的 Automation 介面指標。 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)和 [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)介面會以指標的形式傳回屬性，該結構包含具類型的屬性值或位元組字串的指標。 此外， **IDirectoryObject** 和 **>idirectorysearch** 會直接從目錄伺服器取出屬性，而不是使用本機屬性快取。

本節將說明下列主題：

-   [IADs 和 IDirectoryObject 介面](the-iads-and-idirectoryobject-interfaces.md)
-   [使用 ADSI 存取屬性](accessing-attributes-with-adsi.md)
-   [使用 ADSI 修改屬性](modifying-attributes-with-adsi.md)
-   [使用 IADsProperty 介面直接存取屬性快取](accessing-the-property-cache-directly-with-the-iadsproperty-interfaces.md)
-   [ADSI 屬性語法](adsi-attribute-syntax.md)

 

 