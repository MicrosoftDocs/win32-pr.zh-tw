---
title: 通用控制項版本
description: 本主題列出通用控制項程式庫 (ComCtl32.dll) 的可用版本，說明如何識別您應用程式所使用的版本，並說明如何以特定版本的應用程式為目標。
ms.assetid: 1B524A91-B433-4968-9546-8A6AFB67E89C
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1131466bd4d3afcaae3a241a6f7854fd5a49450
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423958"
---
# <a name="common-control-versions"></a><span data-ttu-id="f5d60-103">通用控制項版本</span><span class="sxs-lookup"><span data-stu-id="f5d60-103">Common Control Versions</span></span>

<span data-ttu-id="f5d60-104">本主題列出通用控制項程式庫 (ComCtl32.dll) 的可用版本，說明如何識別您應用程式所使用的版本，並說明如何以特定版本的應用程式為目標。</span><span class="sxs-lookup"><span data-stu-id="f5d60-104">This topic lists the available versions of the Common Control library (ComCtl32.dll), describes how to identify the version that your application is using, and explains how to target your application for a specific version.</span></span>

<span data-ttu-id="f5d60-105">本主題包含下列各節。</span><span class="sxs-lookup"><span data-stu-id="f5d60-105">This topic contains the following sections.</span></span>

-   [<span data-ttu-id="f5d60-106">通用控制項 DLL 版本號碼</span><span class="sxs-lookup"><span data-stu-id="f5d60-106">Common Control DLL Versions Numbers</span></span>](#common-control-dll-versions-numbers)
-   [<span data-ttu-id="f5d60-107">不同通用控制項版本的結構大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-107">Structure Sizes for Different Common Control Versions</span></span>](#structure-sizes-for-different-common-control-versions)
-   [<span data-ttu-id="f5d60-108">使用 DllGetVersion 來判斷版本號碼</span><span class="sxs-lookup"><span data-stu-id="f5d60-108">Using DllGetVersion to Determine the Version Number</span></span>](#using-dllgetversion-to-determine-the-version-number)
-   [<span data-ttu-id="f5d60-109">專案版本</span><span class="sxs-lookup"><span data-stu-id="f5d60-109">Project Versions</span></span>](#project-versions)
-   [<span data-ttu-id="f5d60-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5d60-110">Related topics</span></span>](#related-topics)

## <a name="common-control-dll-versions-numbers"></a><span data-ttu-id="f5d60-111">通用控制項 DLL 版本號碼</span><span class="sxs-lookup"><span data-stu-id="f5d60-111">Common Control DLL Versions Numbers</span></span>

<span data-ttu-id="f5d60-112">通用控制項的支援是由 ComCtl32.dll 所提供，所有32位和64位版本的 Windows 都包含在內。</span><span class="sxs-lookup"><span data-stu-id="f5d60-112">Support for common controls is provided by ComCtl32.dll, which all 32-bit and 64-bit versions of Windows include.</span></span> <span data-ttu-id="f5d60-113">每個後續版本的 DLL 都支援舊版的功能和 API，並加入新功能。</span><span class="sxs-lookup"><span data-stu-id="f5d60-113">Each successive version of the DLL supports the features and API of earlier versions and adds new features.</span></span>

<span data-ttu-id="f5d60-114">因為不同版本的 ComCtl32.dll 是隨著 Internet Explorer 散發，所以作用中的版本有時會與作業系統隨附的版本不同。</span><span class="sxs-lookup"><span data-stu-id="f5d60-114">Because various versions of ComCtl32.dll were distributed with Internet Explorer, the version that is active is sometimes different from the version that was shipped with the operating system.</span></span> <span data-ttu-id="f5d60-115">因此，您的應用程式必須直接判斷存在的 ComCtl32.dll 版本。</span><span class="sxs-lookup"><span data-stu-id="f5d60-115">Therefore, your application must directly determine which version of ComCtl32.dll is present.</span></span>

<span data-ttu-id="f5d60-116">在通用控制項參考檔中，許多程式設計專案會指定支援的最低 DLL 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="f5d60-116">In the common controls reference documentation, many programming elements specify a minimum supported DLL version number.</span></span> <span data-ttu-id="f5d60-117">此版本號碼表示程式設計專案會在該版本和後續 DLL 版本中執行，除非另有指定。</span><span class="sxs-lookup"><span data-stu-id="f5d60-117">This version number indicates that the programming element is implemented in that version and subsequent versions of the DLL unless otherwise specified.</span></span> <span data-ttu-id="f5d60-118">如果未指定版本號碼，則會在所有現有版本的 DLL 中執行程式設計專案。</span><span class="sxs-lookup"><span data-stu-id="f5d60-118">If no version number is specified, the programming element is implemented in all existing versions of the DLL.</span></span>

<span data-ttu-id="f5d60-119">下表概述不同的 DLL 版本，以及它們在支援的作業系統上的散發方式。</span><span class="sxs-lookup"><span data-stu-id="f5d60-119">The following table outlines the different DLL versions and how they were distributed on supported OSes.</span></span>



<span data-ttu-id="f5d60-120">ComCtl32.dll</span><span class="sxs-lookup"><span data-stu-id="f5d60-120">ComCtl32.dll</span></span>

<span data-ttu-id="f5d60-121">版本</span><span class="sxs-lookup"><span data-stu-id="f5d60-121">Version</span></span>

<span data-ttu-id="f5d60-122">散發平臺</span><span class="sxs-lookup"><span data-stu-id="f5d60-122">Distribution Platform</span></span>

<span data-ttu-id="f5d60-123">5.81</span><span class="sxs-lookup"><span data-stu-id="f5d60-123">5.81</span></span>

<span data-ttu-id="f5d60-124">Microsoft Internet Explorer 5.01、Microsoft Internet Explorer 5.5 和 Microsoft Internet Explorer 6</span><span class="sxs-lookup"><span data-stu-id="f5d60-124">Microsoft Internet Explorer 5.01, Microsoft Internet Explorer 5.5, and Microsoft Internet Explorer 6</span></span>

<span data-ttu-id="f5d60-125">5.82</span><span class="sxs-lookup"><span data-stu-id="f5d60-125">5.82</span></span>

<span data-ttu-id="f5d60-126">Windows Server 2003、Windows Vista、Windows Server 2008 和 Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5d60-126">Windows Server 2003, Windows Vista, Windows Server 2008, and Windows 7</span></span>

<span data-ttu-id="f5d60-127">6.0</span><span class="sxs-lookup"><span data-stu-id="f5d60-127">6.0</span></span>

<span data-ttu-id="f5d60-128">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="f5d60-128">Windows Server 2003</span></span>

<span data-ttu-id="f5d60-129">6.10</span><span class="sxs-lookup"><span data-stu-id="f5d60-129">6.10</span></span>

<span data-ttu-id="f5d60-130">Windows Vista、Windows Server 2008 和 Windows 7</span><span class="sxs-lookup"><span data-stu-id="f5d60-130">Windows Vista, Windows Server 2008, and Windows 7</span></span>



 

## <a name="structure-sizes-for-different-common-control-versions"></a><span data-ttu-id="f5d60-131">不同通用控制項版本的結構大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-131">Structure Sizes for Different Common Control Versions</span></span>

<span data-ttu-id="f5d60-132">對通用控制項進行持續的增強，會導致需要擴充許多結構。</span><span class="sxs-lookup"><span data-stu-id="f5d60-132">Ongoing enhancements to common controls have resulted in the need to extend many of the structures.</span></span> <span data-ttu-id="f5d60-133">基於這個理由，結構的大小在不同版本的 Commctrl 之間已變更。</span><span class="sxs-lookup"><span data-stu-id="f5d60-133">For this reason, the size of the structures has changed between different versions of Commctrl.h.</span></span> <span data-ttu-id="f5d60-134">因為大部分的通用控制項結構都採用結構大小做為其中一個參數，所以如果無法辨識大小，訊息或函式可能會失敗。</span><span class="sxs-lookup"><span data-stu-id="f5d60-134">Because most of the common control structures take a structure size as one of the parameters, a message or function can fail if the size is not recognized.</span></span> <span data-ttu-id="f5d60-135">為了解決這個情況，已定義結構大小常數以協助以不同版本的 ComCtl32.dll 為目標。</span><span class="sxs-lookup"><span data-stu-id="f5d60-135">To remedy this, structure size constants have been defined to aid in targeting different version of ComCtl32.dll.</span></span> <span data-ttu-id="f5d60-136">下列清單會定義結構大小常數。</span><span class="sxs-lookup"><span data-stu-id="f5d60-136">The following list defines the structure size constants.</span></span>



|    <span data-ttu-id="f5d60-137">結構大小常數</span><span class="sxs-lookup"><span data-stu-id="f5d60-137">Structure Size Constant</span></span>                           |     <span data-ttu-id="f5d60-138">定義</span><span class="sxs-lookup"><span data-stu-id="f5d60-138">Definition</span></span>                                                                                         |
|-------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d60-139">HDITEM \_ V1 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-139">HDITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="f5d60-140">4.0 版中 [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-140">The size of the [**HDITEM**](/windows/win32/api/commctrl/ns-commctrl-hditema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="f5d60-141">IMAGELISTDRAWPARAMS \_ V3 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-141">IMAGELISTDRAWPARAMS\_V3\_SIZE</span></span> | <span data-ttu-id="f5d60-142">5.9 版中 [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-142">The size of the [**IMAGELISTDRAWPARAMS**](/windows/win32/api/commctrl/ns-commctrl-imagelistdrawparams) structure in version 5.9.</span></span> |
| <span data-ttu-id="f5d60-143">LVCOLUMN \_ V1 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-143">LVCOLUMN\_V1\_SIZE</span></span>            | <span data-ttu-id="f5d60-144">4.0 版中 [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-144">The size of the [**LVCOLUMN**](/windows/win32/api/commctrl/ns-commctrl-lvcolumna) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="f5d60-145">LVGROUP \_ V5 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-145">LVGROUP\_V5\_SIZE</span></span>             | <span data-ttu-id="f5d60-146">6.0 版中 [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-146">The size of the [**LVGROUP**](/windows/win32/api/commctrl/ns-commctrl-lvgroup) structure in version 6.0.</span></span>                         |
| <span data-ttu-id="f5d60-147">LVHITTESTINFO \_ V1 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-147">LVHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="f5d60-148">4.0 版中 [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-148">The size of the [**LVHITTESTINFO**](/windows/win32/api/commctrl/ns-commctrl-lvhittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="f5d60-149">LVITEM \_ V1 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-149">LVITEM\_V1\_SIZE</span></span>              | <span data-ttu-id="f5d60-150">4.0 版中 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-150">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 4.0.</span></span>                           |
| <span data-ttu-id="f5d60-151">LVITEM \_ V5 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-151">LVITEM\_V5\_SIZE</span></span>              | <span data-ttu-id="f5d60-152">6.0 版中 [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-152">The size of the [**LVITEM**](/windows/win32/api/commctrl/ns-commctrl-lvitema) structure in version 6.0.</span></span>                           |
| <span data-ttu-id="f5d60-153">LVTILEINFO \_ V5 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-153">LVTILEINFO\_V5\_SIZE</span></span>          | <span data-ttu-id="f5d60-154">6.0 版中 [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-154">The size of the [**LVTILEINFO**](/windows/win32/api/commctrl/ns-commctrl-lvtileinfo) structure in version 6.0.</span></span>                   |
| <span data-ttu-id="f5d60-155">MCHITTESTINFO \_ V1 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-155">MCHITTESTINFO\_V1\_SIZE</span></span>       | <span data-ttu-id="f5d60-156">4.0 版中 [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-156">The size of the [**MCHITTESTINFO**](/windows/desktop/api/Commctrl/ns-commctrl-mchittestinfo) structure in version 4.0.</span></span>             |
| <span data-ttu-id="f5d60-157">NMLVCUSTOMDRAW \_ V3 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-157">NMLVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="f5d60-158">4.7 版中 [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-158">The size of the [**NMLVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmlvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="f5d60-159">NMTTDISPINFO \_ V1 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-159">NMTTDISPINFO\_V1\_SIZE</span></span>        | <span data-ttu-id="f5d60-160">4.0 版中 [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-160">The size of the [**NMTTDISPINFO**](/windows/win32/api/commctrl/ns-commctrl-nmttdispinfoa) structure in version 4.0.</span></span>               |
| <span data-ttu-id="f5d60-161">NMTVCUSTOMDRAW \_ V3 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-161">NMTVCUSTOMDRAW\_V3\_SIZE</span></span>      | <span data-ttu-id="f5d60-162">4.7 版中 [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-162">The size of the [**NMTVCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmtvcustomdraw) structure in version 4.7.</span></span>           |
| <span data-ttu-id="f5d60-163">PROPSHEETHEADER \_ V1 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-163">PROPSHEETHEADER\_V1\_SIZE</span></span>     | <span data-ttu-id="f5d60-164">4.0 版中 [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-164">The size of the [**PROPSHEETHEADER**](/windows/desktop/api/Prsht/ns-prsht-propsheetheadera_v2) structure in version 4.0.</span></span>         |
| <span data-ttu-id="f5d60-165">PROPSHEETPAGE \_ V1 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-165">PROPSHEETPAGE\_V1\_SIZE</span></span>       | <span data-ttu-id="f5d60-166">4.0 版中 [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-166">The size of the [**PROPSHEETPAGE**](/windows/desktop/api/Prsht/ns-prsht-propsheetpagea_v2) structure in version 4.0.</span></span>             |
| <span data-ttu-id="f5d60-167">REBARBANDINFO \_ V3 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-167">REBARBANDINFO\_V3\_SIZE</span></span>       | <span data-ttu-id="f5d60-168">4.7 版中 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-168">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 4.7.</span></span>             |
| <span data-ttu-id="f5d60-169">REBARBANDINFO \_ V6 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-169">REBARBANDINFO\_V6\_SIZE</span></span>       | <span data-ttu-id="f5d60-170">6.0 版中 [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-170">The size of the [**REBARBANDINFO**](/windows/win32/api/commctrl/ns-commctrl-rebarbandinfoa) structure in version 6.0.</span></span>             |
| <span data-ttu-id="f5d60-171">TTTOOLINFO \_ V1 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-171">TTTOOLINFO\_V1\_SIZE</span></span>          | <span data-ttu-id="f5d60-172">4.0 版中 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-172">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.0.</span></span>                       |
| <span data-ttu-id="f5d60-173">TTTOOLINFO \_ V2 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-173">TTTOOLINFO\_V2\_SIZE</span></span>          | <span data-ttu-id="f5d60-174">4.7 版中 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-174">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 4.7.</span></span>                       |
| <span data-ttu-id="f5d60-175">TTTOOLINFO \_ V3 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-175">TTTOOLINFO\_V3\_SIZE</span></span>          | <span data-ttu-id="f5d60-176">6.0 版中 [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-176">The size of the [**TOOLINFO**](/windows/win32/api/commctrl/ns-commctrl-tttoolinfoa) structure in version 6.0.</span></span>                       |
| <span data-ttu-id="f5d60-177">TVINSERTSTRUCT \_ V1 \_ 大小</span><span class="sxs-lookup"><span data-stu-id="f5d60-177">TVINSERTSTRUCT\_V1\_SIZE</span></span>      | <span data-ttu-id="f5d60-178">4.0 版中 [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) 結構的大小。</span><span class="sxs-lookup"><span data-stu-id="f5d60-178">The size of the [**TVINSERTSTRUCT**](/windows/win32/api/commctrl/ns-commctrl-tvinsertstructa) structure in version 4.0.</span></span>           |



 

## <a name="using-dllgetversion-to-determine-the-version-number"></a><span data-ttu-id="f5d60-179">使用 DllGetVersion 來判斷版本號碼</span><span class="sxs-lookup"><span data-stu-id="f5d60-179">Using DllGetVersion to Determine the Version Number</span></span>

<span data-ttu-id="f5d60-180">應用程式可以呼叫 [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) 函式來判斷系統上有哪些 DLL 版本。</span><span class="sxs-lookup"><span data-stu-id="f5d60-180">The [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function can be called by an application to determine which DLL version is present on the system.</span></span>

<span data-ttu-id="f5d60-181">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) 會傳回 [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) 結構。</span><span class="sxs-lookup"><span data-stu-id="f5d60-181">[**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="f5d60-182">除了透過 [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo)提供的資訊之外， **DLLVERSIONINFO2** 也會提供可識別最新安裝 service pack 的修正程式編號，以提供更健全的方式來比較版本號碼。</span><span class="sxs-lookup"><span data-stu-id="f5d60-182">In addition to the information provided through [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo), **DLLVERSIONINFO2** also provides the hotfix number that identifies the latest installed service pack, which provides a more robust way to compare version numbers.</span></span> <span data-ttu-id="f5d60-183">由於 **DLLVERSIONINFO2** 的第一個成員是 **DLLVERSIONINFO** 結構，因此之後的結構會回溯相容。</span><span class="sxs-lookup"><span data-stu-id="f5d60-183">Because the first member of **DLLVERSIONINFO2** is a **DLLVERSIONINFO** structure, the later structure is backward-compatible.</span></span>


<span data-ttu-id="f5d60-184">下列範例函數 `GetVersion` 會載入指定的 DLL，並嘗試呼叫其 [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) 函式。</span><span class="sxs-lookup"><span data-stu-id="f5d60-184">The following sample function `GetVersion` loads a specified DLL and attempts to call its [**DllGetVersion**](/windows/desktop/api/shlwapi/nc-shlwapi-dllgetversionproc) function.</span></span> <span data-ttu-id="f5d60-185">如果成功，它會使用宏將 [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) 結構中的主要和次要版本號碼，封裝至傳回給呼叫應用程式的 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="f5d60-185">If successful, it uses a macro to pack the major and minor version numbers from the [**DLLVERSIONINFO**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo) structure into a **DWORD** that is returned to the calling application.</span></span> <span data-ttu-id="f5d60-186">如果 DLL 未匯出 **DllGetVersion**，函數會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f5d60-186">If the DLL does not export **DllGetVersion**, the function returns zero.</span></span> <span data-ttu-id="f5d60-187">您可以修改函數來處理 **DllGetVersion** 傳回 [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) 結構的可能性。</span><span class="sxs-lookup"><span data-stu-id="f5d60-187">You can modify the function to handle the possibility that **DllGetVersion** returns a [**DLLVERSIONINFO2**](/windows/desktop/api/shlwapi/ns-shlwapi-dllversioninfo2) structure.</span></span> <span data-ttu-id="f5d60-188">如果是的話，請使用該 **DLLVERSIONINFO2** 結構的 **ullVersion** 成員中的資訊來比較版本、組建編號和 service pack 版本。</span><span class="sxs-lookup"><span data-stu-id="f5d60-188">If so, use the information in that **DLLVERSIONINFO2** structure's **ullVersion** member to compare versions, build numbers, and service pack releases.</span></span> <span data-ttu-id="f5d60-189">[**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull)宏可簡化將這些值與 **ullVersion** 中的值進行比較的工作。</span><span class="sxs-lookup"><span data-stu-id="f5d60-189">The [**MAKEDLLVERULL**](/windows/desktop/api/shlwapi/nf-shlwapi-makedllverull) macro simplifies the task of comparing these values to those in **ullVersion**.</span></span>

> [!Note]  
> <span data-ttu-id="f5d60-190">不當使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 可能會造成安全性風險。</span><span class="sxs-lookup"><span data-stu-id="f5d60-190">Using [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) incorrectly can pose security risks.</span></span> <span data-ttu-id="f5d60-191">請參閱 **LoadLibrary** 檔，以取得如何使用不同版本的 Windows 正確載入 dll 的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f5d60-191">Refer to the **LoadLibrary** documentation for information on how to correctly load DLLs with different versions of Windows.</span></span>

 


```C++
#include "stdafx.h"
#include "windows.h"
#include "windef.h"
#include "winbase.h"
#include "shlwapi.h"

#define PACKVERSION(major,minor) MAKELONG(minor,major)

DWORD GetVersion(LPCTSTR lpszDllName)
{
    HINSTANCE hinstDll;
    DWORD dwVersion = 0;

    // For security purposes, LoadLibrary should be provided with a fully qualified 
    // path to the DLL. The lpszDllName variable should be tested to ensure that it 
    // is a fully qualified path before it is used. 
    hinstDll = LoadLibrary(lpszDllName);
    
    if(hinstDll)
    {
        DLLGETVERSIONPROC pDllGetVersion;
        pDllGetVersion = (DLLGETVERSIONPROC)GetProcAddress(hinstDll, "DllGetVersion");

        // Because some DLLs might not implement this function, you must test for 
        // it explicitly. Depending on the particular DLL, the lack of a DllGetVersion 
        // function can be a useful indicator of the version. 

        if(pDllGetVersion)
        {
            DLLVERSIONINFO dvi;
            HRESULT hr;

            ZeroMemory(&dvi, sizeof(dvi));
            dvi.info1.cbSize = sizeof(dvi);

            hr = (*pDllGetVersion)(&dvi);

            if(SUCCEEDED(hr))
            {
               dwVersion = PACKVERSION(dvi.info1.dwMajorVersion, dvi.info1.dwMinorVersion);
            }
        }
        FreeLibrary(hinstDll);
    }
    return dwVersion;
}
```



<span data-ttu-id="f5d60-192">下列程式碼範例會示範如何使用 `GetVersion` 來測試 ComCtl32.dll 是否為6.0 版或更新版本。</span><span class="sxs-lookup"><span data-stu-id="f5d60-192">The following code example shows how you can use `GetVersion` to test whether ComCtl32.dll is version 6.0 or later.</span></span>


```C++
LPCTSTR lpszDllName = L"C:\\Windows\\System32\\ComCtl32.dll";
DWORD dwVer = GetVersion(lpszDllName);
DWORD dwTarget = PACKVERSION(6,0);

if(dwVer >= dwTarget)
{
    // This version of ComCtl32.dll is version 6.0 or later.
}
else
{
    // Proceed knowing that version 6.0 or later additions are not available.
    // Use an alternate approach for older the DLL version.
}
```



## <a name="project-versions"></a><span data-ttu-id="f5d60-193">專案版本</span><span class="sxs-lookup"><span data-stu-id="f5d60-193">Project Versions</span></span>

<span data-ttu-id="f5d60-194">為了確保您的應用程式與 .dll 檔案的不同目標版本相容，版本宏會出現在標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="f5d60-194">To ensure that your application is compatible with different targeted versions of a .dll file, version macros are present in the header files.</span></span> <span data-ttu-id="f5d60-195">這些宏可用來定義、排除或重新定義不同版本 DLL 的特定定義。</span><span class="sxs-lookup"><span data-stu-id="f5d60-195">These macros are used to define, exclude, or redefine certain definitions for different versions of the DLL.</span></span> <span data-ttu-id="f5d60-196">如需這些宏的深入說明，請參閱 [使用 Windows 標頭](/windows/desktop/WinProg/using-the-windows-headers) 。</span><span class="sxs-lookup"><span data-stu-id="f5d60-196">See [Using the Windows Headers](/windows/desktop/WinProg/using-the-windows-headers) for an in-depth description of these macros.</span></span>

<span data-ttu-id="f5d60-197">例如，宏名稱 **\_ WIN32 \_ IE** 通常會在較舊的標頭中找到。</span><span class="sxs-lookup"><span data-stu-id="f5d60-197">For example, the macro name **\_WIN32\_IE** is commonly found in older headers.</span></span> <span data-ttu-id="f5d60-198">您必須負責將巨集定義為十六進位數位。</span><span class="sxs-lookup"><span data-stu-id="f5d60-198">You are responsible for defining the macro as a hexadecimal number.</span></span> <span data-ttu-id="f5d60-199">此版本號碼會定義使用 DLL 的應用程式目標版本。</span><span class="sxs-lookup"><span data-stu-id="f5d60-199">This version number defines the target version of the application that is using the DLL.</span></span> <span data-ttu-id="f5d60-200">下表顯示可用的版本號碼，以及每一個應用程式的效果。</span><span class="sxs-lookup"><span data-stu-id="f5d60-200">The following table shows the available version numbers and the effect each has on your application.</span></span>



| <span data-ttu-id="f5d60-201">版本</span><span class="sxs-lookup"><span data-stu-id="f5d60-201">Version</span></span> | <span data-ttu-id="f5d60-202">描述</span><span class="sxs-lookup"><span data-stu-id="f5d60-202">Description</span></span>                                                                                                                                           |
|---------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5d60-203">0x0300</span><span class="sxs-lookup"><span data-stu-id="f5d60-203">0x0300</span></span>  | <span data-ttu-id="f5d60-204">應用程式與 ComCtl32.dll 4.70 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="f5d60-204">The application is compatible with ComCtl32.dll version 4.70 and later.</span></span> <span data-ttu-id="f5d60-205">應用程式無法執行4.70 版之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="f5d60-205">The application cannot implement features that were added after version 4.70.</span></span> |
| <span data-ttu-id="f5d60-206">0x0400</span><span class="sxs-lookup"><span data-stu-id="f5d60-206">0x0400</span></span>  | <span data-ttu-id="f5d60-207">應用程式與 ComCtl32.dll 4.71 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="f5d60-207">The application is compatible with ComCtl32.dll version 4.71 and later.</span></span> <span data-ttu-id="f5d60-208">應用程式無法執行4.71 版之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="f5d60-208">The application cannot implement features that were added after version 4.71.</span></span> |
| <span data-ttu-id="f5d60-209">0x0401</span><span class="sxs-lookup"><span data-stu-id="f5d60-209">0x0401</span></span>  | <span data-ttu-id="f5d60-210">應用程式與 ComCtl32.dll 4.72 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="f5d60-210">The application is compatible with ComCtl32.dll version 4.72 and later.</span></span> <span data-ttu-id="f5d60-211">應用程式無法執行4.72 版之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="f5d60-211">The application cannot implement features that were added after version 4.72.</span></span> |
| <span data-ttu-id="f5d60-212">0x0500</span><span class="sxs-lookup"><span data-stu-id="f5d60-212">0x0500</span></span>  | <span data-ttu-id="f5d60-213">應用程式與 ComCtl32.dll 5.80 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="f5d60-213">The application is compatible with ComCtl32.dll version 5.80 and later.</span></span> <span data-ttu-id="f5d60-214">應用程式無法執行5.80 版之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="f5d60-214">The application cannot implement features that were added after version 5.80.</span></span> |
| <span data-ttu-id="f5d60-215">0x0501</span><span class="sxs-lookup"><span data-stu-id="f5d60-215">0x0501</span></span>  | <span data-ttu-id="f5d60-216">應用程式與 ComCtl32.dll 5.81 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="f5d60-216">The application is compatible with ComCtl32.dll version 5.81 and later.</span></span> <span data-ttu-id="f5d60-217">應用程式無法執行5.81 版之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="f5d60-217">The application cannot implement features that were added after version 5.81.</span></span> |
| <span data-ttu-id="f5d60-218">0x0600</span><span class="sxs-lookup"><span data-stu-id="f5d60-218">0x0600</span></span>  | <span data-ttu-id="f5d60-219">應用程式與 ComCtl32.dll 6.0 版和更新版本相容。</span><span class="sxs-lookup"><span data-stu-id="f5d60-219">The application is compatible with ComCtl32.dll version 6.0 and later.</span></span> <span data-ttu-id="f5d60-220">應用程式無法執行6.0 版之後加入的功能。</span><span class="sxs-lookup"><span data-stu-id="f5d60-220">The application cannot implement features that were added after version 6.0.</span></span>   |



 

<span data-ttu-id="f5d60-221">如果您未在專案中定義 **\_ WIN32 \_ IE** 宏，則會自動將其定義為0x0500。</span><span class="sxs-lookup"><span data-stu-id="f5d60-221">If you do not define the **\_WIN32\_IE** macro in your project, it is automatically defined as 0x0500.</span></span> <span data-ttu-id="f5d60-222">若要定義不同的值，您可以將下列程式檔加入至 make 檔案中的編譯器指示詞。以所需的0x0400 版本號碼取代。</span><span class="sxs-lookup"><span data-stu-id="f5d60-222">To define a different value, you can add the following to the compiler directives in your make file; substitute the desired version number for 0x0400.</span></span>


```C++
/D _WIN32_IE=0x0400
```



<span data-ttu-id="f5d60-223">另一種方法是在包含 Shell 標頭檔之前，在原始程式碼中加入類似下列的程式程式碼。</span><span class="sxs-lookup"><span data-stu-id="f5d60-223">Another method is to add a line similar to the following in your source code before you include the Shell header files.</span></span> <span data-ttu-id="f5d60-224">以所需的0x0400 版本號碼取代。</span><span class="sxs-lookup"><span data-stu-id="f5d60-224">Substitute the desired version number for 0x0400.</span></span>


```C++
#define _WIN32_IE 0x0400
#include <commctrl.h>
```



## <a name="related-topics"></a><span data-ttu-id="f5d60-225">相關主題</span><span class="sxs-lookup"><span data-stu-id="f5d60-225">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5d60-226">關於通用控制項</span><span class="sxs-lookup"><span data-stu-id="f5d60-226">About Common Controls</span></span>](common-controls-intro.md)
</dt> </dl>

 

 