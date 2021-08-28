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
ms.openlocfilehash: 65de3f7b1b58dfb90f76436f324dcc3d4fc3fe9a24b7c60ca3db888771f9192d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119901748"
---
# <a name="networkbufferingprogress"></a>BufferingProgress

**BufferingProgress** 屬性會抓取已完成的緩衝百分比。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**bufferingProgress**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

每次播放都會停止並重新啟動，這個屬性會設定為零。 如果播放暫停，則不會重設。

緩衝處理只適用于串流內容。 這個屬性只會在執行時間（當 *玩家*）時傳回有效的資訊。已設定 **URL** 屬性。

使用 *Player*. * * * * 緩衝 * * * * 事件來判斷緩衝的開始或停止時間。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**bufferingProgress** ，顯示已完成的緩衝百分比。 這項資訊會顯示在以 ID = "BP" 建立的 HTML DIV 中。 此範例使用具有1秒間隔的計時器來更新顯示。 使用 ID = "Player" 建立 **player** 物件。


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
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





