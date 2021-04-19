---
description: SetDrawCoNtext 方法會設定用於繪製的裝置內容。
ms.assetid: dd752970-99b3-42bb-95a5-8103cab276da
title: 'CDrawImage. SetDrawCoNtext 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDrawImage.SetDrawContext
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1d329dd45d1a02afd2cbd0daf8d0da8390b0b395
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982990"
---
# <a name="cdrawimagesetdrawcontext-method"></a>CDrawImage. SetDrawCoNtext 方法

`SetDrawContext`方法會設定用於繪製的裝置內容。

## <a name="syntax"></a>語法


```C++
void SetDrawContext();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法不會傳回值。

## <a name="remarks"></a>備註

這個方法會從擁有的 [**CBaseWindow**](cbasewindow.md) 物件抓取視窗和記憶體裝置內容。 請在初始化視窗之後，但在開始繪製之前呼叫這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CDrawImage 類別**](cdrawimage.md)
</dt> </dl>

 

 




