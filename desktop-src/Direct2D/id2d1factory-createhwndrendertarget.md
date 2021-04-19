---
title: 'ID2D1Factory CreateHwndRenderTarget 方法 (D2d1 .h) '
description: 建立呈現至視窗的 ID2D1HwndRenderTarget，轉譯目標。
ms.assetid: 3b55b1b0-a423-40dc-9581-c1fbe8134ca5
keywords:
- CreateHwndRenderTarget 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 984de8aea923c5b90d05fb79bc0c9edc319fb4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984129"
---
# <a name="id2d1factorycreatehwndrendertarget-methods"></a>ID2D1Factory：： CreateHwndRenderTarget 方法

建立呈現至視窗的 [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))，轉譯目標。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                                                                                                                                                              | 描述                                                                                                             |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**CreateHwndRenderTarget (D2D1 \_ 轉譯 \_ 目標 \_ 屬性 \* 、D2D1 \_ HWND \_ 轉譯 \_ 目標 \_ 屬性 \* 、ID2D1HwndRenderTarget \* \*)**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85)) | 建立呈現至視窗的 [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))，轉譯目標。<br/> |
| [**CreateHwndRenderTarget (D2D1 \_ 轉譯 \_ 目標 \_ 屬性&、D2D1 \_ HWND \_ 轉譯 \_ 目標 \_ 屬性&、ID2D1HwndRenderTarget \* \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createhwndrendertarget(constd2d1_render_target_properties__constd2d1_hwnd_render_target_properties__id2d1hwndrendertarget))   | 建立呈現至視窗的 [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))，轉譯目標。<br/> |



## <a name="remarks"></a>備註

當您建立轉譯目標並提供硬體加速時，您會在電腦的 GPU 上配置資源。 藉由建立轉譯目標一次並保留最長的時間，您就能獲得效能優勢。 您的應用程式應該建立轉譯目標一次，並在應用程式的存留期內保存它們，或在收到 [**D2DERR \_ 重新建立 \_ 目標**](direct2d-error-codes.md) 錯誤之前保留。 當您收到此錯誤時，您必須重新建立轉譯目標 (以及它所建立) 的任何資源。

## <a name="examples"></a>範例

下列範例會建立 [**ID2D1HwndRenderTarget**](/previous-versions/windows/desktop/legacy/dd371275(v=vs.85))。


```C++
RECT rc;
GetClientRect(m_hwnd, &rc);

D2D1_SIZE_U size = D2D1::SizeU(
    rc.right - rc.left,
    rc.bottom - rc.top
    );

// Create a Direct2D render target.
hr = m_pD2DFactory->CreateHwndRenderTarget(
    D2D1::RenderTargetProperties(),
    D2D1::HwndRenderTargetProperties(m_hwnd, size),
    &m_pRenderTarget
    );
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D2d1。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1Factory**](/windows/win32/api/d2d1/nn-d2d1-id2d1factory)
</dt> </dl>
