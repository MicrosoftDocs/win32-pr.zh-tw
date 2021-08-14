---
title: 'IDCompositionVisual SetTransform 方法 (Dcomp .h) '
description: 設定此視覺效果的轉換屬性。 Transform 屬性會指定用來修改此視覺效果之座標系統的2D 轉換。 屬性可以指定3到2個轉換矩陣或轉換物件。
ms.assetid: DA3CBBB6-DB0A-4FCE-9DAC-7A767783A18D
keywords:
- SetTransform 方法 DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: b38c2e8fce2f0687b78b65574858a38bba681c6bc1174cab13dfa254e3b186c8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118281245"
---
# <a name="idcompositionvisualsettransform-methods"></a>IDCompositionVisual：： SetTransform 方法

設定此視覺效果的轉換屬性。 Transform 屬性會指定用來修改此視覺效果之座標系統的2D 轉換。 屬性可以指定3到2個轉換矩陣或轉換物件。

### <a name="overload-list"></a>多載清單



| 方法                                                                                                    | 描述                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform (D2D \_ 矩陣 \_ 3X2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))          | 將轉換屬性設定為指定的轉換矩陣。<br/>      |
| [**SetTransform (IDCompositionTransform \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform)) | 將轉換屬性設定為指定的轉換物件。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2012 desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Dcomp。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Dcomp .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDCompositionMatrixTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[**IDCompositionRotateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[**IDCompositionScaleTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[**IDCompositionSkewTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[**IDCompositionTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[**IDCompositionTranslateTransform**](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[**IDCompositionVisual::SetOffsetX**](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[**IDCompositionVisual::SetOffsetY**](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

�

�
