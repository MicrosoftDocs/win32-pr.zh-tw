---
title: 讀取抽象架構
description: 本主題提供從抽象架構讀取的程式碼範例和指導方針，以提供儲存在架構容器的 attributeSchema 和 classSchema 物件中的資料子集。
ms.assetid: f31fc0ae-048f-413c-9370-96367dc68df8
ms.tgt_platform: multiple
keywords:
- 架構 Active Directory，讀取抽象架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d7fadba33bcc5e93bf2b9e89934e8b440d559b
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842031"
---
# <a name="reading-the-abstract-schema"></a>讀取抽象架構

本主題提供從抽象架構讀取的程式碼範例和指導方針，以提供儲存在架構容器的 **attributeSchema** 和 **classSchema** 物件中的資料子集。 若要取出抽象架構中無法使用的資料，請直接從架構容器讀取資料，如 [讀取 attributeSchema 和 ClassSchema 物件](reading-attributeschema-and-classschema-objects.md)中所述。

使用 "LDAP://schema" 系結字串來系結至抽象架構上的 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 指標。 使用這個指標來列舉抽象架構中的類別、屬性和語法專案。 您也可以使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) 的方法來取出個別專案。


```C++
// Bind to the abstract schema.
IADsContainer *pAbsSchema = NULL;
hr = ADsGetObject(L"LDAP://schema",
                  IID_IADsContainer,
                  (void**)&pAbsSchema);
```




```VB
' Bind to the abstract schema.
Dim adschema As IADsContainer
Set adschema = GetObject("LDAP://schema")
```



使用類似的系結字串 "LDAP://schema/ <object> "，直接系結至抽象架構中的類別或屬性專案。 在此字串中，" &lt; object &gt; " 是類別或屬性的 **lDAPDisplayName** 。 針對類別系結至 [**得到 iadsclass**](/windows/desktop/api/iads/nn-iads-iadsclass) 介面;針對屬性，系結至 [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) 介面。


```C++
// Bind to the user class entry in the abstract schema.
IADsClass *pClass;
hr = ADsGetObject(L"LDAP://schema/user",
                  IID_IADsClass,
                  (void**)&pClass);
```




```VB
Bind to the user class entry in the abstract schema.
Dim userclass As IADsClass
Set userclass = GetObject("LDAP://schema/user")
```



此外， [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 介面會提供 [**IADs 架構**](/windows/desktop/ADSI/iads-property-methods) 屬性。 這個屬性會以抽象架構系結字串格式傳回物件類別的 ADsPath。 如果您有物件的 **IADs** 指標，您可以使用從 **IADs** 傳回的 ADsPath 系結至抽象架構中的類別。

針對類別，下表列出抽象架構所提供的索引鍵屬性。



| 屬性                                                             | 意義                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**得到 iadsclass 抽象**](/windows/desktop/ADSI/iadsclass-property-methods)            | 指出這是否為抽象類別。                                                                                                                                                                                                                                            |
| [**得到 iadsclass 輔助**](/windows/desktop/ADSI/iadsclass-property-methods)           | 指出這是否為輔助類別。                                                                                                                                                                                                                                           |
| [**得到 iadsclass. AuxDerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)      | 此類別衍生自的輔助類別陣列。                                                                                                                                                                                                                                     |
| [**得到 iadsclass 容器**](/windows/desktop/ADSI/iadsclass-property-methods)           | 指出此類別的物件是否可以包含其他物件，如果任何類別在其 **possibleSuperiors** 清單中包含此類別，則為 true。                                                                                                                                 |
| [**得到 iadsclass. DerivedFrom**](/windows/desktop/ADSI/iadsclass-property-methods)         | 衍生自這個類別的類別陣列。                                                                                                                                                                                                                                       |
| [**得到 iadsclass. MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) | 抓取必須針對類別的實例設定之必要屬性的陣列。 傳回的清單包含類別的所有 **mustContain** 和 **systemMustContain** 值，以及從中衍生的類別，包括超類和輔助類別。 |
| [**得到 iadsclass OID**](/windows/desktop/ADSI/iadsclass-property-methods)                 | 捕獲類別的 governsID。                                                                                                                                                                                                                                                   |
| [**得到 iadsclass. OptionalProperties**](/windows/desktop/ADSI/iadsclass-property-methods)  | 抓取可針對類別的實例設定之選擇性屬性的陣列。 傳回的清單包含類別的所有 **mayContain** 和 **systemMayContain** 值，以及從中衍生的類別，包括超類和輔助類別。   |
| [**得到 iadsclass. PossibleSuperiors**](/windows/desktop/ADSI/iadsclass-property-methods)   | 抓取類別的 **possibleSuperiors** 值陣列，這個陣列表示可以包含這個類別之物件的物件類別。                                                                                                                                        |



 

抽象架構會儲存在架構容器的 **ubschema** 物件中。 若要取得 **ubschema** 物件的辨別名稱，請系結至 rootDSE 並讀取 **subSchemaSubEntry** 屬性，如 [無伺服器系結和 rootDSE](serverless-binding-and-rootdse.md)中所述。 請注意，藉由系結至 "LDAP://schema"，而不是直接系結至 **ubschema** 物件，來讀取抽象架構會更有效率。

 

 