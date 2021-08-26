---
description: Get \_ BitErrorRate 方法會捕獲影片的近似位錯誤率。
ms.assetid: 4078611c-6e09-47c8-8e1c-f33bc6ddca79
title: 'CBaseControlVideo.get_BitErrorRate 方法 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.get_BitErrorRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2602d203ca5a418dcc889d26932cd28be78d984390e71cff996e6fd3938030a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120057288"
---
# <a name="cbasecontrolvideoget_biterrorrate-method"></a>CBaseControlVideo. 取得 \_ BitErrorRate 方法

方法會抓取 `get_BitErrorRate` 影片的近似位錯誤率。

## <a name="syntax"></a>語法


```C++
HRESULT get_BitErrorRate(
   long *pBitErrorRate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBitErrorRate* 
</dt> <dd>

位錯誤率的指標 (大約這個多個位) 的一個錯誤。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回 >AAD-USERREADUSINGALTERNATIVESECURITYID-NOERROR \_ ，如果沒有足夠的可用記憶體，則傳回 E OUTOFMEMORY。

## <a name="remarks"></a>備註

此成員函式會實 [**IBasicVideo：： get \_ BitErrorRate**](/windows/desktop/api/Control/nf-control-ibasicvideo-get_biterrorrate) 方法。 它會呼叫純虛擬 [**CBaseControlVideo：： GetVideoFormat**](cbasecontrolvideo-getvideoformat.md) 方法，從衍生類別取出 [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) 結構。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




