---
title: GetMode 方法
description: GetMode 方法會判斷迴圈模式或隨機播放模式是否為使用中狀態。
ms.assetid: 41c3725f-ae8f-4b45-856a-b7245c9ad2b3
keywords:
- getMode 方法 Windows Media Player
- getMode 方法 Windows Media Player，Settings 類別
- Settings 類別 Windows Media Player，getMode 方法
topic_type:
- apiref
api_name:
- Settings.getMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5fc3e82091200d05bb173c71f2c0e5a7d213b80
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976045"
---
# <a name="settingsgetmode-method"></a>GetMode 方法

**GetMode** 方法會判斷迴圈模式或隨機播放模式是否為使用中狀態。

## <a name="syntax"></a>語法


```JScript
bRetVal = Settings.getMode(
  modeName
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*modeName* \[在\]
</dt> <dd>

**字串** ，指定有問題的模式名稱，其中包含下列其中一個值。



| String     | Description                                                                                                              |
|------------|--------------------------------------------------------------------------------------------------------------------------|
| autoRewind | 播放至結尾之後，會在一開始重新開機追蹤。                                                          |
| loop       | 追蹤順序會自行重複。                                                                                   |
| showFrame  | 未播放時，最接近的主要畫面格會顯示在目前的位置。 此模式與音訊播放軌無關。 |
| 隨機播放    | 曲目會以隨機順序播放。                                                                                       |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **布林** 值，指出指定的模式是否為使用中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | 針對迴圈和隨機模式，Windows Media Player 7.0 版或更新版本。 適用于 autoRewind 和 showFrame 模式，Windows Media Player 9 系列或更新版本。<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Settings 物件**](settings-object.md)
</dt> <dt>

[**設定. setMode**](settings-setmode.md)
</dt> </dl>

 

 





