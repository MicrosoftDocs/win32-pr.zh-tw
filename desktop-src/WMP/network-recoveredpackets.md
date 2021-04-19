---
title: RecoveredPackets
description: RecoveredPackets 屬性會捕獲已復原的封包數目。
ms.assetid: ce10b906-2e8b-4b9f-83d0-56ba67cacd3f
keywords:
- RecoveredPackets Windows Media Player
topic_type:
- apiref
api_name:
- Network.recoveredPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a4222033d7e124e6ef29714bc47faf5664950fa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998620"
---
# <a name="networkrecoveredpackets"></a><span data-ttu-id="cfcfc-104">RecoveredPackets</span><span class="sxs-lookup"><span data-stu-id="cfcfc-104">Network.recoveredPackets</span></span>

<span data-ttu-id="cfcfc-105">**RecoveredPackets** 屬性會捕獲已復原的封包數目。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-105">The **recoveredPackets** property retrieves the number of recovered packets.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfcfc-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfcfc-106">Syntax</span></span>

<span data-ttu-id="cfcfc-107">*玩家*。*網路*。**recoveredPackets**</span><span class="sxs-lookup"><span data-stu-id="cfcfc-107">*player*.*network*.**recoveredPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="cfcfc-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="cfcfc-108">Possible Values</span></span>

<span data-ttu-id="cfcfc-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="cfcfc-110">備註</span><span class="sxs-lookup"><span data-stu-id="cfcfc-110">Remarks</span></span>

<span data-ttu-id="cfcfc-111">每次播放都會停止並重新啟動，這個屬性會設定為零。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-111">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="cfcfc-112">如果播放暫停，則不會重設。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-112">It is not reset if playback is paused.</span></span>

<span data-ttu-id="cfcfc-113">這個屬性只有在執行時間才會傳回有效的資訊，而且只有在 *播放玩家* 時才會傳回。也會設定 **URL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-113">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span> <span data-ttu-id="cfcfc-114">使用 HTTP 通訊協定時，它會等於零，而不會失真。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-114">It will equal zero when using the HTTP protocol, which is lossless.</span></span>

## <a name="examples"></a><span data-ttu-id="cfcfc-115">範例</span><span class="sxs-lookup"><span data-stu-id="cfcfc-115">Examples</span></span>

<span data-ttu-id="cfcfc-116">下列 JScript 範例會使用 *網路*。**recoveredPackets** ，顯示已復原的封包數目。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-116">The following JScript example uses *Network*.**recoveredPackets** to display the number of recovered packets.</span></span> <span data-ttu-id="cfcfc-117">這項資訊會顯示在以 ID = "PR" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-117">The information is displayed in an HTML DIV created with ID = "PR".</span></span> <span data-ttu-id="cfcfc-118">此範例使用具有1秒間隔的計時器來更新顯示。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-118">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="cfcfc-119">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-119">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
      // Start the timer. Call the function to update the display every second.
      idI = window.setInterval("UpdatePR()", 1000);
   }
   else{
      // Not playing; stop the timer.
      window.clearInterval(idI);
   }   
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdatePR(){
   PR.innerHTML = "";
   PR.innerHTML = "Packets recovered: " + Player.network.recoveredPackets;
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="cfcfc-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfcfc-120">Requirements</span></span>



| <span data-ttu-id="cfcfc-121">需求</span><span class="sxs-lookup"><span data-stu-id="cfcfc-121">Requirement</span></span> | <span data-ttu-id="cfcfc-122">值</span><span class="sxs-lookup"><span data-stu-id="cfcfc-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="cfcfc-123">版本</span><span class="sxs-lookup"><span data-stu-id="cfcfc-123">Version</span></span><br/> | <span data-ttu-id="cfcfc-124">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="cfcfc-124">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="cfcfc-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cfcfc-125">DLL</span></span><br/>     | <dl> <span data-ttu-id="cfcfc-126"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfcfc-126"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfcfc-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfcfc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfcfc-128">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="cfcfc-128">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="cfcfc-129">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="cfcfc-129">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





