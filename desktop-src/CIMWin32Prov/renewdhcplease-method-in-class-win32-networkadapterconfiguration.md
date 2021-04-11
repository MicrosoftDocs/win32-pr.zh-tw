---
description: RenewDHCPLease WMI 類別方法會更新已啟用 DHCP 的特定網路介面卡上的 IP 位址。
ms.assetid: b6e5d1fb-db3f-4491-bbac-46b1f2e7206e
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 RenewDHCPLease 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.RenewDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 4603f013c6b4c2c80edd555608b5f59325b6a6d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026020"
---
# <a name="renewdhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="fc07b-103">Win32 >networkadapterconfiguration 類別的 RenewDHCPLease 方法 \_</span><span class="sxs-lookup"><span data-stu-id="fc07b-103">RenewDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="fc07b-104">**RenewDHCPLease** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會更新已啟用 DHCP 的特定網路介面卡上的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="fc07b-104">The **RenewDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method renews the IP address on specific DHCP-enabled network adapters.</span></span>

<span data-ttu-id="fc07b-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="fc07b-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="fc07b-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="fc07b-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="fc07b-107">語法</span><span class="sxs-lookup"><span data-stu-id="fc07b-107">Syntax</span></span>


```mof
uint32 RenewDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="fc07b-108">參數</span><span class="sxs-lookup"><span data-stu-id="fc07b-108">Parameters</span></span>

<span data-ttu-id="fc07b-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="fc07b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc07b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="fc07b-110">Return value</span></span>

<span data-ttu-id="fc07b-111">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="fc07b-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="fc07b-112">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="fc07b-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="fc07b-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="fc07b-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="fc07b-114">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="fc07b-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-115">0</span><span class="sxs-lookup"><span data-stu-id="fc07b-115">0</span></span>

<span data-ttu-id="fc07b-116">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="fc07b-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-117">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="fc07b-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-118">1</span><span class="sxs-lookup"><span data-stu-id="fc07b-118">1</span></span>

<span data-ttu-id="fc07b-119">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="fc07b-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-120">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="fc07b-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-121">64</span><span class="sxs-lookup"><span data-stu-id="fc07b-121">64</span></span>

<span data-ttu-id="fc07b-122">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="fc07b-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-123">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="fc07b-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-124">65</span><span class="sxs-lookup"><span data-stu-id="fc07b-124">65</span></span>

<span data-ttu-id="fc07b-125">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="fc07b-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-126">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="fc07b-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-127">66</span><span class="sxs-lookup"><span data-stu-id="fc07b-127">66</span></span>

<span data-ttu-id="fc07b-128">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="fc07b-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-129">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fc07b-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-130">67</span><span class="sxs-lookup"><span data-stu-id="fc07b-130">67</span></span>

<span data-ttu-id="fc07b-131">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="fc07b-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-132">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="fc07b-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-133">68</span><span class="sxs-lookup"><span data-stu-id="fc07b-133">68</span></span>

<span data-ttu-id="fc07b-134">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="fc07b-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-135">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="fc07b-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-136">69</span><span class="sxs-lookup"><span data-stu-id="fc07b-136">69</span></span>

<span data-ttu-id="fc07b-137">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="fc07b-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-138">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="fc07b-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-139">70</span><span class="sxs-lookup"><span data-stu-id="fc07b-139">70</span></span>

<span data-ttu-id="fc07b-140">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="fc07b-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-141">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="fc07b-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-142">71</span><span class="sxs-lookup"><span data-stu-id="fc07b-142">71</span></span>

<span data-ttu-id="fc07b-143">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="fc07b-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-144">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="fc07b-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-145">72</span><span class="sxs-lookup"><span data-stu-id="fc07b-145">72</span></span>

<span data-ttu-id="fc07b-146">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="fc07b-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-147">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="fc07b-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-148">73</span><span class="sxs-lookup"><span data-stu-id="fc07b-148">73</span></span>

<span data-ttu-id="fc07b-149">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="fc07b-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-150">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="fc07b-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-151">74</span><span class="sxs-lookup"><span data-stu-id="fc07b-151">74</span></span>

<span data-ttu-id="fc07b-152">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="fc07b-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-153">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="fc07b-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-154">75</span><span class="sxs-lookup"><span data-stu-id="fc07b-154">75</span></span>

<span data-ttu-id="fc07b-155">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="fc07b-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-156">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="fc07b-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-157">76</span><span class="sxs-lookup"><span data-stu-id="fc07b-157">76</span></span>

<span data-ttu-id="fc07b-158">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="fc07b-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-159">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="fc07b-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-160">77</span><span class="sxs-lookup"><span data-stu-id="fc07b-160">77</span></span>

<span data-ttu-id="fc07b-161">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="fc07b-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-162">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="fc07b-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-163">78</span><span class="sxs-lookup"><span data-stu-id="fc07b-163">78</span></span>

<span data-ttu-id="fc07b-164">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="fc07b-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-165">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="fc07b-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-166">79</span><span class="sxs-lookup"><span data-stu-id="fc07b-166">79</span></span>

<span data-ttu-id="fc07b-167">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="fc07b-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-168">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="fc07b-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-169">80</span><span class="sxs-lookup"><span data-stu-id="fc07b-169">80</span></span>

<span data-ttu-id="fc07b-170">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="fc07b-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-171">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="fc07b-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-172">81</span><span class="sxs-lookup"><span data-stu-id="fc07b-172">81</span></span>

<span data-ttu-id="fc07b-173">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="fc07b-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-174">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="fc07b-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-175">82</span><span class="sxs-lookup"><span data-stu-id="fc07b-175">82</span></span>

<span data-ttu-id="fc07b-176">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="fc07b-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-177">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="fc07b-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-178">83</span><span class="sxs-lookup"><span data-stu-id="fc07b-178">83</span></span>

<span data-ttu-id="fc07b-179">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="fc07b-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-180">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="fc07b-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-181">84</span><span class="sxs-lookup"><span data-stu-id="fc07b-181">84</span></span>

<span data-ttu-id="fc07b-182">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="fc07b-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-183">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="fc07b-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-184">85</span><span class="sxs-lookup"><span data-stu-id="fc07b-184">85</span></span>

<span data-ttu-id="fc07b-185">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="fc07b-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-186">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="fc07b-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-187">86</span><span class="sxs-lookup"><span data-stu-id="fc07b-187">86</span></span>

<span data-ttu-id="fc07b-188">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="fc07b-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-189">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="fc07b-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-190">87</span><span class="sxs-lookup"><span data-stu-id="fc07b-190">87</span></span>

<span data-ttu-id="fc07b-191">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="fc07b-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-192">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="fc07b-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-193">88</span><span class="sxs-lookup"><span data-stu-id="fc07b-193">88</span></span>

<span data-ttu-id="fc07b-194">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="fc07b-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-195">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="fc07b-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-196">89</span><span class="sxs-lookup"><span data-stu-id="fc07b-196">89</span></span>

<span data-ttu-id="fc07b-197">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="fc07b-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-198">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="fc07b-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-199">90</span><span class="sxs-lookup"><span data-stu-id="fc07b-199">90</span></span>

<span data-ttu-id="fc07b-200">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="fc07b-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-201">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="fc07b-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-202">91</span><span class="sxs-lookup"><span data-stu-id="fc07b-202">91</span></span>

<span data-ttu-id="fc07b-203">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="fc07b-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-204">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="fc07b-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-205">92</span><span class="sxs-lookup"><span data-stu-id="fc07b-205">92</span></span>

<span data-ttu-id="fc07b-206">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="fc07b-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-207">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="fc07b-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-208">93</span><span class="sxs-lookup"><span data-stu-id="fc07b-208">93</span></span>

<span data-ttu-id="fc07b-209">已經存在。</span><span class="sxs-lookup"><span data-stu-id="fc07b-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-210">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="fc07b-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-211">94</span><span class="sxs-lookup"><span data-stu-id="fc07b-211">94</span></span>

<span data-ttu-id="fc07b-212">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="fc07b-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-213">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="fc07b-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-214">95</span><span class="sxs-lookup"><span data-stu-id="fc07b-214">95</span></span>

<span data-ttu-id="fc07b-215">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="fc07b-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-216">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="fc07b-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-217">96</span><span class="sxs-lookup"><span data-stu-id="fc07b-217">96</span></span>

<span data-ttu-id="fc07b-218">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="fc07b-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-219">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="fc07b-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-220">97</span><span class="sxs-lookup"><span data-stu-id="fc07b-220">97</span></span>

<span data-ttu-id="fc07b-221">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="fc07b-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-222">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="fc07b-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-223">98</span><span class="sxs-lookup"><span data-stu-id="fc07b-223">98</span></span>

<span data-ttu-id="fc07b-224">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="fc07b-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-225">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="fc07b-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-226">100</span><span class="sxs-lookup"><span data-stu-id="fc07b-226">100</span></span>

<span data-ttu-id="fc07b-227">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="fc07b-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="fc07b-228">**其他**</span><span class="sxs-lookup"><span data-stu-id="fc07b-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="fc07b-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="fc07b-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fc07b-230">備註</span><span class="sxs-lookup"><span data-stu-id="fc07b-230">Remarks</span></span>

<span data-ttu-id="fc07b-231">DHCP 伺服器指派的 IP 位址租用期有到期日，如果用戶端想要繼續使用指派的 IP 位址，就必須更新此期限。</span><span class="sxs-lookup"><span data-stu-id="fc07b-231">The lease for the IP address assigned by a DHCP server has an expiration date that the client must renew if it intends to continue use of the assigned IP address.</span></span>

## <a name="examples"></a><span data-ttu-id="fc07b-232">範例</span><span class="sxs-lookup"><span data-stu-id="fc07b-232">Examples</span></span>

<span data-ttu-id="fc07b-233">在 TechNet 資源庫上使用 PowerShell powershell 範例的 [發行更新 Ip 位址](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) ，會使用 **RenewDHCPLease** 來釋放和更新 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="fc07b-233">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **RenewDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="fc07b-234">在 TechNet 資源庫上 [更新網路介面卡](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) VBScript 範例的 dhcp 租用會使用 **RenewDHCPLease** 來更新電腦上每個 tcp/ip 系結網路介面卡的 dhcp 租用。</span><span class="sxs-lookup"><span data-stu-id="fc07b-234">The [Renew the DHCP Lease for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/39443fd7-0152-4c0a-89e9-e2753049b203) VBScript sample on TechNet Gallery uses **RenewDHCPLease** to renew the DHCP lease for each TCP/IP-bound network adapter in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc07b-235">規格需求</span><span class="sxs-lookup"><span data-stu-id="fc07b-235">Requirements</span></span>



| <span data-ttu-id="fc07b-236">需求</span><span class="sxs-lookup"><span data-stu-id="fc07b-236">Requirement</span></span> | <span data-ttu-id="fc07b-237">值</span><span class="sxs-lookup"><span data-stu-id="fc07b-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="fc07b-238">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fc07b-238">Minimum supported client</span></span><br/> | <span data-ttu-id="fc07b-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="fc07b-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="fc07b-240">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fc07b-240">Minimum supported server</span></span><br/> | <span data-ttu-id="fc07b-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="fc07b-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="fc07b-242">命名空間</span><span class="sxs-lookup"><span data-stu-id="fc07b-242">Namespace</span></span><br/>                | <span data-ttu-id="fc07b-243">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="fc07b-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="fc07b-244">MOF</span><span class="sxs-lookup"><span data-stu-id="fc07b-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fc07b-245"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="fc07b-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="fc07b-246">DLL</span><span class="sxs-lookup"><span data-stu-id="fc07b-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fc07b-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc07b-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc07b-248">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fc07b-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc07b-249">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="fc07b-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="fc07b-250">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="fc07b-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="fc07b-251">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="fc07b-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="fc07b-252">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="fc07b-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="fc07b-253">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="fc07b-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

