---
description: SetDNSSuffixSearchOrder WMI 類別靜態方法會使用 string 元素陣列來設定尾碼搜尋順序。
ms.assetid: 1ad9fc99-8c57-43d4-92d2-b12f2c1451cb
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetDNSSuffixSearchOrder 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSSuffixSearchOrder
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 10088b1d0722f968e5d3742984baa91ec3e423aa
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847423"
---
# <a name="setdnssuffixsearchorder-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="95869-103">Win32 >networkadapterconfiguration 類別的 SetDNSSuffixSearchOrder 方法 \_</span><span class="sxs-lookup"><span data-stu-id="95869-103">SetDNSSuffixSearchOrder method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="95869-104">**SetDNSSuffixSearchOrder** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法會使用 string 元素陣列來設定尾碼搜尋順序。</span><span class="sxs-lookup"><span data-stu-id="95869-104">The **SetDNSSuffixSearchOrder** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method uses an array of string elements to set the suffix search order.</span></span>

<span data-ttu-id="95869-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="95869-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="95869-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="95869-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="95869-107">語法</span><span class="sxs-lookup"><span data-stu-id="95869-107">Syntax</span></span>


```mof
uint32 SetDNSSuffixSearchOrder(
  [in] string DNSDomainSuffixSearchOrder[]
);
```



## <a name="parameters"></a><span data-ttu-id="95869-108">參數</span><span class="sxs-lookup"><span data-stu-id="95869-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="95869-109">*DNSDomainSuffixSearchOrder* \[在\]</span><span class="sxs-lookup"><span data-stu-id="95869-109">*DNSDomainSuffixSearchOrder* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="95869-110">要查詢 DNS 伺服器的伺服器尾碼清單。</span><span class="sxs-lookup"><span data-stu-id="95869-110">List of server suffixes to query for DNS servers.</span></span> <span data-ttu-id="95869-111">DNS 尾碼的登錄位置是 **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **Tcpip \| NameServer**</span><span class="sxs-lookup"><span data-stu-id="95869-111">The registry location of the DNS suffix is **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**Tcpip\|NameServer**</span></span>

<span data-ttu-id="95869-112">範例： "suffix1.company.com"、"suffix2.company.com"</span><span class="sxs-lookup"><span data-stu-id="95869-112">Example: "suffix1.company.com", "suffix2.company.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="95869-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="95869-113">Return value</span></span>

<span data-ttu-id="95869-114">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="95869-114">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="95869-115">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="95869-115">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="95869-116">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="95869-116">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="95869-117">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="95869-117">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="95869-118">0</span><span class="sxs-lookup"><span data-stu-id="95869-118">0</span></span>

<span data-ttu-id="95869-119">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="95869-119">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="95869-120">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="95869-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="95869-121">1</span><span class="sxs-lookup"><span data-stu-id="95869-121">1</span></span>

<span data-ttu-id="95869-122">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="95869-122">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="95869-123">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="95869-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="95869-124">64</span><span class="sxs-lookup"><span data-stu-id="95869-124">64</span></span>

<span data-ttu-id="95869-125">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="95869-125">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="95869-126">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="95869-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="95869-127">65</span><span class="sxs-lookup"><span data-stu-id="95869-127">65</span></span>

<span data-ttu-id="95869-128">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="95869-128">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="95869-129">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="95869-129">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="95869-130">66</span><span class="sxs-lookup"><span data-stu-id="95869-130">66</span></span>

<span data-ttu-id="95869-131">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="95869-131">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="95869-132">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="95869-132">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="95869-133">67</span><span class="sxs-lookup"><span data-stu-id="95869-133">67</span></span>

<span data-ttu-id="95869-134">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="95869-134">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="95869-135">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="95869-135">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="95869-136">68</span><span class="sxs-lookup"><span data-stu-id="95869-136">68</span></span>

<span data-ttu-id="95869-137">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="95869-137">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="95869-138">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="95869-138">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="95869-139">69</span><span class="sxs-lookup"><span data-stu-id="95869-139">69</span></span>

<span data-ttu-id="95869-140">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="95869-140">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="95869-141">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="95869-141">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="95869-142">70</span><span class="sxs-lookup"><span data-stu-id="95869-142">70</span></span>

<span data-ttu-id="95869-143">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="95869-143">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="95869-144">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="95869-144">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="95869-145">71</span><span class="sxs-lookup"><span data-stu-id="95869-145">71</span></span>

<span data-ttu-id="95869-146">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="95869-146">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="95869-147">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="95869-147">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="95869-148">72</span><span class="sxs-lookup"><span data-stu-id="95869-148">72</span></span>

<span data-ttu-id="95869-149">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="95869-149">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="95869-150">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="95869-150">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="95869-151">73</span><span class="sxs-lookup"><span data-stu-id="95869-151">73</span></span>

<span data-ttu-id="95869-152">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="95869-152">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="95869-153">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="95869-153">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="95869-154">74</span><span class="sxs-lookup"><span data-stu-id="95869-154">74</span></span>

<span data-ttu-id="95869-155">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="95869-155">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="95869-156">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="95869-156">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="95869-157">75</span><span class="sxs-lookup"><span data-stu-id="95869-157">75</span></span>

<span data-ttu-id="95869-158">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="95869-158">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="95869-159">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="95869-159">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="95869-160">76</span><span class="sxs-lookup"><span data-stu-id="95869-160">76</span></span>

<span data-ttu-id="95869-161">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="95869-161">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="95869-162">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="95869-162">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="95869-163">77</span><span class="sxs-lookup"><span data-stu-id="95869-163">77</span></span>

<span data-ttu-id="95869-164">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="95869-164">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="95869-165">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="95869-165">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="95869-166">78</span><span class="sxs-lookup"><span data-stu-id="95869-166">78</span></span>

<span data-ttu-id="95869-167">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="95869-167">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="95869-168">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="95869-168">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="95869-169">79</span><span class="sxs-lookup"><span data-stu-id="95869-169">79</span></span>

<span data-ttu-id="95869-170">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="95869-170">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="95869-171">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="95869-171">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="95869-172">80</span><span class="sxs-lookup"><span data-stu-id="95869-172">80</span></span>

<span data-ttu-id="95869-173">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="95869-173">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="95869-174">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="95869-174">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="95869-175">81</span><span class="sxs-lookup"><span data-stu-id="95869-175">81</span></span>

<span data-ttu-id="95869-176">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="95869-176">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="95869-177">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="95869-177">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="95869-178">82</span><span class="sxs-lookup"><span data-stu-id="95869-178">82</span></span>

<span data-ttu-id="95869-179">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="95869-179">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="95869-180">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="95869-180">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="95869-181">83</span><span class="sxs-lookup"><span data-stu-id="95869-181">83</span></span>

<span data-ttu-id="95869-182">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="95869-182">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="95869-183">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="95869-183">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="95869-184">84</span><span class="sxs-lookup"><span data-stu-id="95869-184">84</span></span>

<span data-ttu-id="95869-185">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="95869-185">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="95869-186">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="95869-186">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="95869-187">85</span><span class="sxs-lookup"><span data-stu-id="95869-187">85</span></span>

<span data-ttu-id="95869-188">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="95869-188">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="95869-189">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="95869-189">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="95869-190">86</span><span class="sxs-lookup"><span data-stu-id="95869-190">86</span></span>

<span data-ttu-id="95869-191">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="95869-191">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="95869-192">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="95869-192">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="95869-193">87</span><span class="sxs-lookup"><span data-stu-id="95869-193">87</span></span>

<span data-ttu-id="95869-194">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="95869-194">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="95869-195">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="95869-195">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="95869-196">88</span><span class="sxs-lookup"><span data-stu-id="95869-196">88</span></span>

<span data-ttu-id="95869-197">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="95869-197">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="95869-198">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="95869-198">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="95869-199">89</span><span class="sxs-lookup"><span data-stu-id="95869-199">89</span></span>

<span data-ttu-id="95869-200">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="95869-200">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="95869-201">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="95869-201">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="95869-202">90</span><span class="sxs-lookup"><span data-stu-id="95869-202">90</span></span>

<span data-ttu-id="95869-203">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="95869-203">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="95869-204">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="95869-204">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="95869-205">91</span><span class="sxs-lookup"><span data-stu-id="95869-205">91</span></span>

<span data-ttu-id="95869-206">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="95869-206">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="95869-207">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="95869-207">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="95869-208">92</span><span class="sxs-lookup"><span data-stu-id="95869-208">92</span></span>

<span data-ttu-id="95869-209">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="95869-209">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="95869-210">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="95869-210">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="95869-211">93</span><span class="sxs-lookup"><span data-stu-id="95869-211">93</span></span>

<span data-ttu-id="95869-212">已經存在。</span><span class="sxs-lookup"><span data-stu-id="95869-212">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="95869-213">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="95869-213">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="95869-214">94</span><span class="sxs-lookup"><span data-stu-id="95869-214">94</span></span>

<span data-ttu-id="95869-215">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="95869-215">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="95869-216">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="95869-216">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="95869-217">95</span><span class="sxs-lookup"><span data-stu-id="95869-217">95</span></span>

<span data-ttu-id="95869-218">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="95869-218">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="95869-219">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="95869-219">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="95869-220">96</span><span class="sxs-lookup"><span data-stu-id="95869-220">96</span></span>

<span data-ttu-id="95869-221">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="95869-221">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="95869-222">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="95869-222">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="95869-223">97</span><span class="sxs-lookup"><span data-stu-id="95869-223">97</span></span>

<span data-ttu-id="95869-224">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="95869-224">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="95869-225">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="95869-225">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="95869-226">98</span><span class="sxs-lookup"><span data-stu-id="95869-226">98</span></span>

<span data-ttu-id="95869-227">並非所有的 DHCP 租用都會發行或更新。</span><span class="sxs-lookup"><span data-stu-id="95869-227">Not all DHCP leases are released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="95869-228">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="95869-228">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="95869-229">100</span><span class="sxs-lookup"><span data-stu-id="95869-229">100</span></span>

<span data-ttu-id="95869-230">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="95869-230">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="95869-231">**其他**</span><span class="sxs-lookup"><span data-stu-id="95869-231">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="95869-232">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="95869-232">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="95869-233">備註</span><span class="sxs-lookup"><span data-stu-id="95869-233">Remarks</span></span>

<span data-ttu-id="95869-234">這是適用于所有介面卡但僅適用于 Windows 的獨立實例呼叫。</span><span class="sxs-lookup"><span data-stu-id="95869-234">This is an instance-independent call that applies to all adapters but only for Windows.</span></span>

## <a name="examples"></a><span data-ttu-id="95869-235">範例</span><span class="sxs-lookup"><span data-stu-id="95869-235">Examples</span></span>

<span data-ttu-id="95869-236">[ [修改所有網路介面卡的 DNS 尾碼搜尋順序](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) ] VBScript 程式碼範例會將電腦設定為在執行 DNS 搜尋時使用兩個 dns 尾碼。</span><span class="sxs-lookup"><span data-stu-id="95869-236">The [Modify the DNS Suffix Search Order for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/2857b7b0-1327-4ce2-9f2b-b662cce387c6) VBScript code sample configures a computer to use two DNS suffixes when performing DNS searches.</span></span>

<span data-ttu-id="95869-237">[在 [電腦上啟用 Dhcp 設定](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) ] VBScript 範例會設定在電腦上啟用 dhcp 時通常需要的所有設定。</span><span class="sxs-lookup"><span data-stu-id="95869-237">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample configures all the settings typically required to enable DHCP on a computer.</span></span>

<span data-ttu-id="95869-238">下列 PowerShell 程式碼會設定 DNS 尾碼搜尋順序。</span><span class="sxs-lookup"><span data-stu-id="95869-238">The following PowerShell code sets the DNS suffix search order.</span></span>


```PowerShell
#First store the suffixes to set in a variable
$suffixes = 'microsoft.com', 'google.com', 'yahoo.com'

#Since this is a static method, get a class object and then call the method. 
$class = [wmiclass]'Win32_NetworkAdapterConfiguration'
$class.SetDNSSuffixSearchOrder($suffixes)
```



## <a name="requirements"></a><span data-ttu-id="95869-239">規格需求</span><span class="sxs-lookup"><span data-stu-id="95869-239">Requirements</span></span>



| <span data-ttu-id="95869-240">需求</span><span class="sxs-lookup"><span data-stu-id="95869-240">Requirement</span></span> | <span data-ttu-id="95869-241">值</span><span class="sxs-lookup"><span data-stu-id="95869-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="95869-242">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="95869-242">Minimum supported client</span></span><br/> | <span data-ttu-id="95869-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="95869-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="95869-244">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="95869-244">Minimum supported server</span></span><br/> | <span data-ttu-id="95869-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="95869-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="95869-246">命名空間</span><span class="sxs-lookup"><span data-stu-id="95869-246">Namespace</span></span><br/>                | <span data-ttu-id="95869-247">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="95869-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="95869-248">MOF</span><span class="sxs-lookup"><span data-stu-id="95869-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="95869-249"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="95869-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="95869-250">DLL</span><span class="sxs-lookup"><span data-stu-id="95869-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="95869-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="95869-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="95869-252">另請參閱</span><span class="sxs-lookup"><span data-stu-id="95869-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="95869-253">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="95869-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="95869-254">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="95869-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="95869-255">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="95869-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="95869-256">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="95869-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="95869-257">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="95869-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

