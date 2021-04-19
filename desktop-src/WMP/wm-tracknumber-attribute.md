---
title: WM/TrackNumber 屬性
description: WM/TrackNumber 屬性是原始發行的專輯上專案的曲目編號。
ms.assetid: d1fc5bac-c440-470f-be5c-5aca74aee99e
keywords:
- WM/TrackNumber 屬性 Windows Media Player
topic_type:
- apiref
api_name:
- WM/TrackNumber
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecd9adf3a939a5087ee270e8bef4d4d510b678ea
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993518"
---
# <a name="wmtracknumber-attribute"></a><span data-ttu-id="f8a9d-104">WM/TrackNumber 屬性</span><span class="sxs-lookup"><span data-stu-id="f8a9d-104">WM/TrackNumber Attribute</span></span>

<span data-ttu-id="f8a9d-105">**WM/TrackNumber** 屬性是原始發行的專輯上專案的曲目編號。</span><span class="sxs-lookup"><span data-stu-id="f8a9d-105">The **WM/TrackNumber** attribute is the track number of the item on the album on which it was originally released.</span></span>

## <a name="applies-to"></a><span data-ttu-id="f8a9d-106">套用至</span><span class="sxs-lookup"><span data-stu-id="f8a9d-106">Applies To</span></span>

-   [<span data-ttu-id="f8a9d-107">音訊專案</span><span class="sxs-lookup"><span data-stu-id="f8a9d-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="f8a9d-108">常用的 Windows Media 檔案屬性</span><span class="sxs-lookup"><span data-stu-id="f8a9d-108">Commonly Used Windows Media File Attributes</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="f8a9d-109">備註</span><span class="sxs-lookup"><span data-stu-id="f8a9d-109">Remarks</span></span>

<span data-ttu-id="f8a9d-110">這個屬性會儲存在文件庫和數位媒體檔案中。</span><span class="sxs-lookup"><span data-stu-id="f8a9d-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="f8a9d-111">專輯的曲目編號從1開始。</span><span class="sxs-lookup"><span data-stu-id="f8a9d-111">Track numbers for an album start at 1.</span></span>

<span data-ttu-id="f8a9d-112">**OriginalIndex** 和 **OriginalIndexLeft** 是這個屬性的別名。</span><span class="sxs-lookup"><span data-stu-id="f8a9d-112">**OriginalIndex** and **OriginalIndexLeft** are aliases for this attribute.</span></span>

<span data-ttu-id="f8a9d-113">這個屬性的 Windows Media Format SDK 常數是 g \_ wszWMTrackNumber。</span><span class="sxs-lookup"><span data-stu-id="f8a9d-113">The Windows Media Format SDK constant for this attribute is g\_wszWMTrackNumber.</span></span>

<span data-ttu-id="f8a9d-114">若要判斷是否可以變更這個屬性的值，請使用 [isReadOnlyItem](media-isreadonlyitem.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="f8a9d-114">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a9d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8a9d-115">Requirements</span></span>



| <span data-ttu-id="f8a9d-116">需求</span><span class="sxs-lookup"><span data-stu-id="f8a9d-116">Requirement</span></span> | <span data-ttu-id="f8a9d-117">值</span><span class="sxs-lookup"><span data-stu-id="f8a9d-117">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="f8a9d-118">版本</span><span class="sxs-lookup"><span data-stu-id="f8a9d-118">Version</span></span><br/> | <span data-ttu-id="f8a9d-119">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="f8a9d-119">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f8a9d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8a9d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a9d-121">**屬性參考**</span><span class="sxs-lookup"><span data-stu-id="f8a9d-121">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





