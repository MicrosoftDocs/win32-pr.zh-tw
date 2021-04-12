---
description: 在 Windows Vista 和更新版本的屬性系統中所使用的屬性是在屬性架構中宣告的。
ms.assetid: 4e301210-df3a-41db-a58e-015ee8d41714
title: 建立自訂屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90849383e25889edf7f3abd4704c36354eff153c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319635"
---
# <a name="creating-custom-properties"></a><span data-ttu-id="9960f-103">建立自訂屬性</span><span class="sxs-lookup"><span data-stu-id="9960f-103">Creating Custom Properties</span></span>

<span data-ttu-id="9960f-104">在 Windows Vista 和更新版本的屬性系統中所使用的屬性是在屬性架構中宣告的。</span><span class="sxs-lookup"><span data-stu-id="9960f-104">Properties used in the property system of Windows Vista and later are declared in property schemas.</span></span> <span data-ttu-id="9960f-105">這些屬性架構是在 XML 檔案中定義，而且會描述屬性的各個層面，包括它的型別 (包括其基本型別的資訊，以及它是否為多重值) 、如何在 Windows UI 中顯示、哪些標籤 (方便使用的使用者易記編輯) 字串，以及在搜尋存放區中快取的方式，以加快存取的速度。</span><span class="sxs-lookup"><span data-stu-id="9960f-105">These property schemas are defined in XML files and describe various aspects of a property including its type (including information on its primitive type and whether it is multi-valued), how it can be displayed in the Windows UI, what kind of labels (user-friendly editing strings) are to be used with it, and how it is cached in the search store for faster access.</span></span> <span data-ttu-id="9960f-106">屬性是透過其正式名稱或其屬性索引鍵 (PKEY) 來識別。</span><span class="sxs-lookup"><span data-stu-id="9960f-106">Properties are identified by their Canonical Name or their Property Key (PKEY).</span></span>

<span data-ttu-id="9960f-107">正式名稱是屬性的讀取者易記名稱，並使用類似于 Microsoft .NET 中所使用的命名空間慣例。</span><span class="sxs-lookup"><span data-stu-id="9960f-107">A canonical name is the reader-friendly name of the property and uses a namespace convention similar to that used in Microsoft .NET.</span></span> <span data-ttu-id="9960f-108">如果系統定義的屬性 (Windows) 中所包含的屬性，則慣例為 `System.GroupName.PropertyName` 。</span><span class="sxs-lookup"><span data-stu-id="9960f-108">For system-defined properties (those that are included with Windows), the convention is `System.GroupName.PropertyName`.</span></span> <span data-ttu-id="9960f-109">請注意，在每個單字開頭用來將字母大寫的 Pascal 大小寫配置，都是在這些名稱中使用。</span><span class="sxs-lookup"><span data-stu-id="9960f-109">Note that the Pascal casing scheme, which capitalizes letters at the beginning of each word, is used in these names.</span></span> <span data-ttu-id="9960f-110">標準名稱會用於不同的位置，包括屬性清單和屬性快取中的資料行名稱。</span><span class="sxs-lookup"><span data-stu-id="9960f-110">Canonical names are used in various places including property lists and column names in the property cache.</span></span> <span data-ttu-id="9960f-111">因此，結構化查詢語言 (SQL)  (SQL) 查詢來取得屬性值。</span><span class="sxs-lookup"><span data-stu-id="9960f-111">They are therefore used in Structured Query Language (SQL) queries to retrieve a property value.</span></span>

<span data-ttu-id="9960f-112">PKEY 是由 GUID 和 **DWORD** 組成的一對值，分別稱為 *formatID* 和 *propID* 。</span><span class="sxs-lookup"><span data-stu-id="9960f-112">A PKEY is a pair of values consisting of a GUID and a **DWORD**, referred to as a *formatID* and *propID* respectively.</span></span> <span data-ttu-id="9960f-113">它是以 [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) 結構表示。</span><span class="sxs-lookup"><span data-stu-id="9960f-113">It is represented by a [**PROPERTYKEY**](/windows/win32/api/wtypes/ns-wtypes-propertykey) structure.</span></span> <span data-ttu-id="9960f-114">大部分的屬性系統 Api 都會接受這些屬性索引鍵。</span><span class="sxs-lookup"><span data-stu-id="9960f-114">Most of the property system APIs accept these property keys.</span></span> <span data-ttu-id="9960f-115">Windows 軟體開發套件 (SDK) 包含標頭檔 Propkey，其中包含每個屬性索引鍵的巨集定義，以及的 `System` 慣例 `PKEY_GroupName_PropertyName` 。</span><span class="sxs-lookup"><span data-stu-id="9960f-115">The Windows Software Development Kit (SDK) includes the header file Propkey.h that includes a macro definition of each of the `System` property keys with the convention of `PKEY_GroupName_PropertyName`.</span></span> <span data-ttu-id="9960f-116">例如， `PKEY_Photo_DateTaken` 是具有標準名稱之屬性的屬性索引鍵 `System.Photo.DateTaken` 。</span><span class="sxs-lookup"><span data-stu-id="9960f-116">For example, `PKEY_Photo_DateTaken` is the property key for the property with canonical name `System.Photo.DateTaken`.</span></span> <span data-ttu-id="9960f-117">屬性值會以 [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) 結構的形式儲存，也就是 OLE 變異類型的延伸。</span><span class="sxs-lookup"><span data-stu-id="9960f-117">Property values are stored in the form of a [**PROPVARIANT**](/windows/win32/api/propidlbase/ns-propidlbase-propvariant) structure, which is an extension of the OLE VARIANT types.</span></span>

<span data-ttu-id="9960f-118">本節包含下列主題，這是建立自訂屬性的整數：</span><span class="sxs-lookup"><span data-stu-id="9960f-118">This section contains the following topic, which is integral to creating custom properties:</span></span>

-   [<span data-ttu-id="9960f-119">瞭解屬性描述架構</span><span class="sxs-lookup"><span data-stu-id="9960f-119">Understanding the Property Description Schema</span></span>](./propdesc-schema-entry.md)

> [!Note]  
> <span data-ttu-id="9960f-120">由於索引子在取用屬性系統架構時可能會遇到的問題，因此您必須謹慎地定義屬性，並策略性地針對第一版的架構來定義屬性。</span><span class="sxs-lookup"><span data-stu-id="9960f-120">Due to potential difficulties that the indexer may have when consuming the property system's schema, it is critical that you define attributes carefully and strategically for the first release of the schema.</span></span> <span data-ttu-id="9960f-121">在架構註冊之後，資料庫的任何變更 (類型、資料行寬度、indexible) 是否都不會反映在資料庫中。</span><span class="sxs-lookup"><span data-stu-id="9960f-121">Any changes to attributes (type, column width, whether indexible) will not be reflected in the database after a schema has been registered.</span></span> <span data-ttu-id="9960f-122">當架構在系統上註冊一次之後，唯一可辨識這些變更的方法就是重建索引，然後註冊新的架構，或是註冊架構，然後為每個後續的版本建立新的屬性。例如 `PKEY_GroupName_PropertyNameV2` ，等 `PKEY_GroupName_PropertyNameV3`) 。</span><span class="sxs-lookup"><span data-stu-id="9960f-122">The only ways to have these changes recognized after the schema has been registered once on a system would be either to rebuild the index and then register the new schema, or to register the schema and then create a new property for each subsequent release; for example `PKEY_GroupName_PropertyNameV2`, `PKEY_GroupName_PropertyNameV3`, and so forth).</span></span> <span data-ttu-id="9960f-123">我們不建議以這種方式建立新的屬性，因為多個額外的資料行可能會影響系統效能。</span><span class="sxs-lookup"><span data-stu-id="9960f-123">We do not recommend creating new properties in this manner, because multiple extraneous columns may impact system performance.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="9960f-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="9960f-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9960f-125">執行屬性處理常式</span><span class="sxs-lookup"><span data-stu-id="9960f-125">Implementing Property Handlers</span></span>](./building-property-handlers.md)
</dt> <dt>

[<span data-ttu-id="9960f-126">屬性描述架構</span><span class="sxs-lookup"><span data-stu-id="9960f-126">Property Description Schema</span></span>](./propdesc-schema-entry.md)
</dt> </dl>

 

 
