---
title: 'IWMPControls. isAvailable (VB 和 C ) '
description: IsAvailable 屬性 (\_ 在 C \ ) 的 get isAvailable 方法取得值，指出指定的資訊類型是否可用或是否可以執行指定的動作。
ms.assetid: 00812d5c-513e-49d5-93ba-750b81a852dd
keywords:
- IWMPControls. isAvailable (VB 和 C ) Windows Media Player
topic_type:
- apiref
api_name:
- IWMPControls.isAvailable (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0d5d9ffcd6cad6eefb7cdff25fd2cf34b76ccc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998616"
---
# <a name="iwmpcontrolsisavailable-vb-and-c"></a><span data-ttu-id="145fa-104">IWMPControls. isAvailable (VB 和 c # ) </span><span class="sxs-lookup"><span data-stu-id="145fa-104">IWMPControls.isAvailable (VB and C#)</span></span>

<span data-ttu-id="145fa-105">**IsAvailable** 屬性 (c # 中的 **get \_ isAvailable** 方法 ) 取得值，指出指定的資訊類型是否可用或是否可以執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="145fa-105">The **isAvailable** property (the **get\_isAvailable** method in C#) gets a value indicating whether a specified type of information is available or a specified action can be performed.</span></span>


```
[Visual Basic]
ReadOnly Property isAvailable(
  bstrItem As System.String
) As System.Boolean
```




```
[C#]
bool get_isAvailable (
  System.String bstrItem
);
```



## <a name="parameters"></a><span data-ttu-id="145fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="145fa-106">Parameters</span></span>

<span data-ttu-id="145fa-107">*bstrItem*</span><span class="sxs-lookup"><span data-stu-id="145fa-107">*bstrItem*</span></span>

<span data-ttu-id="145fa-108">System.string，這是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="145fa-108">A System.String that is one of the following values.</span></span>



| <span data-ttu-id="145fa-109">值</span><span class="sxs-lookup"><span data-stu-id="145fa-109">Value</span></span>           | <span data-ttu-id="145fa-110">描述</span><span class="sxs-lookup"><span data-stu-id="145fa-110">Description</span></span>                                                                                                                                                       |
|-----------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="145fa-111">currentItem</span><span class="sxs-lookup"><span data-stu-id="145fa-111">currentItem</span></span>     | <span data-ttu-id="145fa-112">探索使用者是否可以設定 **IWMPControls currentItem** 屬性。</span><span class="sxs-lookup"><span data-stu-id="145fa-112">Discovers whether the user can set the **IWMPControls.currentItem** property.</span></span>                                                                                     |
| <span data-ttu-id="145fa-113">currentMarker</span><span class="sxs-lookup"><span data-stu-id="145fa-113">currentMarker</span></span>   | <span data-ttu-id="145fa-114">探索使用者是否可以搜尋特定標記。</span><span class="sxs-lookup"><span data-stu-id="145fa-114">Discovers whether the user can seek to a specific marker.</span></span>                                                                                                         |
| <span data-ttu-id="145fa-115">currentPosition</span><span class="sxs-lookup"><span data-stu-id="145fa-115">currentPosition</span></span> | <span data-ttu-id="145fa-116">探索使用者是否可以搜尋檔案中的特定位置。</span><span class="sxs-lookup"><span data-stu-id="145fa-116">Discovers whether the user can seek to a specific position in the file.</span></span> <span data-ttu-id="145fa-117">有些檔案不支援搜尋。</span><span class="sxs-lookup"><span data-stu-id="145fa-117">Some files do not support seeking.</span></span>                                                        |
| <span data-ttu-id="145fa-118">fastForward</span><span class="sxs-lookup"><span data-stu-id="145fa-118">fastForward</span></span>     | <span data-ttu-id="145fa-119">探索檔案是否支援快速轉送以及是否可叫用該功能。</span><span class="sxs-lookup"><span data-stu-id="145fa-119">Discovers whether the file supports fast forwarding and whether that functionality can be invoked.</span></span> <span data-ttu-id="145fa-120">許多檔案類型 (和即時資料流) 不支援 fastForward。</span><span class="sxs-lookup"><span data-stu-id="145fa-120">Many file types (and live streams) do not support fastForward.</span></span> |
| <span data-ttu-id="145fa-121">fastReverse</span><span class="sxs-lookup"><span data-stu-id="145fa-121">fastReverse</span></span>     | <span data-ttu-id="145fa-122">探索檔案是否支援 fastReverse，以及是否可叫用該功能。</span><span class="sxs-lookup"><span data-stu-id="145fa-122">Discovers whether the file supports fastReverse and whether that functionality can be invoked.</span></span> <span data-ttu-id="145fa-123">許多檔案類型 (和即時資料流) 不支援 fastReverse。</span><span class="sxs-lookup"><span data-stu-id="145fa-123">Many file types (and live streams) do not support fastReverse.</span></span>     |
| <span data-ttu-id="145fa-124">下一步</span><span class="sxs-lookup"><span data-stu-id="145fa-124">next</span></span>            | <span data-ttu-id="145fa-125">探索使用者是否可以搜尋播放清單中的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="145fa-125">Discovers whether the user can seek to the next entry in a playlist.</span></span>                                                                                              |
| <span data-ttu-id="145fa-126">pause</span><span class="sxs-lookup"><span data-stu-id="145fa-126">pause</span></span>           | <span data-ttu-id="145fa-127">探索 **IWMPControls** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="145fa-127">Discovers whether the **IWMPControls.pause** method is available.</span></span>                                                                                                 |
| <span data-ttu-id="145fa-128">玩遊戲</span><span class="sxs-lookup"><span data-stu-id="145fa-128">play</span></span>            | <span data-ttu-id="145fa-129">探索 IWMPControls 的 **播放** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="145fa-129">Discovers whether the **IWMPControls.play** method is available.</span></span>                                                                                                  |
| <span data-ttu-id="145fa-130">previous</span><span class="sxs-lookup"><span data-stu-id="145fa-130">previous</span></span>        | <span data-ttu-id="145fa-131">探索使用者是否可以搜尋播放清單中的上一個專案。</span><span class="sxs-lookup"><span data-stu-id="145fa-131">Discovers whether the user can seek to the previous entry in a playlist.</span></span>                                                                                          |
| <span data-ttu-id="145fa-132">步驟</span><span class="sxs-lookup"><span data-stu-id="145fa-132">step</span></span>            | <span data-ttu-id="145fa-133">探索是否可在播放期間使用 **IWMPControls2** 方法。</span><span class="sxs-lookup"><span data-stu-id="145fa-133">Discovers whether the **IWMPControls2.step** method is available during playback.</span></span>                                                                                 |
| <span data-ttu-id="145fa-134">stop</span><span class="sxs-lookup"><span data-stu-id="145fa-134">stop</span></span>            | <span data-ttu-id="145fa-135">探索 **IWMPControls. stop** 方法是否可用。</span><span class="sxs-lookup"><span data-stu-id="145fa-135">Discovers whether the **IWMPControls.stop** method is available.</span></span>                                                                                                  |



 

## <a name="property-value"></a><span data-ttu-id="145fa-136">屬性值</span><span class="sxs-lookup"><span data-stu-id="145fa-136">Property Value</span></span>

<span data-ttu-id="145fa-137">**System.Boolean**</span><span class="sxs-lookup"><span data-stu-id="145fa-137">**System.Boolean**</span></span>

<span data-ttu-id="145fa-138">**布林值**，指出指定的資訊類型是否可用，或是否可以執行指定的動作。</span><span class="sxs-lookup"><span data-stu-id="145fa-138">A **System.Boolean** that indicates whether a specified type of information is available or a specified action can be performed.</span></span>

## <a name="remarks"></a><span data-ttu-id="145fa-139">備註</span><span class="sxs-lookup"><span data-stu-id="145fa-139">Remarks</span></span>

<span data-ttu-id="145fa-140">**IWMPControls. isAvailable** 是 Visual Basic 中接受參數的屬性。</span><span class="sxs-lookup"><span data-stu-id="145fa-140">**IWMPControls.isAvailable** is a property in Visual Basic that takes a parameter.</span></span> <span data-ttu-id="145fa-141">在 c # 中，它稱為 **IWMPControls. get \_ isAvailable** 方法。</span><span class="sxs-lookup"><span data-stu-id="145fa-141">In C# it is referred to as the **IWMPControls.get\_isAvailable** method.</span></span>

## <a name="examples"></a><span data-ttu-id="145fa-142">範例</span><span class="sxs-lookup"><span data-stu-id="145fa-142">Examples</span></span>

<span data-ttu-id="145fa-143">下列範例會使用 **isAvailable** 屬性 (c # ) 中的 **get \_ isAvailable** 方法，以確認目前的媒體專案支援 **currentPosition** 屬性。</span><span class="sxs-lookup"><span data-stu-id="145fa-143">The following example uses the **isAvailable** property (the **get\_isAvailable** method in C#) to verify that the current media item supports the **currentPosition** property.</span></span> <span data-ttu-id="145fa-144">**AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。</span><span class="sxs-lookup"><span data-stu-id="145fa-144">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
// If the currentPosition property is supported, seek to position 0.
if (player.Ctlcontrols.get_isAvailable("currentPosition"))
{
    player.Ctlcontrols.currentPosition = 0;
}
```


```VB

' If the currentPosition property is supported, seek to position 0.
If (player.Ctlcontrols.isAvailable(&quot;currentPosition&quot;)) Then

    player.Ctlcontrols.currentPosition = 0

End If
```





## <a name="requirements"></a><span data-ttu-id="145fa-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="145fa-145">Requirements</span></span>



| <span data-ttu-id="145fa-146">需求</span><span class="sxs-lookup"><span data-stu-id="145fa-146">Requirement</span></span> | <span data-ttu-id="145fa-147">值</span><span class="sxs-lookup"><span data-stu-id="145fa-147">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="145fa-148">版本</span><span class="sxs-lookup"><span data-stu-id="145fa-148">Version</span></span><br/>   | <span data-ttu-id="145fa-149">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="145fa-149">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="145fa-150">命名空間</span><span class="sxs-lookup"><span data-stu-id="145fa-150">Namespace</span></span><br/> | <span data-ttu-id="145fa-151">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="145fa-151">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="145fa-152">組件</span><span class="sxs-lookup"><span data-stu-id="145fa-152">Assembly</span></span><br/>  | <dl> <span data-ttu-id="145fa-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt></span><span class="sxs-lookup"><span data-stu-id="145fa-153"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="145fa-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="145fa-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="145fa-155">**IWMPControls 介面 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="145fa-155">**IWMPControls Interface (VB and C#)**</span></span>](iwmpcontrols--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="145fa-156">**IWMPControls. currentItem (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="145fa-156">**IWMPControls.currentItem (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-currentitem--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="145fa-157">**IWMPControls： pause (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="145fa-157">**IWMPControls.pause (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-pause--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="145fa-158">**IWMPControls (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="145fa-158">**IWMPControls.play (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-play--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="145fa-159">**IWMPControls。停止 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="145fa-159">**IWMPControls.stop (VB and C#)**</span></span>](wmplibiwmpcontrols-iwmpcontrols-stop--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="145fa-160">**IWMPControls2 (VB 和 c # )**</span><span class="sxs-lookup"><span data-stu-id="145fa-160">**IWMPControls2.step (VB and C#)**</span></span>](wmplibiwmpcontrols2-iwmpcontrols2-step--vb-and-c.md)
</dt> </dl>

 

 





