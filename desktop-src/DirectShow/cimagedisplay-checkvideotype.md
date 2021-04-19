---
description: CheckVideoType 方法會檢查指定的 VIDEOINFO 格式是否與顯示格式相容。
ms.assetid: a8593c7d-bde0-4c44-b450-10c129dd0007
title: 'CImageDisplay. CheckVideoType 方法 (Winutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageDisplay.CheckVideoType
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7db198270804053993352c4969b924fa7edc891f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000931"
---
# <a name="cimagedisplaycheckvideotype-method"></a>CImageDisplay. CheckVideoType 方法

`CheckVideoType`方法會檢查指定的 [**VIDEOINFO**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfo)格式是否與顯示格式相容。

## <a name="syntax"></a>語法


```C++
HRESULT CheckVideoType(
   const VIDEOINFO *pInput
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInput* 
</dt> <dd>

**VIDEOINFO** 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

\_如果格式相容，則傳回 S OK，否則傳回 E \_ INVALIDARG。

## <a name="remarks"></a>備註

\_如果建議的型別可以在目前的顯示設定下輕鬆顯示，則這個方法會傳回 S OK。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Winutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CImageDisplay 類別**](cimagedisplay.md)
</dt> </dl>

 

 




