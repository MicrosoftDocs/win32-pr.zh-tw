---
title: 滑杆. foregroundProgress
description: ForegroundProgress 屬性會指定或抓取前景進度列的目前位置（以滑杆區域的百分比表示）。
ms.assetid: 1218ca5a-445c-441b-aa62-74a184a25c2d
keywords:
- ForegroundProgress Windows Media Player
topic_type:
- apiref
api_name:
- SLIDER.foregroundProgress
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a4597630453444564411d0bcfad8dc6b39914d13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106979493"
---
# <a name="sliderforegroundprogress"></a><span data-ttu-id="39fa4-104">滑杆. foregroundProgress</span><span class="sxs-lookup"><span data-stu-id="39fa4-104">SLIDER.foregroundProgress</span></span>

<span data-ttu-id="39fa4-105">**ForegroundProgress** 屬性會指定或抓取前景進度列的目前位置（以滑杆區域的百分比表示）。</span><span class="sxs-lookup"><span data-stu-id="39fa4-105">The **foregroundProgress** attribute specifies or retrieves the current position of the foreground progress bar as a percentage of the slider area.</span></span>

``` syntax
        elementID.foregroundProgress
```

## <a name="possible-values"></a><span data-ttu-id="39fa4-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="39fa4-106">Possible Values</span></span>

<span data-ttu-id="39fa4-107">這個屬性是 (**浮點數**) 範圍從0到100的讀取/寫入 **號碼**。</span><span class="sxs-lookup"><span data-stu-id="39fa4-107">This attribute is a read/write **Number** (**float**) ranging from 0 to 100.</span></span>

## <a name="remarks"></a><span data-ttu-id="39fa4-108">備註</span><span class="sxs-lookup"><span data-stu-id="39fa4-108">Remarks</span></span>

<span data-ttu-id="39fa4-109">這個屬性主要是用來追蹤媒體檔案的下載進度，同時使用 **value** 屬性來追蹤檔案目前的播放位置。</span><span class="sxs-lookup"><span data-stu-id="39fa4-109">This attribute is used primarily to track the download progress of a media file while simultaneously tracking the current play position of the file using the **value** attribute.</span></span> <span data-ttu-id="39fa4-110">滑杆捲動方塊的位置會限制為前景進度的區域。</span><span class="sxs-lookup"><span data-stu-id="39fa4-110">The position of the slider thumb is constrained to the area of the foreground progress.</span></span> <span data-ttu-id="39fa4-111">這可讓您只在下載檔案的可用部分內進行互動式搜尋。</span><span class="sxs-lookup"><span data-stu-id="39fa4-111">This allows interactive seeking to take place only within the available portion of a downloading file.</span></span>

<span data-ttu-id="39fa4-112">若要使用此功能， **useForegroundProgress** 屬性必須設定為 true。</span><span class="sxs-lookup"><span data-stu-id="39fa4-112">To use this functionality, the **useForegroundProgress** attribute must be set to true.</span></span>

## <a name="examples"></a><span data-ttu-id="39fa4-113">範例</span><span class="sxs-lookup"><span data-stu-id="39fa4-113">Examples</span></span>


```C++
<SLIDER
  id="seek"
  backgroundColor="blue"
  foregroundColor="red"
  thumbImage="seekthumb.bmp"
  min="0"
  max="wmpprop:player.currentMedia.duration"
  value="wmpprop:player.controls.currentPosition"
  useForegroundProgress="true"
  foregroundProgress="wmpprop:player.network.downloadProgress"
  ondragend="player.controls.currentposition=value"
/>

```



## <a name="requirements"></a><span data-ttu-id="39fa4-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="39fa4-114">Requirements</span></span>



| <span data-ttu-id="39fa4-115">需求</span><span class="sxs-lookup"><span data-stu-id="39fa4-115">Requirement</span></span> | <span data-ttu-id="39fa4-116">值</span><span class="sxs-lookup"><span data-stu-id="39fa4-116">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="39fa4-117">版本</span><span class="sxs-lookup"><span data-stu-id="39fa4-117">Version</span></span><br/> | <span data-ttu-id="39fa4-118">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="39fa4-118">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="39fa4-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39fa4-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39fa4-120">**滑杆元素**</span><span class="sxs-lookup"><span data-stu-id="39fa4-120">**SLIDER Element**</span></span>](slider-element.md)
</dt> <dt>

[<span data-ttu-id="39fa4-121">**滑杆。最小值**</span><span class="sxs-lookup"><span data-stu-id="39fa4-121">**SLIDER.min**</span></span>](slider-min.md)
</dt> <dt>

[<span data-ttu-id="39fa4-122">**滑杆。最大值**</span><span class="sxs-lookup"><span data-stu-id="39fa4-122">**SLIDER.max**</span></span>](slider-max.md)
</dt> <dt>

[<span data-ttu-id="39fa4-123">**滑杆. useForegroundProgress**</span><span class="sxs-lookup"><span data-stu-id="39fa4-123">**SLIDER.useForegroundProgress**</span></span>](slider-useforegroundprogress.md)
</dt> <dt>

[<span data-ttu-id="39fa4-124">**滑杆。值**</span><span class="sxs-lookup"><span data-stu-id="39fa4-124">**SLIDER.value**</span></span>](slider-value.md)
</dt> </dl>

 

 





