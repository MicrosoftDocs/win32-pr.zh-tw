---
description: DisableIPSec WMI 類別方法可用來停用此啟用 TCP/IP 的網路介面卡上 (IPsec) 的網際網路通訊協定安全性。
ms.assetid: 6fff2721-1ee2-42b4-bbf9-fd36b97318e3
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 DisableIPSec 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.DisableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9b2a17bbfa0f10c08edb581b4a4bf51173facfea
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966631"
---
# <a name="disableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="82f20-103">Win32 >networkadapterconfiguration 類別的 DisableIPSec 方法 \_</span><span class="sxs-lookup"><span data-stu-id="82f20-103">DisableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="82f20-104">**DisableIPSec** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法可用來停用此啟用 tcp/ip 的網路介面卡上 (IPsec) 的網際網路通訊協定安全性。</span><span class="sxs-lookup"><span data-stu-id="82f20-104">The **DisableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method is used to disable Internet Protocol security (IPsec) on this TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="82f20-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="82f20-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="82f20-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="82f20-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="82f20-107">語法</span><span class="sxs-lookup"><span data-stu-id="82f20-107">Syntax</span></span>


```mof
uint32 DisableIPSec();
```



## <a name="parameters"></a><span data-ttu-id="82f20-108">參數</span><span class="sxs-lookup"><span data-stu-id="82f20-108">Parameters</span></span>

<span data-ttu-id="82f20-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="82f20-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="82f20-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="82f20-110">Return value</span></span>

<span data-ttu-id="82f20-111">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，以及任何其他數位（如果發生錯誤）。</span><span class="sxs-lookup"><span data-stu-id="82f20-111">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="82f20-112">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="82f20-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="82f20-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="82f20-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="82f20-114">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="82f20-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-115">0</span><span class="sxs-lookup"><span data-stu-id="82f20-115">0</span></span>

<span data-ttu-id="82f20-116">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="82f20-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-117">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="82f20-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-118">1</span><span class="sxs-lookup"><span data-stu-id="82f20-118">1</span></span>

<span data-ttu-id="82f20-119">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="82f20-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-120">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="82f20-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-121">64</span><span class="sxs-lookup"><span data-stu-id="82f20-121">64</span></span>

<span data-ttu-id="82f20-122">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="82f20-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-123">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="82f20-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-124">65</span><span class="sxs-lookup"><span data-stu-id="82f20-124">65</span></span>

<span data-ttu-id="82f20-125">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="82f20-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-126">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="82f20-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-127">66</span><span class="sxs-lookup"><span data-stu-id="82f20-127">66</span></span>

<span data-ttu-id="82f20-128">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="82f20-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-129">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="82f20-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-130">67</span><span class="sxs-lookup"><span data-stu-id="82f20-130">67</span></span>

<span data-ttu-id="82f20-131">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="82f20-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-132">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="82f20-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-133">68</span><span class="sxs-lookup"><span data-stu-id="82f20-133">68</span></span>

<span data-ttu-id="82f20-134">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="82f20-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-135">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="82f20-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-136">69</span><span class="sxs-lookup"><span data-stu-id="82f20-136">69</span></span>

<span data-ttu-id="82f20-137">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="82f20-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-138">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="82f20-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-139">70</span><span class="sxs-lookup"><span data-stu-id="82f20-139">70</span></span>

<span data-ttu-id="82f20-140">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="82f20-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-141">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="82f20-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-142">71</span><span class="sxs-lookup"><span data-stu-id="82f20-142">71</span></span>

<span data-ttu-id="82f20-143">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="82f20-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-144">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="82f20-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-145">72</span><span class="sxs-lookup"><span data-stu-id="82f20-145">72</span></span>

<span data-ttu-id="82f20-146">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="82f20-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-147">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="82f20-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-148">73</span><span class="sxs-lookup"><span data-stu-id="82f20-148">73</span></span>

<span data-ttu-id="82f20-149">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="82f20-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-150">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="82f20-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-151">74</span><span class="sxs-lookup"><span data-stu-id="82f20-151">74</span></span>

<span data-ttu-id="82f20-152">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="82f20-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-153">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="82f20-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-154">75</span><span class="sxs-lookup"><span data-stu-id="82f20-154">75</span></span>

<span data-ttu-id="82f20-155">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="82f20-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-156">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="82f20-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-157">76</span><span class="sxs-lookup"><span data-stu-id="82f20-157">76</span></span>

<span data-ttu-id="82f20-158">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="82f20-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-159">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="82f20-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-160">77</span><span class="sxs-lookup"><span data-stu-id="82f20-160">77</span></span>

<span data-ttu-id="82f20-161">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="82f20-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-162">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="82f20-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-163">78</span><span class="sxs-lookup"><span data-stu-id="82f20-163">78</span></span>

<span data-ttu-id="82f20-164">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="82f20-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-165">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="82f20-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-166">79</span><span class="sxs-lookup"><span data-stu-id="82f20-166">79</span></span>

<span data-ttu-id="82f20-167">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="82f20-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-168">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="82f20-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-169">80</span><span class="sxs-lookup"><span data-stu-id="82f20-169">80</span></span>

<span data-ttu-id="82f20-170">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="82f20-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-171">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="82f20-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-172">81</span><span class="sxs-lookup"><span data-stu-id="82f20-172">81</span></span>

<span data-ttu-id="82f20-173">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="82f20-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-174">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="82f20-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-175">82</span><span class="sxs-lookup"><span data-stu-id="82f20-175">82</span></span>

<span data-ttu-id="82f20-176">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="82f20-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-177">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="82f20-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-178">83</span><span class="sxs-lookup"><span data-stu-id="82f20-178">83</span></span>

<span data-ttu-id="82f20-179">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="82f20-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-180">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="82f20-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-181">84</span><span class="sxs-lookup"><span data-stu-id="82f20-181">84</span></span>

<span data-ttu-id="82f20-182">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="82f20-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-183">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="82f20-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-184">85</span><span class="sxs-lookup"><span data-stu-id="82f20-184">85</span></span>

<span data-ttu-id="82f20-185">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="82f20-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-186">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="82f20-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-187">86</span><span class="sxs-lookup"><span data-stu-id="82f20-187">86</span></span>

<span data-ttu-id="82f20-188">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="82f20-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-189">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="82f20-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-190">87</span><span class="sxs-lookup"><span data-stu-id="82f20-190">87</span></span>

<span data-ttu-id="82f20-191">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="82f20-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-192">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="82f20-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-193">88</span><span class="sxs-lookup"><span data-stu-id="82f20-193">88</span></span>

<span data-ttu-id="82f20-194">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="82f20-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-195">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="82f20-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-196">89</span><span class="sxs-lookup"><span data-stu-id="82f20-196">89</span></span>

<span data-ttu-id="82f20-197">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="82f20-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-198">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="82f20-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-199">90</span><span class="sxs-lookup"><span data-stu-id="82f20-199">90</span></span>

<span data-ttu-id="82f20-200">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="82f20-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-201">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="82f20-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-202">91</span><span class="sxs-lookup"><span data-stu-id="82f20-202">91</span></span>

<span data-ttu-id="82f20-203">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="82f20-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-204">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="82f20-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-205">92</span><span class="sxs-lookup"><span data-stu-id="82f20-205">92</span></span>

<span data-ttu-id="82f20-206">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="82f20-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-207">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="82f20-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-208">93</span><span class="sxs-lookup"><span data-stu-id="82f20-208">93</span></span>

<span data-ttu-id="82f20-209">已經存在。</span><span class="sxs-lookup"><span data-stu-id="82f20-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-210">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="82f20-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-211">94</span><span class="sxs-lookup"><span data-stu-id="82f20-211">94</span></span>

<span data-ttu-id="82f20-212">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="82f20-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-213">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="82f20-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-214">95</span><span class="sxs-lookup"><span data-stu-id="82f20-214">95</span></span>

<span data-ttu-id="82f20-215">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="82f20-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-216">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="82f20-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-217">96</span><span class="sxs-lookup"><span data-stu-id="82f20-217">96</span></span>

<span data-ttu-id="82f20-218">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="82f20-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-219">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="82f20-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-220">97</span><span class="sxs-lookup"><span data-stu-id="82f20-220">97</span></span>

<span data-ttu-id="82f20-221">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="82f20-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-222">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="82f20-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-223">98</span><span class="sxs-lookup"><span data-stu-id="82f20-223">98</span></span>

<span data-ttu-id="82f20-224">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="82f20-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-225">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="82f20-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-226">100</span><span class="sxs-lookup"><span data-stu-id="82f20-226">100</span></span>

<span data-ttu-id="82f20-227">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="82f20-227">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="82f20-228">**其他**</span><span class="sxs-lookup"><span data-stu-id="82f20-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="82f20-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="82f20-229">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="82f20-230">範例</span><span class="sxs-lookup"><span data-stu-id="82f20-230">Examples</span></span>

<span data-ttu-id="82f20-231">下列 VBScript 範例會停用電腦上的 IP 安全性。</span><span class="sxs-lookup"><span data-stu-id="82f20-231">The following VBScript sample disables the IP Security on a computer.</span></span> <span data-ttu-id="82f20-232">請注意，基於安全考慮，會將實際的 DisableIPSec 呼叫批註化。</span><span class="sxs-lookup"><span data-stu-id="82f20-232">Note that the actual call to DisableIPSec is commented out, for safety purposes.</span></span>


```VB
strServer = "."

Set objWMI = GetObject("winmgmts:\\" & strServer & "\root\cimv2")

strWQL = "select * from Win32_NetworkAdapterConfiguration"
Set objInstances = objWMI.ExecQuery(strWQL,,48)

For Each objInstance in objInstances

 ' Uncomment next line to disable security
 ' intResult = objInstance.DisableIPSec

Next
```



## <a name="requirements"></a><span data-ttu-id="82f20-233">規格需求</span><span class="sxs-lookup"><span data-stu-id="82f20-233">Requirements</span></span>



| <span data-ttu-id="82f20-234">需求</span><span class="sxs-lookup"><span data-stu-id="82f20-234">Requirement</span></span> | <span data-ttu-id="82f20-235">值</span><span class="sxs-lookup"><span data-stu-id="82f20-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="82f20-236">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="82f20-236">Minimum supported client</span></span><br/> | <span data-ttu-id="82f20-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="82f20-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="82f20-238">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="82f20-238">Minimum supported server</span></span><br/> | <span data-ttu-id="82f20-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82f20-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="82f20-240">命名空間</span><span class="sxs-lookup"><span data-stu-id="82f20-240">Namespace</span></span><br/>                | <span data-ttu-id="82f20-241">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="82f20-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="82f20-242">MOF</span><span class="sxs-lookup"><span data-stu-id="82f20-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82f20-243"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="82f20-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="82f20-244">DLL</span><span class="sxs-lookup"><span data-stu-id="82f20-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82f20-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82f20-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82f20-246">另請參閱</span><span class="sxs-lookup"><span data-stu-id="82f20-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f20-247">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="82f20-247">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="82f20-248">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="82f20-248">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="82f20-249">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="82f20-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="82f20-250">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="82f20-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="82f20-251">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="82f20-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

