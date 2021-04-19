---
title: DownloadCollection 專案方法
description: 請注意，本節將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Item 方法會抓取暫止的下載物件。
ms.assetid: a79db9db-e80c-48db-aee6-9bd8f77a7dff
keywords:
- item 方法 Windows Media Player
- item 方法 Windows Media Player，DownloadCollection 類別
- DownloadCollection 類別 Windows Media Player，item 方法
topic_type:
- apiref
api_name:
- DownloadCollection.item
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d57db60a776c71d9ff16eceb1584c79a125bbf46
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999461"
---
# <a name="downloadcollectionitem-method"></a>DownloadCollection 專案方法

> [!Note]  
> 本章節描述專為線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**Item** 方法會抓取暫止的下載物件。

## <a name="syntax"></a>語法


```JScript
retVal = DownloadCollection.item(
  itemId
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*itemId* \[在\]
</dt> <dd>

**(** **long**) 指定要取出的 **DownloadItem** 索引。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回 **DownloadItem** 物件。

## <a name="remarks"></a>備註

*ItemID* 值以零為基底。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 9 系列或更新版本<br/>                                  |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**DownloadCollection 物件**](downloadcollection-object.md)
</dt> <dt>

[**DownloadItem 物件**](downloaditem-object.md)
</dt> </dl>

 

 





