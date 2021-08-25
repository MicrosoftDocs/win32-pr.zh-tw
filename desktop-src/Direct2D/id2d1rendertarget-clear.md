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
ms.openlocfilehash: 4e4e0c9843752af0799901537c5ee6d682d895a5ada22843ad2c406e9bda32b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119928948"
---
# <a name="id2d1rendertargetclear-methods"></a>ID2D1RenderTarget：： Clear 方法

將繪圖區域清除為指定的色彩。

### <a name="overload-list"></a>多載清單



| 方法                                                                 | 描述                                                 |
|:-----------------------------------------------------------------------|:------------------------------------------------------------|
| [**清除 (D2D1 \_ COLOR \_ F \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f)) | 將繪圖區域清除為指定的色彩。 <br/> |
| [**清除 (D2D1 \_ COLOR \_ F&)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-clear(constd2d1_color_f_))  | 將繪圖區域清除為指定的色彩。 <br/> |



## <a name="remarks"></a>備註

Direct2D 會將 *clearColor* 轉譯為直接 Alpha (不會) 預乘。 如果轉譯目標的 Alpha 模式是 [**D2D1 \_ Alpha \_ 模式 \_ 略**](/windows/desktop/api/dcommon/ne-dcommon-d2d1_alpha_mode)過，則會忽略 *clearColor* 的 Alpha 通道，並以 1.0 f 取代 (完全不透明的) 。

如果轉譯目標有 [**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))) 所指定的作用中剪輯 (，則 clear 命令只會套用至裁剪區域內的區域。

## <a name="examples"></a>範例

下列範例會使用 **Clear** 方法來建立白色背景，然後再呈現其他內容。


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



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

 

