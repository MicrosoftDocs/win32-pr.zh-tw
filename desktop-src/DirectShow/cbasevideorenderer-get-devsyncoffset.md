---
description: Get \_ DevSyncOffset 方法會從開始串流之後的所有畫面格，取得時間（以毫秒為單位）之間的標準差（以毫秒為單位）。
ms.assetid: 86f60064-f913-4377-bad0-148a213171fc
title: 'CBaseVideoRenderer.get_DevSyncOffset 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_DevSyncOffset
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9926e809901f7290738e2e2cf3d094e54e068580
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989751"
---
# <a name="cbasevideorendererget_devsyncoffset-method"></a>CBaseVideoRenderer. 取得 \_ DevSyncOffset 方法

方法會從 `get_DevSyncOffset` 開始串流之後的所有框架，取得時間（以毫秒為單位）之間的標準差（以毫秒為單位）。

## <a name="syntax"></a>語法


```C++
HRESULT get_DevSyncOffset(
   int *piDev
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*piDev* 
</dt> <dd>

先前所述時間的標準差指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會實 [**IQualProp：： get \_ DevSyncOffset**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_devsyncoffset) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




