---
title: 防火牆動態關鍵字
description: 您可以使用防火牆動態關鍵字 Api 來管理 Microsoft Defender 防火牆中的動態關鍵字位址。
keywords:
- 防火牆動態關鍵字
ms.topic: article
ms.date: 05/17/2021
ms.localizationpriority: low
ms.openlocfilehash: 15e35f26b72ed8d685e8302f6222836507e5c6a3
ms.sourcegitcommit: ae8c320a757558262167a4f4e385235b8d89035c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/24/2021
ms.locfileid: "112765532"
---
# <a name="firewall-dynamic-keywords"></a><span data-ttu-id="fc2ca-104">防火牆動態關鍵字</span><span class="sxs-lookup"><span data-stu-id="fc2ca-104">Firewall dynamic keywords</span></span>

<span data-ttu-id="fc2ca-105">您可以使用防火牆動態關鍵字 Api 來管理 [Microsoft Defender 防火牆](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security)中的 *動態關鍵字位址*。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-105">You use the firewall dynamic keywords APIs to manage *dynamic keyword addresses* in [Microsoft Defender Firewall](/windows/security/threat-protection/windows-firewall/windows-firewall-with-advanced-security).</span></span> <span data-ttu-id="fc2ca-106">動態關鍵字位址可用來建立一組 IP 位址，以供一或多個防火牆規則參考。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-106">A dynamic keyword address is used to create a set of IP addresses to which one or more firewall rules can refer.</span></span> <span data-ttu-id="fc2ca-107">動態關鍵字位址支援 IPv4 和 IPv6。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-107">Dynamic keyword addresses support both IPv4 and IPv6.</span></span>

> [!NOTE]
> <span data-ttu-id="fc2ca-108">如需本主題中所介紹之 Api 的 API 參考內容，請參閱 [防火牆動態關鍵字參考](firewall-dynamic-keywords-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-108">For API reference content for the APIs introduced in this topic, see [Firewall dynamic keywords reference](firewall-dynamic-keywords-reference.md).</span></span>

## <a name="operations-on-dynamic-keyword-addresses"></a><span data-ttu-id="fc2ca-109">動態關鍵字位址的作業</span><span class="sxs-lookup"><span data-stu-id="fc2ca-109">Operations on dynamic keyword addresses</span></span>

<span data-ttu-id="fc2ca-110">使用防火牆動態關鍵字 Api，您可以執行下列作業。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-110">With the Firewall dynamic keywords APIs, you can perform the following operations.</span></span>

* <span data-ttu-id="fc2ca-111">新增動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-111">Add dynamic keyword addresses</span></span>
* <span data-ttu-id="fc2ca-112">刪除動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-112">Delete dynamic keyword addresses</span></span>
* <span data-ttu-id="fc2ca-113">依識別碼或依類型列舉動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-113">Enumerate dynamic keyword addresses by ID, or by type</span></span>
* <span data-ttu-id="fc2ca-114">更新動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-114">Update dynamic keyword addresses</span></span>
* <span data-ttu-id="fc2ca-115">訂閱及處理動態關鍵字位址變更通知</span><span class="sxs-lookup"><span data-stu-id="fc2ca-115">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="fc2ca-116">本主題稍後會提供這些作業的程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-116">There are code examples for all of those operations later in this topic.</span></span>

<span data-ttu-id="fc2ca-117">當您新增動態關鍵字位址之後，它會在重新開機時持續保存。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-117">Once you've added a dynamic keyword address, it persists across reboots.</span></span> <span data-ttu-id="fc2ca-118">當您完成物件之後，就必須刪除動態關鍵字位址。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-118">You must delete a dynamic keyword address once you're done with the object.</span></span>

<span data-ttu-id="fc2ca-119">動態關鍵字位址有兩個類別，如接下來的兩節所述。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-119">There are two classes of dynamic keyword addresses, as described in the next two sections.</span></span>

## <a name="autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="fc2ca-120">自動解析動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-120">AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="fc2ca-121">第一個 *類型是可解析的*，其中 *關鍵字* 欄位代表可解析的名稱，而且在建立時不會定義 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-121">The first type is *AutoResolve*, where the *keyword* field represents a resolvable name, and the IP addresses aren't defined upon creation.</span></span>

<span data-ttu-id="fc2ca-122">這些物件的目的是要自動解析其 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-122">These objects are intended to have their IP addresses resolved automatically.</span></span> <span data-ttu-id="fc2ca-123">也就是，在建立物件時不會透過系統管理員;也不是透過作業系統 (作業系統) 本身。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-123">That is, not through an admin at object creation time; nor through the operating system (OS) itself.</span></span> <span data-ttu-id="fc2ca-124">防火牆服務外部的元件必須為這些物件進行 IP 位址解析，並適當地更新。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-124">A component outside of the firewall service must do the IP address resolution for these objects, and update them appropriately.</span></span> <span data-ttu-id="fc2ca-125">這類元件的執行範圍超出此內容的範圍。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-125">The implementation of such a component is outside the scope of this content.</span></span>

<span data-ttu-id="fc2ca-126">當呼叫 [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0)函式時，會在物件中設定 **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** 旗標，以將動態關鍵字位址表示為自動 *解析*。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-126">A dynamic keyword address is indicated as being *AutoResolve* by setting the **FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE** flag in the object when calling the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span> <span data-ttu-id="fc2ca-127">*關鍵字* 欄位應該用來表示所解析的值 &mdash; ，也就是 (FQDN) 或主機名稱的完整功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-127">The *keyword* field should be used to represent the value being resolved&mdash;that is, a fully qualified domain name (FQDN) or hostname.</span></span> <span data-ttu-id="fc2ca-128">這些物件的 [ *位址* ] 欄位一開始必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-128">The *addresses* field must initially be NULL for these objects.</span></span> <span data-ttu-id="fc2ca-129">這些物件不會在開機週期內保存其 IP 位址，您應該在下一個開機週期重新評估/重新填入其位址。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-129">These objects won't have their IP addresses persisted across boot cycles, and you should re-evaluate/re-populate their addresses during the next boot cycle.</span></span>

> [!NOTE]
> <span data-ttu-id="fc2ca-130">自動解析動態關鍵字位址物件會在 [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) 和 [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)（但不是 [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)）上觸發通知。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-130">AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) and [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), but not [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="non-autoresolve-dynamic-keyword-addresses"></a><span data-ttu-id="fc2ca-131">非自動解析動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-131">Non-AutoResolve dynamic keyword addresses</span></span>

<span data-ttu-id="fc2ca-132">第二種型別是 *不可解析* 的，其中 *關鍵字* 欄位是任何字串，而位址是在建立時定義。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-132">The second type is *non-AutoResolve*, where the *keyword* field is any string, and the addresses are defined at creation time.</span></span>

<span data-ttu-id="fc2ca-133">這些物件是用來儲存一組 IP 位址、子網或範圍。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-133">These objects are used to store a set of IP address, subnets, or ranges.</span></span> <span data-ttu-id="fc2ca-134">這裡的 *關鍵字* 欄位可用於管理便利性，而且可以設定為任何字串。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-134">The *keyword* field here is used for management convenience, and it can be set to any string.</span></span> <span data-ttu-id="fc2ca-135">建立時，[ *位址* ] 欄位必須為非 Null。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-135">The *addresses* field must be non-NULL upon creation.</span></span> <span data-ttu-id="fc2ca-136">這些物件的位址會在重新開機時持續保存。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-136">Addresses for these objects are persisted across reboots.</span></span>

> [!NOTE]
> <span data-ttu-id="fc2ca-137">非自動解析動態關鍵字位址物件會在 [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0)、 [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0)和 [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0)上觸發通知。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-137">Non-AutoResolve dynamic keyword address objects trigger notifications on [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0), [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0), and also [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0).</span></span>

## <a name="more-about-dynamic-keyword-addresses"></a><span data-ttu-id="fc2ca-138">深入瞭解動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-138">More about dynamic keyword addresses</span></span> 

<span data-ttu-id="fc2ca-139">所有動態關鍵字位址都必須有唯一的 [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) 識別碼來代表它們。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-139">All dynamic keyword addresses must have a unique [**GUID**](/windows/win32/api/guiddef/ns-guiddef-guid) identifier to represent them.</span></span>

<span data-ttu-id="fc2ca-140">當動態關鍵字位址變更時， [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) API 會將通知傳遞給用戶端。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-140">The [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) API delivers notifications to a client when dynamic keyword addresses change.</span></span> <span data-ttu-id="fc2ca-141">未提供任何承載給用戶端，以描述系統上的變更。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-141">There's no payload delivered to the client describing exactly what changed on the system.</span></span> <span data-ttu-id="fc2ca-142">如果您需要知道哪些物件已變更，則應該使用 [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) 或 [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) api 查詢系統上物件的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-142">If you need to know what objects changed, then you should query the current state of objects on the system using the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) or [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) APIs.</span></span> <span data-ttu-id="fc2ca-143">您可以使用各種旗標來要求物件子集的通知。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-143">You can use the various flags to request notifications for only a subset of objects.</span></span> <span data-ttu-id="fc2ca-144">如果您沒有使用旗標，則會為所有物件傳遞變更通知。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-144">If you use no flags, then change notifications will be delivered for all objects.</span></span>

<span data-ttu-id="fc2ca-145">防火牆規則可以使用動態關鍵字位址，而不是明確定義其遠端位址條件的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-145">A firewall rule can use dynamic keyword addresses instead of explicitly defining IP addresses for its remote address condition.</span></span> <span data-ttu-id="fc2ca-146">防火牆規則可以同時使用動態關鍵字位址和靜態定義的遠端位址範圍。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-146">A firewall rule can use both dynamic keyword addresses and statically defined remote address ranges.</span></span> <span data-ttu-id="fc2ca-147">單一動態關鍵字位址物件可以跨多個防火牆規則重複使用。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-147">A single dynamic keyword address object can be re-used across multiple firewall rules.</span></span> <span data-ttu-id="fc2ca-148">如果防火牆規則沒有任何已設定的遠端位址 (也就是僅設定了尚未解析) 的自動解析物件，則不會強制執行此規則。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-148">If a firewall rule doesn't have any configured remote addresses (that is, configured with only AutoResolve objects which have not yet been resolved), then the rule won't be enforced.</span></span> <span data-ttu-id="fc2ca-149">此外，如果規則使用多個動態關鍵字位址，則會針對目前已解決的所有位址強制執行規則，即使有其他物件尚未解決也一樣。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-149">Furthermore, if a rule uses multiple dynamic keyword addresses, then the rule will be enforced for all addresses that are currently resolved, even if there are other objects that are not yet resolved.</span></span> <span data-ttu-id="fc2ca-150">當動態關鍵字位址更新時，所有相關聯的規則物件也會更新其遠端位址。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-150">When a dynamic keyword address is updated, all associated rule objects will have their remote addresses updated as well.</span></span>

<span data-ttu-id="fc2ca-151">作業系統 (作業系統) 本身不會強制執行規則與動態關鍵字位址之間的任何相依性。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-151">The operating system (OS) itself doesn't enforce any dependencies between a rule and a dynamic keyword address.</span></span> <span data-ttu-id="fc2ca-152">這表示可以先建立一個物件 &mdash; ，規則可以參考尚未存在的動態關鍵字位址識別碼 (在這種情況下，不會) 強制執行此規則。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-152">This means that either object can be created first&mdash;the rule can reference dynamic keyword address IDs that don't yet exist (in which case, the rule won't be enforced).</span></span> <span data-ttu-id="fc2ca-153">此外，您也可以刪除動態關鍵字位址，即使它是由防火牆規則所使用也一樣。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-153">Furthermore, you can delete a dynamic keyword address even if it's in use by a firewall rule.</span></span> <span data-ttu-id="fc2ca-154">本主題概述系統管理員如何設定規則以使用動態關鍵字位址。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-154">This topic outlines how an admin can configure rules to use dynamic keyword address.</span></span>

## <a name="code-examples"></a><span data-ttu-id="fc2ca-155">程式碼範例</span><span class="sxs-lookup"><span data-stu-id="fc2ca-155">Code examples</span></span>

<span data-ttu-id="fc2ca-156">若要嘗試每個程式碼範例，請先啟動 Visual Studio，並根據 **主控台應用程式** 專案範本建立新專案。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-156">To try out each of these code examples, first launch Visual Studio and create a new project based on the **Console App** project template.</span></span> <span data-ttu-id="fc2ca-157">您可以直接使用程式代碼清單取代的內容 `main.cpp` 。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-157">You can just replace the contents of `main.cpp` with the code listing.</span></span>

<span data-ttu-id="fc2ca-158">大部分的程式碼範例會使用 [Windows 執行程式庫 (的) ](https://github.com/Microsoft/wil)。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-158">Most of the code examples use the [Windows Implementation Libraries (WIL)](https://github.com/Microsoft/wil).</span></span> <span data-ttu-id="fc2ca-159">安裝 go 的便利方式是移至 Visual Studio，按一下 [ **Project** \> **管理 NuGet 封裝** \> **]**，在搜尋方塊中輸入或貼上 **ImplementationLibrary** ，在搜尋結果中選取專案，然後按一下 [ **安裝** ] 以安裝該專案的套件。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-159">A convenient way to install WIL is to go to Visual Studio, click **Project** \> **Manage NuGet Packages...** \> **Browse**, type or paste **Microsoft.Windows.ImplementationLibrary** in the search box, select the item in search results, and then click **Install** to install the package for that project.</span></span>

> [!NOTE]
> <span data-ttu-id="fc2ca-160">NetFw free 函式的指標類型是透過發行 `NetFw.h` ，但是靜態程式庫則不會發行。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-160">Pointer types for the NetFw free functions are published via `NetFw.h`, but a static-link library isn't published.</span></span> <span data-ttu-id="fc2ca-161">使用[LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw) / [GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)模式來呼叫這些函式，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-161">Use the [LoadLibraryExW](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexw)/[GetProcAddress](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) pattern for calling these functions, as shown in these code examples.</span></span>

### <a name="add-a-dynamic-keyword-address"></a><span data-ttu-id="fc2ca-162">新增動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-162">Add a dynamic keyword address</span></span>

<span data-ttu-id="fc2ca-163">此範例示範如何使用 [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) 函數。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-163">This example shows how to use the [**FWAddDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwadddynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWADDDYNAMICKEYWORDADDRESS0 addDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    FW_DYNAMIC_KEYWORD_ADDRESS0 autoResolveKeywordAddress = { 0 };
    FW_DYNAMIC_KEYWORD_ADDRESS0 nonAutoResolveKeywordAddress = { 0 };

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        addDynamicKeywordAddressFn = (PFN_FWADDDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWAddDynamicKeywordAddress0"
        );
    }

    if (addDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Ensure the ID is unique. If not, the add operation will fail with ERROR_ALREADY_EXISTS
    // and you should invoke the API with a new ID.

    // Initialize and add an auto-resolve dynamic keyword address
    autoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_1;
    autoResolveKeywordAddress.keyword = L"bing.com";
    autoResolveKeywordAddress.flags = FW_DYNAMIC_KEYWORD_ADDRESS_FLAGS_AUTO_RESOLVE;
    // must be NULL as we have set the auto resolve flag
    autoResolveKeywordAddress.addresses = NULL;

    error = addDynamicKeywordAddressFn(&autoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    // Initialize and add a non auto-resolve dynamic keyword address
    nonAutoResolveKeywordAddress.id = DYNAMIC_KEYWORD_ADDRESS_ID_2;
    nonAutoResolveKeywordAddress.keyword = L"myServerIPs";
    nonAutoResolveKeywordAddress.flags = 0;
    nonAutoResolveKeywordAddress.addresses = L"10.0.0.5,20.0.0.0/24,30.0.0.0-40.0.0.0";

    error = addDynamicKeywordAddressFn(&nonAutoResolveKeywordAddress);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }
    return error;
}
```

### <a name="delete-a-dynamic-keyword-address"></a><span data-ttu-id="fc2ca-164">刪除動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-164">Delete a dynamic keyword address</span></span>

<span data-ttu-id="fc2ca-165">此範例示範如何使用 [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) 函數。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-165">This example shows how to use the [**FWDeleteDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwdeletedynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};


// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWDELETEDYNAMICKEYWORDADDRESS0 deleteDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });


    if (moduleHandle != NULL)
    {
        deleteDynamicKeywordAddressFn = (PFN_FWDELETEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWDeleteDynamicKeywordAddress0"
        );
    }

    if (deleteDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the functions
    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_1);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 1, err=[%d]", error);
    }

    error = deleteDynamicKeywordAddressFn(DYNAMIC_KEYWORD_ADDRESS_ID_2);
    if (error != ERROR_SUCCESS)
    {
        wprintf(L"Failed to delete object with ID 2, err=[%d]", error);
    }

    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-id"></a><span data-ttu-id="fc2ca-166">依識別碼列舉和釋放動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-166">Enumerate and free dynamic keyword addresses by ID</span></span>

<span data-ttu-id="fc2ca-167">此範例示範如何使用 [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) 和 [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) 函數。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-167">This example shows how to use the [**FWEnumDynamicKeywordAddressById0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressbyid0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

// {e9d5c993-9369-4a96-8228-9c5c37aac51a}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_2 =
{
    0xe9d5c993,
    0x9369,
    0x4a96,
    {0x82,0x28,0x9c,0x5c,0x37,0xaa,0xc5,0x1a}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0 enumDynamicKeywordAddressByIdFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressByIdFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSBYID0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressById0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressByIdFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    error = enumDynamicKeywordAddressByIdFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    if (dynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address
    }

    // Free the dynamic keyword address
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);
    return error;
}
```

### <a name="enumerate-and-free-dynamic-keyword-addresses-by-type"></a><span data-ttu-id="fc2ca-168">依類型列舉和釋放動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-168">Enumerate and free dynamic keyword addresses by type</span></span>

<span data-ttu-id="fc2ca-169">此範例示範如何使用 [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) 和 [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) 函數。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-169">This example shows how to use the [**FWEnumDynamicKeywordAddressesByType0**](/windows/win32/api/netfw/nc-netfw-pfn_fwenumdynamickeywordaddressesbytype0) and [**FWFreeDynamicKeywordAddressData0**](/windows/win32/api/netfw/nc-netfw-pfn_fwfreedynamickeywordaddressdata0) functions.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke enum for ALL dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_ALL,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        // iterate to the next one in the list
        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    return error;
}
```

### <a name="update-dynamic-keyword-addresses"></a><span data-ttu-id="fc2ca-170">更新動態關鍵字位址</span><span class="sxs-lookup"><span data-stu-id="fc2ca-170">Update dynamic keyword addresses</span></span>

<span data-ttu-id="fc2ca-171">此範例示範如何使用 [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) 函數。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-171">This example shows how to use the [**FWUpdateDynamicKeywordAddress0**](/windows/win32/api/netfw/nc-netfw-pfn_fwupdatedynamickeywordaddress0) function.</span></span>

```cpp
// main.cpp in a Console App project.
#include <windows.h>
#include <wil/resource.h>
#include <netfw.h>

// {26548e4f-d486-4a1d-8a1d-22b0837cd53b}
const GUID DYNAMIC_KEYWORD_ADDRESS_ID_1 =
{
    0x26548e4f,
    0xd486,
    0x4a1d,
    {0x8a,0x1d,0x22,0xb0,0x83,0x7c,0xd5,0x3b}
};

int main()
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWUPDATEDYNAMICKEYWORDADDRESS0 updateDynamicKeywordAddressFn = NULL;
    HMODULE moduleHandle = NULL;
    BOOL appendToCurrentAddresses = TRUE;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryExW(L"firewallapi.dll", NULL, LOAD_LIBRARY_SEARCH_SYSTEM32);
    auto onExitFreeModuleHandle = wil::scope_exit([&]
        {
            if (moduleHandle)
            {
                FreeLibrary(moduleHandle);
            }
        });

    if (moduleHandle != NULL)
    {
        updateDynamicKeywordAddressFn = (PFN_FWUPDATEDYNAMICKEYWORDADDRESS0)GetProcAddress(
            moduleHandle,
            "FWUpdateDynamicKeywordAddress0"
        );
    }

    if (updateDynamicKeywordAddressFn == NULL)
    {
        error = GetLastError();
        return error;
    }

    // Invoke the function
    error = updateDynamicKeywordAddressFn(
        DYNAMIC_KEYWORD_ADDRESS_ID_1,
        L"20.0.0.5",
        appendToCurrentAddresses);
    return error;
}
```

### <a name="subscribe-to-and-handle-dynamic-keyword-address-change-notifications"></a><span data-ttu-id="fc2ca-172">訂閱及處理動態關鍵字位址變更通知</span><span class="sxs-lookup"><span data-stu-id="fc2ca-172">Subscribe to, and handle, dynamic keyword address change notifications</span></span>

<span data-ttu-id="fc2ca-173">這個範例示範如何使用 [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) 和 [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) 函數以及 [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) 回呼。</span><span class="sxs-lookup"><span data-stu-id="fc2ca-173">This example shows how to use the [**FwpmDynamicKeywordSubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordsubscribe0) and [**FwpmDynamicKeywordUnsubscribe0**](/windows/win32/api/fwpmu/nf-fwpmu-fwpmdynamickeywordunsubscribe0) functions, and the [**FWPM_DYNAMIC_KEYWORD_CALLBACK0**](/windows/win32/api/fwpmu/nc-fwpmu-fwpm_dynamic_keyword_callback0) callback.</span></span>

```cppwinrt
// main.cpp in a Console App project.
#include <windows.h>
#include <netfw.h>
#include <fwpmu.h>
#pragma comment(lib, "Fwpuclnt")

void CALLBACK TestCallback(_Inout_ VOID* /*pNotification*/, _Inout_ VOID* pContext)
{
    DWORD error = ERROR_SUCCESS;
    PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0 enumDynamicKeywordAddressesByTypeFn = NULL;
    PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0 freeDynamicKeywordAddressDataFn = NULL;
    HMODULE moduleHandle = NULL;

    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 dynamicKeywordAddressData = NULL;
    PFW_DYNAMIC_KEYWORD_ADDRESS_DATA0 currDynamicKeywordAddressData = NULL;
    HANDLE* waitHandle = (HANDLE*)pContext;

    // Use LoadLibrary/GetProcAddress to invoke this function
    moduleHandle = LoadLibraryW(L"firewallapi.dll");
    if (moduleHandle != NULL)
    {
        enumDynamicKeywordAddressesByTypeFn = (PFN_FWENUMDYNAMICKEYWORDADDRESSESBYTYPE0)GetProcAddress(
            moduleHandle,
            "FWEnumDynamicKeywordAddressesByType0"
        );
        freeDynamicKeywordAddressDataFn = (PFN_FWFREEDYNAMICKEYWORDADDRESSDATA0)GetProcAddress(
            moduleHandle,
            "FWFreeDynamicKeywordAddressData0"
        );
    }

    if (enumDynamicKeywordAddressesByTypeFn == NULL ||
        freeDynamicKeywordAddressDataFn == NULL)
    {
        return;
    }

    // Invoke enum for ALL AutoResolve dynamic keyword addresses
    error = enumDynamicKeywordAddressesByTypeFn(
        FW_DYNAMIC_KEYWORD_ADDRESS_ENUM_FLAGS_AUTO_RESOLVE,
        &dynamicKeywordAddressData
    );
    if (error != ERROR_SUCCESS)
    {
        return;
    }

    currDynamicKeywordAddressData = dynamicKeywordAddressData;
    while (currDynamicKeywordAddressData != NULL)
    {
        // Process this dynamic keyword address

        currDynamicKeywordAddressData = currDynamicKeywordAddressData->next;
    }

    // Free the dynamic keyword addresses
    freeDynamicKeywordAddressDataFn(dynamicKeywordAddressData);

    SetEvent(*waitHandle);
}

int main()
{
    DWORD error = ERROR_SUCCESS;
    HANDLE notifyHandle;
    HANDLE waitHandle;

    waitHandle = CreateEventW(
        NULL,
        TRUE,
        FALSE,
        L"subscriptionWaitEvent"
    );


    // Subscribe for change notifications
    error = FwpmDynamicKeywordSubscribe0(
        FWPM_NOTIFY_ADDRESSES_AUTO_RESOLVE,
        TestCallback,
        &waitHandle,
        &notifyHandle);
    if (error != ERROR_SUCCESS)
    {
        return error;
    }

    WaitForSingleObject(waitHandle, INFINITE);

    // When client is ready to unsubscribe
    error = FwpmDynamicKeywordUnsubscribe0(notifyHandle);

    return error;
}
```

## <a name="related-topics"></a><span data-ttu-id="fc2ca-174">相關主題</span><span class="sxs-lookup"><span data-stu-id="fc2ca-174">Related topics</span></span>

* [<span data-ttu-id="fc2ca-175">防火牆動態關鍵字參考</span><span class="sxs-lookup"><span data-stu-id="fc2ca-175">Firewall dynamic keywords reference</span></span>](firewall-dynamic-keywords-reference.md)
