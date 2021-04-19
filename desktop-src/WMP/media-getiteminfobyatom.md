---
title: GetItemInfoByAtom 方法
description: GetItemInfoByAtom 方法會使用指定的索引編號來抓取屬性的值。
ms.assetid: 6e2dea0c-c722-4737-9e8e-f5cb74156cea
keywords:
- getItemInfoByAtom 方法 Windows Media Player
- getItemInfoByAtom 方法 Windows Media Player，媒體類別
- 媒體類別 Windows Media Player，getItemInfoByAtom 方法
topic_type:
- apiref
api_name:
- Media.getItemInfoByAtom
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf54d2ae177a65e1a71b5726090bba90f4ee4e5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997740"
---
# <a name="mediagetiteminfobyatom-method"></a><span data-ttu-id="b8a2b-106">GetItemInfoByAtom 方法</span><span class="sxs-lookup"><span data-stu-id="b8a2b-106">Media.getItemInfoByAtom method</span></span>

<span data-ttu-id="b8a2b-107">**GetItemInfoByAtom** 方法會使用指定的索引編號來抓取屬性的值。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-107">The **getItemInfoByAtom** method retrieves the value of the attribute with the specified index number.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a2b-108">語法</span><span class="sxs-lookup"><span data-stu-id="b8a2b-108">Syntax</span></span>


```JScript
strRetVal = Media.getItemInfoByAtom(
  index
)
```



## <a name="parameters"></a><span data-ttu-id="b8a2b-109">參數</span><span class="sxs-lookup"><span data-stu-id="b8a2b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b8a2b-110">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b8a2b-110">*index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b8a2b-111">**Number** (**Long**) 指定指定屬性位於可用屬性集合內的索引。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-111">**Number** (**long**) specifying the index at which a given attribute resides within the set of available attributes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b8a2b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="b8a2b-112">Return value</span></span>

<span data-ttu-id="b8a2b-113">這個方法會傳回 **字串** ，表示指定之屬性的值。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-113">This method returns a **String** representing the value of the specified attribute.</span></span> <span data-ttu-id="b8a2b-114">針對其基礎值為 **布林** 值的屬性，它會傳回字串 "true" 或 "false"。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-114">For attributes whose underlying value is **Boolean**, it returns the string "true" or "false".</span></span>

## <a name="remarks"></a><span data-ttu-id="b8a2b-115">備註</span><span class="sxs-lookup"><span data-stu-id="b8a2b-115">Remarks</span></span>

<span data-ttu-id="b8a2b-116">這個方法可以用來使用屬性索引編號來取得特定數位媒體專案的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-116">This method can be used to retrieve metadata for a specific digital media item by using an attribute index number.</span></span> <span data-ttu-id="b8a2b-117">**AttributeCount** 屬性可以用來判斷媒體專案可用的屬性數目。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-117">The **attributeCount** property can be used to determine the number of attributes available for the media item.</span></span>

<span data-ttu-id="b8a2b-118">**MediaCollection** 物件的 **getMediaAtom** 方法也可以用來取得特定屬性的索引。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-118">The **getMediaAtom** method of the **MediaCollection** object can also be used to retrieve the index of a particular attribute.</span></span> <span data-ttu-id="b8a2b-119">這項技術通常比使用大型播放清單時的 **getItemInfo** 或 **getItemInfoByType** 方法更有效率。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-119">This technique is generally more efficient than the **getItemInfo** or **getItemInfoByType** methods when working with large playlists.</span></span>

<span data-ttu-id="b8a2b-120">若要使用此方法，需要有程式庫的讀取權限。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-120">To use this method, read access to the library is required.</span></span> <span data-ttu-id="b8a2b-121">如需詳細資訊，請參閱連結 [庫存取](library-access.md)。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-121">For more information, see [Library Access](library-access.md).</span></span>

<span data-ttu-id="b8a2b-122">如需 Windows Media Player 所支援之屬性的詳細資訊，請參閱 Windows Media Player [屬性參考](attribute-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-122">For information about the attributes supported by Windows Media Player, see the Windows Media Player [Attribute Reference](attribute-reference.md)..</span></span>

<span data-ttu-id="b8a2b-123">**Windows Media Player 10** 行動裝置版：媒體專案的屬性只有在播放時才能使用，除非是透過媒體集合從專案中取出。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-123">**Windows Media Player 10 Mobile:** Attributes for a media item are available only during playback unless they are retrieved from the item through the media collection.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8a2b-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8a2b-124">Requirements</span></span>



| <span data-ttu-id="b8a2b-125">需求</span><span class="sxs-lookup"><span data-stu-id="b8a2b-125">Requirement</span></span> | <span data-ttu-id="b8a2b-126">值</span><span class="sxs-lookup"><span data-stu-id="b8a2b-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b8a2b-127">版本</span><span class="sxs-lookup"><span data-stu-id="b8a2b-127">Version</span></span><br/> | <span data-ttu-id="b8a2b-128">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="b8a2b-128">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="b8a2b-129">DLL</span><span class="sxs-lookup"><span data-stu-id="b8a2b-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="b8a2b-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b8a2b-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8a2b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8a2b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a2b-132">**媒體物件**</span><span class="sxs-lookup"><span data-stu-id="b8a2b-132">**Media Object**</span></span>](media-object.md)
</dt> <dt>

[<span data-ttu-id="b8a2b-133">**AttributeCount**</span><span class="sxs-lookup"><span data-stu-id="b8a2b-133">**Media.attributeCount**</span></span>](media-attributecount.md)
</dt> <dt>

[<span data-ttu-id="b8a2b-134">**GetItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b8a2b-134">**Media.getItemInfo**</span></span>](media-getiteminfo.md)
</dt> <dt>

[<span data-ttu-id="b8a2b-135">**GetItemInfoByType**</span><span class="sxs-lookup"><span data-stu-id="b8a2b-135">**Media.getItemInfoByType**</span></span>](media-getiteminfobytype.md)
</dt> <dt>

[<span data-ttu-id="b8a2b-136">**SetItemInfo**</span><span class="sxs-lookup"><span data-stu-id="b8a2b-136">**Media.setItemInfo**</span></span>](media-setiteminfo.md)
</dt> <dt>

[<span data-ttu-id="b8a2b-137">**MediaCollection.getMediaAtom**</span><span class="sxs-lookup"><span data-stu-id="b8a2b-137">**MediaCollection.getMediaAtom**</span></span>](mediacollection-getmediaatom.md)
</dt> <dt>

[<span data-ttu-id="b8a2b-138">**讀取屬性值**</span><span class="sxs-lookup"><span data-stu-id="b8a2b-138">**Reading Attribute Values**</span></span>](reading-attribute-values.md)
</dt> <dt>

[<span data-ttu-id="b8a2b-139">**設定. mediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b8a2b-139">**Settings.mediaAccessRights**</span></span>](settings-mediaaccessrights.md)
</dt> <dt>

[<span data-ttu-id="b8a2b-140">**設定. requestMediaAccessRights**</span><span class="sxs-lookup"><span data-stu-id="b8a2b-140">**Settings.requestMediaAccessRights**</span></span>](settings-requestmediaaccessrights.md)
</dt> </dl>

 

 





