---
title: 'ID2D1RenderTarget FillEllipse 方法 (D2d1 .h) '
description: 繪製指定橢圓形的內部。
ms.assetid: 149fb303-d2e8-416c-b28f-8bc5f1482ba6
keywords:
- FillEllipse 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b8328775d87dd4df0fd015990d31db0751b729bc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999994"
---
# <a name="id2d1rendertargetfillellipse-methods"></a>ID2D1RenderTarget：： FillEllipse 方法

繪製指定橢圓形的內部。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                             | 描述                                               |
|:-------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------|
| [**FillEllipse (D2D1 \_ 橢圓形&、ID2D1Brush \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush))  | 繪製指定橢圓形的內部。 <br/> |
| [**FillEllipse (D2D1 \_ 橢圓形 \* 、ID2D1Brush \*)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-fillellipse(constd2d1_ellipse__id2d1brush)) | 繪製指定橢圓形的內部。 <br/> |



## <a name="remarks"></a>備註

如果失敗，這個方法不會傳回錯誤碼。 若要判斷繪圖作業 (如 **FillEllipse**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。

## <a name="examples"></a>範例

如需範例，請參閱 [如何繪製和填滿基本圖形](how-to-draw-an-ellipse.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D2d1。h</dt> </dl>   |
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl> |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> <dt>

[如何繪製和填滿基本圖形](how-to-draw-an-ellipse.md)
</dt> </dl>

�

�
