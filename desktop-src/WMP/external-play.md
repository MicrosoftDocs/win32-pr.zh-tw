---
title: External. play 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 Play 方法會指示 Windows Media Player 播放一組媒體專案。
ms.assetid: 3e1f45db-9e7f-4a1b-aaa2-513a19c46f70
keywords:
- play 方法 Windows Media Player
- play 方法 Windows Media Player、External 類別
- 外部類別 Windows Media Player、play 方法
topic_type:
- apiref
api_name:
- External.play
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94cfa40d96bbc67c7d41eb1a1a0188be68ec154e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106992787"
---
# <a name="externalplay-method"></a>External. play 方法

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**Play** 方法會指示 Windows Media Player 播放一組媒體專案。

## <a name="syntax"></a>語法


```JScript
External.play(
  LibraryLocationType,
  LibraryLocationIDs
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*LibraryLocationType* \[在\]
</dt> <dd>

連結 [庫位置常數](library-location-constants.md) ，指定要播放之媒體專案的型別。 例如，CPAlbumID 指定要播放一或多個專輯。

</dd> <dt>

*LibraryLocationIDs* \[在\]
</dt> <dd>

**字串** ，包含要播放之媒體專案的識別碼（以分號分隔）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|------------------------------------------------------------------------------------|
| 版本<br/> | Windows Media Player 11。<br/>                                                |
| DLL<br/>     | <dl> <dt>Wmp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**類型1線上商店的外部物件**](external-object-for-type-1-online-stores.md)
</dt> </dl>

 

 





