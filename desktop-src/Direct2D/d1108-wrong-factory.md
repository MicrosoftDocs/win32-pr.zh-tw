---
title: D1108 錯誤的 Factory
ms.assetid: eb851118-0541-4c9a-a22d-b98f041852bb
description: 資源是由 factory 1 所配置，並與 factory 2 搭配使用。
keywords:
- D1108 錯誤的 Factory Direct2D
topic_type:
- apiref
api_name:
- D1108 Wrong Factory
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 463909abeda1410804fa4b842dbdc829c3a74271
ms.sourcegitcommit: 4e94fc75fad7b2a0f3c92a26f97e89924e59b7a9
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/24/2021
ms.locfileid: "122786724"
---
# <a name="d1108-wrong-factory"></a>D1108：錯誤的 Factory

資源 \[ *資源* \] 是由 factory factory 1 所配置 \[  \] ，並與 factory \[ *factory 2* 搭配使用 \] 。

## <a name="placeholders"></a>預留位置

<dl> <dt>

<span id="resource"></span><span id="RESOURCE"></span>*資源*
</dt> <dd>

介面的位址。

</dd> <dt>

<span id="factory_1"></span><span id="FACTORY_1"></span>*factory 1*
</dt> <dd>

配置 *資源* 的 factory 位址。

</dd> <dt>

<span id="factory_2"></span><span id="FACTORY_2"></span>*factory 2*
</dt> <dd>

使用 *資源* 的 factory 位址。

</dd> </dl> 




 

## <a name="examples"></a>範例

下列範例會先建立兩個啟用 debug 的 [**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory) 物件;然後，它會從第一個 factory 建立幾何，並從第二個 factory 建立筆刷。 最後，它會呼叫 [**FillGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillgeometry)，並傳入幾何和筆刷。


```C++
        // If you set the options.debugLevel to D2D1_DEBUG_LEVEL_NONE,
        // the debug layer is not enabled.
#if defined(DEBUG) || defined(_DEBUG)
        D2D1_FACTORY_OPTIONS options;
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;

        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory
            );
#else
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            &m_pD2DFactory
            );
#endif


        // Domain violation. Create a second Direct2D factory.
        options.debugLevel = D2D1_DEBUG_LEVEL_INFORMATION;
        hr = D2D1CreateFactory(
            D2D1_FACTORY_TYPE_SINGLE_THREADED,
            options,
            &m_pD2DFactory1
            );

        // Create a geometry from the second factory.
        hr = m_pD2DFactory1->CreateRectangleGeometry(
            D2D1::RectF(100, 50, 400, 160),
            &m_pRectangleGeometry
            );
```





<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        // Create a render target from the first factory.
        hr = m_pD2DFactory->CreateHwndRenderTarget(
            D2D1::RenderTargetProperties(),
            D2D1::HwndRenderTargetProperties(m_hwnd, size),
            &m_pRenderTarget
            );</code></pre></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        if (SUCCEEDED(hr))
        {
            hr = m_pRenderTarget->CreateSolidColorBrush(
                D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
                &m_pBlackBrush
                );
        }</code></pre></td>
</tr>
</tbody>
</table>



<table>
<colgroup>
<col  />
</colgroup>
<thead>
<tr class="header">
<th>C++</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><pre><code>        m_pRenderTarget->FillGeometry(
            m_pRectangleGeometry,   //The rectangle geometry created from the second factory.
            m_pBlackBrush   //The black brush created from the first factory.
            );</code></pre></td>
</tr>
</tbody>
</table>



此範例會產生下列 debug 訊息：


```
 D2D DEBUG ERROR - The resource [003BD628] was allocated 
by factory [002ED698] and used with factory [002ED470].
```



## <a name="possible-causes"></a>可能的原因

不正確資源使用量。 由一個 factory 配置的資源與另一個 factory 一起使用。

 

 
