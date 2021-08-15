---
title: 播放清單。 setColumnResizeMode
description: SetColumnResizeMode 方法會指定索引資料行本身的大小。
ms.assetid: 84ca0e60-ca24-4058-ae08-5b9cf3d7c38f
keywords:
- 播放清單. setColumnResizeMode Windows Media Player
topic_type:
- apiref
api_name:
- PLAYLIST.setColumnResizeMode
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 72f356108ff016c404468a9b152b4adac247cd72ee089a9e82ea3206c4c2ffea
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118335800"
---
# <a name="playlistsetcolumnresizemode"></a>播放清單。 setColumnResizeMode

**SetColumnResizeMode** 方法會指定索引資料行本身的大小。

``` syntax
        elementID.setColumnResizeMode(column, mode)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="column"></span><span id="COLUMN"></span>*列*
</dt> <dd>

**Number** (**long**) 指出要變更之資料行的索引。

</dd> <dt>

<span id="mode"></span><span id="MODE"></span>*模式*
</dt> <dd>

表示調整大小模式的 **字串**。 包含下列其中一個值。



| 值          | 描述                                                                                                    |
|----------------|----------------------------------------------------------------------------------------------------------------|
| AutosizeHeader | 資料行調整大小以容納資料行和標頭中的所有資料。                                  |
| AutosizeData   | 資料行調整大小以容納資料行中的所有資料。                                                 |
| 固定式          | 此資料行是固定的大小。                                                                                    |
| 延伸      | 當所有其他資料行調整大小之後，資料行調整大小以使用 **播放清單** 元素中的剩餘空間。 |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------|
| 版本<br/> | Windows Media Player 7.0 版或更新版本<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**播放清單元素**](playlist-element.md)
</dt> </dl>

 

 





