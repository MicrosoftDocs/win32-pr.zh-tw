---
title: 'ID2D1RenderTarget PushAxisAlignedClip 方法 (D2d1 \_ 1 .h) '
description: 指定裁剪所有後續繪圖作業的矩形。
ms.assetid: 8b777425-07b1-4494-889a-0c947fb61315
keywords:
- PushAxisAlignedClip 方法 Direct2D
topic_type:
- apiref
api_location:
- D2d1.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: d7e6d59f1c4cbffcde74ecb7b5adb5b12eff06bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996509"
---
# <a name="id2d1rendertargetpushaxisalignedclip-methods"></a>ID2D1RenderTarget：:P ushAxisAlignedClip 方法

指定裁剪所有後續繪圖作業的矩形。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                                                         | 描述                                                                               |
|:-----------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------|
| [**PushAxisAlignedClip (D2D1 \_ RECT \_ F&、D2D1 \_ 消除鋸齒 \_ 模式)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))  | 指定裁剪所有後續繪圖作業的矩形。 <br/> |
| [**PushAxisAlignedClip (D2D1 \_ RECT \_ F \* 、D2D1 \_ 消除鋸齒 \_ 模式)**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode)) | 指定裁剪所有後續繪圖作業的矩形。 <br/> |



## <a name="remarks"></a>備註

[**PushAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushaxisalignedclip(constd2d1_rect_f__d2d1_antialias_mode))和 [**PopAxisAlignedClip**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-popaxisalignedclip)組可以在 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))和 [**PopLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-poplayer)中進行，但不能重迭。 例如， **PushAxisAlignedClip**、 [**PushLayer**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-pushlayer(constd2d1_layer_parameters__id2d1layer))、 **PopLayer**、 **PopAxisAlignedClip** 的序列是有效的，但 **PushAxisAlignedClip**、 **PushLayer**、 **PopAxisAlignedClip**、 **PopLayer** 的序列無效。

如果失敗，這個方法不會傳回錯誤碼。 若要判斷繪圖作業 (如 **PushAxisAlignedClip**) 是否失敗，請檢查 [**ID2D1RenderTarget：： EndDraw**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-enddraw) 或 [**ID2D1RenderTarget：： Flush**](/windows/win32/api/d2d1/nf-d2d1-id2d1rendertarget-flush) 方法所傳回的結果。

## <a name="examples"></a>範例

如需範例，請參閱 [如何使用 Axis-Aligned 剪切矩形的剪輯](how-to-clip-with-axis-aligned-rects.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|-------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>D2d1 \_ 1. h (包括 D2d1) </dt> </dl> |
| 程式庫<br/> | <dl> <dt>D2d1 .lib</dt> </dl>                   |
| DLL<br/>     | <dl> <dt>D2d1.dll</dt> </dl>                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ID2D1RenderTarget**](/windows/win32/api/d2d1/nn-d2d1-id2d1rendertarget)
</dt> </dl>

�

�
