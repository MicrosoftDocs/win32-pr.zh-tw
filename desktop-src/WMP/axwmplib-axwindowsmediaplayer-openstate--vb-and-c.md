---
title: AxWindowsMediaPlayer. openState 屬性
description: OpenState 屬性會取得指出內容來源狀態的列舉值。
ms.assetid: 7a76814a-649f-4516-a92a-5f536fb1b147
keywords:
- openState 屬性 Windows Media Player
- openState 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，openState 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.openState
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 919bf906ce67793c4cd26f32892eae8acf441295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977454"
---
# <a name="axwindowsmediaplayeropenstate-property"></a>AxWindowsMediaPlayer. openState 屬性

OpenState 屬性會取得指出內容來源狀態的列舉值。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public WMPOpenState openState {get;}
```


```VB

Public ReadOnly Property openState As WMPOpenState
```





## <a name="property-value"></a>屬性值

WMPLib. WMPOpenState 列舉值。

## <a name="remarks"></a>備註

Windows Media Player 狀態不保證會以任何特定順序發生。 此外，並非每個狀態都一定會在一連串的事件期間發生。 您不應該撰寫依賴狀態順序的程式碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|----------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                          |
| 命名空間<br/> | **AxWMPLib**<br/>                                                                                                    |
| 組件<br/>  | <dl> <dt>AxInterop.WMPLib.dll (AxInterop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AxWindowsMediaPlayer 物件 (VB 和 c # )**](axwindowsmediaplayer-object--vb-and-c.md)
</dt> <dt>

[**AxWindowsMediaPlayer. OpenStateChange 事件**](axwmplib-axwindowsmediaplayer-openstatechange.md)
</dt> <dt>

[**WMPLib.WMPOpenState**](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpopenstate)
</dt> </dl>

 

 





