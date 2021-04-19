---
title: DownloadCollection. removeItem 方法
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 RemoveItem 方法會從下載集合中移除下載專案。
ms.assetid: 0008752e-c81a-4f91-a582-9d6b46569479
keywords:
- removeItem 方法 Windows Media Player
- removeItem 方法 Windows Media Player，DownloadCollection 類別
- DownloadCollection 類別 Windows Media Player，removeItem 方法
topic_type:
- apiref
api_name:
- DownloadCollection.removeItem
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a1798665b79327b7956c1b78509b55cc6e6dd70c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991029"
---
# <a name="downloadcollectionremoveitem-method"></a>DownloadCollection. removeItem 方法

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**RemoveItem** 方法會從下載集合中移除下載專案。

## <a name="syntax"></a>語法


```JScript
DownloadCollection.removeItem(
  itemID
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*itemID* \[在\]
</dt> <dd>

**數值** (**long**) 指定要移除之 **DownloadItem** 的索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

如果 *itemID* 所表示的下載正在進行中，此方法會取消下載。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DownloadCollection 專案**](downloadcollection-item.md)
</dt> <dt>

[**DownloadCollection 物件**](downloadcollection-object.md)
</dt> </dl>

 

 





