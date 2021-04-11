---
description: SetPMTUDiscovery WMI 類別靜態方法可用來在遠端主機的路徑上，啟用 (MTU) 探索的最大傳輸單位。
ms.assetid: 43c640bb-c4e7-4b4b-9c18-6cc426229954
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetPMTUDiscovery 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetPMTUDiscovery
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: ef3bc9ad5d6203077275f3665c4b0efc98265fbe
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688959"
---
# <a name="setpmtudiscovery-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="d9c5c-103">Win32 >networkadapterconfiguration 類別的 SetPMTUDiscovery 方法 \_</span><span class="sxs-lookup"><span data-stu-id="d9c5c-103">SetPMTUDiscovery method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="d9c5c-104">**SetPMTUDiscovery** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法可用來在遠端主機的路徑上，啟用 (MTU) 探索的最大傳輸單位。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-104">The **SetPMTUDiscovery** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to enable Maximum Transmission Unit (MTU) discovery over the path to a remote host.</span></span>

<span data-ttu-id="d9c5c-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="d9c5c-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="d9c5c-107">語法</span><span class="sxs-lookup"><span data-stu-id="d9c5c-107">Syntax</span></span>


```mof
uint32 SetPMTUDiscovery(
  [in] boolean PMTUDiscoveryEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="d9c5c-108">參數</span><span class="sxs-lookup"><span data-stu-id="d9c5c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d9c5c-109">*PMTUDiscoveryEnabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d9c5c-109">*PMTUDiscoveryEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-110">若為 **true**，則會啟用 TCP 來嘗試探索遠端主機路徑上 (MTU) 或最大的封包大小的最大傳輸單位。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-110">If **true**, TCP is enabled to attempt to discover the Maximum Transmission Unit (MTU) or largest packet size over the path to a remote host.</span></span> <span data-ttu-id="d9c5c-111">預設值為 **True**。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-111">The default is **true**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d9c5c-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="d9c5c-112">Return value</span></span>

<span data-ttu-id="d9c5c-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="d9c5c-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="d9c5c-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="d9c5c-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-117">0</span><span class="sxs-lookup"><span data-stu-id="d9c5c-117">0</span></span>

<span data-ttu-id="d9c5c-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-120">1</span><span class="sxs-lookup"><span data-stu-id="d9c5c-120">1</span></span>

<span data-ttu-id="d9c5c-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-123">64</span><span class="sxs-lookup"><span data-stu-id="d9c5c-123">64</span></span>

<span data-ttu-id="d9c5c-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-126">65</span><span class="sxs-lookup"><span data-stu-id="d9c5c-126">65</span></span>

<span data-ttu-id="d9c5c-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-129">66</span><span class="sxs-lookup"><span data-stu-id="d9c5c-129">66</span></span>

<span data-ttu-id="d9c5c-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-132">67</span><span class="sxs-lookup"><span data-stu-id="d9c5c-132">67</span></span>

<span data-ttu-id="d9c5c-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-135">68</span><span class="sxs-lookup"><span data-stu-id="d9c5c-135">68</span></span>

<span data-ttu-id="d9c5c-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-138">69</span><span class="sxs-lookup"><span data-stu-id="d9c5c-138">69</span></span>

<span data-ttu-id="d9c5c-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-141">70</span><span class="sxs-lookup"><span data-stu-id="d9c5c-141">70</span></span>

<span data-ttu-id="d9c5c-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-144">71</span><span class="sxs-lookup"><span data-stu-id="d9c5c-144">71</span></span>

<span data-ttu-id="d9c5c-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-147">72</span><span class="sxs-lookup"><span data-stu-id="d9c5c-147">72</span></span>

<span data-ttu-id="d9c5c-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-150">73</span><span class="sxs-lookup"><span data-stu-id="d9c5c-150">73</span></span>

<span data-ttu-id="d9c5c-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-153">74</span><span class="sxs-lookup"><span data-stu-id="d9c5c-153">74</span></span>

<span data-ttu-id="d9c5c-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-156">75</span><span class="sxs-lookup"><span data-stu-id="d9c5c-156">75</span></span>

<span data-ttu-id="d9c5c-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-159">76</span><span class="sxs-lookup"><span data-stu-id="d9c5c-159">76</span></span>

<span data-ttu-id="d9c5c-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-162">77</span><span class="sxs-lookup"><span data-stu-id="d9c5c-162">77</span></span>

<span data-ttu-id="d9c5c-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-165">78</span><span class="sxs-lookup"><span data-stu-id="d9c5c-165">78</span></span>

<span data-ttu-id="d9c5c-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-168">79</span><span class="sxs-lookup"><span data-stu-id="d9c5c-168">79</span></span>

<span data-ttu-id="d9c5c-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-171">80</span><span class="sxs-lookup"><span data-stu-id="d9c5c-171">80</span></span>

<span data-ttu-id="d9c5c-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-174">81</span><span class="sxs-lookup"><span data-stu-id="d9c5c-174">81</span></span>

<span data-ttu-id="d9c5c-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-177">82</span><span class="sxs-lookup"><span data-stu-id="d9c5c-177">82</span></span>

<span data-ttu-id="d9c5c-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-180">83</span><span class="sxs-lookup"><span data-stu-id="d9c5c-180">83</span></span>

<span data-ttu-id="d9c5c-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-183">84</span><span class="sxs-lookup"><span data-stu-id="d9c5c-183">84</span></span>

<span data-ttu-id="d9c5c-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-186">85</span><span class="sxs-lookup"><span data-stu-id="d9c5c-186">85</span></span>

<span data-ttu-id="d9c5c-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-189">86</span><span class="sxs-lookup"><span data-stu-id="d9c5c-189">86</span></span>

<span data-ttu-id="d9c5c-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-192">87</span><span class="sxs-lookup"><span data-stu-id="d9c5c-192">87</span></span>

<span data-ttu-id="d9c5c-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-195">88</span><span class="sxs-lookup"><span data-stu-id="d9c5c-195">88</span></span>

<span data-ttu-id="d9c5c-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-198">89</span><span class="sxs-lookup"><span data-stu-id="d9c5c-198">89</span></span>

<span data-ttu-id="d9c5c-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-201">90</span><span class="sxs-lookup"><span data-stu-id="d9c5c-201">90</span></span>

<span data-ttu-id="d9c5c-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-204">91</span><span class="sxs-lookup"><span data-stu-id="d9c5c-204">91</span></span>

<span data-ttu-id="d9c5c-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-207">92</span><span class="sxs-lookup"><span data-stu-id="d9c5c-207">92</span></span>

<span data-ttu-id="d9c5c-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-210">93</span><span class="sxs-lookup"><span data-stu-id="d9c5c-210">93</span></span>

<span data-ttu-id="d9c5c-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-213">94</span><span class="sxs-lookup"><span data-stu-id="d9c5c-213">94</span></span>

<span data-ttu-id="d9c5c-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-216">95</span><span class="sxs-lookup"><span data-stu-id="d9c5c-216">95</span></span>

<span data-ttu-id="d9c5c-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-219">96</span><span class="sxs-lookup"><span data-stu-id="d9c5c-219">96</span></span>

<span data-ttu-id="d9c5c-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-222">97</span><span class="sxs-lookup"><span data-stu-id="d9c5c-222">97</span></span>

<span data-ttu-id="d9c5c-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-225">98</span><span class="sxs-lookup"><span data-stu-id="d9c5c-225">98</span></span>

<span data-ttu-id="d9c5c-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-228">100</span><span class="sxs-lookup"><span data-stu-id="d9c5c-228">100</span></span>

<span data-ttu-id="d9c5c-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="d9c5c-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="d9c5c-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="d9c5c-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d9c5c-232">備註</span><span class="sxs-lookup"><span data-stu-id="d9c5c-232">Remarks</span></span>

<span data-ttu-id="d9c5c-233">藉由探索路徑 MTU 並將 TCP 區段限制為此大小，TCP 可以在連接具有不同 Mtu 之網路的路徑中，排除路由器上的片段。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-233">By discovering the Path MTU and limiting TCP segments to this size, TCP can eliminate fragmentation at routers along the path that connect networks with different MTUs.</span></span> <span data-ttu-id="d9c5c-234">片段會對 TCP 輸送量和網路擁塞造成負面影響。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-234">Fragmentation adversely affects TCP throughput and network congestion.</span></span> <span data-ttu-id="d9c5c-235">將此參數設定為 **FALSE** ，會將576個位元組的 MTU 用於非本機子網上電腦的所有連接。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-235">Setting this parameter to **FALSE** causes an MTU of 576 bytes to be used for all connections that are not to machines on the local subnet</span></span>

## <a name="examples"></a><span data-ttu-id="d9c5c-236">範例</span><span class="sxs-lookup"><span data-stu-id="d9c5c-236">Examples</span></span>

<span data-ttu-id="d9c5c-237">[ [在所有網路介面卡上啟用 PMTU 探索](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) ] VBScript 範例可讓電腦自動探索網路上的最大傳輸單位。</span><span class="sxs-lookup"><span data-stu-id="d9c5c-237">The [Enable PMTU Discovery on all Network Adapters](https://Gallery.TechNet.Microsoft.Com/dd68dc8d-d452-484c-add7-2da5c87c3568) VBScript sample enables a computer to automatically discover the maximum transmission unit on a network.</span></span>

## <a name="requirements"></a><span data-ttu-id="d9c5c-238">規格需求</span><span class="sxs-lookup"><span data-stu-id="d9c5c-238">Requirements</span></span>



| <span data-ttu-id="d9c5c-239">需求</span><span class="sxs-lookup"><span data-stu-id="d9c5c-239">Requirement</span></span> | <span data-ttu-id="d9c5c-240">值</span><span class="sxs-lookup"><span data-stu-id="d9c5c-240">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d9c5c-241">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d9c5c-241">Minimum supported client</span></span><br/> | <span data-ttu-id="d9c5c-242">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d9c5c-242">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d9c5c-243">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d9c5c-243">Minimum supported server</span></span><br/> | <span data-ttu-id="d9c5c-244">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d9c5c-244">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d9c5c-245">命名空間</span><span class="sxs-lookup"><span data-stu-id="d9c5c-245">Namespace</span></span><br/>                | <span data-ttu-id="d9c5c-246">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="d9c5c-246">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d9c5c-247">MOF</span><span class="sxs-lookup"><span data-stu-id="d9c5c-247">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d9c5c-248"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="d9c5c-248"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d9c5c-249">DLL</span><span class="sxs-lookup"><span data-stu-id="d9c5c-249">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d9c5c-250"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d9c5c-250"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d9c5c-251">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d9c5c-251">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d9c5c-252">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="d9c5c-252">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="d9c5c-253">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="d9c5c-253">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="d9c5c-254">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="d9c5c-254">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="d9c5c-255">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="d9c5c-255">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="d9c5c-256">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="d9c5c-256">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

