---
title: 設定。費率
description: '[速率] 屬性會指定或抓取影片媒體的目前播放速率。'
ms.assetid: 0f95f7ac-1bb6-4c80-89eb-eb300a03a0f1
keywords:
- 設定。速率 Windows Media Player
topic_type:
- apiref
api_name:
- Settings.rate
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61287789487fddbe7e77fba5fc033d3103aecb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993316"
---
# <a name="settingsrate"></a><span data-ttu-id="e537c-104">設定。費率</span><span class="sxs-lookup"><span data-stu-id="e537c-104">Settings.rate</span></span>

<span data-ttu-id="e537c-105">[ **速率** ] 屬性會指定或抓取影片媒體的目前播放速率。</span><span class="sxs-lookup"><span data-stu-id="e537c-105">The **rate** property specifies or retrieves the current playback rate of video media.</span></span>

## <a name="syntax"></a><span data-ttu-id="e537c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="e537c-106">Syntax</span></span>

<span data-ttu-id="e537c-107">player. 設定速率</span><span class="sxs-lookup"><span data-stu-id="e537c-107">player.settings.rate</span></span>

## <a name="possible-values"></a><span data-ttu-id="e537c-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="e537c-108">Possible Values</span></span>

<span data-ttu-id="e537c-109">這個屬性是 (**雙精度**) 的讀/寫 **數位**，預設值為1.0。</span><span class="sxs-lookup"><span data-stu-id="e537c-109">This property is a read/write **Number** (**double**) with a default value of 1.0.</span></span>

## <a name="remarks"></a><span data-ttu-id="e537c-110">備註</span><span class="sxs-lookup"><span data-stu-id="e537c-110">Remarks</span></span>

<span data-ttu-id="e537c-111">這個屬性會作為乘數值，讓您以更快或較慢的速率播放剪輯。</span><span class="sxs-lookup"><span data-stu-id="e537c-111">This property acts as a multiplier value that allows you to play a clip at a faster or slower rate.</span></span> <span data-ttu-id="e537c-112">預設值1.0 表示撰寫的速度。</span><span class="sxs-lookup"><span data-stu-id="e537c-112">The default value of 1.0 indicates the authored speed.</span></span> <span data-ttu-id="e537c-113">請注意，在低於0.5 或高於1.5 的速率中，音訊播放軌會變得很難理解。</span><span class="sxs-lookup"><span data-stu-id="e537c-113">Note that an audio track becomes difficult to understand at rates lower than 0.5 or higher than 1.5.</span></span> <span data-ttu-id="e537c-114">播放速率2等於正常播放速度的兩倍。</span><span class="sxs-lookup"><span data-stu-id="e537c-114">A playback rate of 2 equates to twice the normal playback speed.</span></span>

<span data-ttu-id="e537c-115">Windows Media Player 將嘗試使用四種不同播放模式的最有效方式。</span><span class="sxs-lookup"><span data-stu-id="e537c-115">Windows Media Player will attempt to use the most effective of four different playback modes.</span></span> <span data-ttu-id="e537c-116">這些模式是流暢的影片播放，並維持音訊音調、不維護音訊、順暢的影片播放、無音訊的流暢影片播放，以及不含音訊的主要畫面格影片播放。</span><span class="sxs-lookup"><span data-stu-id="e537c-116">These modes are smooth video playback with audio pitch maintained, smooth video playback with audio pitch not maintained, smooth video playback with no audio, and keyframe video playback with no audio.</span></span> <span data-ttu-id="e537c-117">播放程式選擇的模式取決於許多因素，包括檔案類型和位置、作業系統、網路和伺服器。</span><span class="sxs-lookup"><span data-stu-id="e537c-117">The mode chosen by the Player depends on numerous factors including file type and location, operating system, network, and server.</span></span>

<span data-ttu-id="e537c-118">其他考慮也適用于不同的媒體類型：</span><span class="sxs-lookup"><span data-stu-id="e537c-118">Other considerations apply as well, depending on media type:</span></span>

-   <span data-ttu-id="e537c-119">Windows Media Format (WMV) 和 ASF 檔案：此屬性的最佳值為1到10，或從1到10以進行反向播放。</span><span class="sxs-lookup"><span data-stu-id="e537c-119">Windows Media Format (WMV) and ASF files: Optimal values for this property are from 1 to 10, or from  1 to  10 for reverse play.</span></span> <span data-ttu-id="e537c-120">從0.5 到1.0 或從-0.5 到-1.0 的值可能也適用于可以維持音訊音調的情況，例如，播放位於本機電腦上的檔案時。</span><span class="sxs-lookup"><span data-stu-id="e537c-120">Values from 0.5 to 1.0 or from -0.5 to -1.0 may also work well in cases where audio pitch can be maintained, for example, when playing files located on the local computer.</span></span> <span data-ttu-id="e537c-121">允許絕對值大於10的值，但沒有什麼意義。</span><span class="sxs-lookup"><span data-stu-id="e537c-121">Values with an absolute magnitude greater than 10 are allowed, but are not very meaningful.</span></span>
-   <span data-ttu-id="e537c-122">其他影片媒體類型：這個屬性的範圍可以從0到9。</span><span class="sxs-lookup"><span data-stu-id="e537c-122">Other Video Media Types: This property can range from 0 to 9.</span></span> <span data-ttu-id="e537c-123">不允許負數值。</span><span class="sxs-lookup"><span data-stu-id="e537c-123">Negative values are not allowed.</span></span> <span data-ttu-id="e537c-124">小於1的值表示緩慢的移動。</span><span class="sxs-lookup"><span data-stu-id="e537c-124">Values less than 1 represent slow motion.</span></span> <span data-ttu-id="e537c-125">允許超過9個值，但沒有什麼意義。</span><span class="sxs-lookup"><span data-stu-id="e537c-125">Values above 9 are allowed, but are not very meaningful.</span></span>

<span data-ttu-id="e537c-126">*控制項*。**fastForward** 方法會將 **速率** 的值變更為5.0，而 *控制項* 則變更。**fastReverse** 方法會將 **速率** 變更為5.0。</span><span class="sxs-lookup"><span data-stu-id="e537c-126">The *Controls*.**fastForward** method changes the value of **rate** to 5.0, while the *Controls*.**fastReverse** method changes **rate** to  5.0.</span></span>

<span data-ttu-id="e537c-127">某些媒體類型的播放率無法改變。</span><span class="sxs-lookup"><span data-stu-id="e537c-127">The playback rate of some media types cannot be altered.</span></span> <span data-ttu-id="e537c-128">使用這些 *設定*。**isAvailable** 方法，以判斷是否可以針對特定媒體專案指定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e537c-128">Use the *Settings*.**isAvailable** method to determine whether this property can be specified for a particular media item.</span></span>

<span data-ttu-id="e537c-129">**Windows Media Player 10** 行動裝置版：此屬性只接受或傳回值-5.0、1.0 或5.0。</span><span class="sxs-lookup"><span data-stu-id="e537c-129">**Windows Media Player 10 Mobile**: This property only accepts or returns values of -5.0, 1.0, or 5.0.</span></span>

## <a name="examples"></a><span data-ttu-id="e537c-130">範例</span><span class="sxs-lookup"><span data-stu-id="e537c-130">Examples</span></span>

<span data-ttu-id="e537c-131">下列範例會建立 HTML SELECT 元素，讓使用者可以變更目前媒體的播放速度。</span><span class="sxs-lookup"><span data-stu-id="e537c-131">The following example creates an HTML SELECT element that allows the user to change the playback speed of the current media.</span></span> <span data-ttu-id="e537c-132">選取選項提供一般速度、半速度和雙速度的播放速率。</span><span class="sxs-lookup"><span data-stu-id="e537c-132">The SELECT options offer normal speed, half -speed and double-speed playback rates.</span></span> <span data-ttu-id="e537c-133">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="e537c-133">The **Player** object was created with ID = "Player".</span></span>


```
<!-- Create the HTML SELECT element. -->
<SELECT  ID = pbRATE  NAME = "pbRATE"  LANGUAGE="JScript"
         onChange="
                   /* Test whether playback rate can be set. */
                   if(Player.settings.IsAvailable('Rate'))

                   /* Set the playback rate based on the current
                      value of the SELECT element. */
                   Player.settings.rate = this.value
">

/* Create the OPTION list. */
<OPTION VALUE = 1>NORMAL</OPTION>
<OPTION VALUE = .5>half speed</OPTION>
<OPTION VALUE = 2>2 speed</OPTION>
</SELECT>

```



## <a name="requirements"></a><span data-ttu-id="e537c-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="e537c-134">Requirements</span></span>



| <span data-ttu-id="e537c-135">需求</span><span class="sxs-lookup"><span data-stu-id="e537c-135">Requirement</span></span> | <span data-ttu-id="e537c-136">值</span><span class="sxs-lookup"><span data-stu-id="e537c-136">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e537c-137">版本</span><span class="sxs-lookup"><span data-stu-id="e537c-137">Version</span></span><br/> | <span data-ttu-id="e537c-138">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e537c-138">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="e537c-139">DLL</span><span class="sxs-lookup"><span data-stu-id="e537c-139">DLL</span></span><br/>     | <dl> <span data-ttu-id="e537c-140"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e537c-140"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e537c-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e537c-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e537c-142">**FastForward**</span><span class="sxs-lookup"><span data-stu-id="e537c-142">**Controls.fastForward**</span></span>](controls-fastforward.md)
</dt> <dt>

[<span data-ttu-id="e537c-143">**FastReverse**</span><span class="sxs-lookup"><span data-stu-id="e537c-143">**Controls.fastReverse**</span></span>](controls-fastreverse.md)
</dt> <dt>

[<span data-ttu-id="e537c-144">**Settings 物件**</span><span class="sxs-lookup"><span data-stu-id="e537c-144">**Settings Object**</span></span>](settings-object.md)
</dt> <dt>

[<span data-ttu-id="e537c-145">**設定. isAvailable**</span><span class="sxs-lookup"><span data-stu-id="e537c-145">**Settings.isAvailable**</span></span>](settings-isavailable.md)
</dt> </dl>

 

 





