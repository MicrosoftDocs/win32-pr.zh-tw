---
title: AddToBasket 方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 |AddToBasket 方法
ms.assetid: c0dc8cd7-b924-47b8-b36c-caff8f1f892f
keywords:
- addToBasket 方法 Windows Media Player
- addToBasket 方法 Windows Media Player、External 類別
- External class Windows Media Player，addToBasket 方法
topic_type:
- apiref
api_name:
- External.addToBasket
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2e2fab549dec9e24b0c5bbe61f5511e375c4c04
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984130"
---
# <a name="externaladdtobasket-method"></a>AddToBasket 方法

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**AddToBasket** 方法會將媒體專案新增至 [清單] 窗格 (也稱為 Windows Media Player 中的購物籃) 。

## <a name="syntax"></a>語法


```JScript
External.addToBasket(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*ViewType* \[在\]
</dt> <dd>

**字串** ，指定要加入至 [清單] 窗格的專案類型。 呼叫端必須將此參數設定為下列其中一個連結 [庫位置常數](library-location-constants.md)：

CPListID

CPTrackID

CPAlbumID

CPArtist

CPGenreID

CPAlbumSubGenreID

CPRadioID

</dd> <dt>

*Viewid* \[在\]
</dt> <dd>

**字串** ，包含要加入至清單窗格之專案的識別碼（以分號分隔）。

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

[**類型1線上商店的 ExternalObject**](external-object-for-type-1-online-stores.md)
</dt> <dt>

[**BasketTitle**](external-baskettitle.md)
</dt> </dl>

 

 





