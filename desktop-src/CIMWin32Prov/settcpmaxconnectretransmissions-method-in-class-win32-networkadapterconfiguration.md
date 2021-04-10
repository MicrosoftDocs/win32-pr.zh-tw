---
description: SetTcpMaxConnectRetransmissions WMI 類別靜態方法是用來設定在中止之前 TCP 將會重新傳輸連接要求的嘗試次數。
ms.assetid: cb0dfba3-4ef5-4052-94f3-f688a1c55d90
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetTcpMaxConnectRetransmissions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxConnectRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 160d84c2a466bff34070a6dec4a34804d5a3a7fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111616"
---
# <a name="settcpmaxconnectretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="32ce3-103">Win32 >networkadapterconfiguration 類別的 SetTcpMaxConnectRetransmissions 方法 \_</span><span class="sxs-lookup"><span data-stu-id="32ce3-103">SetTcpMaxConnectRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="32ce3-104">**SetTcpMaxConnectRetransmissions** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定在中止之前 TCP 將會重新傳輸連接要求的嘗試次數。</span><span class="sxs-lookup"><span data-stu-id="32ce3-104">The **SetTcpMaxConnectRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of attempts TCP will retransmit a connect request before aborting.</span></span>

<span data-ttu-id="32ce3-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="32ce3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="32ce3-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="32ce3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="32ce3-107">語法</span><span class="sxs-lookup"><span data-stu-id="32ce3-107">Syntax</span></span>


```mof
uint32 SetTcpMaxConnectRetransmissions(
  [in] uint32 TcpMaxConnectRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="32ce3-108">參數</span><span class="sxs-lookup"><span data-stu-id="32ce3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="32ce3-109">*TcpMaxConnectRetransmissions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="32ce3-109">*TcpMaxConnectRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-110">TCP 在中止之前將會重新傳輸連接要求的次數。</span><span class="sxs-lookup"><span data-stu-id="32ce3-110">Number of attempts TCP will retransmit a connect request before aborting.</span></span> <span data-ttu-id="32ce3-111">值的有效範圍為 0-0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="32ce3-111">The valid range for values is 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="32ce3-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="32ce3-112">Return value</span></span>

<span data-ttu-id="32ce3-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="32ce3-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="32ce3-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="32ce3-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="32ce3-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="32ce3-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="32ce3-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="32ce3-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-117">0</span><span class="sxs-lookup"><span data-stu-id="32ce3-117">0</span></span>

<span data-ttu-id="32ce3-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="32ce3-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="32ce3-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-120">1</span><span class="sxs-lookup"><span data-stu-id="32ce3-120">1</span></span>

<span data-ttu-id="32ce3-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="32ce3-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="32ce3-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-123">64</span><span class="sxs-lookup"><span data-stu-id="32ce3-123">64</span></span>

<span data-ttu-id="32ce3-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="32ce3-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="32ce3-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-126">65</span><span class="sxs-lookup"><span data-stu-id="32ce3-126">65</span></span>

<span data-ttu-id="32ce3-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="32ce3-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="32ce3-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-129">66</span><span class="sxs-lookup"><span data-stu-id="32ce3-129">66</span></span>

<span data-ttu-id="32ce3-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="32ce3-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="32ce3-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-132">67</span><span class="sxs-lookup"><span data-stu-id="32ce3-132">67</span></span>

<span data-ttu-id="32ce3-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="32ce3-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="32ce3-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-135">68</span><span class="sxs-lookup"><span data-stu-id="32ce3-135">68</span></span>

<span data-ttu-id="32ce3-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="32ce3-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="32ce3-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-138">69</span><span class="sxs-lookup"><span data-stu-id="32ce3-138">69</span></span>

<span data-ttu-id="32ce3-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="32ce3-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="32ce3-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-141">70</span><span class="sxs-lookup"><span data-stu-id="32ce3-141">70</span></span>

<span data-ttu-id="32ce3-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="32ce3-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="32ce3-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-144">71</span><span class="sxs-lookup"><span data-stu-id="32ce3-144">71</span></span>

<span data-ttu-id="32ce3-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="32ce3-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="32ce3-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-147">72</span><span class="sxs-lookup"><span data-stu-id="32ce3-147">72</span></span>

<span data-ttu-id="32ce3-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="32ce3-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="32ce3-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-150">73</span><span class="sxs-lookup"><span data-stu-id="32ce3-150">73</span></span>

<span data-ttu-id="32ce3-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="32ce3-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="32ce3-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-153">74</span><span class="sxs-lookup"><span data-stu-id="32ce3-153">74</span></span>

<span data-ttu-id="32ce3-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="32ce3-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="32ce3-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-156">75</span><span class="sxs-lookup"><span data-stu-id="32ce3-156">75</span></span>

<span data-ttu-id="32ce3-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="32ce3-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="32ce3-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-159">76</span><span class="sxs-lookup"><span data-stu-id="32ce3-159">76</span></span>

<span data-ttu-id="32ce3-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="32ce3-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="32ce3-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-162">77</span><span class="sxs-lookup"><span data-stu-id="32ce3-162">77</span></span>

<span data-ttu-id="32ce3-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="32ce3-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="32ce3-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-165">78</span><span class="sxs-lookup"><span data-stu-id="32ce3-165">78</span></span>

<span data-ttu-id="32ce3-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="32ce3-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="32ce3-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-168">79</span><span class="sxs-lookup"><span data-stu-id="32ce3-168">79</span></span>

<span data-ttu-id="32ce3-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="32ce3-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="32ce3-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-171">80</span><span class="sxs-lookup"><span data-stu-id="32ce3-171">80</span></span>

<span data-ttu-id="32ce3-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="32ce3-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="32ce3-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-174">81</span><span class="sxs-lookup"><span data-stu-id="32ce3-174">81</span></span>

<span data-ttu-id="32ce3-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="32ce3-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="32ce3-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-177">82</span><span class="sxs-lookup"><span data-stu-id="32ce3-177">82</span></span>

<span data-ttu-id="32ce3-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="32ce3-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="32ce3-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-180">83</span><span class="sxs-lookup"><span data-stu-id="32ce3-180">83</span></span>

<span data-ttu-id="32ce3-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="32ce3-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="32ce3-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-183">84</span><span class="sxs-lookup"><span data-stu-id="32ce3-183">84</span></span>

<span data-ttu-id="32ce3-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="32ce3-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="32ce3-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-186">85</span><span class="sxs-lookup"><span data-stu-id="32ce3-186">85</span></span>

<span data-ttu-id="32ce3-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="32ce3-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="32ce3-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-189">86</span><span class="sxs-lookup"><span data-stu-id="32ce3-189">86</span></span>

<span data-ttu-id="32ce3-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="32ce3-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="32ce3-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-192">87</span><span class="sxs-lookup"><span data-stu-id="32ce3-192">87</span></span>

<span data-ttu-id="32ce3-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="32ce3-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="32ce3-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-195">88</span><span class="sxs-lookup"><span data-stu-id="32ce3-195">88</span></span>

<span data-ttu-id="32ce3-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="32ce3-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="32ce3-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-198">89</span><span class="sxs-lookup"><span data-stu-id="32ce3-198">89</span></span>

<span data-ttu-id="32ce3-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="32ce3-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="32ce3-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-201">90</span><span class="sxs-lookup"><span data-stu-id="32ce3-201">90</span></span>

<span data-ttu-id="32ce3-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="32ce3-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="32ce3-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-204">91</span><span class="sxs-lookup"><span data-stu-id="32ce3-204">91</span></span>

<span data-ttu-id="32ce3-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="32ce3-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="32ce3-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-207">92</span><span class="sxs-lookup"><span data-stu-id="32ce3-207">92</span></span>

<span data-ttu-id="32ce3-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="32ce3-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="32ce3-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-210">93</span><span class="sxs-lookup"><span data-stu-id="32ce3-210">93</span></span>

<span data-ttu-id="32ce3-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="32ce3-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="32ce3-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-213">94</span><span class="sxs-lookup"><span data-stu-id="32ce3-213">94</span></span>

<span data-ttu-id="32ce3-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="32ce3-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="32ce3-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-216">95</span><span class="sxs-lookup"><span data-stu-id="32ce3-216">95</span></span>

<span data-ttu-id="32ce3-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="32ce3-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="32ce3-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-219">96</span><span class="sxs-lookup"><span data-stu-id="32ce3-219">96</span></span>

<span data-ttu-id="32ce3-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="32ce3-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="32ce3-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-222">97</span><span class="sxs-lookup"><span data-stu-id="32ce3-222">97</span></span>

<span data-ttu-id="32ce3-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="32ce3-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="32ce3-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-225">98</span><span class="sxs-lookup"><span data-stu-id="32ce3-225">98</span></span>

<span data-ttu-id="32ce3-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="32ce3-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="32ce3-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-228">100</span><span class="sxs-lookup"><span data-stu-id="32ce3-228">100</span></span>

<span data-ttu-id="32ce3-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="32ce3-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="32ce3-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="32ce3-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="32ce3-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="32ce3-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="32ce3-232">備註</span><span class="sxs-lookup"><span data-stu-id="32ce3-232">Remarks</span></span>

<span data-ttu-id="32ce3-233">初始重新傳輸超時為三秒鐘，每次後續嘗試都會有雙精度浮點數。</span><span class="sxs-lookup"><span data-stu-id="32ce3-233">The initial retransmission timeout is three seconds, and doubles for each successive attempt.</span></span>

## <a name="examples"></a><span data-ttu-id="32ce3-234">範例</span><span class="sxs-lookup"><span data-stu-id="32ce3-234">Examples</span></span>

<span data-ttu-id="32ce3-235">[ [修改允許的 TCP 連接重新傳輸的最大值](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) ] VBScript 範例會設定 tcp 在放棄工作之前，會重新傳輸連接嘗試的次數。</span><span class="sxs-lookup"><span data-stu-id="32ce3-235">The [Modify the Maximum Allowed TCP Connection Retransmissions](https://Gallery.TechNet.Microsoft.Com/e599c6bc-fa37-457d-b7e3-3c003517ed46) VBScript sample configures the number of times TCP will retransmit a connection attempt before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="32ce3-236">規格需求</span><span class="sxs-lookup"><span data-stu-id="32ce3-236">Requirements</span></span>



| <span data-ttu-id="32ce3-237">需求</span><span class="sxs-lookup"><span data-stu-id="32ce3-237">Requirement</span></span> | <span data-ttu-id="32ce3-238">值</span><span class="sxs-lookup"><span data-stu-id="32ce3-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="32ce3-239">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="32ce3-239">Minimum supported client</span></span><br/> | <span data-ttu-id="32ce3-240">Windows Vista、Windows Vista</span><span class="sxs-lookup"><span data-stu-id="32ce3-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="32ce3-241">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="32ce3-241">Minimum supported server</span></span><br/> | <span data-ttu-id="32ce3-242">Windows Server 2008、Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="32ce3-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="32ce3-243">命名空間</span><span class="sxs-lookup"><span data-stu-id="32ce3-243">Namespace</span></span><br/>                | <span data-ttu-id="32ce3-244">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="32ce3-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="32ce3-245">MOF</span><span class="sxs-lookup"><span data-stu-id="32ce3-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32ce3-246"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="32ce3-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="32ce3-247">DLL</span><span class="sxs-lookup"><span data-stu-id="32ce3-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32ce3-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32ce3-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32ce3-249">另請參閱</span><span class="sxs-lookup"><span data-stu-id="32ce3-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32ce3-250">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="32ce3-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="32ce3-251">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="32ce3-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="32ce3-252">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="32ce3-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="32ce3-253">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="32ce3-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="32ce3-254">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="32ce3-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

