---
description: EnableDNS WMI 類別靜態方法會啟用 service 的網域名稱系統 (DNS) 。
ms.assetid: 083dccb1-eb38-4ae5-a252-0001759c0f50
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 EnableDNS 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDNS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: fc217211455d8804de47b2b3ffc761d4328fa49a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110513"
---
# <a name="enabledns-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="4d3c6-103">Win32 >networkadapterconfiguration 類別的 EnableDNS 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4d3c6-103">EnableDNS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="4d3c6-104">**EnableDNS** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法會啟用 service 的網域名稱系統 (DNS) 。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-104">The **EnableDNS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method enables the Domain Name System (DNS) for service.</span></span>

<span data-ttu-id="4d3c6-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-105">This topic uses the Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4d3c6-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4d3c6-107">語法</span><span class="sxs-lookup"><span data-stu-id="4d3c6-107">Syntax</span></span>


```mof
uint32 EnableDNS(
  [in, optional] string DNSHostName,
  [in, optional] string DNSDomain,
  [in, optional] string DNSServerSearchOrder[],
  [in, optional] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="4d3c6-108">參數</span><span class="sxs-lookup"><span data-stu-id="4d3c6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d3c6-109">*DNSHostName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4d3c6-109">*DNSHostName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-110">此方法啟用的 DNS 主機名稱。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-110">Name of the DNS host that this method enables.</span></span>

<span data-ttu-id="4d3c6-111">範例： "corpdns"</span><span class="sxs-lookup"><span data-stu-id="4d3c6-111">Example: "corpdns"</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-112">*功能變數名稱* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4d3c6-112">*DNSDomain* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-113">表示組織名稱，後面接著句號和表示組織類型的延伸。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-113">Represents an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="4d3c6-114">範例： "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="4d3c6-114">Example: "microsoft.com"</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-115">*DNSServerSearchOrder* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4d3c6-115">*DNSServerSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-116">要查詢 DNS 伺服器的伺服器 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-116">List of server IP addresses to query for DNS servers.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-117">*DNSDomainSuffixSearchOrder* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="4d3c6-117">*DNSDomainSuffixSearchOrder* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-118">名稱解析期間附加至主機名稱的 DNS 網域尾碼。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-118">DNS domain suffix that is appended to a host name during name resolution.</span></span> <span data-ttu-id="4d3c6-119">從主機名稱) 解析完整功能變數名稱 (FQDN 時，系統會附加本機功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-119">When resolving a fully qualified domain name (FQDN) from a host-only name, the system appends the local domain name.</span></span> <span data-ttu-id="4d3c6-120">如果名稱解析不成功，系統會使用網域尾碼清單，依列出的順序建立其他 Fqdn，然後查詢每一個 Fqdn 的 DNS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-120">If the name resolution is not successful, the system uses the domain suffix list to create additional FQDNs in the order listed, and then queries DNS servers for each one.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d3c6-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d3c6-121">Return value</span></span>

<span data-ttu-id="4d3c6-122">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，以及任何其他數位（如果發生錯誤）。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="4d3c6-123">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4d3c6-124">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4d3c6-125">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-126">0</span><span class="sxs-lookup"><span data-stu-id="4d3c6-126">0</span></span>

<span data-ttu-id="4d3c6-127">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-128">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-129">1</span><span class="sxs-lookup"><span data-stu-id="4d3c6-129">1</span></span>

<span data-ttu-id="4d3c6-130">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-131">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-132">64</span><span class="sxs-lookup"><span data-stu-id="4d3c6-132">64</span></span>

<span data-ttu-id="4d3c6-133">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-134">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-135">65</span><span class="sxs-lookup"><span data-stu-id="4d3c6-135">65</span></span>

<span data-ttu-id="4d3c6-136">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-137">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-138">66</span><span class="sxs-lookup"><span data-stu-id="4d3c6-138">66</span></span>

<span data-ttu-id="4d3c6-139">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-140">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-141">67</span><span class="sxs-lookup"><span data-stu-id="4d3c6-141">67</span></span>

<span data-ttu-id="4d3c6-142">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-143">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-144">68</span><span class="sxs-lookup"><span data-stu-id="4d3c6-144">68</span></span>

<span data-ttu-id="4d3c6-145">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-146">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-147">69</span><span class="sxs-lookup"><span data-stu-id="4d3c6-147">69</span></span>

<span data-ttu-id="4d3c6-148">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-149">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-150">70</span><span class="sxs-lookup"><span data-stu-id="4d3c6-150">70</span></span>

<span data-ttu-id="4d3c6-151">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-152">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-153">71</span><span class="sxs-lookup"><span data-stu-id="4d3c6-153">71</span></span>

<span data-ttu-id="4d3c6-154">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-155">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-156">72</span><span class="sxs-lookup"><span data-stu-id="4d3c6-156">72</span></span>

<span data-ttu-id="4d3c6-157">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-158">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-159">73</span><span class="sxs-lookup"><span data-stu-id="4d3c6-159">73</span></span>

<span data-ttu-id="4d3c6-160">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-161">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-162">74</span><span class="sxs-lookup"><span data-stu-id="4d3c6-162">74</span></span>

<span data-ttu-id="4d3c6-163">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-164">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-165">75</span><span class="sxs-lookup"><span data-stu-id="4d3c6-165">75</span></span>

<span data-ttu-id="4d3c6-166">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-167">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-168">76</span><span class="sxs-lookup"><span data-stu-id="4d3c6-168">76</span></span>

<span data-ttu-id="4d3c6-169">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-170">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-171">77</span><span class="sxs-lookup"><span data-stu-id="4d3c6-171">77</span></span>

<span data-ttu-id="4d3c6-172">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-173">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-174">78</span><span class="sxs-lookup"><span data-stu-id="4d3c6-174">78</span></span>

<span data-ttu-id="4d3c6-175">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-176">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-177">79</span><span class="sxs-lookup"><span data-stu-id="4d3c6-177">79</span></span>

<span data-ttu-id="4d3c6-178">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-179">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-180">80</span><span class="sxs-lookup"><span data-stu-id="4d3c6-180">80</span></span>

<span data-ttu-id="4d3c6-181">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-182">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-183">81</span><span class="sxs-lookup"><span data-stu-id="4d3c6-183">81</span></span>

<span data-ttu-id="4d3c6-184">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-185">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-186">82</span><span class="sxs-lookup"><span data-stu-id="4d3c6-186">82</span></span>

<span data-ttu-id="4d3c6-187">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-188">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-189">83</span><span class="sxs-lookup"><span data-stu-id="4d3c6-189">83</span></span>

<span data-ttu-id="4d3c6-190">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-191">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-192">84</span><span class="sxs-lookup"><span data-stu-id="4d3c6-192">84</span></span>

<span data-ttu-id="4d3c6-193">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-194">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-195">85</span><span class="sxs-lookup"><span data-stu-id="4d3c6-195">85</span></span>

<span data-ttu-id="4d3c6-196">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-197">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-198">86</span><span class="sxs-lookup"><span data-stu-id="4d3c6-198">86</span></span>

<span data-ttu-id="4d3c6-199">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-200">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-201">87</span><span class="sxs-lookup"><span data-stu-id="4d3c6-201">87</span></span>

<span data-ttu-id="4d3c6-202">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-203">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-204">88</span><span class="sxs-lookup"><span data-stu-id="4d3c6-204">88</span></span>

<span data-ttu-id="4d3c6-205">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-206">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-207">89</span><span class="sxs-lookup"><span data-stu-id="4d3c6-207">89</span></span>

<span data-ttu-id="4d3c6-208">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-209">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-210">90</span><span class="sxs-lookup"><span data-stu-id="4d3c6-210">90</span></span>

<span data-ttu-id="4d3c6-211">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-212">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-213">91</span><span class="sxs-lookup"><span data-stu-id="4d3c6-213">91</span></span>

<span data-ttu-id="4d3c6-214">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-215">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-216">92</span><span class="sxs-lookup"><span data-stu-id="4d3c6-216">92</span></span>

<span data-ttu-id="4d3c6-217">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-218">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-219">93</span><span class="sxs-lookup"><span data-stu-id="4d3c6-219">93</span></span>

<span data-ttu-id="4d3c6-220">已經存在。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-221">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-222">94</span><span class="sxs-lookup"><span data-stu-id="4d3c6-222">94</span></span>

<span data-ttu-id="4d3c6-223">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-224">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-225">95</span><span class="sxs-lookup"><span data-stu-id="4d3c6-225">95</span></span>

<span data-ttu-id="4d3c6-226">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-227">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-228">96</span><span class="sxs-lookup"><span data-stu-id="4d3c6-228">96</span></span>

<span data-ttu-id="4d3c6-229">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-230">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-231">97</span><span class="sxs-lookup"><span data-stu-id="4d3c6-231">97</span></span>

<span data-ttu-id="4d3c6-232">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-233">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-234">98</span><span class="sxs-lookup"><span data-stu-id="4d3c6-234">98</span></span>

<span data-ttu-id="4d3c6-235">並非所有的 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-235">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-236">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-237">100</span><span class="sxs-lookup"><span data-stu-id="4d3c6-237">100</span></span>

<span data-ttu-id="4d3c6-238">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-238">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4d3c6-239">**其他**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="4d3c6-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="4d3c6-240">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="4d3c6-241">範例</span><span class="sxs-lookup"><span data-stu-id="4d3c6-241">Examples</span></span>

<span data-ttu-id="4d3c6-242">下列程式碼範例取自 TechNet 資源庫上的「 [在所有網路介面卡上啟用 dns](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) 」 VBScript 程式碼範例，讓電腦上的所有網路介面卡都能使用 dns。</span><span class="sxs-lookup"><span data-stu-id="4d3c6-242">The following code sample, taken from the [Enable DNS on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/c5736a48-71cc-4483-9605-d71d222740ac) VBScript code sample on TechNet Gallery, enables DNS for all network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
strHostName = "fabrikam1" 
arrDNSSuffixes = Array("hr.fabrikam.com", "research.fabrikam.com") 
objNetworkSettings.EnableDNS strHostName, , , arrDNSSuffixes 
```



## <a name="requirements"></a><span data-ttu-id="4d3c6-243">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d3c6-243">Requirements</span></span>



| <span data-ttu-id="4d3c6-244">需求</span><span class="sxs-lookup"><span data-stu-id="4d3c6-244">Requirement</span></span> | <span data-ttu-id="4d3c6-245">值</span><span class="sxs-lookup"><span data-stu-id="4d3c6-245">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d3c6-246">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d3c6-246">Minimum supported client</span></span><br/> | <span data-ttu-id="4d3c6-247">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4d3c6-247">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4d3c6-248">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d3c6-248">Minimum supported server</span></span><br/> | <span data-ttu-id="4d3c6-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4d3c6-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4d3c6-250">命名空間</span><span class="sxs-lookup"><span data-stu-id="4d3c6-250">Namespace</span></span><br/>                | <span data-ttu-id="4d3c6-251">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4d3c6-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4d3c6-252">MOF</span><span class="sxs-lookup"><span data-stu-id="4d3c6-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4d3c6-253"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4d3c6-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4d3c6-254">DLL</span><span class="sxs-lookup"><span data-stu-id="4d3c6-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d3c6-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d3c6-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d3c6-256">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d3c6-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d3c6-257">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="4d3c6-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="4d3c6-258">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="4d3c6-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="4d3c6-259">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="4d3c6-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="4d3c6-260">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="4d3c6-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="4d3c6-261">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="4d3c6-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

