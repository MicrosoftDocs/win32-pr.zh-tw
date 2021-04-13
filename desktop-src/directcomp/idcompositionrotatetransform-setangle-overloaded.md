---
title: 'IDCompositionRotateTransform SetAngle 方法 (Dcomp .h) '
description: 變更或繪製旋轉轉換之 Angle 屬性值的動畫。 Angle 屬性指定旋轉角度（以度為單位）。 預設值為零。
ms.assetid: 8AE92567-B5A3-47A2-A652-4D777F62019D
keywords:
- SetAngle 方法 DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: 4b2451f5c1616be6a910d182eb0b856e5aeee9a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465505"
---
# <a name="idcompositionrotatetransformsetangle-methods"></a><span data-ttu-id="a74fd-106">IDCompositionRotateTransform：： SetAngle 方法</span><span class="sxs-lookup"><span data-stu-id="a74fd-106">IDCompositionRotateTransform::SetAngle methods</span></span>

<span data-ttu-id="a74fd-107">變更或繪製旋轉轉換之 Angle 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="a74fd-107">Changes or animates the value of the Angle property of a rotation transform.</span></span> <span data-ttu-id="a74fd-108">Angle 屬性指定旋轉角度（以度為單位）。</span><span class="sxs-lookup"><span data-stu-id="a74fd-108">The Angle property specifies the rotation angle, in degrees.</span></span> <span data-ttu-id="a74fd-109">預設值為零。</span><span class="sxs-lookup"><span data-stu-id="a74fd-109">The default value is zero.</span></span>

### <a name="overload-list"></a><span data-ttu-id="a74fd-110">多載清單</span><span class="sxs-lookup"><span data-stu-id="a74fd-110">Overload list</span></span>



| <span data-ttu-id="a74fd-111">方法</span><span class="sxs-lookup"><span data-stu-id="a74fd-111">Method</span></span>                                                                                                     | <span data-ttu-id="a74fd-112">描述</span><span class="sxs-lookup"><span data-stu-id="a74fd-112">Description</span></span>                                          |
|:-----------------------------------------------------------------------------------------------------------|:-----------------------------------------------------|
| <span data-ttu-id="a74fd-113">[**SetAngle (float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform-setangle(float))</span><span class="sxs-lookup"><span data-stu-id="a74fd-113">[**SetAngle(float)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform-setangle(float))</span></span>                                     | <span data-ttu-id="a74fd-114">變更 Angle 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="a74fd-114">Changes the value of the Angle property.</span></span><br/>  |
| <span data-ttu-id="a74fd-115">[**SetAngle (IDCompositionAnimation \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform-setangle(idcompositionanimation))</span><span class="sxs-lookup"><span data-stu-id="a74fd-115">[**SetAngle(IDCompositionAnimation\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionrotatetransform-setangle(idcompositionanimation))</span></span> | <span data-ttu-id="a74fd-116">繪製 Angle 屬性值的動畫。</span><span class="sxs-lookup"><span data-stu-id="a74fd-116">Animates the value of the Angle property.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="a74fd-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="a74fd-117">Requirements</span></span>



| <span data-ttu-id="a74fd-118">需求</span><span class="sxs-lookup"><span data-stu-id="a74fd-118">Requirement</span></span> | <span data-ttu-id="a74fd-119">值</span><span class="sxs-lookup"><span data-stu-id="a74fd-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a74fd-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a74fd-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a74fd-121">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a74fd-121">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a74fd-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a74fd-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a74fd-123">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a74fd-123">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a74fd-124">標頭</span><span class="sxs-lookup"><span data-stu-id="a74fd-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="a74fd-125"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="a74fd-125"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="a74fd-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="a74fd-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="a74fd-127"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a74fd-127"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="a74fd-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a74fd-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a74fd-129"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a74fd-129"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a74fd-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a74fd-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74fd-131">**IDCompositionRotateTransform**</span><span class="sxs-lookup"><span data-stu-id="a74fd-131">**IDCompositionRotateTransform**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionrotatetransform)
</dt> </dl>

<span data-ttu-id="a74fd-132">�</span><span class="sxs-lookup"><span data-stu-id="a74fd-132">�</span></span>

<span data-ttu-id="a74fd-133">�</span><span class="sxs-lookup"><span data-stu-id="a74fd-133">�</span></span>
