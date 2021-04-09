---
title: 'IDCompositionMatrixTransform SetMatrixElement 方法 (Dcomp .h) '
description: 變更或繪製此2D 轉換之矩陣的某個元素值的動畫。
ms.assetid: ADF3D443-6764-40A5-AD5C-7C3053E247CB
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
ms.openlocfilehash: d5707ad441e9a3205ed52808b6203a3172d1ab48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685458"
---
# <a name="idcompositionmatrixtransformsetmatrixelement-methods"></a><span data-ttu-id="ea9f3-104">IDCompositionMatrixTransform：： SetMatrixElement 方法</span><span class="sxs-lookup"><span data-stu-id="ea9f3-104">IDCompositionMatrixTransform::SetMatrixElement methods</span></span>

<span data-ttu-id="ea9f3-105">變更或繪製此2D 轉換之矩陣的某個元素值的動畫。</span><span class="sxs-lookup"><span data-stu-id="ea9f3-105">Changes or animates the value of one element of the matrix of this 2D transform.</span></span>

### <a name="overload-list"></a><span data-ttu-id="ea9f3-106">多載清單</span><span class="sxs-lookup"><span data-stu-id="ea9f3-106">Overload list</span></span>



| <span data-ttu-id="ea9f3-107">方法</span><span class="sxs-lookup"><span data-stu-id="ea9f3-107">Method</span></span>                                                                                                                               | <span data-ttu-id="ea9f3-108">描述</span><span class="sxs-lookup"><span data-stu-id="ea9f3-108">Description</span></span>                                                                      |
|:-------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------|
| <span data-ttu-id="ea9f3-109">[**SetMatrixElement (int，int，float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrixelement(int_int_float))</span><span class="sxs-lookup"><span data-stu-id="ea9f3-109">[**SetMatrixElement(int, int, float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionmatrixtransform-setmatrixelement(int_int_float))</span></span>                                           | <span data-ttu-id="ea9f3-110">變更這個2D 轉換之矩陣的一個元素值。</span><span class="sxs-lookup"><span data-stu-id="ea9f3-110">Changes the value of one element of the matrix of this 2D transform.</span></span><br/>  |
| [<span data-ttu-id="ea9f3-111">**SetMatrixElement (int，int，IDCompositionAnimation \*)**</span><span class="sxs-lookup"><span data-stu-id="ea9f3-111">**SetMatrixElement(int, int, IDCompositionAnimation\*)**</span></span>](idcompositionmatrixtransform-setmatrixelement-idcompositionanimation.md) | <span data-ttu-id="ea9f3-112">將這個2D 轉換之矩陣的某個元素值繪製成動畫。</span><span class="sxs-lookup"><span data-stu-id="ea9f3-112">Animates the value of one element of the matrix of this 2D transform.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="ea9f3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea9f3-113">Requirements</span></span>



| <span data-ttu-id="ea9f3-114">需求</span><span class="sxs-lookup"><span data-stu-id="ea9f3-114">Requirement</span></span> | <span data-ttu-id="ea9f3-115">值</span><span class="sxs-lookup"><span data-stu-id="ea9f3-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ea9f3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea9f3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ea9f3-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea9f3-117">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="ea9f3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea9f3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ea9f3-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea9f3-119">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ea9f3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ea9f3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea9f3-121"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea9f3-121"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="ea9f3-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="ea9f3-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="ea9f3-123"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ea9f3-123"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="ea9f3-124">DLL</span><span class="sxs-lookup"><span data-stu-id="ea9f3-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea9f3-125"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea9f3-125"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea9f3-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ea9f3-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea9f3-127">**IDCompositionMatrixTransform**</span><span class="sxs-lookup"><span data-stu-id="ea9f3-127">**IDCompositionMatrixTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionmatrixtransform)
</dt> </dl>

<span data-ttu-id="ea9f3-128">�</span><span class="sxs-lookup"><span data-stu-id="ea9f3-128">�</span></span>

<span data-ttu-id="ea9f3-129">�</span><span class="sxs-lookup"><span data-stu-id="ea9f3-129">�</span></span>
