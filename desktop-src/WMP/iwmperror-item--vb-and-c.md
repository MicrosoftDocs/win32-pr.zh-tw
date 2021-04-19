---
title: 'IWMPError (VB 和 C ) '
description: 專案屬性 (\_ 在 C \ ) 中的 get 專案方法，會在錯誤佇列中的指定索引處取得 IWMPErrorItem 介面。
ms.assetid: acfaaaa5-eb13-4ba0-8417-4229adc62c5d
keywords:
- " (VB 和 C ) Windows Media Player 的 IWMPError 專案"
topic_type:
- apiref
api_name:
- IWMPError.Item (VB and C )
api_location:
- Interop.WMPLib.dll
api_type:
- Assembly
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e9217ec772512171c828dd0dad06ec8fe3704dba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981365"
---
# <a name="iwmperroritem-vb-and-c"></a>IWMPError (VB 和 c # ) 

**Item** 屬性 (c # 中的 **get \_ Item** 方法 ) 在錯誤佇列中的指定索引處取得 **IWMPErrorItem** 介面。


```
[Visual Basic]
ReadOnly Property Item(
  dwIndex As System.Integer
) As IWMPErrorItem
```




```
[C#]
IWMPErrorItem get_Item (
  System.Int32 dwIndex
);
```



## <a name="parameters"></a>參數

*dwIndex*

在錯誤佇列中， **IWMPErrorItem** 介面之以零為基底之索引的 **system.object** 。

## <a name="property-value"></a>屬性值

**WMPLib IWMPErrorItem** 介面。

## <a name="remarks"></a>備註

Windows Media Player 可能會產生一些錯誤，以回應錯誤狀況。 這個屬性會使用索引編號取得佇列中的特定錯誤。 錯誤佇列的索引編號開頭為零。

如果您選擇顯示自訂錯誤訊息，則應將 **IWMPSettings enableErrorDialogs** 設定為 **false** 。

## <a name="examples"></a>範例

下列範例會使用 **Item** 屬性 (c # 中的 **get \_ Item** 方法 ) 在錯誤事件處理常式中，以抓取和顯示錯誤佇列中最新錯誤的相關資訊。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void player_ErrorEvent_get_Item(object sender, System.EventArgs e)
{
    // Store the index of the most recent error.
    int max = (player.Error.errorCount - 1);

    // Get an interface for the most recent error item. Cast it to
    // a WMPLib.IWMPErrorItem2 interface to get all of the available functionality.
    WMPLib.IWMPErrorItem2 errItem = (WMPLib.IWMPErrorItem2)player.Error.get_Item(max);

    // Use the interface to access and store the error info.
    int errNum = errItem.errorCode;
    string errDesc = errItem.errorDescription;

    // Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + ":  " + errDesc);
}
```


```VB

Public Sub player_ErrorEvent_get_Item(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the index of the most recent error.
    Dim max As Integer = (player.Error.errorCount - 1)

    &#39; Get an interface for the most recent error item. 
    Dim errItem As WMPLib.IWMPErrorItem2 = player.Error.Item(max)

    &#39; Use the interface to access and store the error info.
    Dim errNum As Integer = errItem.errorCode
    Dim errDesc As String = errItem.errorDescription

    &#39; Display the error info.
    System.Windows.Forms.MessageBox.Show(errNum.ToString() + &quot;:  &quot; + errDesc)

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

[**IWMPError 介面 (VB 和 c # )**](iwmperror--vb-and-c.md)
</dt> <dt>

[**IWMPErrorItem 介面 (VB 和 c # )**](iwmperroritem--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. enableErrorDialogs (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





