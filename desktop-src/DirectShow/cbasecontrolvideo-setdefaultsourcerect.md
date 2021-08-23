---
description: SetDefaultSourceRect 方法會將預設的來源影片矩形設定 (純虛擬) 。 這是內部成員函式，會在來源矩形重設時呼叫。
ms.assetid: d0dae0a9-8763-485e-b9d3-80076a3f2f35
title: 'CBaseControlVideo. SetDefaultSourceRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae7f2e88e170b0c21187b2615029fcb4ed2bed4717af09b60eb4309aee2bea0f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432608"
---
# <a name="cbasecontrolvideosetdefaultsourcerect-method"></a>CBaseControlVideo. SetDefaultSourceRect 方法

`SetDefaultSourceRect`方法會將預設的來源影片矩形設定 (純虛擬) 。 這是內部成員函式，會在來源矩形重設時呼叫。

## <a name="syntax"></a>語法


```C++
virtual HRESULT SetDefaultSourceRect() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

衍生類別應該覆寫此值，以重設來源矩形。 它是從 [**CBaseControlVideo：： SetDefaultSourcePosition**](cbasecontrolvideo-setdefaultsourceposition.md)呼叫。

下列範例示範如何在衍生類別中執行此函式。


```C++
// This is called when you reset the default source rectangle.
HRESULT CVideoText::SetDefaultSourceRect()
{
    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    RECT SourceRect = {0,0,pHeader->biWidth,pHeader->biHeight};
    m_pRenderer->m_DrawImage.SetSourceRect(&SourceRect);
    return NOERROR;
}
```



在此範例中，CVideoText 是衍生自 [**CBaseControlVideo**](cbasecontrolvideo.md)的類別，m \_ pRenderer 會保存衍生自 [**CBaseVideoRenderer**](cbasevideorenderer.md)之類別的物件，而在 \_ 衍生類別中定義的 m DrawImage 資料成員則會保留 [**CDrawImage**](cdrawimage.md) 物件。 M \_ mtIn 資料成員（也定義于衍生類別中）會保存具有輸入釘選媒體類型的 [**CMediaType**](cmediatype.md) 物件。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




