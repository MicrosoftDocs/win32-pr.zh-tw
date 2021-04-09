---
title: 尋找要查詢的屬性清單
description: 搜尋特定類別的物件時，您的搜尋篩選中的比較應指定實際存在於該類別物件上的屬性。
ms.assetid: 19d52933-e4b0-414f-9785-871e624da07b
ms.tgt_platform: multiple
keywords:
- 尋找要查詢 AD 的屬性清單
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4b6fb6b4d948a7cbc4d76caba9b78e189324eaa
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681661"
---
# <a name="finding-a-list-of-attributes-to-query"></a><span data-ttu-id="15ddc-104">尋找要查詢的屬性清單</span><span class="sxs-lookup"><span data-stu-id="15ddc-104">Finding a List of Attributes To Query</span></span>

<span data-ttu-id="15ddc-105">搜尋特定類別的物件時，您的搜尋篩選中的比較應指定實際存在於該類別物件上的屬性。</span><span class="sxs-lookup"><span data-stu-id="15ddc-105">When searching for objects of a particular class, comparisons in your search filter should specify attributes that actually exist on the objects of that class.</span></span> <span data-ttu-id="15ddc-106">若要取得特定類別之物件的清單屬性，請系結至抽象架構中的該類別，並取出 [**得到 iadsclass. MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) 和 **得到 iadsclass. OptionalProperties** 屬性。</span><span class="sxs-lookup"><span data-stu-id="15ddc-106">To get the list attributes on an object of a particular class, bind to that class in the abstract schema and retrieve the [**IADsClass.MandatoryProperties**](/windows/desktop/ADSI/iadsclass-property-methods) and **IADsClass.OptionalProperties** properties.</span></span> <span data-ttu-id="15ddc-107">如需詳細資訊，請參閱 [讀取抽象架構](reading-the-abstract-schema.md)。</span><span class="sxs-lookup"><span data-stu-id="15ddc-107">For more information, see [Reading the Abstract Schema](reading-the-abstract-schema.md).</span></span>

<span data-ttu-id="15ddc-108">此外，所有物件都是繼承自 top 抽象類別。</span><span class="sxs-lookup"><span data-stu-id="15ddc-108">In addition, all objects inherit from the top abstract class.</span></span> <span data-ttu-id="15ddc-109">因此， **top** 中的任何屬性都可以存在，但可能不會在任何物件上設定。</span><span class="sxs-lookup"><span data-stu-id="15ddc-109">Therefore, any attribute in **top** can exist, although it may not be set, on any object.</span></span>

<span data-ttu-id="15ddc-110">如果要搜尋通用類別目錄，請務必在通用類別目錄中指定屬性。</span><span class="sxs-lookup"><span data-stu-id="15ddc-110">If searching the global catalog, ensure that you specify attributes in the global catalog.</span></span> <span data-ttu-id="15ddc-111">包含在通用類別目錄中的屬性，其 **attributeSchema** 物件上的 **isMemberOfPartialAttributeSet** 會設定為 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="15ddc-111">Attributes included in the global catalog have the **isMemberOfPartialAttributeSet** set to **TRUE** on their **attributeSchema** objects.</span></span> <span data-ttu-id="15ddc-112">請注意，此資料在抽象架構中無法使用。從架構容器中的 **attributeSchema** 物件讀取。</span><span class="sxs-lookup"><span data-stu-id="15ddc-112">Be aware that this data is not available in the abstract schema; read it from the **attributeSchema** object in the schema container.</span></span>

<span data-ttu-id="15ddc-113">在通用類別目錄中，只有在符合下列兩個條件時，才可以查詢後置連結屬性：首先，屬性已標示為要包含在通用類別目錄中。</span><span class="sxs-lookup"><span data-stu-id="15ddc-113">In the global catalog, a back link attribute can be queried only if both of the following conditions are met: First, the attribute is marked for inclusion in the global catalog.</span></span> <span data-ttu-id="15ddc-114">其次，對應的轉寄連結也會標示為要包含在通用類別目錄中。</span><span class="sxs-lookup"><span data-stu-id="15ddc-114">Second, the corresponding forward link is also marked for inclusion in the global catalog.</span></span> <span data-ttu-id="15ddc-115">這適用于查詢篩選和查詢結果。</span><span class="sxs-lookup"><span data-stu-id="15ddc-115">This applies to query filters as well as query results.</span></span> <span data-ttu-id="15ddc-116">如需詳細資訊，請參閱 [連結的屬性](linked-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="15ddc-116">For more information, see [Linked Attributes](linked-attributes.md).</span></span>

<span data-ttu-id="15ddc-117">此外，也會建立一些大部分在使用者物件上的屬性。</span><span class="sxs-lookup"><span data-stu-id="15ddc-117">In addition, some attributes, mostly on the user object, are constructed.</span></span> <span data-ttu-id="15ddc-118">查詢篩選不能包含已建立的屬性。</span><span class="sxs-lookup"><span data-stu-id="15ddc-118">Query filters cannot contain constructed attributes.</span></span> <span data-ttu-id="15ddc-119">無法在查詢篩選中評估已建立的屬性;不過，它們可以在查詢結果中傳回。</span><span class="sxs-lookup"><span data-stu-id="15ddc-119">Constructed attributes cannot be evaluated in query filters; however, they can be returned in query results.</span></span> <span data-ttu-id="15ddc-120">這適用于所有命名內容和通用類別目錄。</span><span class="sxs-lookup"><span data-stu-id="15ddc-120">This applies to all the naming contexts and the global catalog.</span></span> <span data-ttu-id="15ddc-121">所建立的屬性（attribute）會在 **attributeSchema** 物件的 **systemFlags** 屬性中， (0x00000004) 來 **\_ \_ \_ \_ 建造 SYSTEMFLAG ATTR** 的屬性。</span><span class="sxs-lookup"><span data-stu-id="15ddc-121">Attributes that are constructed have **ADS\_SYSTEMFLAG\_ATTR\_IS\_CONSTRUCTED** (0x00000004) in the **systemFlags** property on their **attributeSchema** objects.</span></span>

> [!Note]  
> <span data-ttu-id="15ddc-122">如需系統隨附的預先定義類別和屬性的詳細資訊，請參閱 [Active Directory Domain Services 參考](active-directory-domain-services-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="15ddc-122">For more information about predefined classes and attributes included with the system, see [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span> <span data-ttu-id="15ddc-123">這些頁面會列出每個物件類別的強制和選擇性屬性。</span><span class="sxs-lookup"><span data-stu-id="15ddc-123">These pages list mandatory and optional attributes of each object class.</span></span> <span data-ttu-id="15ddc-124">若為屬性，參考頁面會指出屬性是否已編制索引、已建立、連結或在通用類別目錄中。</span><span class="sxs-lookup"><span data-stu-id="15ddc-124">For attributes, the reference page indicates whether the attribute is indexed, constructed, linked, or in the global catalog.</span></span>

 

 

 