---
description: SetTcpipNetbios 方法是用來設定 NetBIOS over TCP/IP 的預設作業。
ms.assetid: 2c639595-da13-400d-b4d0-432b39460554
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetTcpipNetbios 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpipNetbios
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 20ecab5918d00dc5f189464becc0252f2a8c0569
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847595"
---
# <a name="settcpipnetbios-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="3a831-103">Win32 >networkadapterconfiguration 類別的 SetTcpipNetbios 方法 \_</span><span class="sxs-lookup"><span data-stu-id="3a831-103">SetTcpipNetbios method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="3a831-104">**SetTcpipNetbios** 方法是用來設定 NetBIOS over TCP/IP 的預設作業。</span><span class="sxs-lookup"><span data-stu-id="3a831-104">The **SetTcpipNetbios** method is used to set the default operation of NetBIOS over TCP/IP.</span></span>

<span data-ttu-id="3a831-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="3a831-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="3a831-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="3a831-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="3a831-107">語法</span><span class="sxs-lookup"><span data-stu-id="3a831-107">Syntax</span></span>


```mof
uint32 SetTcpipNetbios(
  [in] uint32 TcpipNetbiosOptions
);
```



## <a name="parameters"></a><span data-ttu-id="3a831-108">參數</span><span class="sxs-lookup"><span data-stu-id="3a831-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a831-109">*TcpipNetbiosOptions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3a831-109">*TcpipNetbiosOptions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3a831-110">值，指定與 NetBIOS over TCP/IP 相關的可能設定。</span><span class="sxs-lookup"><span data-stu-id="3a831-110">Value that specifies the possible settings related to NetBIOS over TCP/IP.</span></span>

<dt>

<span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>

<span data-ttu-id="3a831-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0) </span><span class="sxs-lookup"><span data-stu-id="3a831-111"><span id="EnableNetbiosViaDhcp"></span><span id="enablenetbiosviadhcp"></span><span id="ENABLENETBIOSVIADHCP"></span>**EnableNetbiosViaDhcp** (0)</span></span>


</dt> <dd>

<span data-ttu-id="3a831-112">透過 DHCP 啟用 Netbios</span><span class="sxs-lookup"><span data-stu-id="3a831-112">Enable Netbios via DHCP</span></span>

</dd> <dt>

<span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>

<span data-ttu-id="3a831-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1) </span><span class="sxs-lookup"><span data-stu-id="3a831-113"><span id="EnableNetbios"></span><span id="enablenetbios"></span><span id="ENABLENETBIOS"></span>**EnableNetbios** (1)</span></span>


</dt> <dd>

<span data-ttu-id="3a831-114">啟用 Netbios</span><span class="sxs-lookup"><span data-stu-id="3a831-114">Enable Netbios</span></span>

</dd> <dt>

<span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>

<span data-ttu-id="3a831-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2) </span><span class="sxs-lookup"><span data-stu-id="3a831-115"><span id="DisableNetbios"></span><span id="disablenetbios"></span><span id="DISABLENETBIOS"></span>**DisableNetbios** (2)</span></span>


</dt> <dd>

<span data-ttu-id="3a831-116">停用 Netbios</span><span class="sxs-lookup"><span data-stu-id="3a831-116">Disable Netbios</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a831-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="3a831-117">Return value</span></span>

<span data-ttu-id="3a831-118">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="3a831-118">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="3a831-119">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="3a831-119">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="3a831-120">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="3a831-120">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="3a831-121">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="3a831-121">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-122">0</span><span class="sxs-lookup"><span data-stu-id="3a831-122">0</span></span>

<span data-ttu-id="3a831-123">順利完成。</span><span class="sxs-lookup"><span data-stu-id="3a831-123">Successful completion.</span></span> <span data-ttu-id="3a831-124">不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="3a831-124">No reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-125">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="3a831-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-126">1</span><span class="sxs-lookup"><span data-stu-id="3a831-126">1</span></span>

<span data-ttu-id="3a831-127">順利完成。</span><span class="sxs-lookup"><span data-stu-id="3a831-127">Successful completion.</span></span> <span data-ttu-id="3a831-128">需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="3a831-128">Reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-129">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="3a831-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-130">64</span><span class="sxs-lookup"><span data-stu-id="3a831-130">64</span></span>

<span data-ttu-id="3a831-131">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="3a831-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-132">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="3a831-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-133">65</span><span class="sxs-lookup"><span data-stu-id="3a831-133">65</span></span>

<span data-ttu-id="3a831-134">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="3a831-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-135">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="3a831-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-136">66</span><span class="sxs-lookup"><span data-stu-id="3a831-136">66</span></span>

<span data-ttu-id="3a831-137">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="3a831-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-138">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="3a831-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-139">67</span><span class="sxs-lookup"><span data-stu-id="3a831-139">67</span></span>

<span data-ttu-id="3a831-140">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a831-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-141">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="3a831-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-142">68</span><span class="sxs-lookup"><span data-stu-id="3a831-142">68</span></span>

<span data-ttu-id="3a831-143">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="3a831-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-144">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="3a831-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-145">69</span><span class="sxs-lookup"><span data-stu-id="3a831-145">69</span></span>

<span data-ttu-id="3a831-146">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="3a831-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-147">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="3a831-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-148">70</span><span class="sxs-lookup"><span data-stu-id="3a831-148">70</span></span>

<span data-ttu-id="3a831-149">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="3a831-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-150">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="3a831-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-151">71</span><span class="sxs-lookup"><span data-stu-id="3a831-151">71</span></span>

<span data-ttu-id="3a831-152">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="3a831-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-153">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="3a831-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-154">72</span><span class="sxs-lookup"><span data-stu-id="3a831-154">72</span></span>

<span data-ttu-id="3a831-155">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a831-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-156">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="3a831-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-157">73</span><span class="sxs-lookup"><span data-stu-id="3a831-157">73</span></span>

<span data-ttu-id="3a831-158">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="3a831-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-159">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="3a831-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-160">74</span><span class="sxs-lookup"><span data-stu-id="3a831-160">74</span></span>

<span data-ttu-id="3a831-161">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="3a831-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-162">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="3a831-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-163">75</span><span class="sxs-lookup"><span data-stu-id="3a831-163">75</span></span>

<span data-ttu-id="3a831-164">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="3a831-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-165">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="3a831-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-166">76</span><span class="sxs-lookup"><span data-stu-id="3a831-166">76</span></span>

<span data-ttu-id="3a831-167">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="3a831-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-168">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="3a831-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-169">77</span><span class="sxs-lookup"><span data-stu-id="3a831-169">77</span></span>

<span data-ttu-id="3a831-170">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="3a831-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-171">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="3a831-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-172">78</span><span class="sxs-lookup"><span data-stu-id="3a831-172">78</span></span>

<span data-ttu-id="3a831-173">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="3a831-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-174">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="3a831-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-175">79</span><span class="sxs-lookup"><span data-stu-id="3a831-175">79</span></span>

<span data-ttu-id="3a831-176">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="3a831-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-177">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="3a831-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-178">80</span><span class="sxs-lookup"><span data-stu-id="3a831-178">80</span></span>

<span data-ttu-id="3a831-179">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="3a831-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-180">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="3a831-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-181">81</span><span class="sxs-lookup"><span data-stu-id="3a831-181">81</span></span>

<span data-ttu-id="3a831-182">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="3a831-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-183">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="3a831-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-184">82</span><span class="sxs-lookup"><span data-stu-id="3a831-184">82</span></span>

<span data-ttu-id="3a831-185">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="3a831-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-186">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="3a831-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-187">83</span><span class="sxs-lookup"><span data-stu-id="3a831-187">83</span></span>

<span data-ttu-id="3a831-188">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="3a831-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-189">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="3a831-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-190">84</span><span class="sxs-lookup"><span data-stu-id="3a831-190">84</span></span>

<span data-ttu-id="3a831-191">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="3a831-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-192">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="3a831-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-193">85</span><span class="sxs-lookup"><span data-stu-id="3a831-193">85</span></span>

<span data-ttu-id="3a831-194">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="3a831-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-195">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="3a831-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-196">86</span><span class="sxs-lookup"><span data-stu-id="3a831-196">86</span></span>

<span data-ttu-id="3a831-197">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="3a831-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-198">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="3a831-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-199">87</span><span class="sxs-lookup"><span data-stu-id="3a831-199">87</span></span>

<span data-ttu-id="3a831-200">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="3a831-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-201">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="3a831-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-202">88</span><span class="sxs-lookup"><span data-stu-id="3a831-202">88</span></span>

<span data-ttu-id="3a831-203">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="3a831-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-204">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="3a831-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-205">89</span><span class="sxs-lookup"><span data-stu-id="3a831-205">89</span></span>

<span data-ttu-id="3a831-206">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="3a831-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-207">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="3a831-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-208">90</span><span class="sxs-lookup"><span data-stu-id="3a831-208">90</span></span>

<span data-ttu-id="3a831-209">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="3a831-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-210">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="3a831-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-211">91</span><span class="sxs-lookup"><span data-stu-id="3a831-211">91</span></span>

<span data-ttu-id="3a831-212">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="3a831-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-213">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="3a831-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-214">92</span><span class="sxs-lookup"><span data-stu-id="3a831-214">92</span></span>

<span data-ttu-id="3a831-215">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="3a831-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-216">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="3a831-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-217">93</span><span class="sxs-lookup"><span data-stu-id="3a831-217">93</span></span>

<span data-ttu-id="3a831-218">已經存在。</span><span class="sxs-lookup"><span data-stu-id="3a831-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-219">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="3a831-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-220">94</span><span class="sxs-lookup"><span data-stu-id="3a831-220">94</span></span>

<span data-ttu-id="3a831-221">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="3a831-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-222">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="3a831-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-223">95</span><span class="sxs-lookup"><span data-stu-id="3a831-223">95</span></span>

<span data-ttu-id="3a831-224">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="3a831-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-225">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="3a831-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-226">96</span><span class="sxs-lookup"><span data-stu-id="3a831-226">96</span></span>

<span data-ttu-id="3a831-227">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="3a831-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-228">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="3a831-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-229">97</span><span class="sxs-lookup"><span data-stu-id="3a831-229">97</span></span>

<span data-ttu-id="3a831-230">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="3a831-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-231">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="3a831-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-232">98</span><span class="sxs-lookup"><span data-stu-id="3a831-232">98</span></span>

<span data-ttu-id="3a831-233">並非所有的 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="3a831-233">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-234">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="3a831-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-235">100</span><span class="sxs-lookup"><span data-stu-id="3a831-235">100</span></span>

<span data-ttu-id="3a831-236">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="3a831-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="3a831-237">**其他**</span><span class="sxs-lookup"><span data-stu-id="3a831-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="3a831-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="3a831-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="3a831-239">範例</span><span class="sxs-lookup"><span data-stu-id="3a831-239">Examples</span></span>

<span data-ttu-id="3a831-240">在 [網路介面卡上修改 Netbios 使用](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) VBScript 範例會啟用網路介面卡的 netbios。</span><span class="sxs-lookup"><span data-stu-id="3a831-240">The [Modify NetBIOS Use on a Network Adapter](https://Gallery.TechNet.Microsoft.Com/01d541f7-5c0d-46d3-8619-28aaab154dc0) VBScript sample enables NetBIOS for a network adapter.</span></span>

<span data-ttu-id="3a831-241">[ [依據 Microsoft 最佳做法設定 ISCSI 網路卡](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) ] 範例會自動執行虛擬機器的設定設定。</span><span class="sxs-lookup"><span data-stu-id="3a831-241">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a831-242">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a831-242">Requirements</span></span>



| <span data-ttu-id="3a831-243">需求</span><span class="sxs-lookup"><span data-stu-id="3a831-243">Requirement</span></span> | <span data-ttu-id="3a831-244">值</span><span class="sxs-lookup"><span data-stu-id="3a831-244">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3a831-245">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a831-245">Minimum supported client</span></span><br/> | <span data-ttu-id="3a831-246">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3a831-246">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3a831-247">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a831-247">Minimum supported server</span></span><br/> | <span data-ttu-id="3a831-248">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a831-248">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3a831-249">命名空間</span><span class="sxs-lookup"><span data-stu-id="3a831-249">Namespace</span></span><br/>                | <span data-ttu-id="3a831-250">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="3a831-250">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3a831-251">MOF</span><span class="sxs-lookup"><span data-stu-id="3a831-251">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a831-252"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="3a831-252"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a831-253">DLL</span><span class="sxs-lookup"><span data-stu-id="3a831-253">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a831-254"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a831-254"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a831-255">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a831-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a831-256">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="3a831-256">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="3a831-257">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="3a831-257">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="3a831-258">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="3a831-258">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="3a831-259">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="3a831-259">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="3a831-260">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="3a831-260">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

