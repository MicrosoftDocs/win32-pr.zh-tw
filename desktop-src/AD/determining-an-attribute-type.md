---
title: 判斷屬性類型
description: AttributeSchema 物件的 systemFlags 屬性包含一組旗標，這些旗標表示屬性物件的各種特性，例如屬性是否為已建立或非複寫。
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- 判斷屬性類型 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023254"
---
# <a name="determining-an-attribute-type"></a><span data-ttu-id="313e6-104">判斷屬性類型</span><span class="sxs-lookup"><span data-stu-id="313e6-104">Determining an Attribute Type</span></span>

<span data-ttu-id="313e6-105">[**AttributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件的 [**systemFlags**](/windows/desktop/ADSchema/a-systemflags)屬性包含一組旗標，這些旗標表示屬性物件的各種特性，例如屬性是否為已建立或非複寫。</span><span class="sxs-lookup"><span data-stu-id="313e6-105">The [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute of an [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object contains a set of flags that indicate various qualities of the attribute object, such as whether the attribute is constructed or non-replicated.</span></span> <span data-ttu-id="313e6-106">下表列出 **systemFlags** 屬性的旗標，其會影響屬性的儲存類型。</span><span class="sxs-lookup"><span data-stu-id="313e6-106">The following table lists the flags of the **systemFlags** attribute that affect the storage type of the attribute.</span></span> 

| <span data-ttu-id="313e6-107">旗標值</span><span class="sxs-lookup"><span data-stu-id="313e6-107">Flag value</span></span> | <span data-ttu-id="313e6-108">Description</span><span class="sxs-lookup"><span data-stu-id="313e6-108">Description</span></span>                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="313e6-109">0x00000001</span><span class="sxs-lookup"><span data-stu-id="313e6-109">0x00000001</span></span> | <span data-ttu-id="313e6-110">如果 [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) 屬性中有此旗標，則不會複寫屬性。</span><span class="sxs-lookup"><span data-stu-id="313e6-110">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is not replicated.</span></span> |
| <span data-ttu-id="313e6-111">0x00000004</span><span class="sxs-lookup"><span data-stu-id="313e6-111">0x00000004</span></span> | <span data-ttu-id="313e6-112">如果 [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) 屬性中有此旗標，則會建立屬性。</span><span class="sxs-lookup"><span data-stu-id="313e6-112">If this flag is present in the [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) attribute, the attribute is constructed.</span></span>    |



 

<span data-ttu-id="313e6-113">您可以建立查詢字串，以用來查詢已建立或非複寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="313e6-113">It is possible to construct a query string that can be used to query for constructed or non-replicated attributes.</span></span> <span data-ttu-id="313e6-114">例如，下列查詢字串會尋找所有非複寫的 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) 物件。</span><span class="sxs-lookup"><span data-stu-id="313e6-114">For example, the following query string finds all non-replicated [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) objects.</span></span> <span data-ttu-id="313e6-115">請注意，查詢字串需要值的十進位對等專案，而不是值的十六進位對等專案。</span><span class="sxs-lookup"><span data-stu-id="313e6-115">Be aware that the query string requires the decimal equivalent of the value, not the hexadecimal equivalent of the value.</span></span> <span data-ttu-id="313e6-116">如需此查詢字串所使用之比對規則 OID 的詳細資訊，請參閱 [如何指定比較值](how-to-specify-comparison-values.md)。</span><span class="sxs-lookup"><span data-stu-id="313e6-116">For more information about the matching rule OID used by this query string, see [How to Specify Comparison Values](how-to-specify-comparison-values.md).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



<span data-ttu-id="313e6-117">每個屬性之 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件的 [**searchFlags**](/windows/desktop/ADSchema/a-searchflags)屬性會定義屬性是否已編制索引;索引屬性的值為1，非索引屬性的值為0。</span><span class="sxs-lookup"><span data-stu-id="313e6-117">The [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is indexed; an indexed attribute has a value of 1, a non-indexed attribute has a value of 0.</span></span> <span data-ttu-id="313e6-118">例如，下列查詢字串會尋找代表已編制索引之屬性的 **attributeSchema** 物件。</span><span class="sxs-lookup"><span data-stu-id="313e6-118">For example, the following query string finds the **attributeSchema** objects representing indexed attributes.</span></span>


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



<span data-ttu-id="313e6-119">每個屬性之 [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema)物件的 [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset)屬性會定義屬性是否要複寫至通用類別目錄。</span><span class="sxs-lookup"><span data-stu-id="313e6-119">The [**isMemberOfPartialAttributeSet**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) attribute of each attribute's [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) object defines whether an attribute is replicated to the global catalog.</span></span> <span data-ttu-id="313e6-120">如果屬性是通用類別目錄的成員，則這個屬性的值為 **TRUE** ，如果屬性不在通用類別目錄中，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="313e6-120">This attribute has a value of **TRUE** if the attribute is a member of the global catalog or **FALSE** if the attributes is not in the global catalog.</span></span> <span data-ttu-id="313e6-121">例如，下列查詢字串會搜尋已複寫至通用類別目錄的 **attributeSchema** 物件。</span><span class="sxs-lookup"><span data-stu-id="313e6-121">For example, the following query string searches the **attributeSchema** objects that are replicated to the global catalog.</span></span>


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 