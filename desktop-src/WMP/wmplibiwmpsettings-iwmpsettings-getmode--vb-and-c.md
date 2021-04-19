---
title: IWMPSettings getMode 方法
description: GetMode 方法會傳回值，指出迴圈模式或隨機播放模式是否為使用中狀態。
ms.assetid: a2e4bf74-017f-4c54-a3a1-a03b75a87a59
keywords:
- getMode 方法 Windows Media Player
- getMode 方法 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，getMode 方法
topic_type:
- apiref
api_name:
- IWMPSettings.getMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 229cacf629410f958a062615cd5feb22be2ab0d0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994053"
---
# <a name="iwmpsettingsgetmode-method"></a>IWMPSettings：： getMode 方法

**GetMode** 方法會傳回值，指出迴圈模式或隨機播放模式是否為使用中狀態。

## <a name="syntax"></a>語法


```CSharp
public System.Boolean getMode(
  System.String bstrMode
);
```


```VB

Public Function getMode( _
  ByVal bstrMode As System.String _
) As System.Boolean
Implements IWMPSettings.getMode
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrMode* \[在\]
</dt> <dd>

**System.string** ，這是下列其中一個值。



| 值      | 描述                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autoRewind | 播放結束之後，會從頭開始重新開機追蹤。                                |
| loop       | 追蹤順序會自行重複。                                                           |
| showFrame  | 未播放時，會顯示最接近的主要畫面格。 此模式與音訊播放軌無關。 |
| 隨機播放    | 曲目會以隨機順序播放。                                                               |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

System.string **值，** 指出指定的模式是否為使用中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| 版本<br/>   | Windows Media Player 9 系列或更新版本<br/>                                                                      |
| 命名空間<br/> | **WMPLib**<br/>                                                                                                  |
| 組件<br/>  | <dl> <dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMPSettings 介面 (VB 和 c # )**](iwmpsettings--vb-and-c.md)
</dt> <dt>

[**IWMPSettings. setMode (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-setmode--vb-and-c.md)
</dt> </dl>

 

 





