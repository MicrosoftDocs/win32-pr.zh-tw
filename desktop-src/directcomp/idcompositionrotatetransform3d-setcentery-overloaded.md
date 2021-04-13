---
title: 'IDCompositionRotateTransform3D SetCenterY 方法 (Dcomp .h) '
description: 變更或繪製3D 旋轉轉換之 CenterY 屬性值的動畫。 CenterY 屬性會指定執行旋轉的點的 y 座標。 預設值為零。
ms.assetid: 19B3B065-BE8C-4CBD-8A94-54934CA0B421
keywords:
- SetCenterY 方法 DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: c492e926ebb2dc6355ce1a3acfa68090dfd560f3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466676"
---
# <a name="idcompositionrotatetransform3dsetcentery-methods"></a><span data-ttu-id="a8e0d-106">IDCompositionRotateTransform3D：： SetCenterY 方法</span><span class="sxs-lookup"><span data-stu-id="a8e0d-106">IDCompositionRotateTransform3D::SetCenterY methods</span></span>

<span data-ttu-id="a8e0d-107">變更或繪製3D 旋轉轉換之 CenterY 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="a8e0d-107">Changes or animates the value of the CenterY property of a 3D rotation transform.</span></span> <span data-ttu-id="a8e0d-108">CenterY 屬性會指定執行旋轉的點的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="a8e0d-108">The CenterY property specifies the y-coordinate of the point about which the rotation is performed.</span></span> <span data-ttu-id="a8e0d-109">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="a8e0d-109">The default value is zero.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a8e0d-110">多載清單</span><span class="sxs-lookup"><span data-stu-id="a8e0d-110">Overload list</span></span>



| <span data-ttu-id="a8e0d-111">方法</span><span class="sxs-lookup"><span data-stu-id="a8e0d-111">Method</span></span>                                                                                                           | <span data-ttu-id="a8e0d-112">描述</span><span class="sxs-lookup"><span data-stu-id="a8e0d-112">Description</span></span>                                            |
|:-----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| <span data-ttu-id="a8e0d-113">[**SetCenterY (float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setcentery(float))</span><span class="sxs-lookup"><span data-stu-id="a8e0d-113">[**SetCenterY(float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setcentery(float))</span></span>                                     | <span data-ttu-id="a8e0d-114">變更 CenterY 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a8e0d-114">Changes the value of the CenterY property.</span></span><br/>  |
| <span data-ttu-id="a8e0d-115">[**SetCenterX (IDCompositionAnimation \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setcentery(idcompositionanimation))</span><span class="sxs-lookup"><span data-stu-id="a8e0d-115">[**SetCenterX(IDCompositionAnimation\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setcentery(idcompositionanimation))</span></span> | <span data-ttu-id="a8e0d-116">繪製 CenterY 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="a8e0d-116">Animates the value of the CenterY property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a8e0d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8e0d-117">Requirements</span></span>



| <span data-ttu-id="a8e0d-118">需求</span><span class="sxs-lookup"><span data-stu-id="a8e0d-118">Requirement</span></span> | <span data-ttu-id="a8e0d-119">值</span><span class="sxs-lookup"><span data-stu-id="a8e0d-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e0d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8e0d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e0d-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8e0d-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a8e0d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8e0d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e0d-123">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a8e0d-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a8e0d-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a8e0d-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a8e0d-125"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a8e0d-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a8e0d-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="a8e0d-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a8e0d-127"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a8e0d-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="a8e0d-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a8e0d-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8e0d-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8e0d-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a8e0d-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8e0d-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e0d-131">**IDCompositionRotateTransform3D**</span><span class="sxs-lookup"><span data-stu-id="a8e0d-131">**IDCompositionRotateTransform3D**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d)
</dt> </dl>

<span data-ttu-id="a8e0d-132">�</span><span class="sxs-lookup"><span data-stu-id="a8e0d-132">�</span></span>

<span data-ttu-id="a8e0d-133">�</span><span class="sxs-lookup"><span data-stu-id="a8e0d-133">�</span></span>
