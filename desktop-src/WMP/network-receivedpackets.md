---
title: ReceivedPackets
description: ReceivedPackets 屬性會抓取收到的封包數目。
ms.assetid: db4f6f08-c248-4db8-ab19-fdd5d2794085
keywords:
- ReceivedPackets Windows Media Player
topic_type:
- apiref
api_name:
- Network.receivedPackets
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7bc792330cd107ca428ad0fbec930fe262a2f131
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001613"
---
# <a name="networkreceivedpackets"></a><span data-ttu-id="73ac6-104">ReceivedPackets</span><span class="sxs-lookup"><span data-stu-id="73ac6-104">Network.receivedPackets</span></span>

<span data-ttu-id="73ac6-105">**ReceivedPackets** 屬性會抓取收到的封包數目。</span><span class="sxs-lookup"><span data-stu-id="73ac6-105">The **receivedPackets** property retrieves the number of packets received.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ac6-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="73ac6-106">Syntax</span></span>

<span data-ttu-id="73ac6-107">*玩家*。*網路*。**receivedPackets**</span><span class="sxs-lookup"><span data-stu-id="73ac6-107">*player*.*network*.**receivedPackets**</span></span>

## <a name="possible-values"></a><span data-ttu-id="73ac6-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="73ac6-108">Possible Values</span></span>

<span data-ttu-id="73ac6-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="73ac6-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="73ac6-110">備註</span><span class="sxs-lookup"><span data-stu-id="73ac6-110">Remarks</span></span>

<span data-ttu-id="73ac6-111">每次停止並重新啟動剪輯播放時，這個屬性會設定為零。</span><span class="sxs-lookup"><span data-stu-id="73ac6-111">Each time clip playback is stopped and restarted, this property is set to zero.</span></span> <span data-ttu-id="73ac6-112">如果檔案播放暫停，則不會重設。</span><span class="sxs-lookup"><span data-stu-id="73ac6-112">It is not reset if file playback is paused.</span></span>

## <a name="examples"></a><span data-ttu-id="73ac6-113">範例</span><span class="sxs-lookup"><span data-stu-id="73ac6-113">Examples</span></span>

<span data-ttu-id="73ac6-114">下列 JScript 範例會使用 *網路*。**receivedPackets** 以顯示收到的封包數目。</span><span class="sxs-lookup"><span data-stu-id="73ac6-114">The following JScript example uses *Network*.**receivedPackets** to display the number of packets received.</span></span> <span data-ttu-id="73ac6-115">這項資訊會顯示在以 ID = "RP" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="73ac6-115">The information is displayed in an HTML DIV created with ID = "RP".</span></span> <span data-ttu-id="73ac6-116">此範例使用具有1秒間隔的計時器來更新顯示。</span><span class="sxs-lookup"><span data-stu-id="73ac6-116">The example uses a timer with a 1-second interval to update the display.</span></span> <span data-ttu-id="73ac6-117">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="73ac6-117">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for play state change. -->
<SCRIPT FOR = Player EVENT = PlayStateChange(NewState)>

   var idI; // Variable for the interval id.

   // Test whether packets may be arriving.
   switch (NewState){
      case 1, 2, 4, 5, 7, 8, 9:
          window.clearInterval(idI);
          break;

      default:
         idI = window.setInterval("UpdateRP()", 1000);

   }</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateRP(){
   RP.innerHTML = "";
   RP.innerHTML = "Packets received: " + Player.network.receivedPackets;         
}

```



## <a name="requirements"></a><span data-ttu-id="73ac6-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="73ac6-118">Requirements</span></span>



| <span data-ttu-id="73ac6-119">需求</span><span class="sxs-lookup"><span data-stu-id="73ac6-119">Requirement</span></span> | <span data-ttu-id="73ac6-120">值</span><span class="sxs-lookup"><span data-stu-id="73ac6-120">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="73ac6-121">版本</span><span class="sxs-lookup"><span data-stu-id="73ac6-121">Version</span></span><br/> | <span data-ttu-id="73ac6-122">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="73ac6-122">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="73ac6-123">DLL</span><span class="sxs-lookup"><span data-stu-id="73ac6-123">DLL</span></span><br/>     | <dl> <span data-ttu-id="73ac6-124"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73ac6-124"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73ac6-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73ac6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ac6-126">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="73ac6-126">**Network Object**</span></span>](network-object.md)
</dt> </dl>

 

 





