---
title: 'D2D1_SIZE_U (D2DBaseTypes) '
description: 儲存已排序的整數配對，通常是矩形的寬度和高度。
ms.assetid: e28da5ee-7d68-4ec5-b477-c6ead0c725e6
keywords:
- D2D1_SIZE_U
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c78b5c317a98169957402dd125c054b8f6e0bc69
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094155"
---
# <a name="d2d1_size_u"></a>D2D1 \_ 大小 \_ U

儲存已排序的整數配對，通常是矩形的寬度和高度。


```C++
typedef D2D_SIZE_U D2D1_SIZE_U;
```



## <a name="remarks"></a>備註

就像點一樣，大小是另一個重要的圖形概念。 在 Direct2D 中，大小會以 **D2D1 \_ 大小 \_ U** 或 [**D2D1 大小的 \_ \_ F**](d2d1-size-f.md) 結構表示。 它們都包含一組已排序的數位。 **D2D1 \_ 大小 \_ U** 結構包含 **UINT32** 值的排序配對，而 **D2D1 \_ 大小 \_ F** 結構包含一組已排序的 **FLOAT** 值配對。

**D2D1 \_ 大小 \_ U** 結構提供一個便利的方式，讓您儲存一組已排序的數位，例如矩形的寬度和高度。

**D2D1 \_大小 \_ u** 是已定義的類型 **D2D \_ 大小 \_ u** 的新名稱。 您可以使用 **D2D1：： SizeU** 函數來建立 **D2D1 \_ 大小 \_ U** 結構。 此結構的常見用法是指定 [**D2D1 \_ HWND 轉譯 \_ \_ 目標 \_ 屬性**](/windows/desktop/api/d2d1/ns-d2d1-d2d1_hwnd_render_target_properties) 結構的圖元大小。 以下提供使用此結構的範例。


```C++
    if (!m_pRenderTarget)
    {
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
|-------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7、windows Vista （含 SP2）和平臺更新（適用于 Windows Vista \[ 桌面應用程式 \| UWP 應用程式）\]<br/>                          |
| 最低支援的伺服器<br/> | Windows server 2008 R2、Windows Server 2008 SP2 和 Windows Server 的平臺更新 2008 \[ 桌面應用程式 \| UWP 應用程式\]<br/> |
| 支援的最小電話<br/>  | Windows Phone 8.1 \[ Windows Phone Silverlight 8.1 和 Windows 執行階段應用程式\]<br/>                                                  |
| 標頭<br/>                   | <dl> <dt>D2DBaseTypes (包含 D2d1) </dt> </dl>                               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**D2D \_ 大小 \_ U**](/windows/desktop/api/dcommon/ns-dcommon-d2d_size_u)
</dt> <dt>

[**D2D1 \_ 大小 \_ F**](d2d1-size-f.md)
</dt> <dt>

[**D2D1::HwndRenderTargetProperties**](/windows/desktop/api/d2d1helper/nf-d2d1helper-hwndrendertargetproperties)
</dt> </dl>

 

