---
title: ColumnID
description: ColumnID 屬性會指定或抓取播放清單控制項中的資料行識別碼。
ms.assetid: c7b51f0b-e347-46be-a26d-aaa0bce83e0c
keywords:
- ColumnID Windows Media Player 的資料行
topic_type:
- apiref
api_name:
- COLUMN.columnID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4bc9aa6485443ae17486616b030b903a911a8e9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993433"
---
# <a name="columncolumnid"></a><span data-ttu-id="43cc2-104">ColumnID</span><span class="sxs-lookup"><span data-stu-id="43cc2-104">COLUMN.columnID</span></span>

<span data-ttu-id="43cc2-105">**ColumnID** 屬性會指定或抓取 **播放清單** 控制項中的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="43cc2-105">The **columnID** attribute specifies or retrieves a column ID in the **PLAYLIST** control.</span></span>

``` syntax
        elementID.columnID
```

## <a name="possible-values"></a><span data-ttu-id="43cc2-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="43cc2-106">Possible Values</span></span>

<span data-ttu-id="43cc2-107">此屬性是讀取/寫入 **字串**。</span><span class="sxs-lookup"><span data-stu-id="43cc2-107">This attribute is a read/write **String**.</span></span>

## <a name="remarks"></a><span data-ttu-id="43cc2-108">備註</span><span class="sxs-lookup"><span data-stu-id="43cc2-108">Remarks</span></span>

<span data-ttu-id="43cc2-109">**ColumnID** 值與 **媒體** 物件上的 **getItemInfo** 方法所使用的值相同。</span><span class="sxs-lookup"><span data-stu-id="43cc2-109">The **columnID** values are the same values used with the **getItemInfo** method on a **Media** object.</span></span> <span data-ttu-id="43cc2-110">您可以使用 *媒體* 取得清單。**attributeCount** 屬性，用來判斷指定之 **媒體** 物件的可用屬性數目。</span><span class="sxs-lookup"><span data-stu-id="43cc2-110">A list can be obtained by using the *Media*.**attributeCount** property to determine the number of attributes available for a given **Media** object.</span></span> <span data-ttu-id="43cc2-111">然後，您可以將索引號碼與 *媒體* 搭配使用。**getAttributeName** 方法，可決定屬性的名稱，然後再傳遞給 *媒體*。**getItemInfo**。</span><span class="sxs-lookup"><span data-stu-id="43cc2-111">Index numbers can then be used with the *Media*.**getAttributeName** method to determine the names of the attributes, which can in turn be passed to *Media*.**getItemInfo**.</span></span> <span data-ttu-id="43cc2-112">**ColumnID** 屬性只能設定為這些值，但可能不會由 *媒體* 傳回的某些值除外。**getAttributeName**。</span><span class="sxs-lookup"><span data-stu-id="43cc2-112">The **columnID** property can only be set to these values, with the exception of some values that may not be returned by *Media*.**getAttributeName**.</span></span> <span data-ttu-id="43cc2-113">下面會列出這些值。</span><span class="sxs-lookup"><span data-stu-id="43cc2-113">These values are listed below.</span></span>



| <span data-ttu-id="43cc2-114">值</span><span class="sxs-lookup"><span data-stu-id="43cc2-114">Value</span></span>     | <span data-ttu-id="43cc2-115">描述</span><span class="sxs-lookup"><span data-stu-id="43cc2-115">Description</span></span>                                                                        |
|-----------|------------------------------------------------------------------------------------|
| <span data-ttu-id="43cc2-116">NAME</span><span class="sxs-lookup"><span data-stu-id="43cc2-116">name</span></span>      | <span data-ttu-id="43cc2-117">顯示 **媒體** 物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="43cc2-117">Displays the name of the **Media** object.</span></span>                                         |
| <span data-ttu-id="43cc2-118">duration</span><span class="sxs-lookup"><span data-stu-id="43cc2-118">duration</span></span>  | <span data-ttu-id="43cc2-119">顯示 **媒體** 物件的持續時間。</span><span class="sxs-lookup"><span data-stu-id="43cc2-119">Displays the duration of the **Media** object.</span></span>                                     |
| <span data-ttu-id="43cc2-120">sourceURL</span><span class="sxs-lookup"><span data-stu-id="43cc2-120">sourceURL</span></span> | <span data-ttu-id="43cc2-121">顯示 **媒體** 物件的 URL。</span><span class="sxs-lookup"><span data-stu-id="43cc2-121">Displays the URL of the **Media** object.</span></span>                                          |
| <span data-ttu-id="43cc2-122">status</span><span class="sxs-lookup"><span data-stu-id="43cc2-122">status</span></span>    | <span data-ttu-id="43cc2-123">顯示覆制檔案的狀態。</span><span class="sxs-lookup"><span data-stu-id="43cc2-123">Displays the status of copying files.</span></span>                                              |
| <span data-ttu-id="43cc2-124">{1}size{2}</span><span class="sxs-lookup"><span data-stu-id="43cc2-124">size</span></span>      | <span data-ttu-id="43cc2-125">顯示 **媒體** 物件所代表之檔案的大小。</span><span class="sxs-lookup"><span data-stu-id="43cc2-125">Displays the size of the file that the **Media** object represents.</span></span>                |
| <span data-ttu-id="43cc2-126">擴充功能</span><span class="sxs-lookup"><span data-stu-id="43cc2-126">extension</span></span> | <span data-ttu-id="43cc2-127">顯示 **媒體** 物件所代表之檔案的副檔名。</span><span class="sxs-lookup"><span data-stu-id="43cc2-127">Displays the file name extension of the file that the **Media** object represents.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="43cc2-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="43cc2-128">Requirements</span></span>



| <span data-ttu-id="43cc2-129">需求</span><span class="sxs-lookup"><span data-stu-id="43cc2-129">Requirement</span></span> | <span data-ttu-id="43cc2-130">值</span><span class="sxs-lookup"><span data-stu-id="43cc2-130">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="43cc2-131">版本</span><span class="sxs-lookup"><span data-stu-id="43cc2-131">Version</span></span><br/> | <span data-ttu-id="43cc2-132">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="43cc2-132">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="43cc2-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43cc2-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43cc2-134">**COLUMN 元素**</span><span class="sxs-lookup"><span data-stu-id="43cc2-134">**COLUMN Element**</span></span>](column-element.md)
</dt> <dt>

[<span data-ttu-id="43cc2-135">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="43cc2-135">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="43cc2-136">**AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="43cc2-136">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="43cc2-137">**GetAttributeName**</span><span class="sxs-lookup"><span data-stu-id="43cc2-137">**Media.getAttributeName**</span></span>](media-getattributename.md)
</dt> <dt>

[<span data-ttu-id="43cc2-138">**GetItemInfo**</span><span class="sxs-lookup"><span data-stu-id="43cc2-138">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> </dl>

 

 





