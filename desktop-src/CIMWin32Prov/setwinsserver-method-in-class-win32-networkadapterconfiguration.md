---
description: SetWINSServer WMI 類別方法會在此 TCP/IP 系結的網路介面卡上，將主要和次要 Windows 網際網路命名服務設定 (WINS) 伺服器。 此方法會獨立套用到網路介面卡。
ms.assetid: fa8ce436-b67e-4975-a5c5-1a7d6aab4c8e
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetWINSServer 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetWINSServer
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 49bfb0103a7d9cbbd6ea3faa0e1a868bac7b0196
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984148"
---
# <a name="setwinsserver-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="ff7ad-104">Win32 >networkadapterconfiguration 類別的 SetWINSServer 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ff7ad-104">SetWINSServer method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="ff7ad-105">**SetWINSServer** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會在此 tcp/ip 系結的網路介面卡上，將主要和次要 Windows 網際網路命名服務設定 (WINS) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-105">The **SetWINSServer** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method sets the primary and secondary Windows Internet Naming Service (WINS) servers on this TCP/IP-bound network adapter.</span></span> <span data-ttu-id="ff7ad-106">此方法會獨立套用到網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-106">This method is applied independently of the network adapter.</span></span>

<span data-ttu-id="ff7ad-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ff7ad-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff7ad-109">語法</span><span class="sxs-lookup"><span data-stu-id="ff7ad-109">Syntax</span></span>


```mof
uint32 SetWINSServer(
  [in] string WINSPrimaryServer,
  [in] string WINSSecondaryServer
);
```



## <a name="parameters"></a><span data-ttu-id="ff7ad-110">參數</span><span class="sxs-lookup"><span data-stu-id="ff7ad-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff7ad-111">*WINSPrimaryServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff7ad-111">*WINSPrimaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-112">主要 WINS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-112">IP address of the primary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="ff7ad-113">當此 IP 位址來自不明來源或您不信任的來源時，請務必確認此 IP 位址的有效性。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-113">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> <dt>

<span data-ttu-id="ff7ad-114">*WINSSecondaryServer* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff7ad-114">*WINSSecondaryServer* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-115">次要 WINS 伺服器的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-115">IP address of the secondary WINS server.</span></span>

> [!Note]  
> <span data-ttu-id="ff7ad-116">當此 IP 位址來自不明來源或您不信任的來源時，請務必確認此 IP 位址的有效性。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-116">Always verify the validity of this IP address when it is from an unknown source, or a source that you do not trust.</span></span>

 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff7ad-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff7ad-117">Return value</span></span>

<span data-ttu-id="ff7ad-118">在成功完成時傳回 0 (零) 的整數值，以及表示錯誤的任何其他數位。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-118">Returns an integer value of 0 (zero) on successful completion, and any other number to indicate an error.</span></span> <span data-ttu-id="ff7ad-119">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ff7ad-120">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ff7ad-121">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-122">0</span><span class="sxs-lookup"><span data-stu-id="ff7ad-122">0</span></span>

<span data-ttu-id="ff7ad-123">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-124">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-125">1</span><span class="sxs-lookup"><span data-stu-id="ff7ad-125">1</span></span>

<span data-ttu-id="ff7ad-126">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-127">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-128">64</span><span class="sxs-lookup"><span data-stu-id="ff7ad-128">64</span></span>

<span data-ttu-id="ff7ad-129">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-130">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-131">65</span><span class="sxs-lookup"><span data-stu-id="ff7ad-131">65</span></span>

<span data-ttu-id="ff7ad-132">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-133">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-134">66</span><span class="sxs-lookup"><span data-stu-id="ff7ad-134">66</span></span>

<span data-ttu-id="ff7ad-135">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-136">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-137">67</span><span class="sxs-lookup"><span data-stu-id="ff7ad-137">67</span></span>

<span data-ttu-id="ff7ad-138">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-139">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-140">68</span><span class="sxs-lookup"><span data-stu-id="ff7ad-140">68</span></span>

<span data-ttu-id="ff7ad-141">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-142">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-143">69</span><span class="sxs-lookup"><span data-stu-id="ff7ad-143">69</span></span>

<span data-ttu-id="ff7ad-144">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-145">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-146">70</span><span class="sxs-lookup"><span data-stu-id="ff7ad-146">70</span></span>

<span data-ttu-id="ff7ad-147">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-148">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-149">71</span><span class="sxs-lookup"><span data-stu-id="ff7ad-149">71</span></span>

<span data-ttu-id="ff7ad-150">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-151">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-152">72</span><span class="sxs-lookup"><span data-stu-id="ff7ad-152">72</span></span>

<span data-ttu-id="ff7ad-153">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-154">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-155">73</span><span class="sxs-lookup"><span data-stu-id="ff7ad-155">73</span></span>

<span data-ttu-id="ff7ad-156">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-157">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-158">74</span><span class="sxs-lookup"><span data-stu-id="ff7ad-158">74</span></span>

<span data-ttu-id="ff7ad-159">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-160">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-161">75</span><span class="sxs-lookup"><span data-stu-id="ff7ad-161">75</span></span>

<span data-ttu-id="ff7ad-162">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-163">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-164">76</span><span class="sxs-lookup"><span data-stu-id="ff7ad-164">76</span></span>

<span data-ttu-id="ff7ad-165">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-166">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-167">77</span><span class="sxs-lookup"><span data-stu-id="ff7ad-167">77</span></span>

<span data-ttu-id="ff7ad-168">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-169">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-170">78</span><span class="sxs-lookup"><span data-stu-id="ff7ad-170">78</span></span>

<span data-ttu-id="ff7ad-171">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-172">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-173">79</span><span class="sxs-lookup"><span data-stu-id="ff7ad-173">79</span></span>

<span data-ttu-id="ff7ad-174">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-175">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-176">80</span><span class="sxs-lookup"><span data-stu-id="ff7ad-176">80</span></span>

<span data-ttu-id="ff7ad-177">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-178">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-179">81</span><span class="sxs-lookup"><span data-stu-id="ff7ad-179">81</span></span>

<span data-ttu-id="ff7ad-180">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-180">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-181">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-181">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-182">82</span><span class="sxs-lookup"><span data-stu-id="ff7ad-182">82</span></span>

<span data-ttu-id="ff7ad-183">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-183">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-184">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-184">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-185">83</span><span class="sxs-lookup"><span data-stu-id="ff7ad-185">83</span></span>

<span data-ttu-id="ff7ad-186">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-186">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-187">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-187">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-188">84</span><span class="sxs-lookup"><span data-stu-id="ff7ad-188">84</span></span>

<span data-ttu-id="ff7ad-189">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-189">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-190">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-190">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-191">85</span><span class="sxs-lookup"><span data-stu-id="ff7ad-191">85</span></span>

<span data-ttu-id="ff7ad-192">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-192">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-193">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-193">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-194">86</span><span class="sxs-lookup"><span data-stu-id="ff7ad-194">86</span></span>

<span data-ttu-id="ff7ad-195">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-195">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-196">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-196">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-197">87</span><span class="sxs-lookup"><span data-stu-id="ff7ad-197">87</span></span>

<span data-ttu-id="ff7ad-198">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-198">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-199">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-199">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-200">88</span><span class="sxs-lookup"><span data-stu-id="ff7ad-200">88</span></span>

<span data-ttu-id="ff7ad-201">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-201">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-202">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-202">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-203">89</span><span class="sxs-lookup"><span data-stu-id="ff7ad-203">89</span></span>

<span data-ttu-id="ff7ad-204">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-204">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-205">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-205">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-206">90</span><span class="sxs-lookup"><span data-stu-id="ff7ad-206">90</span></span>

<span data-ttu-id="ff7ad-207">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-207">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-208">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-208">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-209">91</span><span class="sxs-lookup"><span data-stu-id="ff7ad-209">91</span></span>

<span data-ttu-id="ff7ad-210">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-210">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-211">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-211">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-212">92</span><span class="sxs-lookup"><span data-stu-id="ff7ad-212">92</span></span>

<span data-ttu-id="ff7ad-213">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-213">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-214">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-214">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-215">93</span><span class="sxs-lookup"><span data-stu-id="ff7ad-215">93</span></span>

<span data-ttu-id="ff7ad-216">已經存在。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-216">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-217">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-217">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-218">94</span><span class="sxs-lookup"><span data-stu-id="ff7ad-218">94</span></span>

<span data-ttu-id="ff7ad-219">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-219">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-220">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-220">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-221">95</span><span class="sxs-lookup"><span data-stu-id="ff7ad-221">95</span></span>

<span data-ttu-id="ff7ad-222">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-222">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-223">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-223">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-224">96</span><span class="sxs-lookup"><span data-stu-id="ff7ad-224">96</span></span>

<span data-ttu-id="ff7ad-225">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-225">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-226">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-226">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-227">97</span><span class="sxs-lookup"><span data-stu-id="ff7ad-227">97</span></span>

<span data-ttu-id="ff7ad-228">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-228">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-229">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-229">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-230">98</span><span class="sxs-lookup"><span data-stu-id="ff7ad-230">98</span></span>

<span data-ttu-id="ff7ad-231">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-231">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-232">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-232">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-233">100</span><span class="sxs-lookup"><span data-stu-id="ff7ad-233">100</span></span>

<span data-ttu-id="ff7ad-234">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-234">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ff7ad-235">**其他**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-235">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ff7ad-236">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="ff7ad-236">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ff7ad-237">備註</span><span class="sxs-lookup"><span data-stu-id="ff7ad-237">Remarks</span></span>

<span data-ttu-id="ff7ad-238">如果 *WINSPrimaryServer* 和 *WINSSecondaryServer* 都設定為 "" () 的空字串，則明確的 WINS 伺服器會還原回 DHCP。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-238">If both *WINSPrimaryServer* and *WINSSecondaryServer* are set to "" (an empty string), then explicit WINS servers revert back to DHCP.</span></span>

## <a name="examples"></a><span data-ttu-id="ff7ad-239">範例</span><span class="sxs-lookup"><span data-stu-id="ff7ad-239">Examples</span></span>

<span data-ttu-id="ff7ad-240">[指派從資料庫取出的 IP 位址](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) VBScript 程式碼範例會查閱資料庫中的電腦，並將指定的 IP 位址指派給該電腦。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-240">[The Assign an IP Address Retrieved from a Database](https://Gallery.TechNet.Microsoft.Com/d4526355-e682-4116-a79a-8bba569b084d) VBScript code sample looks up a computer in a database and assigns that computer the specified IP address.</span></span>

<span data-ttu-id="ff7ad-241">下列 VBScript 程式碼範例會設定 TCP/IP 系結網路介面卡的主要和次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ff7ad-241">The following VBScript code sample sets the primary and secondary WINS server for a TCP/IP-bound network adapter.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    strPrimaryServer = "192.168.1.100" 
    strSecondaryServer = "192.168.1.200" 
    objNetCard.SetWINSServer strPrimaryServer, strSecondaryServer 
Next 
```



## <a name="requirements"></a><span data-ttu-id="ff7ad-242">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff7ad-242">Requirements</span></span>



| <span data-ttu-id="ff7ad-243">需求</span><span class="sxs-lookup"><span data-stu-id="ff7ad-243">Requirement</span></span> | <span data-ttu-id="ff7ad-244">值</span><span class="sxs-lookup"><span data-stu-id="ff7ad-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff7ad-245">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff7ad-245">Minimum supported client</span></span><br/> | <span data-ttu-id="ff7ad-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ff7ad-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ff7ad-247">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff7ad-247">Minimum supported server</span></span><br/> | <span data-ttu-id="ff7ad-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ff7ad-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ff7ad-249">命名空間</span><span class="sxs-lookup"><span data-stu-id="ff7ad-249">Namespace</span></span><br/>                | <span data-ttu-id="ff7ad-250">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ff7ad-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ff7ad-251">MOF</span><span class="sxs-lookup"><span data-stu-id="ff7ad-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ff7ad-252"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ff7ad-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ff7ad-253">DLL</span><span class="sxs-lookup"><span data-stu-id="ff7ad-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff7ad-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff7ad-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ff7ad-255">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff7ad-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff7ad-256">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="ff7ad-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ff7ad-257">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="ff7ad-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="ff7ad-258">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="ff7ad-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="ff7ad-259">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="ff7ad-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="ff7ad-260">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="ff7ad-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

