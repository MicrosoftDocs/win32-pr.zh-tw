---
title: WM/MediaClassSecondaryID 屬性
description: WM/MediaClassSecondaryID 屬性是指定次要媒體類別的 GUID，這是主要媒體類別的子類別。
ms.assetid: 8112513a-b73a-497a-9c24-24ccef31cffc
keywords:
- WM/MediaClassSecondaryID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassSecondaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fb88ea03e565df649088366e13b20332256b374d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977674"
---
# <a name="wmmediaclasssecondaryid-attribute"></a><span data-ttu-id="6c9e8-104">WM/MediaClassSecondaryID 屬性</span><span class="sxs-lookup"><span data-stu-id="6c9e8-104">WM/MediaClassSecondaryID Attribute</span></span>

<span data-ttu-id="6c9e8-105">**WM/MediaClassSecondaryID** 屬性是指定次要媒體類別的 GUID，這是主要媒體類別的子類別。</span><span class="sxs-lookup"><span data-stu-id="6c9e8-105">The **WM/MediaClassSecondaryID** attribute is a GUID specifying the secondary media class, which is a subclass of the primary media class.</span></span>

## <a name="applies-to"></a><span data-ttu-id="6c9e8-106">套用至</span><span class="sxs-lookup"><span data-stu-id="6c9e8-106">Applies To</span></span>

-   [<span data-ttu-id="6c9e8-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="6c9e8-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="6c9e8-108">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="6c9e8-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="6c9e8-109">其他專案</span><span class="sxs-lookup"><span data-stu-id="6c9e8-109">Other Items</span></span>](other-item-attributes.md)
-   [<span data-ttu-id="6c9e8-110">相片專案</span><span class="sxs-lookup"><span data-stu-id="6c9e8-110">Photo Items</span></span>](photo-item-attributes.md)
-   [<span data-ttu-id="6c9e8-111">播放清單</span><span class="sxs-lookup"><span data-stu-id="6c9e8-111">Playlists</span></span>](playlist-attributes-ref.md)
-   [<span data-ttu-id="6c9e8-112">單選項目</span><span class="sxs-lookup"><span data-stu-id="6c9e8-112">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="6c9e8-113">影片專案</span><span class="sxs-lookup"><span data-stu-id="6c9e8-113">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="6c9e8-114">備註</span><span class="sxs-lookup"><span data-stu-id="6c9e8-114">Remarks</span></span>

<span data-ttu-id="6c9e8-115">這個屬性會儲存在文件庫和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="6c9e8-115">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="6c9e8-116">下表列出支援的 Guid 及其描述。</span><span class="sxs-lookup"><span data-stu-id="6c9e8-116">The following table lists the supported GUIDs and their descriptions.</span></span>



| <span data-ttu-id="6c9e8-117">GUID</span><span class="sxs-lookup"><span data-stu-id="6c9e8-117">GUID</span></span>                                 | <span data-ttu-id="6c9e8-118">Description</span><span class="sxs-lookup"><span data-stu-id="6c9e8-118">Description</span></span>                                    |
|--------------------------------------|------------------------------------------------|
| <span data-ttu-id="6c9e8-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span><span class="sxs-lookup"><span data-stu-id="6c9e8-119">D0E20D5C-CAD6-4F66-9FA1-6018830F1DCC</span></span> | <span data-ttu-id="6c9e8-120">媒體物件代表靜態播放清單。</span><span class="sxs-lookup"><span data-stu-id="6c9e8-120">The media object represents a static playlist.</span></span> |
| <span data-ttu-id="6c9e8-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span><span class="sxs-lookup"><span data-stu-id="6c9e8-121">EB0BAFB6-3C4F-4C31-AA39-95C7B8D7831D</span></span> | <span data-ttu-id="6c9e8-122">媒體物件代表自動播放清單。</span><span class="sxs-lookup"><span data-stu-id="6c9e8-122">The media object represents an auto playlist.</span></span>  |



 

<span data-ttu-id="6c9e8-123">**MediaClassSecondaryID** 是此屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="6c9e8-123">**MediaClassSecondaryID** is an alias for this attribute.</span></span>

<span data-ttu-id="6c9e8-124">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMMediaClassSecondaryID。</span><span class="sxs-lookup"><span data-stu-id="6c9e8-124">The Windows Media Format SDK constant for this attribute is g\_wszWMMediaClassSecondaryID.</span></span>

<span data-ttu-id="6c9e8-125">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="6c9e8-125">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c9e8-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c9e8-126">Requirements</span></span>



| <span data-ttu-id="6c9e8-127">需求</span><span class="sxs-lookup"><span data-stu-id="6c9e8-127">Requirement</span></span> | <span data-ttu-id="6c9e8-128">值</span><span class="sxs-lookup"><span data-stu-id="6c9e8-128">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9e8-129">版本</span><span class="sxs-lookup"><span data-stu-id="6c9e8-129">Version</span></span><br/> | <span data-ttu-id="6c9e8-130">只有 Windows Media Player 10 或更新版本才支援相片專案。只有 Windows Media Player 9 系列支援 Windows Media Player 9 系列和更新版本中的所有其他專案</span><span class="sxs-lookup"><span data-stu-id="6c9e8-130">The photo item is supported only in Windows Media Player 10 or later The radio item is supported only in Windows Media Player 9 Series All other items are supported in Windows Media Player 9 Series and later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="6c9e8-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c9e8-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c9e8-132">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="6c9e8-132">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





