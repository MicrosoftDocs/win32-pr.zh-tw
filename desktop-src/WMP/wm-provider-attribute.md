---
title: WM/提供者屬性
description: WM/提供者屬性是屬性值提供者的名稱。
ms.assetid: 358651d3-5bcd-4a03-a9aa-a33745d0323a
keywords:
- WM/提供者屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/Provider
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d7c2c1c796edf28a567f72708c60c7976f718bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977484"
---
# <a name="wmprovider-attribute"></a><span data-ttu-id="7563f-104">WM/提供者屬性</span><span class="sxs-lookup"><span data-stu-id="7563f-104">WM/Provider Attribute</span></span>

<span data-ttu-id="7563f-105">**WM/提供者** 屬性是屬性值提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="7563f-105">The **WM/Provider** attribute is the name of the provider of the attribute values.</span></span>

## <a name="applies-to"></a><span data-ttu-id="7563f-106">套用至</span><span class="sxs-lookup"><span data-stu-id="7563f-106">Applies To</span></span>

-   [<span data-ttu-id="7563f-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="7563f-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="7563f-108">CD 播放清單</span><span class="sxs-lookup"><span data-stu-id="7563f-108">CD Playlists</span></span>](cd-playlist-attributes.md)
-   [<span data-ttu-id="7563f-109">CD 曲目</span><span class="sxs-lookup"><span data-stu-id="7563f-109">CD Tracks</span></span>](cd-track-attributes.md)
-   [<span data-ttu-id="7563f-110">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="7563f-110">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)
-   [<span data-ttu-id="7563f-111">單選項目</span><span class="sxs-lookup"><span data-stu-id="7563f-111">Radio Items</span></span>](radio-item-attributes.md)
-   [<span data-ttu-id="7563f-112">影片專案</span><span class="sxs-lookup"><span data-stu-id="7563f-112">Video Items</span></span>](video-item-attributes.md)

## <a name="remarks"></a><span data-ttu-id="7563f-113">備註</span><span class="sxs-lookup"><span data-stu-id="7563f-113">Remarks</span></span>

<span data-ttu-id="7563f-114">這個屬性會儲存在程式庫 (或快取) 和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="7563f-114">This attribute is stored in both the library (or cache) and the digital media file.</span></span>

<span data-ttu-id="7563f-115">**MetadataSource** 是此屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="7563f-115">**MetadataSource** is an alias for this attribute.</span></span>

<span data-ttu-id="7563f-116">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMProvider。</span><span class="sxs-lookup"><span data-stu-id="7563f-116">The Windows Media Format SDK constant for this attribute is g\_wszWMProvider.</span></span>

<span data-ttu-id="7563f-117">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="7563f-117">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="7563f-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="7563f-118">Requirements</span></span>



| <span data-ttu-id="7563f-119">需求</span><span class="sxs-lookup"><span data-stu-id="7563f-119">Requirement</span></span> | <span data-ttu-id="7563f-120">值</span><span class="sxs-lookup"><span data-stu-id="7563f-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7563f-121">版本</span><span class="sxs-lookup"><span data-stu-id="7563f-121">Version</span></span><br/> | <span data-ttu-id="7563f-122">Windows Media Player 9 系列或更新版本 (只有 Windows Media Player 10 或更新版本才支援相片專案) </span><span class="sxs-lookup"><span data-stu-id="7563f-122">Windows Media Player 9 Series or later (The photo item is supported only in Windows Media Player 10 or later)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7563f-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7563f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7563f-124">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="7563f-124">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





