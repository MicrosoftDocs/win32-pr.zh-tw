---
title: BufferingCount
description: BufferingCount 屬性會捕獲在播放播放期間緩衝處理的次數。
ms.assetid: 25a58795-161e-4290-8ea7-51acca968ef9
keywords:
- BufferingCount Windows Media Player
topic_type:
- apiref
api_name:
- Network.bufferingCount
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 524dc66c7f4ed1d413f264a91ae9385d458d632b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999155"
---
# <a name="networkbufferingcount"></a>BufferingCount

**BufferingCount** 屬性會捕獲在播放播放期間緩衝處理的次數。

## <a name="syntax"></a>Syntax

*玩家*。*網路*。**bufferingCount**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。

## <a name="remarks"></a>備註

每次播放都會停止並重新啟動，這個屬性會設定為零。 如果播放暫停，則不會重設。

緩衝處理只適用于串流內容。 這個屬性只會在執行時間于 *播放玩家* 時傳回有效的資訊。已設定 **URL** 屬性。

## <a name="examples"></a>範例

下列 JScript 範例會使用 *網路*。**bufferingCount** ，以顯示在播放期間進行緩衝處理的次數。 這項資訊會顯示在以 ID = "CB" 建立的 HTML DIV 中。 使用 ID = "Player" 建立 **player** 物件。


```JScript
<!-- Create an event handler. -->
<SCRIPT FOR = Player EVENT = buffering(Start)>
   if (true == Start) 
      CB.innerHTML = "Buffering count: " + Player.network.bufferingCount;
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

 

 





