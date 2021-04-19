---
description: GetTargetRect 方法會捕獲目的地矩形。 這是內部 helper 成員函式。
ms.assetid: bf9d95c9-eee8-46b8-bdee-a7d16777ed83
title: 'CBaseControlVideo. GetTargetRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d59a12e134edf37c8ab0a63f46f77923b112605d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106982602"
---
# <a name="cbasecontrolvideogettargetrect-method"></a>CBaseControlVideo. GetTargetRect 方法

方法會抓取 `GetTargetRect` 目的地矩形。 這是內部 helper 成員函式。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetTargetRect(
   RECT *pTargetRect
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTargetRect* 
</dt> <dd>

目的地矩形的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

必須在衍生類別中覆寫這個成員函式，以傳回影片轉譯器所持有的目標矩形。 它會從下列 [**CBaseControlVideo**](cbasecontrolvideo.md) 成員函式中呼叫。

-   [**CBaseControlVideo::GetDestinationPosition**](cbasecontrolvideo-getdestinationposition.md)
-   [**CBaseControlVideo：:p 的 \_ DestinationLeft**](cbasecontrolvideo-put-destinationleft.md)
-   [**CBaseControlVideo：： get \_ DestinationLeft**](cbasecontrolvideo-get-destinationleft.md)
-   [**CBaseControlVideo：:p 的 \_ DestinationWidth**](cbasecontrolvideo-put-destinationwidth.md)
-   [**CBaseControlVideo：： get \_ DestinationWidth**](cbasecontrolvideo-get-destinationwidth.md)
-   [**CBaseControlVideo：:p 的 \_ DestinationTop**](cbasecontrolvideo-put-destinationtop.md)
-   [**CBaseControlVideo：： get \_ DestinationTop**](cbasecontrolvideo-get-destinationtop.md)
-   [**CBaseControlVideo：:p 的 \_ DestinationHeight**](cbasecontrolvideo-put-destinationheight.md)
-   [**CBaseControlVideo：： get \_ DestinationHeight**](cbasecontrolvideo-get-destinationheight.md)

下列範例示範如何在衍生類別中執行此函式。


```C++
// Return the current destination rectangle.
HRESULT CVideoText::GetTargetRect(RECT *pTargetRect)
{
    ASSERT(pTargetRect);
    m_pRenderer->m_DrawImage.GetTargetRect(pTargetRect);
    return NOERROR;
}
```



在此範例中，CVideoText 是衍生自 [**CBaseControlVideo**](cbasecontrolvideo.md)的類別，m \_ pRenderer 會保存衍生自 [**CBaseVideoRenderer**](cbasevideorenderer.md)之類別的物件，而在 \_ 衍生類別中定義的 m DrawImage 資料成員則會保留 [**CDrawImage**](cdrawimage.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




