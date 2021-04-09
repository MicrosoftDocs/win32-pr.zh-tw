---
description: SetGateways &\# 32;WMI 類別方法會指定閘道清單，以將封包路由傳送至與網路介面卡所連線之子網不同的子網。
ms.assetid: 240f7aff-7a07-4e0d-af30-7bcabb68c736
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetGateways 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetGateways
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 215bfa736a0f9d67ae587ac1f0e1b4aa394b85d9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847390"
---
# <a name="setgateways-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="55b2a-103">Win32 >networkadapterconfiguration 類別的 SetGateways 方法 \_</span><span class="sxs-lookup"><span data-stu-id="55b2a-103">SetGateways method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="55b2a-104">**SetGateways** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會指定閘道清單，以將封包路由傳送至與網路介面卡所連線之子網不同的子網。</span><span class="sxs-lookup"><span data-stu-id="55b2a-104">The **SetGateways** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method specifies a list of gateways for routing packets to a subnet that is different from the subnet that the network adapter is connected to.</span></span>

<span data-ttu-id="55b2a-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="55b2a-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="55b2a-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="55b2a-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="55b2a-107">語法</span><span class="sxs-lookup"><span data-stu-id="55b2a-107">Syntax</span></span>


```mof
uint32 SetGateways(
  [in]           string DefaultIPGateway[],
  [in, optional] uint16 GatewayCostMetric[]
);
```



## <a name="parameters"></a><span data-ttu-id="55b2a-108">參數</span><span class="sxs-lookup"><span data-stu-id="55b2a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="55b2a-109">*DefaultIPGateway* \[在\]</span><span class="sxs-lookup"><span data-stu-id="55b2a-109">*DefaultIPGateway* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-110">路由傳送網路封包之閘道的 IP 位址清單。</span><span class="sxs-lookup"><span data-stu-id="55b2a-110">List of IP addresses to gateways where network packets are routed.</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-111">*GatewayCostMetric* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="55b2a-111">*GatewayCostMetric* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-112">指派範圍從1到9999的值，用來計算最快且最可靠的路由。</span><span class="sxs-lookup"><span data-stu-id="55b2a-112">Assigns a value that ranges from 1 to 9999, which is used to calculate the fastest and most reliable routes.</span></span> <span data-ttu-id="55b2a-113">此參數的值會對應到 *DefaultIPGateway* 參數中的值。</span><span class="sxs-lookup"><span data-stu-id="55b2a-113">The values of this parameter correspond with the values in the *DefaultIPGateway* parameter.</span></span> <span data-ttu-id="55b2a-114">閘道的預設值為1。</span><span class="sxs-lookup"><span data-stu-id="55b2a-114">The default value for a gateway is 1.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="55b2a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="55b2a-115">Return value</span></span>

<span data-ttu-id="55b2a-116">如果不需要重新開機，則傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，以及任何其他值（如果發生錯誤）。</span><span class="sxs-lookup"><span data-stu-id="55b2a-116">Returns a value of 0 (zero) for a successful completion when a reboot is not required, 1 (one) for a successful completion when a reboot is required, and any other value if there is an error.</span></span> <span data-ttu-id="55b2a-117">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="55b2a-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="55b2a-118">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="55b2a-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="55b2a-119">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="55b2a-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-120">0</span><span class="sxs-lookup"><span data-stu-id="55b2a-120">0</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-121">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="55b2a-121">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-122">1</span><span class="sxs-lookup"><span data-stu-id="55b2a-122">1</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-123">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="55b2a-123">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-124">64</span><span class="sxs-lookup"><span data-stu-id="55b2a-124">64</span></span>

<span data-ttu-id="55b2a-125">當 NIC 處於 DHCP 模式時不支援的方法。</span><span class="sxs-lookup"><span data-stu-id="55b2a-125">Method not supported when the NIC is in DHCP mode.</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-126">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="55b2a-126">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-127">65</span><span class="sxs-lookup"><span data-stu-id="55b2a-127">65</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="55b2a-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-129">66</span><span class="sxs-lookup"><span data-stu-id="55b2a-129">66</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-130">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="55b2a-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-131">67</span><span class="sxs-lookup"><span data-stu-id="55b2a-131">67</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-132">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="55b2a-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-133">68</span><span class="sxs-lookup"><span data-stu-id="55b2a-133">68</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-134">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="55b2a-134">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-135">69</span><span class="sxs-lookup"><span data-stu-id="55b2a-135">69</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-136">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="55b2a-136">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-137">70</span><span class="sxs-lookup"><span data-stu-id="55b2a-137">70</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-138">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="55b2a-138">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-139">71</span><span class="sxs-lookup"><span data-stu-id="55b2a-139">71</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-140">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="55b2a-140">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-141">72</span><span class="sxs-lookup"><span data-stu-id="55b2a-141">72</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-142">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="55b2a-142">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-143">73</span><span class="sxs-lookup"><span data-stu-id="55b2a-143">73</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-144">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="55b2a-144">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-145">74</span><span class="sxs-lookup"><span data-stu-id="55b2a-145">74</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-146">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="55b2a-146">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-147">75</span><span class="sxs-lookup"><span data-stu-id="55b2a-147">75</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-148">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="55b2a-148">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-149">76</span><span class="sxs-lookup"><span data-stu-id="55b2a-149">76</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-150">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="55b2a-150">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-151">77</span><span class="sxs-lookup"><span data-stu-id="55b2a-151">77</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-152">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="55b2a-152">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-153">78</span><span class="sxs-lookup"><span data-stu-id="55b2a-153">78</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-154">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="55b2a-154">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-155">79</span><span class="sxs-lookup"><span data-stu-id="55b2a-155">79</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-156">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="55b2a-156">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-157">80</span><span class="sxs-lookup"><span data-stu-id="55b2a-157">80</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-158">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="55b2a-158">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-159">81</span><span class="sxs-lookup"><span data-stu-id="55b2a-159">81</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-160">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="55b2a-160">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-161">82</span><span class="sxs-lookup"><span data-stu-id="55b2a-161">82</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-162">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="55b2a-162">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-163">83</span><span class="sxs-lookup"><span data-stu-id="55b2a-163">83</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-164">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="55b2a-164">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-165">84</span><span class="sxs-lookup"><span data-stu-id="55b2a-165">84</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-166">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="55b2a-166">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-167">85</span><span class="sxs-lookup"><span data-stu-id="55b2a-167">85</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-168">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="55b2a-168">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-169">86</span><span class="sxs-lookup"><span data-stu-id="55b2a-169">86</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-170">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="55b2a-170">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-171">87</span><span class="sxs-lookup"><span data-stu-id="55b2a-171">87</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-172">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="55b2a-172">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-173">88</span><span class="sxs-lookup"><span data-stu-id="55b2a-173">88</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-174">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="55b2a-174">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-175">89</span><span class="sxs-lookup"><span data-stu-id="55b2a-175">89</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-176">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="55b2a-176">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-177">90</span><span class="sxs-lookup"><span data-stu-id="55b2a-177">90</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-178">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="55b2a-178">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-179">91</span><span class="sxs-lookup"><span data-stu-id="55b2a-179">91</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-180">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="55b2a-180">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-181">92</span><span class="sxs-lookup"><span data-stu-id="55b2a-181">92</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-182">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="55b2a-182">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-183">93</span><span class="sxs-lookup"><span data-stu-id="55b2a-183">93</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-184">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="55b2a-184">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-185">94</span><span class="sxs-lookup"><span data-stu-id="55b2a-185">94</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-186">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="55b2a-186">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-187">95</span><span class="sxs-lookup"><span data-stu-id="55b2a-187">95</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-188">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="55b2a-188">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-189">96</span><span class="sxs-lookup"><span data-stu-id="55b2a-189">96</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-190">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="55b2a-190">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-191">97</span><span class="sxs-lookup"><span data-stu-id="55b2a-191">97</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-192">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="55b2a-192">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-193">98</span><span class="sxs-lookup"><span data-stu-id="55b2a-193">98</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-194">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="55b2a-194">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-195">100</span><span class="sxs-lookup"><span data-stu-id="55b2a-195">100</span></span>

</dd> <dt>

<span data-ttu-id="55b2a-196">**其他**</span><span class="sxs-lookup"><span data-stu-id="55b2a-196">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="55b2a-197">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="55b2a-197">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="55b2a-198">備註</span><span class="sxs-lookup"><span data-stu-id="55b2a-198">Remarks</span></span>

<span data-ttu-id="55b2a-199">只有當網路介面卡 (NIC) 處於靜態 IP 模式時，此方法才會運作。</span><span class="sxs-lookup"><span data-stu-id="55b2a-199">This method only works when the Network Interface Card (NIC) is in the static IP mode.</span></span>

<span data-ttu-id="55b2a-200">若要清除閘道，請將您的閘道設定為您在 [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md)上使用的相同 IP。</span><span class="sxs-lookup"><span data-stu-id="55b2a-200">To clear the gateway, set your gateway to the same IP you use on [**EnableStatic**](enablestatic-method-in-class-win32-networkadapterconfiguration.md).</span></span>

## <a name="examples"></a><span data-ttu-id="55b2a-201">範例</span><span class="sxs-lookup"><span data-stu-id="55b2a-201">Examples</span></span>

<span data-ttu-id="55b2a-202">[修改網路介面卡](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f)VBScript 範例的閘道會針對網路介面卡設定兩個閘道。</span><span class="sxs-lookup"><span data-stu-id="55b2a-202">The [Modify the Gateways for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/9ea7670b-f68f-4efb-9cd2-7c299a8f657f) VBScript sample configures two gateways for a network adapter.</span></span>

<span data-ttu-id="55b2a-203">[指派靜態 IP 位址](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a)VBScript 範例會設定電腦的 IP 位址和閘道。</span><span class="sxs-lookup"><span data-stu-id="55b2a-203">The [Assign a Static IP Address](https://Gallery.TechNet.Microsoft.Com/8979c752-8288-4a18-b5ed-f3b79f013f4a) VBScript sample sets the IP address and gateway of a computer.</span></span>

<span data-ttu-id="55b2a-204">[靜態 IP 然後加入網域](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a)PowerShell 範例可協助重建電腦。</span><span class="sxs-lookup"><span data-stu-id="55b2a-204">The [Static IP and then join to a domain](https://Gallery.TechNet.Microsoft.Com/Static-IP-and-then-join-to-130d4b8a) PowerShell sample assists in rebuilding machines.</span></span>

## <a name="requirements"></a><span data-ttu-id="55b2a-205">規格需求</span><span class="sxs-lookup"><span data-stu-id="55b2a-205">Requirements</span></span>



| <span data-ttu-id="55b2a-206">需求</span><span class="sxs-lookup"><span data-stu-id="55b2a-206">Requirement</span></span> | <span data-ttu-id="55b2a-207">值</span><span class="sxs-lookup"><span data-stu-id="55b2a-207">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="55b2a-208">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="55b2a-208">Minimum supported client</span></span><br/> | <span data-ttu-id="55b2a-209">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="55b2a-209">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="55b2a-210">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="55b2a-210">Minimum supported server</span></span><br/> | <span data-ttu-id="55b2a-211">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="55b2a-211">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="55b2a-212">命名空間</span><span class="sxs-lookup"><span data-stu-id="55b2a-212">Namespace</span></span><br/>                | <span data-ttu-id="55b2a-213">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="55b2a-213">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="55b2a-214">MOF</span><span class="sxs-lookup"><span data-stu-id="55b2a-214">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55b2a-215"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="55b2a-215"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="55b2a-216">DLL</span><span class="sxs-lookup"><span data-stu-id="55b2a-216">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b2a-217"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="55b2a-217"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55b2a-218">另請參閱</span><span class="sxs-lookup"><span data-stu-id="55b2a-218">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b2a-219">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="55b2a-219">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="55b2a-220">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="55b2a-220">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="55b2a-221">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="55b2a-221">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="55b2a-222">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="55b2a-222">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="55b2a-223">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="55b2a-223">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

