---
title: External. 購買方法
description: 請注意，本主題將說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。 購買方法會起始一組媒體專案的購買。
ms.assetid: 78496de6-214e-4712-8fbc-11e002adce88
keywords:
- 購買方法 Windows Media Player
- 購買方法 Windows Media Player，外部類別
- 外部類別 Windows Media Player，購買方法
topic_type:
- apiref
api_name:
- External.buy
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5ffee188372e33ed4ceadf1bb1ee2ea0f986207
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978743"
---
# <a name="externalbuy-method"></a>External. 購買方法

> [!Note]  
> 本主題說明針對線上商店使用而設計的功能。 不支援在線上商店的內容之外使用這項功能。

 

**購買** 方法會起始一組媒體專案的購買。

## <a name="syntax"></a>語法


```JScript
External.buy(
  ViewType,
  ViewIDs
)
```



## <a name="parameters"></a>參數

<dl> <dt>

*ViewType* \[在\]
</dt> <dd>

**字串** ，指定要購買的專案類型。 呼叫端必須將此參數設定為下列其中一個連結 [庫位置常數](library-location-constants.md)：

CPListID

CPTrackID

CPAlbumID

</dd> <dt>

*Viewid* \[在\]
</dt> <dd>

**字串** ，包含要購買之專案的識別碼（以分號分隔）。

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
</dt> <dt>

[**External. 下載**](external-download.md)
</dt> <dt>

[**IWMPContentPartner：：購買**](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)
</dt> <dt>

[**購買媒體內容**](purchasing-media-content.md)
</dt> </dl>

 

 





