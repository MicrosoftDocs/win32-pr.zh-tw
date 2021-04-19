---
description: GetDIBData 方法會抓取此物件正在管理之 GDI 裝置獨立點陣圖 (DIB) 的相關資訊。
ms.assetid: ec337336-69ec-47ff-a522-42c0388f9bc0
title: 'CImageSample. GetDIBData 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageSample.GetDIBData
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd198152e7c0042a6d48cf942a48745540960d3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977422"
---
# <a name="cimagesamplegetdibdata-method"></a>CImageSample. GetDIBData 方法

`GetDIBData`方法會抓取此物件正在管理之 GDI 裝置獨立點陣圖 (DIB) 的相關資訊。

## <a name="syntax"></a>語法


```C++
DIBDATA* GetDIBData();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 [**DIBDATA**](dibdata.md) 結構的指標。

## <a name="remarks"></a>備註

呼叫這個方法之前，呼叫端必須初始化 **DIBDATA** 結構。檢查 **CImageSample：： m \_ bInit** 的值。 若要初始化結構，請呼叫 [**CImageSample：： SetDIBData**](cimagesample-setdibdata.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageSample 類別**](cimagesample.md)
</dt> </dl>

 

 




