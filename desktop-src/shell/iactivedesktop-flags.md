---
description: 本節描述 IActiveDesktop 介面方法所使用的旗標。
title: 'IActiveDesktop 旗標 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 6d1a2f69-0730-4805-8b50-071332ff7070
api_name:
- AD_APPLY_ALL
- AD_APPLY_BUFFERED_REFRESH
- AD_APPLY_DYNAMICREFRESH
- AD_APPLY_FORCE
- AD_APPLY_HTMLGEN
- AD_APPLY_REFRESH
- AD_APPLY_SAVE
- COMP_ELEM_ALL
- COMP_ELEM_CHECKED
- COMP_ELEM_CURITEMSTATE
- COMP_ELEM_FRIENDLYNAME
- COMP_ELEM_NOSCROLL
- COMP_ELEM_ORIGINAL_CSI
- COMP_ELEM_POS_LEFT
- COMP_ELEM_POS_TOP
- COMP_ELEM_POS_ZINDEX
- COMP_ELEM_RESTORED_CSI
- COMP_ELEM_SIZE_HEIGHT
- COMP_ELEM_SIZE_WIDTH
- COMP_ELEM_SOURCE
- COMP_ELEM_TYPE
- COMP_TYPE_CFHTML
- COMP_TYPE_CONTROL
- COMP_TYPE_HTMLDOC
- COMP_TYPE_MAX
- COMP_TYPE_PICTURE
- COMP_TYPE_WEBSITE
- COMPONENT_TOP
- WPSTYLE_CENTER
- WPSTYLE_MAX
- WPSTYLE_STRETCH
- WPSTYLE_TILE
- WPSTYLE_SPAN
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: dae164c696ae54963f802a6ddd5cb1f6862b2f14
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "104974837"
---
# <a name="iactivedesktop-flags"></a><span data-ttu-id="332f6-103">IActiveDesktop 旗標</span><span class="sxs-lookup"><span data-stu-id="332f6-103">IActiveDesktop Flags</span></span>

<span data-ttu-id="332f6-104">本節描述 [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) 介面方法所使用的旗標。</span><span class="sxs-lookup"><span data-stu-id="332f6-104">This section describes the flags used by [**IActiveDesktop**](/windows/win32/api/shlobj_core/nn-shlobj_core-iactivedesktop) interface methods.</span></span>

<dl> <dt>

<span data-ttu-id="332f6-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD \_ \_ 全部套用**</span><span class="sxs-lookup"><span data-stu-id="332f6-105"><span id="AD_APPLY_ALL"></span><span id="ad_apply_all"></span>**AD\_APPLY\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-106">\* \* \* \* AD \_ apply \_ SAVE \* \* \* *、* \* \* \* ad apply \_ \_ HTMLGEN \* \* \* \* 和 \* \* \* \* ad \_ apply REFRESH \* \* \* \_ \* 值的匯總。</span><span class="sxs-lookup"><span data-stu-id="332f6-106">Aggregate of the \*\*\*\*AD\_APPLY\_SAVE\*\*\*\*, \*\*\*\*AD\_APPLY\_HTMLGEN\*\*\*\*, and \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD 套用緩衝的重新整理 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="332f6-107"><span id="AD_APPLY_BUFFERED_REFRESH"></span><span id="ad_apply_buffered_refresh"></span>**AD\_APPLY\_BUFFERED\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-108">啟動計時器，並將在該時間間隔內使用此旗標所做的所有重新整理要求匯總成單一重新整理。</span><span class="sxs-lookup"><span data-stu-id="332f6-108">Starts a timer and aggregates all the refresh requests made with this flag during that time interval into a single refresh.</span></span> <span data-ttu-id="332f6-109">此間隔設定為5秒。</span><span class="sxs-lookup"><span data-stu-id="332f6-109">This interval is set at five seconds.</span></span> <span data-ttu-id="332f6-110">At the end of the interval, or if a refresh is requested during the interval without an \*\*\*\*AD\_APPLY\_BUFFERED\_REFRESH\*\*\*\* flag, the refresh is made and the timer is stopped.</span><span class="sxs-lookup"><span data-stu-id="332f6-110">At the end of the interval, or if a refresh is requested during the interval without an \*\*\*\*AD\_APPLY\_BUFFERED\_REFRESH\*\*\*\* flag, the refresh is made and the timer is stopped.</span></span> <span data-ttu-id="332f6-111">此旗標必須與 \* \* \* \* AD \_ APPLY REFRESH \* \* \* 旗標合併 \_ 。</span><span class="sxs-lookup"><span data-stu-id="332f6-111">This flag must be combined with the \*\*\*\*AD\_APPLY\_REFRESH\*\*\*\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD \_ APPLY \_ DYNAMICREFRESH**</span><span class="sxs-lookup"><span data-stu-id="332f6-112"><span id="AD_APPLY_DYNAMICREFRESH"></span><span id="ad_apply_dynamicrefresh"></span>**AD\_APPLY\_DYNAMICREFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-113">[版本 5.0](versions.md)。</span><span class="sxs-lookup"><span data-stu-id="332f6-113">[Version 5.0](versions.md).</span></span> <span data-ttu-id="332f6-114">使用動態 HTML，只重新整理自上次重新整理之後變更的專案，而不是整個桌面。</span><span class="sxs-lookup"><span data-stu-id="332f6-114">Use dynamic HTML to refresh only those items that have changed since the last refresh, not the entire desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD \_ APPLY \_ FORCE**</span><span class="sxs-lookup"><span data-stu-id="332f6-115"><span id="AD_APPLY_FORCE"></span><span id="ad_apply_force"></span>**AD\_APPLY\_FORCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-116">強制 Active Desktop 變更。</span><span class="sxs-lookup"><span data-stu-id="332f6-116">Force an Active Desktop change.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD \_ APPLY \_ HTMLGEN**</span><span class="sxs-lookup"><span data-stu-id="332f6-117"><span id="AD_APPLY_HTMLGEN"></span><span id="ad_apply_htmlgen"></span>**AD\_APPLY\_HTMLGEN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-118">重新產生桌面 HTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="332f6-118">Regenerate the desktop HTML file.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD \_ APPLY \_ REFRESH**</span><span class="sxs-lookup"><span data-stu-id="332f6-119"><span id="AD_APPLY_REFRESH"></span><span id="ad_apply_refresh"></span>**AD\_APPLY\_REFRESH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-120">重新整理桌面專案。</span><span class="sxs-lookup"><span data-stu-id="332f6-120">Refresh the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD \_ 套用 \_ 儲存**</span><span class="sxs-lookup"><span data-stu-id="332f6-121"><span id="AD_APPLY_SAVE"></span><span id="ad_apply_save"></span>**AD\_APPLY\_SAVE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-122">儲存桌面專案。</span><span class="sxs-lookup"><span data-stu-id="332f6-122">Save the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP \_ ELEM \_ ALL**</span><span class="sxs-lookup"><span data-stu-id="332f6-123"><span id="COMP_ELEM_ALL"></span><span id="comp_elem_all"></span>**COMP\_ELEM\_ALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-124">複合 \_ ELEM 值的匯總 \_ \* 。</span><span class="sxs-lookup"><span data-stu-id="332f6-124">Aggregate of the COMP\_ELEM\_\* values.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**\_ \_ 已檢查的複合 ELEM**</span><span class="sxs-lookup"><span data-stu-id="332f6-125"><span id="COMP_ELEM_CHECKED"></span><span id="comp_elem_checked"></span>**COMP\_ELEM\_CHECKED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-126">已核取此專案。</span><span class="sxs-lookup"><span data-stu-id="332f6-126">The item has been checked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP \_ ELEM \_ CURITEMSTATE**</span><span class="sxs-lookup"><span data-stu-id="332f6-127"><span id="COMP_ELEM_CURITEMSTATE"></span><span id="comp_elem_curitemstate"></span>**COMP\_ELEM\_CURITEMSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-128">桌面專案的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="332f6-128">The current state of the desktop item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP \_ ELEM \_ FRIENDLYNAME**</span><span class="sxs-lookup"><span data-stu-id="332f6-129"><span id="COMP_ELEM_FRIENDLYNAME"></span><span id="comp_elem_friendlyname"></span>**COMP\_ELEM\_FRIENDLYNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-130">專案的易記名稱。</span><span class="sxs-lookup"><span data-stu-id="332f6-130">The friendly name of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP \_ ELEM \_ NOSCROLL**</span><span class="sxs-lookup"><span data-stu-id="332f6-131"><span id="COMP_ELEM_NOSCROLL"></span><span id="comp_elem_noscroll"></span>**COMP\_ELEM\_NOSCROLL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-132">專案不可滾動。</span><span class="sxs-lookup"><span data-stu-id="332f6-132">The item is not scrollable.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP \_ ELEM \_ 原始 \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="332f6-133"><span id="COMP_ELEM_ORIGINAL_CSI"></span><span id="comp_elem_original_csi"></span>**COMP\_ELEM\_ORIGINAL\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-134">原始桌面專案狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="332f6-134">The original desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP \_ ELEM \_ POS \_ 左方**</span><span class="sxs-lookup"><span data-stu-id="332f6-135"><span id="COMP_ELEM_POS_LEFT"></span><span id="comp_elem_pos_left"></span>**COMP\_ELEM\_POS\_LEFT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-136">專案的水準位置。</span><span class="sxs-lookup"><span data-stu-id="332f6-136">The horizontal position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP \_ ELEM \_ POS \_ TOP**</span><span class="sxs-lookup"><span data-stu-id="332f6-137"><span id="COMP_ELEM_POS_TOP"></span><span id="comp_elem_pos_top"></span>**COMP\_ELEM\_POS\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-138">專案的垂直位置。</span><span class="sxs-lookup"><span data-stu-id="332f6-138">The vertical position of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP \_ ELEM \_ POS \_ ZINDEX**</span><span class="sxs-lookup"><span data-stu-id="332f6-139"><span id="COMP_ELEM_POS_ZINDEX"></span><span id="comp_elem_pos_zindex"></span>**COMP\_ELEM\_POS\_ZINDEX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-140">專案的 z-索引。</span><span class="sxs-lookup"><span data-stu-id="332f6-140">The z-index of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP \_ ELEM \_ 還原的 \_ CSI**</span><span class="sxs-lookup"><span data-stu-id="332f6-141"><span id="COMP_ELEM_RESTORED_CSI"></span><span id="comp_elem_restored_csi"></span>**COMP\_ELEM\_RESTORED\_CSI**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-142">還原的桌面專案狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="332f6-142">The restored desktop item state information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**COMP \_ ELEM \_ 大小 \_ 高度**</span><span class="sxs-lookup"><span data-stu-id="332f6-143"><span id="COMP_ELEM_SIZE_HEIGHT"></span><span id="comp_elem_size_height"></span>**COMP\_ELEM\_SIZE\_HEIGHT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-144">項目的高度。</span><span class="sxs-lookup"><span data-stu-id="332f6-144">The height of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**COMP \_ ELEM \_ 大小 \_ 寬度**</span><span class="sxs-lookup"><span data-stu-id="332f6-145"><span id="COMP_ELEM_SIZE_WIDTH"></span><span id="comp_elem_size_width"></span>**COMP\_ELEM\_SIZE\_WIDTH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-146">項目的寬度。</span><span class="sxs-lookup"><span data-stu-id="332f6-146">The width of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP \_ ELEM \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="332f6-147"><span id="COMP_ELEM_SOURCE"></span><span id="comp_elem_source"></span>**COMP\_ELEM\_SOURCE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-148">專案的原始來源。</span><span class="sxs-lookup"><span data-stu-id="332f6-148">The original source of the item.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP \_ ELEM \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="332f6-149"><span id="COMP_ELEM_TYPE"></span><span id="comp_elem_type"></span>**COMP\_ELEM\_TYPE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-150">項目類型。</span><span class="sxs-lookup"><span data-stu-id="332f6-150">The item type.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**複合 \_ 類型 \_ CFHTML**</span><span class="sxs-lookup"><span data-stu-id="332f6-151"><span id="COMP_TYPE_CFHTML"></span><span id="comp_type_cfhtml"></span>**COMP\_TYPE\_CFHTML**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-152">壓縮格式的 HTML。</span><span class="sxs-lookup"><span data-stu-id="332f6-152">Compressed format HTML.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP \_ 類型 \_ 控制項**</span><span class="sxs-lookup"><span data-stu-id="332f6-153"><span id="COMP_TYPE_CONTROL"></span><span id="comp_type_control"></span>**COMP\_TYPE\_CONTROL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-154">專案是控制項。</span><span class="sxs-lookup"><span data-stu-id="332f6-154">The item is a control.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**複合 \_ 類型 \_ HTMLDOC**</span><span class="sxs-lookup"><span data-stu-id="332f6-155"><span id="COMP_TYPE_HTMLDOC"></span><span id="comp_type_htmldoc"></span>**COMP\_TYPE\_HTMLDOC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-156">專案是 HTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="332f6-156">The item is an HTML document.</span></span> <span data-ttu-id="332f6-157">只有在絕對必要時，才應該使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="332f6-157">This flag should only be used when absolutely necessary.</span></span> <span data-ttu-id="332f6-158">它會讓 HTML 檔案逐字插入 htt 檔案，用來控制桌面的版面配置。</span><span class="sxs-lookup"><span data-stu-id="332f6-158">It causes an HTML document to be inserted verbatim into the Desktop.htt file used to control layout of the desktop.</span></span> <span data-ttu-id="332f6-159">For most cases, you should use the \*\*\*\*COMP\_TYPE\_WEBSITE\*\*\*\* flag to add items to the desktop.</span><span class="sxs-lookup"><span data-stu-id="332f6-159">For most cases, you should use the \*\*\*\*COMP\_TYPE\_WEBSITE\*\*\*\* flag to add items to the desktop.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**\_ \_ 最大的複合類型**</span><span class="sxs-lookup"><span data-stu-id="332f6-160"><span id="COMP_TYPE_MAX"></span><span id="comp_type_max"></span>**COMP\_TYPE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-161">複合類型旗標的最大值 \_ \_ \* 。</span><span class="sxs-lookup"><span data-stu-id="332f6-161">The maximum value of a COMP\_TYPE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**複合 \_ 類型 \_ 圖片**</span><span class="sxs-lookup"><span data-stu-id="332f6-162"><span id="COMP_TYPE_PICTURE"></span><span id="comp_type_picture"></span>**COMP\_TYPE\_PICTURE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-163">專案是一張圖片。</span><span class="sxs-lookup"><span data-stu-id="332f6-163">The item is a picture.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**COMP \_ 類型 \_ 網站**</span><span class="sxs-lookup"><span data-stu-id="332f6-164"><span id="COMP_TYPE_WEBSITE"></span><span id="comp_type_website"></span>**COMP\_TYPE\_WEBSITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-165">專案是網站。</span><span class="sxs-lookup"><span data-stu-id="332f6-165">The item is a website.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**元件 \_ TOP**</span><span class="sxs-lookup"><span data-stu-id="332f6-166"><span id="COMPONENT_TOP"></span><span id="component_top"></span>**COMPONENT\_TOP**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-167">Z 順序值，表示專案位於頂端。</span><span class="sxs-lookup"><span data-stu-id="332f6-167">A z-order value meaning the item is at the top.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE \_ 中心**</span><span class="sxs-lookup"><span data-stu-id="332f6-168"><span id="WPSTYLE_CENTER"></span><span id="wpstyle_center"></span>**WPSTYLE\_CENTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-169">背景圖樣的中心。</span><span class="sxs-lookup"><span data-stu-id="332f6-169">The wallpaper is centered.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE \_ MAX**</span><span class="sxs-lookup"><span data-stu-id="332f6-170"><span id="WPSTYLE_MAX"></span><span id="wpstyle_max"></span>**WPSTYLE\_MAX**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-171">WPSTYLE 旗標的最大值 \_ \* 。</span><span class="sxs-lookup"><span data-stu-id="332f6-171">The maximum value of a WPSTYLE\_\* flag.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE \_ STRETCH**</span><span class="sxs-lookup"><span data-stu-id="332f6-172"><span id="WPSTYLE_STRETCH"></span><span id="wpstyle_stretch"></span>**WPSTYLE\_STRETCH**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-173">背景圖樣會伸展以容納整個螢幕。</span><span class="sxs-lookup"><span data-stu-id="332f6-173">The wallpaper is stretched to fit the entire screen.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**WPSTYLE \_ 圖格**</span><span class="sxs-lookup"><span data-stu-id="332f6-174"><span id="WPSTYLE_TILE"></span><span id="wpstyle_tile"></span>**WPSTYLE\_TILE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-175">背景圖樣會並排顯示。</span><span class="sxs-lookup"><span data-stu-id="332f6-175">The wallpaper is tiled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="332f6-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE \_ 範圍**</span><span class="sxs-lookup"><span data-stu-id="332f6-176"><span id="WPSTYLE_SPAN"></span><span id="wpstyle_span"></span>**WPSTYLE\_SPAN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="332f6-177">**Windows 8 和更新版本**：背景圖樣橫跨多個監視器。</span><span class="sxs-lookup"><span data-stu-id="332f6-177">**Windows 8 and later**: The wallpaper spans multiple monitors.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="332f6-178">規格需求</span><span class="sxs-lookup"><span data-stu-id="332f6-178">Requirements</span></span>



| <span data-ttu-id="332f6-179">需求</span><span class="sxs-lookup"><span data-stu-id="332f6-179">Requirement</span></span> | <span data-ttu-id="332f6-180">值</span><span class="sxs-lookup"><span data-stu-id="332f6-180">Value</span></span> |
|-------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="332f6-181">標頭</span><span class="sxs-lookup"><span data-stu-id="332f6-181">Header</span></span><br/> | <dl> <span data-ttu-id="332f6-182"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="332f6-182"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
