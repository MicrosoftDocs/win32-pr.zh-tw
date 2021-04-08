---
title: 'IDCompositionVisual SetClip 方法 (Dcomp .h) '
description: 將此視覺效果的 [剪切] 屬性設定為指定的 [矩形區域] 或 [剪切] 物件。
ms.assetid: ACEBA4F9-E1B0-459B-8DC2-272A822AB214
keywords:
- SetClip 方法 DirectComposition
topic_type:
- apiref
api_location:
- Dcomp.dll
api_type:
- DllExport
ms.date: 07/02/2019
ms.topic: reference
ms.openlocfilehash: e421c916d305b95029bb6ffd8328346b4ea36918
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686385"
---
# <a name="idcompositionvisualsetclip-methods"></a><span data-ttu-id="6c850-104">IDCompositionVisual：： SetClip 方法</span><span class="sxs-lookup"><span data-stu-id="6c850-104">IDCompositionVisual::SetClip methods</span></span>

<span data-ttu-id="6c850-105">將此視覺效果的 [剪切] 屬性設定為指定的 [矩形區域] 或 [剪切] 物件。</span><span class="sxs-lookup"><span data-stu-id="6c850-105">Sets the Clip property of this visual to the specified rectangular region or clip object.</span></span> <span data-ttu-id="6c850-106">剪輯屬性會將此視覺效果根目錄的視覺化子樹轉譯，限制為矩形區域。</span><span class="sxs-lookup"><span data-stu-id="6c850-106">The Clip property restricts the rendering of the visual subtree that is rooted at this visual to a rectangular region.</span></span>

### <a name="overload-list"></a><span data-ttu-id="6c850-107">多載清單</span><span class="sxs-lookup"><span data-stu-id="6c850-107">Overload list</span></span>



| <span data-ttu-id="6c850-108">方法</span><span class="sxs-lookup"><span data-stu-id="6c850-108">Method</span></span>                                                                                | <span data-ttu-id="6c850-109">描述</span><span class="sxs-lookup"><span data-stu-id="6c850-109">Description</span></span>                                                            |
|:--------------------------------------------------------------------------------------|:-----------------------------------------------------------------------|
| <span data-ttu-id="6c850-110">[**SetClip (常數 D2D \_ RECT \_ F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span><span class="sxs-lookup"><span data-stu-id="6c850-110">[**SetClip(const D2D\_RECT\_F&)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(constd2d_rect_f_))</span></span> | <span data-ttu-id="6c850-111">將剪輯屬性設定為指定的矩形區域。</span><span class="sxs-lookup"><span data-stu-id="6c850-111">Sets the Clip property to the specified rectangular region.</span></span><br/> |
| <span data-ttu-id="6c850-112">[**SetClip (IDCompositionClip \*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span><span class="sxs-lookup"><span data-stu-id="6c850-112">[**SetClip(IDCompositionClip\*)**](/windows/win32/api/dcomp/nf-dcomp-idcompositionvisual-setclip(idcompositionclip))</span></span> | <span data-ttu-id="6c850-113">將剪輯屬性設定為指定的剪切物件。</span><span class="sxs-lookup"><span data-stu-id="6c850-113">Sets the Clip property to the specified clip object.</span></span><br/>        |



## <a name="requirements"></a><span data-ttu-id="6c850-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c850-114">Requirements</span></span>



| <span data-ttu-id="6c850-115">需求</span><span class="sxs-lookup"><span data-stu-id="6c850-115">Requirement</span></span> | <span data-ttu-id="6c850-116">值</span><span class="sxs-lookup"><span data-stu-id="6c850-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="6c850-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c850-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6c850-118">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c850-118">Windows�8 \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="6c850-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c850-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6c850-120">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c850-120">Windows Server�2012 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="6c850-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6c850-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c850-122"><dt>Dcomp。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c850-122"><dt>Dcomp.h</dt></span></span> </dl>   |
| <span data-ttu-id="6c850-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c850-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c850-124"><dt>Dcomp .lib</dt></span><span class="sxs-lookup"><span data-stu-id="6c850-124"><dt>Dcomp.lib</dt></span></span> </dl> |
| <span data-ttu-id="6c850-125">DLL</span><span class="sxs-lookup"><span data-stu-id="6c850-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6c850-126"><dt>Dcomp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c850-126"><dt>Dcomp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c850-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c850-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c850-128">裁剪</span><span class="sxs-lookup"><span data-stu-id="6c850-128">Clipping</span></span>](clipping.md)
</dt> <dt>

[<span data-ttu-id="6c850-129">**IDCompositionVisual**</span><span class="sxs-lookup"><span data-stu-id="6c850-129">**IDCompositionVisual**</span></span>](/windows/win32/api/dcomp/nn-dcomp-idcompositionvisual)
</dt> </dl>

<span data-ttu-id="6c850-130">�</span><span class="sxs-lookup"><span data-stu-id="6c850-130">�</span></span>

<span data-ttu-id="6c850-131">�</span><span class="sxs-lookup"><span data-stu-id="6c850-131">�</span></span>
