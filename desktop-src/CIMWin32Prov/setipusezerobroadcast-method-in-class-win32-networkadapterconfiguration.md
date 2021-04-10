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
# <a name="setipusezerobroadcast-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="75d89-103">Win32 >networkadapterconfiguration 類別的 SetIPUseZeroBroadcast 方法 \_</span><span class="sxs-lookup"><span data-stu-id="75d89-103">SetIPUseZeroBroadcast method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="75d89-104">**SetIPUseZeroBroadcast** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定 IP 零廣播的使用方式。</span><span class="sxs-lookup"><span data-stu-id="75d89-104">The **SetIPUseZeroBroadcast** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set IP zero broadcast usage.</span></span>

<span data-ttu-id="75d89-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="75d89-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="75d89-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="75d89-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="75d89-107">語法</span><span class="sxs-lookup"><span data-stu-id="75d89-107">Syntax</span></span>


```mof
uint32 SetIPUseZeroBroadcast(
  [in] boolean IPUseZeroBroadcast
);
```



## <a name="parameters"></a><span data-ttu-id="75d89-108">參數</span><span class="sxs-lookup"><span data-stu-id="75d89-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75d89-109">*IPUseZeroBroadcast* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75d89-109">*IPUseZeroBroadcast* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75d89-110">若 **為 true**，則使用 IP 零廣播。</span><span class="sxs-lookup"><span data-stu-id="75d89-110">If **true**, IP zero broadcast is used.</span></span> <span data-ttu-id="75d89-111">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="75d89-111">The default is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75d89-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="75d89-112">Return value</span></span>

<span data-ttu-id="75d89-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="75d89-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="75d89-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="75d89-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="75d89-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="75d89-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="75d89-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="75d89-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-117">0</span><span class="sxs-lookup"><span data-stu-id="75d89-117">0</span></span>

<span data-ttu-id="75d89-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="75d89-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="75d89-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-120">1</span><span class="sxs-lookup"><span data-stu-id="75d89-120">1</span></span>

<span data-ttu-id="75d89-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="75d89-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="75d89-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-123">64</span><span class="sxs-lookup"><span data-stu-id="75d89-123">64</span></span>

<span data-ttu-id="75d89-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="75d89-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="75d89-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-126">65</span><span class="sxs-lookup"><span data-stu-id="75d89-126">65</span></span>

<span data-ttu-id="75d89-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="75d89-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="75d89-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-129">66</span><span class="sxs-lookup"><span data-stu-id="75d89-129">66</span></span>

<span data-ttu-id="75d89-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="75d89-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="75d89-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-132">67</span><span class="sxs-lookup"><span data-stu-id="75d89-132">67</span></span>

<span data-ttu-id="75d89-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="75d89-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="75d89-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-135">68</span><span class="sxs-lookup"><span data-stu-id="75d89-135">68</span></span>

<span data-ttu-id="75d89-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="75d89-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="75d89-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-138">69</span><span class="sxs-lookup"><span data-stu-id="75d89-138">69</span></span>

<span data-ttu-id="75d89-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="75d89-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="75d89-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-141">70</span><span class="sxs-lookup"><span data-stu-id="75d89-141">70</span></span>

<span data-ttu-id="75d89-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="75d89-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="75d89-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-144">71</span><span class="sxs-lookup"><span data-stu-id="75d89-144">71</span></span>

<span data-ttu-id="75d89-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="75d89-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="75d89-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-147">72</span><span class="sxs-lookup"><span data-stu-id="75d89-147">72</span></span>

<span data-ttu-id="75d89-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="75d89-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="75d89-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-150">73</span><span class="sxs-lookup"><span data-stu-id="75d89-150">73</span></span>

<span data-ttu-id="75d89-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="75d89-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="75d89-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-153">74</span><span class="sxs-lookup"><span data-stu-id="75d89-153">74</span></span>

<span data-ttu-id="75d89-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="75d89-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="75d89-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-156">75</span><span class="sxs-lookup"><span data-stu-id="75d89-156">75</span></span>

<span data-ttu-id="75d89-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="75d89-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="75d89-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-159">76</span><span class="sxs-lookup"><span data-stu-id="75d89-159">76</span></span>

<span data-ttu-id="75d89-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="75d89-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="75d89-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-162">77</span><span class="sxs-lookup"><span data-stu-id="75d89-162">77</span></span>

<span data-ttu-id="75d89-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="75d89-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="75d89-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-165">78</span><span class="sxs-lookup"><span data-stu-id="75d89-165">78</span></span>

<span data-ttu-id="75d89-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="75d89-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="75d89-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-168">79</span><span class="sxs-lookup"><span data-stu-id="75d89-168">79</span></span>

<span data-ttu-id="75d89-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="75d89-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="75d89-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-171">80</span><span class="sxs-lookup"><span data-stu-id="75d89-171">80</span></span>

<span data-ttu-id="75d89-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="75d89-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="75d89-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-174">81</span><span class="sxs-lookup"><span data-stu-id="75d89-174">81</span></span>

<span data-ttu-id="75d89-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="75d89-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="75d89-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-177">82</span><span class="sxs-lookup"><span data-stu-id="75d89-177">82</span></span>

<span data-ttu-id="75d89-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="75d89-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="75d89-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-180">83</span><span class="sxs-lookup"><span data-stu-id="75d89-180">83</span></span>

<span data-ttu-id="75d89-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="75d89-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="75d89-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-183">84</span><span class="sxs-lookup"><span data-stu-id="75d89-183">84</span></span>

<span data-ttu-id="75d89-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="75d89-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="75d89-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-186">85</span><span class="sxs-lookup"><span data-stu-id="75d89-186">85</span></span>

<span data-ttu-id="75d89-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="75d89-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="75d89-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-189">86</span><span class="sxs-lookup"><span data-stu-id="75d89-189">86</span></span>

<span data-ttu-id="75d89-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="75d89-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="75d89-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-192">87</span><span class="sxs-lookup"><span data-stu-id="75d89-192">87</span></span>

<span data-ttu-id="75d89-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="75d89-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="75d89-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-195">88</span><span class="sxs-lookup"><span data-stu-id="75d89-195">88</span></span>

<span data-ttu-id="75d89-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="75d89-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="75d89-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-198">89</span><span class="sxs-lookup"><span data-stu-id="75d89-198">89</span></span>

<span data-ttu-id="75d89-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="75d89-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="75d89-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-201">90</span><span class="sxs-lookup"><span data-stu-id="75d89-201">90</span></span>

<span data-ttu-id="75d89-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="75d89-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="75d89-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-204">91</span><span class="sxs-lookup"><span data-stu-id="75d89-204">91</span></span>

<span data-ttu-id="75d89-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="75d89-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="75d89-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-207">92</span><span class="sxs-lookup"><span data-stu-id="75d89-207">92</span></span>

<span data-ttu-id="75d89-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="75d89-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="75d89-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-210">93</span><span class="sxs-lookup"><span data-stu-id="75d89-210">93</span></span>

<span data-ttu-id="75d89-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="75d89-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="75d89-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-213">94</span><span class="sxs-lookup"><span data-stu-id="75d89-213">94</span></span>

<span data-ttu-id="75d89-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="75d89-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="75d89-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-216">95</span><span class="sxs-lookup"><span data-stu-id="75d89-216">95</span></span>

<span data-ttu-id="75d89-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="75d89-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="75d89-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-219">96</span><span class="sxs-lookup"><span data-stu-id="75d89-219">96</span></span>

<span data-ttu-id="75d89-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="75d89-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="75d89-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-222">97</span><span class="sxs-lookup"><span data-stu-id="75d89-222">97</span></span>

<span data-ttu-id="75d89-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="75d89-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="75d89-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-225">98</span><span class="sxs-lookup"><span data-stu-id="75d89-225">98</span></span>

<span data-ttu-id="75d89-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="75d89-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="75d89-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-228">100</span><span class="sxs-lookup"><span data-stu-id="75d89-228">100</span></span>

<span data-ttu-id="75d89-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="75d89-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="75d89-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="75d89-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="75d89-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="75d89-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="75d89-232">備註</span><span class="sxs-lookup"><span data-stu-id="75d89-232">Remarks</span></span>

<span data-ttu-id="75d89-233">如果 *IPUseZeroBroadcast* 參數設定為 **TRUE**，則 IP 會使用零 (0.0.0.0) ，而不是使用一則廣播 (255.255.255.255) 。</span><span class="sxs-lookup"><span data-stu-id="75d89-233">If the *IPUseZeroBroadcast* parameter is set to **TRUE**, then IP will use zero-broadcasts (0.0.0.0) instead of one-broadcasts (255.255.255.255).</span></span> <span data-ttu-id="75d89-234">大部分的系統都會使用一個廣播，但衍生自 BSD 的系統會使用零廣播。</span><span class="sxs-lookup"><span data-stu-id="75d89-234">Most systems use one-broadcasts, but systems derived from BSD implementations use zero-broadcasts.</span></span> <span data-ttu-id="75d89-235">使用不同廣播的系統將無法在相同的網路上交互操作。</span><span class="sxs-lookup"><span data-stu-id="75d89-235">Systems that use different broadcasts will not interoperate on the same network.</span></span>

## <a name="examples"></a><span data-ttu-id="75d89-236">範例</span><span class="sxs-lookup"><span data-stu-id="75d89-236">Examples</span></span>

<span data-ttu-id="75d89-237">[修改 Zero-Broadcast 用於所有網路介面卡](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3)的 VBScript 範例會將電腦設定為使用零的廣播 (0.0.0.0) 而不是單一廣播 (255.255.255.255) 。</span><span class="sxs-lookup"><span data-stu-id="75d89-237">The [Modify Zero-Broadcast Use for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/3d1ec74a-bf96-41cf-bb90-f98cd6494fb3) VBScript sample configures a computer to use zero-broadcasts (0.0.0.0) rather than one-broadcasts (255.255.255.255).</span></span>

## <a name="requirements"></a><span data-ttu-id="75d89-238">規格需求</span><span class="sxs-lookup"><span data-stu-id="75d89-238">Requirements</span></span>



| <span data-ttu-id="75d89-239">需求</span><span class="sxs-lookup"><span data-stu-id="75d89-239">Requirement</span></span> | <span data-ttu-id="75d89-240">值</span><span class="sxs-lookup"><span data-stu-id="75d89-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="75d89-241">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="75d89-241">Minimum supported client</span></span><br/> | <span data-ttu-id="75d89-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="75d89-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="75d89-243">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="75d89-243">Minimum supported server</span></span><br/> | <span data-ttu-id="75d89-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="75d89-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="75d89-245">命名空間</span><span class="sxs-lookup"><span data-stu-id="75d89-245">Namespace</span></span><br/>                | <span data-ttu-id="75d89-246">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="75d89-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="75d89-247">MOF</span><span class="sxs-lookup"><span data-stu-id="75d89-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75d89-248"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="75d89-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="75d89-249">DLL</span><span class="sxs-lookup"><span data-stu-id="75d89-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75d89-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75d89-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75d89-251">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75d89-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75d89-252">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="75d89-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="75d89-253">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="75d89-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="75d89-254">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="75d89-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="75d89-255">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="75d89-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="75d89-256">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="75d89-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

