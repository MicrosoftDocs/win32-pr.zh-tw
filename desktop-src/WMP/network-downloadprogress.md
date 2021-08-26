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
ms.openlocfilehash: ffc8d2707cd5fc24129363d53f9ee58fedf7b15c5da4eb5b80f032524ee66c09
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901718"
---
# <a name="networkdownloadprogress"></a>DownloadProgress

**DownloadProgress** 屬性會抓取下載完成的百分比。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**downloadProgress**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

當 Windows Media Player 控制項連接到可同時播放和下載的媒體檔案時， **downloadProgress** 屬性會傳回已下載的檔案總數百分比。 這項功能目前只在 web 伺服器上受到支援。 您可以同時下載並播放下列檔案格式：

-   進階系統格式 (ASF)
-   Windows Media 音訊 (WMA)
-   Windows Media 視訊 (WMV)
-   MP3
-   MPEG
-   WAV
-   某些 AVI 檔案

使用 *播放*。**緩衝** 事件，以判斷下載開始和結束的時間。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**downloadProgress** 顯示已完成的下載百分比。 這項資訊會顯示在以 ID = "DP" 建立的 HTML DIV 中。 此範例使用具有1秒間隔的計時器來更新顯示。 使用 ID = "Player" 建立 **player** 物件。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Network 物件**](network-object.md)
</dt> <dt>

[**Media Player. 緩衝事件**](player-player-buffering.md)
</dt> </dl>

 

 





