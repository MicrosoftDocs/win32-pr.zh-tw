---
title: AxWindowsMediaPlayer. URL 屬性
description: URL 屬性會取得或設定要播放之媒體專案的名稱。
ms.assetid: 521a3b39-efd6-45a7-895b-a9ae69e0bf39
keywords:
- URL 屬性 Windows Media Player
- URL 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，URL 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.URL
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d953f2d85fc1fd83edcd37a491cb2f7cbabc3e3dfaf61e48feb1cd30e6d01934
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120123878"
---
# <a name="axwindowsmediaplayerurl-property"></a>AxWindowsMediaPlayer. URL 屬性

URL 屬性會取得或設定要播放之媒體專案的名稱。

## <a name="syntax"></a>Syntax


```CSharp
public System.String URL {get; set;}
```


```VB

Public Property URL As System.String
```





## <a name="property-value"></a>屬性值

System.string，此為媒體專案的 URL。

## <a name="remarks"></a>備註

這個屬性只能設定為安全性區域中的 URL，該 URL 的安全性區域與呼叫的程式或網頁的安全性區域相同或較不嚴格。

如果使用功能變數名稱伺服器 (DNS) 名稱（而非 IP 位址）指定位址，則從防火牆後方開啟媒體專案的應用程式將會有較佳的效能。

請勿從事件處理常式程式碼呼叫此方法。 從事件處理常式呼叫 **URL** 可能會產生非預期的結果。

## <a name="examples"></a>範例

下列範例可讓使用者在文字方塊中輸入檔案路徑，以指定媒體檔案。 按一下按鈕時，[URL] 屬性會設定為指定的檔案，並播放該檔案。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


```CSharp
private void openMedia_Click(object sender, System.EventArgs e)
{
    // Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text;

    // Play the media file. 
    player.Ctlcontrols.play();
}
```


```VB

Public Sub openMedia_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles openMedia.Click

    &#39; Set the URL property to the file path obtained from the text box. 
    player.URL = inputURL.Text

    &#39; Play the media file. 
    player.Ctlcontrols.play()

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

 

 





