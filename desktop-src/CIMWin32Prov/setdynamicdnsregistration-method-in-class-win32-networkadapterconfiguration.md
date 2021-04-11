---
description: SetDynamicDNSRegistration 方法會針對此 IP 系結介面卡，指出 IP 位址的動態 DNS 註冊。
ms.assetid: 8e6ca408-3283-40b8-b621-9befdc39b730
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetDynamicDNSRegistration 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDynamicDNSRegistration
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 36818205e356f873b391159293e9204a9ced44a7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847422"
---
# <a name="setdynamicdnsregistration-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="ed331-103">Win32 >networkadapterconfiguration 類別的 SetDynamicDNSRegistration 方法 \_</span><span class="sxs-lookup"><span data-stu-id="ed331-103">SetDynamicDNSRegistration method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="ed331-104">**SetDynamicDNSRegistration** 方法會針對此 ip 系結介面卡，指出 ip 位址的動態 DNS 註冊。</span><span class="sxs-lookup"><span data-stu-id="ed331-104">The **SetDynamicDNSRegistration** method indicates the dynamic DNS registration of IP addresses for this IP-bound adapter.</span></span>

<span data-ttu-id="ed331-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="ed331-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="ed331-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="ed331-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="ed331-107">語法</span><span class="sxs-lookup"><span data-stu-id="ed331-107">Syntax</span></span>


```mof
uint32 SetDynamicDNSRegistration(
  [in]           boolean FullDNSRegistrationEnabled,
  [in, optional] boolean DomainDNSRegistrationEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="ed331-108">參數</span><span class="sxs-lookup"><span data-stu-id="ed331-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed331-109">*FullDNSRegistrationEnabled* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ed331-109">*FullDNSRegistrationEnabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed331-110">若為 **true**，此連線的 IP 位址會在 dns 中，以電腦的完整 dns 名稱註冊。</span><span class="sxs-lookup"><span data-stu-id="ed331-110">If **true**, the IP addresses for this connection is registered in DNS under the computer's full DNS name.</span></span> <span data-ttu-id="ed331-111">電腦的完整 DNS 名稱會顯示在系統主控台的 [ **網路識別** ] 索引標籤上。</span><span class="sxs-lookup"><span data-stu-id="ed331-111">The full DNS name of the computer is displayed on the **Network Identification** tab of the system Control Panel.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-112">*DomainDNSRegistrationEnabled* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ed331-112">*DomainDNSRegistrationEnabled* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ed331-113">若為 **true**，則除了在電腦的完整 DNS 名稱下註冊，此連線的 IP 位址也會在此連線的功能變數名稱下註冊。</span><span class="sxs-lookup"><span data-stu-id="ed331-113">If **true**, the IP addresses for this connection are registered under the domain name of this connection, in addition to being registered under the computer's full DNS name.</span></span> <span data-ttu-id="ed331-114">您可以使用 [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) 或由 DHCP 指派的方法來設定此連線的功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="ed331-114">The domain name of this connection is either set using the method [**SetDNSDomain**](setdnsdomain-method-in-class-win32-networkadapterconfiguration.md) or assigned by DHCP.</span></span> <span data-ttu-id="ed331-115">註冊的名稱是已附加功能變數名稱之電腦的主機名稱。</span><span class="sxs-lookup"><span data-stu-id="ed331-115">The registered name is the host name of the computer with the domain name appended.</span></span> <span data-ttu-id="ed331-116">只有在啟用 *FullDNSRegistrationEnabled* 時，此參數才有意義。</span><span class="sxs-lookup"><span data-stu-id="ed331-116">This parameter has meaning only when *FullDNSRegistrationEnabled* is enabled.</span></span> <span data-ttu-id="ed331-117">預設值為 **false**。</span><span class="sxs-lookup"><span data-stu-id="ed331-117">The default value is **false**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed331-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="ed331-118">Return value</span></span>

<span data-ttu-id="ed331-119">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="ed331-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="ed331-120">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="ed331-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="ed331-121">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="ed331-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="ed331-122">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="ed331-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-123">0</span><span class="sxs-lookup"><span data-stu-id="ed331-123">0</span></span>

<span data-ttu-id="ed331-124">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="ed331-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-125">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="ed331-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-126">1</span><span class="sxs-lookup"><span data-stu-id="ed331-126">1</span></span>

<span data-ttu-id="ed331-127">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="ed331-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-128">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="ed331-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-129">64</span><span class="sxs-lookup"><span data-stu-id="ed331-129">64</span></span>

<span data-ttu-id="ed331-130">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="ed331-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-131">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="ed331-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-132">65</span><span class="sxs-lookup"><span data-stu-id="ed331-132">65</span></span>

<span data-ttu-id="ed331-133">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="ed331-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-134">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="ed331-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-135">66</span><span class="sxs-lookup"><span data-stu-id="ed331-135">66</span></span>

<span data-ttu-id="ed331-136">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="ed331-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-137">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="ed331-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-138">67</span><span class="sxs-lookup"><span data-stu-id="ed331-138">67</span></span>

<span data-ttu-id="ed331-139">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ed331-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-140">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="ed331-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-141">68</span><span class="sxs-lookup"><span data-stu-id="ed331-141">68</span></span>

<span data-ttu-id="ed331-142">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="ed331-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-143">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="ed331-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-144">69</span><span class="sxs-lookup"><span data-stu-id="ed331-144">69</span></span>

<span data-ttu-id="ed331-145">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="ed331-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-146">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="ed331-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-147">70</span><span class="sxs-lookup"><span data-stu-id="ed331-147">70</span></span>

<span data-ttu-id="ed331-148">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="ed331-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-149">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="ed331-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-150">71</span><span class="sxs-lookup"><span data-stu-id="ed331-150">71</span></span>

<span data-ttu-id="ed331-151">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="ed331-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-152">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="ed331-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-153">72</span><span class="sxs-lookup"><span data-stu-id="ed331-153">72</span></span>

<span data-ttu-id="ed331-154">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="ed331-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-155">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="ed331-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-156">73</span><span class="sxs-lookup"><span data-stu-id="ed331-156">73</span></span>

<span data-ttu-id="ed331-157">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="ed331-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-158">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="ed331-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-159">74</span><span class="sxs-lookup"><span data-stu-id="ed331-159">74</span></span>

<span data-ttu-id="ed331-160">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="ed331-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-161">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="ed331-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-162">75</span><span class="sxs-lookup"><span data-stu-id="ed331-162">75</span></span>

<span data-ttu-id="ed331-163">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="ed331-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-164">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="ed331-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-165">76</span><span class="sxs-lookup"><span data-stu-id="ed331-165">76</span></span>

<span data-ttu-id="ed331-166">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="ed331-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-167">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="ed331-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-168">77</span><span class="sxs-lookup"><span data-stu-id="ed331-168">77</span></span>

<span data-ttu-id="ed331-169">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="ed331-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-170">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="ed331-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-171">78</span><span class="sxs-lookup"><span data-stu-id="ed331-171">78</span></span>

<span data-ttu-id="ed331-172">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="ed331-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-173">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="ed331-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-174">79</span><span class="sxs-lookup"><span data-stu-id="ed331-174">79</span></span>

<span data-ttu-id="ed331-175">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="ed331-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-176">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="ed331-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-177">80</span><span class="sxs-lookup"><span data-stu-id="ed331-177">80</span></span>

<span data-ttu-id="ed331-178">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="ed331-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-179">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="ed331-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-180">81</span><span class="sxs-lookup"><span data-stu-id="ed331-180">81</span></span>

<span data-ttu-id="ed331-181">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="ed331-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-182">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="ed331-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-183">82</span><span class="sxs-lookup"><span data-stu-id="ed331-183">82</span></span>

<span data-ttu-id="ed331-184">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="ed331-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-185">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="ed331-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-186">83</span><span class="sxs-lookup"><span data-stu-id="ed331-186">83</span></span>

<span data-ttu-id="ed331-187">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="ed331-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-188">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="ed331-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-189">84</span><span class="sxs-lookup"><span data-stu-id="ed331-189">84</span></span>

<span data-ttu-id="ed331-190">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="ed331-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-191">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="ed331-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-192">85</span><span class="sxs-lookup"><span data-stu-id="ed331-192">85</span></span>

<span data-ttu-id="ed331-193">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="ed331-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-194">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="ed331-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-195">86</span><span class="sxs-lookup"><span data-stu-id="ed331-195">86</span></span>

<span data-ttu-id="ed331-196">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="ed331-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-197">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="ed331-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-198">87</span><span class="sxs-lookup"><span data-stu-id="ed331-198">87</span></span>

<span data-ttu-id="ed331-199">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="ed331-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-200">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="ed331-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-201">88</span><span class="sxs-lookup"><span data-stu-id="ed331-201">88</span></span>

<span data-ttu-id="ed331-202">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="ed331-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-203">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="ed331-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-204">89</span><span class="sxs-lookup"><span data-stu-id="ed331-204">89</span></span>

<span data-ttu-id="ed331-205">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="ed331-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-206">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="ed331-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-207">90</span><span class="sxs-lookup"><span data-stu-id="ed331-207">90</span></span>

<span data-ttu-id="ed331-208">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="ed331-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-209">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="ed331-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-210">91</span><span class="sxs-lookup"><span data-stu-id="ed331-210">91</span></span>

<span data-ttu-id="ed331-211">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="ed331-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-212">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="ed331-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-213">92</span><span class="sxs-lookup"><span data-stu-id="ed331-213">92</span></span>

<span data-ttu-id="ed331-214">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="ed331-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-215">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="ed331-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-216">93</span><span class="sxs-lookup"><span data-stu-id="ed331-216">93</span></span>

<span data-ttu-id="ed331-217">已經存在。</span><span class="sxs-lookup"><span data-stu-id="ed331-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-218">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="ed331-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-219">94</span><span class="sxs-lookup"><span data-stu-id="ed331-219">94</span></span>

<span data-ttu-id="ed331-220">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="ed331-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-221">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="ed331-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-222">95</span><span class="sxs-lookup"><span data-stu-id="ed331-222">95</span></span>

<span data-ttu-id="ed331-223">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="ed331-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-224">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="ed331-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-225">96</span><span class="sxs-lookup"><span data-stu-id="ed331-225">96</span></span>

<span data-ttu-id="ed331-226">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="ed331-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-227">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="ed331-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-228">97</span><span class="sxs-lookup"><span data-stu-id="ed331-228">97</span></span>

<span data-ttu-id="ed331-229">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="ed331-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-230">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="ed331-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-231">98</span><span class="sxs-lookup"><span data-stu-id="ed331-231">98</span></span>

<span data-ttu-id="ed331-232">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="ed331-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-233">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="ed331-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-234">100</span><span class="sxs-lookup"><span data-stu-id="ed331-234">100</span></span>

<span data-ttu-id="ed331-235">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="ed331-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="ed331-236">**其他**</span><span class="sxs-lookup"><span data-stu-id="ed331-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="ed331-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="ed331-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="ed331-238">範例</span><span class="sxs-lookup"><span data-stu-id="ed331-238">Examples</span></span>

<span data-ttu-id="ed331-239">「 [修改網路介面卡的動態 Dns 註冊](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) 」 VBScript 範例會設定網路介面卡的動態 dns 註冊。</span><span class="sxs-lookup"><span data-stu-id="ed331-239">The [Modify Dynamic DNS Registration for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6c72969c-16c8-4bb6-92e9-b9020001759f) VBScript sample configures dynamic DNS registration for a network adapter.</span></span>

<span data-ttu-id="ed331-240">[ [依據 Microsoft 最佳做法設定 ISCSI 網路卡](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) ] 範例會自動執行虛擬機器的設定設定。</span><span class="sxs-lookup"><span data-stu-id="ed331-240">The [Configure iSCSI Network Cards as per Microsoft Best Practices PowerShell](https://Gallery.TechNet.Microsoft.Com/Configure-iSCSI-Network-81232a5e) sample automates the configuration settings for a Virtual Machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed331-241">規格需求</span><span class="sxs-lookup"><span data-stu-id="ed331-241">Requirements</span></span>



| <span data-ttu-id="ed331-242">需求</span><span class="sxs-lookup"><span data-stu-id="ed331-242">Requirement</span></span> | <span data-ttu-id="ed331-243">值</span><span class="sxs-lookup"><span data-stu-id="ed331-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ed331-244">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ed331-244">Minimum supported client</span></span><br/> | <span data-ttu-id="ed331-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ed331-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="ed331-246">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ed331-246">Minimum supported server</span></span><br/> | <span data-ttu-id="ed331-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ed331-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="ed331-248">命名空間</span><span class="sxs-lookup"><span data-stu-id="ed331-248">Namespace</span></span><br/>                | <span data-ttu-id="ed331-249">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="ed331-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="ed331-250">MOF</span><span class="sxs-lookup"><span data-stu-id="ed331-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed331-251"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed331-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed331-252">DLL</span><span class="sxs-lookup"><span data-stu-id="ed331-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed331-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ed331-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed331-254">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ed331-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed331-255">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="ed331-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="ed331-256">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="ed331-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="ed331-257">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="ed331-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="ed331-258">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="ed331-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="ed331-259">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="ed331-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

