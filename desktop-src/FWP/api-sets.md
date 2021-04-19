---
title: WFP API
description: Windows 篩選平台 (WFP) API 分為下列元件。
ms.assetid: ff3f0d74-7e0b-4a3e-b66d-eaa61b89038a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4230c82105f85c36e6fb112508a7128758b2ad60
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "106966073"
---
# <a name="wfp-api"></a><span data-ttu-id="753ed-103">WFP API</span><span class="sxs-lookup"><span data-stu-id="753ed-103">WFP API</span></span>

<span data-ttu-id="753ed-104">Windows 篩選平台 (WFP) API 分為下列元件。</span><span class="sxs-lookup"><span data-stu-id="753ed-104">The Windows Filtering Platform (WFP) API is divided into the following components.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="753ed-105">元件</span><span class="sxs-lookup"><span data-stu-id="753ed-105">Component</span></span></th>
<th><span data-ttu-id="753ed-106">描述</span><span class="sxs-lookup"><span data-stu-id="753ed-106">Description</span></span></th>
<th><span data-ttu-id="753ed-107">標頭檔</span><span class="sxs-lookup"><span data-stu-id="753ed-107">Header Files</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="753ed-108"><a href="/windows-hardware/drivers/ddi/_netvista/">標注 API</a> (FWPS) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="753ed-108"><a href="/windows-hardware/drivers/ddi/_netvista/">Callout API</a> (FWPS)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="753ed-109">由標注使用的<a href="/windows-hardware/drivers/ddi/_netvista/">資料類型</a>。<strong>注意</strong> 這些資料類型記載于 Microsoft Windows 驅動程式開發工具組 (DDK) 。</span><span class="sxs-lookup"><span data-stu-id="753ed-109"><a href="/windows-hardware/drivers/ddi/_netvista/">Data types</a> used by callouts.<strong>Note</strong>  These data types are documented in the Microsoft Windows Driver Development Kit (DDK).</span></span><br/></td>
<td><dl> <span data-ttu-id="753ed-110">fwpstypes。h</span><span class="sxs-lookup"><span data-stu-id="753ed-110">fwpstypes.h</span></span><br />
<span data-ttu-id="753ed-111">fwpstypes .idl</span><span class="sxs-lookup"><span data-stu-id="753ed-111">fwpstypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="753ed-112">用來執行標注的<a href="/windows-hardware/drivers/ddi/_netvista/">函數</a>和<a href="/windows-hardware/drivers/ddi/_netvista/">列舉類型</a>。<strong>注意</strong> 這些函式和列舉類型記載于 DDK 中。</span><span class="sxs-lookup"><span data-stu-id="753ed-112"><a href="/windows-hardware/drivers/ddi/_netvista/">Functions</a> and <a href="/windows-hardware/drivers/ddi/_netvista/">enumerated types</a> used to implement callouts.<strong>Note</strong>  These functions and enumerated types are documented in the DDK.</span></span><br/></td>
<td><dl> <span data-ttu-id="753ed-113">fwpsu。h</span><span class="sxs-lookup"><span data-stu-id="753ed-113">fwpsu.h</span></span><br />
<span data-ttu-id="753ed-114">fwpsk。h</span><span class="sxs-lookup"><span data-stu-id="753ed-114">fwpsk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="753ed-115">IKE/AuthIP API (IKEEXT) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="753ed-115">IKE/AuthIP API (IKEEXT)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="753ed-116">用來管理 IKE 和 AuthIP 主要模式 (MM) 原則和安全性關聯的<a href="fwp-enums.md">列舉類型</a>和<a href="fwp-structs.md">結構</a>。</span><span class="sxs-lookup"><span data-stu-id="753ed-116"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IKE and AuthIP main mode (MM) policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="753ed-117">iketypes。h</span><span class="sxs-lookup"><span data-stu-id="753ed-117">iketypes.h</span></span><br />
<span data-ttu-id="753ed-118">iketypes .idl</span><span class="sxs-lookup"><span data-stu-id="753ed-118">iketypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="753ed-119"><a href="fwp-ike-functions.md">用來</a> 管理 IKE 和 AuthIP MM 原則和安全性關聯的函式。</span><span class="sxs-lookup"><span data-stu-id="753ed-119"><a href="fwp-ike-functions.md">Functions</a> used for managing IKE and AuthIP MM policy and security associations.</span></span></td>
<td><dl> <span data-ttu-id="753ed-120">fwpmu。h</span><span class="sxs-lookup"><span data-stu-id="753ed-120">fwpmu.h</span></span><br />
<span data-ttu-id="753ed-121">fwpmk。h</span><span class="sxs-lookup"><span data-stu-id="753ed-121">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="753ed-122">IPsec API (IPSEC) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="753ed-122">IPsec API (IPSEC)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="753ed-123">用來管理 IPsec 原則和安全性關聯的<a href="fwp-enums.md">列舉類型</a>和<a href="fwp-structs.md">結構</a>。</span><span class="sxs-lookup"><span data-stu-id="753ed-123"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="753ed-124">ipsectypes。h</span><span class="sxs-lookup"><span data-stu-id="753ed-124">ipsectypes.h</span></span><br />
<span data-ttu-id="753ed-125">ipsectypes .idl</span><span class="sxs-lookup"><span data-stu-id="753ed-125">ipsectypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="753ed-126"><a href="fwp-ipsec-functions.md">用來</a> 管理 IPsec 原則和安全性關聯的函式。</span><span class="sxs-lookup"><span data-stu-id="753ed-126"><a href="fwp-ipsec-functions.md">Functions</a> used for managing IPsec policies and security associations.</span></span></td>
<td><dl> <span data-ttu-id="753ed-127">fwpmu。h</span><span class="sxs-lookup"><span data-stu-id="753ed-127">fwpmu.h</span></span><br />
<span data-ttu-id="753ed-128">fwpmk。h</span><span class="sxs-lookup"><span data-stu-id="753ed-128">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="753ed-129">管理 API (FWPM) $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="753ed-129">Management API (FWPM)${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="753ed-130">用來管理篩選引擎的<a href="fwp-enums.md">列舉類型</a>和<a href="fwp-structs.md">結構</a>。</span><span class="sxs-lookup"><span data-stu-id="753ed-130"><a href="fwp-enums.md">Enumerated types</a> and <a href="fwp-structs.md">structures</a> used for managing the filter engine.</span></span></td>
<td><dl> <span data-ttu-id="753ed-131">fwpmtypes。h</span><span class="sxs-lookup"><span data-stu-id="753ed-131">fwpmtypes.h</span></span><br />
<span data-ttu-id="753ed-132">fwpmtypes .idl</span><span class="sxs-lookup"><span data-stu-id="753ed-132">fwpmtypes.idl</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="753ed-133">用於管理篩選引擎的<a href="fwp-mgmt-functions.md">函數</a>。</span><span class="sxs-lookup"><span data-stu-id="753ed-133"><a href="fwp-mgmt-functions.md">Functions</a> used for managing the filter engine.</span></span> <span data-ttu-id="753ed-134">這些函式是用來執行下列工作：</span><span class="sxs-lookup"><span data-stu-id="753ed-134">These functions are used to perform the following tasks:</span></span><br/>
<ul>
<li><span data-ttu-id="753ed-135">設定和查詢篩選、提供者和標注。</span><span class="sxs-lookup"><span data-stu-id="753ed-135">Set and query filters, providers, and callouts.</span></span></li>
<li><span data-ttu-id="753ed-136">取出 IPsec 統計資料。</span><span class="sxs-lookup"><span data-stu-id="753ed-136">Retrieve IPsec statistics.</span></span></li>
<li><span data-ttu-id="753ed-137">設定 Windows 篩選平台。</span><span class="sxs-lookup"><span data-stu-id="753ed-137">Configure the Windows Filtering Platform.</span></span></li>
</ul></td>
<td><dl> <span data-ttu-id="753ed-138">fwpmu。h</span><span class="sxs-lookup"><span data-stu-id="753ed-138">fwpmu.h</span></span><br />
<span data-ttu-id="753ed-139">fwpmk。h</span><span class="sxs-lookup"><span data-stu-id="753ed-139">fwpmk.h</span></span><br />
</dl></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="753ed-140">共用 API (.FWP) </span><span class="sxs-lookup"><span data-stu-id="753ed-140">Shared API (FWP)</span></span></td>
<td><span data-ttu-id="753ed-141">跨 Windows 篩選平台共用的基本 <a href="fwp-enums.md">列舉類型</a> 和 <a href="fwp-structs.md">結構</a> 。</span><span class="sxs-lookup"><span data-stu-id="753ed-141">Fundamental <a href="fwp-enums.md">enumerated types</a> and <a href="fwp-structs.md">structures</a> shared across the Windows Filtering Platform.</span></span></td>
<td><dl> <span data-ttu-id="753ed-142">fwptypes。h</span><span class="sxs-lookup"><span data-stu-id="753ed-142">fwptypes.h</span></span><br />
<span data-ttu-id="753ed-143">fwptypes .idl</span><span class="sxs-lookup"><span data-stu-id="753ed-143">fwptypes.idl</span></span><br />
</dl></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="753ed-144">資料型別名稱全都是大寫和底線分隔。</span><span class="sxs-lookup"><span data-stu-id="753ed-144">Data type names are all upper-case and underscore-delimited.</span></span> <span data-ttu-id="753ed-145">名稱的開頭一律是識別其元件群組的前置詞，例如 [**FWPM \_ PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0)。</span><span class="sxs-lookup"><span data-stu-id="753ed-145">The name always begins with a prefix that identifies its component group, such as [**FWPM\_PROVIDER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_provider0).</span></span>

<span data-ttu-id="753ed-146">函式名稱為混合大小寫和以大小寫分隔。</span><span class="sxs-lookup"><span data-stu-id="753ed-146">Function names are mixed-case and case-delimited.</span></span> <span data-ttu-id="753ed-147">名稱的開頭一律是識別其元件群組的前置詞，例如 [**FwpmProviderCoNtextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0)。</span><span class="sxs-lookup"><span data-stu-id="753ed-147">The name always begins with a prefix that identifies its component group, such as [**FwpmProviderContextAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmprovidercontextadd0).</span></span>

<span data-ttu-id="753ed-148">大部分資料和函式名稱的結尾都是版本號碼。</span><span class="sxs-lookup"><span data-stu-id="753ed-148">Most data and function names end with a version number.</span></span> <span data-ttu-id="753ed-149">Fwpvi .h 標頭檔會將與版本無關的資料和函式名稱對應至適用于指定作業系統的版本。</span><span class="sxs-lookup"><span data-stu-id="753ed-149">The fwpvi.h header file maps version-independent data and function names to the version that is appropriate for use with a given operating system.</span></span> <span data-ttu-id="753ed-150">如需詳細資訊，請參閱 [WFP Version-Independent 名稱，並以特定的 Windows 版本為目標](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md)。</span><span class="sxs-lookup"><span data-stu-id="753ed-150">For more information, see [WFP Version-Independent Names and Targeting Specific Versions of Windows](wfp-version-independent-names-and-targeting-specific-versions-of-windows.md).</span></span>

<span data-ttu-id="753ed-151">每個元件都不會獨立。</span><span class="sxs-lookup"><span data-stu-id="753ed-151">Each component does not stand alone.</span></span> <span data-ttu-id="753ed-152">例如，IKE 主要模式 (MM) 原則會定義在 IKEEXT 元件中，但會儲存在提供者內容中，並與在 FWPM API 元件中找到的篩選準則相關聯。</span><span class="sxs-lookup"><span data-stu-id="753ed-152">For example, IKE main mode (MM) policies are defined in the IKEEXT component, but are stored in a provider context and are associated with a filter both of which are found in the FWPM API component.</span></span>

## <a name="user-mode-and-kernel-mode-public-header-files"></a><span data-ttu-id="753ed-153">User-Mode 和 Kernel-Mode 公用標頭檔</span><span class="sxs-lookup"><span data-stu-id="753ed-153">User-Mode and Kernel-Mode Public Header Files</span></span>

<span data-ttu-id="753ed-154">您可以從使用者模式或核心模式呼叫大部分的 WFP 函數。</span><span class="sxs-lookup"><span data-stu-id="753ed-154">Most of the WFP functions can be called from either user mode or kernel mode.</span></span> <span data-ttu-id="753ed-155">不過，使用者模式函數會傳回代表 Win32 錯誤碼的 **DWORD** 值，而核心模式函數則會傳回代表 NT 狀態碼的 **NTSTATUS** 值。</span><span class="sxs-lookup"><span data-stu-id="753ed-155">However, user-mode functions return a **DWORD** value that represents a Win32 error code, whereas kernel-mode functions return an **NTSTATUS** value that represents an NT status code.</span></span> <span data-ttu-id="753ed-156">因此，使用者模式和核心模式之間的函式名稱和語義都相同，但函式簽章則否。</span><span class="sxs-lookup"><span data-stu-id="753ed-156">As a result, function names and semantics are identical between user mode and kernel mode, but function signatures are not.</span></span> <span data-ttu-id="753ed-157">這需要函式原型的不同使用者模式和核心模式的特定標頭。</span><span class="sxs-lookup"><span data-stu-id="753ed-157">This requires separate user-mode and kernel-mode specific headers for the function prototypes.</span></span> <span data-ttu-id="753ed-158">使用者模式標頭檔名稱的結尾是 "u"，核心模式標頭檔名稱則以 "k" 結尾。</span><span class="sxs-lookup"><span data-stu-id="753ed-158">User-mode header file names end in "u" and kernel-mode header file names end in "k".</span></span>

<span data-ttu-id="753ed-159">下表列出定義 WFP 函數的 Win32 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="753ed-159">The following table lists the Win32 header files that define the WFP functions.</span></span>

| <span data-ttu-id="753ed-160">標頭檔</span><span class="sxs-lookup"><span data-stu-id="753ed-160">Header Files</span></span> | <span data-ttu-id="753ed-161">Description</span><span class="sxs-lookup"><span data-stu-id="753ed-161">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
|--------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="753ed-162">fwpmk。h</span><span class="sxs-lookup"><span data-stu-id="753ed-162">fwpmk.h</span></span>      | <span data-ttu-id="753ed-163">FWPM、IPsec 和 IKEEXT 元件的核心模式函數原型。</span><span class="sxs-lookup"><span data-stu-id="753ed-163">Kernel-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="753ed-164">僅適用于 DDK。</span><span class="sxs-lookup"><span data-stu-id="753ed-164">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| <span data-ttu-id="753ed-165">fwpmu。h</span><span class="sxs-lookup"><span data-stu-id="753ed-165">fwpmu.h</span></span>      | <span data-ttu-id="753ed-166">FWPM、IPsec 和 IKEEXT 元件的使用者模式函數原型。</span><span class="sxs-lookup"><span data-stu-id="753ed-166">User-mode function prototypes for FWPM, IPsec, and IKEEXT components.</span></span> <span data-ttu-id="753ed-167">僅適用于 Microsoft Windows 軟體開發套件 (SDK) 。</span><span class="sxs-lookup"><span data-stu-id="753ed-167">Available in the Microsoft Windows Software Development Kit (SDK) only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="753ed-168">fwpsk。h</span><span class="sxs-lookup"><span data-stu-id="753ed-168">fwpsk.h</span></span>      | <span data-ttu-id="753ed-169">FWPS 元件的核心模式函數原型和列舉類型。</span><span class="sxs-lookup"><span data-stu-id="753ed-169">Kernel-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="753ed-170">僅適用于 DDK。</span><span class="sxs-lookup"><span data-stu-id="753ed-170">Available in the DDK only.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="753ed-171">fwpsu。h</span><span class="sxs-lookup"><span data-stu-id="753ed-171">fwpsu.h</span></span>      | <span data-ttu-id="753ed-172">FWPS 元件的使用者模式函數原型和列舉類型。</span><span class="sxs-lookup"><span data-stu-id="753ed-172">User-mode function prototypes and enumerated types for FWPS component.</span></span> <span data-ttu-id="753ed-173">僅適用于 Windows SDK。**注意**  使用者模式 FWPS 列舉類型與核心模式 FWPS 列舉類型相同。</span><span class="sxs-lookup"><span data-stu-id="753ed-173">Available in the Windows SDK only.**Note**  The user-mode FWPS enumerated types are identical to the kernel-mode FWPS enumerated types.</span></span> <span data-ttu-id="753ed-174">因此，這些類型只記錄在 DDK 中。</span><span class="sxs-lookup"><span data-stu-id="753ed-174">In consequence, these types are documented in the DDK only.</span></span><br/> <span data-ttu-id="753ed-175">**注意**  使用者模式 FWPS 函式原型與核心模式 FWPS 函式原型相同，但傳回碼例外。</span><span class="sxs-lookup"><span data-stu-id="753ed-175">**Note**  The user-mode FWPS function prototypes are identical to the kernel-mode FWPS function prototypes with the exception of the return code.</span></span> <span data-ttu-id="753ed-176">使用者模式 FWPS 函式會傳回 **DWORD**，而核心模式的 FWPS 函式會傳回一個 **NTSTATUS**。</span><span class="sxs-lookup"><span data-stu-id="753ed-176">User-mode FWPS functions return a **DWORD**, whereas kernel-mode FWPS functions return an **NTSTATUS**.</span></span> <span data-ttu-id="753ed-177">因此，這些函式只會記錄在 DDK 中。</span><span class="sxs-lookup"><span data-stu-id="753ed-177">In consequence, these functions are documented in the DDK only.</span></span><br/> |



 

<span data-ttu-id="753ed-178">所有使用者模式函數都會從 fwpuclnt.dll 匯出。</span><span class="sxs-lookup"><span data-stu-id="753ed-178">All user-mode functions are exported from fwpuclnt.dll.</span></span> <span data-ttu-id="753ed-179">所有核心模式函數都會從 fwpkclnt.sys 匯出。</span><span class="sxs-lookup"><span data-stu-id="753ed-179">All kernel-mode functions are exported from fwpkclnt.sys.</span></span>

### <a name="management-fwpm-and-callout-fwps-data-types"></a><span data-ttu-id="753ed-180">管理 (FWPM) 和標注 () 資料類型</span><span class="sxs-lookup"><span data-stu-id="753ed-180">Management (FWPM) and Callout (FWPS) Data Types</span></span>

<span data-ttu-id="753ed-181">大部分的 FWPM 資料類型（用於管理工作，例如從應用程式或驅動程式新增篩選或標注）都會有 FWPS 的對應專案。</span><span class="sxs-lookup"><span data-stu-id="753ed-181">Most FWPM data types, which are used for management tasks such as adding filters or callouts from an application or driver, have FWPS counterparts.</span></span> <span data-ttu-id="753ed-182">FWPS 資料類型會在實際的網路流量篩選期間使用，而在分類的標注常式內容中。</span><span class="sxs-lookup"><span data-stu-id="753ed-182">The FWPS data types are used during the actual filtering of network traffic, in the context of a callout routine for classification.</span></span>

<span data-ttu-id="753ed-183">例如，為了將篩選加入至特定篩選引擎層，程式設計人員應該使用 FWPM 類型，例如： `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET` 。</span><span class="sxs-lookup"><span data-stu-id="753ed-183">For example, in order to add a filter to a certain filtering engine layer, the programmer should use an FWPM type, like: `filter.layerKey = FWPM_LAYER_INBOUND_IPPACKET`.</span></span> <span data-ttu-id="753ed-184">若要檢查正在呼叫標注的圖層，程式設計人員應使用對應的 FWPS 類型： ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)` 。</span><span class="sxs-lookup"><span data-stu-id="753ed-184">To check which layer a callout is being called from, the programmer should use the corresponding FWPS type: ` if (inFixedValues->layerId == FWPS_LAYER_INBOUND_IPPACKET)`.</span></span>

<span data-ttu-id="753ed-185">FWPM 資料類型的某些 FWPS 對應項會擴充原始 FWPM 資料類型。</span><span class="sxs-lookup"><span data-stu-id="753ed-185">Some FWPS counterparts to FWPM data types are expanding the original FWPM data types.</span></span> <span data-ttu-id="753ed-186">例如，若要在許多篩選引擎層級加入篩選準則，程式設計人員會指定， `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` 無論篩選引擎層為何。</span><span class="sxs-lookup"><span data-stu-id="753ed-186">For example, to add a filter condition at many filtering engine layers, the programmer specifies the `filterCondition.fieldKey = FWPM_CONDITION_IP_PROTOCOL` regardless of the filtering engine layer.</span></span> <span data-ttu-id="753ed-187">為了尋找篩選準則值，程式設計人員會指定圖層特定的 FWPS 類型，例如： `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]` 。</span><span class="sxs-lookup"><span data-stu-id="753ed-187">To find a filter condition value, the programmer specifies a layer specific FWPS type, like: `inFixedValues->incomingValue[FWPS_FIELD_ALE_FLOW_ESTABLISHED_V4_IP_PROTOCOL]`.</span></span>

<span data-ttu-id="753ed-188">FWPS 資料類型通常小於其 FWPM 對應專案。</span><span class="sxs-lookup"><span data-stu-id="753ed-188">The FWPS data types are generally smaller than their FWPM counterparts.</span></span> <span data-ttu-id="753ed-189">例如， [**FWPM 篩選層識別碼**](management-filtering-layer-identifiers-.md) 是 (16 個位元組的 **GUID**) ，而 [FWPS 篩選層識別碼](/windows-hardware/drivers/network/management-filtering-layer-identifiers) 則為 **UINT16** (16 位) 。</span><span class="sxs-lookup"><span data-stu-id="753ed-189">For example, the [**FWPM filtering layer identifiers**](management-filtering-layer-identifiers-.md) are **GUID** s (16-bytes) whereas the [FWPS filtering layer identifiers](/windows-hardware/drivers/network/management-filtering-layer-identifiers) are **UINT16** (16-bits).</span></span> <span data-ttu-id="753ed-190">FWPS 資料類型的較小大小可改善系統效能，因為整數比較超過了即時流量的 **GUID** 比較。</span><span class="sxs-lookup"><span data-stu-id="753ed-190">The smaller size for FWPS data types improves system performance since integer comparisons outweigh **GUID** comparisons for real-time traffic.</span></span> <span data-ttu-id="753ed-191">此外，核心記憶體會有效率地使用，因為 FWPS 類型全都在核心中用來管理篩選，而 FWPM 類型則以使用者模式儲存以管理不同的層級。</span><span class="sxs-lookup"><span data-stu-id="753ed-191">Also, the kernel memory is used efficiently since the FWPS types are all used in the kernel for managing the filters, whereas the FWPM types are stored in user-mode to manage the different layers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="753ed-192">相關主題</span><span class="sxs-lookup"><span data-stu-id="753ed-192">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="753ed-193">WFP API 物件模型</span><span class="sxs-lookup"><span data-stu-id="753ed-193">WFP API Object Model</span></span>](object-model.md)
</dt> <dt>

[<span data-ttu-id="753ed-194">WFP API 物件管理</span><span class="sxs-lookup"><span data-stu-id="753ed-194">WFP API Object Management</span></span>](object-management.md)
</dt> </dl>

