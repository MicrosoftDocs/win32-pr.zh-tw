---
title: AxWindowsMediaPlayer。 status 屬性
description: Status 屬性會取得值，指出 Windows Media Player 的狀態。
ms.assetid: fefed54d-1fae-4599-8efc-eb2efdbd8ebd
keywords:
- status 屬性 Windows Media Player
- status 屬性 Windows Media Player，AxWindowsMediaPlayer 類別
- AxWindowsMediaPlayer 類別 Windows Media Player，status 屬性
topic_type:
- apiref
api_name:
- AxWindowsMediaPlayer.status
api_location:
- AxInterop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ac46eeef411e1d728994d829d95727cdaf4020c2ef1b7511391b6ca0d2e31ff7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119864558"
---
# <a name="axwindowsmediaplayerstatus-property"></a>AxWindowsMediaPlayer。 status 屬性

Status 屬性會取得值，指出 Windows Media Player 的狀態。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```CSharp
public System.String status {get;}
```


```VB

Public ReadOnly Property status As System.String
```





## <a name="property-value"></a>屬性值

表示狀態的 System.string。

## <a name="remarks"></a>備註

這個屬性中包含的值隨時可能會變更，而且僅供顯示之用。

AxWindowsMediaPlayer。每當這個屬性變更值時，就會引發 **StatusChange** 事件。

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

[**AxWindowsMediaPlayer. StatusChange 事件 (VB 和 c # )**](axwmplib-axwindowsmediaplayer-statuschange.md)
</dt> </dl>

 

 





