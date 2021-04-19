---
title: PlayState
description: PlayState 屬性會抓取值，指出 Windows Media Player 作業的狀態。
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- PlayState Windows Media Player
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984053"
---
# <a name="playerplaystate"></a><span data-ttu-id="f0ecc-104">PlayState</span><span class="sxs-lookup"><span data-stu-id="f0ecc-104">Player.playState</span></span>

<span data-ttu-id="f0ecc-105">**PlayState** 屬性會抓取值，指出 Windows Media Player 作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-105">The **playState** property retrieves a value indicating the state of the Windows Media Player operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="f0ecc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="f0ecc-106">Syntax</span></span>

<span data-ttu-id="f0ecc-107">*玩家* 。**playState**</span><span class="sxs-lookup"><span data-stu-id="f0ecc-107">*player* .**playState**</span></span>

## <a name="possible-values"></a><span data-ttu-id="f0ecc-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="f0ecc-108">Possible Values</span></span>

<span data-ttu-id="f0ecc-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-109">This property is a read-only **Number** (**long**).</span></span> <span data-ttu-id="f0ecc-110">C 樣式的列舉常數可以藉由在 state 值前面加上 "wmpps" 來衍生。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-110">The C-style enumeration constant can be derived by prefixing the state value with "wmpps".</span></span> <span data-ttu-id="f0ecc-111">例如，播放狀態的常數是 **wmppsPlaying**。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-111">For example, the constant for the Playing state is **wmppsPlaying**.</span></span>



| <span data-ttu-id="f0ecc-112">值</span><span class="sxs-lookup"><span data-stu-id="f0ecc-112">Value</span></span> | <span data-ttu-id="f0ecc-113">州</span><span class="sxs-lookup"><span data-stu-id="f0ecc-113">State</span></span>         | <span data-ttu-id="f0ecc-114">描述</span><span class="sxs-lookup"><span data-stu-id="f0ecc-114">Description</span></span>                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ecc-115">0</span><span class="sxs-lookup"><span data-stu-id="f0ecc-115">0</span></span>     | <span data-ttu-id="f0ecc-116">未定義</span><span class="sxs-lookup"><span data-stu-id="f0ecc-116">Undefined</span></span>     | <span data-ttu-id="f0ecc-117">Windows Media Player 處於未定義狀態。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-117">Windows Media Player is in an undefined state.</span></span>                                                                              |
| <span data-ttu-id="f0ecc-118">1</span><span class="sxs-lookup"><span data-stu-id="f0ecc-118">1</span></span>     | <span data-ttu-id="f0ecc-119">已停止</span><span class="sxs-lookup"><span data-stu-id="f0ecc-119">Stopped</span></span>       | <span data-ttu-id="f0ecc-120">目前媒體專案的播放已停止。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-120">Playback of the current media item is stopped.</span></span>                                                                              |
| <span data-ttu-id="f0ecc-121">2</span><span class="sxs-lookup"><span data-stu-id="f0ecc-121">2</span></span>     | <span data-ttu-id="f0ecc-122">已暫停</span><span class="sxs-lookup"><span data-stu-id="f0ecc-122">Paused</span></span>        | <span data-ttu-id="f0ecc-123">目前媒體專案的播放已暫停。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-123">Playback of the current media item is paused.</span></span> <span data-ttu-id="f0ecc-124">當媒體專案暫停時，就會從相同的位置開始繼續播放。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-124">When a media item is paused, resuming playback begins from the same location.</span></span> |
| <span data-ttu-id="f0ecc-125">3</span><span class="sxs-lookup"><span data-stu-id="f0ecc-125">3</span></span>     | <span data-ttu-id="f0ecc-126">正在播放</span><span class="sxs-lookup"><span data-stu-id="f0ecc-126">Playing</span></span>       | <span data-ttu-id="f0ecc-127">目前的媒體專案現正播放中。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-127">The current media item is playing.</span></span>                                                                                          |
| <span data-ttu-id="f0ecc-128">4</span><span class="sxs-lookup"><span data-stu-id="f0ecc-128">4</span></span>     | <span data-ttu-id="f0ecc-129">ScanForward</span><span class="sxs-lookup"><span data-stu-id="f0ecc-129">ScanForward</span></span>   | <span data-ttu-id="f0ecc-130">目前的媒體專案是快速轉送。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-130">The current media item is fast forwarding.</span></span>                                                                                  |
| <span data-ttu-id="f0ecc-131">5</span><span class="sxs-lookup"><span data-stu-id="f0ecc-131">5</span></span>     | <span data-ttu-id="f0ecc-132">ScanReverse</span><span class="sxs-lookup"><span data-stu-id="f0ecc-132">ScanReverse</span></span>   | <span data-ttu-id="f0ecc-133">目前的媒體專案是快速倒轉。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-133">The current media item is fast rewinding.</span></span>                                                                                   |
| <span data-ttu-id="f0ecc-134">6</span><span class="sxs-lookup"><span data-stu-id="f0ecc-134">6</span></span>     | <span data-ttu-id="f0ecc-135">緩衝</span><span class="sxs-lookup"><span data-stu-id="f0ecc-135">Buffering</span></span>     | <span data-ttu-id="f0ecc-136">目前的媒體專案正在從伺服器取得額外的資料。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-136">The current media item is getting additional data from the server.</span></span>                                                          |
| <span data-ttu-id="f0ecc-137">7</span><span class="sxs-lookup"><span data-stu-id="f0ecc-137">7</span></span>     | <span data-ttu-id="f0ecc-138">等候中</span><span class="sxs-lookup"><span data-stu-id="f0ecc-138">Waiting</span></span>       | <span data-ttu-id="f0ecc-139">連接已建立，但伺服器不會傳送資料。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-139">Connection is established, but the server is not sending data.</span></span> <span data-ttu-id="f0ecc-140">正在等候會話開始。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-140">Waiting for session to begin.</span></span>                                |
| <span data-ttu-id="f0ecc-141">8</span><span class="sxs-lookup"><span data-stu-id="f0ecc-141">8</span></span>     | <span data-ttu-id="f0ecc-142">MediaEnded</span><span class="sxs-lookup"><span data-stu-id="f0ecc-142">MediaEnded</span></span>    | <span data-ttu-id="f0ecc-143">媒體專案已完成播放。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-143">Media item has completed playback.</span></span>                                                                                          |
| <span data-ttu-id="f0ecc-144">9</span><span class="sxs-lookup"><span data-stu-id="f0ecc-144">9</span></span>     | <span data-ttu-id="f0ecc-145">過渡</span><span class="sxs-lookup"><span data-stu-id="f0ecc-145">Transitioning</span></span> | <span data-ttu-id="f0ecc-146">正在準備新的媒體專案。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-146">Preparing new media item.</span></span>                                                                                                   |
| <span data-ttu-id="f0ecc-147">10</span><span class="sxs-lookup"><span data-stu-id="f0ecc-147">10</span></span>    | <span data-ttu-id="f0ecc-148">就緒</span><span class="sxs-lookup"><span data-stu-id="f0ecc-148">Ready</span></span>         | <span data-ttu-id="f0ecc-149">準備開始播放。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-149">Ready to begin playing.</span></span>                                                                                                     |
| <span data-ttu-id="f0ecc-150">11</span><span class="sxs-lookup"><span data-stu-id="f0ecc-150">11</span></span>    | <span data-ttu-id="f0ecc-151">重新</span><span class="sxs-lookup"><span data-stu-id="f0ecc-151">Reconnecting</span></span>  | <span data-ttu-id="f0ecc-152">重新連接到 stream。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-152">Reconnecting to stream.</span></span>                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="f0ecc-153">備註</span><span class="sxs-lookup"><span data-stu-id="f0ecc-153">Remarks</span></span>

<span data-ttu-id="f0ecc-154">Windows Media Player 狀態不保證會以任何特定順序發生。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-154">Windows Media Player states are not guaranteed to occur in any particular order.</span></span> <span data-ttu-id="f0ecc-155">此外，並非每個狀態都一定會在一連串的事件期間發生。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-155">Furthermore, not every state necessarily occurs during a sequence of events.</span></span> <span data-ttu-id="f0ecc-156">您不應該撰寫依賴狀態順序的程式碼。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-156">You should not write code that relies upon state order.</span></span>

## <a name="examples"></a><span data-ttu-id="f0ecc-157">範例</span><span class="sxs-lookup"><span data-stu-id="f0ecc-157">Examples</span></span>

<span data-ttu-id="f0ecc-158">下列 JScript 程式碼顯示 *播放機* 的使用。**playState** 屬性。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-158">The following JScript code shows the use of the *player*.**playState** property.</span></span> <span data-ttu-id="f0ecc-159">HTML 文字元素（名稱為 "myText"）會顯示目前的狀態。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-159">An HTML text element, named "myText", displays the current status.</span></span> <span data-ttu-id="f0ecc-160">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-160">The **Player** object was created with ID = "Player".</span></span>


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a><span data-ttu-id="f0ecc-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0ecc-161">Requirements</span></span>



| <span data-ttu-id="f0ecc-162">需求</span><span class="sxs-lookup"><span data-stu-id="f0ecc-162">Requirement</span></span> | <span data-ttu-id="f0ecc-163">值</span><span class="sxs-lookup"><span data-stu-id="f0ecc-163">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f0ecc-164">版本</span><span class="sxs-lookup"><span data-stu-id="f0ecc-164">Version</span></span><br/> | <span data-ttu-id="f0ecc-165">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f0ecc-165">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="f0ecc-166">DLL</span><span class="sxs-lookup"><span data-stu-id="f0ecc-166">DLL</span></span><br/>     | <dl> <span data-ttu-id="f0ecc-167"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0ecc-167"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0ecc-168">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0ecc-168">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0ecc-169">**Player 物件**</span><span class="sxs-lookup"><span data-stu-id="f0ecc-169">**Player Object**</span></span>](player-object.md)
</dt> <dt>

[<span data-ttu-id="f0ecc-170">**PlayStateChange 事件**</span><span class="sxs-lookup"><span data-stu-id="f0ecc-170">**Player.PlayStateChange Event**</span></span>](player-player-playstatechange.md)
</dt> </dl>

 

 





