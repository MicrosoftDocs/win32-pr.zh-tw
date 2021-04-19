---
title: 'IWMPStringCollection2 (VB 和 C ) 介面 (h.264. h) '
description: 提供補充 IWMPStringCollection 介面的方法。
ms.assetid: be93ff47-7f76-4b5e-ad30-3094a75147c8
keywords:
- IWMPStringCollection2 (VB 和 C ) 介面 Windows Media Player
- IWMPStringCollection2 (VB 和 C ) 介面 Windows Media Player，說明
topic_type:
- apiref
api_name:
- IWMPStringCollection2 (VB and C )
api_location:
- wmp.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 184e1a16ea0e6b33cc5b67eaeac6b050e5cda97a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995345"
---
# <a name="iwmpstringcollection2-vb-and-c-interface"></a><span data-ttu-id="ac807-105">IWMPStringCollection2 (VB 和 c # ) 介面</span><span class="sxs-lookup"><span data-stu-id="ac807-105">IWMPStringCollection2 (VB and C#) interface</span></span>

<span data-ttu-id="ac807-106">提供補充 **IWMPStringCollection** 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="ac807-106">Provides methods that supplement the **IWMPStringCollection** interface.</span></span>

## <a name="members"></a><span data-ttu-id="ac807-107">成員</span><span class="sxs-lookup"><span data-stu-id="ac807-107">Members</span></span>

<span data-ttu-id="ac807-108">**IWMPStringCollection2 (VB 和 c # )** 介面都有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ac807-108">The **IWMPStringCollection2 (VB and C#)** interface has these types of members:</span></span>

-   [<span data-ttu-id="ac807-109">方法</span><span class="sxs-lookup"><span data-stu-id="ac807-109">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ac807-110">方法</span><span class="sxs-lookup"><span data-stu-id="ac807-110">Methods</span></span>

<span data-ttu-id="ac807-111">**IWMPStringCollection2 (VB 和 c # )** 介面都有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ac807-111">The **IWMPStringCollection2 (VB and C#)** interface has these methods.</span></span>



| <span data-ttu-id="ac807-112">方法</span><span class="sxs-lookup"><span data-stu-id="ac807-112">Method</span></span>                                                                                                                 | <span data-ttu-id="ac807-113">描述</span><span class="sxs-lookup"><span data-stu-id="ac807-113">Description</span></span>                                                                                                                           |
|:-----------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac807-114">**getAttributeCountByType**</span><span class="sxs-lookup"><span data-stu-id="ac807-114">**getAttributeCountByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getattributecountbytype--vb-and-c.md) | <span data-ttu-id="ac807-115">傳回與指定的字串集合專案索引、屬性名稱和語言相關聯的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="ac807-115">Returns the number of attributes associated with the specified string collection item index, attribute name, and language.</span></span><br/> |
| [<span data-ttu-id="ac807-116">**getItemInfo**</span><span class="sxs-lookup"><span data-stu-id="ac807-116">**getItemInfo**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfo--vb-and-c.md)                         | <span data-ttu-id="ac807-117">傳回對應至指定之字串集合專案索引和名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="ac807-117">Returns the string corresponding to the specified string collection item index and name.</span></span><br/>                                   |
| [<span data-ttu-id="ac807-118">**getItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="ac807-118">**getItemInfoByType**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-getiteminfobytype--vb-and-c.md)             | <span data-ttu-id="ac807-119">傳回對應至指定之字串集合專案索引、名稱、語言和屬性索引的值。</span><span class="sxs-lookup"><span data-stu-id="ac807-119">Returns the value corresponding to the specified string collection item index, name, language, and attribute index.</span></span><br/>        |
| [<span data-ttu-id="ac807-120">**isIdentical**</span><span class="sxs-lookup"><span data-stu-id="ac807-120">**isIdentical**</span></span>](wmplibiwmpstringcollection2-iwmpstringcollection2-isidentical--vb-and-c.md)                         | <span data-ttu-id="ac807-121">傳回值，指出提供的物件是否與目前的物件相同。</span><span class="sxs-lookup"><span data-stu-id="ac807-121">Returns a value indicating whether the supplied object is the same as the current one.</span></span><br/>                                     |



 

<span data-ttu-id="ac807-122">藉由轉換 [**IWMPMediaCollection. getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection)方法所傳回的值來取得 **IWMPStringCollection2** 介面。</span><span class="sxs-lookup"><span data-stu-id="ac807-122">Get an **IWMPStringCollection2** interface by casting the value returned by the [**IWMPMediaCollection.getAttributeStringCollection**](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getattributestringcollection) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ac807-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac807-123">Requirements</span></span>



| <span data-ttu-id="ac807-124">需求</span><span class="sxs-lookup"><span data-stu-id="ac807-124">Requirement</span></span> | <span data-ttu-id="ac807-125">值</span><span class="sxs-lookup"><span data-stu-id="ac807-125">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="ac807-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ac807-126">Header</span></span><br/> | <dl> <span data-ttu-id="ac807-127"><dt>Wmp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac807-127"><dt>Wmp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ac807-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac807-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac807-129">**適用于 Visual Basic .NET 和 C 的介面#**</span><span class="sxs-lookup"><span data-stu-id="ac807-129">**Interfaces for Visual Basic .NET and C#**</span></span>](interfaces-for-visual-basic--net-and-c.md)
</dt> <dt>

[<span data-ttu-id="ac807-130">**IWMPStringCollection 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="ac807-130">**IWMPStringCollection Interface (VB and C#)**</span></span>](iwmpstringcollection--vb-and-c.md)
</dt> </dl>

 

 





