---
description: 「取得 \_ 抖動」方法會將每個畫面格之間的標準差（以毫秒為單位），從串流開始的所有框架中取出。
ms.assetid: 629e725e-7dee-4824-8f79-cd3335f4901b
title: 'CBaseVideoRenderer.get_Jitter 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_Jitter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ef39cdb1b7a77dab22db9728268bf7b23b9fcefb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989750"
---
# <a name="cbasevideorendererget_jitter-method"></a>CBaseVideoRenderer。取得 \_ 抖動方法

此 `get_Jitter` 方法會在串流開始之後，從每個畫面格與所有畫面格之間的間隔中，取得時間的標準差（毫秒）。

## <a name="syntax"></a>語法


```C++
HRESULT get_Jitter(
   int *piJitter
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*piJitter* 
</dt> <dd>

幀出時間的標準差指標（以毫秒為單位）。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會實 [**IQualProp：： get \_ 抖動**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_jitter) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




