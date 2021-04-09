---
description: SetTcpWindowSize WMI 類別靜態方法是用來設定系統提供的 TCP 接收視窗大小上限。
ms.assetid: c108fd9c-6de4-4f3e-9691-b0b5c1a3dc5f
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetTcpWindowSize 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpWindowSize
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: d4a77acdc81c06d1f78da8bbc0160bd0d21bcfd8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110737"
---
# <a name="settcpwindowsize-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="4c182-103">Win32 >networkadapterconfiguration 類別的 SetTcpWindowSize 方法 \_</span><span class="sxs-lookup"><span data-stu-id="4c182-103">SetTcpWindowSize method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="4c182-104">**SetTcpWindowSize** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定系統提供的 TCP 接收視窗大小上限。</span><span class="sxs-lookup"><span data-stu-id="4c182-104">The **SetTcpWindowSize** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the maximum TCP Receive Window size offered by the system.</span></span>

<span data-ttu-id="4c182-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="4c182-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="4c182-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="4c182-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="4c182-107">語法</span><span class="sxs-lookup"><span data-stu-id="4c182-107">Syntax</span></span>


```mof
uint32 SetTcpWindowSize(
  [in] uint16 TcpWindowSize
);
```



## <a name="parameters"></a><span data-ttu-id="4c182-108">參數</span><span class="sxs-lookup"><span data-stu-id="4c182-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4c182-109">*TcpWindowSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4c182-109">*TcpWindowSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4c182-110">系統提供的 TCP 接收視窗大小上限。</span><span class="sxs-lookup"><span data-stu-id="4c182-110">Maximum TCP receive window size offered by the system.</span></span> <span data-ttu-id="4c182-111">以位元組為單位的有效值範圍是 0-65535。</span><span class="sxs-lookup"><span data-stu-id="4c182-111">The valid range of values in bytes is 0 - 65535.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4c182-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="4c182-112">Return value</span></span>

<span data-ttu-id="4c182-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="4c182-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="4c182-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="4c182-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="4c182-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="4c182-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="4c182-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="4c182-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-117">0</span><span class="sxs-lookup"><span data-stu-id="4c182-117">0</span></span>

<span data-ttu-id="4c182-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="4c182-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="4c182-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-120">1</span><span class="sxs-lookup"><span data-stu-id="4c182-120">1</span></span>

<span data-ttu-id="4c182-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="4c182-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="4c182-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-123">64</span><span class="sxs-lookup"><span data-stu-id="4c182-123">64</span></span>

<span data-ttu-id="4c182-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="4c182-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="4c182-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-126">65</span><span class="sxs-lookup"><span data-stu-id="4c182-126">65</span></span>

<span data-ttu-id="4c182-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="4c182-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="4c182-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-129">66</span><span class="sxs-lookup"><span data-stu-id="4c182-129">66</span></span>

<span data-ttu-id="4c182-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="4c182-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="4c182-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-132">67</span><span class="sxs-lookup"><span data-stu-id="4c182-132">67</span></span>

<span data-ttu-id="4c182-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c182-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="4c182-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-135">68</span><span class="sxs-lookup"><span data-stu-id="4c182-135">68</span></span>

<span data-ttu-id="4c182-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="4c182-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="4c182-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-138">69</span><span class="sxs-lookup"><span data-stu-id="4c182-138">69</span></span>

<span data-ttu-id="4c182-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="4c182-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="4c182-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-141">70</span><span class="sxs-lookup"><span data-stu-id="4c182-141">70</span></span>

<span data-ttu-id="4c182-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="4c182-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="4c182-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-144">71</span><span class="sxs-lookup"><span data-stu-id="4c182-144">71</span></span>

<span data-ttu-id="4c182-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="4c182-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="4c182-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-147">72</span><span class="sxs-lookup"><span data-stu-id="4c182-147">72</span></span>

<span data-ttu-id="4c182-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c182-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="4c182-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-150">73</span><span class="sxs-lookup"><span data-stu-id="4c182-150">73</span></span>

<span data-ttu-id="4c182-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="4c182-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="4c182-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-153">74</span><span class="sxs-lookup"><span data-stu-id="4c182-153">74</span></span>

<span data-ttu-id="4c182-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="4c182-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="4c182-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-156">75</span><span class="sxs-lookup"><span data-stu-id="4c182-156">75</span></span>

<span data-ttu-id="4c182-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="4c182-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="4c182-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-159">76</span><span class="sxs-lookup"><span data-stu-id="4c182-159">76</span></span>

<span data-ttu-id="4c182-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="4c182-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="4c182-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-162">77</span><span class="sxs-lookup"><span data-stu-id="4c182-162">77</span></span>

<span data-ttu-id="4c182-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="4c182-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="4c182-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-165">78</span><span class="sxs-lookup"><span data-stu-id="4c182-165">78</span></span>

<span data-ttu-id="4c182-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="4c182-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="4c182-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-168">79</span><span class="sxs-lookup"><span data-stu-id="4c182-168">79</span></span>

<span data-ttu-id="4c182-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="4c182-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="4c182-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-171">80</span><span class="sxs-lookup"><span data-stu-id="4c182-171">80</span></span>

<span data-ttu-id="4c182-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="4c182-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="4c182-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-174">81</span><span class="sxs-lookup"><span data-stu-id="4c182-174">81</span></span>

<span data-ttu-id="4c182-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="4c182-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="4c182-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-177">82</span><span class="sxs-lookup"><span data-stu-id="4c182-177">82</span></span>

<span data-ttu-id="4c182-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="4c182-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="4c182-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-180">83</span><span class="sxs-lookup"><span data-stu-id="4c182-180">83</span></span>

<span data-ttu-id="4c182-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="4c182-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="4c182-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-183">84</span><span class="sxs-lookup"><span data-stu-id="4c182-183">84</span></span>

<span data-ttu-id="4c182-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="4c182-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="4c182-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-186">85</span><span class="sxs-lookup"><span data-stu-id="4c182-186">85</span></span>

<span data-ttu-id="4c182-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="4c182-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="4c182-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-189">86</span><span class="sxs-lookup"><span data-stu-id="4c182-189">86</span></span>

<span data-ttu-id="4c182-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="4c182-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="4c182-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-192">87</span><span class="sxs-lookup"><span data-stu-id="4c182-192">87</span></span>

<span data-ttu-id="4c182-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="4c182-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="4c182-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-195">88</span><span class="sxs-lookup"><span data-stu-id="4c182-195">88</span></span>

<span data-ttu-id="4c182-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="4c182-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="4c182-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-198">89</span><span class="sxs-lookup"><span data-stu-id="4c182-198">89</span></span>

<span data-ttu-id="4c182-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="4c182-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="4c182-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-201">90</span><span class="sxs-lookup"><span data-stu-id="4c182-201">90</span></span>

<span data-ttu-id="4c182-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="4c182-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="4c182-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-204">91</span><span class="sxs-lookup"><span data-stu-id="4c182-204">91</span></span>

<span data-ttu-id="4c182-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="4c182-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="4c182-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-207">92</span><span class="sxs-lookup"><span data-stu-id="4c182-207">92</span></span>

<span data-ttu-id="4c182-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="4c182-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="4c182-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-210">93</span><span class="sxs-lookup"><span data-stu-id="4c182-210">93</span></span>

<span data-ttu-id="4c182-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="4c182-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="4c182-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-213">94</span><span class="sxs-lookup"><span data-stu-id="4c182-213">94</span></span>

<span data-ttu-id="4c182-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="4c182-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="4c182-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-216">95</span><span class="sxs-lookup"><span data-stu-id="4c182-216">95</span></span>

<span data-ttu-id="4c182-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="4c182-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="4c182-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-219">96</span><span class="sxs-lookup"><span data-stu-id="4c182-219">96</span></span>

<span data-ttu-id="4c182-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="4c182-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="4c182-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-222">97</span><span class="sxs-lookup"><span data-stu-id="4c182-222">97</span></span>

<span data-ttu-id="4c182-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="4c182-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="4c182-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-225">98</span><span class="sxs-lookup"><span data-stu-id="4c182-225">98</span></span>

<span data-ttu-id="4c182-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="4c182-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="4c182-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-228">100</span><span class="sxs-lookup"><span data-stu-id="4c182-228">100</span></span>

<span data-ttu-id="4c182-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="4c182-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="4c182-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="4c182-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="4c182-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="4c182-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4c182-232">備註</span><span class="sxs-lookup"><span data-stu-id="4c182-232">Remarks</span></span>

<span data-ttu-id="4c182-233">接收視窗指定傳送者不需收到通知就可傳送的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="4c182-233">The receive window specifies the number of bytes a sender can transmit without receiving an acknowledgment.</span></span> <span data-ttu-id="4c182-234">一般而言，較大的接收視窗會透過高延遲和高頻寬的網路改善效能。</span><span class="sxs-lookup"><span data-stu-id="4c182-234">In general, larger receive windows improve performance over high-delay and high-bandwidth networks.</span></span> <span data-ttu-id="4c182-235">為了提高效率，接收視窗應該是 (MSS) 的 TCP 最大區段大小的倍數。</span><span class="sxs-lookup"><span data-stu-id="4c182-235">For efficiency, the receive window should be an even multiple of the TCP Maximum Segment Size (MSS).</span></span>

> [!Note]  
> <span data-ttu-id="4c182-236">Windows Vista：此方法會存取 `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` 登錄專案，此專案不會用於目前的作業系統執行。</span><span class="sxs-lookup"><span data-stu-id="4c182-236">Windows Vista: This method accesses the `"CurrentControlSet\\Services\\Tcpip\\Parameters|TcpWindowSize"` registry entry, which is not used in the current implementation of the operating system.</span></span>

 

## <a name="examples"></a><span data-ttu-id="4c182-237">範例</span><span class="sxs-lookup"><span data-stu-id="4c182-237">Examples</span></span>

<span data-ttu-id="4c182-238">[ [修改所有網路介面卡的 Tcp 視窗大小]](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript 範例會設定電腦上所有網路介面卡的 tcp 視窗大小。</span><span class="sxs-lookup"><span data-stu-id="4c182-238">The [Modify the TCP Window Size for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/74cf7be0-0044-4a88-85a3-9bc98490897b) VBScript sample sets the TCP window size for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="4c182-239">規格需求</span><span class="sxs-lookup"><span data-stu-id="4c182-239">Requirements</span></span>



| <span data-ttu-id="4c182-240">需求</span><span class="sxs-lookup"><span data-stu-id="4c182-240">Requirement</span></span> | <span data-ttu-id="4c182-241">值</span><span class="sxs-lookup"><span data-stu-id="4c182-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4c182-242">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4c182-242">Minimum supported client</span></span><br/> | <span data-ttu-id="4c182-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4c182-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4c182-244">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4c182-244">Minimum supported server</span></span><br/> | <span data-ttu-id="4c182-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c182-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c182-246">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4c182-246">End of client support</span></span><br/>    | <span data-ttu-id="4c182-247">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4c182-247">Windows 7</span></span><br/>                                                                    |
| <span data-ttu-id="4c182-248">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="4c182-248">End of server support</span></span><br/>    | <span data-ttu-id="4c182-249">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4c182-249">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4c182-250">命名空間</span><span class="sxs-lookup"><span data-stu-id="4c182-250">Namespace</span></span><br/>                | <span data-ttu-id="4c182-251">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="4c182-251">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4c182-252">MOF</span><span class="sxs-lookup"><span data-stu-id="4c182-252">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4c182-253"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="4c182-253"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4c182-254">DLL</span><span class="sxs-lookup"><span data-stu-id="4c182-254">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4c182-255"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4c182-255"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4c182-256">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4c182-256">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4c182-257">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="4c182-257">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="4c182-258">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="4c182-258">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="4c182-259">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="4c182-259">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="4c182-260">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="4c182-260">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="4c182-261">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="4c182-261">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

