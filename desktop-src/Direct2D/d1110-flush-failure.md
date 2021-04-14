---
title: D1110 排清失敗
ms.assetid: 44f122b0-08e3-4f63-a575-0f3619144823
description: 呈現目標的 Flush 呼叫失敗
keywords:
- D1110 排清失敗 Direct2D
topic_type:
- apiref
api_name:
- D1110 Flush Failure
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 4821ba291f3adc8d22d1d1298a88c74b47dc648b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104382805"
---
# <a name="d1110-flush-failure"></a>D1110： Flush 失敗

轉譯目標失敗資源的 Flush 呼叫 \[  \] 。 標記 \[ *tag1*、 *tag2* \] 。

## <a name="placeholders"></a>預留位置

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*資源*
</dt> <dd>

呈現目標的位址。

</dd> <dt>

<span id="tag1"></span><span id="TAG1"></span>*tag1*
</dt> <dd>

第一個標記值。 如需詳細資訊，請參閱 [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) 。

</dd> <dt>

<span id="tag2"></span><span id="TAG2"></span>*tag2*
</dt> <dd>

第二個標記值。 如需詳細資訊，請參閱 [**SetTags**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-settags) 。

</dd> </dl> 

|             |         |
|-------------|---------|
| 錯誤層級 | 警告 |



 

## <a name="examples"></a>範例

**範例1：** 下列程式碼顯示繪製呼叫處於無效狀態。 若要避免出現警告訊息，請使用 [**SetAntialiasMode**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-setantialiasmode) \_ \_ \_ 在 [**FillOpacityMask**](id2d1rendertarget-fillopacitymask.md) 呼叫之前設定 D2D1 消除鋸齒模式反鋸齒。


```C++
       
        if(SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateBitmap(
                D2D1::SizeU(1,1),
                NULL,
                0,
                D2D1::BitmapProperties(D2D1::PixelFormat(
                    DXGI_FORMAT_A8_UNORM, 
                    D2D1_ALPHA_MODE_PREMULTIPLIED
                    )),
                &m_pBitmap
                );                    
        }


        m_pRenderTarget->FillOpacityMask(
            m_pBitmapMask,
            m_pFernBitmapBrush,
            D2D1_OPACITY_MASK_CONTENT_GRAPHICS,
            &rcBrushRect
            );

        hr = m_pRenderTarget->Flush();

        hr = m_pRenderTarget->EndDraw();
```





此範例會產生下列 debug 訊息：

``` syntax
D2D DEBUG WARNING - Flush call on render target failed [88990001]. Tags [0, 0].
```

**範例2：** 下列程式碼顯示在 [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)呼叫之後呼叫 [**Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 。


```C++
        // Calling Flush after EndDraw generates a
        // flush error message from the debug layer.
       hr = m_pRenderTarget->EndDraw();       
       
       hr = m_pRenderTarget->Flush();
```



此範例會產生下列 debug 訊息：

``` syntax
DEBUG WARNING - A Flush call by a render target failed [88990001]. Tags [0, 0].
```

## <a name="possible-causes"></a>可能的原因

因為有兩個原因，所以 [**清除**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 呼叫可能會失敗。 它可能會因為在 [**BeginDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-begindraw) / [**EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw)呼叫之外呼叫方法而失敗，否則可能會失敗，因為其中一個轉譯目標作業產生的錯誤，自從上次排清呼叫或 **EndDraw** 呼叫之後已經處理過。 若要修正此問題，應用程式應判斷錯誤的原因，並採取適當的動作。

## <a name="fixes"></a>修正

[**清除**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush)呼叫可能會失敗的原因有很多。 應用程式應該判斷錯誤的原因，並採取適當的動作。

 

 