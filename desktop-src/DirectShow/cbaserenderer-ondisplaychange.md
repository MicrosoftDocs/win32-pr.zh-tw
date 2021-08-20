---
description: OnDisplayChange 方法會將 EC \_ 顯示 \_ 變更事件張貼至篩選圖形管理員。
ms.assetid: e4cdcdf2-7fc2-4893-9897-97bcf2c12610
title: 'CBaseRenderer. OnDisplayChange 方法 (Renbase .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnDisplayChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3f7fc5d733d90ab88f1114558947b6e72958c1d8b18d507ce612c1865fc400e3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016876"
---
# <a name="cbaserendererondisplaychange-method"></a>CBaseRenderer. OnDisplayChange 方法

方法會將 `OnDisplayChange` [**EC \_ 顯示 \_ 變更**](ec-display-changed.md) 事件張貼至篩選圖形管理員。

## <a name="syntax"></a>語法


```C++
BOOL OnDisplayChange();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果已張貼事件，則傳回 **TRUE** ，否則傳回 **FALSE** 。

## <a name="remarks"></a>備註

影片轉譯器應該呼叫這個方法以回應 WM \_ DISPLAYCHANGE 訊息。 如果輸入連接已連接，方法會將 EC \_ 顯示 \_ 已變更的事件傳送至篩選圖形管理員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseRenderer 類別**](cbaserenderer.md)
</dt> </dl>

 

 




