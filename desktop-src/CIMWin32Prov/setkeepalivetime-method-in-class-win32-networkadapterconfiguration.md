---
description: SetKeepAliveTime WMI 類別靜態方法是用來設定 TCP 嘗試驗證閒置連線是否仍可供使用的頻率，方法是傳送 Keep-alive 封包。
ms.assetid: 8640b109-928b-46fc-8dce-9ee5dcbd94e3
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetKeepAliveTime 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetKeepAliveTime
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 1dc2674f3c09626749b4c7ac6151349401670e27
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972777"
---
# <a name="setkeepalivetime-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="3bd73-103">Win32 >networkadapterconfiguration 類別的 SetKeepAliveTime 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3bd73-103">SetKeepAliveTime method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="3bd73-104">**SetKeepAliveTime** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定 TCP 嘗試驗證閒置連線是否仍可供使用的頻率，方法是傳送 keep-alive 封包。</span><span class="sxs-lookup"><span data-stu-id="3bd73-104">The **SetKeepAliveTime** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set how often TCP attempts to verify that an idle connection is still available by sending a Keep Alive packet.</span></span>

<span data-ttu-id="3bd73-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="3bd73-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3bd73-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="3bd73-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3bd73-107">語法</span><span class="sxs-lookup"><span data-stu-id="3bd73-107">Syntax</span></span>


```mof
uint32 SetKeepAliveTime(
  [in] uint32 KeepAliveTime
);
```



## <a name="parameters"></a><span data-ttu-id="3bd73-108">參數</span><span class="sxs-lookup"><span data-stu-id="3bd73-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3bd73-109">*KeepAliveTime* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3bd73-109">*KeepAliveTime* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-110">TCP 等待檢查閒置連接是否仍然可用的間隔（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="3bd73-110">Interval, in milliseconds, the TCP waits to check that an idle connection is still available.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3bd73-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3bd73-111">Return value</span></span>

<span data-ttu-id="3bd73-112">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="3bd73-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="3bd73-113">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="3bd73-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3bd73-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="3bd73-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3bd73-115">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="3bd73-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-116">0</span><span class="sxs-lookup"><span data-stu-id="3bd73-116">0</span></span>

<span data-ttu-id="3bd73-117">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="3bd73-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-118">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="3bd73-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-119">1</span><span class="sxs-lookup"><span data-stu-id="3bd73-119">1</span></span>

<span data-ttu-id="3bd73-120">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="3bd73-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-121">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="3bd73-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-122">64</span><span class="sxs-lookup"><span data-stu-id="3bd73-122">64</span></span>

<span data-ttu-id="3bd73-123">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="3bd73-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-124">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="3bd73-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-125">65</span><span class="sxs-lookup"><span data-stu-id="3bd73-125">65</span></span>

<span data-ttu-id="3bd73-126">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="3bd73-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-127">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="3bd73-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-128">66</span><span class="sxs-lookup"><span data-stu-id="3bd73-128">66</span></span>

<span data-ttu-id="3bd73-129">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="3bd73-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-130">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="3bd73-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-131">67</span><span class="sxs-lookup"><span data-stu-id="3bd73-131">67</span></span>

<span data-ttu-id="3bd73-132">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3bd73-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-133">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="3bd73-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-134">68</span><span class="sxs-lookup"><span data-stu-id="3bd73-134">68</span></span>

<span data-ttu-id="3bd73-135">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="3bd73-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-136">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="3bd73-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-137">69</span><span class="sxs-lookup"><span data-stu-id="3bd73-137">69</span></span>

<span data-ttu-id="3bd73-138">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="3bd73-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-139">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="3bd73-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-140">70</span><span class="sxs-lookup"><span data-stu-id="3bd73-140">70</span></span>

<span data-ttu-id="3bd73-141">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="3bd73-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-142">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="3bd73-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-143">71</span><span class="sxs-lookup"><span data-stu-id="3bd73-143">71</span></span>

<span data-ttu-id="3bd73-144">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="3bd73-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-145">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="3bd73-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-146">72</span><span class="sxs-lookup"><span data-stu-id="3bd73-146">72</span></span>

<span data-ttu-id="3bd73-147">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3bd73-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-148">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="3bd73-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-149">73</span><span class="sxs-lookup"><span data-stu-id="3bd73-149">73</span></span>

<span data-ttu-id="3bd73-150">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="3bd73-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-151">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="3bd73-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-152">74</span><span class="sxs-lookup"><span data-stu-id="3bd73-152">74</span></span>

<span data-ttu-id="3bd73-153">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="3bd73-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-154">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="3bd73-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-155">75</span><span class="sxs-lookup"><span data-stu-id="3bd73-155">75</span></span>

<span data-ttu-id="3bd73-156">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3bd73-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-157">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="3bd73-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-158">76</span><span class="sxs-lookup"><span data-stu-id="3bd73-158">76</span></span>

<span data-ttu-id="3bd73-159">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="3bd73-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-160">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="3bd73-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-161">77</span><span class="sxs-lookup"><span data-stu-id="3bd73-161">77</span></span>

<span data-ttu-id="3bd73-162">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="3bd73-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-163">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="3bd73-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-164">78</span><span class="sxs-lookup"><span data-stu-id="3bd73-164">78</span></span>

<span data-ttu-id="3bd73-165">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="3bd73-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-166">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="3bd73-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-167">79</span><span class="sxs-lookup"><span data-stu-id="3bd73-167">79</span></span>

<span data-ttu-id="3bd73-168">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="3bd73-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-169">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="3bd73-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-170">80</span><span class="sxs-lookup"><span data-stu-id="3bd73-170">80</span></span>

<span data-ttu-id="3bd73-171">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="3bd73-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-172">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="3bd73-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-173">81</span><span class="sxs-lookup"><span data-stu-id="3bd73-173">81</span></span>

<span data-ttu-id="3bd73-174">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="3bd73-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-175">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="3bd73-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-176">82</span><span class="sxs-lookup"><span data-stu-id="3bd73-176">82</span></span>

<span data-ttu-id="3bd73-177">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="3bd73-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-178">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="3bd73-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-179">83</span><span class="sxs-lookup"><span data-stu-id="3bd73-179">83</span></span>

<span data-ttu-id="3bd73-180">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="3bd73-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-181">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="3bd73-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-182">84</span><span class="sxs-lookup"><span data-stu-id="3bd73-182">84</span></span>

<span data-ttu-id="3bd73-183">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="3bd73-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-184">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="3bd73-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-185">85</span><span class="sxs-lookup"><span data-stu-id="3bd73-185">85</span></span>

<span data-ttu-id="3bd73-186">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="3bd73-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-187">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="3bd73-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-188">86</span><span class="sxs-lookup"><span data-stu-id="3bd73-188">86</span></span>

<span data-ttu-id="3bd73-189">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="3bd73-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-190">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="3bd73-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-191">87</span><span class="sxs-lookup"><span data-stu-id="3bd73-191">87</span></span>

<span data-ttu-id="3bd73-192">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="3bd73-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-193">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="3bd73-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-194">88</span><span class="sxs-lookup"><span data-stu-id="3bd73-194">88</span></span>

<span data-ttu-id="3bd73-195">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="3bd73-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-196">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="3bd73-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-197">89</span><span class="sxs-lookup"><span data-stu-id="3bd73-197">89</span></span>

<span data-ttu-id="3bd73-198">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="3bd73-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-199">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="3bd73-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-200">90</span><span class="sxs-lookup"><span data-stu-id="3bd73-200">90</span></span>

<span data-ttu-id="3bd73-201">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="3bd73-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-202">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="3bd73-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-203">91</span><span class="sxs-lookup"><span data-stu-id="3bd73-203">91</span></span>

<span data-ttu-id="3bd73-204">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="3bd73-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-205">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="3bd73-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-206">92</span><span class="sxs-lookup"><span data-stu-id="3bd73-206">92</span></span>

<span data-ttu-id="3bd73-207">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="3bd73-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-208">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="3bd73-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-209">93</span><span class="sxs-lookup"><span data-stu-id="3bd73-209">93</span></span>

<span data-ttu-id="3bd73-210">已經存在。</span><span class="sxs-lookup"><span data-stu-id="3bd73-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-211">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="3bd73-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-212">94</span><span class="sxs-lookup"><span data-stu-id="3bd73-212">94</span></span>

<span data-ttu-id="3bd73-213">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="3bd73-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-214">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="3bd73-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-215">95</span><span class="sxs-lookup"><span data-stu-id="3bd73-215">95</span></span>

<span data-ttu-id="3bd73-216">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="3bd73-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-217">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="3bd73-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-218">96</span><span class="sxs-lookup"><span data-stu-id="3bd73-218">96</span></span>

<span data-ttu-id="3bd73-219">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="3bd73-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-220">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="3bd73-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-221">97</span><span class="sxs-lookup"><span data-stu-id="3bd73-221">97</span></span>

<span data-ttu-id="3bd73-222">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="3bd73-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-223">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="3bd73-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-224">98</span><span class="sxs-lookup"><span data-stu-id="3bd73-224">98</span></span>

<span data-ttu-id="3bd73-225">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="3bd73-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-226">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="3bd73-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-227">100</span><span class="sxs-lookup"><span data-stu-id="3bd73-227">100</span></span>

<span data-ttu-id="3bd73-228">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="3bd73-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3bd73-229">**其他**</span><span class="sxs-lookup"><span data-stu-id="3bd73-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3bd73-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="3bd73-230">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3bd73-231">備註</span><span class="sxs-lookup"><span data-stu-id="3bd73-231">Remarks</span></span>

<span data-ttu-id="3bd73-232">如果遠端系統仍然可連線且正常運作，它會確認「保持運作傳輸」。</span><span class="sxs-lookup"><span data-stu-id="3bd73-232">If the remote system is still reachable and functioning, it will acknowledge the Keep Alive transmission.</span></span> <span data-ttu-id="3bd73-233">預設不會傳送存活的封包。</span><span class="sxs-lookup"><span data-stu-id="3bd73-233">Keep Alive packets are not sent by default.</span></span> <span data-ttu-id="3bd73-234">這項功能可以在應用程式的連接中啟用。</span><span class="sxs-lookup"><span data-stu-id="3bd73-234">This feature may be enabled in a connection by an application.</span></span>

## <a name="examples"></a><span data-ttu-id="3bd73-235">範例</span><span class="sxs-lookup"><span data-stu-id="3bd73-235">Examples</span></span>

<span data-ttu-id="3bd73-236">[ [修改所有網路介面卡的即時存留時間](https://Gallery.TechNet.Microsoft.Com/35c1b0ac-285d-4baa-be6e-d3fb0b461676) ] VBScript 範例會將電腦上所有網路介面卡的存留時間設定為300000毫秒 (5 分鐘) 。</span><span class="sxs-lookup"><span data-stu-id="3bd73-236">The [Modify Keep Alive Time for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/35c1b0ac-285d-4baa-be6e-d3fb0b461676) VBScript sample configures the keep alive time for all network adapters on a computer to 300,000 milliseconds (5 minutes).</span></span>

## <a name="requirements"></a><span data-ttu-id="3bd73-237">規格需求</span><span class="sxs-lookup"><span data-stu-id="3bd73-237">Requirements</span></span>



| <span data-ttu-id="3bd73-238">需求</span><span class="sxs-lookup"><span data-stu-id="3bd73-238">Requirement</span></span> | <span data-ttu-id="3bd73-239">值</span><span class="sxs-lookup"><span data-stu-id="3bd73-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3bd73-240">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3bd73-240">Minimum supported client</span></span><br/> | <span data-ttu-id="3bd73-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3bd73-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3bd73-242">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3bd73-242">Minimum supported server</span></span><br/> | <span data-ttu-id="3bd73-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3bd73-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3bd73-244">命名空間</span><span class="sxs-lookup"><span data-stu-id="3bd73-244">Namespace</span></span><br/>                | <span data-ttu-id="3bd73-245">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3bd73-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3bd73-246">MOF</span><span class="sxs-lookup"><span data-stu-id="3bd73-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3bd73-247"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3bd73-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3bd73-248">DLL</span><span class="sxs-lookup"><span data-stu-id="3bd73-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3bd73-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3bd73-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3bd73-250">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3bd73-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3bd73-251">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="3bd73-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3bd73-252">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="3bd73-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="3bd73-253">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="3bd73-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="3bd73-254">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="3bd73-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="3bd73-255">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="3bd73-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

