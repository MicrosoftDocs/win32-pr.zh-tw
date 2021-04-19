---
title: 'IDCompositionRotateTransform3D SetAxisY 方法 (Dcomp .h) '
description: 變更或繪製旋轉轉換之 AxisY 屬性值的動畫。 AxisY 屬性會指定旋轉軸向量的 y 座標。 預設值為零。
ms.assetid: C86E4D59-4E9D-44BF-BA9D-91714D0C2D37
keywords:
- SetAxisY 方法 DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: eab0006db884aa0f91f589ed8d80c9daa36f7f36
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966317"
---
# <a name="idcompositionrotatetransform3dsetaxisy-methods"></a><span data-ttu-id="6fb3c-106">IDCompositionRotateTransform3D：： SetAxisY 方法</span><span class="sxs-lookup"><span data-stu-id="6fb3c-106">IDCompositionRotateTransform3D::SetAxisY methods</span></span>

<span data-ttu-id="6fb3c-107">變更或繪製旋轉轉換之 AxisY 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="6fb3c-107">Changes or animates the value of the AxisY property of a rotation transform.</span></span> <span data-ttu-id="6fb3c-108">AxisY 屬性會指定旋轉軸向量的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="6fb3c-108">The AxisY property specifies the y-coordinate for the axis vector of rotation.</span></span> <span data-ttu-id="6fb3c-109">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="6fb3c-109">The default value is zero.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6fb3c-110">多載清單</span><span class="sxs-lookup"><span data-stu-id="6fb3c-110">Overload list</span></span>



| <span data-ttu-id="6fb3c-111">方法</span><span class="sxs-lookup"><span data-stu-id="6fb3c-111">Method</span></span>                                                                                                       | <span data-ttu-id="6fb3c-112">描述</span><span class="sxs-lookup"><span data-stu-id="6fb3c-112">Description</span></span>                                          |
|:-------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| <span data-ttu-id="6fb3c-113">[**SetAxisY (float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisy(float))</span><span class="sxs-lookup"><span data-stu-id="6fb3c-113">[**SetAxisY(float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisy(float))</span></span>                                     | <span data-ttu-id="6fb3c-114">變更 AxisY 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="6fb3c-114">Changes the value of the AxisY property.</span></span><br/>  |
| <span data-ttu-id="6fb3c-115">[**SetAxisY (IDCompositionAnimation \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisy(idcompositionanimation))</span><span class="sxs-lookup"><span data-stu-id="6fb3c-115">[**SetAxisY(IDCompositionAnimation\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform3d-setaxisy(idcompositionanimation))</span></span> | <span data-ttu-id="6fb3c-116">繪製 AxisY 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="6fb3c-116">Animates the value of the AxisY property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6fb3c-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6fb3c-117">Requirements</span></span>



| <span data-ttu-id="6fb3c-118">需求</span><span class="sxs-lookup"><span data-stu-id="6fb3c-118">Requirement</span></span> | <span data-ttu-id="6fb3c-119">值</span><span class="sxs-lookup"><span data-stu-id="6fb3c-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6fb3c-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6fb3c-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6fb3c-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6fb3c-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6fb3c-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6fb3c-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6fb3c-123">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6fb3c-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6fb3c-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6fb3c-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6fb3c-125"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6fb3c-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6fb3c-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="6fb3c-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="6fb3c-127"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6fb3c-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="6fb3c-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6fb3c-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6fb3c-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6fb3c-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6fb3c-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6fb3c-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6fb3c-131">**IDCompositionRotateTransform3D**</span><span class="sxs-lookup"><span data-stu-id="6fb3c-131">**IDCompositionRotateTransform3D**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform3d)
</dt> </dl>

<span data-ttu-id="6fb3c-132">�</span><span class="sxs-lookup"><span data-stu-id="6fb3c-132">�</span></span>

<span data-ttu-id="6fb3c-133">�</span><span class="sxs-lookup"><span data-stu-id="6fb3c-133">�</span></span>
