---
title: IWMPMedia durationString 屬性
description: DurationString 屬性會取得字串，表示目前媒體專案的持續時間（以 HH MM SS 格式表示）。
ms.assetid: de33c737-d73e-41f0-9c1b-944279194738
keywords:
- durationString 屬性 Windows Media Player
- durationString 屬性 Windows Media Player，IWMPMedia 介面
- IWMPMedia 介面 Windows Media Player，durationString 屬性
topic_type:
- apiref
api_name:
- IWMPMedia.durationString
- IWMPMedia.get_durationString
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9e6bc732388036aa9e79aeedd988de94fa263bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976229"
---
# <a name="iwmpmediadurationstring-property"></a>IWMPMedia：:d urationString 屬性

**DurationString** 屬性會取得字串，指出目前媒體專案的持續時間（以 HH： MM： SS 格式表示）。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public System.String durationString {get;}
```


```VB

Public ReadOnly Property durationString As System.String
```





## <a name="property-value"></a>屬性值

持續期間的 **system.string** 。

## <a name="remarks"></a>備註

如果這個屬性與 AxWindowsMediaPlayer. currentMedia 中所指定的媒體專案不同，它可能不包含有效的值。 如果媒體專案的長度不到一小時，則會省略傳回值的時數部分。

使用這個屬性之前，您必須擁有程式庫的讀取權限。 如需詳細資訊，請參閱連結 [庫存取](library-access.md)。

## <a name="examples"></a>範例

下列範例會使用 **durationString** ，以標籤中的格式化文字顯示目前媒體專案的持續時間。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
// Create an event handler for the OpenStateChange event.
private void player_OpenStateChange(object sender, AxWMPLib._WMPOCXEvents_OpenStateChangeEvent e)
{
    // Test whether the current media item is open.
    if (e.newState == (int)WMPLib.WMPOpenState.wmposMediaOpen)
    {
         // Display the formatted duration string in the label.
         mediaDuration.Text = player.currentMedia.durationString;
    }
}
```


```VB

' Create an event handler for the OpenStateChange event.
Public Sub player_OpenStateChange(ByVal sender As Object, ByVal e As AxWMPLib._WMPOCXEvents_OpenStateChangeEvent) Handles player.OpenStateChange

    &#39; Test whether the current media item is open.
    If (e.newState = 13) Then

        &#39; Display the formatted duration string in the label.
        mediaDuration.Text = player.currentMedia.durationString

    End If

End Sub
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer. currentMedia (VB 和 c # )**](axwmplib-axwindowsmediaplayer-currentmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia 介面 (VB 和 c # )**](iwmpmedia--vb-and-c.md)
</dt> <dt>

[**IWMPMedia duration (VB 和 c # )**](wmplibiwmpmedia-iwmpmedia-duration--vb-and-c.md)
</dt> </dl>

 

 





