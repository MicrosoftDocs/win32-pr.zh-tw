---
title: IWMPError errorCount 屬性
description: ErrorCount 屬性會取得錯誤佇列中的錯誤數目。
ms.assetid: a30750c8-2025-4087-bd2b-f313ccbde38c
keywords:
- errorCount 屬性 Windows Media Player
- errorCount 屬性 Windows Media Player，IWMPError 介面
- IWMPError 介面 Windows Media Player，errorCount 屬性
topic_type:
- apiref
api_name:
- IWMPError.errorCount
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b62c16f07260847c91f1c9f18885587444a4ceb8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999497"
---
# <a name="iwmperrorerrorcount-property"></a>IWMPError：： errorCount 屬性

**ErrorCount** 屬性會取得錯誤佇列中的錯誤數目。

## <a name="syntax"></a>Syntax


```CSharp
public System.Int32 errorCount {get; set;}
```


```VB

Public ReadOnly Property errorCount As System.Int32
```





## <a name="property-value"></a>屬性值

錯誤數目的 **system.object** 。

## <a name="remarks"></a>備註

如果您選擇顯示自訂錯誤訊息，則應將 **IWMPSettings enableErrorDialogs** 設定為 **false** 。

## <a name="examples"></a>範例

下列範例會在錯誤事件處理常式中使用 **errorCount** ，警示使用者錯誤佇列中的最新錯誤。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void player_ErrorEvent_errorCount(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Get the description of the last error. Error items start at zero,
    // so the item index will always be one less than the error count.
    string errDesc = player.Error.get_Item(max-1).errorDescription;

    // Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc);
}
```


```VB

Public Sub player_ErrorEvent_errorCount(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Get the description of the last error. Error items start at zero,
    &#39; so the item index will always be one less than the error count.
    Dim errDesc As String = player.Error.Item(max - 1).errorDescription

    &#39; Display the error description.
    System.Windows.Forms.MessageBox.Show(errDesc)

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

[**IWMPSettings. enableErrorDialogs (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-enableerrordialogs--vb-and-c.md)
</dt> </dl>

 

 





