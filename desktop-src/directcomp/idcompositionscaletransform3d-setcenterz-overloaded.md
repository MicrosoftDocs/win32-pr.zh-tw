---
title: 'IDCompositionScaleTransform3D SetCenterZ 方法 (Dcomp .h) '
description: 變更或繪製3D 縮放轉換之 CenterZ 屬性值的動畫。
ms.assetid: 1A5C63FE-2378-4274-8ADD-04A88B60FF8F
keywords:
- SetCenterZ 方法 DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 24a554689c7f0a26047ac011686b7dcd6c41ffbf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317447"
---
# <a name="idcompositionscaletransform3dsetcenterz-methods"></a><span data-ttu-id="ca1c1-104">IDCompositionScaleTransform3D：： SetCenterZ 方法</span><span class="sxs-lookup"><span data-stu-id="ca1c1-104">IDCompositionScaleTransform3D::SetCenterZ methods</span></span>

<span data-ttu-id="ca1c1-105">變更或繪製3D 縮放轉換之 CenterZ 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="ca1c1-105">Changes or animates the value of the CenterZ property of a 3D scale transform.</span></span> <span data-ttu-id="ca1c1-106">CenterZ 屬性會指定執行調整的點的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="ca1c1-106">The CenterZ property specifies the z-coordinate of the point about which scaling is performed.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ca1c1-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="ca1c1-107">Overload list</span></span>



| <span data-ttu-id="ca1c1-108">方法</span><span class="sxs-lookup"><span data-stu-id="ca1c1-108">Method</span></span>                                                                                                          | <span data-ttu-id="ca1c1-109">描述</span><span class="sxs-lookup"><span data-stu-id="ca1c1-109">Description</span></span>                                            |
|:----------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| <span data-ttu-id="ca1c1-110">[**SetCenterZ (float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform3d-setcenterz(float))</span><span class="sxs-lookup"><span data-stu-id="ca1c1-110">[**SetCenterZ(float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform3d-setcenterz(float))</span></span>                                     | <span data-ttu-id="ca1c1-111">變更 CenterZ 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="ca1c1-111">Changes the value of the CenterZ property.</span></span><br/>  |
| <span data-ttu-id="ca1c1-112">[**SetCenterZ (IDCompositionAnimation \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform3d-setcenterz(idcompositionanimation))</span><span class="sxs-lookup"><span data-stu-id="ca1c1-112">[**SetCenterZ(IDCompositionAnimation\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform3d-setcenterz(idcompositionanimation))</span></span> | <span data-ttu-id="ca1c1-113">繪製 CenterZ 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="ca1c1-113">Animates the value of the CenterZ property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ca1c1-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca1c1-114">Requirements</span></span>



| <span data-ttu-id="ca1c1-115">需求</span><span class="sxs-lookup"><span data-stu-id="ca1c1-115">Requirement</span></span> | <span data-ttu-id="ca1c1-116">值</span><span class="sxs-lookup"><span data-stu-id="ca1c1-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ca1c1-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca1c1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ca1c1-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca1c1-118">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ca1c1-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca1c1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ca1c1-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca1c1-120">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ca1c1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ca1c1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca1c1-122"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca1c1-122"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ca1c1-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="ca1c1-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="ca1c1-124"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ca1c1-124"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="ca1c1-125">DLL</span><span class="sxs-lookup"><span data-stu-id="ca1c1-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca1c1-126"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca1c1-126"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca1c1-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca1c1-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca1c1-128">**IDCompositionScaleTransform3D**</span><span class="sxs-lookup"><span data-stu-id="ca1c1-128">**IDCompositionScaleTransform3D**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="ca1c1-129">**IDCompositionScaleTransform3D::SetCenterX**</span><span class="sxs-lookup"><span data-stu-id="ca1c1-129">**IDCompositionScaleTransform3D::SetCenterX**</span></span>](idcompositionscaletransform3d-setcenterx-overloaded.md)
</dt> <dt>

[<span data-ttu-id="ca1c1-130">**IDCompositionScaleTransform3D::SetCenterY**</span><span class="sxs-lookup"><span data-stu-id="ca1c1-130">**IDCompositionScaleTransform3D::SetCenterY**</span></span>](idcompositionscaletransform3d-setcentery-overloaded.md)
</dt> </dl>

<span data-ttu-id="ca1c1-131">�</span><span class="sxs-lookup"><span data-stu-id="ca1c1-131">�</span></span>

<span data-ttu-id="ca1c1-132">�</span><span class="sxs-lookup"><span data-stu-id="ca1c1-132">�</span></span>
