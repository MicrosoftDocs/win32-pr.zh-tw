---
title: 關於 Windows Vista 的平臺更新
description: 概述適用于 Windows Vista 的平臺更新，以及 Windows Server 2008 和其功能的平臺更新。
ms.assetid: ec5f03ae-9454-4964-943f-f97821984254
keywords:
- Windows Server 2008 的平臺更新
- Windows Vista 的平臺更新
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b2bcd3e94f8784ce3d060a8e56c0b089a065d288
ms.sourcegitcommit: 7b8f6151ebe247536304866459b2973276271d4d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/06/2021
ms.locfileid: "106998963"
---
# <a name="about-platform-update-for-windows-vista"></a><span data-ttu-id="76430-105">關於 Windows Vista 的平臺更新</span><span class="sxs-lookup"><span data-stu-id="76430-105">About Platform Update for Windows Vista</span></span>

<span data-ttu-id="76430-106">適用于 Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新為終端使用者作業系統更新，可支援在舊版 Windows 作業系統上使用所選的 Windows 7 技術。</span><span class="sxs-lookup"><span data-stu-id="76430-106">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 are end-user operating system updates that support the use of selected Windows 7 technologies on previous versions of the Windows operating system.</span></span> <span data-ttu-id="76430-107">這些更新包含一組執行時間程式庫，可讓應用程式開發人員以目前的版本、Windows 7 和 Windows Server 2008 R2，以及舊版、Windows Vista 和 Windows Server 2008 為目標。</span><span class="sxs-lookup"><span data-stu-id="76430-107">The updates include a set of runtime libraries that enable application developers to target current releases, Windows 7 and Windows Server 2008 R2 as well as previous versions, Windows Vista and Windows Server 2008.</span></span>

## <a name="summary-of-supported-api-by-technology"></a><span data-ttu-id="76430-108">支援的 API （依技術）摘要</span><span class="sxs-lookup"><span data-stu-id="76430-108">Summary of Supported API by Technology</span></span>

<span data-ttu-id="76430-109">適用于 Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新所支援的每一種技術，都包含一組 API，可用於以舊版 Windows 為目標的應用程式。</span><span class="sxs-lookup"><span data-stu-id="76430-109">Each technology that is supported by the Platform Update for Windows Vista and the Platform Update for Windows Server 2008 updates includes a set of API that can be used in an application that targets previous version of Windows.</span></span>

<span data-ttu-id="76430-110">如需在以舊版 Windows 為目標的應用程式中使用更新所支援之 Api 的詳細資訊，請參閱 [針對舊版 Windows 開發應用程式](developing-applications-for-previous-versions-of-windows.md)。</span><span class="sxs-lookup"><span data-stu-id="76430-110">For more information about using APIs supported by the updates in an application that targets previous versions of Windows, see [Developing Application for Previous Versions of Windows](developing-applications-for-previous-versions-of-windows.md).</span></span>

> [!Note]  
> <span data-ttu-id="76430-111">某些與技術相關聯的 Api 可能不受支援，而且某些支援的 Api 的行為、效能或需求可能會因不同的 Windows 版本而異。</span><span class="sxs-lookup"><span data-stu-id="76430-111">Some APIs that are associated with a technology may not be supported and the behavior, performance, or requirements for some supported APIs may vary across Windows versions.</span></span> <span data-ttu-id="76430-112">如需特定技術支援的 API 的詳細資訊，請按一下其中一個摘要表格中的連結，移至該技術的相關章節。</span><span class="sxs-lookup"><span data-stu-id="76430-112">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

 

### <a name="technologies-supported-with-platform-update-for-windows-vista"></a><span data-ttu-id="76430-113">適用于 Windows Vista 的平臺更新所支援的技術</span><span class="sxs-lookup"><span data-stu-id="76430-113">Technologies Supported with Platform Update for Windows Vista</span></span>

<span data-ttu-id="76430-114">如需特定技術支援的 API 的詳細資訊，請按一下其中一個摘要表格中的連結，移至該技術的相關章節。</span><span class="sxs-lookup"><span data-stu-id="76430-114">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="76430-115">下表顯示 Windows Vista 和 Windows XP 搭配 Windows Vista 平臺更新所支援的技術。</span><span class="sxs-lookup"><span data-stu-id="76430-115">The technologies that are supported for Windows Vista and Windows XP with the Platform Update for Windows Vista are shown in the following table.</span></span>

| <span data-ttu-id="76430-116">技術</span><span class="sxs-lookup"><span data-stu-id="76430-116">Technology</span></span>                                                                                    | <span data-ttu-id="76430-117">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76430-117">Windows Vista</span></span> | <span data-ttu-id="76430-118">Windows XP</span><span class="sxs-lookup"><span data-stu-id="76430-118">Windows XP</span></span> |
|-----------------------------------------------------------------------------------------------|---------------|------------|
| [<span data-ttu-id="76430-119">Windows 自動化 API</span><span class="sxs-lookup"><span data-stu-id="76430-119">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="76430-120">是</span><span class="sxs-lookup"><span data-stu-id="76430-120">Yes</span></span>           | <span data-ttu-id="76430-121">是</span><span class="sxs-lookup"><span data-stu-id="76430-121">Yes</span></span>        |
| [<span data-ttu-id="76430-122">Windows 圖形、影像處理和 XPS 程式庫</span><span class="sxs-lookup"><span data-stu-id="76430-122">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="76430-123">是</span><span class="sxs-lookup"><span data-stu-id="76430-123">Yes</span></span>           | <span data-ttu-id="76430-124">否</span><span class="sxs-lookup"><span data-stu-id="76430-124">No</span></span>         |
| [<span data-ttu-id="76430-125">Windows 功能區和動畫管理員程式庫</span><span class="sxs-lookup"><span data-stu-id="76430-125">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="76430-126">是</span><span class="sxs-lookup"><span data-stu-id="76430-126">Yes</span></span>           | <span data-ttu-id="76430-127">否</span><span class="sxs-lookup"><span data-stu-id="76430-127">No</span></span>         |
| [<span data-ttu-id="76430-128">Windows 可攜式裝置平臺</span><span class="sxs-lookup"><span data-stu-id="76430-128">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="76430-129">是</span><span class="sxs-lookup"><span data-stu-id="76430-129">Yes</span></span>           | <span data-ttu-id="76430-130">否</span><span class="sxs-lookup"><span data-stu-id="76430-130">No</span></span>         |



 

### <a name="technologies-supported-with-platform-update-for-windows-server-2008"></a><span data-ttu-id="76430-131">Windows Server 2008 平臺更新所支援的技術</span><span class="sxs-lookup"><span data-stu-id="76430-131">Technologies Supported with Platform Update for Windows Server 2008</span></span>

<span data-ttu-id="76430-132">如需特定技術支援的 API 的詳細資訊，請按一下其中一個摘要表格中的連結，移至該技術的相關章節。</span><span class="sxs-lookup"><span data-stu-id="76430-132">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

<span data-ttu-id="76430-133">下表顯示 Windows Server 2008 和 windows server 2003 搭配 Windows Server 2008 的平臺更新所支援的技術。</span><span class="sxs-lookup"><span data-stu-id="76430-133">The technologies that are supported for Windows Server 2008 and Windows Server 2003 with the Platform Update for Windows Server 2008 are shown in the following table.</span></span>

| <span data-ttu-id="76430-134">技術</span><span class="sxs-lookup"><span data-stu-id="76430-134">Technology</span></span>                                                                                    | <span data-ttu-id="76430-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76430-135">Windows Server 2008</span></span> | <span data-ttu-id="76430-136">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76430-136">Windows Server 2003</span></span> |
|-----------------------------------------------------------------------------------------------|---------------------|---------------------|
| [<span data-ttu-id="76430-137">Windows 自動化 API</span><span class="sxs-lookup"><span data-stu-id="76430-137">Windows Automation API</span></span>](#windows-automation-api)                                             | <span data-ttu-id="76430-138">是</span><span class="sxs-lookup"><span data-stu-id="76430-138">Yes</span></span>                 | <span data-ttu-id="76430-139">是</span><span class="sxs-lookup"><span data-stu-id="76430-139">Yes</span></span>                 |
| [<span data-ttu-id="76430-140">Windows 圖形、影像處理和 XPS 程式庫</span><span class="sxs-lookup"><span data-stu-id="76430-140">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)        | <span data-ttu-id="76430-141">是</span><span class="sxs-lookup"><span data-stu-id="76430-141">Yes</span></span>                 | <span data-ttu-id="76430-142">否</span><span class="sxs-lookup"><span data-stu-id="76430-142">No</span></span>                  |
| [<span data-ttu-id="76430-143">Windows 功能區和動畫管理員程式庫</span><span class="sxs-lookup"><span data-stu-id="76430-143">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library) | <span data-ttu-id="76430-144">是</span><span class="sxs-lookup"><span data-stu-id="76430-144">Yes</span></span>                 | <span data-ttu-id="76430-145">否</span><span class="sxs-lookup"><span data-stu-id="76430-145">No</span></span>                  |
| [<span data-ttu-id="76430-146">Windows 可攜式裝置平臺</span><span class="sxs-lookup"><span data-stu-id="76430-146">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)                       | <span data-ttu-id="76430-147">否</span><span class="sxs-lookup"><span data-stu-id="76430-147">No</span></span>                  | <span data-ttu-id="76430-148">否</span><span class="sxs-lookup"><span data-stu-id="76430-148">No</span></span>                  |



 

## <a name="descriptions-of-supported-api-by-technology"></a><span data-ttu-id="76430-149">依技術支援的 API 說明</span><span class="sxs-lookup"><span data-stu-id="76430-149">Descriptions of Supported API by Technology</span></span>

<span data-ttu-id="76430-150">如需特定技術支援的 API 的詳細資訊，請按一下其中一個摘要表格中的連結，移至該技術的相關章節。</span><span class="sxs-lookup"><span data-stu-id="76430-150">For details about the supported API for a specific technology, click the link in one of the summary tables to go to the section about that technology.</span></span>

-   [<span data-ttu-id="76430-151">Windows 自動化 API</span><span class="sxs-lookup"><span data-stu-id="76430-151">Windows Automation API</span></span>](#windows-automation-api)
-   [<span data-ttu-id="76430-152">Windows 圖形、影像處理和 XPS 程式庫</span><span class="sxs-lookup"><span data-stu-id="76430-152">Windows Graphics, Imaging and XPS Library</span></span>](#windows-graphics-imaging-and-xps-library)
-   [<span data-ttu-id="76430-153">Windows 功能區和動畫管理員程式庫</span><span class="sxs-lookup"><span data-stu-id="76430-153">Windows Ribbon and Animation Manager Library</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="76430-154">Windows 可攜式裝置平臺</span><span class="sxs-lookup"><span data-stu-id="76430-154">Windows Portable Devices Platform</span></span>](#windows-portable-devices-platform)

### <a name="windows-automation-api"></a><span data-ttu-id="76430-155">Windows 自動化 API</span><span class="sxs-lookup"><span data-stu-id="76430-155">Windows Automation API</span></span>

<span data-ttu-id="76430-156">Windows Automation API 3.0 是一組 Dll 和 API 元素，可在) 產品上提供輔助技術 (，以提供更好的電腦存取權給有實體或認知難題、障礙或殘障人士的個人。</span><span class="sxs-lookup"><span data-stu-id="76430-156">Windows Automation API 3.0 is a set of DLLs and API elements that enable Assistive Technology (AT) products to provide better computer access for individuals who have physical or cognitive difficulties, impairments, or disabilities.</span></span> <span data-ttu-id="76430-157">此外，由於 Windows Automation API 3.0 可讓應用程式存取和操作使用者介面 (UI) 其他應用程式的元素，因此它是執行自動化測試控管的理想技術。</span><span class="sxs-lookup"><span data-stu-id="76430-157">Additionally, because Windows Automation API 3.0 enables applications to access and manipulate the user interface (UI) elements of other applications, it is an ideal technology for implementing automated testing tools.</span></span>

<span data-ttu-id="76430-158">Microsoft Active Accessibility (MSAA) 和消費者介面自動化很類似，因為兩者都提供公開和收集使用者介面元素和控制項相關資訊的方法，以支援使用者介面協助工具和軟體測試自動化。</span><span class="sxs-lookup"><span data-stu-id="76430-158">Microsoft Active Accessibility (MSAA) and UI Automation are similar in that both provide a means for exposing and collecting information about user interface elements and controls to support user interface accessibility and software test automation.</span></span> <span data-ttu-id="76430-159">消費者介面自動化是消費者介面自動化規格的 Windows 執行。</span><span class="sxs-lookup"><span data-stu-id="76430-159">UI Automation is a Windows implementation of the UI Automation specification.</span></span> <span data-ttu-id="76430-160">它是一項較新的技術，可解決 MSAA 的許多限制。</span><span class="sxs-lookup"><span data-stu-id="76430-160">It is a newer technology that addresses many of the limitations of MSAA.</span></span>

<span data-ttu-id="76430-161">如需 Windows Automation API 3.0 的詳細資訊，請參閱 [Windows AUTOMATION api：總覽](/windows/desktop/WinAuto/windows-automation-api-overview)。</span><span class="sxs-lookup"><span data-stu-id="76430-161">For more information about the Windows Automation API 3.0, see [Windows Automation API: Overview](/windows/desktop/WinAuto/windows-automation-api-overview).</span></span>

<span data-ttu-id="76430-162">適用于 Windows Vista 的平臺更新和 Windows Server 2008 的平臺更新支援下列 Windows Automation API 3.0：</span><span class="sxs-lookup"><span data-stu-id="76430-162">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 support the following Windows Automation API 3.0:</span></span>

-   [<span data-ttu-id="76430-163">Microsoft Active Accessibility (MSAA) </span><span class="sxs-lookup"><span data-stu-id="76430-163">Microsoft Active Accessibility (MSAA)</span></span>](#microsoft-active-accessibility-msaa)
-   [<span data-ttu-id="76430-164">使用者介面自動化</span><span class="sxs-lookup"><span data-stu-id="76430-164">UI Automation</span></span>](#ui-automation)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="76430-165">適用于更新的 Windows 版本</span><span class="sxs-lookup"><span data-stu-id="76430-165">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="76430-166">適用于 windows Vista 的平臺更新和 Windows Server 2008 的平臺更新，會在下表所示的 Windows 版本上啟用 Windows 自動化 API 3.0 支援。</span><span class="sxs-lookup"><span data-stu-id="76430-166">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Automation API 3.0 support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="76430-167">Windows 版本</span><span class="sxs-lookup"><span data-stu-id="76430-167">Windows Version</span></span></th>
<th><span data-ttu-id="76430-168">適用于 Update 的版本</span><span class="sxs-lookup"><span data-stu-id="76430-168">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76430-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76430-169">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="76430-170">使用 SP2 的 Starter (x86) </span><span class="sxs-lookup"><span data-stu-id="76430-170">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="76430-171">Home Basic SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-171">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-172">Home Premium SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-172">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-173">使用 SP2 (x86 和 amd64) 的企業</span><span class="sxs-lookup"><span data-stu-id="76430-173">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-174">Enterprise SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-174">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-175">SP2 (x86 和 amd64) 的終極</span><span class="sxs-lookup"><span data-stu-id="76430-175">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76430-176">Windows XP</span><span class="sxs-lookup"><span data-stu-id="76430-176">Windows XP</span></span></td>
<td><dl> <span data-ttu-id="76430-177">Windows XP Home SP3 (x86) </span><span class="sxs-lookup"><span data-stu-id="76430-177">Windows XP Home with SP3 (x86)</span></span><br />
<span data-ttu-id="76430-178">Windows XP Professional SP3 (x86) </span><span class="sxs-lookup"><span data-stu-id="76430-178">Windows XP Professional with SP3 (x86)</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="76430-179">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76430-179">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="76430-180">Windows Server 2008 SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-180">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76430-181">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="76430-181">Windows Server 2003</span></span></td>
<td><dl> <span data-ttu-id="76430-182">Windows Server 2003 SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-182">Windows Server 2003 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="microsoft-active-accessibility-msaa"></a><span data-ttu-id="76430-183">Microsoft Active Accessibility (MSAA) </span><span class="sxs-lookup"><span data-stu-id="76430-183">Microsoft Active Accessibility (MSAA)</span></span>

<span data-ttu-id="76430-184">Microsoft Active Accessibility (MSAA) 是 Windows 95 首次引進的舊版技術。</span><span class="sxs-lookup"><span data-stu-id="76430-184">Microsoft Active Accessibility (MSAA) is a legacy technology that was first introduced with Windows 95.</span></span> <span data-ttu-id="76430-185">它是一組 Api，可改善) 產品的輔助技術 (與在 Microsoft Windows 上執行的應用程式搭配運作的方式。</span><span class="sxs-lookup"><span data-stu-id="76430-185">It is a set of APIs that improves the way Assistive Technology (AT) products work with applications running on Microsoft Windows.</span></span> <span data-ttu-id="76430-186">API 會提供程式設計介面和方法，以公開使用者介面專案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="76430-186">The API provide programming interfaces and methods for exposing information about user interface elements.</span></span>

<span data-ttu-id="76430-187">如需 Microsoft Active Accessibility 的詳細資訊，請參閱 [技術總覽](/windows/desktop/WinAuto/technical-overview)。</span><span class="sxs-lookup"><span data-stu-id="76430-187">For more information about Microsoft Active Accessibility, see the [Technical Overview](/windows/desktop/WinAuto/technical-overview).</span></span>

### <a name="supported-microsoft-active-accessibility-api-elements"></a><span data-ttu-id="76430-188">支援的 Microsoft Active Accessibility API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-188">Supported Microsoft Active Accessibility API Elements</span></span>

<span data-ttu-id="76430-189">舊版 Windows 支援所有 Api，其適用于 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="76430-189">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="ui-automation"></a><span data-ttu-id="76430-190">UI 自動化</span><span class="sxs-lookup"><span data-stu-id="76430-190">UI Automation</span></span>

<span data-ttu-id="76430-191">消費者介面自動化是一種較新的技術，可實消費者介面自動化規格並解決許多 Microsoft Active Accessibility 的限制。</span><span class="sxs-lookup"><span data-stu-id="76430-191">UI Automation is a newer technology that implements the UI Automation specification and addresses many of the limitations of Microsoft Active Accessibility.</span></span> <span data-ttu-id="76430-192">它是一組 Api，可讓您以程式設計方式存取應用程式的使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="76430-192">It is a set of APIs that provides programmatic access to the user interface elements of applications.</span></span> <span data-ttu-id="76430-193">提供的 API 可協助輔助技術產品和自動化測試控管存取、識別和操作應用程式的標準和自訂 UI 元素。</span><span class="sxs-lookup"><span data-stu-id="76430-193">The provided API help Assistive Technology products and automated testing tools access, identify, and manipulate the standard and custom UI elements of an application.</span></span>

<span data-ttu-id="76430-194">如需消費者介面自動化的詳細資訊，請參閱 [Windows AUTOMATION API：消費者介面自動化](../winauto/entry-uiauto-win32.md)。</span><span class="sxs-lookup"><span data-stu-id="76430-194">For more information about UI Automation, see [Windows Automation API: UI Automation](../winauto/entry-uiauto-win32.md).</span></span>

### <a name="supported-ui-automation-api-elements"></a><span data-ttu-id="76430-195">支援的消費者介面自動化 API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-195">Supported UI Automation API Elements</span></span>

<span data-ttu-id="76430-196">舊版 Windows 支援所有 Api，其適用于 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="76430-196">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-ui-automation-on-previous-windows-versions"></a><span data-ttu-id="76430-197">在舊版 Windows 上執行消費者介面自動化</span><span class="sxs-lookup"><span data-stu-id="76430-197">Running UI Automation on Previous Windows Versions</span></span>

<span data-ttu-id="76430-198">由於通用控制項和 Windows 標準控制項在不同的 Windows 版本上的執行方式有所差異，因此消費者介面自動化 proxy 針對這些控制項從某個版本取得至另一個版本的資訊可能會有些微差異。</span><span class="sxs-lookup"><span data-stu-id="76430-198">Because of differences in how the common controls and the Windows standard controls are implemented on different Windows versions, there might be slight differences in the information that the UI Automation proxies retrieve for these controls from one version to another.</span></span>

### <a name="windows-graphics-imaging-and-xps-library"></a><span data-ttu-id="76430-199">Windows 圖形、影像處理和 XPS 程式庫</span><span class="sxs-lookup"><span data-stu-id="76430-199">Windows Graphics, Imaging and XPS Library</span></span>

<span data-ttu-id="76430-200">Windows Vista 的平臺更新支援下列 windows 7 Api： Windows 圖形、映射和 XPS 程式庫：</span><span class="sxs-lookup"><span data-stu-id="76430-200">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Graphics, Imaging, and XPS Library:</span></span>

-   [<span data-ttu-id="76430-201">Direct2D</span><span class="sxs-lookup"><span data-stu-id="76430-201">Direct2D</span></span>](#direct2d)
-   [<span data-ttu-id="76430-202">Direct3D</span><span class="sxs-lookup"><span data-stu-id="76430-202">Direct3D</span></span>](#direct3d)
-   [<span data-ttu-id="76430-203">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="76430-203">DirectWrite</span></span>](#directwrite)
-   [<span data-ttu-id="76430-204">包裝</span><span class="sxs-lookup"><span data-stu-id="76430-204">Packaging</span></span>](#packaging)
-   [<span data-ttu-id="76430-205">Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="76430-205">Windows Imaging Component</span></span>](#windows-imaging-component)
-   [<span data-ttu-id="76430-206">XPS 檔</span><span class="sxs-lookup"><span data-stu-id="76430-206">XPS Document</span></span>](#xps-document)
-   [<span data-ttu-id="76430-207">XPS 列印</span><span class="sxs-lookup"><span data-stu-id="76430-207">XPS Print</span></span>](#xps-print)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="76430-208">適用于更新的 Windows 版本</span><span class="sxs-lookup"><span data-stu-id="76430-208">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="76430-209">適用于 windows Vista 的平臺更新和 Windows Server 2008 的平臺更新可讓您在下表所示的 Windows 版本上啟用 Windows 圖形、映射處理和 XPS 程式庫支援。</span><span class="sxs-lookup"><span data-stu-id="76430-209">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Graphics, Imaging, and XPS Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="76430-210">Windows 版本</span><span class="sxs-lookup"><span data-stu-id="76430-210">Windows Version</span></span></th>
<th><span data-ttu-id="76430-211">適用于 Update 的版本</span><span class="sxs-lookup"><span data-stu-id="76430-211">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76430-212">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76430-212">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="76430-213">使用 SP2 的 Starter (x86) </span><span class="sxs-lookup"><span data-stu-id="76430-213">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="76430-214">Home Basic SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-214">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-215">Home Premium SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-215">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-216">使用 SP2 (x86 和 amd64) 的企業</span><span class="sxs-lookup"><span data-stu-id="76430-216">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-217">Enterprise SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-217">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-218">SP2 (x86 和 amd64) 的終極</span><span class="sxs-lookup"><span data-stu-id="76430-218">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76430-219">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76430-219">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="76430-220">Windows Server 2008 SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-220">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="direct2d"></a><span data-ttu-id="76430-221">Direct2D</span><span class="sxs-lookup"><span data-stu-id="76430-221">Direct2D</span></span>

<span data-ttu-id="76430-222">Direct2D API 是新的硬體加速、即時模式的2-d 圖形 API，可為2D 幾何、點陣圖和文字提供高效能和高品質的呈現。</span><span class="sxs-lookup"><span data-stu-id="76430-222">The Direct2D API is a new hardware-accelerated, immediate-mode 2-D graphics API that provides high performance and high quality rendering for 2-D geometry, bitmaps, and text.</span></span> <span data-ttu-id="76430-223">Direct2D API 是設計來與使用 GDI、GDI + 或 Direct3D 的現有程式碼交互操作。</span><span class="sxs-lookup"><span data-stu-id="76430-223">The Direct2D API is designed to interoperate well with existing code that uses GDI, GDI+, or Direct3D.</span></span>

<span data-ttu-id="76430-224">如需 Direct2D 的詳細資訊，請參閱 [關於 Direct2D](/windows/desktop/Direct2D/direct2d-overview)。</span><span class="sxs-lookup"><span data-stu-id="76430-224">For more information about Direct2D, see [About Direct2D](/windows/desktop/Direct2D/direct2d-overview).</span></span>

### <a name="supported-direct2d-api-elements"></a><span data-ttu-id="76430-225">支援的 Direct2D API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-225">Supported Direct2D API Elements</span></span>

<span data-ttu-id="76430-226">舊版 Windows 支援所有 Api，其適用于 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="76430-226">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-direct2d-on-previous-windows-versions"></a><span data-ttu-id="76430-227">在先前的 Windows 版本上執行 Direct2D</span><span class="sxs-lookup"><span data-stu-id="76430-227">Running Direct2D on Previous Windows Versions</span></span>

<span data-ttu-id="76430-228">如果 Windows Vista 上缺少 WDDM 1.1 驅動程式，Direct2D/GDI 互通性的效能會降低。</span><span class="sxs-lookup"><span data-stu-id="76430-228">If the WDDM 1.1 driver is missing on Windows Vista, the performance of Direct2D/GDI interoperability degrades.</span></span>

### <a name="direct3d"></a><span data-ttu-id="76430-229">Direct3D</span><span class="sxs-lookup"><span data-stu-id="76430-229">Direct3D</span></span>

<span data-ttu-id="76430-230">適用于 Windows Vista 的平臺更新提供 Direct3D10 和 Direct3D 10.1 程式碼路徑的 BGRA 介面支援。</span><span class="sxs-lookup"><span data-stu-id="76430-230">The Platform Update for Windows Vista provides BGRA surface support for Direct3D10 and Direct3D10.1 code-paths.</span></span> <span data-ttu-id="76430-231">Direct3D10Level9 可讓 Direct3D10 功能在 Direct3D9 硬體上運作。</span><span class="sxs-lookup"><span data-stu-id="76430-231">Direct3D10Level9 enables Direct3D10 functionality to work on Direct3D9 hardware.</span></span> <span data-ttu-id="76430-232">Direct3D WARP10 是適用于 Direct3D10 應用程式的高效能軟體轉譯器。</span><span class="sxs-lookup"><span data-stu-id="76430-232">Direct3D WARP10 is a performant software rasterizer for Direct3D10 applications.</span></span> <span data-ttu-id="76430-233">Direct3D11 是最新版的 Direct3D，可提供新的功能，例如改良的多執行緒支援、鑲嵌式、DirectCompute 功能和動態著色器連結。</span><span class="sxs-lookup"><span data-stu-id="76430-233">Direct3D11, the latest version of Direct3D, provides new capabilities such as improved multithreading support, tessellation, DirectCompute functionality, and dynamic shader linkage.</span></span>

<span data-ttu-id="76430-234">如果您建立使用 Direct3D 的應用程式，則需要 [DIRECTX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="76430-234">If you create applications that use Direct3D, the [DirectX SDK](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/aa937788.aspx) is required.</span></span>

<span data-ttu-id="76430-235">如需 Direct3D 的詳細資訊，請參閱 [direct3d](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="76430-235">For more information about Direct3D, see [Direct3D](/previous-versions/windows/apps/hh452744(v=win.10)) (https://msdn.microsoft.com/directx/default.aspx).</span></span>

### <a name="supported-direct3d-api-elements"></a><span data-ttu-id="76430-236">支援的 Direct3D API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-236">Supported Direct3D API Elements</span></span>

<span data-ttu-id="76430-237">舊版 Windows 支援所有 Api，其適用于 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="76430-237">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="directwrite"></a><span data-ttu-id="76430-238">DirectWrite</span><span class="sxs-lookup"><span data-stu-id="76430-238">DirectWrite</span></span>

<span data-ttu-id="76430-239">DirectWrite API 是新的文字 API，提供多層的功能，包括文字配置、腳本處理、圖像轉譯和字型系統。</span><span class="sxs-lookup"><span data-stu-id="76430-239">The DirectWrite API is a new text API that provides multiple layers of functionality, including text layout, script processing, glyph rendering, and the font system.</span></span> <span data-ttu-id="76430-240">DirectWrite 使用 OpenType 字型和子圖元 ClearType 轉譯來加強應用程式所提供的文字體驗。</span><span class="sxs-lookup"><span data-stu-id="76430-240">DirectWrite uses OpenType fonts and sub-pixel ClearType rendering to enhance the text experience provided by applications.</span></span> <span data-ttu-id="76430-241">使用 Direct2D 時，文字轉譯是硬體加速。</span><span class="sxs-lookup"><span data-stu-id="76430-241">Text rendering is hardware-accelerated when used with Direct2D.</span></span>

<span data-ttu-id="76430-242">如需 DirectWrite 的詳細資訊，請參閱 [DirectWrite 簡介](/windows/desktop/DirectWrite/introducing-directwrite)。</span><span class="sxs-lookup"><span data-stu-id="76430-242">For more information about DirectWrite, see [Introducing DirectWrite](/windows/desktop/DirectWrite/introducing-directwrite).</span></span>

### <a name="supported-directwrite-api-elements"></a><span data-ttu-id="76430-243">支援的 DirectWrite API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-243">Supported DirectWrite API Elements</span></span>

<span data-ttu-id="76430-244">舊版 Windows 支援所有 Api，其適用于 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="76430-244">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="running-directwrite-on-previous-windows-versions"></a><span data-ttu-id="76430-245">在先前的 Windows 版本上執行 DirectWrite</span><span class="sxs-lookup"><span data-stu-id="76430-245">Running DirectWrite on Previous Windows Versions</span></span>

<span data-ttu-id="76430-246">下列行為問題可能會影響在先前的 Windows 版本上使用 DirectWrite API：</span><span class="sxs-lookup"><span data-stu-id="76430-246">The following behavioral issues may affect the use of DirectWrite API on previous Windows versions:</span></span>

-   <span data-ttu-id="76430-247">Windows 7 的新腳本可能無法在先前的 Windows 版本上完全正確轉譯。</span><span class="sxs-lookup"><span data-stu-id="76430-247">Scripts new to Windows 7 may not render entirely correctly on previous Windows versions.</span></span>
-   <span data-ttu-id="76430-248">先前的 Windows 版本中未提供的地區設定會回復為預設行為。</span><span class="sxs-lookup"><span data-stu-id="76430-248">Locales not available in previous Windows versions fall back to default behavior.</span></span>
-   <span data-ttu-id="76430-249">在舊版的 Windows 上無法使用 ClearType 調諧器。</span><span class="sxs-lookup"><span data-stu-id="76430-249">The ClearType Tuner is not available on previous Windows versions.</span></span>
-   <span data-ttu-id="76430-250">在舊版 Windows 上的某些案例中，GDI 互通性的記憶體成本較高。</span><span class="sxs-lookup"><span data-stu-id="76430-250">GDI interoperability has a higher memory cost in some scenarios on previous Windows versions.</span></span>

### <a name="packaging"></a><span data-ttu-id="76430-251">包裝</span><span class="sxs-lookup"><span data-stu-id="76430-251">Packaging</span></span>

<span data-ttu-id="76430-252">Windows Vista 的平臺更新支援在非受控應用程式中使用 XPS 檔 API 執行工作所需的有限封裝 Api 子集。</span><span class="sxs-lookup"><span data-stu-id="76430-252">The Platform Update for Windows Vista supports a limited subset of the Packaging APIs that are needed to perform tasks with the XPS Document API in unmanaged applications.</span></span>

<span data-ttu-id="76430-253">如需封裝 Api 的詳細資訊，請參閱 [封裝 Api 總覽](/previous-versions/windows/desktop/opc/packaging-api-overview)。</span><span class="sxs-lookup"><span data-stu-id="76430-253">For more information about Packaging APIs, please see the [Packaging API Overview](/previous-versions/windows/desktop/opc/packaging-api-overview).</span></span>

### <a name="supported-packaging-api-elements"></a><span data-ttu-id="76430-254">支援的封裝 API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-254">Supported Packaging API Elements</span></span>

<span data-ttu-id="76430-255">僅支援下列封裝介面：</span><span class="sxs-lookup"><span data-stu-id="76430-255">Only the following Packaging interfaces are supported:</span></span>

-   <span data-ttu-id="76430-256">IOpcUri</span><span class="sxs-lookup"><span data-stu-id="76430-256">IOpcUri</span></span>
-   <span data-ttu-id="76430-257">IOpcPartUri</span><span class="sxs-lookup"><span data-stu-id="76430-257">IOpcPartUri</span></span>
-   <span data-ttu-id="76430-258">IOpcFactory (僅支援下列方法) </span><span class="sxs-lookup"><span data-stu-id="76430-258">IOpcFactory (only the following methods are supported)</span></span>
    -   <span data-ttu-id="76430-259">CreatePackageRootUri</span><span class="sxs-lookup"><span data-stu-id="76430-259">CreatePackageRootUri</span></span>
    -   <span data-ttu-id="76430-260">CreatePartUri</span><span class="sxs-lookup"><span data-stu-id="76430-260">CreatePartUri</span></span>
    -   <span data-ttu-id="76430-261">CreateStreamOnFile</span><span class="sxs-lookup"><span data-stu-id="76430-261">CreateStreamOnFile</span></span>

<span data-ttu-id="76430-262">支援的封裝 Api 可以用來建立檔案的資料流程，以及建立以套件為基礎的 URI 並與其互動。</span><span class="sxs-lookup"><span data-stu-id="76430-262">Supported Packaging APIs can be used to create streams over files as well as to create and interact with package-based URI.</span></span>

### <a name="running-packaging-api-on-previous-windows-versions"></a><span data-ttu-id="76430-263">在先前的 Windows 版本上執行封裝 API</span><span class="sxs-lookup"><span data-stu-id="76430-263">Running Packaging API on Previous Windows Versions</span></span>

<span data-ttu-id="76430-264">在所有支援的平臺上，支援的封裝介面和方法的行為和效能都相同。</span><span class="sxs-lookup"><span data-stu-id="76430-264">The behavior and performance of supported Packaging interfaces and methods are the same on all supported platforms.</span></span>

<span data-ttu-id="76430-265">如果應用程式嘗試具現化或呼叫不支援的封裝介面或方法，則嘗試將會失敗。</span><span class="sxs-lookup"><span data-stu-id="76430-265">If an application attempts to instantiate or call an unsupported Packaging interface or method, the attempt will fail.</span></span> <span data-ttu-id="76430-266">如果呼叫的是不支援的 [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) 方法， \_ 將會傳回 E >notimpl 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="76430-266">If the call is to an unsupported [**IOpcFactory**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcfactory) method, the E\_NOTIMPL error code will be returned.</span></span>

### <a name="windows-imaging-component"></a><span data-ttu-id="76430-267">Windows Imaging Component</span><span class="sxs-lookup"><span data-stu-id="76430-267">Windows Imaging Component</span></span>

<span data-ttu-id="76430-268">Windows 影像處理元件 (WIC) 的新功能包括增強的安全性、支援高的色彩，以及更好的中繼資料互通性。</span><span class="sxs-lookup"><span data-stu-id="76430-268">New features for the Windows Imaging Component (WIC) include enhanced security, support for high color, and better metadata interoperability.</span></span> <span data-ttu-id="76430-269">此外，Windows 影像處理元件藉由提供漸進式影像解碼、擴充的 PNG 功能、GIF 中繼資料、HD 相片更新，以及橫跨 APPn 區段的中繼資料支援，來拓寬其標準合規性。</span><span class="sxs-lookup"><span data-stu-id="76430-269">In addition, the Windows Imaging Component broadens its standards compliance by providing support for progressive image decoding, expanded PNG features, GIF metadata, , HD Photo updates, and metadata that spans APPn segments.</span></span>

<span data-ttu-id="76430-270">如需有關 Windows 影像處理元件的詳細資訊，請參閱 [Windows 影像處理元件總覽](/windows/desktop/wic/-wic-about-windows-imaging-codec)。</span><span class="sxs-lookup"><span data-stu-id="76430-270">For more information about the Windows Imaging Component, see the [Windows Imaging Component Overview](/windows/desktop/wic/-wic-about-windows-imaging-codec).</span></span>

### <a name="supported-wic-api-elements"></a><span data-ttu-id="76430-271">支援的 WIC API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-271">Supported WIC API Elements</span></span>

<span data-ttu-id="76430-272">舊版 Windows 支援所有 Api，其適用于 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="76430-272">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="xps-document"></a><span data-ttu-id="76430-273">XPS 檔</span><span class="sxs-lookup"><span data-stu-id="76430-273">XPS Document</span></span>

<span data-ttu-id="76430-274">XPS 檔 Api 支援在非受控應用程式中建立、修改及儲存 XPS 檔</span><span class="sxs-lookup"><span data-stu-id="76430-274">The XPS Document APIs support the creating, modifying, and saving of XPS Documents in unmanaged applications</span></span>

<span data-ttu-id="76430-275">如需 XPS 檔 Api 的詳細資訊，請參閱 [Xps 檔程式設計指南。](/previous-versions//dd372978(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="76430-275">For more information about XPS Document APIs, please see the [XPS Document Programming Guide.](/previous-versions//dd372978(v=vs.85))</span></span>

### <a name="supported-xps-document-api-elements"></a><span data-ttu-id="76430-276">支援的 XPS 檔 API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-276">Supported XPS Document API Elements</span></span>

<span data-ttu-id="76430-277">舊版作業系統版本只支援 [XPS 數位簽章](/previous-versions/windows/desktop/dd372947(v=vs.85)) 介面。</span><span class="sxs-lookup"><span data-stu-id="76430-277">Only the [XPS Digital Signatures](/previous-versions/windows/desktop/dd372947(v=vs.85)) interfaces are not supported on down-level OS versions.</span></span>

### <a name="xps-print"></a><span data-ttu-id="76430-278">XPS 列印</span><span class="sxs-lookup"><span data-stu-id="76430-278">XPS Print</span></span>

<span data-ttu-id="76430-279">XPS 列印 Api 支援從以 Windows 為基礎的應用程式列印 XPS 檔。</span><span class="sxs-lookup"><span data-stu-id="76430-279">The XPS Print APIs support the printing of XPS documents from Windows-based applications.</span></span>

<span data-ttu-id="76430-280">如需 XPS 列印 Api 的詳細資訊，請參閱 [XPSPRINT API](/windows/desktop/printdocs/xpsprint-api)。</span><span class="sxs-lookup"><span data-stu-id="76430-280">For more information about XPS Print APIs, please see the [XpsPrint API](/windows/desktop/printdocs/xpsprint-api).</span></span>

### <a name="supported-xps-print-api-elements"></a><span data-ttu-id="76430-281">支援的 XPS 列印 API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-281">Supported XPS Print API Elements</span></span>

<span data-ttu-id="76430-282">舊版 Windows 支援所有 Api，其適用于 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="76430-282">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-ribbon-and-animation-manager-library"></a><span data-ttu-id="76430-283">Windows 功能區和動畫管理員程式庫</span><span class="sxs-lookup"><span data-stu-id="76430-283">Windows Ribbon and Animation Manager Library</span></span>

<span data-ttu-id="76430-284">Windows Vista 的平臺更新支援 Windows 功能區和動畫庫中的下列 Windows 7 Api：</span><span class="sxs-lookup"><span data-stu-id="76430-284">The Platform Update for Windows Vista supports the following Windows 7 APIs from the Windows Ribbon and Animation Library:</span></span>

-   [<span data-ttu-id="76430-285">Windows 功能區架構</span><span class="sxs-lookup"><span data-stu-id="76430-285">Windows Ribbon Framework</span></span>](#windows-ribbon-and-animation-manager-library)
-   [<span data-ttu-id="76430-286">Windows 動畫管理員</span><span class="sxs-lookup"><span data-stu-id="76430-286">Windows Animation Manager</span></span>](#windows-animation-manager)

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="76430-287">適用于更新的 Windows 版本</span><span class="sxs-lookup"><span data-stu-id="76430-287">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="76430-288">適用于 windows Vista 的平臺更新和 Windows Server 2008 的平臺更新可讓您在下表所示的 Windows 版本上啟用 Windows 功能區和動畫管理員程式庫支援。</span><span class="sxs-lookup"><span data-stu-id="76430-288">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Ribbon and Animation Manager Library support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="76430-289">Windows 版本</span><span class="sxs-lookup"><span data-stu-id="76430-289">Windows Version</span></span></th>
<th><span data-ttu-id="76430-290">適用于 Update 的版本</span><span class="sxs-lookup"><span data-stu-id="76430-290">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76430-291">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76430-291">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="76430-292">使用 SP2 的 Starter (x86) </span><span class="sxs-lookup"><span data-stu-id="76430-292">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="76430-293">Home Basic SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-293">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-294">Home Premium SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-294">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-295">使用 SP2 (x86 和 amd64) 的企業</span><span class="sxs-lookup"><span data-stu-id="76430-295">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-296">Enterprise SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-296">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-297">SP2 (x86 和 amd64) 的終極</span><span class="sxs-lookup"><span data-stu-id="76430-297">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="76430-298">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="76430-298">Windows Server 2008</span></span></td>
<td><dl> <span data-ttu-id="76430-299">Windows Server 2008 SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-299">Windows Server 2008 with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="windows-ribbon-framework"></a><span data-ttu-id="76430-300">Windows 功能區架構</span><span class="sxs-lookup"><span data-stu-id="76430-300">Windows Ribbon Framework</span></span>

<span data-ttu-id="76430-301">Windows 功能區 (功能區) 架構是一種豐富的命令呈現系統，可提供傳統 Windows 應用程式之階層式功能表、工具列和工作窗格的新式替代方案。</span><span class="sxs-lookup"><span data-stu-id="76430-301">The Windows Ribbon (Ribbon) framework is a rich command presentation system that provides a modern alternative to the layered menus, toolbars, and task panes of traditional Windows applications.</span></span>

<span data-ttu-id="76430-302">此架構是 Microsoft Win32 Api 的集合，可為 Windows 開發人員提供新的使用者介面功能，並同時包含功能區和內容功能表系統。</span><span class="sxs-lookup"><span data-stu-id="76430-302">The framework is a collection of Microsoft Win32 APIs that provide a host of new user interface capabilities for Windows developers and includes both the Ribbon and a context menu system.</span></span>

<span data-ttu-id="76430-303">如需功能區架構的詳細資訊，請參閱 [Windows 功能區架構簡介](../windowsribbon/windowsribbon-introduction.md)。</span><span class="sxs-lookup"><span data-stu-id="76430-303">For more information about the Ribbon framework, see [Introducing the Windows Ribbon Framework](../windowsribbon/windowsribbon-introduction.md).</span></span>

### <a name="supported-ribbon-framework-api-elements"></a><span data-ttu-id="76430-304">支援的功能區架構 API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-304">Supported Ribbon Framework API Elements</span></span>

<span data-ttu-id="76430-305">舊版 Windows 支援所有 Api，其適用于 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="76430-305">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-animation-manager"></a><span data-ttu-id="76430-306">Windows 動畫管理員</span><span class="sxs-lookup"><span data-stu-id="76430-306">Windows Animation Manager</span></span>

<span data-ttu-id="76430-307">Windows 動畫管理員 (Windows 動畫) 是一種程式設計介面，可支援 Windows 應用程式之視覺元素的動畫。</span><span class="sxs-lookup"><span data-stu-id="76430-307">The Windows Animation Manager (Windows Animation) is a programmatic interface that supports the animation of visual elements of Windows applications.</span></span> <span data-ttu-id="76430-308">Windows 動畫的設計目的是簡化動畫順序的開發和維護，以及讓開發人員能夠執行一致且直覺的動畫。</span><span class="sxs-lookup"><span data-stu-id="76430-308">Windows Animation is designed to simplify the development and maintenance of animation sequences and to enable developers to implement animations that are consistent and intuitive.</span></span> <span data-ttu-id="76430-309">Windows 動畫可與任何圖形平台搭配使用，包括 Direct2D、Direct3D 或 GDI +。</span><span class="sxs-lookup"><span data-stu-id="76430-309">Windows Animation can be used with any graphics platform including Direct2D, Direct3D, or GDI+.</span></span>

<span data-ttu-id="76430-310">Windows 動畫是單一執行緒 COM API，可提供開發人員建立、管理和驅動 UI 動畫所需的一切。</span><span class="sxs-lookup"><span data-stu-id="76430-310">Windows Animation is a single-threaded COM API that provides everything a developer needs to create, manage, and drive UI animation.</span></span>

<span data-ttu-id="76430-311">如需 Windows 動畫管理員的詳細資訊，請參閱 [Windows 動畫簡介](/windows/desktop/UIAnimation/introducing-windows-animation-manager)。</span><span class="sxs-lookup"><span data-stu-id="76430-311">For more information about the Windows Animation Manager, see [Introducing Windows Animation](/windows/desktop/UIAnimation/introducing-windows-animation-manager).</span></span>

### <a name="supported-animation-manager-api-elements"></a><span data-ttu-id="76430-312">支援的動畫管理員 API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-312">Supported Animation Manager API Elements</span></span>

<span data-ttu-id="76430-313">舊版 Windows 支援所有 Api，其適用于 Windows Vista 的平臺更新或 Windows Server 2008 的平臺更新。</span><span class="sxs-lookup"><span data-stu-id="76430-313">All APIs are supported on previous versions of Windows that are eligible for the Platform Update for Windows Vista or the Platform Update for Windows Server 2008.</span></span>

### <a name="windows-portable-devices-platform"></a><span data-ttu-id="76430-314">Windows 可攜式裝置平臺</span><span class="sxs-lookup"><span data-stu-id="76430-314">Windows Portable Devices Platform</span></span>

<span data-ttu-id="76430-315">適用于 windows Vista 的平臺更新支援 windows 7 延伸模組至 Windows 可攜式裝置 (WPD) 平臺。</span><span class="sxs-lookup"><span data-stu-id="76430-315">The Platform Update for Windows Vista supports the Windows 7 extensions to the Windows Portable Devices (WPD) platform.</span></span> <span data-ttu-id="76430-316">這項功能可讓電腦與連接的媒體和存放裝置進行通訊。</span><span class="sxs-lookup"><span data-stu-id="76430-316">This feature enables computers to communicate with attached media and storage devices.</span></span> <span data-ttu-id="76430-317">WPD 提供彈性且健全的方式，讓電腦與數位相機、音樂播放機、行動電話以及許多其他類型的連線裝置進行通訊。</span><span class="sxs-lookup"><span data-stu-id="76430-317">WPD provides a flexible, robust way for computers to communicate with digital cameras, music players, mobile phones, and many other types of connected devices.</span></span>

<span data-ttu-id="76430-318">如需 Windows 可攜式裝置的詳細資訊，請參閱 [Windows 可攜式裝置](/windows-hardware/drivers/portable/) (https://docs.microsoft.com/windows-hardware/drivers/portable/) 。</span><span class="sxs-lookup"><span data-stu-id="76430-318">For more information about Windows Portable Devices, see [Windows Portable Devices](/windows-hardware/drivers/portable/) (https://docs.microsoft.com/windows-hardware/drivers/portable/).</span></span>

### <a name="windows-editions-eligible-for-the-updates"></a><span data-ttu-id="76430-319">適用于更新的 Windows 版本</span><span class="sxs-lookup"><span data-stu-id="76430-319">Windows Editions Eligible for the Updates</span></span>

<span data-ttu-id="76430-320">適用于 windows Vista 的平臺更新和 Windows Server 2008 的平臺更新可讓 Windows 可攜式裝置 (下表所示之 Windows 版本的 WPD) 支援。</span><span class="sxs-lookup"><span data-stu-id="76430-320">The Platform Update for Windows Vista and the Platform Update for Windows Server 2008 enable Windows Portable Devices (WPD) support on the editions of Windows shown in the following table.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="76430-321">Windows 版本</span><span class="sxs-lookup"><span data-stu-id="76430-321">Windows Version</span></span></th>
<th><span data-ttu-id="76430-322">適用于 Update 的版本</span><span class="sxs-lookup"><span data-stu-id="76430-322">Editions Eligible for Update</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="76430-323">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76430-323">Windows Vista</span></span></td>
<td><dl> <span data-ttu-id="76430-324">使用 SP2 的 Starter (x86) </span><span class="sxs-lookup"><span data-stu-id="76430-324">Starter with SP2 (x86)</span></span><br />
<span data-ttu-id="76430-325">Home Basic SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-325">Home Basic with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-326">Home Premium SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-326">Home Premium with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-327">使用 SP2 (x86 和 amd64) 的企業</span><span class="sxs-lookup"><span data-stu-id="76430-327">Business with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-328">Enterprise SP2 (x86 和 amd64) </span><span class="sxs-lookup"><span data-stu-id="76430-328">Enterprise with SP2 (x86 and amd64)</span></span><br />
<span data-ttu-id="76430-329">SP2 (x86 和 amd64) 的終極</span><span class="sxs-lookup"><span data-stu-id="76430-329">Ultimate with SP2 (x86 and amd64)</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

### <a name="supported-wpd-api-elements"></a><span data-ttu-id="76430-330">支援的 WPD API 元素</span><span class="sxs-lookup"><span data-stu-id="76430-330">Supported WPD API Elements</span></span>

<span data-ttu-id="76430-331">下表指出 windows 7、Windows Vista 和 Windows Vista （windows vista windows Vista 版本的 windows 作業系統）支援的功能。</span><span class="sxs-lookup"><span data-stu-id="76430-331">The following table identifies the features that are supported for the Windows 7, Windows Vista, and Windows Vista with Platform Update for Windows Vista versions of the Windows operating system.</span></span>

| <span data-ttu-id="76430-332">WPD 功能</span><span class="sxs-lookup"><span data-stu-id="76430-332">WPD Feature</span></span>                    | <span data-ttu-id="76430-333">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76430-333">Windows 7</span></span> | <span data-ttu-id="76430-334">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="76430-334">Windows Vista</span></span> | <span data-ttu-id="76430-335">Windows vista 與 Windows Vista 平臺更新</span><span class="sxs-lookup"><span data-stu-id="76430-335">Windows Vista with Platform Update for Windows Vista</span></span> |
|--------------------------------|-----------|---------------|------------------------------------------------------|
| <span data-ttu-id="76430-336">透過 USB 的 MTP</span><span class="sxs-lookup"><span data-stu-id="76430-336">MTP over USB</span></span>                   | <span data-ttu-id="76430-337">是</span><span class="sxs-lookup"><span data-stu-id="76430-337">Yes</span></span>       | <span data-ttu-id="76430-338">是</span><span class="sxs-lookup"><span data-stu-id="76430-338">Yes</span></span>           | <span data-ttu-id="76430-339">是</span><span class="sxs-lookup"><span data-stu-id="76430-339">Yes</span></span>                                                  |
| <span data-ttu-id="76430-340">IP 上的 MTP</span><span class="sxs-lookup"><span data-stu-id="76430-340">MTP over IP</span></span>                    | <span data-ttu-id="76430-341">是</span><span class="sxs-lookup"><span data-stu-id="76430-341">Yes</span></span>       | <span data-ttu-id="76430-342">是</span><span class="sxs-lookup"><span data-stu-id="76430-342">Yes</span></span>           | <span data-ttu-id="76430-343">是</span><span class="sxs-lookup"><span data-stu-id="76430-343">Yes</span></span>                                                  |
| <span data-ttu-id="76430-344">透過藍牙的 MTP</span><span class="sxs-lookup"><span data-stu-id="76430-344">MTP over Bluetooth</span></span>             | <span data-ttu-id="76430-345">是</span><span class="sxs-lookup"><span data-stu-id="76430-345">Yes</span></span>       | <span data-ttu-id="76430-346">否</span><span class="sxs-lookup"><span data-stu-id="76430-346">No</span></span>            | <span data-ttu-id="76430-347">是</span><span class="sxs-lookup"><span data-stu-id="76430-347">Yes</span></span>                                                  |
| <span data-ttu-id="76430-348">WPD 和 MTP 裝置服務</span><span class="sxs-lookup"><span data-stu-id="76430-348">WPD and MTP Device Services</span></span>    | <span data-ttu-id="76430-349">是</span><span class="sxs-lookup"><span data-stu-id="76430-349">Yes</span></span>       | <span data-ttu-id="76430-350">否</span><span class="sxs-lookup"><span data-stu-id="76430-350">No</span></span>            | <span data-ttu-id="76430-351">是</span><span class="sxs-lookup"><span data-stu-id="76430-351">Yes</span></span>                                                  |
| <span data-ttu-id="76430-352">WPD 自動化</span><span class="sxs-lookup"><span data-stu-id="76430-352">WPD Automation</span></span>                 | <span data-ttu-id="76430-353">是</span><span class="sxs-lookup"><span data-stu-id="76430-353">Yes</span></span>       | <span data-ttu-id="76430-354">否</span><span class="sxs-lookup"><span data-stu-id="76430-354">No</span></span>            | <span data-ttu-id="76430-355">否</span><span class="sxs-lookup"><span data-stu-id="76430-355">No</span></span>                                                   |
| <span data-ttu-id="76430-356">多函數/多重傳輸</span><span class="sxs-lookup"><span data-stu-id="76430-356">Multi-function/Multi-transport</span></span> | <span data-ttu-id="76430-357">是</span><span class="sxs-lookup"><span data-stu-id="76430-357">Yes</span></span>       | <span data-ttu-id="76430-358">否</span><span class="sxs-lookup"><span data-stu-id="76430-358">No</span></span>            | <span data-ttu-id="76430-359">否</span><span class="sxs-lookup"><span data-stu-id="76430-359">No</span></span>                                                   |
| <span data-ttu-id="76430-360">Device Stage</span><span class="sxs-lookup"><span data-stu-id="76430-360">Device Stage</span></span>                   | <span data-ttu-id="76430-361">是</span><span class="sxs-lookup"><span data-stu-id="76430-361">Yes</span></span>       | <span data-ttu-id="76430-362">否</span><span class="sxs-lookup"><span data-stu-id="76430-362">No</span></span>            | <span data-ttu-id="76430-363">否</span><span class="sxs-lookup"><span data-stu-id="76430-363">No</span></span>                                                   |
| <span data-ttu-id="76430-364">裝置同步平臺</span><span class="sxs-lookup"><span data-stu-id="76430-364">Device Sync Platform</span></span>           | <span data-ttu-id="76430-365">是</span><span class="sxs-lookup"><span data-stu-id="76430-365">Yes</span></span>       | <span data-ttu-id="76430-366">否</span><span class="sxs-lookup"><span data-stu-id="76430-366">No</span></span>            | <span data-ttu-id="76430-367">否</span><span class="sxs-lookup"><span data-stu-id="76430-367">No</span></span>                                                   |



 

<span data-ttu-id="76430-368">針對沒有預設安裝 Microsoft Windows Media Player 的 Windows 7 和 Windows Vista 版本 (N 和 KN 版) ，您必須安裝 [Windows Media Format 11 SDK]( ../audio-and-video.md) (https://msdn.microsoft.com/windows/bb190326.aspx) 才能啟用 WPD 功能。</span><span class="sxs-lookup"><span data-stu-id="76430-368">For editions of Windows 7 and Windows Vista that do not have Microsoft Windows Media Player installed by default (the N and KN editions), you must install the [Windows Media Format 11 SDK]( ../audio-and-video.md) (https://msdn.microsoft.com/windows/bb190326.aspx) to enable WPD functionality.</span></span> <span data-ttu-id="76430-369">如需詳細資訊，請參閱 [知識庫文章](https://support.microsoft.com/kb/953693) (https://go.microsoft.com/fwlink/p/?linkid=158715) ，其原本是發佈為 Windows Vista 的解決方案。</span><span class="sxs-lookup"><span data-stu-id="76430-369">For more information, see the [Knowledge Base article](https://support.microsoft.com/kb/953693) (https://go.microsoft.com/fwlink/p/?linkid=158715), which was originally published as a resolution for Windows Vista.</span></span>

## <a name="related-topics"></a><span data-ttu-id="76430-370">相關主題</span><span class="sxs-lookup"><span data-stu-id="76430-370">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="76430-371">Windows Vista 的平臺更新</span><span class="sxs-lookup"><span data-stu-id="76430-371">Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-portal.md)
</dt> <dt>

<span data-ttu-id="76430-372">**概觀**</span><span class="sxs-lookup"><span data-stu-id="76430-372">**Overviews**</span></span>
</dt> <dt>

[<span data-ttu-id="76430-373">關於 Windows Vista 的平臺更新</span><span class="sxs-lookup"><span data-stu-id="76430-373">About Platform Update for Windows Vista</span></span>](platform-update-for-windows-vista-overview.md)
</dt> <dt>

[<span data-ttu-id="76430-374">適用于 Windows Vista 的平臺更新 (KB 971644) 的知識庫文章 </span><span class="sxs-lookup"><span data-stu-id="76430-374">Knowledge Base article about the Platform Update for Windows Vista (KB 971644)</span></span>](https://support.microsoft.com/kb/971644)
</dt> </dl>

 

 