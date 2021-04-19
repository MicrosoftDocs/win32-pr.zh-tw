---
title: IWMPErrorItem errorCode 屬性
description: ErrorCode 屬性會取得目前的錯誤碼。
ms.assetid: 00719067-685d-4ef2-9eec-72c7892fcdb9
keywords:
- errorCode 屬性 Windows Media Player
- errorCode 屬性 Windows Media Player，IWMPErrorItem 介面
- IWMPErrorItem 介面 Windows Media Player，errorCode 屬性
topic_type:
- apiref
api_name:
- IWMPErrorItem.errorCode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f284d5655fc1f4007695a1f681c744a9c5c6fc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991348"
---
# <a name="iwmperroritemerrorcode-property"></a>IWMPErrorItem：： errorCode 屬性

**ErrorCode** 屬性會取得目前的錯誤碼。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 errorCode {get; set;}
```


```VB

Public ReadOnly Property errorCode As System.Int32
```





## <a name="property-value"></a>屬性值

錯誤碼的 **system.object** 。

## <a name="remarks"></a>備註

如果您選擇顯示自訂錯誤訊息，則應將 **IWMPSettings enableErrorDialogs** 設定為 **false** 。

## <a name="examples"></a>範例

下列範例會在錯誤事件處理常式中使用 **errorCode** ，向使用者顯示錯誤碼。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void player_ErrorEvent_errorCode(object sender, System.EventArgs e)
{
    // Get the error code for the first error item.
    int errCode = player.Error.get_Item(0).errorCode;

    // Display the error code.
    System.Windows.Forms.MessageBox.Show("Error number: " + errCode.ToString());
}
```


```VB

Public Sub player_ErrorEvent_errorCode(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Get the error code for the first error item.
    Dim errCode As Integer = player.Error.Item(0).errorCode

    &#39; Display the error code.
    System.Windows.Forms.MessageBox.Show(&quot;Error number: &quot; + errCode.ToString())

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

[**IWMPErrorItem 介面 (VB 和 c # )**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





