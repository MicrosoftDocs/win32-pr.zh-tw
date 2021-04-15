---
description: SetDeadGWDetect WMI 類別靜態方法是用來啟用死閘道偵測。
ms.assetid: c813aaef-7215-4759-b68f-7808fd203d9c
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetDeadGWDetect 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDeadGWDetect
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 83f62d84af193be99850f1a82b720a2983ca77c3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468080"
---
# <a name="setdeadgwdetect-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="558e0-103">Win32 >networkadapterconfiguration 類別的 SetDeadGWDetect 方法 \_</span><span class="sxs-lookup"><span data-stu-id="558e0-103">SetDeadGWDetect method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="558e0-104">**SetDeadGWDetect** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來啟用死閘道偵測。</span><span class="sxs-lookup"><span data-stu-id="558e0-104">The **SetDeadGWDetect** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable dead gateway detection.</span></span>

<span data-ttu-id="558e0-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="558e0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="558e0-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="558e0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="558e0-107">語法</span><span class="sxs-lookup"><span data-stu-id="558e0-107">Syntax</span></span>


```mof
uint32 SetDeadGWDetect(
  [in] boolean DeadGWDetectEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="558e0-108">參數</span><span class="sxs-lookup"><span data-stu-id="558e0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="558e0-109">*DeadGWDetectEnabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="558e0-109">*DeadGWDetectEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="558e0-110">若 **為 true，則** 應啟用死閘道偵測。</span><span class="sxs-lookup"><span data-stu-id="558e0-110">If **true**, dead gateway detection should be enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="558e0-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="558e0-111">Return value</span></span>

<span data-ttu-id="558e0-112">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="558e0-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="558e0-113">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="558e0-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="558e0-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="558e0-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="558e0-115">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="558e0-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-116">0</span><span class="sxs-lookup"><span data-stu-id="558e0-116">0</span></span>

<span data-ttu-id="558e0-117">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="558e0-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-118">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="558e0-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-119">1</span><span class="sxs-lookup"><span data-stu-id="558e0-119">1</span></span>

<span data-ttu-id="558e0-120">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="558e0-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-121">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="558e0-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-122">64</span><span class="sxs-lookup"><span data-stu-id="558e0-122">64</span></span>

<span data-ttu-id="558e0-123">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="558e0-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-124">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="558e0-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-125">65</span><span class="sxs-lookup"><span data-stu-id="558e0-125">65</span></span>

<span data-ttu-id="558e0-126">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="558e0-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-127">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="558e0-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-128">66</span><span class="sxs-lookup"><span data-stu-id="558e0-128">66</span></span>

<span data-ttu-id="558e0-129">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="558e0-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-130">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="558e0-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-131">67</span><span class="sxs-lookup"><span data-stu-id="558e0-131">67</span></span>

<span data-ttu-id="558e0-132">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="558e0-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-133">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="558e0-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-134">68</span><span class="sxs-lookup"><span data-stu-id="558e0-134">68</span></span>

<span data-ttu-id="558e0-135">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="558e0-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-136">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="558e0-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-137">69</span><span class="sxs-lookup"><span data-stu-id="558e0-137">69</span></span>

<span data-ttu-id="558e0-138">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="558e0-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-139">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="558e0-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-140">70</span><span class="sxs-lookup"><span data-stu-id="558e0-140">70</span></span>

<span data-ttu-id="558e0-141">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="558e0-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-142">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="558e0-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-143">71</span><span class="sxs-lookup"><span data-stu-id="558e0-143">71</span></span>

<span data-ttu-id="558e0-144">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="558e0-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-145">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="558e0-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-146">72</span><span class="sxs-lookup"><span data-stu-id="558e0-146">72</span></span>

<span data-ttu-id="558e0-147">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="558e0-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-148">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="558e0-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-149">73</span><span class="sxs-lookup"><span data-stu-id="558e0-149">73</span></span>

<span data-ttu-id="558e0-150">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="558e0-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-151">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="558e0-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-152">74</span><span class="sxs-lookup"><span data-stu-id="558e0-152">74</span></span>

<span data-ttu-id="558e0-153">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="558e0-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-154">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="558e0-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-155">75</span><span class="sxs-lookup"><span data-stu-id="558e0-155">75</span></span>

<span data-ttu-id="558e0-156">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="558e0-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-157">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="558e0-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-158">76</span><span class="sxs-lookup"><span data-stu-id="558e0-158">76</span></span>

<span data-ttu-id="558e0-159">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="558e0-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-160">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="558e0-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-161">77</span><span class="sxs-lookup"><span data-stu-id="558e0-161">77</span></span>

<span data-ttu-id="558e0-162">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="558e0-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-163">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="558e0-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-164">78</span><span class="sxs-lookup"><span data-stu-id="558e0-164">78</span></span>

<span data-ttu-id="558e0-165">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="558e0-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-166">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="558e0-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-167">79</span><span class="sxs-lookup"><span data-stu-id="558e0-167">79</span></span>

<span data-ttu-id="558e0-168">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="558e0-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-169">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="558e0-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-170">80</span><span class="sxs-lookup"><span data-stu-id="558e0-170">80</span></span>

<span data-ttu-id="558e0-171">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="558e0-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-172">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="558e0-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-173">81</span><span class="sxs-lookup"><span data-stu-id="558e0-173">81</span></span>

<span data-ttu-id="558e0-174">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="558e0-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-175">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="558e0-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-176">82</span><span class="sxs-lookup"><span data-stu-id="558e0-176">82</span></span>

<span data-ttu-id="558e0-177">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="558e0-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-178">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="558e0-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-179">83</span><span class="sxs-lookup"><span data-stu-id="558e0-179">83</span></span>

<span data-ttu-id="558e0-180">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="558e0-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-181">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="558e0-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-182">84</span><span class="sxs-lookup"><span data-stu-id="558e0-182">84</span></span>

<span data-ttu-id="558e0-183">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="558e0-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-184">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="558e0-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-185">85</span><span class="sxs-lookup"><span data-stu-id="558e0-185">85</span></span>

<span data-ttu-id="558e0-186">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="558e0-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-187">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="558e0-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-188">86</span><span class="sxs-lookup"><span data-stu-id="558e0-188">86</span></span>

<span data-ttu-id="558e0-189">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="558e0-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-190">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="558e0-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-191">87</span><span class="sxs-lookup"><span data-stu-id="558e0-191">87</span></span>

<span data-ttu-id="558e0-192">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="558e0-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-193">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="558e0-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-194">88</span><span class="sxs-lookup"><span data-stu-id="558e0-194">88</span></span>

<span data-ttu-id="558e0-195">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="558e0-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-196">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="558e0-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-197">89</span><span class="sxs-lookup"><span data-stu-id="558e0-197">89</span></span>

<span data-ttu-id="558e0-198">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="558e0-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-199">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="558e0-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-200">90</span><span class="sxs-lookup"><span data-stu-id="558e0-200">90</span></span>

<span data-ttu-id="558e0-201">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="558e0-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-202">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="558e0-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-203">91</span><span class="sxs-lookup"><span data-stu-id="558e0-203">91</span></span>

<span data-ttu-id="558e0-204">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="558e0-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-205">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="558e0-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-206">92</span><span class="sxs-lookup"><span data-stu-id="558e0-206">92</span></span>

<span data-ttu-id="558e0-207">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="558e0-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-208">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="558e0-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-209">93</span><span class="sxs-lookup"><span data-stu-id="558e0-209">93</span></span>

<span data-ttu-id="558e0-210">已經存在。</span><span class="sxs-lookup"><span data-stu-id="558e0-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-211">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="558e0-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-212">94</span><span class="sxs-lookup"><span data-stu-id="558e0-212">94</span></span>

<span data-ttu-id="558e0-213">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="558e0-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-214">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="558e0-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-215">95</span><span class="sxs-lookup"><span data-stu-id="558e0-215">95</span></span>

<span data-ttu-id="558e0-216">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="558e0-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-217">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="558e0-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-218">96</span><span class="sxs-lookup"><span data-stu-id="558e0-218">96</span></span>

<span data-ttu-id="558e0-219">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="558e0-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-220">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="558e0-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-221">97</span><span class="sxs-lookup"><span data-stu-id="558e0-221">97</span></span>

<span data-ttu-id="558e0-222">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="558e0-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-223">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="558e0-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-224">98</span><span class="sxs-lookup"><span data-stu-id="558e0-224">98</span></span>

<span data-ttu-id="558e0-225">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="558e0-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-226">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="558e0-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-227">100</span><span class="sxs-lookup"><span data-stu-id="558e0-227">100</span></span>

<span data-ttu-id="558e0-228">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="558e0-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="558e0-229">**其他**</span><span class="sxs-lookup"><span data-stu-id="558e0-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="558e0-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="558e0-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="558e0-231">備註</span><span class="sxs-lookup"><span data-stu-id="558e0-231">Remarks</span></span>

<span data-ttu-id="558e0-232">啟用這項功能之後，TCP 會要求 IP 變更為備份閘道，如果它會多次重新傳輸區段，而不會收到回應。</span><span class="sxs-lookup"><span data-stu-id="558e0-232">With this feature enabled, TCP asks IP to change to a backup gateway if it retransmits a segment several times without receiving a response.</span></span>

## <a name="examples"></a><span data-ttu-id="558e0-233">範例</span><span class="sxs-lookup"><span data-stu-id="558e0-233">Examples</span></span>

<span data-ttu-id="558e0-234">TechNet 資源庫上的所有網路介面卡 VBScript 範例的「 [啟用死閘道偵測](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) 」會使用 **SetDeadGWDetect** 來設定電腦上的所有網路介面卡，以自動偵測死閘道。</span><span class="sxs-lookup"><span data-stu-id="558e0-234">The [Enable Dead Gateway Detection for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/4a24b080-1a8b-4085-9419-58d096ef8437) VBScript sample on TechNet Gallery uses **SetDeadGWDetect** to configure all network adapters on a computer to automatically detect dead gateways.</span></span>

## <a name="requirements"></a><span data-ttu-id="558e0-235">規格需求</span><span class="sxs-lookup"><span data-stu-id="558e0-235">Requirements</span></span>



| <span data-ttu-id="558e0-236">需求</span><span class="sxs-lookup"><span data-stu-id="558e0-236">Requirement</span></span> | <span data-ttu-id="558e0-237">值</span><span class="sxs-lookup"><span data-stu-id="558e0-237">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="558e0-238">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="558e0-238">Minimum supported client</span></span><br/> | <span data-ttu-id="558e0-239">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="558e0-239">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="558e0-240">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="558e0-240">Minimum supported server</span></span><br/> | <span data-ttu-id="558e0-241">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="558e0-241">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="558e0-242">命名空間</span><span class="sxs-lookup"><span data-stu-id="558e0-242">Namespace</span></span><br/>                | <span data-ttu-id="558e0-243">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="558e0-243">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="558e0-244">MOF</span><span class="sxs-lookup"><span data-stu-id="558e0-244">MOF</span></span><br/>                      | <dl> <span data-ttu-id="558e0-245"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="558e0-245"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="558e0-246">DLL</span><span class="sxs-lookup"><span data-stu-id="558e0-246">DLL</span></span><br/>                      | <dl> <span data-ttu-id="558e0-247"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="558e0-247"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="558e0-248">另請參閱</span><span class="sxs-lookup"><span data-stu-id="558e0-248">See also</span></span>

<dl> <dt>

[<span data-ttu-id="558e0-249">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="558e0-249">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="558e0-250">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="558e0-250">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="558e0-251">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="558e0-251">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="558e0-252">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="558e0-252">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="558e0-253">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="558e0-253">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

