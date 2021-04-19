---
title: IWMPSettings 靜音屬性
description: '[靜音] 屬性會取得或設定值，指出音訊是否為靜音。'
ms.assetid: d99e47db-70cc-41e0-aca9-b765b075e7b4
keywords:
- 靜音屬性 Windows Media Player
- 靜音屬性 Windows Media Player、IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，靜音屬性
topic_type:
- apiref
api_name:
- IWMPSettings.mute
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67518bb9a6eccee13e4cc262f37341d30689439e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001232"
---
# <a name="iwmpsettingsmute-property"></a>IWMPSettings：：靜音屬性

[ **靜音** ] 屬性會取得或設定值，指出音訊是否為靜音。

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean mute {get; set;}
```


```VB

Public Property mute As System.Boolean
```





## <a name="property-value"></a>屬性值

指出音訊是否已靜音的 **system.object** 值。 預設值為 **false**。

## <a name="examples"></a>範例

下列範例會建立核取方塊，並在方塊的核取狀態變更時，切換 [ **靜音** ] 屬性以將音訊靜音並取消靜音。 **AxWMPLib. AxWindowsMediaPlayer** 物件是由名為 player 的變數表示。


```CSharp
private void Mute_CheckStateChanged(object sender, System.EventArgs e)
{
    System.Windows.Forms.CheckBox Mute = (System.Windows.Forms.CheckBox)sender;

    // Change the check box text depending on the checked state.
    Mute.Text = Mute.Checked ? "Un-mute Audio" : Mute.Text = "Mute Audio";

    // Use the checked state to set the mute property. 
    player.settings.mute = Mute.Checked;
}
```


```VB

Public Sub Mute_CheckStateChanged(ByVal sender As Object, ByVal e As System.EventArgs) Handles Mute.CheckStateChanged

    Dim cb As System.Windows.Forms.CheckBox = sender

    &#39;  Change the check box text depending on the checked state.
    If (cb.Checked) Then

        cb.Text = &quot;Un-mute Audio&quot;

    Else

        cb.Text = &quot;Mute Audio&quot;

    End If

    &#39;  Use the checked state to set the mute property. 
    player.settings.mute = cb.Checked

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

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings (VB 和 c # 的速率 )**](wmplibiwmpsettings-iwmpsettings-rate--vb-and-c.md)
</dt> </dl>

 

 





