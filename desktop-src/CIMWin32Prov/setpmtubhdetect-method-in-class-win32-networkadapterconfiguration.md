---
description: SetPMTUBHDetect WMI 類別靜態方法是用來在執行路徑 MTU 探索時啟用黑洞路由器的偵測。
ms.assetid: a1e45ed9-85a9-4fdd-890a-d578c3f94b72
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetPMTUBHDetect 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUBHDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 098652c6ea0a53f9d3b1f616def3dd8b5e7228af
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110941"
---
# <a name="setpmtubhdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="ec179-103">Win32 >networkadapterconfiguration 類別的 SetPMTUBHDetect 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ec179-103">SetPMTUBHDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="ec179-104">**SetPMTUBHDetect** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來在執行路徑 MTU 探索時啟用黑洞路由器的偵測。</span><span class="sxs-lookup"><span data-stu-id="ec179-104">The **SetPMTUBHDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable the detection of Black Hole routers while doing Path MTU Discovery.</span></span>

<span data-ttu-id="ec179-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="ec179-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ec179-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="ec179-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ec179-107">語法</span><span class="sxs-lookup"><span data-stu-id="ec179-107">Syntax</span></span>


```mof
uint32 SetPMTUBHDetect(
  [in] boolean PMTUBHDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="ec179-108">參數</span><span class="sxs-lookup"><span data-stu-id="ec179-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ec179-109">*PMTUBHDetectEnabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ec179-109">*PMTUBHDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ec179-110">若 **為 true**，TCP 會嘗試探索黑洞，並在不同的網路路徑中路由封包。</span><span class="sxs-lookup"><span data-stu-id="ec179-110">If **true**, TCP attempts to discover Black Hole and route packets in different network paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ec179-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ec179-111">Return value</span></span>

<span data-ttu-id="ec179-112">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="ec179-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="ec179-113">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="ec179-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ec179-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="ec179-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ec179-115">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="ec179-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-116">0</span><span class="sxs-lookup"><span data-stu-id="ec179-116">0</span></span>

<span data-ttu-id="ec179-117">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="ec179-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-118">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="ec179-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-119">1</span><span class="sxs-lookup"><span data-stu-id="ec179-119">1</span></span>

<span data-ttu-id="ec179-120">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="ec179-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-121">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="ec179-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-122">64</span><span class="sxs-lookup"><span data-stu-id="ec179-122">64</span></span>

<span data-ttu-id="ec179-123">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="ec179-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-124">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="ec179-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-125">65</span><span class="sxs-lookup"><span data-stu-id="ec179-125">65</span></span>

<span data-ttu-id="ec179-126">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="ec179-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-127">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="ec179-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-128">66</span><span class="sxs-lookup"><span data-stu-id="ec179-128">66</span></span>

<span data-ttu-id="ec179-129">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="ec179-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-130">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="ec179-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-131">67</span><span class="sxs-lookup"><span data-stu-id="ec179-131">67</span></span>

<span data-ttu-id="ec179-132">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ec179-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-133">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="ec179-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-134">68</span><span class="sxs-lookup"><span data-stu-id="ec179-134">68</span></span>

<span data-ttu-id="ec179-135">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="ec179-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-136">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="ec179-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-137">69</span><span class="sxs-lookup"><span data-stu-id="ec179-137">69</span></span>

<span data-ttu-id="ec179-138">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="ec179-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-139">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="ec179-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-140">70</span><span class="sxs-lookup"><span data-stu-id="ec179-140">70</span></span>

<span data-ttu-id="ec179-141">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="ec179-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-142">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="ec179-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-143">71</span><span class="sxs-lookup"><span data-stu-id="ec179-143">71</span></span>

<span data-ttu-id="ec179-144">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="ec179-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-145">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="ec179-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-146">72</span><span class="sxs-lookup"><span data-stu-id="ec179-146">72</span></span>

<span data-ttu-id="ec179-147">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ec179-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-148">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="ec179-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-149">73</span><span class="sxs-lookup"><span data-stu-id="ec179-149">73</span></span>

<span data-ttu-id="ec179-150">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="ec179-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-151">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="ec179-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-152">74</span><span class="sxs-lookup"><span data-stu-id="ec179-152">74</span></span>

<span data-ttu-id="ec179-153">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="ec179-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-154">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="ec179-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-155">75</span><span class="sxs-lookup"><span data-stu-id="ec179-155">75</span></span>

<span data-ttu-id="ec179-156">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ec179-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-157">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="ec179-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-158">76</span><span class="sxs-lookup"><span data-stu-id="ec179-158">76</span></span>

<span data-ttu-id="ec179-159">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="ec179-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-160">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="ec179-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-161">77</span><span class="sxs-lookup"><span data-stu-id="ec179-161">77</span></span>

<span data-ttu-id="ec179-162">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="ec179-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-163">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="ec179-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-164">78</span><span class="sxs-lookup"><span data-stu-id="ec179-164">78</span></span>

<span data-ttu-id="ec179-165">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="ec179-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-166">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="ec179-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-167">79</span><span class="sxs-lookup"><span data-stu-id="ec179-167">79</span></span>

<span data-ttu-id="ec179-168">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="ec179-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-169">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="ec179-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-170">80</span><span class="sxs-lookup"><span data-stu-id="ec179-170">80</span></span>

<span data-ttu-id="ec179-171">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="ec179-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-172">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="ec179-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-173">81</span><span class="sxs-lookup"><span data-stu-id="ec179-173">81</span></span>

<span data-ttu-id="ec179-174">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="ec179-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-175">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="ec179-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-176">82</span><span class="sxs-lookup"><span data-stu-id="ec179-176">82</span></span>

<span data-ttu-id="ec179-177">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="ec179-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-178">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="ec179-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-179">83</span><span class="sxs-lookup"><span data-stu-id="ec179-179">83</span></span>

<span data-ttu-id="ec179-180">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="ec179-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-181">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="ec179-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-182">84</span><span class="sxs-lookup"><span data-stu-id="ec179-182">84</span></span>

<span data-ttu-id="ec179-183">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="ec179-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-184">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="ec179-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-185">85</span><span class="sxs-lookup"><span data-stu-id="ec179-185">85</span></span>

<span data-ttu-id="ec179-186">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="ec179-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-187">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="ec179-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-188">86</span><span class="sxs-lookup"><span data-stu-id="ec179-188">86</span></span>

<span data-ttu-id="ec179-189">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="ec179-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-190">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="ec179-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-191">87</span><span class="sxs-lookup"><span data-stu-id="ec179-191">87</span></span>

<span data-ttu-id="ec179-192">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="ec179-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-193">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="ec179-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-194">88</span><span class="sxs-lookup"><span data-stu-id="ec179-194">88</span></span>

<span data-ttu-id="ec179-195">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="ec179-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-196">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="ec179-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-197">89</span><span class="sxs-lookup"><span data-stu-id="ec179-197">89</span></span>

<span data-ttu-id="ec179-198">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="ec179-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-199">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="ec179-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-200">90</span><span class="sxs-lookup"><span data-stu-id="ec179-200">90</span></span>

<span data-ttu-id="ec179-201">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="ec179-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-202">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="ec179-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-203">91</span><span class="sxs-lookup"><span data-stu-id="ec179-203">91</span></span>

<span data-ttu-id="ec179-204">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="ec179-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-205">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="ec179-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-206">92</span><span class="sxs-lookup"><span data-stu-id="ec179-206">92</span></span>

<span data-ttu-id="ec179-207">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="ec179-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-208">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="ec179-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-209">93</span><span class="sxs-lookup"><span data-stu-id="ec179-209">93</span></span>

<span data-ttu-id="ec179-210">已經存在。</span><span class="sxs-lookup"><span data-stu-id="ec179-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-211">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="ec179-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-212">94</span><span class="sxs-lookup"><span data-stu-id="ec179-212">94</span></span>

<span data-ttu-id="ec179-213">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="ec179-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-214">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="ec179-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-215">95</span><span class="sxs-lookup"><span data-stu-id="ec179-215">95</span></span>

<span data-ttu-id="ec179-216">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="ec179-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-217">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="ec179-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-218">96</span><span class="sxs-lookup"><span data-stu-id="ec179-218">96</span></span>

<span data-ttu-id="ec179-219">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="ec179-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-220">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="ec179-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-221">97</span><span class="sxs-lookup"><span data-stu-id="ec179-221">97</span></span>

<span data-ttu-id="ec179-222">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="ec179-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-223">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="ec179-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-224">98</span><span class="sxs-lookup"><span data-stu-id="ec179-224">98</span></span>

<span data-ttu-id="ec179-225">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="ec179-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-226">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="ec179-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-227">100</span><span class="sxs-lookup"><span data-stu-id="ec179-227">100</span></span>

<span data-ttu-id="ec179-228">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="ec179-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ec179-229">**其他**</span><span class="sxs-lookup"><span data-stu-id="ec179-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ec179-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="ec179-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ec179-231">備註</span><span class="sxs-lookup"><span data-stu-id="ec179-231">Remarks</span></span>

<span data-ttu-id="ec179-232">當您需要將 IP 資料包分割但未設定片段位時，黑洞路由器不會將網際網路控制訊息通訊協定傳回 (ICMP) 目的地無法連線的訊息。</span><span class="sxs-lookup"><span data-stu-id="ec179-232">A Black Hole router does not return the Internet Control Message Protocol (ICMP) Destination Unreachable messages when it needs to fragment an IP datagram with the Don't Fragment bit set.</span></span> <span data-ttu-id="ec179-233">TCP 取決於接收這些訊息來執行路徑 MTU 探索。</span><span class="sxs-lookup"><span data-stu-id="ec179-233">TCP depends on receiving these messages to perform Path MTU Discovery.</span></span>

<span data-ttu-id="ec179-234">啟用這項功能之後，如果區段的數次重新傳輸未確認，TCP 將會嘗試傳送區段，而不會設定片段位。</span><span class="sxs-lookup"><span data-stu-id="ec179-234">With this feature enabled, TCP will try to send segments without the Don't Fragment bit set if several retransmissions of a segment go unacknowledged.</span></span> <span data-ttu-id="ec179-235">如果已確認區段， (MSS) 的最大區段大小將會減少，而且在未來的封包中，將不會設定「不」片段位。</span><span class="sxs-lookup"><span data-stu-id="ec179-235">If the segment is acknowledged as a result, the maximum segment size (MSS) will be decreased and the Don't Fragment bit will be set in future packets on the connection.</span></span> <span data-ttu-id="ec179-236">啟用黑洞偵測會增加針對指定區段執行的重新傳輸數目上限。</span><span class="sxs-lookup"><span data-stu-id="ec179-236">Enabling black hole detection increases the maximum number of retransmissions performed for a given segment.</span></span>

## <a name="examples"></a><span data-ttu-id="ec179-237">範例</span><span class="sxs-lookup"><span data-stu-id="ec179-237">Examples</span></span>

<span data-ttu-id="ec179-238">[所有網路介面卡上的修改 PMTUBH 偵測](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c)，可在判斷網路上的最大傳輸單位時，自動探索黑色孔路由器。</span><span class="sxs-lookup"><span data-stu-id="ec179-238">The [Modify PMTUBH Detection on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/a576d97b-38fe-437e-a632-d2f7e122301c) enables the auto-discovery of black hole routers when determining the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="ec179-239">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec179-239">Requirements</span></span>



| <span data-ttu-id="ec179-240">需求</span><span class="sxs-lookup"><span data-stu-id="ec179-240">Requirement</span></span> | <span data-ttu-id="ec179-241">值</span><span class="sxs-lookup"><span data-stu-id="ec179-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec179-242">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec179-242">Minimum supported client</span></span><br/> | <span data-ttu-id="ec179-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ec179-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ec179-244">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec179-244">Minimum supported server</span></span><br/> | <span data-ttu-id="ec179-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ec179-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ec179-246">命名空間</span><span class="sxs-lookup"><span data-stu-id="ec179-246">Namespace</span></span><br/>                | <span data-ttu-id="ec179-247">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ec179-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ec179-248">MOF</span><span class="sxs-lookup"><span data-stu-id="ec179-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ec179-249"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ec179-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ec179-250">DLL</span><span class="sxs-lookup"><span data-stu-id="ec179-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec179-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec179-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ec179-252">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ec179-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ec179-253">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="ec179-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ec179-254">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="ec179-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="ec179-255">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="ec179-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="ec179-256">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="ec179-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="ec179-257">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="ec179-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

