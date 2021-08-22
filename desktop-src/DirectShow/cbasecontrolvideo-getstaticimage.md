---
description: 衍生類別覆寫的純虛擬方法。
ms.assetid: 05c73f6b-27f4-4930-b4d5-1688b6bf1791
title: 'CBaseControlVideo. GetStaticImage 方法 (Ctlutil .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlVideo.GetStaticImage
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69496754c8a1f80be341c475f422229aba6108dbc0e73cd1db9506a301690ffa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660828"
---
# <a name="cbasecontrolvideogetstaticimage-method"></a>CBaseControlVideo. GetStaticImage 方法

衍生類別覆寫的純虛擬方法。

## <a name="syntax"></a>語法


```C++
virtual HRESULT GetStaticImage(
   long *pBufferSize,
   long *pDIBImage
) = 0;
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBufferSize* 
</dt> <dd>

輸出緩衝區大小的指標。

</dd> <dt>

*pDIBImage* 
</dt> <dd>

輸出緩衝區的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回 **HRESULT** 值。

## <a name="remarks"></a>備註

透過 [**IBasicVideo**](/windows/desktop/api/Control/nn-control-ibasicvideo) 介面，應用程式可以要求在記憶體緩衝區中取得目前映射的複本， (某些轉譯器可能會在 \_) 不支援時，將電子 >notimpl 傳給它。 衍生類別會決定如何取出影像。 當應用程式呼叫 **CBaseControlVideo：： GetStaticImage** 時，它會呼叫此純虛擬方法，衍生類別應該覆寫此方法來執行它。 這也是由 [**CBaseControlVideo：： GetCurrentImage**](cbasecontrolvideo-getcurrentimage.md) 成員函式所呼叫。

類別會提供 helper 成員函式 [**CBaseControlVideo：： CopyImage**](cbasecontrolvideo-copyimage.md)，其可提供包含影像的範例，而且成員函式會根據目前的來源矩形) ，將它的相關區段 (複製到應用程式所提供的輸出緩衝區。

下列範例示範如何在衍生類別中執行這個成員函式。 在此範例中，m \_ pRenderer 會保存衍生自 [**CBaseVideoRenderer**](cbasevideorenderer.md)之類別的物件。


```C++
// Return a copy of the current image in the video renderer
HRESULT CVideoText::GetStaticImage(long *pBufferSize,long *pDIBImage)
{
    // Get any sample the renderer may be holding.

    IMediaSample *pMediaSample = m_pRenderer->GetCurrentSample();
    if (pMediaSample == NULL) {
        return E_UNEXPECTED;
    }

    // Call the base class helper method to do the work.

    HRESULT hr = CopyImage(pMediaSample,       // Buffer containing image
                      &m_pRenderer->m_mtIn,    // Type representing bitmap
                      pBufferSize,             // Size of buffer for DIB
                     (BYTE*) pDIBImage);       // Data buffer for output

    pMediaSample->Release();
    return hr;
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CBaseControlVideo 類別**](cbasecontrolvideo.md)
</dt> </dl>

 

 




