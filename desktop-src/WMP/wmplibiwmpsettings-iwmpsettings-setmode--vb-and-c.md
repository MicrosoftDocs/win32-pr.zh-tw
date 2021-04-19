---
title: IWMPSettings setMode 方法
description: SetMode 方法會將迴圈模式或隨機模式設定為作用中或非作用中。
ms.assetid: e9d3765e-6edb-47a5-ac97-5e00b62498c2
keywords:
- setMode 方法 Windows Media Player
- setMode 方法 Windows Media Player，IWMPSettings 介面
- IWMPSettings 介面 Windows Media Player，setMode 方法
topic_type:
- apiref
api_name:
- IWMPSettings.setMode
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f8dffede5e634c5c4f726cff1631b79781ed5179
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989258"
---
# <a name="iwmpsettingssetmode-method"></a>IWMPSettings：： setMode 方法

**SetMode** 方法會將迴圈模式或隨機模式設定為作用中或非作用中。

## <a name="syntax"></a>語法


```CSharp
public void setMode(
  System.String bstrMode,
  System.Boolean varfMode
);
```


```VB

Public Sub setMode( _
  ByVal bstrMode As System.String, _
  ByVal varfMode As System.Boolean _
)
Implements IWMPSettings.setMode
```





## <a name="parameters"></a>參數

<dl> <dt>

*bstrMode* \[在\]
</dt> <dd>

**System.string** ，這是要變更的模式名稱，其中包含下列其中一個值。



| 值      | 描述                                                                                      |
|------------|--------------------------------------------------------------------------------------------------|
| autoRewind | 播放結束之後，會從頭開始重新開機追蹤。                                |
| loop       | 追蹤順序會自行重複。                                                           |
| showFrame  | 未播放時，會顯示最接近的主要畫面格。 此模式與音訊播放軌無關。 |
| 隨機播放    | 曲目會以隨機順序播放。                                                               |



 

</dd> <dt>

*varfMode* \[在\]
</dt> <dd>

System.string **值，** 指定新指定的模式是否為使用中。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當 showFrame 模式為使用中時，Windows Media Player 必須存取曲目內容才能取出影片畫面。 播放非本機的內容時，請謹慎使用這個模式。

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

[**IWMPSettings. getMode (VB 和 c # )**](wmplibiwmpsettings-iwmpsettings-getmode--vb-and-c.md)
</dt> </dl>

 

 





