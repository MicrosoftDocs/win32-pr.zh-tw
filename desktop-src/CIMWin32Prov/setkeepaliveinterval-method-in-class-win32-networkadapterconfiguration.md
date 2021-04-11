---
description: SetKeepAliveInterval WMI 類別靜態方法可用來設定間隔，以分隔保持運作的重新傳輸，直到收到回應為止。
ms.assetid: 83415000-124a-44a7-93cc-92ce9df143aa
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetKeepAliveInterval 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveInterval
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 2ce6a1491fd9e414f503d0165216794c67db0e97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110944"
---
# <a name="setkeepaliveinterval-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="2a525-103">Win32 >networkadapterconfiguration 類別的 SetKeepAliveInterval 方法 \_</span><span class="sxs-lookup"><span data-stu-id="2a525-103">SetKeepAliveInterval method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="2a525-104">**SetKeepAliveInterval** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法可用來設定間隔，以分隔保持運作的重新傳輸，直到收到回應為止。</span><span class="sxs-lookup"><span data-stu-id="2a525-104">The **SetKeepAliveInterval** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the interval separating Keep Alive Retransmissions until a response is received.</span></span>

<span data-ttu-id="2a525-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="2a525-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="2a525-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="2a525-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="2a525-107">語法</span><span class="sxs-lookup"><span data-stu-id="2a525-107">Syntax</span></span>


```mof
uint32 SetKeepAliveInterval(
  [in] uint32 KeepAliveInterval
);
```



## <a name="parameters"></a><span data-ttu-id="2a525-108">參數</span><span class="sxs-lookup"><span data-stu-id="2a525-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a525-109">*KeepAliveInterval* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a525-109">*KeepAliveInterval* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a525-110">以毫秒為單位的值，以毫秒為單位分隔保持運作的重新傳輸，直到收到回應為止。</span><span class="sxs-lookup"><span data-stu-id="2a525-110">Value, in milliseconds, for the interval separating Keep Alive Retransmissions until a response is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a525-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a525-111">Return value</span></span>

<span data-ttu-id="2a525-112">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="2a525-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="2a525-113">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="2a525-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="2a525-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="2a525-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="2a525-115">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="2a525-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-116">0</span><span class="sxs-lookup"><span data-stu-id="2a525-116">0</span></span>

<span data-ttu-id="2a525-117">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="2a525-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-118">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="2a525-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-119">1</span><span class="sxs-lookup"><span data-stu-id="2a525-119">1</span></span>

<span data-ttu-id="2a525-120">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="2a525-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-121">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="2a525-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-122">64</span><span class="sxs-lookup"><span data-stu-id="2a525-122">64</span></span>

<span data-ttu-id="2a525-123">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="2a525-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-124">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="2a525-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-125">65</span><span class="sxs-lookup"><span data-stu-id="2a525-125">65</span></span>

<span data-ttu-id="2a525-126">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="2a525-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-127">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="2a525-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-128">66</span><span class="sxs-lookup"><span data-stu-id="2a525-128">66</span></span>

<span data-ttu-id="2a525-129">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="2a525-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-130">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="2a525-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-131">67</span><span class="sxs-lookup"><span data-stu-id="2a525-131">67</span></span>

<span data-ttu-id="2a525-132">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="2a525-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-133">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="2a525-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-134">68</span><span class="sxs-lookup"><span data-stu-id="2a525-134">68</span></span>

<span data-ttu-id="2a525-135">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="2a525-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-136">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="2a525-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-137">69</span><span class="sxs-lookup"><span data-stu-id="2a525-137">69</span></span>

<span data-ttu-id="2a525-138">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="2a525-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-139">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="2a525-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-140">70</span><span class="sxs-lookup"><span data-stu-id="2a525-140">70</span></span>

<span data-ttu-id="2a525-141">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="2a525-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-142">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="2a525-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-143">71</span><span class="sxs-lookup"><span data-stu-id="2a525-143">71</span></span>

<span data-ttu-id="2a525-144">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="2a525-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-145">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="2a525-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-146">72</span><span class="sxs-lookup"><span data-stu-id="2a525-146">72</span></span>

<span data-ttu-id="2a525-147">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="2a525-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-148">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="2a525-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-149">73</span><span class="sxs-lookup"><span data-stu-id="2a525-149">73</span></span>

<span data-ttu-id="2a525-150">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="2a525-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-151">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="2a525-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-152">74</span><span class="sxs-lookup"><span data-stu-id="2a525-152">74</span></span>

<span data-ttu-id="2a525-153">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="2a525-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-154">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="2a525-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-155">75</span><span class="sxs-lookup"><span data-stu-id="2a525-155">75</span></span>

<span data-ttu-id="2a525-156">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="2a525-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-157">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="2a525-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-158">76</span><span class="sxs-lookup"><span data-stu-id="2a525-158">76</span></span>

<span data-ttu-id="2a525-159">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="2a525-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-160">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="2a525-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-161">77</span><span class="sxs-lookup"><span data-stu-id="2a525-161">77</span></span>

<span data-ttu-id="2a525-162">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="2a525-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-163">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="2a525-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-164">78</span><span class="sxs-lookup"><span data-stu-id="2a525-164">78</span></span>

<span data-ttu-id="2a525-165">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="2a525-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-166">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="2a525-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-167">79</span><span class="sxs-lookup"><span data-stu-id="2a525-167">79</span></span>

<span data-ttu-id="2a525-168">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="2a525-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-169">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="2a525-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-170">80</span><span class="sxs-lookup"><span data-stu-id="2a525-170">80</span></span>

<span data-ttu-id="2a525-171">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="2a525-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-172">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="2a525-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-173">81</span><span class="sxs-lookup"><span data-stu-id="2a525-173">81</span></span>

<span data-ttu-id="2a525-174">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="2a525-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-175">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="2a525-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-176">82</span><span class="sxs-lookup"><span data-stu-id="2a525-176">82</span></span>

<span data-ttu-id="2a525-177">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="2a525-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-178">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="2a525-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-179">83</span><span class="sxs-lookup"><span data-stu-id="2a525-179">83</span></span>

<span data-ttu-id="2a525-180">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="2a525-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-181">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="2a525-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-182">84</span><span class="sxs-lookup"><span data-stu-id="2a525-182">84</span></span>

<span data-ttu-id="2a525-183">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="2a525-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-184">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="2a525-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-185">85</span><span class="sxs-lookup"><span data-stu-id="2a525-185">85</span></span>

<span data-ttu-id="2a525-186">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="2a525-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-187">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="2a525-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-188">86</span><span class="sxs-lookup"><span data-stu-id="2a525-188">86</span></span>

<span data-ttu-id="2a525-189">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="2a525-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-190">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="2a525-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-191">87</span><span class="sxs-lookup"><span data-stu-id="2a525-191">87</span></span>

<span data-ttu-id="2a525-192">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="2a525-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-193">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="2a525-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-194">88</span><span class="sxs-lookup"><span data-stu-id="2a525-194">88</span></span>

<span data-ttu-id="2a525-195">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="2a525-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-196">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="2a525-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-197">89</span><span class="sxs-lookup"><span data-stu-id="2a525-197">89</span></span>

<span data-ttu-id="2a525-198">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="2a525-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-199">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="2a525-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-200">90</span><span class="sxs-lookup"><span data-stu-id="2a525-200">90</span></span>

<span data-ttu-id="2a525-201">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="2a525-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-202">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="2a525-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-203">91</span><span class="sxs-lookup"><span data-stu-id="2a525-203">91</span></span>

<span data-ttu-id="2a525-204">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="2a525-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-205">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="2a525-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-206">92</span><span class="sxs-lookup"><span data-stu-id="2a525-206">92</span></span>

<span data-ttu-id="2a525-207">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="2a525-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-208">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="2a525-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-209">93</span><span class="sxs-lookup"><span data-stu-id="2a525-209">93</span></span>

<span data-ttu-id="2a525-210">已經存在。</span><span class="sxs-lookup"><span data-stu-id="2a525-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-211">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="2a525-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-212">94</span><span class="sxs-lookup"><span data-stu-id="2a525-212">94</span></span>

<span data-ttu-id="2a525-213">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="2a525-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-214">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="2a525-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-215">95</span><span class="sxs-lookup"><span data-stu-id="2a525-215">95</span></span>

<span data-ttu-id="2a525-216">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="2a525-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-217">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="2a525-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-218">96</span><span class="sxs-lookup"><span data-stu-id="2a525-218">96</span></span>

<span data-ttu-id="2a525-219">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="2a525-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-220">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="2a525-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-221">97</span><span class="sxs-lookup"><span data-stu-id="2a525-221">97</span></span>

<span data-ttu-id="2a525-222">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="2a525-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-223">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="2a525-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-224">98</span><span class="sxs-lookup"><span data-stu-id="2a525-224">98</span></span>

<span data-ttu-id="2a525-225">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="2a525-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-226">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="2a525-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-227">100</span><span class="sxs-lookup"><span data-stu-id="2a525-227">100</span></span>

<span data-ttu-id="2a525-228">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="2a525-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="2a525-229">**其他**</span><span class="sxs-lookup"><span data-stu-id="2a525-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="2a525-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="2a525-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2a525-231">備註</span><span class="sxs-lookup"><span data-stu-id="2a525-231">Remarks</span></span>

<span data-ttu-id="2a525-232">收到回應之後，會延遲到下一個保持運作的傳輸，再由 [**KeepAliveTime**](win32-networkadapterconfiguration.md) 屬性的值來控制。</span><span class="sxs-lookup"><span data-stu-id="2a525-232">After a response is received, the delay until the next Keep Alive Transmission is again controlled by the value of the [**KeepAliveTime**](win32-networkadapterconfiguration.md) property.</span></span> <span data-ttu-id="2a525-233">在 **TcpMaxDataRetransmissions** 屬性所指定的重新傳輸數目未接聽之後，連接會終止</span><span class="sxs-lookup"><span data-stu-id="2a525-233">The connection is terminated after the number of retransmissions specified by the **TcpMaxDataRetransmissions** property have gone unanswered</span></span>

## <a name="examples"></a><span data-ttu-id="2a525-234">範例</span><span class="sxs-lookup"><span data-stu-id="2a525-234">Examples</span></span>

<span data-ttu-id="2a525-235">[ [修改所有網路介面卡的保持運作間隔](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) ] VBScript 範例會將電腦上所有網路介面卡的保持運作間隔設定為300、00毫秒 (5 分鐘的) 。</span><span class="sxs-lookup"><span data-stu-id="2a525-235">The [Modify the Keep Alive Interval for all Network Adapters](https://Gallery.TechNet.Microsoft.Com/f6d4a0e7-5b59-42e3-888d-82a028e2bf35) VBScript sample configures the keep alive interval for all network adapters on a computer to 300,00 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a525-236">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a525-236">Requirements</span></span>



| <span data-ttu-id="2a525-237">需求</span><span class="sxs-lookup"><span data-stu-id="2a525-237">Requirement</span></span> | <span data-ttu-id="2a525-238">值</span><span class="sxs-lookup"><span data-stu-id="2a525-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2a525-239">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2a525-239">Minimum supported client</span></span><br/> | <span data-ttu-id="2a525-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2a525-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2a525-241">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2a525-241">Minimum supported server</span></span><br/> | <span data-ttu-id="2a525-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2a525-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2a525-243">命名空間</span><span class="sxs-lookup"><span data-stu-id="2a525-243">Namespace</span></span><br/>                | <span data-ttu-id="2a525-244">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="2a525-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2a525-245">MOF</span><span class="sxs-lookup"><span data-stu-id="2a525-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a525-246"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="2a525-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a525-247">DLL</span><span class="sxs-lookup"><span data-stu-id="2a525-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a525-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2a525-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a525-249">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a525-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a525-250">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="2a525-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="2a525-251">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="2a525-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="2a525-252">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="2a525-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="2a525-253">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="2a525-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="2a525-254">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="2a525-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

