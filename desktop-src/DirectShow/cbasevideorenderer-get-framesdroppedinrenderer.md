---
description: Get FramesDroppedInRenderer 方法會抓取轉譯器 \_ 捨棄的框架數目。
ms.assetid: d890f285-b3bb-426c-80f6-e273cf0cccbb
title: 'CBaseVideoRenderer.get_FramesDroppedInRenderer 方法 (Renbase) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.get_FramesDroppedInRenderer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21bd2e9c2f9edb50ca3800c95b59ba19fd91674d5ef343cf35842380ce617978
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016756"
---
# <a name="cbasevideorendererget_framesdroppedinrenderer-method"></a>CBaseVideoRenderer. 取得 \_ FramesDroppedInRenderer 方法

方法會抓取轉譯器 `get_FramesDroppedInRenderer` 捨棄的框架數目。

## <a name="syntax"></a>語法


```C++
HRESULT get_FramesDroppedInRenderer(
   int *pcFramesDropped
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pcFramesDropped* 
</dt> <dd>

已卸載的框架數目指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

此成員函式會實 [**IQualProp：： get \_ FramesDroppedInRenderer**](/previous-versions/windows/desktop/api/Amvideo/nf-amvideo-iqualprop-get_framesdroppedinrenderer) 方法。 這是屬性頁從排程器抓取資料的方式。 您也可以在不看到轉譯器的情況下，將框架卸載至上游。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Renbase (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseVideoRenderer 類別**](cbasevideorenderer.md)
</dt> </dl>

 

 




