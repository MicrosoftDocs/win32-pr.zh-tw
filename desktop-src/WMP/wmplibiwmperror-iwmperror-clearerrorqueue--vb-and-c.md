---
title: IWMPError clearErrorQueue 方法
description: ClearErrorQueue 方法會清除錯誤佇列中的錯誤。 |IWMPError clearErrorQueue 方法
ms.assetid: a8e8e666-56e4-4e75-9ed5-2714d272ce7c
keywords:
- clearErrorQueue 方法 Windows Media Player
- clearErrorQueue 方法 Windows Media Player，IWMPError 介面
- IWMPError 介面 Windows Media Player，clearErrorQueue 方法
topic_type:
- apiref
api_name:
- IWMPError.clearErrorQueue
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f75b4e4d2a0e80a3f55a38744758497abc71f5899498fee95ee3b3db752631c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000448"
---
# <a name="iwmperrorclearerrorqueue-method"></a>IWMPError：： clearErrorQueue 方法

**ClearErrorQueue** 方法會清除錯誤佇列中的錯誤。

## <a name="syntax"></a>語法


```CSharp
public void clearErrorQueue();
```


```VB

Public Sub clearErrorQueue()
Implements IWMPError.clearErrorQueue
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

使用這個方法可在處理一系列錯誤之後清除錯誤佇列。

如果您選擇顯示自訂錯誤訊息，則應將 **IWMPSettings enableErrorDialogs** 設定為 **false** 。

## <a name="examples"></a>範例

下列範例會在顯示所有錯誤描述之後，于錯誤事件處理常式中使用 **clearErrorQueue** 來清空錯誤佇列。 **AxWMPLib. AxWindowsMediaPlayer** 物件是以名為 player 的變數來表示。


```CSharp
private void player_ErrorEvent_clearErrorQueue(object sender, System.EventArgs e)
{
    // Store the number of errors in the queue.
    int max = player.Error.errorCount;

    // Loop through the list of errors.
    for (int i = 0; i < max; i++)
    {
        // Get the description for this error.
        string errDesc = player.Error.get_Item(i).errorDescription;

        // Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc);
    }

    // Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue();
}
```


```VB

Public Sub player_ErrorEvent_clearErrorQueue(ByVal sender As Object, ByVal e As System.EventArgs) Handles player.ErrorEvent

    &#39; Store the number of errors in the queue.
    Dim max As Integer = player.Error.errorCount

    &#39; Loop through the list of errors.
    For i As Integer = 0 To (max - 1)

        &#39; Get the description for this error.
        Dim errDesc As String = player.Error.Item(i).errorDescription

        &#39; Display the error message.
        System.Windows.Forms.MessageBox.Show(errDesc)

    Next i

    &#39; Clear the error queue to prepare for the next group of errors.
    player.Error.clearErrorQueue()

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

 

 





