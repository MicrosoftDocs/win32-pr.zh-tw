---
title: 'IDCompositionSkewTransform SetCenterY 方法 (Dcomp .h) '
description: 變更或繪製2D 扭曲轉換之 CenterY 屬性值的動畫。
ms.assetid: D3F5E009-D6D2-431F-AC5C-C14C0AE1CD36
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
ms.openlocfilehash: 1b66953c8aa7d99a2a416e135f060001758a9ee0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935021"
---
# <a name="idcompositionskewtransformsetcentery-methods"></a><span data-ttu-id="6010b-104">IDCompositionSkewTransform：： SetCenterY 方法</span><span class="sxs-lookup"><span data-stu-id="6010b-104">IDCompositionSkewTransform::SetCenterY methods</span></span>

<span data-ttu-id="6010b-105">變更或繪製2D 扭曲轉換之 CenterY 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="6010b-105">Changes or animates the value of the CenterY property of a of a 2D skew transform.</span></span> <span data-ttu-id="6010b-106">CenterY 屬性會指定執行扭曲的點的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="6010b-106">The CenterY property specifies the y-coordinate of the point about which the skew is performed.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6010b-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="6010b-107">Overload list</span></span>



| <span data-ttu-id="6010b-108">方法</span><span class="sxs-lookup"><span data-stu-id="6010b-108">Method</span></span>                                                                                                       | <span data-ttu-id="6010b-109">描述</span><span class="sxs-lookup"><span data-stu-id="6010b-109">Description</span></span>                                            |
|:-------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| <span data-ttu-id="6010b-110">[**SetCenterY (float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionskewtransform-setcentery(float))</span><span class="sxs-lookup"><span data-stu-id="6010b-110">[**SetCenterY(float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionskewtransform-setcentery(float))</span></span>                                     | <span data-ttu-id="6010b-111">變更 CenterY 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="6010b-111">Changes the value of the CenterY property.</span></span><br/>  |
| <span data-ttu-id="6010b-112">[**SetCenterY (IDCompositionAnimation \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionskewtransform-setcentery(idcompositionanimation))</span><span class="sxs-lookup"><span data-stu-id="6010b-112">[**SetCenterY(IDCompositionAnimation\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionskewtransform-setcentery(idcompositionanimation))</span></span> | <span data-ttu-id="6010b-113">繪製 CenterY 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="6010b-113">Animates the value of the CenterY property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="6010b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6010b-114">Requirements</span></span>



| <span data-ttu-id="6010b-115">需求</span><span class="sxs-lookup"><span data-stu-id="6010b-115">Requirement</span></span> | <span data-ttu-id="6010b-116">值</span><span class="sxs-lookup"><span data-stu-id="6010b-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6010b-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6010b-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6010b-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6010b-118">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6010b-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6010b-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6010b-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6010b-120">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6010b-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6010b-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6010b-122"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6010b-122"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6010b-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="6010b-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="6010b-124"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6010b-124"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="6010b-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6010b-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6010b-126"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6010b-126"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6010b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6010b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6010b-128">**IDCompositionSkewTransform**</span><span class="sxs-lookup"><span data-stu-id="6010b-128">**IDCompositionSkewTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionskewtransform)
</dt> </dl>

<span data-ttu-id="6010b-129">�</span><span class="sxs-lookup"><span data-stu-id="6010b-129">�</span></span>

<span data-ttu-id="6010b-130">�</span><span class="sxs-lookup"><span data-stu-id="6010b-130">�</span></span>
