---
description: SetSourceRect 方法會將目前的來源影片矩形設定 (純虛擬) 。 這是來源矩形變更時所呼叫的內部成員函式。
ms.assetid: 13bb594b-b154-40a2-ad00-f1e86781074d
title: 'CBaseControlVideo. SetSourceRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.SetSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e3be6cc3819e1452fd196d4906377204a6e90bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996462"
---
# <a name="cbasecontrolvideosetsourcerect-method"></a>CBaseControlVideo. SetSourceRect 方法

`SetSourceRect`方法會將目前的來源影片矩形設定 (純虛擬) 。 這是來源矩形變更時所呼叫的內部成員函式。

## <a name="syntax"></a>語法


```C++
virtual HRESULT SetSourceRect(
   RECT *pSourceRect
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*pSourceRect* 
</dt> <dd>

來源矩形的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

衍生類別應該覆寫這個成員函式，以得知來源矩形何時變更。 它是從下列成員函式所呼叫。

-   [**CBaseControlVideo::SetSourcePosition**](cbasecontrolvideo-setsourceposition.md)
-   [**CBaseControlVideo：:p 的 \_ SourceLeft**](cbasecontrolvideo-put-sourceleft.md)
-   [**CBaseControlVideo：:p 的 \_ SourceWidth**](cbasecontrolvideo-put-sourcewidth.md)
-   [**CBaseControlVideo：:p 的 \_ SourceTop**](cbasecontrolvideo-put-sourcetop.md)
-   [**CBaseControlVideo：:p 的 \_ SourceHeight**](cbasecontrolvideo-put-sourceheight.md)

下列範例示範如何在衍生類別中執行此函式。


```C++
HRESULT CVideoText::SetSourceRect(RECT *pSourceRect)
{
    m_pRenderer->m_DrawImage.SetSourceRect(pSourceRect);
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

 

 




