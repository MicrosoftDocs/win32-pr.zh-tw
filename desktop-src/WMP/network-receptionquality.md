---
title: ReceptionQuality
description: ReceptionQuality 屬性會抓取過去30秒內收到的封包百分比。
ms.assetid: 432f7f0a-0130-4485-b4a3-daa80ce9bb36
keywords:
- ReceptionQuality Windows Media Player
topic_type:
- apiref
api_name:
- Network.receptionQuality
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3706ba4d953f80c4a9e799971a7e73d49553c709
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978453"
---
# <a name="networkreceptionquality"></a><span data-ttu-id="59396-104">ReceptionQuality</span><span class="sxs-lookup"><span data-stu-id="59396-104">Network.receptionQuality</span></span>

<span data-ttu-id="59396-105">**ReceptionQuality** 屬性會抓取過去30秒內收到的封包百分比。</span><span class="sxs-lookup"><span data-stu-id="59396-105">The **receptionQuality** property retrieves the percentage of packets received in the last 30 seconds.</span></span>

## <a name="syntax"></a><span data-ttu-id="59396-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="59396-106">Syntax</span></span>

<span data-ttu-id="59396-107">*玩家*。*網路*。**receptionQuality**</span><span class="sxs-lookup"><span data-stu-id="59396-107">*player*.*network*.**receptionQuality**</span></span>

## <a name="possible-values"></a><span data-ttu-id="59396-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="59396-108">Possible Values</span></span>

<span data-ttu-id="59396-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="59396-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="59396-110">備註</span><span class="sxs-lookup"><span data-stu-id="59396-110">Remarks</span></span>

<span data-ttu-id="59396-111">串流期間接收、遺失和復原的封包數目會每秒監視一次。</span><span class="sxs-lookup"><span data-stu-id="59396-111">The number of packets received, lost, and recovered during streaming is monitored once every second.</span></span> <span data-ttu-id="59396-112">**receptionQuality** 是過去30秒內未遺失的封包百分比。</span><span class="sxs-lookup"><span data-stu-id="59396-112">**receptionQuality** is the percentage of packets not lost during the last 30 seconds.</span></span>

<span data-ttu-id="59396-113">每次播放都會停止並重新啟動，這個屬性會設定為零。</span><span class="sxs-lookup"><span data-stu-id="59396-113">Each time playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="59396-114">如果播放暫停，則不會重設。</span><span class="sxs-lookup"><span data-stu-id="59396-114">It is not reset if playback is paused.</span></span>

<span data-ttu-id="59396-115">這個屬性只有在執行時間才會傳回有效的資訊，而且只有在 *播放玩家* 時才會傳回。也會設定 **URL** 屬性。</span><span class="sxs-lookup"><span data-stu-id="59396-115">This property returns valid information only during run time and only if the *Player*.**URL** property is also set.</span></span>

## <a name="examples"></a><span data-ttu-id="59396-116">範例</span><span class="sxs-lookup"><span data-stu-id="59396-116">Examples</span></span>

<span data-ttu-id="59396-117">下列 JScript 範例會使用 *網路*。**receptionQuality** ，顯示已接收的封包百分比。</span><span class="sxs-lookup"><span data-stu-id="59396-117">The following JScript example uses *Network*.**receptionQuality** to display the percentage of packets received.</span></span> <span data-ttu-id="59396-118">這項資訊會顯示在以 ID = "RQ" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="59396-118">The information is displayed in an HTML DIV created with ID = "RQ".</span></span> <span data-ttu-id="59396-119">此範例使用具有30秒間隔的計時器來更新顯示。</span><span class="sxs-lookup"><span data-stu-id="59396-119">The example uses a timer with a 30-second interval to update the display.</span></span> <span data-ttu-id="59396-120">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="59396-120">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>
   var idI; // Variable for the interval id.

   // Test whether content is playing.
   if (3 == NewState){
         // Start the timer. Update the display every 30 seconds.
         idI = window.setInterval("UpdateRQ()", 30000);
   }

      else{
         // Not playing; stop the timer.
         window.clearInterval(idI);
      }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRQ(){
         RQ.innerHTML = "";
         RQ.innerHTML = "Reception quality: " + Player.network.receptionQuality;
         RQ.innerHTML += "%";         
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="59396-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="59396-121">Requirements</span></span>



| <span data-ttu-id="59396-122">需求</span><span class="sxs-lookup"><span data-stu-id="59396-122">Requirement</span></span> | <span data-ttu-id="59396-123">值</span><span class="sxs-lookup"><span data-stu-id="59396-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="59396-124">版本</span><span class="sxs-lookup"><span data-stu-id="59396-124">Version</span></span><br/> | <span data-ttu-id="59396-125">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="59396-125">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="59396-126">DLL</span><span class="sxs-lookup"><span data-stu-id="59396-126">DLL</span></span><br/>     | <dl> <span data-ttu-id="59396-127"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59396-127"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59396-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59396-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59396-129">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="59396-129">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="59396-130">**Player. URL**</span><span class="sxs-lookup"><span data-stu-id="59396-130">**Player.URL**</span></span>](player-url.md)
</dt> </dl>

 

 





