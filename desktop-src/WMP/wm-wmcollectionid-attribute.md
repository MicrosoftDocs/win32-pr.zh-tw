---
title: WM/WMCollectionID 屬性
description: WM/WMCollectionID 屬性是識別專案所屬集合的 GUID。
ms.assetid: 21fc0a62-d374-4ca3-bbb8-278e0d2497ce
keywords:
- WM/WMCollectionID 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/WMCollectionID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bce21196e1da9583db293dab004812265c85308
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978771"
---
# <a name="wmwmcollectionid-attribute"></a><span data-ttu-id="11108-104">WM/WMCollectionID 屬性</span><span class="sxs-lookup"><span data-stu-id="11108-104">WM/WMCollectionID Attribute</span></span>

<span data-ttu-id="11108-105">**WM/WMCollectionID** 屬性是識別專案所屬集合的 GUID。</span><span class="sxs-lookup"><span data-stu-id="11108-105">The **WM/WMCollectionID** attribute is a GUID identifying the collection to which the item belongs.</span></span>

## <a name="applies-to"></a><span data-ttu-id="11108-106">套用至</span><span class="sxs-lookup"><span data-stu-id="11108-106">Applies To</span></span>

-   [<span data-ttu-id="11108-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="11108-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="11108-108">CD 播放清單</span><span class="sxs-lookup"><span data-stu-id="11108-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="11108-109">CD 曲目</span><span class="sxs-lookup"><span data-stu-id="11108-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="11108-110">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="11108-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="11108-111">備註</span><span class="sxs-lookup"><span data-stu-id="11108-111">Remarks</span></span>

<span data-ttu-id="11108-112">這個屬性會儲存在程式庫 (或快取) 和媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="11108-112">This attribute is stored in both the library (or cache) and the media file.</span></span>

<span data-ttu-id="11108-113">**WMCollectionID** 是此屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="11108-113">**WMCollectionID** is an alias for this attribute.</span></span>

<span data-ttu-id="11108-114">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMCollectionID。</span><span class="sxs-lookup"><span data-stu-id="11108-114">The Windows Media Format SDK constant for this attribute is g\_wszWMCollectionID.</span></span>

<span data-ttu-id="11108-115">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="11108-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="11108-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="11108-116">Requirements</span></span>



| <span data-ttu-id="11108-117">需求</span><span class="sxs-lookup"><span data-stu-id="11108-117">Requirement</span></span> | <span data-ttu-id="11108-118">值</span><span class="sxs-lookup"><span data-stu-id="11108-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="11108-119">版本</span><span class="sxs-lookup"><span data-stu-id="11108-119">Version</span></span><br/> | <span data-ttu-id="11108-120">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="11108-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="11108-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="11108-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11108-122">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="11108-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





