---
description: SetIPConnectionMetric 方法是用來設定與此 IP 系結介面卡相關聯的路由度量。
ms.assetid: d7f7c0df-51e3-4dc8-8a53-977ecde075df
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetIPConnectionMetric 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPConnectionMetric
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 73d6dde0a8faea2aeaf0982459e3c377bb1ac51d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110949"
---
# <a name="setipconnectionmetric-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="5b969-103">Win32 >networkadapterconfiguration 類別的 SetIPConnectionMetric 方法 \_</span><span class="sxs-lookup"><span data-stu-id="5b969-103">SetIPConnectionMetric method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="5b969-104">**SetIPConnectionMetric** 方法是用來設定與此 IP 系結介面卡相關聯的路由度量。</span><span class="sxs-lookup"><span data-stu-id="5b969-104">The **SetIPConnectionMetric** method is used to set the routing metric associated with this IP-bound adapter.</span></span>

<span data-ttu-id="5b969-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="5b969-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="5b969-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="5b969-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="5b969-107">語法</span><span class="sxs-lookup"><span data-stu-id="5b969-107">Syntax</span></span>


```mof
uint32 SetIPConnectionMetric(
  [in] uint32 IPConnectionMetric
);
```



## <a name="parameters"></a><span data-ttu-id="5b969-108">參數</span><span class="sxs-lookup"><span data-stu-id="5b969-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5b969-109">*IPConnectionMetric* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5b969-109">*IPConnectionMetric* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5b969-110">指出使用此 IP 系結介面卡設定之路由的成本。</span><span class="sxs-lookup"><span data-stu-id="5b969-110">Indicates the cost of using the configured routes for this IP-bound adapter.</span></span> <span data-ttu-id="5b969-111">IP 路由表中的這些路由會加權值。</span><span class="sxs-lookup"><span data-stu-id="5b969-111">The value is weighted for those routes in the IP routing table.</span></span> <span data-ttu-id="5b969-112">如果路由表中有多個目的地的路由，則會使用最低計量的路由。</span><span class="sxs-lookup"><span data-stu-id="5b969-112">If there are multiple routes to a destination in the routing table, the route with the lowest metric is used.</span></span> <span data-ttu-id="5b969-113">有效值的範圍為1到9999。</span><span class="sxs-lookup"><span data-stu-id="5b969-113">The range of valid values is 1 through 9999.</span></span> <span data-ttu-id="5b969-114">預設值為 1。</span><span class="sxs-lookup"><span data-stu-id="5b969-114">The default value is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5b969-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="5b969-115">Return value</span></span>

<span data-ttu-id="5b969-116">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="5b969-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="5b969-117">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="5b969-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="5b969-118">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="5b969-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="5b969-119">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="5b969-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-120">0</span><span class="sxs-lookup"><span data-stu-id="5b969-120">0</span></span>

<span data-ttu-id="5b969-121">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="5b969-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-122">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="5b969-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-123">1</span><span class="sxs-lookup"><span data-stu-id="5b969-123">1</span></span>

<span data-ttu-id="5b969-124">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="5b969-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-125">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="5b969-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-126">64</span><span class="sxs-lookup"><span data-stu-id="5b969-126">64</span></span>

<span data-ttu-id="5b969-127">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="5b969-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-128">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="5b969-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-129">65</span><span class="sxs-lookup"><span data-stu-id="5b969-129">65</span></span>

<span data-ttu-id="5b969-130">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="5b969-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-131">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="5b969-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-132">66</span><span class="sxs-lookup"><span data-stu-id="5b969-132">66</span></span>

<span data-ttu-id="5b969-133">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="5b969-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-134">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="5b969-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-135">67</span><span class="sxs-lookup"><span data-stu-id="5b969-135">67</span></span>

<span data-ttu-id="5b969-136">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="5b969-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-137">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="5b969-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-138">68</span><span class="sxs-lookup"><span data-stu-id="5b969-138">68</span></span>

<span data-ttu-id="5b969-139">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="5b969-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-140">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="5b969-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-141">69</span><span class="sxs-lookup"><span data-stu-id="5b969-141">69</span></span>

<span data-ttu-id="5b969-142">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="5b969-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-143">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="5b969-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-144">70</span><span class="sxs-lookup"><span data-stu-id="5b969-144">70</span></span>

<span data-ttu-id="5b969-145">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="5b969-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-146">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="5b969-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-147">71</span><span class="sxs-lookup"><span data-stu-id="5b969-147">71</span></span>

<span data-ttu-id="5b969-148">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="5b969-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-149">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="5b969-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-150">72</span><span class="sxs-lookup"><span data-stu-id="5b969-150">72</span></span>

<span data-ttu-id="5b969-151">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="5b969-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-152">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="5b969-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-153">73</span><span class="sxs-lookup"><span data-stu-id="5b969-153">73</span></span>

<span data-ttu-id="5b969-154">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="5b969-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-155">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="5b969-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-156">74</span><span class="sxs-lookup"><span data-stu-id="5b969-156">74</span></span>

<span data-ttu-id="5b969-157">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="5b969-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-158">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="5b969-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-159">75</span><span class="sxs-lookup"><span data-stu-id="5b969-159">75</span></span>

<span data-ttu-id="5b969-160">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="5b969-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-161">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="5b969-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-162">76</span><span class="sxs-lookup"><span data-stu-id="5b969-162">76</span></span>

<span data-ttu-id="5b969-163">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="5b969-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-164">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="5b969-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-165">77</span><span class="sxs-lookup"><span data-stu-id="5b969-165">77</span></span>

<span data-ttu-id="5b969-166">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="5b969-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-167">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="5b969-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-168">78</span><span class="sxs-lookup"><span data-stu-id="5b969-168">78</span></span>

<span data-ttu-id="5b969-169">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="5b969-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-170">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="5b969-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-171">79</span><span class="sxs-lookup"><span data-stu-id="5b969-171">79</span></span>

<span data-ttu-id="5b969-172">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="5b969-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-173">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="5b969-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-174">80</span><span class="sxs-lookup"><span data-stu-id="5b969-174">80</span></span>

<span data-ttu-id="5b969-175">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="5b969-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-176">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="5b969-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-177">81</span><span class="sxs-lookup"><span data-stu-id="5b969-177">81</span></span>

<span data-ttu-id="5b969-178">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="5b969-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-179">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="5b969-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-180">82</span><span class="sxs-lookup"><span data-stu-id="5b969-180">82</span></span>

<span data-ttu-id="5b969-181">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="5b969-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-182">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="5b969-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-183">83</span><span class="sxs-lookup"><span data-stu-id="5b969-183">83</span></span>

<span data-ttu-id="5b969-184">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="5b969-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-185">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="5b969-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-186">84</span><span class="sxs-lookup"><span data-stu-id="5b969-186">84</span></span>

<span data-ttu-id="5b969-187">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="5b969-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-188">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="5b969-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-189">85</span><span class="sxs-lookup"><span data-stu-id="5b969-189">85</span></span>

<span data-ttu-id="5b969-190">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="5b969-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-191">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="5b969-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-192">86</span><span class="sxs-lookup"><span data-stu-id="5b969-192">86</span></span>

<span data-ttu-id="5b969-193">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="5b969-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-194">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="5b969-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-195">87</span><span class="sxs-lookup"><span data-stu-id="5b969-195">87</span></span>

<span data-ttu-id="5b969-196">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="5b969-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-197">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="5b969-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-198">88</span><span class="sxs-lookup"><span data-stu-id="5b969-198">88</span></span>

<span data-ttu-id="5b969-199">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="5b969-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-200">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="5b969-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-201">89</span><span class="sxs-lookup"><span data-stu-id="5b969-201">89</span></span>

<span data-ttu-id="5b969-202">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="5b969-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-203">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="5b969-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-204">90</span><span class="sxs-lookup"><span data-stu-id="5b969-204">90</span></span>

<span data-ttu-id="5b969-205">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="5b969-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-206">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="5b969-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-207">91</span><span class="sxs-lookup"><span data-stu-id="5b969-207">91</span></span>

<span data-ttu-id="5b969-208">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="5b969-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-209">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="5b969-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-210">92</span><span class="sxs-lookup"><span data-stu-id="5b969-210">92</span></span>

<span data-ttu-id="5b969-211">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="5b969-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-212">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="5b969-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-213">93</span><span class="sxs-lookup"><span data-stu-id="5b969-213">93</span></span>

<span data-ttu-id="5b969-214">已經存在。</span><span class="sxs-lookup"><span data-stu-id="5b969-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-215">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="5b969-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-216">94</span><span class="sxs-lookup"><span data-stu-id="5b969-216">94</span></span>

<span data-ttu-id="5b969-217">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="5b969-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-218">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="5b969-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-219">95</span><span class="sxs-lookup"><span data-stu-id="5b969-219">95</span></span>

<span data-ttu-id="5b969-220">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="5b969-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-221">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="5b969-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-222">96</span><span class="sxs-lookup"><span data-stu-id="5b969-222">96</span></span>

<span data-ttu-id="5b969-223">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="5b969-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-224">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="5b969-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-225">97</span><span class="sxs-lookup"><span data-stu-id="5b969-225">97</span></span>

<span data-ttu-id="5b969-226">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="5b969-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-227">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="5b969-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-228">98</span><span class="sxs-lookup"><span data-stu-id="5b969-228">98</span></span>

<span data-ttu-id="5b969-229">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="5b969-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-230">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="5b969-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-231">100</span><span class="sxs-lookup"><span data-stu-id="5b969-231">100</span></span>

<span data-ttu-id="5b969-232">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="5b969-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="5b969-233">**其他**</span><span class="sxs-lookup"><span data-stu-id="5b969-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="5b969-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="5b969-234">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="5b969-235">範例</span><span class="sxs-lookup"><span data-stu-id="5b969-235">Examples</span></span>

<span data-ttu-id="5b969-236">[ [修改網路介面卡的 Ip 連接](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) 計量] VBScript 範例會將網路介面卡的 ip 連接計量設定為100。</span><span class="sxs-lookup"><span data-stu-id="5b969-236">The [Modify the IP Connection Metric for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/73367c75-7a39-44dc-a8d7-eb2359030969) VBScript sample sets the IP connection metric for a network adapter to 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="5b969-237">規格需求</span><span class="sxs-lookup"><span data-stu-id="5b969-237">Requirements</span></span>



| <span data-ttu-id="5b969-238">需求</span><span class="sxs-lookup"><span data-stu-id="5b969-238">Requirement</span></span> | <span data-ttu-id="5b969-239">值</span><span class="sxs-lookup"><span data-stu-id="5b969-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5b969-240">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5b969-240">Minimum supported client</span></span><br/> | <span data-ttu-id="5b969-241">Windows Vista、Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5b969-241">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="5b969-242">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5b969-242">Minimum supported server</span></span><br/> | <span data-ttu-id="5b969-243">Windows Server 2008、Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5b969-243">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="5b969-244">命名空間</span><span class="sxs-lookup"><span data-stu-id="5b969-244">Namespace</span></span><br/>                | <span data-ttu-id="5b969-245">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="5b969-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="5b969-246">MOF</span><span class="sxs-lookup"><span data-stu-id="5b969-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5b969-247"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="5b969-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="5b969-248">DLL</span><span class="sxs-lookup"><span data-stu-id="5b969-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5b969-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5b969-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5b969-250">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5b969-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5b969-251">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="5b969-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="5b969-252">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="5b969-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="5b969-253">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="5b969-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="5b969-254">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="5b969-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="5b969-255">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="5b969-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

