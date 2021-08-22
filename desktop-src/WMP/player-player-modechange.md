---
title: ModeChange 事件
description: 當 Windows Media Player 的模式變更時，就會發生 ModeChange 事件。 |ModeChange 事件
ms.assetid: 45b57660-b186-4c0f-8735-61134058b8c9
keywords:
- ModeChange 事件 Windows Media Player
- ModeChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，ModeChange 事件
topic_type:
- apiref
api_name:
- Player.ModeChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e4a1102d49064c602d04915f77eda7ecfa1c748d4aea000cef1271679da1ec62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119054356"
---
# <a name="playermodechange-event"></a>ModeChange 事件

當 Windows Media Player 的模式變更時，就會發生 **ModeChange** 事件。

## <a name="syntax"></a>語法


```JScript
Player.ModeChange(
  ModeName,
  NewValue
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*ModeName* 
</dt> <dd>

表示已變更之模式的 **字串**。 包含下列其中一個值。



| 值   | 描述                                         |
|---------|-----------------------------------------------------|
| 隨機播放 | 曲目會以隨機順序播放。                  |
| loop    | 整個播放曲目順序都會重複播放。 |



 

</dd> <dt>

*NewValue* 
</dt> <dd>

**布林值** ，表示指定之模式的新狀態。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> <dt>

[**設定. getMode**](settings-getmode.md)
</dt> <dt>

[**設定. setMode**](settings-setmode.md)
</dt> </dl>

 

 





