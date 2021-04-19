---
title: IWMPError webHelp 方法
description: WebHelp 方法會啟動 Windows Media Player 的 Web 說明頁，以顯示錯誤佇列中第一個錯誤的詳細資訊 (索引零) 。 |IWMPError webHelp 方法
ms.assetid: 30fc765a-04b2-44e5-99d8-0b4720ccbb25
keywords:
- webHelp 方法 Windows Media Player
- webHelp 方法 Windows Media Player，IWMPError 介面
- IWMPError 介面 Windows Media Player，webHelp 方法
topic_type:
- apiref
api_name:
- IWMPError.webHelp
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9b0cd48d45ac5e5e5d77d0150b8acdf13347e2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996271"
---
# <a name="iwmperrorwebhelp-method"></a>IWMPError：： webHelp 方法

**WebHelp** 方法會啟動 Windows Media Player 的 Web 說明頁，以顯示錯誤佇列中第一個錯誤的詳細資訊 (索引零) 。

## <a name="syntax"></a>語法


```CSharp
public void webHelp();
```


```VB

Public Sub webHelp()
Implements IWMPError.webHelp
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

Web 說明頁面一律包含 Windows Media Player 錯誤的最新和最詳細的資訊。 此方法會自動傳送 Web 說明所需的其他資訊，例如使用的作業系統版本。

若要直接存取 Web 說明頁面，請使用下列錯誤碼和支援中心連結：

-   [Windows Media Player 錯誤碼資訊](https://support.microsoft.com/kb/886273)
-   [Windows Media Player 解決方案中心](https://support.microsoft.com/ph/7763#tab0)

## <a name="examples"></a>範例

下列範例會建立一個按鈕，在瀏覽器中啟動 Microsoft Windows Media Player Web 說明頁。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


```CSharp
private void webHelpButton_Click(object sender, System.EventArgs e)
{
    // Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp();
}
```


```VB

Public Sub webHelpButton_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles webHelpButton.Click

    &#39; Launch the Microsoft Windows Media Player Web Help page in the browser.
    player.Error.webHelp()

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
</dt> </dl>

 

 





