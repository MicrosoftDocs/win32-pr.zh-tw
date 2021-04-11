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
ms.openlocfilehash: 00f5da890cd22c5c827a36062a0b0c3f9bc19cc3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317443"
---
# <a name="idcompositionvisualsettransform-methods"></a><span data-ttu-id="bf5e2-106">IDCompositionVisual：： SetTransform 方法</span><span class="sxs-lookup"><span data-stu-id="bf5e2-106">IDCompositionVisual::SetTransform methods</span></span>

<span data-ttu-id="bf5e2-107">設定此視覺效果的轉換屬性。</span><span class="sxs-lookup"><span data-stu-id="bf5e2-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="bf5e2-108">Transform 屬性會指定用來修改此視覺效果之座標系統的2D 轉換。</span><span class="sxs-lookup"><span data-stu-id="bf5e2-108">The Transform property specifies a 2D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="bf5e2-109">屬性可以指定3到2個轉換矩陣或轉換物件。</span><span class="sxs-lookup"><span data-stu-id="bf5e2-109">The property can specify either a 3-by-2 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="bf5e2-110">多載清單</span><span class="sxs-lookup"><span data-stu-id="bf5e2-110">Overload list</span></span>



| <span data-ttu-id="bf5e2-111">方法</span><span class="sxs-lookup"><span data-stu-id="bf5e2-111">Method</span></span>                                                                                                    | <span data-ttu-id="bf5e2-112">描述</span><span class="sxs-lookup"><span data-stu-id="bf5e2-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="bf5e2-113">[**SetTransform (D2D \_ 矩陣 \_ 3X2 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span><span class="sxs-lookup"><span data-stu-id="bf5e2-113">[**SetTransform(D2D\_MATRIX\_3X2\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(constd2d_matrix_3x2_f_))</span></span>          | <span data-ttu-id="bf5e2-114">將轉換屬性設定為指定的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="bf5e2-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="bf5e2-115">[**SetTransform (IDCompositionTransform \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span><span class="sxs-lookup"><span data-stu-id="bf5e2-115">[**SetTransform(IDCompositionTransform\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-settransform(idcompositiontransform))</span></span> | <span data-ttu-id="bf5e2-116">將轉換屬性設定為指定的轉換物件。</span><span class="sxs-lookup"><span data-stu-id="bf5e2-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="bf5e2-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf5e2-117">Requirements</span></span>



| <span data-ttu-id="bf5e2-118">需求</span><span class="sxs-lookup"><span data-stu-id="bf5e2-118">Requirement</span></span> | <span data-ttu-id="bf5e2-119">值</span><span class="sxs-lookup"><span data-stu-id="bf5e2-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="bf5e2-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf5e2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf5e2-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf5e2-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="bf5e2-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf5e2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf5e2-123">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bf5e2-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="bf5e2-124">標頭</span><span class="sxs-lookup"><span data-stu-id="bf5e2-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf5e2-125"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="bf5e2-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf5e2-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="bf5e2-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="bf5e2-127"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bf5e2-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="bf5e2-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bf5e2-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf5e2-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf5e2-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf5e2-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf5e2-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf5e2-131">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="bf5e2-131">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="bf5e2-132">**IDCompositionRotateTransform**</span><span class="sxs-lookup"><span data-stu-id="bf5e2-132">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="bf5e2-133">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="bf5e2-133">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="bf5e2-134">**IDCompositionSkewTransform**</span><span class="sxs-lookup"><span data-stu-id="bf5e2-134">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="bf5e2-135">**IDCompositionTransform**</span><span class="sxs-lookup"><span data-stu-id="bf5e2-135">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="bf5e2-136">**IDCompositionTranslateTransform**</span><span class="sxs-lookup"><span data-stu-id="bf5e2-136">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="bf5e2-137">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="bf5e2-137">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="bf5e2-138">**IDCompositionVisual::SetOffsetX**</span><span class="sxs-lookup"><span data-stu-id="bf5e2-138">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="bf5e2-139">**IDCompositionVisual::SetOffsetY**</span><span class="sxs-lookup"><span data-stu-id="bf5e2-139">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="bf5e2-140">�</span><span class="sxs-lookup"><span data-stu-id="bf5e2-140">�</span></span>

<span data-ttu-id="bf5e2-141">�</span><span class="sxs-lookup"><span data-stu-id="bf5e2-141">�</span></span>
