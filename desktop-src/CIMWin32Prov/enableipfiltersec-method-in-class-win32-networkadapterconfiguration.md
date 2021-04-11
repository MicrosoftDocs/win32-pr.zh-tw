---
description: EnableIPFilterSec WMI 類別靜態方法可用來在所有 IP 系結的網路介面卡上， (IPsec) 全域啟用網際網路通訊協定安全性。
ms.assetid: 565acc18-61e7-473e-b2cc-41f0e8c29193
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 EnableIPFilterSec 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPFilterSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3429e2c2ba78e013da9195961b76ff84ffda9b68
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847211"
---
# <a name="enableipfiltersec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="69aa1-103">Win32 >networkadapterconfiguration 類別的 EnableIPFilterSec 方法 \_</span><span class="sxs-lookup"><span data-stu-id="69aa1-103">EnableIPFilterSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="69aa1-104">**EnableIPFilterSec** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法可用來在所有 IP 系結的網路介面卡上， (IPsec) 全域啟用網際網路通訊協定安全性。</span><span class="sxs-lookup"><span data-stu-id="69aa1-104">The **EnableIPFilterSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Internet Protocol security (IPsec) globally across all IP-bound network adapters.</span></span>

<span data-ttu-id="69aa1-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="69aa1-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="69aa1-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="69aa1-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="69aa1-107">語法</span><span class="sxs-lookup"><span data-stu-id="69aa1-107">Syntax</span></span>


```mof
uint32 EnableIPFilterSec(
  [in] boolean IPFilterSecurityEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="69aa1-108">參數</span><span class="sxs-lookup"><span data-stu-id="69aa1-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69aa1-109">*IPFilterSecurityEnabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="69aa1-109">*IPFilterSecurityEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-110">若 **為 true**，則會在所有 IP 系結的網路介面卡上全域啟用 IPsec。</span><span class="sxs-lookup"><span data-stu-id="69aa1-110">If **true**, IPsec is enabled globally across all IP-bound network adapters.</span></span> <span data-ttu-id="69aa1-111">如果 **為 false**，則表示允許所有埠和通訊協定流量進行未篩選的流程。</span><span class="sxs-lookup"><span data-stu-id="69aa1-111">If **false**, all port and protocol traffic is allowed to flow unfiltered.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="69aa1-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="69aa1-112">Return value</span></span>

<span data-ttu-id="69aa1-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，以及任何其他數位（如果發生錯誤）。</span><span class="sxs-lookup"><span data-stu-id="69aa1-113">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="69aa1-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="69aa1-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="69aa1-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="69aa1-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="69aa1-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="69aa1-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-117">0</span><span class="sxs-lookup"><span data-stu-id="69aa1-117">0</span></span>

<span data-ttu-id="69aa1-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="69aa1-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="69aa1-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-120">1</span><span class="sxs-lookup"><span data-stu-id="69aa1-120">1</span></span>

<span data-ttu-id="69aa1-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="69aa1-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="69aa1-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-123">64</span><span class="sxs-lookup"><span data-stu-id="69aa1-123">64</span></span>

<span data-ttu-id="69aa1-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="69aa1-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="69aa1-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-126">65</span><span class="sxs-lookup"><span data-stu-id="69aa1-126">65</span></span>

<span data-ttu-id="69aa1-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="69aa1-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="69aa1-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-129">66</span><span class="sxs-lookup"><span data-stu-id="69aa1-129">66</span></span>

<span data-ttu-id="69aa1-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="69aa1-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="69aa1-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-132">67</span><span class="sxs-lookup"><span data-stu-id="69aa1-132">67</span></span>

<span data-ttu-id="69aa1-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="69aa1-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="69aa1-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-135">68</span><span class="sxs-lookup"><span data-stu-id="69aa1-135">68</span></span>

<span data-ttu-id="69aa1-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="69aa1-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="69aa1-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-138">69</span><span class="sxs-lookup"><span data-stu-id="69aa1-138">69</span></span>

<span data-ttu-id="69aa1-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="69aa1-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="69aa1-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-141">70</span><span class="sxs-lookup"><span data-stu-id="69aa1-141">70</span></span>

<span data-ttu-id="69aa1-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="69aa1-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="69aa1-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-144">71</span><span class="sxs-lookup"><span data-stu-id="69aa1-144">71</span></span>

<span data-ttu-id="69aa1-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="69aa1-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="69aa1-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-147">72</span><span class="sxs-lookup"><span data-stu-id="69aa1-147">72</span></span>

<span data-ttu-id="69aa1-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="69aa1-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="69aa1-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-150">73</span><span class="sxs-lookup"><span data-stu-id="69aa1-150">73</span></span>

<span data-ttu-id="69aa1-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="69aa1-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="69aa1-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-153">74</span><span class="sxs-lookup"><span data-stu-id="69aa1-153">74</span></span>

<span data-ttu-id="69aa1-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="69aa1-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="69aa1-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-156">75</span><span class="sxs-lookup"><span data-stu-id="69aa1-156">75</span></span>

<span data-ttu-id="69aa1-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="69aa1-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="69aa1-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-159">76</span><span class="sxs-lookup"><span data-stu-id="69aa1-159">76</span></span>

<span data-ttu-id="69aa1-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="69aa1-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="69aa1-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-162">77</span><span class="sxs-lookup"><span data-stu-id="69aa1-162">77</span></span>

<span data-ttu-id="69aa1-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="69aa1-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="69aa1-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-165">78</span><span class="sxs-lookup"><span data-stu-id="69aa1-165">78</span></span>

<span data-ttu-id="69aa1-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="69aa1-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="69aa1-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-168">79</span><span class="sxs-lookup"><span data-stu-id="69aa1-168">79</span></span>

<span data-ttu-id="69aa1-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="69aa1-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="69aa1-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-171">80</span><span class="sxs-lookup"><span data-stu-id="69aa1-171">80</span></span>

<span data-ttu-id="69aa1-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="69aa1-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="69aa1-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-174">81</span><span class="sxs-lookup"><span data-stu-id="69aa1-174">81</span></span>

<span data-ttu-id="69aa1-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="69aa1-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="69aa1-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-177">82</span><span class="sxs-lookup"><span data-stu-id="69aa1-177">82</span></span>

<span data-ttu-id="69aa1-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="69aa1-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="69aa1-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-180">83</span><span class="sxs-lookup"><span data-stu-id="69aa1-180">83</span></span>

<span data-ttu-id="69aa1-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="69aa1-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="69aa1-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-183">84</span><span class="sxs-lookup"><span data-stu-id="69aa1-183">84</span></span>

<span data-ttu-id="69aa1-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="69aa1-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="69aa1-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-186">85</span><span class="sxs-lookup"><span data-stu-id="69aa1-186">85</span></span>

<span data-ttu-id="69aa1-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="69aa1-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="69aa1-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-189">86</span><span class="sxs-lookup"><span data-stu-id="69aa1-189">86</span></span>

<span data-ttu-id="69aa1-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="69aa1-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="69aa1-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-192">87</span><span class="sxs-lookup"><span data-stu-id="69aa1-192">87</span></span>

<span data-ttu-id="69aa1-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="69aa1-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="69aa1-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-195">88</span><span class="sxs-lookup"><span data-stu-id="69aa1-195">88</span></span>

<span data-ttu-id="69aa1-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="69aa1-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="69aa1-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-198">89</span><span class="sxs-lookup"><span data-stu-id="69aa1-198">89</span></span>

<span data-ttu-id="69aa1-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="69aa1-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="69aa1-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-201">90</span><span class="sxs-lookup"><span data-stu-id="69aa1-201">90</span></span>

<span data-ttu-id="69aa1-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="69aa1-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="69aa1-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-204">91</span><span class="sxs-lookup"><span data-stu-id="69aa1-204">91</span></span>

<span data-ttu-id="69aa1-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="69aa1-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="69aa1-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-207">92</span><span class="sxs-lookup"><span data-stu-id="69aa1-207">92</span></span>

<span data-ttu-id="69aa1-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="69aa1-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="69aa1-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-210">93</span><span class="sxs-lookup"><span data-stu-id="69aa1-210">93</span></span>

<span data-ttu-id="69aa1-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="69aa1-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="69aa1-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-213">94</span><span class="sxs-lookup"><span data-stu-id="69aa1-213">94</span></span>

<span data-ttu-id="69aa1-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="69aa1-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="69aa1-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-216">95</span><span class="sxs-lookup"><span data-stu-id="69aa1-216">95</span></span>

<span data-ttu-id="69aa1-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="69aa1-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="69aa1-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-219">96</span><span class="sxs-lookup"><span data-stu-id="69aa1-219">96</span></span>

<span data-ttu-id="69aa1-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="69aa1-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="69aa1-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-222">97</span><span class="sxs-lookup"><span data-stu-id="69aa1-222">97</span></span>

<span data-ttu-id="69aa1-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="69aa1-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="69aa1-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-225">98</span><span class="sxs-lookup"><span data-stu-id="69aa1-225">98</span></span>

<span data-ttu-id="69aa1-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="69aa1-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="69aa1-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-228">100</span><span class="sxs-lookup"><span data-stu-id="69aa1-228">100</span></span>

<span data-ttu-id="69aa1-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="69aa1-229">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="69aa1-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="69aa1-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="69aa1-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="69aa1-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69aa1-232">備註</span><span class="sxs-lookup"><span data-stu-id="69aa1-232">Remarks</span></span>

<span data-ttu-id="69aa1-233">啟用安全性之後，您可以使用網路介面卡專屬的 [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) 方法來控制任何一張網路介面卡的操作安全性特性。</span><span class="sxs-lookup"><span data-stu-id="69aa1-233">With security enabled, the operational security characteristics for any one network adapter can be controlled by using the network adapter-specific [**EnableIPSec**](enableipsec-method-in-class-win32-networkadapterconfiguration.md) method.</span></span>

## <a name="examples"></a><span data-ttu-id="69aa1-234">範例</span><span class="sxs-lookup"><span data-stu-id="69aa1-234">Examples</span></span>

<span data-ttu-id="69aa1-235">下列程式碼取自 TechNet 資源庫上的「 [在所有網路介面卡上啟用 IPFilter 安全性](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) 」範例，可針對安裝在電腦中的所有網路介面卡啟用 IP 篩選安全性。</span><span class="sxs-lookup"><span data-stu-id="69aa1-235">The following code, taken from the [Enable IPFilter Security on All Network Adapters](https://Gallery.TechNet.Microsoft.Com/f8e56021-5a54-4554-b7b6-d76cc40d8d1d) sample on TechNet Gallery, enables IP filter security for all the network adapters installed in a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.EnableIPFilterSec(True)
```



## <a name="requirements"></a><span data-ttu-id="69aa1-236">規格需求</span><span class="sxs-lookup"><span data-stu-id="69aa1-236">Requirements</span></span>



| <span data-ttu-id="69aa1-237">需求</span><span class="sxs-lookup"><span data-stu-id="69aa1-237">Requirement</span></span> | <span data-ttu-id="69aa1-238">值</span><span class="sxs-lookup"><span data-stu-id="69aa1-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69aa1-239">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="69aa1-239">Minimum supported client</span></span><br/> | <span data-ttu-id="69aa1-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="69aa1-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="69aa1-241">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="69aa1-241">Minimum supported server</span></span><br/> | <span data-ttu-id="69aa1-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69aa1-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69aa1-243">命名空間</span><span class="sxs-lookup"><span data-stu-id="69aa1-243">Namespace</span></span><br/>                | <span data-ttu-id="69aa1-244">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="69aa1-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="69aa1-245">MOF</span><span class="sxs-lookup"><span data-stu-id="69aa1-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69aa1-246"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="69aa1-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="69aa1-247">DLL</span><span class="sxs-lookup"><span data-stu-id="69aa1-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69aa1-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69aa1-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69aa1-249">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69aa1-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69aa1-250">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="69aa1-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="69aa1-251">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="69aa1-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="69aa1-252">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="69aa1-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="69aa1-253">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="69aa1-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="69aa1-254">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="69aa1-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

