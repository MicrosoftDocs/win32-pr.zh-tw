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
ms.openlocfilehash: 464f7ad27603e506632d87254eaa4f76cbedf39ed15e353050cd13da0fa46204
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134931"
---
# <a name="networkrecoveredpackets"></a>RecoveredPackets

**RecoveredPackets** 屬性會捕獲已復原的封包數目。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**recoveredPackets**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

每次播放都會停止並重新啟動，這個屬性會設定為零。 如果播放暫停，則不會重設。

這個屬性只有在執行時間才會傳回有效的資訊，而且只有在 *播放玩家* 時才會傳回。也會設定 **URL** 屬性。 使用 HTTP 通訊協定時，它會等於零，而不會失真。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**recoveredPackets** ，顯示已復原的封包數目。 這項資訊會顯示在以 ID = "PR" 建立的 HTML DIV 中。 此範例使用具有1秒間隔的計時器來更新顯示。 使用 ID = "Player" 建立 **player** 物件。


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

 

 





