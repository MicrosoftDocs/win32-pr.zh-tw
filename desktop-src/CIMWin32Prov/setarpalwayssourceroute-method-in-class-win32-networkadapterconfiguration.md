---
description: SetArpAlwaysSourceRoute WMI 類別靜態方法是用來設定依 TCP/IP 的 ARP 查詢傳輸。
ms.assetid: bbff4e2e-aea6-400e-8bd8-f62aaa9fa601
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetArpAlwaysSourceRoute 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetArpAlwaysSourceRoute
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7151fbbd13d3ac6fdf4ac3b129cdcb438abe73a9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110357"
---
# <a name="setarpalwayssourceroute-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f3dbd-103">Win32 >networkadapterconfiguration 類別的 SetArpAlwaysSourceRoute 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f3dbd-103">SetArpAlwaysSourceRoute method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f3dbd-104">**SetArpAlwaysSourceRoute** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定依 tcp/ip 的 ARP 查詢傳輸。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-104">The **SetArpAlwaysSourceRoute** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the transmission of ARP queries by TCP/IP.</span></span>

<span data-ttu-id="f3dbd-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="f3dbd-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="f3dbd-107">語法</span><span class="sxs-lookup"><span data-stu-id="f3dbd-107">Syntax</span></span>


```mof
uint32 SetArpAlwaysSourceRoute(
  [in] boolean ArpAlwaysSourceRoute
);
```



## <a name="parameters"></a><span data-ttu-id="f3dbd-108">參數</span><span class="sxs-lookup"><span data-stu-id="f3dbd-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3dbd-109">*ArpAlwaysSourceRoute* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f3dbd-109">*ArpAlwaysSourceRoute* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-110">若 **為 true**，則會強制 tcp/ip 傳輸在權杖環狀網路上啟用來源路由的 ARP 查詢。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-110">If **true**, TCP/IP is forced to transmit ARP queries with source routing enabled on Token Ring networks.</span></span> <span data-ttu-id="f3dbd-111">根據預設，堆疊會先傳送不含來源路由的 ARP 查詢，然後在未收到回復時，以啟用來源路由的方式重試。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-111">By default, the stack transmits ARP queries without source routing first, then retries with source routing enabled if no reply is received.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3dbd-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3dbd-112">Return value</span></span>

<span data-ttu-id="f3dbd-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="f3dbd-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="f3dbd-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="f3dbd-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-117">0</span><span class="sxs-lookup"><span data-stu-id="f3dbd-117">0</span></span>

<span data-ttu-id="f3dbd-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-120">1</span><span class="sxs-lookup"><span data-stu-id="f3dbd-120">1</span></span>

<span data-ttu-id="f3dbd-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-123">64</span><span class="sxs-lookup"><span data-stu-id="f3dbd-123">64</span></span>

<span data-ttu-id="f3dbd-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-126">65</span><span class="sxs-lookup"><span data-stu-id="f3dbd-126">65</span></span>

<span data-ttu-id="f3dbd-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-129">66</span><span class="sxs-lookup"><span data-stu-id="f3dbd-129">66</span></span>

<span data-ttu-id="f3dbd-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-132">67</span><span class="sxs-lookup"><span data-stu-id="f3dbd-132">67</span></span>

<span data-ttu-id="f3dbd-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-135">68</span><span class="sxs-lookup"><span data-stu-id="f3dbd-135">68</span></span>

<span data-ttu-id="f3dbd-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-138">69</span><span class="sxs-lookup"><span data-stu-id="f3dbd-138">69</span></span>

<span data-ttu-id="f3dbd-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-141">70</span><span class="sxs-lookup"><span data-stu-id="f3dbd-141">70</span></span>

<span data-ttu-id="f3dbd-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-144">71</span><span class="sxs-lookup"><span data-stu-id="f3dbd-144">71</span></span>

<span data-ttu-id="f3dbd-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-147">72</span><span class="sxs-lookup"><span data-stu-id="f3dbd-147">72</span></span>

<span data-ttu-id="f3dbd-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-150">73</span><span class="sxs-lookup"><span data-stu-id="f3dbd-150">73</span></span>

<span data-ttu-id="f3dbd-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-153">74</span><span class="sxs-lookup"><span data-stu-id="f3dbd-153">74</span></span>

<span data-ttu-id="f3dbd-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-156">75</span><span class="sxs-lookup"><span data-stu-id="f3dbd-156">75</span></span>

<span data-ttu-id="f3dbd-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-159">76</span><span class="sxs-lookup"><span data-stu-id="f3dbd-159">76</span></span>

<span data-ttu-id="f3dbd-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-162">77</span><span class="sxs-lookup"><span data-stu-id="f3dbd-162">77</span></span>

<span data-ttu-id="f3dbd-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-165">78</span><span class="sxs-lookup"><span data-stu-id="f3dbd-165">78</span></span>

<span data-ttu-id="f3dbd-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-168">79</span><span class="sxs-lookup"><span data-stu-id="f3dbd-168">79</span></span>

<span data-ttu-id="f3dbd-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-171">80</span><span class="sxs-lookup"><span data-stu-id="f3dbd-171">80</span></span>

<span data-ttu-id="f3dbd-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-174">81</span><span class="sxs-lookup"><span data-stu-id="f3dbd-174">81</span></span>

<span data-ttu-id="f3dbd-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-177">82</span><span class="sxs-lookup"><span data-stu-id="f3dbd-177">82</span></span>

<span data-ttu-id="f3dbd-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-180">83</span><span class="sxs-lookup"><span data-stu-id="f3dbd-180">83</span></span>

<span data-ttu-id="f3dbd-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-183">84</span><span class="sxs-lookup"><span data-stu-id="f3dbd-183">84</span></span>

<span data-ttu-id="f3dbd-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-186">85</span><span class="sxs-lookup"><span data-stu-id="f3dbd-186">85</span></span>

<span data-ttu-id="f3dbd-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-189">86</span><span class="sxs-lookup"><span data-stu-id="f3dbd-189">86</span></span>

<span data-ttu-id="f3dbd-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-192">87</span><span class="sxs-lookup"><span data-stu-id="f3dbd-192">87</span></span>

<span data-ttu-id="f3dbd-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-195">88</span><span class="sxs-lookup"><span data-stu-id="f3dbd-195">88</span></span>

<span data-ttu-id="f3dbd-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-198">89</span><span class="sxs-lookup"><span data-stu-id="f3dbd-198">89</span></span>

<span data-ttu-id="f3dbd-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-201">90</span><span class="sxs-lookup"><span data-stu-id="f3dbd-201">90</span></span>

<span data-ttu-id="f3dbd-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-204">91</span><span class="sxs-lookup"><span data-stu-id="f3dbd-204">91</span></span>

<span data-ttu-id="f3dbd-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-207">92</span><span class="sxs-lookup"><span data-stu-id="f3dbd-207">92</span></span>

<span data-ttu-id="f3dbd-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-210">93</span><span class="sxs-lookup"><span data-stu-id="f3dbd-210">93</span></span>

<span data-ttu-id="f3dbd-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-213">94</span><span class="sxs-lookup"><span data-stu-id="f3dbd-213">94</span></span>

<span data-ttu-id="f3dbd-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-216">95</span><span class="sxs-lookup"><span data-stu-id="f3dbd-216">95</span></span>

<span data-ttu-id="f3dbd-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-219">96</span><span class="sxs-lookup"><span data-stu-id="f3dbd-219">96</span></span>

<span data-ttu-id="f3dbd-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-222">97</span><span class="sxs-lookup"><span data-stu-id="f3dbd-222">97</span></span>

<span data-ttu-id="f3dbd-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-225">98</span><span class="sxs-lookup"><span data-stu-id="f3dbd-225">98</span></span>

<span data-ttu-id="f3dbd-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-228">100</span><span class="sxs-lookup"><span data-stu-id="f3dbd-228">100</span></span>

<span data-ttu-id="f3dbd-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="f3dbd-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="f3dbd-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="f3dbd-231">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="f3dbd-232">範例</span><span class="sxs-lookup"><span data-stu-id="f3dbd-232">Examples</span></span>

<span data-ttu-id="f3dbd-233">若要在 TechNet 資源庫上 [使用來源路由 VBScript 範例修改 ARP 查詢](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) ，請使用 **SetArpAlwaysSourceRoute** 將 tcp/ip 設定為一律使用所有權杖環網路上的來源路由。</span><span class="sxs-lookup"><span data-stu-id="f3dbd-233">The [Modify ARP Queries to Use Source Routing](https://Gallery.TechNet.Microsoft.Com/e0298c96-acc2-4809-9365-fce3000db00e) VBScript sample on TechNet Gallery uses **SetArpAlwaysSourceRoute** to configure TCP/IP to always use source routing on all Token Ring networks.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3dbd-234">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3dbd-234">Requirements</span></span>



| <span data-ttu-id="f3dbd-235">需求</span><span class="sxs-lookup"><span data-stu-id="f3dbd-235">Requirement</span></span> | <span data-ttu-id="f3dbd-236">值</span><span class="sxs-lookup"><span data-stu-id="f3dbd-236">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f3dbd-237">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3dbd-237">Minimum supported client</span></span><br/> | <span data-ttu-id="f3dbd-238">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f3dbd-238">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f3dbd-239">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3dbd-239">Minimum supported server</span></span><br/> | <span data-ttu-id="f3dbd-240">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f3dbd-240">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f3dbd-241">命名空間</span><span class="sxs-lookup"><span data-stu-id="f3dbd-241">Namespace</span></span><br/>                | <span data-ttu-id="f3dbd-242">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f3dbd-242">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f3dbd-243">MOF</span><span class="sxs-lookup"><span data-stu-id="f3dbd-243">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3dbd-244"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3dbd-244"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3dbd-245">DLL</span><span class="sxs-lookup"><span data-stu-id="f3dbd-245">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3dbd-246"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f3dbd-246"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3dbd-247">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3dbd-247">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3dbd-248">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="f3dbd-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="f3dbd-249">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="f3dbd-249">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="f3dbd-250">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="f3dbd-250">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="f3dbd-251">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="f3dbd-251">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="f3dbd-252">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="f3dbd-252">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

