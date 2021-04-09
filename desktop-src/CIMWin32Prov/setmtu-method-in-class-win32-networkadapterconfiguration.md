---
description: SetMTU WMI 類別靜態方法是用來設定網路介面 (MTU) 的預設最大傳輸單位。
ms.assetid: 262c8bd7-1057-4204-80ab-725c60fc9c52
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetMTU 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetMTU
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 466c344892f2c4bf4a1e979ac9c1f50cd709325a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688963"
---
# <a name="setmtu-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="35c90-103">Win32 >networkadapterconfiguration 類別的 SetMTU 方法 \_</span><span class="sxs-lookup"><span data-stu-id="35c90-103">SetMTU method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="35c90-104">**SetMTU** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定網路介面 (MTU) 的預設最大傳輸單位。</span><span class="sxs-lookup"><span data-stu-id="35c90-104">The **SetMTU** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Maximum Transmission Unit (MTU) for a network interface.</span></span>

<span data-ttu-id="35c90-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="35c90-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="35c90-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="35c90-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="35c90-107">語法</span><span class="sxs-lookup"><span data-stu-id="35c90-107">Syntax</span></span>


```mof
uint32 SetMTU(
  [in] uint32 MTU
);
```



## <a name="parameters"></a><span data-ttu-id="35c90-108">參數</span><span class="sxs-lookup"><span data-stu-id="35c90-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35c90-109">*MTU* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35c90-109">*MTU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35c90-110">網路介面的預設最大傳輸單位 (MTU) 。</span><span class="sxs-lookup"><span data-stu-id="35c90-110">Default Maximum Transmission Unit (MTU) for a network interface.</span></span> <span data-ttu-id="35c90-111">此值的範圍會跨越基礎網路所支援的 MTU (68) 的最小封包大小。</span><span class="sxs-lookup"><span data-stu-id="35c90-111">The range of this value spans the minimum packet size (68) to the MTU supported by the underlying network.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35c90-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="35c90-112">Return value</span></span>

<span data-ttu-id="35c90-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="35c90-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="35c90-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="35c90-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="35c90-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="35c90-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="35c90-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="35c90-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-117">0</span><span class="sxs-lookup"><span data-stu-id="35c90-117">0</span></span>

<span data-ttu-id="35c90-118">順利完成。</span><span class="sxs-lookup"><span data-stu-id="35c90-118">Successful completion.</span></span> <span data-ttu-id="35c90-119">不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="35c90-119">No reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-120">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="35c90-120">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-121">1</span><span class="sxs-lookup"><span data-stu-id="35c90-121">1</span></span>

<span data-ttu-id="35c90-122">順利完成。</span><span class="sxs-lookup"><span data-stu-id="35c90-122">Successful completion.</span></span> <span data-ttu-id="35c90-123">需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="35c90-123">Reboot is required.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-124">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="35c90-124">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-125">64</span><span class="sxs-lookup"><span data-stu-id="35c90-125">64</span></span>

<span data-ttu-id="35c90-126">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="35c90-126">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-127">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="35c90-127">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-128">65</span><span class="sxs-lookup"><span data-stu-id="35c90-128">65</span></span>

<span data-ttu-id="35c90-129">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="35c90-129">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-130">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="35c90-130">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-131">66</span><span class="sxs-lookup"><span data-stu-id="35c90-131">66</span></span>

<span data-ttu-id="35c90-132">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="35c90-132">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-133">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="35c90-133">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-134">67</span><span class="sxs-lookup"><span data-stu-id="35c90-134">67</span></span>

<span data-ttu-id="35c90-135">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="35c90-135">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-136">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="35c90-136">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-137">68</span><span class="sxs-lookup"><span data-stu-id="35c90-137">68</span></span>

<span data-ttu-id="35c90-138">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="35c90-138">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-139">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="35c90-139">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-140">69</span><span class="sxs-lookup"><span data-stu-id="35c90-140">69</span></span>

<span data-ttu-id="35c90-141">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="35c90-141">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-142">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="35c90-142">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-143">70</span><span class="sxs-lookup"><span data-stu-id="35c90-143">70</span></span>

<span data-ttu-id="35c90-144">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="35c90-144">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-145">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="35c90-145">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-146">71</span><span class="sxs-lookup"><span data-stu-id="35c90-146">71</span></span>

<span data-ttu-id="35c90-147">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="35c90-147">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-148">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="35c90-148">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-149">72</span><span class="sxs-lookup"><span data-stu-id="35c90-149">72</span></span>

<span data-ttu-id="35c90-150">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="35c90-150">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-151">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="35c90-151">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-152">73</span><span class="sxs-lookup"><span data-stu-id="35c90-152">73</span></span>

<span data-ttu-id="35c90-153">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="35c90-153">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-154">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="35c90-154">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-155">74</span><span class="sxs-lookup"><span data-stu-id="35c90-155">74</span></span>

<span data-ttu-id="35c90-156">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="35c90-156">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-157">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="35c90-157">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-158">75</span><span class="sxs-lookup"><span data-stu-id="35c90-158">75</span></span>

<span data-ttu-id="35c90-159">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="35c90-159">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-160">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="35c90-160">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-161">76</span><span class="sxs-lookup"><span data-stu-id="35c90-161">76</span></span>

<span data-ttu-id="35c90-162">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="35c90-162">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-163">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="35c90-163">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-164">77</span><span class="sxs-lookup"><span data-stu-id="35c90-164">77</span></span>

<span data-ttu-id="35c90-165">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="35c90-165">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-166">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="35c90-166">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-167">78</span><span class="sxs-lookup"><span data-stu-id="35c90-167">78</span></span>

<span data-ttu-id="35c90-168">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="35c90-168">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-169">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="35c90-169">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-170">79</span><span class="sxs-lookup"><span data-stu-id="35c90-170">79</span></span>

<span data-ttu-id="35c90-171">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="35c90-171">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-172">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="35c90-172">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-173">80</span><span class="sxs-lookup"><span data-stu-id="35c90-173">80</span></span>

<span data-ttu-id="35c90-174">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="35c90-174">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-175">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="35c90-175">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-176">81</span><span class="sxs-lookup"><span data-stu-id="35c90-176">81</span></span>

<span data-ttu-id="35c90-177">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="35c90-177">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-178">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="35c90-178">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-179">82</span><span class="sxs-lookup"><span data-stu-id="35c90-179">82</span></span>

<span data-ttu-id="35c90-180">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="35c90-180">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-181">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="35c90-181">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-182">83</span><span class="sxs-lookup"><span data-stu-id="35c90-182">83</span></span>

<span data-ttu-id="35c90-183">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="35c90-183">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-184">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="35c90-184">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-185">84</span><span class="sxs-lookup"><span data-stu-id="35c90-185">84</span></span>

<span data-ttu-id="35c90-186">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="35c90-186">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-187">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="35c90-187">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-188">85</span><span class="sxs-lookup"><span data-stu-id="35c90-188">85</span></span>

<span data-ttu-id="35c90-189">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="35c90-189">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-190">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="35c90-190">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-191">86</span><span class="sxs-lookup"><span data-stu-id="35c90-191">86</span></span>

<span data-ttu-id="35c90-192">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="35c90-192">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-193">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="35c90-193">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-194">87</span><span class="sxs-lookup"><span data-stu-id="35c90-194">87</span></span>

<span data-ttu-id="35c90-195">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="35c90-195">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-196">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="35c90-196">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-197">88</span><span class="sxs-lookup"><span data-stu-id="35c90-197">88</span></span>

<span data-ttu-id="35c90-198">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="35c90-198">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-199">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="35c90-199">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-200">89</span><span class="sxs-lookup"><span data-stu-id="35c90-200">89</span></span>

<span data-ttu-id="35c90-201">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="35c90-201">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-202">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="35c90-202">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-203">90</span><span class="sxs-lookup"><span data-stu-id="35c90-203">90</span></span>

<span data-ttu-id="35c90-204">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="35c90-204">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-205">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="35c90-205">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-206">91</span><span class="sxs-lookup"><span data-stu-id="35c90-206">91</span></span>

<span data-ttu-id="35c90-207">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="35c90-207">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-208">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="35c90-208">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-209">92</span><span class="sxs-lookup"><span data-stu-id="35c90-209">92</span></span>

<span data-ttu-id="35c90-210">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="35c90-210">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-211">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="35c90-211">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-212">93</span><span class="sxs-lookup"><span data-stu-id="35c90-212">93</span></span>

<span data-ttu-id="35c90-213">已經存在。</span><span class="sxs-lookup"><span data-stu-id="35c90-213">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-214">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="35c90-214">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-215">94</span><span class="sxs-lookup"><span data-stu-id="35c90-215">94</span></span>

<span data-ttu-id="35c90-216">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="35c90-216">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-217">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="35c90-217">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-218">95</span><span class="sxs-lookup"><span data-stu-id="35c90-218">95</span></span>

<span data-ttu-id="35c90-219">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="35c90-219">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-220">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="35c90-220">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-221">96</span><span class="sxs-lookup"><span data-stu-id="35c90-221">96</span></span>

<span data-ttu-id="35c90-222">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="35c90-222">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-223">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="35c90-223">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-224">97</span><span class="sxs-lookup"><span data-stu-id="35c90-224">97</span></span>

<span data-ttu-id="35c90-225">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="35c90-225">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-226">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="35c90-226">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-227">98</span><span class="sxs-lookup"><span data-stu-id="35c90-227">98</span></span>

<span data-ttu-id="35c90-228">並非所有的 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="35c90-228">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-229">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="35c90-229">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-230">100</span><span class="sxs-lookup"><span data-stu-id="35c90-230">100</span></span>

<span data-ttu-id="35c90-231">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="35c90-231">DHCP is not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="35c90-232">**其他**</span><span class="sxs-lookup"><span data-stu-id="35c90-232">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="35c90-233">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="35c90-233">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="35c90-234">備註</span><span class="sxs-lookup"><span data-stu-id="35c90-234">Remarks</span></span>

<span data-ttu-id="35c90-235">MTU 是傳輸會透過基礎網路傳輸的封包大小上限 (位元組) 。</span><span class="sxs-lookup"><span data-stu-id="35c90-235">The MTU is the maximum packet size (in bytes) that a transport will transmit over the underlying network.</span></span> <span data-ttu-id="35c90-236">大小包含傳輸標頭。</span><span class="sxs-lookup"><span data-stu-id="35c90-236">The size includes the transport header.</span></span>

<span data-ttu-id="35c90-237">請注意，IP 資料包可以橫跨多個封包。</span><span class="sxs-lookup"><span data-stu-id="35c90-237">Note that an IP datagram can span multiple packets.</span></span> <span data-ttu-id="35c90-238">大於基礎網路預設值的值，會導致使用網路預設 MTU 的傳輸。</span><span class="sxs-lookup"><span data-stu-id="35c90-238">Values larger than the default for the underlying network result in the transport using the network default MTU.</span></span> <span data-ttu-id="35c90-239">小於68的值會導致使用68的 MTU 進行傳輸。</span><span class="sxs-lookup"><span data-stu-id="35c90-239">Values smaller than 68 result in the transport using an MTU of 68.</span></span>

## <a name="examples"></a><span data-ttu-id="35c90-240">範例</span><span class="sxs-lookup"><span data-stu-id="35c90-240">Examples</span></span>

<span data-ttu-id="35c90-241">[ [修改所有網路介面卡的 MTU](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) ] VBScript 範例會設定電腦上安裝之所有網路介面卡的最大傳輸單位。</span><span class="sxs-lookup"><span data-stu-id="35c90-241">The [Modify the MTU for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/49c26363-d46c-4288-9c8d-feb0a1982998) VBScript sample configures the maximum transmission unit for all network adapters installed in a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="35c90-242">規格需求</span><span class="sxs-lookup"><span data-stu-id="35c90-242">Requirements</span></span>



| <span data-ttu-id="35c90-243">需求</span><span class="sxs-lookup"><span data-stu-id="35c90-243">Requirement</span></span> | <span data-ttu-id="35c90-244">值</span><span class="sxs-lookup"><span data-stu-id="35c90-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="35c90-245">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35c90-245">Minimum supported client</span></span><br/> | <span data-ttu-id="35c90-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="35c90-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="35c90-247">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35c90-247">Minimum supported server</span></span><br/> | <span data-ttu-id="35c90-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="35c90-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="35c90-249">命名空間</span><span class="sxs-lookup"><span data-stu-id="35c90-249">Namespace</span></span><br/>                | <span data-ttu-id="35c90-250">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="35c90-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="35c90-251">MOF</span><span class="sxs-lookup"><span data-stu-id="35c90-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="35c90-252"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="35c90-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="35c90-253">DLL</span><span class="sxs-lookup"><span data-stu-id="35c90-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="35c90-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="35c90-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35c90-255">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35c90-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35c90-256">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="35c90-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="35c90-257">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="35c90-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="35c90-258">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="35c90-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="35c90-259">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="35c90-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="35c90-260">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="35c90-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

