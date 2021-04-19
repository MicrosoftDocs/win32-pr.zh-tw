---
title: AxWindowsMediaPlayer. launchURL 方法
description: LaunchURL 方法會將 URL 傳送給使用者的預設瀏覽器，以呈現。 |AxWindowsMediaPlayer. launchURL 方法
ms.assetid: 3e8dfdbb-b5ad-44ea-97a6-e860386b7fb4
keywords:
- launchURL 方法 Windows Media Player
- launchURL 方法 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，launchURL 方法
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.launchURL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27fe8e544bb14b119785b26b9cb5be5cdad48015
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990789"
---
# <a name="axwindowsmediaplayerlaunchurl-method"></a>AxWindowsMediaPlayer. launchURL 方法

LaunchURL 方法會將 URL 傳送給使用者的預設瀏覽器，以呈現。

## <a name="syntax"></a>語法


```CSharp
public void launchURL(
  System.String bstrURL
);
```


```VB

Public Sub launchURL( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrURL* 
</dt> <dd>

要啟動之 URL 的 **system.string** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法只會使用 HTTP 或 HTTPS 通訊協定來開啟網頁。

## <a name="examples"></a>範例

下列範例會建立一個按鈕，當您按一下此按鈕時，就會在新的瀏覽器視窗中顯示 Microsoft 網站。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


```CSharp
private void goToMS_Click(object sender, System.EventArgs e)
{
    // Open the Microsoft website. 
    player.launchURL("https://www.microsoft.com");
}
```


```VB

Public Sub goToMS_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles goToMS.Click

    &#39; Open the Microsoft website. 
    player.launchURL(&quot;https://www.microsoft.com&quot;)

End Sub
```





## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> </dl>

 

 





