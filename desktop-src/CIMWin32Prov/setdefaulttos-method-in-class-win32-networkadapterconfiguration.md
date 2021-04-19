---
description: 這個方法已過時。 應用程式應該使用服務品質 (QoS) API 來管理服務的類型 (TOS) 位。
ms.assetid: 18860c13-7324-4a37-b83c-f3d15c425acb
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetDefaultTOS 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTOS
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5df55ff88c87047a48a84a122c8e58c8148a7cff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970342"
---
# <a name="setdefaulttos-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="16c5b-104">Win32 >networkadapterconfiguration 類別的 SetDefaultTOS 方法 \_</span><span class="sxs-lookup"><span data-stu-id="16c5b-104">SetDefaultTOS method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="16c5b-105">這個方法已過時。</span><span class="sxs-lookup"><span data-stu-id="16c5b-105">This method is obsolete.</span></span> <span data-ttu-id="16c5b-106">應用程式應該使用服務品質 (QoS) API 來管理服務的類型 (TOS) 位。</span><span class="sxs-lookup"><span data-stu-id="16c5b-106">Applications should use the Quality of Service (QoS) API to manipulate Type of Service (TOS) bits.</span></span> <span data-ttu-id="16c5b-107">如需詳細資訊，請參閱 [服務品質](/previous-versions/windows/desktop/qos/qos-start-page)。</span><span class="sxs-lookup"><span data-stu-id="16c5b-107">For more information, see [Quality of Service](/previous-versions/windows/desktop/qos/qos-start-page).</span></span>

<span data-ttu-id="16c5b-108">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="16c5b-108">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="16c5b-109">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="16c5b-109">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="16c5b-110">語法</span><span class="sxs-lookup"><span data-stu-id="16c5b-110">Syntax</span></span>


```mof
uint32 SetDefaultTOS(
  [in] uint8 DefaultTOS
);
```



## <a name="parameters"></a><span data-ttu-id="16c5b-111">參數</span><span class="sxs-lookup"><span data-stu-id="16c5b-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="16c5b-112">*DefaultTOS* \[在\]</span><span class="sxs-lookup"><span data-stu-id="16c5b-112">*DefaultTOS* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-113">服務類型 (TOS) 值放在連出 IP 封包的標頭中。</span><span class="sxs-lookup"><span data-stu-id="16c5b-113">Type of Service (TOS) value put in the header of outgoing IP packets.</span></span> <span data-ttu-id="16c5b-114">如需值的定義，請參閱 RFC 791。</span><span class="sxs-lookup"><span data-stu-id="16c5b-114">For a definition of the values, see RFC 791.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="16c5b-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="16c5b-115">Return value</span></span>

<span data-ttu-id="16c5b-116">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="16c5b-116">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="16c5b-117">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="16c5b-117">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="16c5b-118">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="16c5b-118">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="16c5b-119">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="16c5b-119">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-120">0</span><span class="sxs-lookup"><span data-stu-id="16c5b-120">0</span></span>

<span data-ttu-id="16c5b-121">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="16c5b-121">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-122">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="16c5b-122">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-123">1</span><span class="sxs-lookup"><span data-stu-id="16c5b-123">1</span></span>

<span data-ttu-id="16c5b-124">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="16c5b-124">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-125">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="16c5b-125">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-126">64</span><span class="sxs-lookup"><span data-stu-id="16c5b-126">64</span></span>

<span data-ttu-id="16c5b-127">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="16c5b-127">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-128">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="16c5b-128">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-129">65</span><span class="sxs-lookup"><span data-stu-id="16c5b-129">65</span></span>

<span data-ttu-id="16c5b-130">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="16c5b-130">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-131">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="16c5b-131">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-132">66</span><span class="sxs-lookup"><span data-stu-id="16c5b-132">66</span></span>

<span data-ttu-id="16c5b-133">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="16c5b-133">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-134">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="16c5b-134">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-135">67</span><span class="sxs-lookup"><span data-stu-id="16c5b-135">67</span></span>

<span data-ttu-id="16c5b-136">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="16c5b-136">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-137">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="16c5b-137">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-138">68</span><span class="sxs-lookup"><span data-stu-id="16c5b-138">68</span></span>

<span data-ttu-id="16c5b-139">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="16c5b-139">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-140">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="16c5b-140">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-141">69</span><span class="sxs-lookup"><span data-stu-id="16c5b-141">69</span></span>

<span data-ttu-id="16c5b-142">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="16c5b-142">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-143">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="16c5b-143">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-144">70</span><span class="sxs-lookup"><span data-stu-id="16c5b-144">70</span></span>

<span data-ttu-id="16c5b-145">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="16c5b-145">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-146">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="16c5b-146">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-147">71</span><span class="sxs-lookup"><span data-stu-id="16c5b-147">71</span></span>

<span data-ttu-id="16c5b-148">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="16c5b-148">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-149">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="16c5b-149">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-150">72</span><span class="sxs-lookup"><span data-stu-id="16c5b-150">72</span></span>

<span data-ttu-id="16c5b-151">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="16c5b-151">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-152">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="16c5b-152">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-153">73</span><span class="sxs-lookup"><span data-stu-id="16c5b-153">73</span></span>

<span data-ttu-id="16c5b-154">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="16c5b-154">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-155">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="16c5b-155">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-156">74</span><span class="sxs-lookup"><span data-stu-id="16c5b-156">74</span></span>

<span data-ttu-id="16c5b-157">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="16c5b-157">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-158">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="16c5b-158">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-159">75</span><span class="sxs-lookup"><span data-stu-id="16c5b-159">75</span></span>

<span data-ttu-id="16c5b-160">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="16c5b-160">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-161">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="16c5b-161">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-162">76</span><span class="sxs-lookup"><span data-stu-id="16c5b-162">76</span></span>

<span data-ttu-id="16c5b-163">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="16c5b-163">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-164">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="16c5b-164">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-165">77</span><span class="sxs-lookup"><span data-stu-id="16c5b-165">77</span></span>

<span data-ttu-id="16c5b-166">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="16c5b-166">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-167">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="16c5b-167">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-168">78</span><span class="sxs-lookup"><span data-stu-id="16c5b-168">78</span></span>

<span data-ttu-id="16c5b-169">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="16c5b-169">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-170">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="16c5b-170">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-171">79</span><span class="sxs-lookup"><span data-stu-id="16c5b-171">79</span></span>

<span data-ttu-id="16c5b-172">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="16c5b-172">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-173">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="16c5b-173">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-174">80</span><span class="sxs-lookup"><span data-stu-id="16c5b-174">80</span></span>

<span data-ttu-id="16c5b-175">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="16c5b-175">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-176">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="16c5b-176">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-177">81</span><span class="sxs-lookup"><span data-stu-id="16c5b-177">81</span></span>

<span data-ttu-id="16c5b-178">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="16c5b-178">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-179">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="16c5b-179">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-180">82</span><span class="sxs-lookup"><span data-stu-id="16c5b-180">82</span></span>

<span data-ttu-id="16c5b-181">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="16c5b-181">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-182">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="16c5b-182">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-183">83</span><span class="sxs-lookup"><span data-stu-id="16c5b-183">83</span></span>

<span data-ttu-id="16c5b-184">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="16c5b-184">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-185">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="16c5b-185">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-186">84</span><span class="sxs-lookup"><span data-stu-id="16c5b-186">84</span></span>

<span data-ttu-id="16c5b-187">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="16c5b-187">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-188">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="16c5b-188">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-189">85</span><span class="sxs-lookup"><span data-stu-id="16c5b-189">85</span></span>

<span data-ttu-id="16c5b-190">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="16c5b-190">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-191">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="16c5b-191">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-192">86</span><span class="sxs-lookup"><span data-stu-id="16c5b-192">86</span></span>

<span data-ttu-id="16c5b-193">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="16c5b-193">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-194">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="16c5b-194">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-195">87</span><span class="sxs-lookup"><span data-stu-id="16c5b-195">87</span></span>

<span data-ttu-id="16c5b-196">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="16c5b-196">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-197">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="16c5b-197">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-198">88</span><span class="sxs-lookup"><span data-stu-id="16c5b-198">88</span></span>

<span data-ttu-id="16c5b-199">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="16c5b-199">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-200">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="16c5b-200">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-201">89</span><span class="sxs-lookup"><span data-stu-id="16c5b-201">89</span></span>

<span data-ttu-id="16c5b-202">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="16c5b-202">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-203">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="16c5b-203">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-204">90</span><span class="sxs-lookup"><span data-stu-id="16c5b-204">90</span></span>

<span data-ttu-id="16c5b-205">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="16c5b-205">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-206">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="16c5b-206">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-207">91</span><span class="sxs-lookup"><span data-stu-id="16c5b-207">91</span></span>

<span data-ttu-id="16c5b-208">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="16c5b-208">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-209">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="16c5b-209">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-210">92</span><span class="sxs-lookup"><span data-stu-id="16c5b-210">92</span></span>

<span data-ttu-id="16c5b-211">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="16c5b-211">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-212">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="16c5b-212">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-213">93</span><span class="sxs-lookup"><span data-stu-id="16c5b-213">93</span></span>

<span data-ttu-id="16c5b-214">已經存在。</span><span class="sxs-lookup"><span data-stu-id="16c5b-214">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-215">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="16c5b-215">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-216">94</span><span class="sxs-lookup"><span data-stu-id="16c5b-216">94</span></span>

<span data-ttu-id="16c5b-217">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="16c5b-217">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-218">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="16c5b-218">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-219">95</span><span class="sxs-lookup"><span data-stu-id="16c5b-219">95</span></span>

<span data-ttu-id="16c5b-220">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="16c5b-220">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-221">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="16c5b-221">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-222">96</span><span class="sxs-lookup"><span data-stu-id="16c5b-222">96</span></span>

<span data-ttu-id="16c5b-223">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="16c5b-223">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-224">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="16c5b-224">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-225">97</span><span class="sxs-lookup"><span data-stu-id="16c5b-225">97</span></span>

<span data-ttu-id="16c5b-226">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="16c5b-226">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-227">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="16c5b-227">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-228">98</span><span class="sxs-lookup"><span data-stu-id="16c5b-228">98</span></span>

<span data-ttu-id="16c5b-229">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="16c5b-229">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-230">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="16c5b-230">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-231">100</span><span class="sxs-lookup"><span data-stu-id="16c5b-231">100</span></span>

<span data-ttu-id="16c5b-232">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="16c5b-232">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="16c5b-233">**其他**</span><span class="sxs-lookup"><span data-stu-id="16c5b-233">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="16c5b-234">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="16c5b-234">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="16c5b-235">備註</span><span class="sxs-lookup"><span data-stu-id="16c5b-235">Remarks</span></span>

<span data-ttu-id="16c5b-236">**SetDefaultTOS** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來在連出 IP 封包的標頭中設定預設的 TOS 值。</span><span class="sxs-lookup"><span data-stu-id="16c5b-236">The **SetDefaultTOS** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default TOS value in the header of outgoing IP packets.</span></span>

## <a name="requirements"></a><span data-ttu-id="16c5b-237">規格需求</span><span class="sxs-lookup"><span data-stu-id="16c5b-237">Requirements</span></span>



| <span data-ttu-id="16c5b-238">需求</span><span class="sxs-lookup"><span data-stu-id="16c5b-238">Requirement</span></span> | <span data-ttu-id="16c5b-239">值</span><span class="sxs-lookup"><span data-stu-id="16c5b-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="16c5b-240">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="16c5b-240">Minimum supported client</span></span><br/> | <span data-ttu-id="16c5b-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="16c5b-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="16c5b-242">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="16c5b-242">Minimum supported server</span></span><br/> | <span data-ttu-id="16c5b-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="16c5b-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="16c5b-244">命名空間</span><span class="sxs-lookup"><span data-stu-id="16c5b-244">Namespace</span></span><br/>                | <span data-ttu-id="16c5b-245">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="16c5b-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="16c5b-246">MOF</span><span class="sxs-lookup"><span data-stu-id="16c5b-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="16c5b-247"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="16c5b-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="16c5b-248">DLL</span><span class="sxs-lookup"><span data-stu-id="16c5b-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="16c5b-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="16c5b-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="16c5b-250">另請參閱</span><span class="sxs-lookup"><span data-stu-id="16c5b-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="16c5b-251">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="16c5b-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="16c5b-252">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="16c5b-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="16c5b-253">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="16c5b-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="16c5b-254">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="16c5b-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="16c5b-255">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="16c5b-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

