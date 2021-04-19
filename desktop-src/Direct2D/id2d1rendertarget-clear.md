---
title: ID2D1RenderTarget Clear 方法
description: 將繪圖區域清除為指定的色彩。
ms.assetid: 3bfec923-17fc-479a-a760-9baab2ff3a56
keywords:
- 清除方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
api_name: ''
ms.openlocfilehash: 346e44e3ce0b59e40577d3207f45faafdc33b367
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981375"
---
# <a name="id2d1rendertargetclear-methods"></a><span data-ttu-id="26275-104">ID2D1RenderTarget：： Clear 方法</span><span class="sxs-lookup"><span data-stu-id="26275-104">ID2D1RenderTarget::Clear methods</span></span>

<span data-ttu-id="26275-105">將繪圖區域清除為指定的色彩。</span><span class="sxs-lookup"><span data-stu-id="26275-105">Clears the drawing area to the specified color.</span></span>

### <a name="overload-list"></a><span data-ttu-id="26275-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="26275-106">Overload list</span></span>



| <span data-ttu-id="26275-107">方法</span><span class="sxs-lookup"><span data-stu-id="26275-107">Method</span></span>                                                                 | <span data-ttu-id="26275-108">描述</span><span class="sxs-lookup"><span data-stu-id="26275-108">Description</span></span>                                                 |
|:-----------------------------------------------------------------------|:------------------------------------------------------------|
| <span data-ttu-id="26275-109">[**清除 (D2D1 \_ COLOR \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f))</span><span class="sxs-lookup"><span data-stu-id="26275-109">[**Clear(D2D1\_COLOR\_F\*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f))</span></span> | <span data-ttu-id="26275-110">將繪圖區域清除為指定的色彩。</span><span class="sxs-lookup"><span data-stu-id="26275-110">Clears the drawing area to the specified color.</span></span> <br/> |
| <span data-ttu-id="26275-111">[**清除 (D2D1 \_ COLOR \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))</span><span class="sxs-lookup"><span data-stu-id="26275-111">[**Clear(D2D1\_COLOR\_F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))</span></span>  | <span data-ttu-id="26275-112">將繪圖區域清除為指定的色彩。</span><span class="sxs-lookup"><span data-stu-id="26275-112">Clears the drawing area to the specified color.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="26275-113">備註</span><span class="sxs-lookup"><span data-stu-id="26275-113">Remarks</span></span>

<span data-ttu-id="26275-114">Direct2D 會將 *clearColor* 轉譯為直接 Alpha (不會) 預乘。</span><span class="sxs-lookup"><span data-stu-id="26275-114">Direct2D interprets the *clearColor* as straight alpha (not premultiplied).</span></span> <span data-ttu-id="26275-115">如果轉譯目標的 Alpha 模式是 [**D2D1 \_ Alpha \_ 模式 \_ 略**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)過，則會忽略 *clearColor* 的 Alpha 通道，並以 1.0 f 取代 (完全不透明的) 。</span><span class="sxs-lookup"><span data-stu-id="26275-115">If the render target's alpha mode is [**D2D1\_ALPHA\_MODE\_IGNORE**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode), the alpha channel of *clearColor* is ignored and replaced with 1.0f (fully opaque).</span></span>

<span data-ttu-id="26275-116">如果轉譯目標有 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))) 所指定的作用中剪輯 (，則 clear 命令只會套用至裁剪區域內的區域。</span><span class="sxs-lookup"><span data-stu-id="26275-116">If the render target has an active clip (specified by [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))), the clear command is only applied to the area within the clip region.</span></span>

## <a name="examples"></a><span data-ttu-id="26275-117">範例</span><span class="sxs-lookup"><span data-stu-id="26275-117">Examples</span></span>

<span data-ttu-id="26275-118">下列範例會使用 **Clear** 方法來建立白色背景，然後再呈現其他內容。</span><span class="sxs-lookup"><span data-stu-id="26275-118">The following example uses the **Clear** method to create a white background before rendering other content.</span></span>


```C++
//  Called whenever the application needs to display the client
//  window. This method writes "Hello, World"
//
//  Note that this function will automatically discard device-specific
//  resources if the Direct3D device disappears during function
//  invocation, and will recreate the resources the next time it's
//  invoked.
//
HRESULT DemoApp::OnRender()
{
    HRESULT hr;

    hr = CreateDeviceResources();

    if (SUCCEEDED(hr))
    {
        static const WCHAR sc_helloWorld[] = L"Hello, World!";

        // Retrieve the size of the render target.
        D2D1_SIZE_F renderTargetSize = m_pRenderTarget->GetSize();

        m_pRenderTarget->BeginDraw();

        m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

        m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

        m_pRenderTarget->DrawText(
            sc_helloWorld,
            ARRAYSIZE(sc_helloWorld) - 1,
            m_pTextFormat,
            D2D1::RectF(0, 0, renderTargetSize.width, renderTargetSize.height),
            m_pBlackBrush
            );

        hr = m_pRenderTarget->EndDraw();

        if (hr == D2DERR_RECREATE_TARGET)
        {
            hr = S_OK;
            DiscardDeviceResources();
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="26275-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="26275-119">Requirements</span></span>



| <span data-ttu-id="26275-120">需求</span><span class="sxs-lookup"><span data-stu-id="26275-120">Requirement</span></span> | <span data-ttu-id="26275-121">值</span><span class="sxs-lookup"><span data-stu-id="26275-121">Value</span></span> |
|--------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="26275-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="26275-122">Library</span></span><br/> | <dl> <span data-ttu-id="26275-123"><dt>D2d1 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="26275-123"><dt>D2d1.lib</dt></span></span> </dl> |
| <span data-ttu-id="26275-124">DLL</span><span class="sxs-lookup"><span data-stu-id="26275-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="26275-125"><dt>D2d1.dll</dt></span><span class="sxs-lookup"><span data-stu-id="26275-125"><dt>D2d1.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="26275-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="26275-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="26275-127">**ID2D1RenderTarget**</span><span class="sxs-lookup"><span data-stu-id="26275-127">**ID2D1RenderTarget**</span></span>](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

