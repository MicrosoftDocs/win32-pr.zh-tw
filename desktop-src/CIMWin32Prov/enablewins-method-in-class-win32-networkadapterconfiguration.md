---
description: '>enablewins &\# 32;WMI 類別靜態方法可讓 Windows 網際網路命名服務 (TCP/IP 的 WINS) 設定，但與網路介面卡無關。'
ms.assetid: ce0fb170-978f-4d70-bced-e530e43da719
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 >enablewins 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableWINS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 77f5ba32606ff228908e8b7a1559a73ae5139e9c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510508"
---
# <a name="enablewins-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="17aa8-103">Win32 >networkadapterconfiguration 類別的 >enablewins 方法 \_</span><span class="sxs-lookup"><span data-stu-id="17aa8-103">EnableWINS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="17aa8-104">**>enablewins** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法可讓 WINDOWS Internet 命名服務 (tcp/ip 的 WINS) 設定，但與網路介面卡無關。</span><span class="sxs-lookup"><span data-stu-id="17aa8-104">The **EnableWINS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables Windows Internet Naming Service (WINS) settings specific to TCP/IP, but independent of the network adapter.</span></span>

<span data-ttu-id="17aa8-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="17aa8-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="17aa8-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="17aa8-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="17aa8-107">語法</span><span class="sxs-lookup"><span data-stu-id="17aa8-107">Syntax</span></span>


```mof
uint32 EnableWINS(
  [in]           boolean DNSEnabledForWINSResolution,
  [in]           boolean WINSEnableLMHostsLookup,
  [in, optional] string  WINSHostLookupFile,
  [in, optional] string  WINSScopeID
);
```



## <a name="parameters"></a><span data-ttu-id="17aa8-108">參數</span><span class="sxs-lookup"><span data-stu-id="17aa8-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17aa8-109">*DNSEnabledForWINSResolution* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17aa8-109">*DNSEnabledForWINSResolution* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17aa8-110">若 **為 true**，則會啟用網域名稱系統 (DNS) ，以透過 WINS 解析進行名稱解析。</span><span class="sxs-lookup"><span data-stu-id="17aa8-110">If **true**, the Domain Name System (DNS) is enabled for name resolution over WINS resolution.</span></span>

</dd> <dt>

<span data-ttu-id="17aa8-111">*WINSEnableLMHostsLookup* \[在\]</span><span class="sxs-lookup"><span data-stu-id="17aa8-111">*WINSEnableLMHostsLookup* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="17aa8-112">若 **為 true**，則會使用本機查閱檔案。</span><span class="sxs-lookup"><span data-stu-id="17aa8-112">If **true**, local lookup files are used.</span></span> <span data-ttu-id="17aa8-113">查閱檔案將包含 IP 位址與主機名稱的對應。</span><span class="sxs-lookup"><span data-stu-id="17aa8-113">Lookup files will contain mappings of IP addresses to host names.</span></span>

</dd> <dt>

<span data-ttu-id="17aa8-114">*WINSHostLookupFile* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="17aa8-114">*WINSHostLookupFile* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="17aa8-115">查閱檔案，其中包含 IP 位址與主機名稱的對應。</span><span class="sxs-lookup"><span data-stu-id="17aa8-115">Lookup files that contain mappings of IP addresses to host names.</span></span> <span data-ttu-id="17aa8-116">如果有的話，檔案會在% SystemRoot% \\ system32 \\ 驅動程式中找到 \\ 。</span><span class="sxs-lookup"><span data-stu-id="17aa8-116">If available, the files will be found in %SystemRoot%\\system32\\drivers\\ .</span></span>

</dd> <dt>

<span data-ttu-id="17aa8-117">*WINSScopeID* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="17aa8-117">*WINSScopeID* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="17aa8-118">將附加至電腦 NetBIOS 名稱結尾的範圍識別碼值。</span><span class="sxs-lookup"><span data-stu-id="17aa8-118">Scope identifier value that will be appended to the end of the computer's NetBIOS name.</span></span> <span data-ttu-id="17aa8-119">使用相同範圍識別碼的系統可以與這部電腦通訊。</span><span class="sxs-lookup"><span data-stu-id="17aa8-119">Systems that use the same scope identifier can communicate with this computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17aa8-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="17aa8-120">Return value</span></span>

<span data-ttu-id="17aa8-121">傳回值為 0 (零) 表示在不需要重新開機時成功完成;1 (需要重新開機時，成功完成的一) ;如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="17aa8-121">Returns a value of 0 (zero) for a successful completion when no reboot is required; 1 (one) for a successful completion when a reboot is required; a different number if there is an error.</span></span> <span data-ttu-id="17aa8-122">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="17aa8-122">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="17aa8-123">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="17aa8-123">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="17aa8-124">**成功完成，不需要重新開機** (0) </span><span class="sxs-lookup"><span data-stu-id="17aa8-124">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-125">**成功完成，需要重新開機** (1) </span><span class="sxs-lookup"><span data-stu-id="17aa8-125">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-126">**此平臺 (64) 不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="17aa8-126">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-127">**未知的失敗** (65) </span><span class="sxs-lookup"><span data-stu-id="17aa8-127">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-128">**不正確子網路遮罩** (66) </span><span class="sxs-lookup"><span data-stu-id="17aa8-128">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-129">**處理傳回的實例時發生錯誤** (67) </span><span class="sxs-lookup"><span data-stu-id="17aa8-129">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-130">**不正確輸入參數** (68) </span><span class="sxs-lookup"><span data-stu-id="17aa8-130">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-131"> (69) **指定超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="17aa8-131">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-132">**不正確 IP 位址** (70) </span><span class="sxs-lookup"><span data-stu-id="17aa8-132">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-133">**不正確閘道 IP 位址** (71) </span><span class="sxs-lookup"><span data-stu-id="17aa8-133">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-134">**存取所要求資訊** 的登錄時發生錯誤 (72) </span><span class="sxs-lookup"><span data-stu-id="17aa8-134">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-135">**不正確功能變數名稱** (73) </span><span class="sxs-lookup"><span data-stu-id="17aa8-135">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-136">**不正確主機名稱** (74) </span><span class="sxs-lookup"><span data-stu-id="17aa8-136">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-137">**未定義任何主要/次要 WINS 伺服器** (75) </span><span class="sxs-lookup"><span data-stu-id="17aa8-137">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-138">**不正確檔** (76) </span><span class="sxs-lookup"><span data-stu-id="17aa8-138">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-139">**不正確系統路徑** (77) </span><span class="sxs-lookup"><span data-stu-id="17aa8-139">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-140">檔案 **複製失敗** (78) </span><span class="sxs-lookup"><span data-stu-id="17aa8-140">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-141"> (79) 的 **安全性參數無效**</span><span class="sxs-lookup"><span data-stu-id="17aa8-141">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-142">**無法設定 tcp/ip 服務** (80) </span><span class="sxs-lookup"><span data-stu-id="17aa8-142">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-143">**無法設定 DHCP 服務** (81) </span><span class="sxs-lookup"><span data-stu-id="17aa8-143">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-144">**無法更新 DHCP 租用** (82) </span><span class="sxs-lookup"><span data-stu-id="17aa8-144">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-145">**無法釋放 DHCP 租用** (83) </span><span class="sxs-lookup"><span data-stu-id="17aa8-145">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-146">**介面卡上未啟用 IP** (84) </span><span class="sxs-lookup"><span data-stu-id="17aa8-146">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-147">**未在介面卡上啟用 IPX** (85) </span><span class="sxs-lookup"><span data-stu-id="17aa8-147">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-148">**畫面格/網路編號界限錯誤** (86) </span><span class="sxs-lookup"><span data-stu-id="17aa8-148">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-149">**不正確框架類型** (87) </span><span class="sxs-lookup"><span data-stu-id="17aa8-149">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-150"> (88) 的 **網路編號無效**</span><span class="sxs-lookup"><span data-stu-id="17aa8-150">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-151"> (89) **重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="17aa8-151">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-152">**參數超出範圍** (90) </span><span class="sxs-lookup"><span data-stu-id="17aa8-152">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-153">**拒絕存取** (91) </span><span class="sxs-lookup"><span data-stu-id="17aa8-153">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-154">**記憶體不足** (92) </span><span class="sxs-lookup"><span data-stu-id="17aa8-154">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-155">**已存在** (93) </span><span class="sxs-lookup"><span data-stu-id="17aa8-155">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-156">**找不到路徑、檔案或物件** (94) </span><span class="sxs-lookup"><span data-stu-id="17aa8-156">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-157">**無法通知服務** (95) </span><span class="sxs-lookup"><span data-stu-id="17aa8-157">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-158">**無法通知 DNS 服務** (96) </span><span class="sxs-lookup"><span data-stu-id="17aa8-158">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-159">**介面無法** 設定 (97) </span><span class="sxs-lookup"><span data-stu-id="17aa8-159">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-160">**並非所有 DHCP 租用都** 可以釋出/更新 (98) </span><span class="sxs-lookup"><span data-stu-id="17aa8-160">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-161">**未在介面卡上啟用 DHCP** (100) </span><span class="sxs-lookup"><span data-stu-id="17aa8-161">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="17aa8-162">**其他** (101 4294967295) </span><span class="sxs-lookup"><span data-stu-id="17aa8-162">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="examples"></a><span data-ttu-id="17aa8-163">範例</span><span class="sxs-lookup"><span data-stu-id="17aa8-163">Examples</span></span>

<span data-ttu-id="17aa8-164">TechNet 資源庫上的「 [啟用所有網路介面卡的 wins](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) 」 VBScript 程式碼範例會使用 **>enablewins** ，在電腦上安裝的所有網路介面卡上啟用 wins。</span><span class="sxs-lookup"><span data-stu-id="17aa8-164">The [Enable WINS for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/64cae6dd-4155-4825-ab25-5727503edf5a) VBScript code sample, on TechNet Gallery, uses **EnableWINS** to Enables WINS on all the network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="17aa8-165">規格需求</span><span class="sxs-lookup"><span data-stu-id="17aa8-165">Requirements</span></span>



| <span data-ttu-id="17aa8-166">需求</span><span class="sxs-lookup"><span data-stu-id="17aa8-166">Requirement</span></span> | <span data-ttu-id="17aa8-167">值</span><span class="sxs-lookup"><span data-stu-id="17aa8-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="17aa8-168">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="17aa8-168">Minimum supported client</span></span><br/> | <span data-ttu-id="17aa8-169">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17aa8-169">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="17aa8-170">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="17aa8-170">Minimum supported server</span></span><br/> | <span data-ttu-id="17aa8-171">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17aa8-171">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="17aa8-172">命名空間</span><span class="sxs-lookup"><span data-stu-id="17aa8-172">Namespace</span></span><br/>                | <span data-ttu-id="17aa8-173">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="17aa8-173">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="17aa8-174">MOF</span><span class="sxs-lookup"><span data-stu-id="17aa8-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="17aa8-175"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="17aa8-175"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="17aa8-176">DLL</span><span class="sxs-lookup"><span data-stu-id="17aa8-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="17aa8-177"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="17aa8-177"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17aa8-178">另請參閱</span><span class="sxs-lookup"><span data-stu-id="17aa8-178">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17aa8-179">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="17aa8-179">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="17aa8-180">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="17aa8-180">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="17aa8-181">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="17aa8-181">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="17aa8-182">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="17aa8-182">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="17aa8-183">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="17aa8-183">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

