---
description: SetDefaultTargetRect 方法會將預設目標影片矩形設定 (純虛擬) 。 這是重設來源矩形時所呼叫的內部成員函式。
ms.assetid: bb7e32b2-f02c-465f-a8cb-6172d9724790
title: 'CBaseControlVideo. SetDefaultTargetRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultTargetRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1ab9cf310ffc35df07ecd9e332325bb5f20f3cb4884ee17e672294b89c5abc9d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120087478"
---
# <a name="cbasecontrolvideosetdefaulttargetrect-method"></a>CBaseControlVideo. SetDefaultTargetRect 方法

`SetDefaultTargetRect`方法會將預設目標的影片矩形設定 (純虛擬) 。 這是重設來源矩形時所呼叫的內部成員函式。

## <a name="syntax"></a>語法


```C++
virtual HRESULT SetDefaultTargetRect() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

衍生類別應該覆寫此值，以重設目的地影片矩形。 它是從 [**CBaseControlVideo：： SetDefaultDestinationPosition**](cbasecontrolvideo-setdefaultdestinationposition.md) 成員函式所呼叫。

下列範例示範如何在衍生類別中執行此函式。


```C++
// This is called when you reset the default target rectangle.
HRESULT CVideoText::SetDefaultTargetRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT TargetRect = {0,0,m_Size.cx,m_Size.cy};
    m_pRenderer->m_DrawImage.SetTargetRect(&TargetRect);
    return NOERROR;
}
```



在此範例中，CVideoText 是衍生自 [**CBaseControlVideo**](cbasecontrolvideo.md)的類別，m \_ pRenderer 會保存衍生自 [**CBaseVideoRenderer**](cbasevideorenderer.md)之類別的物件，而在 \_ 衍生類別中定義的 m DrawImage 資料成員則會保留 [**CDrawImage**](cdrawimage.md) 物件。 在 \_ 衍生類別中也定義的 m mtIn 資料成員，會保存具有輸入釘選媒體類型的 [**CMediaType**](cmediatype.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




