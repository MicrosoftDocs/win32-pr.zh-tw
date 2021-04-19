---
title: BufferingProgress
description: BufferingProgress 屬性會抓取已完成的緩衝百分比。
ms.assetid: d604159b-7c42-47f8-8085-53f859f24703
keywords:
- BufferingProgress Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9e3a4f37f8f6b8ffe8ff93ca72b0c9551d7e314
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989532"
---
# <a name="networkbufferingprogress"></a><span data-ttu-id="c37c0-104">BufferingProgress</span><span class="sxs-lookup"><span data-stu-id="c37c0-104">Network.bufferingProgress</span></span>

<span data-ttu-id="c37c0-105">**BufferingProgress** 屬性會抓取已完成的緩衝百分比。</span><span class="sxs-lookup"><span data-stu-id="c37c0-105">The **bufferingProgress** property retrieves the percentage of buffering completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="c37c0-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="c37c0-106">Syntax</span></span>

<span data-ttu-id="c37c0-107">*玩家*。*網路*。**bufferingProgress**</span><span class="sxs-lookup"><span data-stu-id="c37c0-107">*player*.*network*.**bufferingProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="c37c0-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="c37c0-108">Possible Values</span></span>

<span data-ttu-id="c37c0-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="c37c0-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="c37c0-110">備註</span><span class="sxs-lookup"><span data-stu-id="c37c0-110">Remarks</span></span>

<span data-ttu-id="c37c0-111">每次播放都會停止並重新啟動，這個屬性會設定為零。</span><span class="sxs-lookup"><span data-stu-id="c37c0-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="c37c0-112">如果播放暫停，則不會重設。</span><span class="sxs-lookup"><span data-stu-id="c37c0-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="c37c0-113">緩衝處理只適用于串流內容。</span><span class="sxs-lookup"><span data-stu-id="c37c0-113">Buffering only applies to streaming content.</span></span> <span data-ttu-id="c37c0-114">這個屬性只會在執行時間（當 *玩家*）時傳回有效的資訊。已設定 **URL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c37c0-114">This property returns valid information only during run time, when the *Player*.**URL** property is set.</span></span>

<span data-ttu-id="c37c0-115">使用 *Player*. \* \* \* \* 緩衝 \* \* \* \* 事件來判斷緩衝的開始或停止時間。</span><span class="sxs-lookup"><span data-stu-id="c37c0-115">Use the *Player*.\*\*\*\*Buffering\*\*\*\* event to determine when buffering starts or stops.</span></span>

## <a name="examples"></a><span data-ttu-id="c37c0-116">範例</span><span class="sxs-lookup"><span data-stu-id="c37c0-116">Examples</span></span>

<span data-ttu-id="c37c0-117">下列 JScript 範例會使用 *網路*。**bufferingProgress** ，顯示已完成的緩衝百分比。</span><span class="sxs-lookup"><span data-stu-id="c37c0-117">The following JScript example uses *Network*.**bufferingProgress** to display the percentage of buffering completed.</span></span> <span data-ttu-id="c37c0-118">這項資訊會顯示在以 ID = "BP" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="c37c0-118">The information is displayed in an HTML DIV created with ID = "BP".</span></span> <span data-ttu-id="c37c0-119">此範例使用具有1秒間隔的計時器來更新顯示。</span><span class="sxs-lookup"><span data-stu-id="c37c0-119">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="c37c0-120">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="c37c0-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.

   // Test whether buffering has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdateBP()", 1000);
   }

   else{
      // Buffering is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateBP(){
   BP.innerHTML = "";
   BP.innerHTML = "Buffering progress: " + Player.network.bufferingProgress;
   BP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="c37c0-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="c37c0-121">Requirements</span></span>



| <span data-ttu-id="c37c0-122">需求</span><span class="sxs-lookup"><span data-stu-id="c37c0-122">Requirement</span></span> | <span data-ttu-id="c37c0-123">值</span><span class="sxs-lookup"><span data-stu-id="c37c0-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c37c0-124">版本</span><span class="sxs-lookup"><span data-stu-id="c37c0-124">Version</span></span><br/> | <span data-ttu-id="c37c0-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="c37c0-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="c37c0-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c37c0-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="c37c0-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c37c0-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c37c0-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c37c0-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c37c0-129">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="c37c0-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="c37c0-130">**Media Player. 緩衝事件**</span><span class="sxs-lookup"><span data-stu-id="c37c0-130">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> <dt>

[<span data-ttu-id="c37c0-131">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="c37c0-131">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





