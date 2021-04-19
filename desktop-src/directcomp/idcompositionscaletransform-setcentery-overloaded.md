---
title: 'IDCompositionScaleTransform SetCenterY 方法 (Dcomp .h) '
description: 變更或繪製2D 縮放轉換之 CenterY 屬性值的動畫。
ms.assetid: 18A755E6-C6E8-437C-BBB5-58F36F754BE7
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
ms.openlocfilehash: 9b39df7d5452f5046ff6bb20b72946c2aa7d556f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969820"
---
# <a name="idcompositionscaletransformsetcentery-methods"></a><span data-ttu-id="cd9fb-104">IDCompositionScaleTransform：： SetCenterY 方法</span><span class="sxs-lookup"><span data-stu-id="cd9fb-104">IDCompositionScaleTransform::SetCenterY methods</span></span>

<span data-ttu-id="cd9fb-105">變更或繪製2D 縮放轉換之 CenterY 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="cd9fb-105">Changes or animates the value of the CenterY property of a 2D scale transform.</span></span> <span data-ttu-id="cd9fb-106">CenterY 屬性會指定執行調整的起點的 y 座標。</span><span class="sxs-lookup"><span data-stu-id="cd9fb-106">The CenterY property specifies the y-coordinate of the point about which scaling is performed.</span></span>

### <a name="overload-list"></a><span data-ttu-id="cd9fb-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="cd9fb-107">Overload list</span></span>



| <span data-ttu-id="cd9fb-108">方法</span><span class="sxs-lookup"><span data-stu-id="cd9fb-108">Method</span></span>                                                                                                        | <span data-ttu-id="cd9fb-109">描述</span><span class="sxs-lookup"><span data-stu-id="cd9fb-109">Description</span></span>                                            |
|:--------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------|
| <span data-ttu-id="cd9fb-110">[**SetCenterY (float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setcentery(float))</span><span class="sxs-lookup"><span data-stu-id="cd9fb-110">[**SetCenterY(float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setcentery(float))</span></span>                                     | <span data-ttu-id="cd9fb-111">變更 CenterY 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="cd9fb-111">Changes the value of the CenterY property.</span></span><br/>  |
| <span data-ttu-id="cd9fb-112">[**SetCenterY (IDCompositionAnimation \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setcentery(idcompositionanimation))</span><span class="sxs-lookup"><span data-stu-id="cd9fb-112">[**SetCenterY(IDCompositionAnimation\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionscaletransform-setcentery(idcompositionanimation))</span></span> | <span data-ttu-id="cd9fb-113">繪製 CenterY 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="cd9fb-113">Animates the value of the CenterY property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="cd9fb-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="cd9fb-114">Requirements</span></span>



| <span data-ttu-id="cd9fb-115">需求</span><span class="sxs-lookup"><span data-stu-id="cd9fb-115">Requirement</span></span> | <span data-ttu-id="cd9fb-116">值</span><span class="sxs-lookup"><span data-stu-id="cd9fb-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cd9fb-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cd9fb-117">Minimum supported client</span></span><br/> | <span data-ttu-id="cd9fb-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd9fb-118">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="cd9fb-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cd9fb-119">Minimum supported server</span></span><br/> | <span data-ttu-id="cd9fb-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cd9fb-120">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="cd9fb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="cd9fb-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="cd9fb-122"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="cd9fb-122"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="cd9fb-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="cd9fb-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="cd9fb-124"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="cd9fb-124"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="cd9fb-125">DLL</span><span class="sxs-lookup"><span data-stu-id="cd9fb-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cd9fb-126"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cd9fb-126"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cd9fb-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cd9fb-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cd9fb-128">**IDCompositionScaleTransform**</span><span class="sxs-lookup"><span data-stu-id="cd9fb-128">**IDCompositionScaleTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionscaletransform)
</dt> <dt>

[<span data-ttu-id="cd9fb-129">**IDCompositionScaleTransform::SetCenterX**</span><span class="sxs-lookup"><span data-stu-id="cd9fb-129">**IDCompositionScaleTransform::SetCenterX**</span></span>](idcompositionscaletransform-setcenterx-overloaded.md)
</dt> </dl>

<span data-ttu-id="cd9fb-130">�</span><span class="sxs-lookup"><span data-stu-id="cd9fb-130">�</span></span>

<span data-ttu-id="cd9fb-131">�</span><span class="sxs-lookup"><span data-stu-id="cd9fb-131">�</span></span>
