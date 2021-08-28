---
title: AxWindowsMediaPlayer. openPlayer 方法
description: openPlayer 方法會使用指定的 URL 開啟 Windows Media Player。 |AxWindowsMediaPlayer. openPlayer 方法
ms.assetid: 9a9d8200-f427-42ff-b49f-d973cf86014f
keywords:
- openPlayer 方法 Windows Media Player
- openPlayer 方法 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，openPlayer 方法
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openPlayer
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c9a2ae5660969e78aeb165c5f9fd9420ea04c79a6aeec9a57c4627cd61d32ef8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119764708"
---
# <a name="axwindowsmediaplayeropenplayer-method"></a>AxWindowsMediaPlayer. openPlayer 方法

**openPlayer** 方法會使用指定的 URL 開啟 Windows Media Player。

## <a name="syntax"></a>語法


```CSharp
public void openPlayer(
  System.String bstrURL
);
```


```VB

Public Sub openPlayer( _
  ByVal bstrURL As System.String _
)
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrURL* 
</dt> <dd>

**System.string** ，此為要播放之媒體專案的 URL。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會啟動 Windows Media Player，並將指定的 URL 設定為目前的媒體專案。 如果播放程式之前是在面板模式中關閉，則會使用使用者最後選擇的面板來開啟。 否則，播放會以完整模式開啟。

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

 

 





