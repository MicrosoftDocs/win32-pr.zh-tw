---
title: DownloadProgress
description: DownloadProgress 屬性會抓取下載完成的百分比。
ms.assetid: bb57ce84-babb-4dc2-bc2b-c40cbb587e91
keywords:
- DownloadProgress Windows Media Player
topic_type:
- apiref
api_name:
- Network.downloadProgress
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 605d7d08b346c5cc279176098b2a6d593a2fb925
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994629"
---
# <a name="networkdownloadprogress"></a><span data-ttu-id="a01af-104">DownloadProgress</span><span class="sxs-lookup"><span data-stu-id="a01af-104">Network.downloadProgress</span></span>

<span data-ttu-id="a01af-105">**DownloadProgress** 屬性會抓取下載完成的百分比。</span><span class="sxs-lookup"><span data-stu-id="a01af-105">The **downloadProgress** property retrieves the percentage of download completed.</span></span>

## <a name="syntax"></a><span data-ttu-id="a01af-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="a01af-106">Syntax</span></span>

<span data-ttu-id="a01af-107">*玩家*。*網路*。**downloadProgress**</span><span class="sxs-lookup"><span data-stu-id="a01af-107">*player*.*network*.**downloadProgress**</span></span>

## <a name="possible-values"></a><span data-ttu-id="a01af-108">可能的值</span><span class="sxs-lookup"><span data-stu-id="a01af-108">Possible Values</span></span>

<span data-ttu-id="a01af-109">這個屬性是唯讀的 **數位** (**long**) 。</span><span class="sxs-lookup"><span data-stu-id="a01af-109">This property is a read-only **Number** (**long**).</span></span>

## <a name="remarks"></a><span data-ttu-id="a01af-110">備註</span><span class="sxs-lookup"><span data-stu-id="a01af-110">Remarks</span></span>

<span data-ttu-id="a01af-111">當 Windows Media Player 控制項連接到可同時播放和下載的媒體檔案時， **downloadProgress** 屬性會傳回已下載的檔案總數百分比。</span><span class="sxs-lookup"><span data-stu-id="a01af-111">When the Windows Media Player control is connected to a media file that can be played and downloaded at the same time, the **downloadProgress** property returns the percentage of the total file that has been downloaded.</span></span> <span data-ttu-id="a01af-112">這項功能目前只在 web 伺服器上受到支援。</span><span class="sxs-lookup"><span data-stu-id="a01af-112">This feature is currently supported only on web servers.</span></span> <span data-ttu-id="a01af-113">您可以同時下載並播放下列檔案格式：</span><span class="sxs-lookup"><span data-stu-id="a01af-113">The following file formats can be downloaded and played simultaneously:</span></span>

-   <span data-ttu-id="a01af-114">進階系統格式 (ASF)</span><span class="sxs-lookup"><span data-stu-id="a01af-114">Advanced Systems Format (ASF)</span></span>
-   <span data-ttu-id="a01af-115">Windows Media 音訊 (WMA)</span><span class="sxs-lookup"><span data-stu-id="a01af-115">Windows Media Audio (WMA)</span></span>
-   <span data-ttu-id="a01af-116">Windows Media 視訊 (WMV)</span><span class="sxs-lookup"><span data-stu-id="a01af-116">Windows Media Video (WMV)</span></span>
-   <span data-ttu-id="a01af-117">MP3</span><span class="sxs-lookup"><span data-stu-id="a01af-117">MP3</span></span>
-   <span data-ttu-id="a01af-118">MPEG</span><span class="sxs-lookup"><span data-stu-id="a01af-118">MPEG</span></span>
-   <span data-ttu-id="a01af-119">WAV</span><span class="sxs-lookup"><span data-stu-id="a01af-119">WAV</span></span>
-   <span data-ttu-id="a01af-120">某些 AVI 檔案</span><span class="sxs-lookup"><span data-stu-id="a01af-120">Some AVI files</span></span>

<span data-ttu-id="a01af-121">使用 *播放*。**緩衝** 事件，以判斷下載開始和結束的時間。</span><span class="sxs-lookup"><span data-stu-id="a01af-121">Use the *Player*.**Buffering** event to determine when the downloading begins and ends.</span></span>

## <a name="examples"></a><span data-ttu-id="a01af-122">範例</span><span class="sxs-lookup"><span data-stu-id="a01af-122">Examples</span></span>

<span data-ttu-id="a01af-123">下列 JScript 範例會使用 *網路*。**downloadProgress** 顯示已完成的下載百分比。</span><span class="sxs-lookup"><span data-stu-id="a01af-123">The following JScript example uses *Network*.**downloadProgress** to display the percentage of downloading completed.</span></span> <span data-ttu-id="a01af-124">這項資訊會顯示在以 ID = "DP" 建立的 HTML DIV 中。</span><span class="sxs-lookup"><span data-stu-id="a01af-124">The information is displayed in an HTML DIV created with ID = "DP".</span></span> <span data-ttu-id="a01af-125">此範例使用具有1秒間隔的計時器來更新顯示。</span><span class="sxs-lookup"><span data-stu-id="a01af-125">The example uses a timer with a 1 second interval to update the display.</span></span> <span data-ttu-id="a01af-126">使用 ID = "Player" 建立 **player** 物件。</span><span class="sxs-lookup"><span data-stu-id="a01af-126">The **Player** object was created with ID = "Player".</span></span>


```JScript
<!-- Create an event handler for buffering. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   var idI; // Variable for the interval id.
   
   // Test whether downloading has started or stopped.
   if (true == Start){ 
      // Start the timer. Call the function to update the display.
      idI = window.setInterval("UpdateDP()", 1000);
   }
   else{
      // Downloading is complete. Stop the timer.
      window.clearInterval(idI);
   }
</SCRIPT>

<!-- Put the function to update the display in a separate code block. -->
<SCRIPT>
function UpdateDP(){
   DP.innerHTML = "";
   DP.innerHTML = "Download progress: " + Player.network.downloadProgress;
   DP.innerHTML += " percent complete";
}
</SCRIPT>

```



## <a name="requirements"></a><span data-ttu-id="a01af-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="a01af-127">Requirements</span></span>



| <span data-ttu-id="a01af-128">需求</span><span class="sxs-lookup"><span data-stu-id="a01af-128">Requirement</span></span> | <span data-ttu-id="a01af-129">值</span><span class="sxs-lookup"><span data-stu-id="a01af-129">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="a01af-130">版本</span><span class="sxs-lookup"><span data-stu-id="a01af-130">Version</span></span><br/> | <span data-ttu-id="a01af-131">Windows Media Player 7.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="a01af-131">Windows Media Player version 7.0 or later.</span></span><br/>                              |
| <span data-ttu-id="a01af-132">DLL</span><span class="sxs-lookup"><span data-stu-id="a01af-132">DLL</span></span><br/>     | <dl> <span data-ttu-id="a01af-133"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a01af-133"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a01af-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a01af-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a01af-135">**Network 物件**</span><span class="sxs-lookup"><span data-stu-id="a01af-135">**Network Object**</span></span>](network-object.md)
</dt> <dt>

[<span data-ttu-id="a01af-136">**Media Player. 緩衝事件**</span><span class="sxs-lookup"><span data-stu-id="a01af-136">**Player.Buffering Event**</span></span>](player-player-buffering.md)
</dt> </dl>

 

 





