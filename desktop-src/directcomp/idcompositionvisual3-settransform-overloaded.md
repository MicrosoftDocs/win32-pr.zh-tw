---
title: 'IDCompositionVisual3 SetTransform 方法 (Dcomp .h) '
description: 設定此視覺效果的轉換屬性。 Transform 屬性會指定用來修改此視覺效果之座標系統的3D 轉換。 屬性可以指定四個轉換矩陣或一個轉換物件。
ms.assetid: a59498c2-8659-dd35-8dc2-87457f493965
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
ms.openlocfilehash: 50237d4bbc8504a6bdcc9650f6c02dbdc30d093c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969591"
---
# <a name="idcompositionvisual3settransform-methods"></a>IDCompositionVisual3：： SetTransform 方法

設定此視覺效果的轉換屬性。 Transform 屬性會指定用來修改此視覺效果之座標系統的3D 轉換。 屬性可以指定四個轉換矩陣或一個轉換物件。

### <a name="overload-list"></a>多載清單



| 方法                                                                                  | 描述                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| [**SetTransform (D2D \_ 矩陣 \_ 4x4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))       | 將轉換屬性設定為指定的轉換矩陣。<br/>      |
| [**SetTransform (IDCompositionTransform3D \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d)) | 將轉換屬性設定為指定的轉換物件。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                 |
| 標頭<br/>                   | <dl> <dt>Dcomp。h</dt> </dl>   |
| 程式庫<br/>                  | <dl> <dt>Dcomp .lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Dcomp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IDCompositionVisual3**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

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
