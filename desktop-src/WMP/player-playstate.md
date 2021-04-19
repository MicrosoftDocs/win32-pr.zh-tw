---
title: PlayState
description: PlayState 屬性會抓取值，指出 Windows Media Player 作業的狀態。
ms.assetid: 8ed1ee1f-8731-402a-aff5-5ae513a35eea
keywords:
- PlayState Windows Media Player
topic_type:
- apiref
api_name:
- Player.playState
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c442b1be9e1ea15b8a54c2dafc264edf8aeb479
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984053"
---
# <a name="playerplaystate"></a>PlayState

**PlayState** 屬性會抓取值，指出 Windows Media Player 作業的狀態。

## <a name="syntax"></a>Syntax

*玩家* 。**playState**

## <a name="possible-values"></a>可能的值

這個屬性是唯讀的 **數位** (**long**) 。 C 樣式的列舉常數可以藉由在 state 值前面加上 "wmpps" 來衍生。 例如，播放狀態的常數是 **wmppsPlaying**。



| 值 | 州         | 描述                                                                                                                 |
|-------|---------------|-----------------------------------------------------------------------------------------------------------------------------|
| 0     | 未定義     | Windows Media Player 處於未定義狀態。                                                                              |
| 1     | 已停止       | 目前媒體專案的播放已停止。                                                                              |
| 2     | 已暫停        | 目前媒體專案的播放已暫停。 當媒體專案暫停時，就會從相同的位置開始繼續播放。 |
| 3     | 正在播放       | 目前的媒體專案現正播放中。                                                                                          |
| 4     | ScanForward   | 目前的媒體專案是快速轉送。                                                                                  |
| 5     | ScanReverse   | 目前的媒體專案是快速倒轉。                                                                                   |
| 6     | 緩衝     | 目前的媒體專案正在從伺服器取得額外的資料。                                                          |
| 7     | 等候中       | 連接已建立，但伺服器不會傳送資料。 正在等候會話開始。                                |
| 8     | MediaEnded    | 媒體專案已完成播放。                                                                                          |
| 9     | 過渡 | 正在準備新的媒體專案。                                                                                                   |
| 10    | 就緒         | 準備開始播放。                                                                                                     |
| 11    | 重新  | 重新連接到 stream。                                                                                                     |



 

## <a name="remarks"></a>備註

Windows Media Player 狀態不保證會以任何特定順序發生。 此外，並非每個狀態都一定會在一連串的事件期間發生。 您不應該撰寫依賴狀態順序的程式碼。

## <a name="examples"></a>範例

下列 JScript 程式碼顯示 *播放機* 的使用。**playState** 屬性。 HTML 文字元素（名稱為 "myText"）會顯示目前的狀態。 使用 ID = "Player" 建立 **player** 物件。


```JScript
// Test whether Windows Media Player is in the playing state.
if (3 == Player.playState)
    myText.value = "Windows Media Player is playing!";
else
    myText.value = "Windows Media Player is NOT playing!";
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**PlayStateChange 事件**](player-player-playstatechange.md)
</dt> </dl>

 

 





