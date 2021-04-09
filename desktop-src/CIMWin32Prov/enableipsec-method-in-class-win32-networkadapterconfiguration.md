---
description: EnableIPSec&\# 8194;WMI 類別方法會在啟用 TCP/IP 的網路介面卡上啟用網際網路通訊協定安全性 (IPsec) 。
ms.assetid: 0a45d864-606d-4adb-9b51-62d46a0d68b1
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 EnableIPSec 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.EnableIPSec
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 6988d68f9939752e3c8c2c9ace063b895a2d3720
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847210"
---
# <a name="enableipsec-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="38c6e-103">Win32 >networkadapterconfiguration 類別的 EnableIPSec 方法 \_</span><span class="sxs-lookup"><span data-stu-id="38c6e-103">EnableIPSec method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="38c6e-104">**EnableIPSec** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會在啟用 tcp/ip 的網路介面卡上啟用網際網路通訊協定安全性 (IPsec) 。</span><span class="sxs-lookup"><span data-stu-id="38c6e-104">The **EnableIPSec** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method enables Internet Protocol security (IPsec) on a TCP/IP-enabled network adapter.</span></span>

<span data-ttu-id="38c6e-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="38c6e-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="38c6e-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="38c6e-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="38c6e-107">語法</span><span class="sxs-lookup"><span data-stu-id="38c6e-107">Syntax</span></span>


```mof
uint32 EnableIPSec(
  [in] string IPSecPermitTCPPorts[],
  [in] string IPSecPermitUDPPorts[],
  [in] string IPSecPermitIPProtocols[]
);
```



## <a name="parameters"></a><span data-ttu-id="38c6e-108">參數</span><span class="sxs-lookup"><span data-stu-id="38c6e-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38c6e-109">*IPSecPermitTCPPorts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38c6e-109">*IPSecPermitTCPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-110">要授與 TCP 之存取權限的埠清單。</span><span class="sxs-lookup"><span data-stu-id="38c6e-110">List of ports to be granted access permission for TCP.</span></span> <span data-ttu-id="38c6e-111">數值 0 (零) 表示授與所有埠的存取權限。</span><span class="sxs-lookup"><span data-stu-id="38c6e-111">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="38c6e-112">空的陣列指出沒有任何埠可被授與存取權限。</span><span class="sxs-lookup"><span data-stu-id="38c6e-112">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-113">*IPSecPermitUDPPorts* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38c6e-113">*IPSecPermitUDPPorts* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-114">要授與 UDP 存取權的埠清單。</span><span class="sxs-lookup"><span data-stu-id="38c6e-114">List of ports to be granted access permission for UDP.</span></span> <span data-ttu-id="38c6e-115">數值 0 (零) 表示授與所有埠的存取權限。</span><span class="sxs-lookup"><span data-stu-id="38c6e-115">A numeric value of 0 (zero) indicates access permission is granted for all ports.</span></span> <span data-ttu-id="38c6e-116">空的陣列指出沒有任何埠可被授與存取權限。</span><span class="sxs-lookup"><span data-stu-id="38c6e-116">An empty array indicates that no ports are to be granted access permission.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-117">*IPSecPermitIPProtocols* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38c6e-117">*IPSecPermitIPProtocols* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-118">允許透過 IP 執行的通訊協定清單。</span><span class="sxs-lookup"><span data-stu-id="38c6e-118">List of protocols permitted to run over the IP.</span></span> <span data-ttu-id="38c6e-119">數值 0 (零) 表示授與所有通訊協定的存取權限。</span><span class="sxs-lookup"><span data-stu-id="38c6e-119">A numeric value of 0 (zero) indicates access permission is granted for all protocols.</span></span> <span data-ttu-id="38c6e-120">空陣列指出沒有任何通訊協定被授與存取權限。</span><span class="sxs-lookup"><span data-stu-id="38c6e-120">An empty array indicates that no protocols are granted access permission.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38c6e-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="38c6e-121">Return value</span></span>

<span data-ttu-id="38c6e-122">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，以及任何其他數位（如果發生錯誤）。</span><span class="sxs-lookup"><span data-stu-id="38c6e-122">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other number if there is an error.</span></span> <span data-ttu-id="38c6e-123">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="38c6e-123">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="38c6e-124">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="38c6e-124">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="38c6e-125">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="38c6e-125">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-126">0</span><span class="sxs-lookup"><span data-stu-id="38c6e-126">0</span></span>

<span data-ttu-id="38c6e-127">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="38c6e-127">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-128">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="38c6e-128">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-129">1</span><span class="sxs-lookup"><span data-stu-id="38c6e-129">1</span></span>

<span data-ttu-id="38c6e-130">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="38c6e-130">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-131">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="38c6e-131">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-132">64</span><span class="sxs-lookup"><span data-stu-id="38c6e-132">64</span></span>

<span data-ttu-id="38c6e-133">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="38c6e-133">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-134">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="38c6e-134">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-135">65</span><span class="sxs-lookup"><span data-stu-id="38c6e-135">65</span></span>

<span data-ttu-id="38c6e-136">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="38c6e-136">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-137">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="38c6e-137">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-138">66</span><span class="sxs-lookup"><span data-stu-id="38c6e-138">66</span></span>

<span data-ttu-id="38c6e-139">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="38c6e-139">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-140">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="38c6e-140">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-141">67</span><span class="sxs-lookup"><span data-stu-id="38c6e-141">67</span></span>

<span data-ttu-id="38c6e-142">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="38c6e-142">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-143">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="38c6e-143">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-144">68</span><span class="sxs-lookup"><span data-stu-id="38c6e-144">68</span></span>

<span data-ttu-id="38c6e-145">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="38c6e-145">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-146">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="38c6e-146">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-147">69</span><span class="sxs-lookup"><span data-stu-id="38c6e-147">69</span></span>

<span data-ttu-id="38c6e-148">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="38c6e-148">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-149">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="38c6e-149">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-150">70</span><span class="sxs-lookup"><span data-stu-id="38c6e-150">70</span></span>

<span data-ttu-id="38c6e-151">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="38c6e-151">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-152">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="38c6e-152">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-153">71</span><span class="sxs-lookup"><span data-stu-id="38c6e-153">71</span></span>

<span data-ttu-id="38c6e-154">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="38c6e-154">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-155">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="38c6e-155">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-156">72</span><span class="sxs-lookup"><span data-stu-id="38c6e-156">72</span></span>

<span data-ttu-id="38c6e-157">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="38c6e-157">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-158">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="38c6e-158">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-159">73</span><span class="sxs-lookup"><span data-stu-id="38c6e-159">73</span></span>

<span data-ttu-id="38c6e-160">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="38c6e-160">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-161">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="38c6e-161">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-162">74</span><span class="sxs-lookup"><span data-stu-id="38c6e-162">74</span></span>

<span data-ttu-id="38c6e-163">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="38c6e-163">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-164">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="38c6e-164">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-165">75</span><span class="sxs-lookup"><span data-stu-id="38c6e-165">75</span></span>

<span data-ttu-id="38c6e-166">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="38c6e-166">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-167">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="38c6e-167">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-168">76</span><span class="sxs-lookup"><span data-stu-id="38c6e-168">76</span></span>

<span data-ttu-id="38c6e-169">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="38c6e-169">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-170">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="38c6e-170">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-171">77</span><span class="sxs-lookup"><span data-stu-id="38c6e-171">77</span></span>

<span data-ttu-id="38c6e-172">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="38c6e-172">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-173">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="38c6e-173">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-174">78</span><span class="sxs-lookup"><span data-stu-id="38c6e-174">78</span></span>

<span data-ttu-id="38c6e-175">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="38c6e-175">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-176">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="38c6e-176">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-177">79</span><span class="sxs-lookup"><span data-stu-id="38c6e-177">79</span></span>

<span data-ttu-id="38c6e-178">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="38c6e-178">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-179">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="38c6e-179">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-180">80</span><span class="sxs-lookup"><span data-stu-id="38c6e-180">80</span></span>

<span data-ttu-id="38c6e-181">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="38c6e-181">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-182">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="38c6e-182">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-183">81</span><span class="sxs-lookup"><span data-stu-id="38c6e-183">81</span></span>

<span data-ttu-id="38c6e-184">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="38c6e-184">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-185">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="38c6e-185">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-186">82</span><span class="sxs-lookup"><span data-stu-id="38c6e-186">82</span></span>

<span data-ttu-id="38c6e-187">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="38c6e-187">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-188">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="38c6e-188">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-189">83</span><span class="sxs-lookup"><span data-stu-id="38c6e-189">83</span></span>

<span data-ttu-id="38c6e-190">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="38c6e-190">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-191">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="38c6e-191">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-192">84</span><span class="sxs-lookup"><span data-stu-id="38c6e-192">84</span></span>

<span data-ttu-id="38c6e-193">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="38c6e-193">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-194">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="38c6e-194">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-195">85</span><span class="sxs-lookup"><span data-stu-id="38c6e-195">85</span></span>

<span data-ttu-id="38c6e-196">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="38c6e-196">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-197">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="38c6e-197">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-198">86</span><span class="sxs-lookup"><span data-stu-id="38c6e-198">86</span></span>

<span data-ttu-id="38c6e-199">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="38c6e-199">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-200">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="38c6e-200">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-201">87</span><span class="sxs-lookup"><span data-stu-id="38c6e-201">87</span></span>

<span data-ttu-id="38c6e-202">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="38c6e-202">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-203">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="38c6e-203">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-204">88</span><span class="sxs-lookup"><span data-stu-id="38c6e-204">88</span></span>

<span data-ttu-id="38c6e-205">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="38c6e-205">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-206">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="38c6e-206">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-207">89</span><span class="sxs-lookup"><span data-stu-id="38c6e-207">89</span></span>

<span data-ttu-id="38c6e-208">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="38c6e-208">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-209">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="38c6e-209">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-210">90</span><span class="sxs-lookup"><span data-stu-id="38c6e-210">90</span></span>

<span data-ttu-id="38c6e-211">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="38c6e-211">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-212">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="38c6e-212">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-213">91</span><span class="sxs-lookup"><span data-stu-id="38c6e-213">91</span></span>

<span data-ttu-id="38c6e-214">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="38c6e-214">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-215">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="38c6e-215">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-216">92</span><span class="sxs-lookup"><span data-stu-id="38c6e-216">92</span></span>

<span data-ttu-id="38c6e-217">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="38c6e-217">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-218">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="38c6e-218">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-219">93</span><span class="sxs-lookup"><span data-stu-id="38c6e-219">93</span></span>

<span data-ttu-id="38c6e-220">已經存在。</span><span class="sxs-lookup"><span data-stu-id="38c6e-220">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-221">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="38c6e-221">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-222">94</span><span class="sxs-lookup"><span data-stu-id="38c6e-222">94</span></span>

<span data-ttu-id="38c6e-223">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="38c6e-223">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-224">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="38c6e-224">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-225">95</span><span class="sxs-lookup"><span data-stu-id="38c6e-225">95</span></span>

<span data-ttu-id="38c6e-226">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="38c6e-226">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-227">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="38c6e-227">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-228">96</span><span class="sxs-lookup"><span data-stu-id="38c6e-228">96</span></span>

<span data-ttu-id="38c6e-229">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="38c6e-229">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-230">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="38c6e-230">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-231">97</span><span class="sxs-lookup"><span data-stu-id="38c6e-231">97</span></span>

<span data-ttu-id="38c6e-232">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="38c6e-232">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-233">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="38c6e-233">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-234">98</span><span class="sxs-lookup"><span data-stu-id="38c6e-234">98</span></span>

<span data-ttu-id="38c6e-235">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="38c6e-235">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-236">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="38c6e-236">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-237">100</span><span class="sxs-lookup"><span data-stu-id="38c6e-237">100</span></span>

<span data-ttu-id="38c6e-238">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="38c6e-238">DHCP not enabled on the adapter.</span></span>

</dd> <dt>

<span data-ttu-id="38c6e-239">**其他**</span><span class="sxs-lookup"><span data-stu-id="38c6e-239">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="38c6e-240">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="38c6e-240">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="38c6e-241">備註</span><span class="sxs-lookup"><span data-stu-id="38c6e-241">Remarks</span></span>

<span data-ttu-id="38c6e-242">只有當 [**Win32 \_ >networkadapterconfiguration**](win32-networkadapterconfiguration.md)中的 **IPFilterSecurityEnabled** 屬性為 **true** 時，才會保護埠。</span><span class="sxs-lookup"><span data-stu-id="38c6e-242">Ports are secured only when the **IPFilterSecurityEnabled** property in [**Win32\_NetworkAdapterConfiguration**](win32-networkadapterconfiguration.md) is **true**.</span></span>

## <a name="examples"></a><span data-ttu-id="38c6e-243">範例</span><span class="sxs-lookup"><span data-stu-id="38c6e-243">Examples</span></span>

<span data-ttu-id="38c6e-244">TechNet 資源庫上的「在 [網路介面卡上啟用 IPSec](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) 」 VBScript 範例會使用 **EnableIPSec** 來啟用網路介面卡的 IP 安全性。</span><span class="sxs-lookup"><span data-stu-id="38c6e-244">The [Enable IPSec on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/ff821218-c392-42fb-a77c-c3eab899587c) VBScript sample, on TechNet Gallery, uses **EnableIPSec** to enable IP security for a network adapter.</span></span>

## <a name="requirements"></a><span data-ttu-id="38c6e-245">規格需求</span><span class="sxs-lookup"><span data-stu-id="38c6e-245">Requirements</span></span>



| <span data-ttu-id="38c6e-246">需求</span><span class="sxs-lookup"><span data-stu-id="38c6e-246">Requirement</span></span> | <span data-ttu-id="38c6e-247">值</span><span class="sxs-lookup"><span data-stu-id="38c6e-247">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38c6e-248">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38c6e-248">Minimum supported client</span></span><br/> | <span data-ttu-id="38c6e-249">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="38c6e-249">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="38c6e-250">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38c6e-250">Minimum supported server</span></span><br/> | <span data-ttu-id="38c6e-251">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="38c6e-251">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="38c6e-252">命名空間</span><span class="sxs-lookup"><span data-stu-id="38c6e-252">Namespace</span></span><br/>                | <span data-ttu-id="38c6e-253">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="38c6e-253">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="38c6e-254">MOF</span><span class="sxs-lookup"><span data-stu-id="38c6e-254">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38c6e-255"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="38c6e-255"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="38c6e-256">DLL</span><span class="sxs-lookup"><span data-stu-id="38c6e-256">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38c6e-257"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38c6e-257"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38c6e-258">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38c6e-258">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38c6e-259">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="38c6e-259">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="38c6e-260">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="38c6e-260">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="38c6e-261">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="38c6e-261">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="38c6e-262">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="38c6e-262">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="38c6e-263">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="38c6e-263">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

