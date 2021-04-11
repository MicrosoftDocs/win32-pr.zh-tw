---
description: SetDNSDomain WMI 類別方法允許 DNS 網域的設定。
ms.assetid: a531133e-1b7c-4d85-979d-63bf4f7c9bed
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetDNSDomain 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDNSDomain
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: c440d8cb5c720bf6922707f04bc75e2383755c1e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104190994"
---
# <a name="setdnsdomain-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="54f25-103">Win32 >networkadapterconfiguration 類別的 SetDNSDomain 方法 \_</span><span class="sxs-lookup"><span data-stu-id="54f25-103">SetDNSDomain method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="54f25-104">**SetDNSDomain** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法允許 DNS 網域的設定。</span><span class="sxs-lookup"><span data-stu-id="54f25-104">The **SetDNSDomain** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method allows for the setting of the DNS domain.</span></span>

<span data-ttu-id="54f25-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="54f25-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="54f25-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="54f25-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="54f25-107">語法</span><span class="sxs-lookup"><span data-stu-id="54f25-107">Syntax</span></span>


```mof
uint32 SetDNSDomain(
  [in] string DNSDomain
);
```



## <a name="parameters"></a><span data-ttu-id="54f25-108">參數</span><span class="sxs-lookup"><span data-stu-id="54f25-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="54f25-109">*功能變數名稱* \[在\]</span><span class="sxs-lookup"><span data-stu-id="54f25-109">*DNSDomain* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="54f25-110">與 DNS 相關聯的網域，以組織名稱（後面接著句點和指出組織類型的延伸）表示。</span><span class="sxs-lookup"><span data-stu-id="54f25-110">Domain with which the DNS is associated, represented by an organization name followed by a period and an extension that indicates the type of organization.</span></span>

<span data-ttu-id="54f25-111">範例： "microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="54f25-111">Example: "microsoft.com"</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="54f25-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="54f25-112">Return value</span></span>

<span data-ttu-id="54f25-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則會傳回不同的數位。</span><span class="sxs-lookup"><span data-stu-id="54f25-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required and a different number if there is an error.</span></span> <span data-ttu-id="54f25-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="54f25-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="54f25-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="54f25-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="54f25-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="54f25-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-117">0</span><span class="sxs-lookup"><span data-stu-id="54f25-117">0</span></span>

<span data-ttu-id="54f25-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="54f25-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="54f25-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-120">1</span><span class="sxs-lookup"><span data-stu-id="54f25-120">1</span></span>

<span data-ttu-id="54f25-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="54f25-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="54f25-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-123">64</span><span class="sxs-lookup"><span data-stu-id="54f25-123">64</span></span>

<span data-ttu-id="54f25-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="54f25-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="54f25-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-126">65</span><span class="sxs-lookup"><span data-stu-id="54f25-126">65</span></span>

<span data-ttu-id="54f25-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="54f25-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="54f25-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-129">66</span><span class="sxs-lookup"><span data-stu-id="54f25-129">66</span></span>

<span data-ttu-id="54f25-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="54f25-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="54f25-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-132">67</span><span class="sxs-lookup"><span data-stu-id="54f25-132">67</span></span>

<span data-ttu-id="54f25-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="54f25-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="54f25-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-135">68</span><span class="sxs-lookup"><span data-stu-id="54f25-135">68</span></span>

<span data-ttu-id="54f25-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="54f25-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="54f25-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-138">69</span><span class="sxs-lookup"><span data-stu-id="54f25-138">69</span></span>

<span data-ttu-id="54f25-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="54f25-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="54f25-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-141">70</span><span class="sxs-lookup"><span data-stu-id="54f25-141">70</span></span>

<span data-ttu-id="54f25-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="54f25-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="54f25-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-144">71</span><span class="sxs-lookup"><span data-stu-id="54f25-144">71</span></span>

<span data-ttu-id="54f25-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="54f25-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="54f25-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-147">72</span><span class="sxs-lookup"><span data-stu-id="54f25-147">72</span></span>

<span data-ttu-id="54f25-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="54f25-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="54f25-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-150">73</span><span class="sxs-lookup"><span data-stu-id="54f25-150">73</span></span>

<span data-ttu-id="54f25-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="54f25-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="54f25-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-153">74</span><span class="sxs-lookup"><span data-stu-id="54f25-153">74</span></span>

<span data-ttu-id="54f25-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="54f25-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="54f25-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-156">75</span><span class="sxs-lookup"><span data-stu-id="54f25-156">75</span></span>

<span data-ttu-id="54f25-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="54f25-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="54f25-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-159">76</span><span class="sxs-lookup"><span data-stu-id="54f25-159">76</span></span>

<span data-ttu-id="54f25-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="54f25-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="54f25-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-162">77</span><span class="sxs-lookup"><span data-stu-id="54f25-162">77</span></span>

<span data-ttu-id="54f25-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="54f25-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="54f25-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-165">78</span><span class="sxs-lookup"><span data-stu-id="54f25-165">78</span></span>

<span data-ttu-id="54f25-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="54f25-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="54f25-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-168">79</span><span class="sxs-lookup"><span data-stu-id="54f25-168">79</span></span>

<span data-ttu-id="54f25-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="54f25-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="54f25-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-171">80</span><span class="sxs-lookup"><span data-stu-id="54f25-171">80</span></span>

<span data-ttu-id="54f25-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="54f25-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="54f25-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-174">81</span><span class="sxs-lookup"><span data-stu-id="54f25-174">81</span></span>

<span data-ttu-id="54f25-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="54f25-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="54f25-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-177">82</span><span class="sxs-lookup"><span data-stu-id="54f25-177">82</span></span>

<span data-ttu-id="54f25-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="54f25-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="54f25-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-180">83</span><span class="sxs-lookup"><span data-stu-id="54f25-180">83</span></span>

<span data-ttu-id="54f25-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="54f25-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="54f25-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-183">84</span><span class="sxs-lookup"><span data-stu-id="54f25-183">84</span></span>

<span data-ttu-id="54f25-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="54f25-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="54f25-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-186">85</span><span class="sxs-lookup"><span data-stu-id="54f25-186">85</span></span>

<span data-ttu-id="54f25-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="54f25-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="54f25-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-189">86</span><span class="sxs-lookup"><span data-stu-id="54f25-189">86</span></span>

<span data-ttu-id="54f25-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="54f25-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="54f25-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-192">87</span><span class="sxs-lookup"><span data-stu-id="54f25-192">87</span></span>

<span data-ttu-id="54f25-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="54f25-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="54f25-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-195">88</span><span class="sxs-lookup"><span data-stu-id="54f25-195">88</span></span>

<span data-ttu-id="54f25-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="54f25-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="54f25-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-198">89</span><span class="sxs-lookup"><span data-stu-id="54f25-198">89</span></span>

<span data-ttu-id="54f25-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="54f25-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="54f25-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-201">90</span><span class="sxs-lookup"><span data-stu-id="54f25-201">90</span></span>

<span data-ttu-id="54f25-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="54f25-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="54f25-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-204">91</span><span class="sxs-lookup"><span data-stu-id="54f25-204">91</span></span>

<span data-ttu-id="54f25-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="54f25-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="54f25-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-207">92</span><span class="sxs-lookup"><span data-stu-id="54f25-207">92</span></span>

<span data-ttu-id="54f25-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="54f25-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="54f25-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-210">93</span><span class="sxs-lookup"><span data-stu-id="54f25-210">93</span></span>

<span data-ttu-id="54f25-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="54f25-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="54f25-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-213">94</span><span class="sxs-lookup"><span data-stu-id="54f25-213">94</span></span>

<span data-ttu-id="54f25-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="54f25-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="54f25-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-216">95</span><span class="sxs-lookup"><span data-stu-id="54f25-216">95</span></span>

<span data-ttu-id="54f25-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="54f25-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="54f25-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-219">96</span><span class="sxs-lookup"><span data-stu-id="54f25-219">96</span></span>

<span data-ttu-id="54f25-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="54f25-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="54f25-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-222">97</span><span class="sxs-lookup"><span data-stu-id="54f25-222">97</span></span>

<span data-ttu-id="54f25-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="54f25-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="54f25-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-225">98</span><span class="sxs-lookup"><span data-stu-id="54f25-225">98</span></span>

<span data-ttu-id="54f25-226">並非所有的 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="54f25-226">Not all DHCP leases can be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="54f25-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-228">100</span><span class="sxs-lookup"><span data-stu-id="54f25-228">100</span></span>

<span data-ttu-id="54f25-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="54f25-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="54f25-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="54f25-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="54f25-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="54f25-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="54f25-232">備註</span><span class="sxs-lookup"><span data-stu-id="54f25-232">Remarks</span></span>

<span data-ttu-id="54f25-233">這是每個介面卡上套用的實例相依方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="54f25-233">This is an instance-dependent method call that applies on a per-adapter basis.</span></span> <span data-ttu-id="54f25-234">此設定會套用至目標介面卡。</span><span class="sxs-lookup"><span data-stu-id="54f25-234">The setting applies to the targeted adapter.</span></span>

## <a name="examples"></a><span data-ttu-id="54f25-235">範例</span><span class="sxs-lookup"><span data-stu-id="54f25-235">Examples</span></span>

<span data-ttu-id="54f25-236">TechNet 資源庫上的為 [網路介面卡 VBScript 程式碼範例指派 Dns 網域](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) 使用 **SETDNSDOMAIN** 來設定 tcp/ip 系結網路介面卡的 dns 網域。</span><span class="sxs-lookup"><span data-stu-id="54f25-236">The [Assign the DNS Domain for a Network Adapter](https://Gallery.TechNet.Microsoft.Com/6044a0a4-d320-4c18-a94b-c125796d219b) VBScript code sample on TechNet gallery uses **SetDNSDomain** to set the DNS domain for a TCP/IP-bound network adapter.</span></span>

<span data-ttu-id="54f25-237">在 TechNet 資源庫上 [修改電腦 VBScript 程式](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) 代碼範例的 tcp/ip 設定會使用 **SetDNSDomain** 來修改網路介面卡的 tcp/ip 設定。</span><span class="sxs-lookup"><span data-stu-id="54f25-237">The [Modify the TCP/IP Configuration for a Computer](https://Gallery.TechNet.Microsoft.Com/3d5ae334-1d75-4cea-8079-78c6bd836faf) VBScript code sample on TechNet Gallery uses **SetDNSDomain** to modify TCP/IP settings for a network adapter.</span></span>

<span data-ttu-id="54f25-238">TechNet 資源庫上的電腦 VBScript 範例上的 [啟用 Dhcp 設定](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) ，會使用 **SetDNSDomain** 來設定在電腦上啟用 DHCP 時通常需要的所有設定。</span><span class="sxs-lookup"><span data-stu-id="54f25-238">The [Enable DHCP Settings on a Computer](https://Gallery.TechNet.Microsoft.Com/41e6ab51-78c0-4413-b086-03fde33ea125) VBScript sample on TechNet Gallery uses **SetDNSDomain** to configure all the settings typically required to enable DHCP on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="54f25-239">規格需求</span><span class="sxs-lookup"><span data-stu-id="54f25-239">Requirements</span></span>



| <span data-ttu-id="54f25-240">需求</span><span class="sxs-lookup"><span data-stu-id="54f25-240">Requirement</span></span> | <span data-ttu-id="54f25-241">值</span><span class="sxs-lookup"><span data-stu-id="54f25-241">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="54f25-242">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54f25-242">Minimum supported client</span></span><br/> | <span data-ttu-id="54f25-243">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="54f25-243">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="54f25-244">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54f25-244">Minimum supported server</span></span><br/> | <span data-ttu-id="54f25-245">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="54f25-245">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="54f25-246">命名空間</span><span class="sxs-lookup"><span data-stu-id="54f25-246">Namespace</span></span><br/>                | <span data-ttu-id="54f25-247">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="54f25-247">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="54f25-248">MOF</span><span class="sxs-lookup"><span data-stu-id="54f25-248">MOF</span></span><br/>                      | <dl> <span data-ttu-id="54f25-249"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="54f25-249"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="54f25-250">DLL</span><span class="sxs-lookup"><span data-stu-id="54f25-250">DLL</span></span><br/>                      | <dl> <span data-ttu-id="54f25-251"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="54f25-251"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="54f25-252">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54f25-252">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54f25-253">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="54f25-253">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="54f25-254">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="54f25-254">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="54f25-255">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="54f25-255">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="54f25-256">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="54f25-256">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="54f25-257">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="54f25-257">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

