---
title: 'IDCompositionMatrixTransform3D SetMatrixElement 方法 (Dcomp .h) '
description: 變更或繪製此3D 轉換之矩陣的某個元素值的動畫。
ms.assetid: 0494B335-B613-4F0A-9CDA-3BBC63A7B996
keywords:
- SetMatrixElement 方法 DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 62eec746db5543fdf34893970b120aa6517139ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934955"
---
# <a name="idcompositionmatrixtransform3dsetmatrixelement-methods"></a><span data-ttu-id="671be-104">IDCompositionMatrixTransform3D：： SetMatrixElement 方法</span><span class="sxs-lookup"><span data-stu-id="671be-104">IDCompositionMatrixTransform3D::SetMatrixElement methods</span></span>

<span data-ttu-id="671be-105">變更或繪製此3D 轉換之矩陣的某個元素值的動畫。</span><span class="sxs-lookup"><span data-stu-id="671be-105">Changes or animates the value of one element of the matrix of this 3D transform.</span></span>

### <a name="overload-list"></a><span data-ttu-id="671be-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="671be-106">Overload list</span></span>



| <span data-ttu-id="671be-107">方法</span><span class="sxs-lookup"><span data-stu-id="671be-107">Method</span></span>                                                                                                                                 | <span data-ttu-id="671be-108">描述</span><span class="sxs-lookup"><span data-stu-id="671be-108">Description</span></span>                                                                      |
|:---------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| <span data-ttu-id="671be-109">[**SetMatrixElement (int，int，float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform3d-setmatrixelement(int_int_float))</span><span class="sxs-lookup"><span data-stu-id="671be-109">[**SetMatrixElement(int, int, float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform3d-setmatrixelement(int_int_float))</span></span>                                     | <span data-ttu-id="671be-110">變更此3D 轉換之矩陣的一個元素值。</span><span class="sxs-lookup"><span data-stu-id="671be-110">Changes the value of one element of the matrix of this 3D transform.</span></span><br/>  |
| <span data-ttu-id="671be-111">[**SetMatrixElement (int，int，IDCompositionAnimation \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform3d-setmatrixelement(int_int_idcompositionanimation))</span><span class="sxs-lookup"><span data-stu-id="671be-111">[**SetMatrixElement(int, int, IDCompositionAnimation\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform3d-setmatrixelement(int_int_idcompositionanimation))</span></span> | <span data-ttu-id="671be-112">將此3D 轉換之矩陣的某個元素值繪製成動畫。</span><span class="sxs-lookup"><span data-stu-id="671be-112">Animates the value of one element of the matrix of this 3D transform.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="671be-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="671be-113">Requirements</span></span>



| <span data-ttu-id="671be-114">需求</span><span class="sxs-lookup"><span data-stu-id="671be-114">Requirement</span></span> | <span data-ttu-id="671be-115">值</span><span class="sxs-lookup"><span data-stu-id="671be-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="671be-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="671be-116">Minimum supported client</span></span><br/> | <span data-ttu-id="671be-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="671be-117">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="671be-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="671be-118">Minimum supported server</span></span><br/> | <span data-ttu-id="671be-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="671be-119">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="671be-120">標頭</span><span class="sxs-lookup"><span data-stu-id="671be-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="671be-121"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="671be-121"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="671be-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="671be-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="671be-123"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="671be-123"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="671be-124">DLL</span><span class="sxs-lookup"><span data-stu-id="671be-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="671be-125"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="671be-125"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="671be-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="671be-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="671be-127">**IDCompositionMatrixTransform3D**</span><span class="sxs-lookup"><span data-stu-id="671be-127">**IDCompositionMatrixTransform3D**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform3d)
</dt> </dl>

<span data-ttu-id="671be-128">�</span><span class="sxs-lookup"><span data-stu-id="671be-128">�</span></span>

<span data-ttu-id="671be-129">�</span><span class="sxs-lookup"><span data-stu-id="671be-129">�</span></span>
