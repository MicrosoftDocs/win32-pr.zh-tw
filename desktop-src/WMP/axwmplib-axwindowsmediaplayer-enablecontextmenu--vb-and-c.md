---
title: AxWindowsMediaPlayer. enableCoNtextMenu 屬性
description: EnableCoNtextMenu 屬性會取得或設定值，指出是否要啟用操作功能表，這會在按一下滑鼠右鍵時顯示。
ms.assetid: 6096cab7-c1fa-4b71-804b-e84facab2229
keywords:
- enableCoNtextMenu 屬性 Windows Media Player
- enableCoNtextMenu 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，enableCoNtextMenu 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.enableContextMenu
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5603762ec9823f7e9896c5c22c1dee33f2399bb02301921057f8502046bcc002
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118582337"
---
# <a name="axwindowsmediaplayerenablecontextmenu-property"></a>AxWindowsMediaPlayer. enableCoNtextMenu 屬性

EnableCoNtextMenu 屬性會取得或設定值，指出是否要啟用操作功能表，這會在按一下滑鼠右鍵時顯示。

## <a name="syntax"></a>Syntax


```CSharp
public System.Boolean enableContextMenu {get; set;}
```


```VB

Public Property enableContextMenu As System.Boolean
```





## <a name="property-value"></a>屬性值

指出是否要啟用內容功能表的 system.string 值。 預設值為 true。

## <a name="remarks"></a>備註

在全螢幕播放期間，Windows Media Player 會在 **enableCoNtextMenu** 等於 false 且 **uiMode** 等於 "none" 時隱藏滑鼠游標。

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

 

 





