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
# <a name="idcompositionvisual3settransform-methods"></a><span data-ttu-id="d16f1-106">IDCompositionVisual3：： SetTransform 方法</span><span class="sxs-lookup"><span data-stu-id="d16f1-106">IDCompositionVisual3::SetTransform methods</span></span>

<span data-ttu-id="d16f1-107">設定此視覺效果的轉換屬性。</span><span class="sxs-lookup"><span data-stu-id="d16f1-107">Sets the Transform property of this visual.</span></span> <span data-ttu-id="d16f1-108">Transform 屬性會指定用來修改此視覺效果之座標系統的3D 轉換。</span><span class="sxs-lookup"><span data-stu-id="d16f1-108">The Transform property specifies a 3D transform used to modify the coordinate system of this visual.</span></span> <span data-ttu-id="d16f1-109">屬性可以指定四個轉換矩陣或一個轉換物件。</span><span class="sxs-lookup"><span data-stu-id="d16f1-109">The property can specify either a 4-by-4 transform matrix or a transform object.</span></span>

### <a name="overload-list"></a><span data-ttu-id="d16f1-110">多載清單</span><span class="sxs-lookup"><span data-stu-id="d16f1-110">Overload list</span></span>



| <span data-ttu-id="d16f1-111">方法</span><span class="sxs-lookup"><span data-stu-id="d16f1-111">Method</span></span>                                                                                  | <span data-ttu-id="d16f1-112">描述</span><span class="sxs-lookup"><span data-stu-id="d16f1-112">Description</span></span>                                                                    |
|:----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------|
| <span data-ttu-id="d16f1-113">[**SetTransform (D2D \_ 矩陣 \_ 4x4 \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span><span class="sxs-lookup"><span data-stu-id="d16f1-113">[**SetTransform(D2D\_MATRIX\_4X4\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(constd2d_matrix_4x4_f_))</span></span>       | <span data-ttu-id="d16f1-114">將轉換屬性設定為指定的轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="d16f1-114">Sets the Transform property to the specified transform matrix.</span></span><br/>      |
| <span data-ttu-id="d16f1-115">[**SetTransform (IDCompositionTransform3D \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span><span class="sxs-lookup"><span data-stu-id="d16f1-115">[**SetTransform(IDCompositionTransform3D\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual3-settransform(idcompositiontransform3d))</span></span> | <span data-ttu-id="d16f1-116">將轉換屬性設定為指定的轉換物件。</span><span class="sxs-lookup"><span data-stu-id="d16f1-116">Sets the Transform property to the specified transformation object.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="d16f1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="d16f1-117">Requirements</span></span>



| <span data-ttu-id="d16f1-118">需求</span><span class="sxs-lookup"><span data-stu-id="d16f1-118">Requirement</span></span> | <span data-ttu-id="d16f1-119">值</span><span class="sxs-lookup"><span data-stu-id="d16f1-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d16f1-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d16f1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="d16f1-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d16f1-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d16f1-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d16f1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="d16f1-123">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d16f1-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d16f1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d16f1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d16f1-125"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="d16f1-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="d16f1-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="d16f1-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="d16f1-127"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d16f1-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="d16f1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d16f1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d16f1-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d16f1-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d16f1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d16f1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d16f1-131">**IDCompositionVisual3**</span><span class="sxs-lookup"><span data-stu-id="d16f1-131">**IDCompositionVisual3**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual3)
</dt> <dt>

[<span data-ttu-id="d16f1-132">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="d16f1-132">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> <dt>

[<span data-ttu-id="d16f1-133">**IDCompositionRotateTransform**</span><span class="sxs-lookup"><span data-stu-id="d16f1-133">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> <dt>

[<span data-ttu-id="d16f1-134">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="d16f1-134">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="d16f1-135">**IDCompositionSkewTransform**</span><span class="sxs-lookup"><span data-stu-id="d16f1-135">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> <dt>

[<span data-ttu-id="d16f1-136">**IDCompositionTransform**</span><span class="sxs-lookup"><span data-stu-id="d16f1-136">**IDCompositionTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontransform)
</dt> <dt>

[<span data-ttu-id="d16f1-137">**IDCompositionTranslateTransform**</span><span class="sxs-lookup"><span data-stu-id="d16f1-137">**IDCompositionTranslateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositiontranslatetransform)
</dt> <dt>

[<span data-ttu-id="d16f1-138">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="d16f1-138">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> <dt>

[<span data-ttu-id="d16f1-139">**IDCompositionVisual::SetOffsetX**</span><span class="sxs-lookup"><span data-stu-id="d16f1-139">**IDCompositionVisual::SetOffsetX**</span></span>](idcompositionvisual-setoffsetx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="d16f1-140">**IDCompositionVisual::SetOffsetY**</span><span class="sxs-lookup"><span data-stu-id="d16f1-140">**IDCompositionVisual::SetOffsetY**</span></span>](idcompositionvisual-setoffsety-overloaded.md)
</dt> </dl>

<span data-ttu-id="d16f1-141">�</span><span class="sxs-lookup"><span data-stu-id="d16f1-141">�</span></span>

<span data-ttu-id="d16f1-142">�</span><span class="sxs-lookup"><span data-stu-id="d16f1-142">�</span></span>
