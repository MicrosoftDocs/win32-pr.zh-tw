---
title: 'IDCompositionRotateTransform3D SetAxisZ 方法 (Dcomp .h) '
description: 變更或繪製3D 旋轉轉換之 AxisZ 屬性值的動畫。 AxisZ 屬性會指定旋轉軸向量的 z 座標。 預設值為 1.0。
ms.assetid: 1A96FA00-20FE-4876-B7DF-2B833B17E925
keywords:
- SetAxisZ 方法 DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 386ce53ea59023448b66c0baab4e46125e507427
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384737"
---
# <a name="idcompositionrotatetransform3dsetaxisz-methods"></a><span data-ttu-id="757b1-106">IDCompositionRotateTransform3D：： SetAxisZ 方法</span><span class="sxs-lookup"><span data-stu-id="757b1-106">IDCompositionRotateTransform3D::SetAxisZ methods</span></span>

<span data-ttu-id="757b1-107">變更或繪製3D 旋轉轉換之 AxisZ 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="757b1-107">Changes or animates the value of the AxisZ property of a 3D rotation transform.</span></span> <span data-ttu-id="757b1-108">AxisZ 屬性會指定旋轉軸向量的 z 座標。</span><span class="sxs-lookup"><span data-stu-id="757b1-108">The AxisZ property specifies the z-coordinate for the axis vector of rotation.</span></span> <span data-ttu-id="757b1-109">預設值為 1.0。</span><span class="sxs-lookup"><span data-stu-id="757b1-109">The default value is 1.0.</span></span>

### <a name="overload-list"></a><span data-ttu-id="757b1-110">多載清單</span><span class="sxs-lookup"><span data-stu-id="757b1-110">Overload list</span></span>



| <span data-ttu-id="757b1-111">方法</span><span class="sxs-lookup"><span data-stu-id="757b1-111">Method</span></span>                                                                                                       | <span data-ttu-id="757b1-112">描述</span><span class="sxs-lookup"><span data-stu-id="757b1-112">Description</span></span>                                          |
|:-------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| <span data-ttu-id="757b1-113">[**SetAxisZ (float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisz(float))</span><span class="sxs-lookup"><span data-stu-id="757b1-113">[**SetAxisZ(float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisz(float))</span></span>                                     | <span data-ttu-id="757b1-114">變更 AxisZ 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="757b1-114">Changes the value of the AxisZ property.</span></span><br/>  |
| <span data-ttu-id="757b1-115">[**SetAxisZ (IDCompositionAnimation \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisz(idcompositionanimation))</span><span class="sxs-lookup"><span data-stu-id="757b1-115">[**SetAxisZ(IDCompositionAnimation\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisz(idcompositionanimation))</span></span> | <span data-ttu-id="757b1-116">繪製 AxisZ 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="757b1-116">Animates the value of the AxisZ property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="757b1-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="757b1-117">Requirements</span></span>



| <span data-ttu-id="757b1-118">需求</span><span class="sxs-lookup"><span data-stu-id="757b1-118">Requirement</span></span> | <span data-ttu-id="757b1-119">值</span><span class="sxs-lookup"><span data-stu-id="757b1-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="757b1-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="757b1-120">Minimum supported client</span></span><br/> | <span data-ttu-id="757b1-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="757b1-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="757b1-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="757b1-122">Minimum supported server</span></span><br/> | <span data-ttu-id="757b1-123">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="757b1-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="757b1-124">標頭</span><span class="sxs-lookup"><span data-stu-id="757b1-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="757b1-125"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="757b1-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="757b1-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="757b1-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="757b1-127"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="757b1-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="757b1-128">DLL</span><span class="sxs-lookup"><span data-stu-id="757b1-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="757b1-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="757b1-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="757b1-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="757b1-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="757b1-131">**IDCompositionRotateTransform3D**</span><span class="sxs-lookup"><span data-stu-id="757b1-131">**IDCompositionRotateTransform3D**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d)
</dt> </dl>

<span data-ttu-id="757b1-132">�</span><span class="sxs-lookup"><span data-stu-id="757b1-132">�</span></span>

<span data-ttu-id="757b1-133">�</span><span class="sxs-lookup"><span data-stu-id="757b1-133">�</span></span>
