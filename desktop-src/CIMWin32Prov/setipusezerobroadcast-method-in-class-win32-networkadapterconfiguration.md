---
description: SetIPUseZeroBroadcast WMI 類別靜態方法是用來設定 IP 零廣播的使用方式。
ms.assetid: d20ac6fc-a5d5-4ad9-a2a5-65142b4c7d02
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetIPUseZeroBroadcast 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPUseZeroBroadcast
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 564f122242407f4d6f5dd28da9fd4d151ab6b47f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110948"
---
# <a name="setipusezerobroadcast-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="affbf-103">Win32 >networkadapterconfiguration 類別的 SetIPUseZeroBroadcast 方法 \_</span><span class="sxs-lookup"><span data-stu-id="affbf-103">SetIPUseZeroBroadcast method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="affbf-104">**SetIPUseZeroBroadcast** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定 IP 零廣播的使用方式。</span><span class="sxs-lookup"><span data-stu-id="affbf-104">The **SetIPUseZeroBroadcast** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set IP zero broadcast usage.</span></span>

<span data-ttu-id="affbf-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="affbf-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="affbf-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="affbf-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="affbf-107">語法</span><span class="sxs-lookup"><span data-stu-id="affbf-107">Syntax</span></span>


```mof
uint32 SetIPUseZeroBroadcast(
  [in] boolean IPUseZeroBroadcast
);
```



## <a name="parameters"></a><span data-ttu-id="affbf-108">參數</span><span class="sxs-lookup"><span data-stu-id="affbf-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="affbf-109">*IPUseZeroBroadcast* \[在\]</span><span class="sxs-lookup"><span data-stu-id="affbf-109">*IPUseZeroBroadcast* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="affbf-110">若 **為 true**，則使用 IP 零廣播。</span><span class="sxs-lookup"><span data-stu-id="affbf-110">If **true**, IP zero broadcast is used.</span></span> <span data-ttu-id="affbf-111">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="affbf-111">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="affbf-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="affbf-112">Return value</span></span>

<span data-ttu-id="affbf-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="affbf-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="affbf-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="affbf-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="affbf-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="affbf-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="affbf-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="affbf-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-117">0</span><span class="sxs-lookup"><span data-stu-id="affbf-117">0</span></span>

<span data-ttu-id="affbf-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="affbf-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="affbf-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-120">1</span><span class="sxs-lookup"><span data-stu-id="affbf-120">1</span></span>

<span data-ttu-id="affbf-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="affbf-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="affbf-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-123">64</span><span class="sxs-lookup"><span data-stu-id="affbf-123">64</span></span>

<span data-ttu-id="affbf-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="affbf-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="affbf-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-126">65</span><span class="sxs-lookup"><span data-stu-id="affbf-126">65</span></span>

<span data-ttu-id="affbf-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="affbf-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="affbf-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-129">66</span><span class="sxs-lookup"><span data-stu-id="affbf-129">66</span></span>

<span data-ttu-id="affbf-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="affbf-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="affbf-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-132">67</span><span class="sxs-lookup"><span data-stu-id="affbf-132">67</span></span>

<span data-ttu-id="affbf-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="affbf-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="affbf-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-135">68</span><span class="sxs-lookup"><span data-stu-id="affbf-135">68</span></span>

<span data-ttu-id="affbf-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="affbf-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="affbf-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-138">69</span><span class="sxs-lookup"><span data-stu-id="affbf-138">69</span></span>

<span data-ttu-id="affbf-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="affbf-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="affbf-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-141">70</span><span class="sxs-lookup"><span data-stu-id="affbf-141">70</span></span>

<span data-ttu-id="affbf-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="affbf-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="affbf-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-144">71</span><span class="sxs-lookup"><span data-stu-id="affbf-144">71</span></span>

<span data-ttu-id="affbf-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="affbf-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="affbf-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-147">72</span><span class="sxs-lookup"><span data-stu-id="affbf-147">72</span></span>

<span data-ttu-id="affbf-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="affbf-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="affbf-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-150">73</span><span class="sxs-lookup"><span data-stu-id="affbf-150">73</span></span>

<span data-ttu-id="affbf-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="affbf-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="affbf-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-153">74</span><span class="sxs-lookup"><span data-stu-id="affbf-153">74</span></span>

<span data-ttu-id="affbf-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="affbf-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="affbf-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-156">75</span><span class="sxs-lookup"><span data-stu-id="affbf-156">75</span></span>

<span data-ttu-id="affbf-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="affbf-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="affbf-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-159">76</span><span class="sxs-lookup"><span data-stu-id="affbf-159">76</span></span>

<span data-ttu-id="affbf-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="affbf-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="affbf-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-162">77</span><span class="sxs-lookup"><span data-stu-id="affbf-162">77</span></span>

<span data-ttu-id="affbf-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="affbf-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="affbf-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-165">78</span><span class="sxs-lookup"><span data-stu-id="affbf-165">78</span></span>

<span data-ttu-id="affbf-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="affbf-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="affbf-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-168">79</span><span class="sxs-lookup"><span data-stu-id="affbf-168">79</span></span>

<span data-ttu-id="affbf-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="affbf-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="affbf-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-171">80</span><span class="sxs-lookup"><span data-stu-id="affbf-171">80</span></span>

<span data-ttu-id="affbf-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="affbf-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="affbf-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-174">81</span><span class="sxs-lookup"><span data-stu-id="affbf-174">81</span></span>

<span data-ttu-id="affbf-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="affbf-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="affbf-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-177">82</span><span class="sxs-lookup"><span data-stu-id="affbf-177">82</span></span>

<span data-ttu-id="affbf-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="affbf-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="affbf-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-180">83</span><span class="sxs-lookup"><span data-stu-id="affbf-180">83</span></span>

<span data-ttu-id="affbf-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="affbf-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="affbf-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-183">84</span><span class="sxs-lookup"><span data-stu-id="affbf-183">84</span></span>

<span data-ttu-id="affbf-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="affbf-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="affbf-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-186">85</span><span class="sxs-lookup"><span data-stu-id="affbf-186">85</span></span>

<span data-ttu-id="affbf-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="affbf-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="affbf-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-189">86</span><span class="sxs-lookup"><span data-stu-id="affbf-189">86</span></span>

<span data-ttu-id="affbf-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="affbf-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="affbf-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-192">87</span><span class="sxs-lookup"><span data-stu-id="affbf-192">87</span></span>

<span data-ttu-id="affbf-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="affbf-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="affbf-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-195">88</span><span class="sxs-lookup"><span data-stu-id="affbf-195">88</span></span>

<span data-ttu-id="affbf-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="affbf-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="affbf-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-198">89</span><span class="sxs-lookup"><span data-stu-id="affbf-198">89</span></span>

<span data-ttu-id="affbf-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="affbf-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="affbf-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-201">90</span><span class="sxs-lookup"><span data-stu-id="affbf-201">90</span></span>

<span data-ttu-id="affbf-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="affbf-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="affbf-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-204">91</span><span class="sxs-lookup"><span data-stu-id="affbf-204">91</span></span>

<span data-ttu-id="affbf-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="affbf-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="affbf-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-207">92</span><span class="sxs-lookup"><span data-stu-id="affbf-207">92</span></span>

<span data-ttu-id="affbf-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="affbf-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="affbf-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-210">93</span><span class="sxs-lookup"><span data-stu-id="affbf-210">93</span></span>

<span data-ttu-id="affbf-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="affbf-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="affbf-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-213">94</span><span class="sxs-lookup"><span data-stu-id="affbf-213">94</span></span>

<span data-ttu-id="affbf-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="affbf-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="affbf-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-216">95</span><span class="sxs-lookup"><span data-stu-id="affbf-216">95</span></span>

<span data-ttu-id="affbf-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="affbf-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="affbf-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-219">96</span><span class="sxs-lookup"><span data-stu-id="affbf-219">96</span></span>

<span data-ttu-id="affbf-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="affbf-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="affbf-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-222">97</span><span class="sxs-lookup"><span data-stu-id="affbf-222">97</span></span>

<span data-ttu-id="affbf-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="affbf-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="affbf-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-225">98</span><span class="sxs-lookup"><span data-stu-id="affbf-225">98</span></span>

<span data-ttu-id="affbf-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="affbf-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="affbf-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-228">100</span><span class="sxs-lookup"><span data-stu-id="affbf-228">100</span></span>

<span data-ttu-id="affbf-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="affbf-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="affbf-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="affbf-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="affbf-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="affbf-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="affbf-232">備註</span><span class="sxs-lookup"><span data-stu-id="affbf-232">Remarks</span></span>

<span data-ttu-id="affbf-233">如果 *IPUseZeroBroadcast* 參數設定為 **TRUE**，則 IP 會使用零 (0.0.0.0) ，而不是使用一則廣播 (255.255.255.255) 。</span><span class="sxs-lookup"><span data-stu-id="affbf-233">If the *IPUseZeroBroadcast* parameter is set to **TRUE**, then IP will use zero-broadcasts (0.0.0.0) instead of one-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="affbf-234">大部分的系統都會使用一個廣播，但衍生自 BSD 的系統會使用零廣播。</span><span class="sxs-lookup"><span data-stu-id="affbf-234">Most systems use one-broadcasts, but systems derived from BSD implementations use zero-broadcasts.</span></span> <span data-ttu-id="affbf-235">使用不同廣播的系統將無法在相同的網路上交互操作。</span><span class="sxs-lookup"><span data-stu-id="affbf-235">Systems that use different broadcasts will not interoperate on the same network.</span></span>

## <a name="examples"></a><span data-ttu-id="affbf-236">範例</span><span class="sxs-lookup"><span data-stu-id="affbf-236">Examples</span></span>

<span data-ttu-id="affbf-237">[修改 Zero-Broadcast 用於所有網路介面卡](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3)的 VBScript 範例會將電腦設定為使用零的廣播 (0.0.0.0) 而不是單一廣播 (255.255.255.255) 。</span><span class="sxs-lookup"><span data-stu-id="affbf-237">The [Modify Zero-Broadcast Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) VBScript sample configures a computer to use zero-broadcasts (0.0.0.0) rather than one-broadcasts (255.255.255.255).</span></span>

## <a name="requirements"></a><span data-ttu-id="affbf-238">規格需求</span><span class="sxs-lookup"><span data-stu-id="affbf-238">Requirements</span></span>



| <span data-ttu-id="affbf-239">需求</span><span class="sxs-lookup"><span data-stu-id="affbf-239">Requirement</span></span> | <span data-ttu-id="affbf-240">值</span><span class="sxs-lookup"><span data-stu-id="affbf-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="affbf-241">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="affbf-241">Minimum supported client</span></span><br/> | <span data-ttu-id="affbf-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="affbf-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="affbf-243">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="affbf-243">Minimum supported server</span></span><br/> | <span data-ttu-id="affbf-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="affbf-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="affbf-245">命名空間</span><span class="sxs-lookup"><span data-stu-id="affbf-245">Namespace</span></span><br/>                | <span data-ttu-id="affbf-246">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="affbf-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="affbf-247">MOF</span><span class="sxs-lookup"><span data-stu-id="affbf-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="affbf-248"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="affbf-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="affbf-249">DLL</span><span class="sxs-lookup"><span data-stu-id="affbf-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="affbf-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="affbf-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="affbf-251">另請參閱</span><span class="sxs-lookup"><span data-stu-id="affbf-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="affbf-252">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="affbf-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="affbf-253">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="affbf-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="affbf-254">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="affbf-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="affbf-255">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="affbf-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="affbf-256">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="affbf-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

