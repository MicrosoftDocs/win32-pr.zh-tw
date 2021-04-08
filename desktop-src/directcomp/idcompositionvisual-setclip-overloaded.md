---
title: 'IDCompositionVisual SetClip 方法 (Dcomp .h) '
description: 將此視覺效果的 [剪切] 屬性設定為指定的 [矩形區域] 或 [剪切] 物件。
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- SetClip 方法 DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e421c916d305b95029bb6ffd8328346b4ea36918
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686385"
---
# <a name="idcompositionvisualsetclip-methods"></a>IDCompositionVisual：： SetClip 方法

將此視覺效果的 [剪切] 屬性設定為指定的 [矩形區域] 或 [剪切] 物件。 剪輯屬性會將此視覺效果根目錄的視覺化子樹轉譯，限制為矩形區域。

### <a name="overload-list"></a>多載清單



| 方法                                                                                | 描述                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| [**SetClip (常數 D2D \_ RECT \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_)) | 將剪輯屬性設定為指定的矩形區域。<br/> |
| [**SetClip (IDCompositionClip \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip)) | 將剪輯屬性設定為指定的剪切物件。<br/>        |



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

[裁剪](clipping.md)
</dt> <dt>

[**IDCompositionVisual**](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

�

�
