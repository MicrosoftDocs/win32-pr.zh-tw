---
description: EnableDHCP WMI 類別方法會啟用動態主機設定通訊協定， (DHCP) 用於此網路介面卡的服務。 DHCP 允許動態配置 IP 位址。
ms.assetid: 8c61d731-77a3-4ef4-bad9-26edaca60892
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 EnableDHCP 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableDHCP
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 002dedd3b0165053fea98dda035316676af638f4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936222"
---
# <a name="enabledhcp-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="a0a5f-104">Win32 >networkadapterconfiguration 類別的 EnableDHCP 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a0a5f-104">EnableDHCP method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="a0a5f-105">**EnableDHCP** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會啟用動態主機設定通訊協定， (DHCP) 用於此網路介面卡的服務。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-105">The **EnableDHCP** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables the Dynamic Host Configuration Protocol (DHCP) for service with this network adapter.</span></span> <span data-ttu-id="a0a5f-106">DHCP 允許動態配置 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-106">DHCP allows IP addresses to be dynamically allocated.</span></span>

<span data-ttu-id="a0a5f-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a0a5f-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a0a5f-109">語法</span><span class="sxs-lookup"><span data-stu-id="a0a5f-109">Syntax</span></span>


```mof
uint32 EnableDHCP();
```



## <a name="parameters"></a><span data-ttu-id="a0a5f-110">參數</span><span class="sxs-lookup"><span data-stu-id="a0a5f-110">Parameters</span></span>

<span data-ttu-id="a0a5f-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a0a5f-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="a0a5f-112">Return value</span></span>

<span data-ttu-id="a0a5f-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，以及任何其他數位（如果發生錯誤）。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="a0a5f-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a0a5f-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a0a5f-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-117">0</span><span class="sxs-lookup"><span data-stu-id="a0a5f-117">0</span></span>

<span data-ttu-id="a0a5f-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-120">1</span><span class="sxs-lookup"><span data-stu-id="a0a5f-120">1</span></span>

<span data-ttu-id="a0a5f-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-123">64</span><span class="sxs-lookup"><span data-stu-id="a0a5f-123">64</span></span>

<span data-ttu-id="a0a5f-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-126">65</span><span class="sxs-lookup"><span data-stu-id="a0a5f-126">65</span></span>

<span data-ttu-id="a0a5f-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-129">66</span><span class="sxs-lookup"><span data-stu-id="a0a5f-129">66</span></span>

<span data-ttu-id="a0a5f-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-132">67</span><span class="sxs-lookup"><span data-stu-id="a0a5f-132">67</span></span>

<span data-ttu-id="a0a5f-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-135">68</span><span class="sxs-lookup"><span data-stu-id="a0a5f-135">68</span></span>

<span data-ttu-id="a0a5f-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-138">69</span><span class="sxs-lookup"><span data-stu-id="a0a5f-138">69</span></span>

<span data-ttu-id="a0a5f-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-141">70</span><span class="sxs-lookup"><span data-stu-id="a0a5f-141">70</span></span>

<span data-ttu-id="a0a5f-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-144">71</span><span class="sxs-lookup"><span data-stu-id="a0a5f-144">71</span></span>

<span data-ttu-id="a0a5f-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-147">72</span><span class="sxs-lookup"><span data-stu-id="a0a5f-147">72</span></span>

<span data-ttu-id="a0a5f-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-150">73</span><span class="sxs-lookup"><span data-stu-id="a0a5f-150">73</span></span>

<span data-ttu-id="a0a5f-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-153">74</span><span class="sxs-lookup"><span data-stu-id="a0a5f-153">74</span></span>

<span data-ttu-id="a0a5f-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-156">75</span><span class="sxs-lookup"><span data-stu-id="a0a5f-156">75</span></span>

<span data-ttu-id="a0a5f-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-159">76</span><span class="sxs-lookup"><span data-stu-id="a0a5f-159">76</span></span>

<span data-ttu-id="a0a5f-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-162">77</span><span class="sxs-lookup"><span data-stu-id="a0a5f-162">77</span></span>

<span data-ttu-id="a0a5f-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-165">78</span><span class="sxs-lookup"><span data-stu-id="a0a5f-165">78</span></span>

<span data-ttu-id="a0a5f-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-168">79</span><span class="sxs-lookup"><span data-stu-id="a0a5f-168">79</span></span>

<span data-ttu-id="a0a5f-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-171">80</span><span class="sxs-lookup"><span data-stu-id="a0a5f-171">80</span></span>

<span data-ttu-id="a0a5f-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-174">81</span><span class="sxs-lookup"><span data-stu-id="a0a5f-174">81</span></span>

<span data-ttu-id="a0a5f-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-177">82</span><span class="sxs-lookup"><span data-stu-id="a0a5f-177">82</span></span>

<span data-ttu-id="a0a5f-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-180">83</span><span class="sxs-lookup"><span data-stu-id="a0a5f-180">83</span></span>

<span data-ttu-id="a0a5f-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-183">84</span><span class="sxs-lookup"><span data-stu-id="a0a5f-183">84</span></span>

<span data-ttu-id="a0a5f-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-186">85</span><span class="sxs-lookup"><span data-stu-id="a0a5f-186">85</span></span>

<span data-ttu-id="a0a5f-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-189">86</span><span class="sxs-lookup"><span data-stu-id="a0a5f-189">86</span></span>

<span data-ttu-id="a0a5f-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-192">87</span><span class="sxs-lookup"><span data-stu-id="a0a5f-192">87</span></span>

<span data-ttu-id="a0a5f-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-195">88</span><span class="sxs-lookup"><span data-stu-id="a0a5f-195">88</span></span>

<span data-ttu-id="a0a5f-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-198">89</span><span class="sxs-lookup"><span data-stu-id="a0a5f-198">89</span></span>

<span data-ttu-id="a0a5f-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-201">90</span><span class="sxs-lookup"><span data-stu-id="a0a5f-201">90</span></span>

<span data-ttu-id="a0a5f-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-204">91</span><span class="sxs-lookup"><span data-stu-id="a0a5f-204">91</span></span>

<span data-ttu-id="a0a5f-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-207">92</span><span class="sxs-lookup"><span data-stu-id="a0a5f-207">92</span></span>

<span data-ttu-id="a0a5f-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-210">93</span><span class="sxs-lookup"><span data-stu-id="a0a5f-210">93</span></span>

<span data-ttu-id="a0a5f-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-213">94</span><span class="sxs-lookup"><span data-stu-id="a0a5f-213">94</span></span>

<span data-ttu-id="a0a5f-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-216">95</span><span class="sxs-lookup"><span data-stu-id="a0a5f-216">95</span></span>

<span data-ttu-id="a0a5f-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-219">96</span><span class="sxs-lookup"><span data-stu-id="a0a5f-219">96</span></span>

<span data-ttu-id="a0a5f-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-222">97</span><span class="sxs-lookup"><span data-stu-id="a0a5f-222">97</span></span>

<span data-ttu-id="a0a5f-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-225">98</span><span class="sxs-lookup"><span data-stu-id="a0a5f-225">98</span></span>

<span data-ttu-id="a0a5f-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-228">100</span><span class="sxs-lookup"><span data-stu-id="a0a5f-228">100</span></span>

<span data-ttu-id="a0a5f-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a0a5f-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="a0a5f-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="a0a5f-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0a5f-232">備註</span><span class="sxs-lookup"><span data-stu-id="a0a5f-232">Remarks</span></span>

<span data-ttu-id="a0a5f-233">這個方法不會清除任何存在於電腦上的靜態預設閘道。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-233">This method does not clears any static default gateways present on the machine.</span></span>

## <a name="examples"></a><span data-ttu-id="a0a5f-234">範例</span><span class="sxs-lookup"><span data-stu-id="a0a5f-234">Examples</span></span>

<span data-ttu-id="a0a5f-235">TechNet 資源庫上的 [啟用 dhcp 和指派 Dns 伺服器](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) VBScript 程式碼範例會使用 EnableDHCP 來啟用 dhcp，並將 dns 伺服器指派給電腦。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-235">The [Enable DHCP and Assign DNS Servers](https://Gallery.TechNet.Microsoft.Com/7b1cec46-bdb8-4afc-b240-9789eefce6de) VBScript code sample on TechNet Gallery uses EnableDHCP to enable DHCP and assign DNS servers to a computer.</span></span>

<span data-ttu-id="a0a5f-236">下列 VBScript 程式碼範例示範如何在 [**Win32 \_ >networkadapterconfiguration**](win32-networkadapterconfiguration.md) 的實例上啟用 DHCP 使用。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-236">The following VBScript code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="a0a5f-237">在此情況下，我們會指定索引為0的介面卡。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-237">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="a0a5f-238">您應該從其他介面的 Win32 NetworkAdapter 實例中選取正確的索引 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-238">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="a0a5f-239">僅在 NT 平臺上支援。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-239">Supported on NT platforms only.</span></span>

 


```VB
Set Adapter = GetObject("winmgmts:Win32_NetworkAdapterConfiguration=0")

RetVal = Adapter.EnableDHCP()

if RetVal = 0 then 
 WScript.Echo "DHCP Enabled"
else 
 WScript.Echo "DHCP enable failed"
end if
```



<span data-ttu-id="a0a5f-240">下列 Perl 程式碼範例示範如何在 [**Win32 \_ >networkadapterconfiguration**](win32-networkadapterconfiguration.md) 的實例上啟用 DHCP 使用。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-240">The following Perl code sample demonstrates how to enable DHCP use on an instance of [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) .</span></span> <span data-ttu-id="a0a5f-241">在此情況下，我們會指定索引為0的介面卡。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-241">In this case we specify the adapter with an Index of 0.</span></span> <span data-ttu-id="a0a5f-242">您應該從其他介面的 Win32 NetworkAdapter 實例中選取正確的索引 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-242">The correct index should be selected from Win32\_NetworkAdapter instances for other interfaces.</span></span>

> [!Note]  
> <span data-ttu-id="a0a5f-243">僅在 NT 平臺上支援。</span><span class="sxs-lookup"><span data-stu-id="a0a5f-243">Supported on NT platforms only.</span></span>

 


```
use strict;
use Win32::OLE;

my ( $Adapter, $RetVal );

eval { $Adapter = Win32::OLE->GetObject("winmgmts:{impersonationLevel=impersonate}!\\\\.\\root\\cimv2")->
       Get("Win32_NetworkAdapterConfiguration=0"); };
unless ($@)
{
 print "\n";
 $RetVal = $Adapter->EnableDHCP();
 if ( $RetVal == 0)
 {
  print "DHCP Enabled\n";
 }
 else
 {
  print "DHCP enable failed\n";
 }
}
else
{
 print STDERR Win32::OLE->LastError, "\n";
}
```



## <a name="requirements"></a><span data-ttu-id="a0a5f-244">規格需求</span><span class="sxs-lookup"><span data-stu-id="a0a5f-244">Requirements</span></span>



| <span data-ttu-id="a0a5f-245">需求</span><span class="sxs-lookup"><span data-stu-id="a0a5f-245">Requirement</span></span> | <span data-ttu-id="a0a5f-246">值</span><span class="sxs-lookup"><span data-stu-id="a0a5f-246">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a0a5f-247">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a0a5f-247">Minimum supported client</span></span><br/> | <span data-ttu-id="a0a5f-248">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0a5f-248">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a0a5f-249">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a0a5f-249">Minimum supported server</span></span><br/> | <span data-ttu-id="a0a5f-250">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a0a5f-250">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a0a5f-251">命名空間</span><span class="sxs-lookup"><span data-stu-id="a0a5f-251">Namespace</span></span><br/>                | <span data-ttu-id="a0a5f-252">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a0a5f-252">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a0a5f-253">MOF</span><span class="sxs-lookup"><span data-stu-id="a0a5f-253">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a0a5f-254"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a0a5f-254"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a0a5f-255">DLL</span><span class="sxs-lookup"><span data-stu-id="a0a5f-255">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a0a5f-256"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a0a5f-256"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0a5f-257">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a0a5f-257">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0a5f-258">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="a0a5f-258">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a0a5f-259">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="a0a5f-259">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="a0a5f-260">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="a0a5f-260">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="a0a5f-261">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="a0a5f-261">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="a0a5f-262">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="a0a5f-262">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

