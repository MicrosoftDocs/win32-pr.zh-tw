---
title: 查詢類別1或2個架構物件
description: AttributeSchema 和 classSchema 物件的 systemFlags 屬性是一個整數位遮罩，其中包含的旗標會指出屬性或類別的其他系統品質。
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- 查詢類別1或2個架構物件 AD
- 物件 AD，查詢類別1或2個架構物件
- 架構 AD，查詢類別1或2個架構物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314620"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a><span data-ttu-id="63529-106">查詢類別1或2個架構物件</span><span class="sxs-lookup"><span data-stu-id="63529-106">Querying for Category 1 or 2 Schema Objects</span></span>

<span data-ttu-id="63529-107">**AttributeSchema** 和 **ClassSchema** 物件的 **systemFlags** 屬性是一個整數位遮罩，其中包含的旗標會指出屬性或類別的其他系統品質。</span><span class="sxs-lookup"><span data-stu-id="63529-107">The **systemFlags** attribute of **attributeSchema** and **classSchema** objects is an integer bitmask that contains flags that indicate additional system qualities of the attribute or class.</span></span> <span data-ttu-id="63529-108">[**ADS \_ SYSTEMFLAG \_ ENUM**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum)列舉包含的值，會對應至您可以在 **systemFlags** 屬性中設定的位。</span><span class="sxs-lookup"><span data-stu-id="63529-108">The [**ADS\_SYSTEMFLAG\_ENUM**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) enumeration contains values that correspond to the bits you can set in the **systemFlags** attribute.</span></span> <span data-ttu-id="63529-109">您還無法設定額外的 **systemFlags** 位，例如，表示屬性或類別為類別1或類別2的0x10 位。</span><span class="sxs-lookup"><span data-stu-id="63529-109">There are additional **systemFlags** bits that you cannot set, such as the 0x10 bit which indicates whether the attribute or class is category 1 or category 2.</span></span> <span data-ttu-id="63529-110">0x10 位是針對類別1物件所設定，也就是包含在系統所包含的基底架構中的類別和屬性。</span><span class="sxs-lookup"><span data-stu-id="63529-110">The 0x10 bit is set for category 1 objects, which are the classes and attributes included in the base schema included with the system.</span></span> <span data-ttu-id="63529-111">未針對類別2屬性和類別設定位，這是架構的延伸。</span><span class="sxs-lookup"><span data-stu-id="63529-111">The bit is not set for category 2 attributes and classes, which are extensions to the schema.</span></span> <span data-ttu-id="63529-112">如果 **attributeSchema** 或 **classSchema** 物件上沒有 **systemFlags** 屬性，則為類別2。</span><span class="sxs-lookup"><span data-stu-id="63529-112">If no **systemFlags** property exists on an **attributeSchema** or **classSchema** object, it is category 2.</span></span>

<span data-ttu-id="63529-113">您可以使用 **LDAP \_ 比對 \_ 規則 \_ 位 \_ 和比** 對規則來搜尋在 **systemFlags** 屬性中設定了0x10 旗標的物件。</span><span class="sxs-lookup"><span data-stu-id="63529-113">The **LDAP\_MATCHING\_RULE\_BIT\_AND** matching rule can be used to search for objects that have the 0x10 flag set in the **systemFlags** attribute.</span></span> <span data-ttu-id="63529-114">如需詳細資訊，請參閱 [搜尋篩選語法](/windows/desktop/ADSI/search-filter-syntax)。</span><span class="sxs-lookup"><span data-stu-id="63529-114">For more information, see [Search Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).</span></span>

## <a name="querying-for-category-1"></a><span data-ttu-id="63529-115">查詢類別1</span><span class="sxs-lookup"><span data-stu-id="63529-115">Querying for Category 1</span></span>

<span data-ttu-id="63529-116">下列查詢字串會搜尋類別1屬性 (**attributeSchema** 物件，並在 **systemFlags** 屬性) 中設定0x10 位。</span><span class="sxs-lookup"><span data-stu-id="63529-116">The following query string searches for category 1 attributes (**attributeSchema** objects with the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



<span data-ttu-id="63529-117">請注意，在上述範例中，LDAP 查詢語法需要十進位值;因此，旗標的十六進位值必須轉換成 decimal。</span><span class="sxs-lookup"><span data-stu-id="63529-117">Be aware that, in the example above, the LDAP query syntax requires decimal values; therefore, the hex value of the flag must be converted to decimal.</span></span> <span data-ttu-id="63529-118">在此情況下，類別1位為0x10，因此篩選值必須指定為16。</span><span class="sxs-lookup"><span data-stu-id="63529-118">In this case, category 1 bit is 0x10 so the filter value must be specified as 16.</span></span>

## <a name="querying-for-category-2"></a><span data-ttu-id="63529-119">查詢類別2</span><span class="sxs-lookup"><span data-stu-id="63529-119">Querying for Category 2</span></span>

<span data-ttu-id="63529-120">下列查詢字串會在 [ **systemFlags** ] 屬性) 中， (**attributeSchema** 未設定0x10 位的物件來搜尋類別2屬性。</span><span class="sxs-lookup"><span data-stu-id="63529-120">The following query string searches for category 2 attributes (**attributeSchema** objects that do not have the 0x10 bit set in the **systemFlags** property).</span></span>


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



<span data-ttu-id="63529-121">請注意，此查詢也會傳回沒有 **systemFlags** 屬性的 **attributeSchema** 物件，因此，隱含地不會設定指定的旗標。</span><span class="sxs-lookup"><span data-stu-id="63529-121">Be aware that this query also returns **attributeSchema** objects that do not have a **systemFlags** property, and, therefore, implicitly do not have the specified flag set.</span></span>

 

 