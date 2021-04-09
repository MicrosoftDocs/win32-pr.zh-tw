---
description: EnableStatic WMI 類別方法會啟用目標網路介面卡的靜態 TCP/IP 定址。 因此，會停用此網路介面卡的 DHCP。
ms.assetid: d0076424-58c0-4cfe-b55b-44c0f2620388
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 EnableStatic 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableStatic
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 74a7b9ca8c8016cca5a78f2e7fe753f00398193e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688748"
---
# <a name="enablestatic-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="07afd-104">Win32 >networkadapterconfiguration 類別的 EnableStatic 方法 \_</span><span class="sxs-lookup"><span data-stu-id="07afd-104">EnableStatic method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="07afd-105">**EnableStatic** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會啟用目標網路介面卡的靜態 tcp/ip 定址。</span><span class="sxs-lookup"><span data-stu-id="07afd-105">The **EnableStatic** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables static TCP/IP addressing for the target network adapter.</span></span> <span data-ttu-id="07afd-106">因此，會停用此網路介面卡的 DHCP。</span><span class="sxs-lookup"><span data-stu-id="07afd-106">As a result, DHCP for this network adapter is disabled.</span></span>

<span data-ttu-id="07afd-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="07afd-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="07afd-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="07afd-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="07afd-109">語法</span><span class="sxs-lookup"><span data-stu-id="07afd-109">Syntax</span></span>


```mof
uint32 EnableStatic(
  [in] string IPAddress[],
  [in] string SubnetMask[]
);
```



## <a name="parameters"></a><span data-ttu-id="07afd-110">參數</span><span class="sxs-lookup"><span data-stu-id="07afd-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07afd-111">*IPAddress* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07afd-111">*IPAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07afd-112">列出目前網路介面卡的所有靜態 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="07afd-112">Lists all of the static IP addresses for the current network adapter.</span></span>

<span data-ttu-id="07afd-113">範例：155.34.22.0。</span><span class="sxs-lookup"><span data-stu-id="07afd-113">Example: 155.34.22.0.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-114">*SubnetMask* \[在\]</span><span class="sxs-lookup"><span data-stu-id="07afd-114">*SubnetMask* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="07afd-115">子網路遮罩，可補充 *IPAddress* 參數中的值。</span><span class="sxs-lookup"><span data-stu-id="07afd-115">Subnet masks that complement the values in the *IPAddress* parameter.</span></span>

<span data-ttu-id="07afd-116">範例：255.255.0.0。</span><span class="sxs-lookup"><span data-stu-id="07afd-116">Example: 255.255.0.0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07afd-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="07afd-117">Return value</span></span>

<span data-ttu-id="07afd-118">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，以及任何其他數位（如果發生錯誤）。</span><span class="sxs-lookup"><span data-stu-id="07afd-118">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="07afd-119">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="07afd-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="07afd-120">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="07afd-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="07afd-121">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="07afd-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-122">0</span><span class="sxs-lookup"><span data-stu-id="07afd-122">0</span></span>

<span data-ttu-id="07afd-123">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="07afd-123">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-124">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="07afd-124">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-125">1</span><span class="sxs-lookup"><span data-stu-id="07afd-125">1</span></span>

<span data-ttu-id="07afd-126">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="07afd-126">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-127">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="07afd-127">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-128">64</span><span class="sxs-lookup"><span data-stu-id="07afd-128">64</span></span>

<span data-ttu-id="07afd-129">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="07afd-129">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-130">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="07afd-130">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-131">65</span><span class="sxs-lookup"><span data-stu-id="07afd-131">65</span></span>

<span data-ttu-id="07afd-132">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="07afd-132">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-133">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="07afd-133">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-134">66</span><span class="sxs-lookup"><span data-stu-id="07afd-134">66</span></span>

<span data-ttu-id="07afd-135">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="07afd-135">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-136">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="07afd-136">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-137">67</span><span class="sxs-lookup"><span data-stu-id="07afd-137">67</span></span>

<span data-ttu-id="07afd-138">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="07afd-138">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-139">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="07afd-139">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-140">68</span><span class="sxs-lookup"><span data-stu-id="07afd-140">68</span></span>

<span data-ttu-id="07afd-141">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="07afd-141">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-142">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="07afd-142">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-143">69</span><span class="sxs-lookup"><span data-stu-id="07afd-143">69</span></span>

<span data-ttu-id="07afd-144">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="07afd-144">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-145">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="07afd-145">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-146">70</span><span class="sxs-lookup"><span data-stu-id="07afd-146">70</span></span>

<span data-ttu-id="07afd-147">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="07afd-147">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-148">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="07afd-148">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-149">71</span><span class="sxs-lookup"><span data-stu-id="07afd-149">71</span></span>

<span data-ttu-id="07afd-150">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="07afd-150">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-151">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="07afd-151">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-152">72</span><span class="sxs-lookup"><span data-stu-id="07afd-152">72</span></span>

<span data-ttu-id="07afd-153">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="07afd-153">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-154">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="07afd-154">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-155">73</span><span class="sxs-lookup"><span data-stu-id="07afd-155">73</span></span>

<span data-ttu-id="07afd-156">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="07afd-156">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-157">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="07afd-157">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-158">74</span><span class="sxs-lookup"><span data-stu-id="07afd-158">74</span></span>

<span data-ttu-id="07afd-159">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="07afd-159">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-160">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="07afd-160">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-161">75</span><span class="sxs-lookup"><span data-stu-id="07afd-161">75</span></span>

<span data-ttu-id="07afd-162">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="07afd-162">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-163">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="07afd-163">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-164">76</span><span class="sxs-lookup"><span data-stu-id="07afd-164">76</span></span>

<span data-ttu-id="07afd-165">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="07afd-165">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-166">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="07afd-166">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-167">77</span><span class="sxs-lookup"><span data-stu-id="07afd-167">77</span></span>

<span data-ttu-id="07afd-168">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="07afd-168">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-169">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="07afd-169">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-170">78</span><span class="sxs-lookup"><span data-stu-id="07afd-170">78</span></span>

<span data-ttu-id="07afd-171">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="07afd-171">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-172">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="07afd-172">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-173">79</span><span class="sxs-lookup"><span data-stu-id="07afd-173">79</span></span>

<span data-ttu-id="07afd-174">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="07afd-174">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-175">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="07afd-175">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-176">80</span><span class="sxs-lookup"><span data-stu-id="07afd-176">80</span></span>

<span data-ttu-id="07afd-177">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="07afd-177">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-178">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="07afd-178">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-179">81</span><span class="sxs-lookup"><span data-stu-id="07afd-179">81</span></span>

<span data-ttu-id="07afd-180">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="07afd-180">Unable to configure DHCP service.</span></span> <span data-ttu-id="07afd-181">如需詳細資訊，請參閱＜備註＞一節。</span><span class="sxs-lookup"><span data-stu-id="07afd-181">For more information, see the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-182">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="07afd-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-183">82</span><span class="sxs-lookup"><span data-stu-id="07afd-183">82</span></span>

<span data-ttu-id="07afd-184">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="07afd-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-185">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="07afd-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-186">83</span><span class="sxs-lookup"><span data-stu-id="07afd-186">83</span></span>

<span data-ttu-id="07afd-187">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="07afd-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-188">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="07afd-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-189">84</span><span class="sxs-lookup"><span data-stu-id="07afd-189">84</span></span>

<span data-ttu-id="07afd-190">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="07afd-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-191">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="07afd-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-192">85</span><span class="sxs-lookup"><span data-stu-id="07afd-192">85</span></span>

<span data-ttu-id="07afd-193">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="07afd-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-194">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="07afd-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-195">86</span><span class="sxs-lookup"><span data-stu-id="07afd-195">86</span></span>

<span data-ttu-id="07afd-196">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="07afd-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-197">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="07afd-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-198">87</span><span class="sxs-lookup"><span data-stu-id="07afd-198">87</span></span>

<span data-ttu-id="07afd-199">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="07afd-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-200">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="07afd-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-201">88</span><span class="sxs-lookup"><span data-stu-id="07afd-201">88</span></span>

<span data-ttu-id="07afd-202">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="07afd-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-203">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="07afd-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-204">89</span><span class="sxs-lookup"><span data-stu-id="07afd-204">89</span></span>

<span data-ttu-id="07afd-205">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="07afd-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-206">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="07afd-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-207">90</span><span class="sxs-lookup"><span data-stu-id="07afd-207">90</span></span>

<span data-ttu-id="07afd-208">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="07afd-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-209">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="07afd-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-210">91</span><span class="sxs-lookup"><span data-stu-id="07afd-210">91</span></span>

<span data-ttu-id="07afd-211">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="07afd-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-212">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="07afd-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-213">92</span><span class="sxs-lookup"><span data-stu-id="07afd-213">92</span></span>

<span data-ttu-id="07afd-214">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="07afd-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-215">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="07afd-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-216">93</span><span class="sxs-lookup"><span data-stu-id="07afd-216">93</span></span>

<span data-ttu-id="07afd-217">已經存在。</span><span class="sxs-lookup"><span data-stu-id="07afd-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-218">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="07afd-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-219">94</span><span class="sxs-lookup"><span data-stu-id="07afd-219">94</span></span>

<span data-ttu-id="07afd-220">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="07afd-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-221">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="07afd-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-222">95</span><span class="sxs-lookup"><span data-stu-id="07afd-222">95</span></span>

<span data-ttu-id="07afd-223">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="07afd-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-224">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="07afd-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-225">96</span><span class="sxs-lookup"><span data-stu-id="07afd-225">96</span></span>

<span data-ttu-id="07afd-226">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="07afd-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-227">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="07afd-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-228">97</span><span class="sxs-lookup"><span data-stu-id="07afd-228">97</span></span>

<span data-ttu-id="07afd-229">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="07afd-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-230">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="07afd-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-231">98</span><span class="sxs-lookup"><span data-stu-id="07afd-231">98</span></span>

<span data-ttu-id="07afd-232">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="07afd-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-233">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="07afd-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-234">100</span><span class="sxs-lookup"><span data-stu-id="07afd-234">100</span></span>

<span data-ttu-id="07afd-235">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="07afd-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="07afd-236">**2147786788**</span><span class="sxs-lookup"><span data-stu-id="07afd-236">**2147786788**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-237">未啟用寫入鎖定。</span><span class="sxs-lookup"><span data-stu-id="07afd-237">Write lock not enabled.</span></span> <span data-ttu-id="07afd-238">如需詳細資訊，請參閱 [**INetCfgLock：： AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="07afd-238">For more information, see [**INetCfgLock::AcquireWriteLock**](/previous-versions/windows/hardware/network/ff547914(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="07afd-239">**其他**</span><span class="sxs-lookup"><span data-stu-id="07afd-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="07afd-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="07afd-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="07afd-241">備註</span><span class="sxs-lookup"><span data-stu-id="07afd-241">Remarks</span></span>

<span data-ttu-id="07afd-242">當使用 **EnableStatic** 來變更遠端電腦的 IP 位址時，當您透過該介面卡連線時，您可能會失去與遠端電腦的連線，並收到 RPC 無法使用的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="07afd-242">When using **EnableStatic** to change the IP address of the remote computer, while being connected through that adapter, you will likely loose connection to the remote computer, and receive an RPC not available error-message.</span></span> <span data-ttu-id="07afd-243">不過 (設定會) 變更。</span><span class="sxs-lookup"><span data-stu-id="07afd-243">(the settings are changed however).</span></span> <span data-ttu-id="07afd-244">若要避免這種情況，請考慮在設定介面卡的 IP 位址之前變更閘道和/或 DNS 設定。</span><span class="sxs-lookup"><span data-stu-id="07afd-244">To avoid this scenario, consider changing the Gateway and/or DNS-settings prior to setting the adapter's IP-address.</span></span>

<span data-ttu-id="07afd-245">使用 **EnableStatic** 為介面卡提供靜態 IP 設定時，如果已使用靜態位址設定介面卡，此函式會傳回「81-無法設定 DHCP 服務」。</span><span class="sxs-lookup"><span data-stu-id="07afd-245">When using **EnableStatic** to give an adapter a static IP configuration, the function returns an "81 - Unable to configure DHCP service" if the adapter is already configured with a static address.</span></span> <span data-ttu-id="07afd-246">不過，此函式仍會與新的作業一起設定成功。</span><span class="sxs-lookup"><span data-stu-id="07afd-246">However, the function still succeeds in setting with the new operation.</span></span>

## <a name="examples"></a><span data-ttu-id="07afd-247">範例</span><span class="sxs-lookup"><span data-stu-id="07afd-247">Examples</span></span>

<span data-ttu-id="07afd-248">在 TechNet 資源庫上， [靜態 ip 接著加入網域](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell 程式碼範例會使用 **ENABLESTATIC** 將靜態 ip 新增至本機電腦。</span><span class="sxs-lookup"><span data-stu-id="07afd-248">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell code sample, on TechNet Gallery, uses **EnableStatic** to add a static IP to a local machine.</span></span>

<span data-ttu-id="07afd-249">在 TechNet 資源庫上， [指派靜態 IP 位址](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript 程式碼範例會使用 **EnableStatic** 來設定電腦的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="07afd-249">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript code example, on TechNet Gallery, uses **EnableStatic** to set the IP address of a computer.</span></span>

<span data-ttu-id="07afd-250">下列 VBScript 範例示範如何停用在 [**Win32 \_ >networkadapterconfiguration**](win32-networkadapterconfiguration.md)實例上使用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="07afd-250">The following VBScript sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="07afd-251">在此情況下，我們會指定索引為0的介面卡。</span><span class="sxs-lookup"><span data-stu-id="07afd-251">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="07afd-252">您應該從其他介面的 Win32 NetworkAdapter 實例中選取正確的索引 \_ 。</span><span class="sxs-lookup"><span data-stu-id="07afd-252">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="07afd-253">此腳本僅適用于以 NT 為基礎的系統，將下列 ipaddr 和子網變數變更為您想要套用至介面卡的值。</span><span class="sxs-lookup"><span data-stu-id="07afd-253">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=1")

ipaddr = Array("1.1.1.1")
subnet = Array("255.255.255.0")


RetVal = Adapter.EnableStatic(ipaddr,subnet)

if RetVal = 0 then 
 WScript.Echo "DHCP disabled, using static IP address"
else 
 WScript.Echo "DHCP disable failed"
end if
```



<span data-ttu-id="07afd-254">下列 Perl 範例示範如何停用在 [**Win32 \_ >networkadapterconfiguration**](win32-networkadapterconfiguration.md)實例上使用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="07afd-254">The following Perl sample demonstrates how to disable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md).</span></span> <span data-ttu-id="07afd-255">在此情況下，我們會指定索引為0的介面卡。</span><span class="sxs-lookup"><span data-stu-id="07afd-255">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="07afd-256">您應該從其他介面的 Win32 NetworkAdapter 實例中選取正確的索引 \_ 。</span><span class="sxs-lookup"><span data-stu-id="07afd-256">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="07afd-257">此腳本僅適用于以 NT 為基礎的系統，將下列 ipaddr 和子網變數變更為您想要套用至介面卡的值。</span><span class="sxs-lookup"><span data-stu-id="07afd-257">This script only applies to NT-based systems Change the ipaddr and subnet variables below to the values you wish to apply to the adapter.</span></span>

 


```
use strict;
use Win32::OLE;

my ($Adapter, @ipaddr, @subnet, $RetVal);  
eval { $Adapter = 
 Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2:Win32_NetworkAdapterConfiguration.Index=\"0\""); };

unless ($@) 
{
 push @ipaddr, "192.168.144.107";
 push @subnet, "255.255.255.0";

 $RetVal = $Adapter->EnableStatic(\@ipaddr, \@subnet);

 if ($RetVal == 0) 
 {
  print "\nDHCP disabled, using static IP address\n";
 }
 else 
 {
  print "\nDHCP disable failed\n";
 }
}
else
{
 print STDERR "\n", Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="07afd-258">規格需求</span><span class="sxs-lookup"><span data-stu-id="07afd-258">Requirements</span></span>



| <span data-ttu-id="07afd-259">需求</span><span class="sxs-lookup"><span data-stu-id="07afd-259">Requirement</span></span> | <span data-ttu-id="07afd-260">值</span><span class="sxs-lookup"><span data-stu-id="07afd-260">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="07afd-261">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="07afd-261">Minimum supported client</span></span><br/> | <span data-ttu-id="07afd-262">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="07afd-262">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="07afd-263">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="07afd-263">Minimum supported server</span></span><br/> | <span data-ttu-id="07afd-264">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="07afd-264">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="07afd-265">命名空間</span><span class="sxs-lookup"><span data-stu-id="07afd-265">Namespace</span></span><br/>                | <span data-ttu-id="07afd-266">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="07afd-266">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="07afd-267">MOF</span><span class="sxs-lookup"><span data-stu-id="07afd-267">MOF</span></span><br/>                      | <dl> <span data-ttu-id="07afd-268"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="07afd-268"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="07afd-269">DLL</span><span class="sxs-lookup"><span data-stu-id="07afd-269">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07afd-270"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="07afd-270"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07afd-271">另請參閱</span><span class="sxs-lookup"><span data-stu-id="07afd-271">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07afd-272">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="07afd-272">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="07afd-273">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="07afd-273">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="07afd-274">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="07afd-274">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="07afd-275">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="07afd-275">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="07afd-276">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="07afd-276">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

