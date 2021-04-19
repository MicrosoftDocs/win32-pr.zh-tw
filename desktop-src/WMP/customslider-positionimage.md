---
title: CUSTOMSLIDER.positionImage
description: PositionImage 屬性會指定或抓取用來判斷影像檔案中所要顯示之位置影像的影像地圖。
ms.assetid: 7e99dc21-ebba-438a-a983-190dbe429578
keywords:
- CUSTOMSLIDER. positionImage Windows Media Player
topic_type:
- apiref
api_name:
- CUSTOMSLIDER.positionImage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: dc92a9c263e2b450e64d526ccfc7976fdd6227a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106986150"
---
# <a name="customsliderpositionimage"></a><span data-ttu-id="0d1fc-104">CUSTOMSLIDER.positionImage</span><span class="sxs-lookup"><span data-stu-id="0d1fc-104">CUSTOMSLIDER.positionImage</span></span>

<span data-ttu-id="0d1fc-105">**PositionImage** 屬性會指定或抓取用來判斷影像檔案中所要顯示之位置影像的影像地圖。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-105">The **positionImage** attribute specifies or retrieves the image map used to determine which position image from the image file to display.</span></span>

``` syntax
        elementID.positionImage
```

## <a name="possible-values"></a><span data-ttu-id="0d1fc-106">可能的值</span><span class="sxs-lookup"><span data-stu-id="0d1fc-106">Possible Values</span></span>

<span data-ttu-id="0d1fc-107">這個屬性是包含影像檔案名稱的讀取/寫入 **字串** 。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-107">This attribute is a read/write **String** containing the name of an image file.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d1fc-108">備註</span><span class="sxs-lookup"><span data-stu-id="0d1fc-108">Remarks</span></span>

<span data-ttu-id="0d1fc-109">這個屬性是必要的，而且必須指定。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-109">This attribute is required and must be specified.</span></span>

<span data-ttu-id="0d1fc-110">不會顯示 **positionImage** 。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-110">The **positionImage** is not displayed.</span></span> <span data-ttu-id="0d1fc-111">相反地，它會作為對應，以定義所顯示影像的可按區域。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-111">Instead, it serves as a map defining the clickable regions of the displayed image.</span></span> <span data-ttu-id="0d1fc-112">顯示的影像是影像檔案的其中一個子影像，代表滑杆的實際狀態。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-112">The displayed image is one of the sub-images of the image file and represents the actual state of the slider.</span></span> <span data-ttu-id="0d1fc-113">**PositionImage** 包含一些相當於這些子影像數目的灰色比例區域。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-113">The **positionImage** includes a number of gray scale regions equal to the number of these sub-images.</span></span> <span data-ttu-id="0d1fc-114">子映射必須與 **positionImage** 具有相同的維度，否則自訂滑杆將無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-114">The sub-images must have the same dimensions as the **positionImage** or the custom slider will not work correctly.</span></span>

<span data-ttu-id="0d1fc-115">任何不是灰色縮放的區域都將無法按。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-115">Any region that is not in gray scale will not be clickable.</span></span> <span data-ttu-id="0d1fc-116">可點按的區域應設定為色彩值，這些值會從黑色到白色的灰色尺規範圍平均，而且第一個區域是純黑色，而最後一個區域是純白色。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-116">The clickable regions should be set to color values that range evenly across the gray scale spectrum from black to white, with the first region being pure black and the last region being pure white.</span></span> <span data-ttu-id="0d1fc-117">每個後續區域的色彩值，應以等於255除以區域總數減一的值遞增，四捨五入為最接近的整數。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-117">The color values of each successive region should be incremented by a value equal to 255 divided by the total number of regions minus one, rounding to the nearest whole number.</span></span>

<span data-ttu-id="0d1fc-118">例如，如果有六個區域，則遞增量會是 51 (255 除以 5) ，而六個灰色小數位數值為0、51、102、153、204和255。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-118">For example, if there are six regions, the increment would be 51 (255 divided by 5), and the six gray scale values would be 0, 51, 102, 153, 204, and 255.</span></span> <span data-ttu-id="0d1fc-119">六個區域的十六進位色彩值接著會是 \# 000000、 \# 333333、 \# 666666、 \# 999999、 \# CCCCCC 和 \# FFFFFF。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-119">The hexadecimal color values for the six regions would then be \#000000, \#333333, \#666666, \#999999, \#CCCCCC, and \#FFFFFF.</span></span>

<span data-ttu-id="0d1fc-120">如此一來，區域會有以灰色縮放色彩值為依據的序列，而此順序會對應至影像檔案中的子影像順序。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-120">In this way, the regions will have a sequence dictated by their gray scale color values, and this sequence will correspond to the sequence of sub-images in the image file.</span></span> <span data-ttu-id="0d1fc-121">按一下其中一個區域時，會顯示對應的子影像，並據此更新自訂滑杆的 **值** 。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-121">When one of the regions is clicked, the corresponding sub-image is shown and the **value** of the custom slider is updated accordingly.</span></span>

<span data-ttu-id="0d1fc-122">支援的影像檔案類型為 BMP、JPG、PNG 和 GIF (不包括動畫 Gif) 。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-122">The supported image file types are BMP, JPG, PNG, and GIF (not including animated GIFs).</span></span>

## <a name="examples"></a><span data-ttu-id="0d1fc-123">範例</span><span class="sxs-lookup"><span data-stu-id="0d1fc-123">Examples</span></span>

<span data-ttu-id="0d1fc-124">以下是自訂滑杆 **positionImage** 的範例。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-124">The following is an example of a custom slider **positionImage**.</span></span> <span data-ttu-id="0d1fc-125">對應的影像會顯示在 [ **影像** ] 屬性的 [範例] 區段中。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-125">The corresponding image is shown in the example section of the **image** property.</span></span>

![範例 positionimage 圖形](images/dialmap.png)

<span data-ttu-id="0d1fc-127">下列程式碼說明如何使用 **CUSTOMSLIDER** 屬性。</span><span class="sxs-lookup"><span data-stu-id="0d1fc-127">The following code illustrates the use of **CUSTOMSLIDER** attributes.</span></span>


```XML
<THEME>
  <VIEW
    backgroundImage = "background.bmp"
    titleBar = "False"
  >

    <PLAYER
      URL = "https://proseware.com/mellow.wma"
    >
      <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition;"
      />
    </PLAYER>

    <SLIDER
      id = "myslider"
      min = "0"
      max = "wmpprop:player.currentMedia.duration"
      onmouseup = "player.controls.currentPosition = myslider.value; "
      tooltip = "current position"
      height = "10"
      width = "180"
      top = "150"
      left = "88"
      backgroundColor = "red"
      foregroundColor = "blue"
      thumbImage = "thumb.bmp"
    />

    <CUSTOMSLIDER
      top = "120"
      left = "23"
      min = "0"
      max = "100"
      borderSize = "10"
      toolTip = "volume control"
      image = "dial.bmp"
      transparencyColor = "#00FFFF"
      positionImage = "dialmap.bmp"
      enabled = "true"
      value = "wmpprop:player.settings.volume"
      value_onchange = "player.settings.volume = value"
    />

    <EFFECTS
      id = "myeffects"
      top = "25"
      left = "88"
      width = "180"
      height = "100"
    />

    <BUTTONGROUP
      mappingImage = "map.bmp"
      hoverImage = "hover.bmp"
    > 

      <BUTTONELEMENT
        mappingColor = "#00FF00"
        upToolTip = "Next"
        onClick = "JScript:myeffects.next();"
      />

      <BUTTONELEMENT
        mappingColor = "#FF0000"
        upToolTip = "Previous"
        onClick = "JScript:myeffects.previous();"
      />

    </BUTTONGROUP>

  </VIEW>
</THEME>

```



## <a name="requirements"></a><span data-ttu-id="0d1fc-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d1fc-128">Requirements</span></span>



| <span data-ttu-id="0d1fc-129">需求</span><span class="sxs-lookup"><span data-stu-id="0d1fc-129">Requirement</span></span> | <span data-ttu-id="0d1fc-130">值</span><span class="sxs-lookup"><span data-stu-id="0d1fc-130">Value</span></span> |
|--------------------|------------------------------------------------------|
| <span data-ttu-id="0d1fc-131">版本</span><span class="sxs-lookup"><span data-stu-id="0d1fc-131">Version</span></span><br/> | <span data-ttu-id="0d1fc-132">Windows Media Player 7.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="0d1fc-132">Windows Media Player version 7.0 or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0d1fc-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d1fc-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d1fc-134">**CUSTOMSLIDER 元素**</span><span class="sxs-lookup"><span data-stu-id="0d1fc-134">**CUSTOMSLIDER Element**</span></span>](customslider-element.md)
</dt> <dt>

[<span data-ttu-id="0d1fc-135">**CUSTOMSLIDER 影像**</span><span class="sxs-lookup"><span data-stu-id="0d1fc-135">**CUSTOMSLIDER.image**</span></span>](customslider-image.md)
</dt> </dl>

 

 





