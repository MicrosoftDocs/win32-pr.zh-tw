---
title: SetMode 方法
description: SetMode 方法會將各種模式設定為作用中或非作用中。
ms.assetid: 9ab88aeb-53f6-4798-9299-14961e373ca6
keywords:
- setMode 方法 Windows Media Player
- setMode 方法 Windows Media Player，Settings 類別
- Settings 類別 Windows Media Player，setMode 方法
topic_type:
- apiref
api_name:
- Settings.setMode
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf5740bf5638ce34e161414ac96eaa0fc80fcdb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994261"
---
# <a name="settingssetmode-method"></a>SetMode 方法

**SetMode** 方法會將各種模式設定為作用中或非作用中。

## <a name="syntax"></a>語法


```JScript
Settings.setMode(
  modeName,
  state
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*modeName* \[在\]
</dt> <dd>

**字串** ，指定要變更的模式名稱，其中包含下列其中一個值。



| String     | Description                                                                                                                                                       |
|------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| autoRewind | 模式，指出播放到結尾之後，是否要將曲目倒轉到開頭。 預設狀態為 true。                                                  |
| loop       | 指出曲目順序是否會自行重複的模式。 預設狀態為 false。                                                                            |
| showFrame  | 指出最近的影片主要畫面格是否在未播放時顯示于目前位置的模式。 預設狀態為 false。 對音軌沒有任何影響。 |
| 隨機播放    | 指出是否以隨機順序播放曲目的模式。 預設狀態為 false。                                                                            |



 

</dd> <dt>

*狀態* \[在\]
</dt> <dd>

**布林值** ，指定新指定的模式是否為使用中。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

當 showFrame 模式為使用中時，播放程式必須存取曲目內容才能取出影片畫面。 基於頻寬考慮，播放非區域內容時請小心使用這個模式。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 版本<br/> | 針對迴圈和隨機模式，Windows Media Player 7.0 版或更新版本。 適用于 autoRewind 和 showFrame 模式，Windows Media Player 9 系列或更新版本。<br/> |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl>                                                                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Settings 物件**](settings-object.md)
</dt> <dt>

[**設定. getMode**](settings-getmode.md)
</dt> </dl>

 

 





