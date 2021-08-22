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
ms.openlocfilehash: ca9544332fa6e81211dae45cddc74ce9daee0d47e70d467137aaca2084bbc6f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054496"
---
# <a name="networkreceivedpackets"></a>ReceivedPackets

**ReceivedPackets** 屬性會抓取收到的封包數目。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**receivedPackets**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

每次停止並重新啟動剪輯播放時，這個屬性會設定為零。 如果檔案播放暫停，則不會重設。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**receivedPackets** 以顯示收到的封包數目。 這項資訊會顯示在以 ID = "RP" 建立的 HTML DIV 中。 此範例使用具有1秒間隔的計時器來更新顯示。 使用 ID = "Player" 建立 **player** 物件。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Network 物件**](network-object.md)
</dt> </dl>

 

 





