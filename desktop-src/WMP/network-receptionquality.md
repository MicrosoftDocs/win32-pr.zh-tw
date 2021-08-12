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
ms.openlocfilehash: 159bcac192d5a5bd9197ecc3ea935027dd6d707dde42a54c64a318459ae00040
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574154"
---
# <a name="networkreceptionquality"></a>ReceptionQuality

**ReceptionQuality** 屬性會抓取過去30秒內收到的封包百分比。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**receptionQuality**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

串流期間接收、遺失和復原的封包數目會每秒監視一次。 **receptionQuality** 是過去30秒內未遺失的封包百分比。

每次播放都會停止並重新啟動，這個屬性會設定為零。 如果播放暫停，則不會重設。

這個屬性只有在執行時間才會傳回有效的資訊，而且只有在 *播放玩家* 時才會傳回。也會設定 **URL** 屬性。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**receptionQuality** ，顯示已接收的封包百分比。 這項資訊會顯示在以 ID = "RQ" 建立的 HTML DIV 中。 此範例使用具有30秒間隔的計時器來更新顯示。 使用 ID = "Player" 建立 **player** 物件。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Network 物件**](network-object.md)
</dt> <dt>

[**Player. URL**](player-url.md)
</dt> </dl>

 

 





