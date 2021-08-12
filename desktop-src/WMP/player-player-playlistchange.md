---
title: PlaylistChange 事件
description: 當播放清單變更時，就會發生 PlaylistChange 事件。 |PlaylistChange 事件
ms.assetid: 09ab0560-e18d-4ee8-a649-2b2468b40c31
keywords:
- PlaylistChange 事件 Windows Media Player
- PlaylistChange 事件 Windows Media Player，Player 類別
- Player 類別 Windows Media Player，PlaylistChange 事件
topic_type:
- apiref
api_name:
- Player.PlaylistChange
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ff4c45449c8de2062aa53ce9bda89c8d634dd30bc1ac8c03f091e8b97e9ce60
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118572801"
---
# <a name="playerplaylistchange-event"></a>PlaylistChange 事件

當播放清單變更時，就會發生 **PlaylistChange** 事件。

## <a name="syntax"></a>語法


```JScript
Player.PlaylistChange(
  Playlist,
  change
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*播放 清單* 
</dt> <dd>

變更的 **播放清單** 物件。

</dd> <dt>

*change* 
</dt> <dd>

**Number** (**long**) 指出播放清單所發生的變更類型。 包含下列其中一個值。



| 數字 | 名稱          |
|--------|---------------|
| 0      | Unknown       |
| 1      | 清除         |
| 2      | InfoChange    |
| 3      | 移動          |
| 4      | 刪除        |
| 5      | 插入        |
| 6      | Append        |
| 7      | 不支援 |
| 8      | NameChange    |
| 9      | 不支援 |
| 10     | Sort          |



 

C 樣式的列舉常數可以藉由在名稱值前面加上 "wmplc" 來衍生。 例如，移動狀態的常數是 **wmplcMove**。

</dd> </dl>

## <a name="return-value"></a>傳回值

此事件不會傳回值。

## <a name="remarks"></a>備註

事件參數的值是由 Windows Media Player 指定，而且可以使用指定的參數名稱，存取或傳遞至匯入 JScript 檔案中的方法。 此參數名稱的類型必須完全如所示，包括大小寫。

**Windows Media Player 10** 行動裝置版：不支援這個事件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本。<br/>                              |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Player 物件**](player-object.md)
</dt> </dl>

 

 





