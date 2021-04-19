---
title: 控制函數
description: 控制函數
ms.assetid: 9774a320-1d00-48a4-ba13-fb1cd683a635
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7099afab5c035e394eafc30c4475dbe6bc97cec5
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106988569"
---
# <a name="control-functions"></a><span data-ttu-id="91a68-103">控制函數</span><span class="sxs-lookup"><span data-stu-id="91a68-103">Control Functions</span></span>

## <a name="in-this-section"></a><span data-ttu-id="91a68-104">本節內容</span><span class="sxs-lookup"><span data-stu-id="91a68-104">In This Section</span></span>

-   [<span data-ttu-id="91a68-105">**DoReaderMode**</span><span class="sxs-lookup"><span data-stu-id="91a68-105">**DoReaderMode**</span></span>](doreadermode.md)
-   [<span data-ttu-id="91a68-106">**DPA \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="91a68-106">**DPA\_Clone**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_clone)
-   [<span data-ttu-id="91a68-107">**DPA \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="91a68-107">**DPA\_Create**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_create)
-   [<span data-ttu-id="91a68-108">**DPA \_ CreateEx**</span><span class="sxs-lookup"><span data-stu-id="91a68-108">**DPA\_CreateEx**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_createex)
-   [<span data-ttu-id="91a68-109">**DPA \_ DeleteAllPtrs**</span><span class="sxs-lookup"><span data-stu-id="91a68-109">**DPA\_DeleteAllPtrs**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_deleteallptrs)
-   [<span data-ttu-id="91a68-110">**DPA \_ DeletePtr**</span><span class="sxs-lookup"><span data-stu-id="91a68-110">**DPA\_DeletePtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_deleteptr)
-   [<span data-ttu-id="91a68-111">**DPA 損 \_ 毀**</span><span class="sxs-lookup"><span data-stu-id="91a68-111">**DPA\_Destroy**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_destroy)
-   [<span data-ttu-id="91a68-112">**DPA \_ DestroyCallback**</span><span class="sxs-lookup"><span data-stu-id="91a68-112">**DPA\_DestroyCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_destroycallback)
-   [<span data-ttu-id="91a68-113">**DPA \_ EnumCallback**</span><span class="sxs-lookup"><span data-stu-id="91a68-113">**DPA\_EnumCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_enumcallback)
-   [<span data-ttu-id="91a68-114">**DPA \_ GetPtr**</span><span class="sxs-lookup"><span data-stu-id="91a68-114">**DPA\_GetPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getptr)
-   [<span data-ttu-id="91a68-115">**DPA \_ GetPtrIndex**</span><span class="sxs-lookup"><span data-stu-id="91a68-115">**DPA\_GetPtrIndex**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getptrindex)
-   [<span data-ttu-id="91a68-116">**DPA \_ GetSize**</span><span class="sxs-lookup"><span data-stu-id="91a68-116">**DPA\_GetSize**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_getsize)
-   [<span data-ttu-id="91a68-117">**DPA \_ 成長**</span><span class="sxs-lookup"><span data-stu-id="91a68-117">**DPA\_Grow**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_grow)
-   [<span data-ttu-id="91a68-118">**DPA \_ InsertPtr**</span><span class="sxs-lookup"><span data-stu-id="91a68-118">**DPA\_InsertPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_insertptr)
-   [<span data-ttu-id="91a68-119">**DPA \_ LoadStream**</span><span class="sxs-lookup"><span data-stu-id="91a68-119">**DPA\_LoadStream**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_loadstream)
-   [<span data-ttu-id="91a68-120">**DPA \_ 合併**</span><span class="sxs-lookup"><span data-stu-id="91a68-120">**DPA\_Merge**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_merge)
-   [<span data-ttu-id="91a68-121">**DPA \_ SaveStream**</span><span class="sxs-lookup"><span data-stu-id="91a68-121">**DPA\_SaveStream**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_savestream)
-   [<span data-ttu-id="91a68-122">**DPA \_ 搜尋**</span><span class="sxs-lookup"><span data-stu-id="91a68-122">**DPA\_Search**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_search)
-   [<span data-ttu-id="91a68-123">**DPA \_ SetPtr**</span><span class="sxs-lookup"><span data-stu-id="91a68-123">**DPA\_SetPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_setptr)
-   [<span data-ttu-id="91a68-124">**DPA \_ 排序**</span><span class="sxs-lookup"><span data-stu-id="91a68-124">**DPA\_Sort**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dpa_sort)
-   [<span data-ttu-id="91a68-125">**DrawShadowText**</span><span class="sxs-lookup"><span data-stu-id="91a68-125">**DrawShadowText**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-drawshadowtext)
-   [<span data-ttu-id="91a68-126">**DrawTextExPrivWrap**</span><span class="sxs-lookup"><span data-stu-id="91a68-126">**DrawTextExPrivWrap**</span></span>](drawtextexprivwrap.md)
-   [<span data-ttu-id="91a68-127">**DrawTextWrap**</span><span class="sxs-lookup"><span data-stu-id="91a68-127">**DrawTextWrap**</span></span>](drawtextwrap.md)
-   [<span data-ttu-id="91a68-128">**DSA \_ 複製**</span><span class="sxs-lookup"><span data-stu-id="91a68-128">**DSA\_Clone**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_clone)
-   [<span data-ttu-id="91a68-129">**DSA \_ 建立**</span><span class="sxs-lookup"><span data-stu-id="91a68-129">**DSA\_Create**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_create)
-   [<span data-ttu-id="91a68-130">**DSA \_ DeleteAllItems**</span><span class="sxs-lookup"><span data-stu-id="91a68-130">**DSA\_DeleteAllItems**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_deleteallitems)
-   [<span data-ttu-id="91a68-131">**DSA \_ DeleteItem**</span><span class="sxs-lookup"><span data-stu-id="91a68-131">**DSA\_DeleteItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_deleteitem)
-   [<span data-ttu-id="91a68-132">**DSA 損 \_ 毀**</span><span class="sxs-lookup"><span data-stu-id="91a68-132">**DSA\_Destroy**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_destroy)
-   [<span data-ttu-id="91a68-133">**DSA \_ DestroyCallback**</span><span class="sxs-lookup"><span data-stu-id="91a68-133">**DSA\_DestroyCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_destroycallback)
-   [<span data-ttu-id="91a68-134">**DSA \_ EnumCallback**</span><span class="sxs-lookup"><span data-stu-id="91a68-134">**DSA\_EnumCallback**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_enumcallback)
-   [<span data-ttu-id="91a68-135">**DSA \_ GetItem**</span><span class="sxs-lookup"><span data-stu-id="91a68-135">**DSA\_GetItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getitem)
-   [<span data-ttu-id="91a68-136">**DSA \_ GetItemPtr**</span><span class="sxs-lookup"><span data-stu-id="91a68-136">**DSA\_GetItemPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getitemptr)
-   [<span data-ttu-id="91a68-137">**DSA \_ GetSize**</span><span class="sxs-lookup"><span data-stu-id="91a68-137">**DSA\_GetSize**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_getsize)
-   [<span data-ttu-id="91a68-138">**DSA \_ InsertItem**</span><span class="sxs-lookup"><span data-stu-id="91a68-138">**DSA\_InsertItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_insertitem)
-   [<span data-ttu-id="91a68-139">**DSA \_ SetItem**</span><span class="sxs-lookup"><span data-stu-id="91a68-139">**DSA\_SetItem**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_setitem)
-   [<span data-ttu-id="91a68-140">**DSA \_ 排序**</span><span class="sxs-lookup"><span data-stu-id="91a68-140">**DSA\_Sort**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-dsa_sort)
-   [<span data-ttu-id="91a68-141">**ExtTextOutWrap**</span><span class="sxs-lookup"><span data-stu-id="91a68-141">**ExtTextOutWrap**</span></span>](exttextoutwrap.md)
-   [<span data-ttu-id="91a68-142">**GetEffectiveClientRect**</span><span class="sxs-lookup"><span data-stu-id="91a68-142">**GetEffectiveClientRect**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-geteffectiveclientrect)
-   [<span data-ttu-id="91a68-143">**GetMUILanguage**</span><span class="sxs-lookup"><span data-stu-id="91a68-143">**GetMUILanguage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-getmuilanguage)
-   [<span data-ttu-id="91a68-144">**GetTextExtentPoint32Wrap**</span><span class="sxs-lookup"><span data-stu-id="91a68-144">**GetTextExtentPoint32Wrap**</span></span>](gettextextentpoint32wrap.md)
-   [<span data-ttu-id="91a68-145">**函式**</span><span class="sxs-lookup"><span data-stu-id="91a68-145">**InitCommonControls**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrols)
-   [<span data-ttu-id="91a68-146">**InitCommonControlsEx**</span><span class="sxs-lookup"><span data-stu-id="91a68-146">**InitCommonControlsEx**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-initcommoncontrolsex)
-   [<span data-ttu-id="91a68-147">**InitMUILanguage**</span><span class="sxs-lookup"><span data-stu-id="91a68-147">**InitMUILanguage**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-initmuilanguage)
-   [<span data-ttu-id="91a68-148">**LoadIconMetric**</span><span class="sxs-lookup"><span data-stu-id="91a68-148">**LoadIconMetric**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-loadiconmetric)
-   [<span data-ttu-id="91a68-149">**LoadIconWithScaleDown**</span><span class="sxs-lookup"><span data-stu-id="91a68-149">**LoadIconWithScaleDown**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-loadiconwithscaledown)
-   [<span data-ttu-id="91a68-150">**MirrorIcon**</span><span class="sxs-lookup"><span data-stu-id="91a68-150">**MirrorIcon**</span></span>](mirroricon.md)
-   [<span data-ttu-id="91a68-151">**PFNDACOMPARE**</span><span class="sxs-lookup"><span data-stu-id="91a68-151">**PFNDACOMPARE**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompare)
-   [<span data-ttu-id="91a68-152">**PFNDACOMPARECONST**</span><span class="sxs-lookup"><span data-stu-id="91a68-152">**PFNDACOMPARECONST**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndacompareconst)
-   [<span data-ttu-id="91a68-153">**PFNDAENUMCALLBACK**</span><span class="sxs-lookup"><span data-stu-id="91a68-153">**PFNDAENUMCALLBACK**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallback)
-   [<span data-ttu-id="91a68-154">**PFNDAENUMCALLBACKCONST**</span><span class="sxs-lookup"><span data-stu-id="91a68-154">**PFNDAENUMCALLBACKCONST**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndaenumcallbackconst)
-   <span data-ttu-id="91a68-155">[**PFNDPACOMPARE**](/previous-versions/windows/desktop/legacy/bb775715(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91a68-155">[**PFNDPACOMPARE**](/previous-versions/windows/desktop/legacy/bb775715(v=vs.85))</span></span>
-   <span data-ttu-id="91a68-156">[**PFNDPACOMPARECONST**](/previous-versions/windows/desktop/legacy/bb775717(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91a68-156">[**PFNDPACOMPARECONST**](/previous-versions/windows/desktop/legacy/bb775717(v=vs.85))</span></span>
-   <span data-ttu-id="91a68-157">[**PFNDPAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775719(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91a68-157">[**PFNDPAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775719(v=vs.85))</span></span>
-   [<span data-ttu-id="91a68-158">**PFNDPAMERGE**</span><span class="sxs-lookup"><span data-stu-id="91a68-158">**PFNDPAMERGE**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamerge)
-   [<span data-ttu-id="91a68-159">**PFNDPAMERGECONST**</span><span class="sxs-lookup"><span data-stu-id="91a68-159">**PFNDPAMERGECONST**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpamergeconst)
-   [<span data-ttu-id="91a68-160">**PFNDPASTREAM**</span><span class="sxs-lookup"><span data-stu-id="91a68-160">**PFNDPASTREAM**</span></span>](/windows/desktop/api/dpa_dsa/nc-dpa_dsa-pfndpastream)
-   <span data-ttu-id="91a68-161">[**PFNDSAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775727(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="91a68-161">[**PFNDSAENUMCALLBACK**](/previous-versions/windows/desktop/legacy/bb775727(v=vs.85))</span></span>
-   [<span data-ttu-id="91a68-162">**ReaderScroll**</span><span class="sxs-lookup"><span data-stu-id="91a68-162">**ReaderScroll**</span></span>](readerscroll.md)
-   [<span data-ttu-id="91a68-163">**ShowHideMenuCtl**</span><span class="sxs-lookup"><span data-stu-id="91a68-163">**ShowHideMenuCtl**</span></span>](/windows/desktop/api/Commctrl/nf-commctrl-showhidemenuctl)
-   [<span data-ttu-id="91a68-164">**Str \_ GetPtr**</span><span class="sxs-lookup"><span data-stu-id="91a68-164">**Str\_GetPtr**</span></span>](str-getptr.md)
-   [<span data-ttu-id="91a68-165">**Str \_ SetPtr**</span><span class="sxs-lookup"><span data-stu-id="91a68-165">**Str\_SetPtr**</span></span>](/windows/desktop/api/dpa_dsa/nf-dpa_dsa-str_setptrw)
-   [<span data-ttu-id="91a68-166">**TranslateDispatch**</span><span class="sxs-lookup"><span data-stu-id="91a68-166">**TranslateDispatch**</span></span>](translatedispatch.md)

 

 
