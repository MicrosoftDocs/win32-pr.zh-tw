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
ms.openlocfilehash: ef81678fce8d349c7c047b0453cc480d8673f8f8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106985753"
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

 

 




