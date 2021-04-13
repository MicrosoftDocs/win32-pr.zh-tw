---
title: 'IDCompositionScaleTransform SetScaleX 方法 (Dcomp .h) '
description: 變更或繪製2D 縮放轉換之 ScaleX 屬性值的動畫。
ms.assetid: 114C4907-280C-4060-9157-30E0E8989251
keywords:
- SetScaleX 方法 DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 33c5e250015d09f578a3e5aa4a7a880b3da3fdc0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509319"
---
# <a name="idcompositionscaletransformsetscalex-methods"></a><span data-ttu-id="1ce9d-104">IDCompositionScaleTransform：： SetScaleX 方法</span><span class="sxs-lookup"><span data-stu-id="1ce9d-104">IDCompositionScaleTransform::SetScaleX methods</span></span>

<span data-ttu-id="1ce9d-105">變更或繪製2D 縮放轉換之 ScaleX 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="1ce9d-105">Changes or animates the value of the ScaleX property of a 2D scale transform.</span></span> <span data-ttu-id="1ce9d-106">ScaleX 屬性會指定沿著 X 軸的縮放比例。</span><span class="sxs-lookup"><span data-stu-id="1ce9d-106">The ScaleX property specifies the scale factor along the x-axis.</span></span>

### <a name="overload-list"></a><span data-ttu-id="1ce9d-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="1ce9d-107">Overload list</span></span>



| <span data-ttu-id="1ce9d-108">方法</span><span class="sxs-lookup"><span data-stu-id="1ce9d-108">Method</span></span>                                                                                                      | <span data-ttu-id="1ce9d-109">描述</span><span class="sxs-lookup"><span data-stu-id="1ce9d-109">Description</span></span>                                           |
|:------------------------------------------------------------------------------------------------------------|:------------------------------------------------------|
| <span data-ttu-id="1ce9d-110">[**SetScaleX (float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setscalex(float))</span><span class="sxs-lookup"><span data-stu-id="1ce9d-110">[**SetScaleX(float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setscalex(float))</span></span>                                     | <span data-ttu-id="1ce9d-111">變更 ScaleX 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="1ce9d-111">Changes the value of the ScaleX property.</span></span><br/>  |
| <span data-ttu-id="1ce9d-112">[**SetScaleX (IDCompositionAnimation \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setscalex(idcompositionanimation))</span><span class="sxs-lookup"><span data-stu-id="1ce9d-112">[**SetScaleX(IDCompositionAnimation\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setscalex(idcompositionanimation))</span></span> | <span data-ttu-id="1ce9d-113">將 ScaleX 屬性的值繪製成動畫。</span><span class="sxs-lookup"><span data-stu-id="1ce9d-113">Animates the value of the ScaleX property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="1ce9d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ce9d-114">Requirements</span></span>



| <span data-ttu-id="1ce9d-115">需求</span><span class="sxs-lookup"><span data-stu-id="1ce9d-115">Requirement</span></span> | <span data-ttu-id="1ce9d-116">值</span><span class="sxs-lookup"><span data-stu-id="1ce9d-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce9d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ce9d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce9d-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ce9d-118">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="1ce9d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ce9d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce9d-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ce9d-120">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1ce9d-121">標頭</span><span class="sxs-lookup"><span data-stu-id="1ce9d-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="1ce9d-122"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="1ce9d-122"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="1ce9d-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="1ce9d-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="1ce9d-124"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1ce9d-124"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="1ce9d-125">DLL</span><span class="sxs-lookup"><span data-stu-id="1ce9d-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ce9d-126"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ce9d-126"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ce9d-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ce9d-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce9d-128">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="1ce9d-128">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

<span data-ttu-id="1ce9d-129">[**IDCompositionScaleTransform::SetScaleY**](/previous-versions/windows/desktop/legacy/hh449055(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1ce9d-129">[**IDCompositionScaleTransform::SetScaleY**](/previous-versions/windows/desktop/legacy/hh449055(v=vs.85))</span></span>
</dt> </dl>

<span data-ttu-id="1ce9d-130">�</span><span class="sxs-lookup"><span data-stu-id="1ce9d-130">�</span></span>

<span data-ttu-id="1ce9d-131">�</span><span class="sxs-lookup"><span data-stu-id="1ce9d-131">�</span></span>
