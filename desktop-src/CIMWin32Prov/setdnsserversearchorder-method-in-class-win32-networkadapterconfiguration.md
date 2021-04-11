---
description: SetDNSServerSearchOrder &\# 32;WMI 類別方法會使用 string 元素陣列來設定伺服器搜尋順序。
ms.assetid: fce688fa-7264-4965-8e1c-138160e03a7e
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetDNSServerSearchOrder 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSServerSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2bfe731ea1d89e8e0ad702bfa229a61fba30dfc7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025960"
---
# <a name="setdnsserversearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="0ee19-103">Win32 >networkadapterconfiguration 類別的 SetDNSServerSearchOrder 方法 \_</span><span class="sxs-lookup"><span data-stu-id="0ee19-103">SetDNSServerSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="0ee19-104">**SetDNSServerSearchOrder** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會使用 string 元素陣列來設定伺服器搜尋順序。</span><span class="sxs-lookup"><span data-stu-id="0ee19-104">The **SetDNSServerSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method uses an array of string elements to set the server search order.</span></span>

<span data-ttu-id="0ee19-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="0ee19-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="0ee19-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="0ee19-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="0ee19-107">語法</span><span class="sxs-lookup"><span data-stu-id="0ee19-107">Syntax</span></span>


```mof
uint32 SetDNSServerSearchOrder(
  [in] string DNSServerSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="0ee19-108">參數</span><span class="sxs-lookup"><span data-stu-id="0ee19-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0ee19-109">*DNSServerSearchOrder* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0ee19-109">*DNSServerSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0ee19-110">要查詢 DNS 伺服器的伺服器 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="0ee19-110">List of server IP addresses to query for DNS servers.</span></span>

<span data-ttu-id="0ee19-111">範例：130.215.24.1 或157.54.164。1</span><span class="sxs-lookup"><span data-stu-id="0ee19-111">Example: 130.215.24.1 or 157.54.164.1</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0ee19-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="0ee19-112">Return value</span></span>

<span data-ttu-id="0ee19-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="0ee19-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="0ee19-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="0ee19-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="0ee19-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="0ee19-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="0ee19-116">**成功完成，不需要重新開機** (0) </span><span class="sxs-lookup"><span data-stu-id="0ee19-116">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-117">**成功完成，需要重新開機** (1) </span><span class="sxs-lookup"><span data-stu-id="0ee19-117">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-118">**此平臺 (64) 不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="0ee19-118">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-119">**未知的失敗** (65) </span><span class="sxs-lookup"><span data-stu-id="0ee19-119">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-120">**不正確子網路遮罩** (66) </span><span class="sxs-lookup"><span data-stu-id="0ee19-120">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-121">**處理傳回的實例時發生錯誤** (67) </span><span class="sxs-lookup"><span data-stu-id="0ee19-121">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-122">**不正確輸入參數** (68) </span><span class="sxs-lookup"><span data-stu-id="0ee19-122">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-123"> (69) **指定超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="0ee19-123">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-124">**不正確 IP 位址** (70) </span><span class="sxs-lookup"><span data-stu-id="0ee19-124">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-125">**不正確閘道 IP 位址** (71) </span><span class="sxs-lookup"><span data-stu-id="0ee19-125">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-126">**存取所要求資訊** 的登錄時發生錯誤 (72) </span><span class="sxs-lookup"><span data-stu-id="0ee19-126">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-127">**不正確功能變數名稱** (73) </span><span class="sxs-lookup"><span data-stu-id="0ee19-127">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-128">**不正確主機名稱** (74) </span><span class="sxs-lookup"><span data-stu-id="0ee19-128">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-129">**未定義任何主要/次要 WINS 伺服器** (75) </span><span class="sxs-lookup"><span data-stu-id="0ee19-129">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-130">**不正確檔** (76) </span><span class="sxs-lookup"><span data-stu-id="0ee19-130">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-131">**不正確系統路徑** (77) </span><span class="sxs-lookup"><span data-stu-id="0ee19-131">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-132">檔案 **複製失敗** (78) </span><span class="sxs-lookup"><span data-stu-id="0ee19-132">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-133"> (79) 的 **安全性參數無效**</span><span class="sxs-lookup"><span data-stu-id="0ee19-133">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-134">**無法設定 tcp/ip 服務** (80) </span><span class="sxs-lookup"><span data-stu-id="0ee19-134">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-135">**無法設定 DHCP 服務** (81) </span><span class="sxs-lookup"><span data-stu-id="0ee19-135">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-136">**無法更新 DHCP 租用** (82) </span><span class="sxs-lookup"><span data-stu-id="0ee19-136">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-137">**無法釋放 DHCP 租用** (83) </span><span class="sxs-lookup"><span data-stu-id="0ee19-137">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-138">**介面卡上未啟用 IP** (84) </span><span class="sxs-lookup"><span data-stu-id="0ee19-138">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-139">**未在介面卡上啟用 IPX** (85) </span><span class="sxs-lookup"><span data-stu-id="0ee19-139">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-140">**畫面格/網路編號界限錯誤** (86) </span><span class="sxs-lookup"><span data-stu-id="0ee19-140">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-141">**不正確框架類型** (87) </span><span class="sxs-lookup"><span data-stu-id="0ee19-141">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-142"> (88) 的 **網路編號無效**</span><span class="sxs-lookup"><span data-stu-id="0ee19-142">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-143"> (89) **重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="0ee19-143">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-144">**參數超出範圍** (90) </span><span class="sxs-lookup"><span data-stu-id="0ee19-144">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-145">**拒絕存取** (91) </span><span class="sxs-lookup"><span data-stu-id="0ee19-145">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-146">**記憶體不足** (92) </span><span class="sxs-lookup"><span data-stu-id="0ee19-146">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-147">**已存在** (93) </span><span class="sxs-lookup"><span data-stu-id="0ee19-147">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-148">**找不到路徑、檔案或物件** (94) </span><span class="sxs-lookup"><span data-stu-id="0ee19-148">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-149">**無法通知服務** (95) </span><span class="sxs-lookup"><span data-stu-id="0ee19-149">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-150">**無法通知 DNS 服務** (96) </span><span class="sxs-lookup"><span data-stu-id="0ee19-150">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-151">**介面無法** 設定 (97) </span><span class="sxs-lookup"><span data-stu-id="0ee19-151">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-152">**並非所有 DHCP 租用都** 可以釋出/更新 (98) </span><span class="sxs-lookup"><span data-stu-id="0ee19-152">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-153">**未在介面卡上啟用 DHCP** (100) </span><span class="sxs-lookup"><span data-stu-id="0ee19-153">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="0ee19-154">**其他** (101 4294967295) </span><span class="sxs-lookup"><span data-stu-id="0ee19-154">**Other** (101 4294967295)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="0ee19-155">備註</span><span class="sxs-lookup"><span data-stu-id="0ee19-155">Remarks</span></span>

<span data-ttu-id="0ee19-156">這是每個介面卡上套用的實例相依方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="0ee19-156">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="0ee19-157">指定靜態 DNS 伺服器來開始使用動態主機設定通訊協定 (DHCP) 而不是靜態 DNS 伺服器，您可以呼叫方法，而不需提供 "in" 參數。</span><span class="sxs-lookup"><span data-stu-id="0ee19-157">After static DNS servers are specified to start using Dynamic Host Configuration Protocol (DHCP) instead of static DNS servers, you can call the method without supplying "in" parameters.</span></span>

## <a name="examples"></a><span data-ttu-id="0ee19-158">範例</span><span class="sxs-lookup"><span data-stu-id="0ee19-158">Examples</span></span>

<span data-ttu-id="0ee19-159">TechNet 資源庫上的 [多部電腦在組織單位的 VBScript 範例中設定 Dns 伺服器搜尋順序](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) ，可針對屬於一個組織單位的多部電腦，取得或設定 dns 伺服器搜尋順序。</span><span class="sxs-lookup"><span data-stu-id="0ee19-159">The [Set DNS Server Search Order for Multiple Computers in an Organizational Unit](https://Gallery.TechNet.Microsoft.Com/Set-DNS-Server-Search-6a3e3ede) VBScript sample on TechNet Gallery retrieves or sets DNS Server search order for multiple computers that belongs to one organizational unit.</span></span>

<span data-ttu-id="0ee19-160">「 [修改網路介面卡的 DNS 伺服器搜尋順序](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) 」 VBScript 範例會設定 tcp/ip 系結的網路介面卡，以使用兩部 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="0ee19-160">The [Modify the DNS Server Search Order for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/7824348c-5a92-42cb-b4e9-ef2187702e02) VBScript sample configures a TCP/IP-bound network adapter to use two DNS servers.</span></span>

## <a name="requirements"></a><span data-ttu-id="0ee19-161">規格需求</span><span class="sxs-lookup"><span data-stu-id="0ee19-161">Requirements</span></span>



| <span data-ttu-id="0ee19-162">需求</span><span class="sxs-lookup"><span data-stu-id="0ee19-162">Requirement</span></span> | <span data-ttu-id="0ee19-163">值</span><span class="sxs-lookup"><span data-stu-id="0ee19-163">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0ee19-164">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0ee19-164">Minimum supported client</span></span><br/> | <span data-ttu-id="0ee19-165">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0ee19-165">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="0ee19-166">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0ee19-166">Minimum supported server</span></span><br/> | <span data-ttu-id="0ee19-167">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0ee19-167">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0ee19-168">命名空間</span><span class="sxs-lookup"><span data-stu-id="0ee19-168">Namespace</span></span><br/>                | <span data-ttu-id="0ee19-169">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="0ee19-169">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="0ee19-170">MOF</span><span class="sxs-lookup"><span data-stu-id="0ee19-170">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0ee19-171"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="0ee19-171"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="0ee19-172">DLL</span><span class="sxs-lookup"><span data-stu-id="0ee19-172">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0ee19-173"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0ee19-173"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0ee19-174">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0ee19-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0ee19-175">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="0ee19-175">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="0ee19-176">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="0ee19-176">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="0ee19-177">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="0ee19-177">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="0ee19-178">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="0ee19-178">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="0ee19-179">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="0ee19-179">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

