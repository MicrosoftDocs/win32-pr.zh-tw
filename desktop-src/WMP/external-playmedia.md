---
title: PlayMedia 方法
description: 本頁面記載 Windows Media Player 9 系列 SDK 和 Windows Media Player 10 SDK 的功能。 它可能在後續版本中無法使用。
ms.assetid: 48071318-e853-4139-8fe4-17d1cdbef8f5
keywords:
- playMedia 方法 Windows Media Player
- playMedia 方法 Windows Media Player、External 類別
- External class Windows Media Player，playMedia 方法
topic_type:
- apiref
api_name:
- External.playMedia
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2cf0330e7e68d8b4e3747c019e0841f872d279c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984286"
---
# <a name="externalplaymedia-method"></a>PlayMedia 方法

本頁面記載 Windows Media Player 9 系列 SDK 和 Windows Media Player 10 SDK 的功能。 它可能在後續版本中無法使用。

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**PlayMedia** 方法會指定要播放之數位媒體專案的 URL。

## <a name="syntax"></a>語法


```JScript
External.playMedia(
  URL
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*URL* \[在\]
</dt> <dd>

**字串** ，指定要播放之數位媒體專案的 URL。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

此方法僅適用于 **指南** 功能中裝載的網頁。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player  9  系列或更新的版本。<br/>                                 |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型2線上商店的外部物件**](external-object-for-type-2-online-stores.md)
</dt> </dl>

 

 





