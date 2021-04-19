---
title: 'D2D1_COLOR_F (D2DBaseTypes) '
description: '描述色彩的紅色、綠色、藍色和 Alpha 元件。 |D2D1_COLOR_F (D2DBaseTypes) '
ms.assetid: 564d4f41-2da7-49ed-b85a-d1070d662b40
keywords:
- D2D1_COLOR_F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 78f12c4c833d7f73946b2309673dff8f3dd11395
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991956"
---
# <a name="d2d1_color_f"></a>D2D1 \_ 色彩 \_ F

描述色彩的紅色、綠色、藍色和 Alpha 元件。


```C++
typedef D2D_COLOR_F D2D1_COLOR_F;
```



## <a name="remarks"></a>備註

**D2D1 \_\_F** 色是 [**D2D \_ 色 \_ f**](d2d-color-f.md)的 typedef，它本身是 [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)的 typedef。 如需 **D2D1 \_ COLOR \_ F** 所提供成員的詳細資訊，請參閱 [D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)。

[**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)類別會提供一組預先定義的色彩，以及用來定義色彩的 helper 函數。 如需詳細資訊，請參閱 [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 參考。

## <a name="examples"></a>範例

下列範例會使用 [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 類別，在建立 [**ID2D1SolidColorBrush**](/windows/win32/api/d2d1/nn-d2d1-id2d1solidcolorbrush)時，指定 (黑色) 預先定義的色彩。


```C++
hr = m_pRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF::Black, 1.0f),
    &m_pBlackBrush
    );
```



下列範例會使用 [**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf) 類別來指定使用紅色、綠色、藍色和 Alpha 值的色彩。


```C++
ID2D1SolidColorBrush *pGridBrush = NULL;
hr = pCompatibleRenderTarget->CreateSolidColorBrush(
    D2D1::ColorF(D2D1::ColorF(0.93f, 0.94f, 0.96f, 1.0f)),
    &pGridBrush
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

[D3DCOLORVALUE](../direct3d9/d3dcolorvalue.md)
</dt> <dt>

[**ColorF**](/windows/win32/api/d2d1helper/nl-d2d1helper-colorf)
</dt> </dl>

 

