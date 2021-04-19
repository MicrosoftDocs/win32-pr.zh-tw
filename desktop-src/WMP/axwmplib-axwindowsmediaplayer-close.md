---
title: AxWindowsMediaPlayer. close 方法
description: Close 方法會關閉目前的數位媒體檔案，在 Windows Media Player 中停止播放，並 Windows Media Player 資源釋出。
ms.assetid: 3e555086-c31c-42d7-b671-0fd824f66641
keywords:
- close 方法 Windows Media Player
- close 方法 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，close 方法
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.close
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1dc0c93e449e9ef1b00af7fb073068078f0fcc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981120"
---
# <a name="axwindowsmediaplayerclose-method"></a>AxWindowsMediaPlayer. close 方法

Close 方法會關閉目前的數位媒體檔案，在 Windows Media Player 中停止播放，並 Windows Media Player 資源釋出。

## <a name="syntax"></a>語法


```CSharp
public void close();
```


```VB

Public Sub close()
```





## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會關閉目前的數位媒體檔案，而不是 Windows Media Player 本身。

## <a name="examples"></a>範例

下列範例會建立一個按鈕，當按下此按鈕時，會在 Windows Media Player 中停止播放，並釋放使用中的資源。 AxWMPLib. AxWindowsMediaPlayer 物件是以名為 player 的變數來表示。


```CSharp
private void closeIt_Click(object sender, System.EventArgs e)
{
    // Close the Player. 
    player.close();
}
```


```VB

Public Sub closeIt_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles closeIt.Click

    &#39; Close the Player. 
    player.close()

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

 

 





