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
# <a name="reading-the-abstract-schema"></a><span data-ttu-id="4daa5-104">讀取抽象架構</span><span class="sxs-lookup"><span data-stu-id="4daa5-104">Reading the Abstract Schema</span></span>

<span data-ttu-id="4daa5-105">本主題提供從抽象架構讀取的程式碼範例和指導方針，以提供儲存在架構容器的 **attributeSchema** 和 **classSchema** 物件中的資料子集。</span><span class="sxs-lookup"><span data-stu-id="4daa5-105">This topic provides a code example and guidelines for reading from the abstract schema, which provides a subset of the data stored in the **attributeSchema** and **classSchema** objects in the schema container.</span></span> <span data-ttu-id="4daa5-106">若要取出抽象架構中無法使用的資料，請直接從架構容器讀取資料，如 [讀取 attributeSchema 和 ClassSchema 物件](reading-attributeschema-and-classschema-objects.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="4daa5-106">To retrieve data that is unavailable in the abstract schema, read the data directly from the schema container as described in [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="4daa5-107">使用 "LDAP://schema" 系結字串來系結至抽象架構上的 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 指標。</span><span class="sxs-lookup"><span data-stu-id="4daa5-107">Use the "LDAP://schema" binding string to bind to an [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) pointer on the abstract schema.</span></span> <span data-ttu-id="4daa5-108">使用這個指標來列舉抽象架構中的類別、屬性和語法專案。</span><span class="sxs-lookup"><span data-stu-id="4daa5-108">Use this pointer to enumerate the class, attribute, and syntax entries in the abstract schema.</span></span> <span data-ttu-id="4daa5-109">您也可以使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) 的方法來取出個別專案。</span><span class="sxs-lookup"><span data-stu-id="4daa5-109">You can also use the [**IADsContainer.GetObject**](/windows/desktop/api/iads/nf-iads-iadscontainer-getobject) method to retrieve individual entries.</span></span>


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



<span data-ttu-id="4daa5-110">使用類似的系結字串 "LDAP://schema/ <object> "，直接系結至抽象架構中的類別或屬性專案。</span><span class="sxs-lookup"><span data-stu-id="4daa5-110">Use a similar binding string, "LDAP://schema/<object>", to bind directly to a class or attribute entry in the abstract schema.</span></span> <span data-ttu-id="4daa5-111">在此字串中，" &lt; object &gt; " 是類別或屬性的 **lDAPDisplayName** 。</span><span class="sxs-lookup"><span data-stu-id="4daa5-111">In this string, "&lt;object&gt;" is the **lDAPDisplayName** of a class or attribute.</span></span> <span data-ttu-id="4daa5-112">針對類別系結至 [**得到 iadsclass**](/windows/desktop/api/iads/nn-iads-iadsclass) 介面;針對屬性，系結至 [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) 介面。</span><span class="sxs-lookup"><span data-stu-id="4daa5-112">For classes bind to the [**IADsClass**](/windows/desktop/api/iads/nn-iads-iadsclass) interface; for attributes, bind to [**IADsProperty**](/windows/desktop/api/iads/nn-iads-iadsproperty) interface.</span></span>


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



<span data-ttu-id="4daa5-113">此外， [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 介面會提供 [**IADs 架構**](/windows/desktop/ADSI/iads-property-methods) 屬性。</span><span class="sxs-lookup"><span data-stu-id="4daa5-113">In addition, the [**IADs**](/windows/desktop/api/iads/nn-iads-iads) interface provides the [**IADs.Schema**](/windows/desktop/ADSI/iads-property-methods) property.</span></span> <span data-ttu-id="4daa5-114">這個屬性會以抽象架構系結字串格式傳回物件類別的 ADsPath。</span><span class="sxs-lookup"><span data-stu-id="4daa5-114">This property returns the ADsPath for the object class in abstract schema binding string format.</span></span> <span data-ttu-id="4daa5-115">如果您有物件的 **IADs** 指標，您可以使用從 **IADs** 傳回的 ADsPath 系結至抽象架構中的類別。</span><span class="sxs-lookup"><span data-stu-id="4daa5-115">If you have an **IADs** pointer to an object, you can bind to its class in the abstract schema using the ADsPath returned from **IADs.Schema**.</span></span>

<span data-ttu-id="4daa5-116">針對類別，下表列出抽象架構所提供的索引鍵屬性。</span><span class="sxs-lookup"><span data-stu-id="4daa5-116">For classes, the following table lists key properties provided by the abstract schema.</span></span>



| <span data-ttu-id="4daa5-117">屬性</span><span class="sxs-lookup"><span data-stu-id="4daa5-117">Property</span></span>                                                             | <span data-ttu-id="4daa5-118">意義</span><span class="sxs-lookup"><span data-stu-id="4daa5-118">Meaning</span></span>                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="4daa5-119">**得到 iadsclass 抽象**</span><span class="sxs-lookup"><span data-stu-id="4daa5-119">**IADsClass.Abstract**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)            | <span data-ttu-id="4daa5-120">指出這是否為抽象類別。</span><span class="sxs-lookup"><span data-stu-id="4daa5-120">Indicates whether this is an abstract class.</span></span>                                                                                                                                                                                                                                            |
| [<span data-ttu-id="4daa5-121">**得到 iadsclass 輔助**</span><span class="sxs-lookup"><span data-stu-id="4daa5-121">**IADsClass.Auxiliary**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="4daa5-122">指出這是否為輔助類別。</span><span class="sxs-lookup"><span data-stu-id="4daa5-122">Indicates whether this is an auxiliary class.</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="4daa5-123">**得到 iadsclass. AuxDerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="4daa5-123">**IADsClass.AuxDerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)      | <span data-ttu-id="4daa5-124">此類別衍生自的輔助類別陣列。</span><span class="sxs-lookup"><span data-stu-id="4daa5-124">Array of auxiliary classes this class derives from.</span></span>                                                                                                                                                                                                                                     |
| [<span data-ttu-id="4daa5-125">**得到 iadsclass 容器**</span><span class="sxs-lookup"><span data-stu-id="4daa5-125">**IADsClass.Container**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)           | <span data-ttu-id="4daa5-126">指出此類別的物件是否可以包含其他物件，如果任何類別在其 **possibleSuperiors** 清單中包含此類別，則為 true。</span><span class="sxs-lookup"><span data-stu-id="4daa5-126">Indicates whether objects of this class can contain other objects, which is true if any class includes this class in its list of **possibleSuperiors**.</span></span>                                                                                                                                 |
| [<span data-ttu-id="4daa5-127">**得到 iadsclass. DerivedFrom**</span><span class="sxs-lookup"><span data-stu-id="4daa5-127">**IADsClass.DerivedFrom**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)         | <span data-ttu-id="4daa5-128">衍生自這個類別的類別陣列。</span><span class="sxs-lookup"><span data-stu-id="4daa5-128">Array of classes that this class is derived from.</span></span>                                                                                                                                                                                                                                       |
| [<span data-ttu-id="4daa5-129">**得到 iadsclass. MandatoryProperties**</span><span class="sxs-lookup"><span data-stu-id="4daa5-129">**IADsClass.MandatoryProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods) | <span data-ttu-id="4daa5-130">抓取必須針對類別的實例設定之必要屬性的陣列。</span><span class="sxs-lookup"><span data-stu-id="4daa5-130">Retrieves an array of the mandatory properties that must be set for an instance of the class.</span></span> <span data-ttu-id="4daa5-131">傳回的清單包含類別的所有 **mustContain** 和 **systemMustContain** 值，以及從中衍生的類別，包括超類和輔助類別。</span><span class="sxs-lookup"><span data-stu-id="4daa5-131">The returned list includes all the **mustContain** and **systemMustContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span> |
| [<span data-ttu-id="4daa5-132">**得到 iadsclass OID**</span><span class="sxs-lookup"><span data-stu-id="4daa5-132">**IADsClass.OID**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)                 | <span data-ttu-id="4daa5-133">捕獲類別的 governsID。</span><span class="sxs-lookup"><span data-stu-id="4daa5-133">Retrieves the governsID of the class.</span></span>                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="4daa5-134">**得到 iadsclass. OptionalProperties**</span><span class="sxs-lookup"><span data-stu-id="4daa5-134">**IADsClass.OptionalProperties**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)  | <span data-ttu-id="4daa5-135">抓取可針對類別的實例設定之選擇性屬性的陣列。</span><span class="sxs-lookup"><span data-stu-id="4daa5-135">Retrieves an array of the optional properties that might be set for an instance of the class.</span></span> <span data-ttu-id="4daa5-136">傳回的清單包含類別的所有 **mayContain** 和 **systemMayContain** 值，以及從中衍生的類別，包括超類和輔助類別。</span><span class="sxs-lookup"><span data-stu-id="4daa5-136">The returned list includes all the **mayContain** and **systemMayContain** values for the class and the classes from which it is derived, including superclasses and auxiliary classes.</span></span>   |
| [<span data-ttu-id="4daa5-137">**得到 iadsclass. PossibleSuperiors**</span><span class="sxs-lookup"><span data-stu-id="4daa5-137">**IADsClass.PossibleSuperiors**</span></span>](/windows/desktop/ADSI/iadsclass-property-methods)   | <span data-ttu-id="4daa5-138">抓取類別的 **possibleSuperiors** 值陣列，這個陣列表示可以包含這個類別之物件的物件類別。</span><span class="sxs-lookup"><span data-stu-id="4daa5-138">Retrieves an array of the **possibleSuperiors** values for the class, which indicates the object classes that can contain objects of this class.</span></span>                                                                                                                                        |



 

<span data-ttu-id="4daa5-139">抽象架構會儲存在架構容器的 **ubschema** 物件中。</span><span class="sxs-lookup"><span data-stu-id="4daa5-139">The abstract schema is stored in the **subSchema** object in the schema container.</span></span> <span data-ttu-id="4daa5-140">若要取得 **ubschema** 物件的辨別名稱，請系結至 rootDSE 並讀取 **subSchemaSubEntry** 屬性，如 [無伺服器系結和 rootDSE](serverless-binding-and-rootdse.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="4daa5-140">To get the distinguished name of the **subSchema** object, bind to rootDSE and read the **subSchemaSubEntry** attribute, as described in [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span> <span data-ttu-id="4daa5-141">請注意，藉由系結至 "LDAP://schema"，而不是直接系結至 **ubschema** 物件，來讀取抽象架構會更有效率。</span><span class="sxs-lookup"><span data-stu-id="4daa5-141">Be aware that it is more efficient to read the abstract schema by binding to "LDAP://schema", than by binding directly to the **subSchema** object.</span></span>

 

 