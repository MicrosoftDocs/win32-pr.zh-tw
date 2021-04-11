---
description: SetTcpNumConnections WMI 類別靜態方法是用來設定 TCP 可能同時開啟的最大連接數目。
ms.assetid: 50458161-1f28-47f9-b395-09586e859d5d
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetTcpNumConnections 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpNumConnections
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5708c7ce80930c0924b560cc7b84e5af45ad7962
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110741"
---
# <a name="settcpnumconnections-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d535d-103">Win32 >networkadapterconfiguration 類別的 SetTcpNumConnections 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d535d-103">SetTcpNumConnections method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d535d-104">**SetTcpNumConnections** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定 TCP 可能同時開啟的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="d535d-104">The **SetTcpNumConnections** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum number of connections that TCP may have open simultaneously.</span></span>

<span data-ttu-id="d535d-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="d535d-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d535d-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="d535d-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d535d-107">語法</span><span class="sxs-lookup"><span data-stu-id="d535d-107">Syntax</span></span>


```mof
uint32 SetTcpNumConnections(
  [in] uint32 TcpNumConnections
);
```



## <a name="parameters"></a><span data-ttu-id="d535d-108">參數</span><span class="sxs-lookup"><span data-stu-id="d535d-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d535d-109">*TcpNumConnections* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d535d-109">*TcpNumConnections* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d535d-110">TCP 可能同時開啟的最大連接數目。</span><span class="sxs-lookup"><span data-stu-id="d535d-110">Maximum number of connections that TCP may have open simultaneously.</span></span> <span data-ttu-id="d535d-111">值的有效範圍為 0-0xFFFFFE。</span><span class="sxs-lookup"><span data-stu-id="d535d-111">The valid range of values is 0 - 0xFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d535d-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d535d-112">Return value</span></span>

<span data-ttu-id="d535d-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="d535d-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="d535d-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="d535d-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d535d-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="d535d-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d535d-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="d535d-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-117">0</span><span class="sxs-lookup"><span data-stu-id="d535d-117">0</span></span>

<span data-ttu-id="d535d-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="d535d-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="d535d-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-120">1</span><span class="sxs-lookup"><span data-stu-id="d535d-120">1</span></span>

<span data-ttu-id="d535d-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="d535d-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="d535d-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-123">64</span><span class="sxs-lookup"><span data-stu-id="d535d-123">64</span></span>

<span data-ttu-id="d535d-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="d535d-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="d535d-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-126">65</span><span class="sxs-lookup"><span data-stu-id="d535d-126">65</span></span>

<span data-ttu-id="d535d-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="d535d-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="d535d-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-129">66</span><span class="sxs-lookup"><span data-stu-id="d535d-129">66</span></span>

<span data-ttu-id="d535d-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="d535d-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d535d-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-132">67</span><span class="sxs-lookup"><span data-stu-id="d535d-132">67</span></span>

<span data-ttu-id="d535d-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="d535d-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="d535d-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-135">68</span><span class="sxs-lookup"><span data-stu-id="d535d-135">68</span></span>

<span data-ttu-id="d535d-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="d535d-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="d535d-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-138">69</span><span class="sxs-lookup"><span data-stu-id="d535d-138">69</span></span>

<span data-ttu-id="d535d-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="d535d-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="d535d-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-141">70</span><span class="sxs-lookup"><span data-stu-id="d535d-141">70</span></span>

<span data-ttu-id="d535d-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="d535d-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="d535d-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-144">71</span><span class="sxs-lookup"><span data-stu-id="d535d-144">71</span></span>

<span data-ttu-id="d535d-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="d535d-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d535d-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-147">72</span><span class="sxs-lookup"><span data-stu-id="d535d-147">72</span></span>

<span data-ttu-id="d535d-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="d535d-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="d535d-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-150">73</span><span class="sxs-lookup"><span data-stu-id="d535d-150">73</span></span>

<span data-ttu-id="d535d-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="d535d-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="d535d-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-153">74</span><span class="sxs-lookup"><span data-stu-id="d535d-153">74</span></span>

<span data-ttu-id="d535d-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="d535d-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="d535d-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-156">75</span><span class="sxs-lookup"><span data-stu-id="d535d-156">75</span></span>

<span data-ttu-id="d535d-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="d535d-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="d535d-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-159">76</span><span class="sxs-lookup"><span data-stu-id="d535d-159">76</span></span>

<span data-ttu-id="d535d-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="d535d-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="d535d-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-162">77</span><span class="sxs-lookup"><span data-stu-id="d535d-162">77</span></span>

<span data-ttu-id="d535d-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="d535d-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="d535d-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-165">78</span><span class="sxs-lookup"><span data-stu-id="d535d-165">78</span></span>

<span data-ttu-id="d535d-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="d535d-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="d535d-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-168">79</span><span class="sxs-lookup"><span data-stu-id="d535d-168">79</span></span>

<span data-ttu-id="d535d-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="d535d-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="d535d-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-171">80</span><span class="sxs-lookup"><span data-stu-id="d535d-171">80</span></span>

<span data-ttu-id="d535d-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="d535d-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="d535d-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-174">81</span><span class="sxs-lookup"><span data-stu-id="d535d-174">81</span></span>

<span data-ttu-id="d535d-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="d535d-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="d535d-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-177">82</span><span class="sxs-lookup"><span data-stu-id="d535d-177">82</span></span>

<span data-ttu-id="d535d-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="d535d-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="d535d-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-180">83</span><span class="sxs-lookup"><span data-stu-id="d535d-180">83</span></span>

<span data-ttu-id="d535d-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="d535d-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="d535d-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-183">84</span><span class="sxs-lookup"><span data-stu-id="d535d-183">84</span></span>

<span data-ttu-id="d535d-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="d535d-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="d535d-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-186">85</span><span class="sxs-lookup"><span data-stu-id="d535d-186">85</span></span>

<span data-ttu-id="d535d-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="d535d-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="d535d-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-189">86</span><span class="sxs-lookup"><span data-stu-id="d535d-189">86</span></span>

<span data-ttu-id="d535d-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="d535d-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="d535d-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-192">87</span><span class="sxs-lookup"><span data-stu-id="d535d-192">87</span></span>

<span data-ttu-id="d535d-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="d535d-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="d535d-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-195">88</span><span class="sxs-lookup"><span data-stu-id="d535d-195">88</span></span>

<span data-ttu-id="d535d-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="d535d-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="d535d-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-198">89</span><span class="sxs-lookup"><span data-stu-id="d535d-198">89</span></span>

<span data-ttu-id="d535d-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="d535d-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="d535d-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-201">90</span><span class="sxs-lookup"><span data-stu-id="d535d-201">90</span></span>

<span data-ttu-id="d535d-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="d535d-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="d535d-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-204">91</span><span class="sxs-lookup"><span data-stu-id="d535d-204">91</span></span>

<span data-ttu-id="d535d-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="d535d-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="d535d-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-207">92</span><span class="sxs-lookup"><span data-stu-id="d535d-207">92</span></span>

<span data-ttu-id="d535d-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="d535d-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="d535d-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-210">93</span><span class="sxs-lookup"><span data-stu-id="d535d-210">93</span></span>

<span data-ttu-id="d535d-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="d535d-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="d535d-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-213">94</span><span class="sxs-lookup"><span data-stu-id="d535d-213">94</span></span>

<span data-ttu-id="d535d-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="d535d-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="d535d-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-216">95</span><span class="sxs-lookup"><span data-stu-id="d535d-216">95</span></span>

<span data-ttu-id="d535d-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="d535d-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="d535d-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-219">96</span><span class="sxs-lookup"><span data-stu-id="d535d-219">96</span></span>

<span data-ttu-id="d535d-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="d535d-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="d535d-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-222">97</span><span class="sxs-lookup"><span data-stu-id="d535d-222">97</span></span>

<span data-ttu-id="d535d-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="d535d-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="d535d-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-225">98</span><span class="sxs-lookup"><span data-stu-id="d535d-225">98</span></span>

<span data-ttu-id="d535d-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="d535d-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="d535d-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-228">100</span><span class="sxs-lookup"><span data-stu-id="d535d-228">100</span></span>

<span data-ttu-id="d535d-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="d535d-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d535d-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="d535d-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d535d-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d535d-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="d535d-232">範例</span><span class="sxs-lookup"><span data-stu-id="d535d-232">Examples</span></span>

<span data-ttu-id="d535d-233">[ [修改允許的 TCP 連線數目](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) ] VBScript 範例會將電腦上同時開啟的 tcp 連線數目上限設為10。</span><span class="sxs-lookup"><span data-stu-id="d535d-233">The [Modify the Allowed Number of TCP Connections](https://Gallery.TechNet.Microsoft.Com/016d09f3-28aa-47eb-b439-100b89999bab) VBScript sample sets the maximum allowed number of simultaneously-opened TCP connections on a computer to 10.</span></span>

## <a name="requirements"></a><span data-ttu-id="d535d-234">規格需求</span><span class="sxs-lookup"><span data-stu-id="d535d-234">Requirements</span></span>



| <span data-ttu-id="d535d-235">需求</span><span class="sxs-lookup"><span data-stu-id="d535d-235">Requirement</span></span> | <span data-ttu-id="d535d-236">值</span><span class="sxs-lookup"><span data-stu-id="d535d-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d535d-237">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d535d-237">Minimum supported client</span></span><br/> | <span data-ttu-id="d535d-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d535d-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d535d-239">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d535d-239">Minimum supported server</span></span><br/> | <span data-ttu-id="d535d-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d535d-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d535d-241">命名空間</span><span class="sxs-lookup"><span data-stu-id="d535d-241">Namespace</span></span><br/>                | <span data-ttu-id="d535d-242">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d535d-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d535d-243">MOF</span><span class="sxs-lookup"><span data-stu-id="d535d-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d535d-244"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d535d-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d535d-245">DLL</span><span class="sxs-lookup"><span data-stu-id="d535d-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d535d-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d535d-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d535d-247">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d535d-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d535d-248">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="d535d-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d535d-249">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="d535d-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d535d-250">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="d535d-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d535d-251">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="d535d-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d535d-252">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="d535d-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

