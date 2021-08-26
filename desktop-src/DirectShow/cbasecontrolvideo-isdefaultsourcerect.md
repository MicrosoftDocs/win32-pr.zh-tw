---
description: IsDefaultSourceRect 方法會判斷轉譯器是否使用預設的來源矩形 (純虛擬) 。
ms.assetid: 08c7a365-585c-47e6-9c26-6aa1fa3625e7
title: 'CBaseControlVideo. IsDefaultSourceRect 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.IsDefaultSourceRect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d8cdce3f01bc3a0ed28ee9ce758ef6cb136676a9bd8b4b314547103045e5b284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056868"
---
# <a name="cbasecontrolvideoisdefaultsourcerect-method"></a>CBaseControlVideo. IsDefaultSourceRect 方法

`IsDefaultSourceRect`方法會判斷轉譯器是否使用預設的來源矩形 (純虛擬) 。

## <a name="syntax"></a>語法


```C++
virtual HRESULT IsDefaultSourceRect() = 0;
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

如果轉譯器 \_ 使用預設來源，則傳回 [確定]，否則傳回 \_ FALSE。

## <a name="remarks"></a>備註

此成員函式必須在衍生類別中執行。 它是由 [**CBaseControlVideo：： IsUsingDefaultSource**](cbasecontrolvideo-isusingdefaultsource.md) 成員函式所呼叫。

下列範例示範如何在衍生類別中執行此函式。


```C++
// Return S_OK if using the default source; otherwise, S_FALSE.
HRESULT CVideoText::IsDefaultSourceRect()
{
    RECT SourceRect;

    VIDEOINFO *pVideoInfo = (VIDEOINFO *) m_pRenderer->m_mtIn.Format();
    BITMAPINFOHEADER *pHeader = HEADER(pVideoInfo);
    m_pRenderer->m_DrawImage.GetSourceRect(&SourceRect);

    // Check the coordinates that match the video dimensions.

    if (SourceRect.left != 0 || SourceRect.top != 0 ||
            SourceRect.right != pHeader->biWidth ||
                SourceRect.bottom != pHeader->biHeight) {
                    return S_FALSE;
    }
    return S_OK;
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

 

 




