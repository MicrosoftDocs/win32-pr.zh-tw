---
description: SetDefaultTTL WMI 類別靜態方法是用來設定傳出 IP 封包標頭中 (TTL) 值的預設存留時間。
ms.assetid: 74b060de-512c-407e-9f93-c3b496f8d09d
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetDefaultTTL 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetDefaultTTL
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 253048b44a836f92646124fb972fe32c135e3b9a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103846968"
---
# <a name="setdefaultttl-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="8ecc0-103">Win32 >networkadapterconfiguration 類別的 SetDefaultTTL 方法 \_</span><span class="sxs-lookup"><span data-stu-id="8ecc0-103">SetDefaultTTL method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="8ecc0-104">**SetDefaultTTL** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定傳出 IP 封包標頭中 (TTL) 值的預設存留時間。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-104">The **SetDefaultTTL** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the default Time to Live (TTL) value in the header of outgoing IP packets.</span></span>

<span data-ttu-id="8ecc0-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="8ecc0-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="8ecc0-107">語法</span><span class="sxs-lookup"><span data-stu-id="8ecc0-107">Syntax</span></span>


```mof
uint32 SetDefaultTTL(
  [in] uint8 DefaultTTL
);
```



## <a name="parameters"></a><span data-ttu-id="8ecc0-108">參數</span><span class="sxs-lookup"><span data-stu-id="8ecc0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ecc0-109">*DefaultTTL* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8ecc0-109">*DefaultTTL* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-110">在傳出 IP 封包的標頭中設定存留時間值。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-110">Time to Live value set in the header of outgoing IP packets.</span></span> <span data-ttu-id="8ecc0-111">預設值為 32;有效範圍： 1-255</span><span class="sxs-lookup"><span data-stu-id="8ecc0-111">The default value is 32; Valid range: 1 - 255</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ecc0-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="8ecc0-112">Return value</span></span>

<span data-ttu-id="8ecc0-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="8ecc0-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="8ecc0-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="8ecc0-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-117">0</span><span class="sxs-lookup"><span data-stu-id="8ecc0-117">0</span></span>

<span data-ttu-id="8ecc0-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-120">1</span><span class="sxs-lookup"><span data-stu-id="8ecc0-120">1</span></span>

<span data-ttu-id="8ecc0-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-123">64</span><span class="sxs-lookup"><span data-stu-id="8ecc0-123">64</span></span>

<span data-ttu-id="8ecc0-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-126">65</span><span class="sxs-lookup"><span data-stu-id="8ecc0-126">65</span></span>

<span data-ttu-id="8ecc0-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-129">66</span><span class="sxs-lookup"><span data-stu-id="8ecc0-129">66</span></span>

<span data-ttu-id="8ecc0-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-132">67</span><span class="sxs-lookup"><span data-stu-id="8ecc0-132">67</span></span>

<span data-ttu-id="8ecc0-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-135">68</span><span class="sxs-lookup"><span data-stu-id="8ecc0-135">68</span></span>

<span data-ttu-id="8ecc0-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-138">69</span><span class="sxs-lookup"><span data-stu-id="8ecc0-138">69</span></span>

<span data-ttu-id="8ecc0-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-141">70</span><span class="sxs-lookup"><span data-stu-id="8ecc0-141">70</span></span>

<span data-ttu-id="8ecc0-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-144">71</span><span class="sxs-lookup"><span data-stu-id="8ecc0-144">71</span></span>

<span data-ttu-id="8ecc0-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-147">72</span><span class="sxs-lookup"><span data-stu-id="8ecc0-147">72</span></span>

<span data-ttu-id="8ecc0-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-150">73</span><span class="sxs-lookup"><span data-stu-id="8ecc0-150">73</span></span>

<span data-ttu-id="8ecc0-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-153">74</span><span class="sxs-lookup"><span data-stu-id="8ecc0-153">74</span></span>

<span data-ttu-id="8ecc0-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-156">75</span><span class="sxs-lookup"><span data-stu-id="8ecc0-156">75</span></span>

<span data-ttu-id="8ecc0-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-159">76</span><span class="sxs-lookup"><span data-stu-id="8ecc0-159">76</span></span>

<span data-ttu-id="8ecc0-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-162">77</span><span class="sxs-lookup"><span data-stu-id="8ecc0-162">77</span></span>

<span data-ttu-id="8ecc0-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-165">78</span><span class="sxs-lookup"><span data-stu-id="8ecc0-165">78</span></span>

<span data-ttu-id="8ecc0-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-168">79</span><span class="sxs-lookup"><span data-stu-id="8ecc0-168">79</span></span>

<span data-ttu-id="8ecc0-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-171">80</span><span class="sxs-lookup"><span data-stu-id="8ecc0-171">80</span></span>

<span data-ttu-id="8ecc0-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-174">81</span><span class="sxs-lookup"><span data-stu-id="8ecc0-174">81</span></span>

<span data-ttu-id="8ecc0-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-177">82</span><span class="sxs-lookup"><span data-stu-id="8ecc0-177">82</span></span>

<span data-ttu-id="8ecc0-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-180">83</span><span class="sxs-lookup"><span data-stu-id="8ecc0-180">83</span></span>

<span data-ttu-id="8ecc0-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-183">84</span><span class="sxs-lookup"><span data-stu-id="8ecc0-183">84</span></span>

<span data-ttu-id="8ecc0-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-186">85</span><span class="sxs-lookup"><span data-stu-id="8ecc0-186">85</span></span>

<span data-ttu-id="8ecc0-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-189">86</span><span class="sxs-lookup"><span data-stu-id="8ecc0-189">86</span></span>

<span data-ttu-id="8ecc0-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-192">87</span><span class="sxs-lookup"><span data-stu-id="8ecc0-192">87</span></span>

<span data-ttu-id="8ecc0-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-195">88</span><span class="sxs-lookup"><span data-stu-id="8ecc0-195">88</span></span>

<span data-ttu-id="8ecc0-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-198">89</span><span class="sxs-lookup"><span data-stu-id="8ecc0-198">89</span></span>

<span data-ttu-id="8ecc0-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-201">90</span><span class="sxs-lookup"><span data-stu-id="8ecc0-201">90</span></span>

<span data-ttu-id="8ecc0-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-204">91</span><span class="sxs-lookup"><span data-stu-id="8ecc0-204">91</span></span>

<span data-ttu-id="8ecc0-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-207">92</span><span class="sxs-lookup"><span data-stu-id="8ecc0-207">92</span></span>

<span data-ttu-id="8ecc0-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-210">93</span><span class="sxs-lookup"><span data-stu-id="8ecc0-210">93</span></span>

<span data-ttu-id="8ecc0-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-213">94</span><span class="sxs-lookup"><span data-stu-id="8ecc0-213">94</span></span>

<span data-ttu-id="8ecc0-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-216">95</span><span class="sxs-lookup"><span data-stu-id="8ecc0-216">95</span></span>

<span data-ttu-id="8ecc0-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-219">96</span><span class="sxs-lookup"><span data-stu-id="8ecc0-219">96</span></span>

<span data-ttu-id="8ecc0-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-222">97</span><span class="sxs-lookup"><span data-stu-id="8ecc0-222">97</span></span>

<span data-ttu-id="8ecc0-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-225">98</span><span class="sxs-lookup"><span data-stu-id="8ecc0-225">98</span></span>

<span data-ttu-id="8ecc0-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-228">100</span><span class="sxs-lookup"><span data-stu-id="8ecc0-228">100</span></span>

<span data-ttu-id="8ecc0-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="8ecc0-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="8ecc0-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="8ecc0-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8ecc0-232">備註</span><span class="sxs-lookup"><span data-stu-id="8ecc0-232">Remarks</span></span>

<span data-ttu-id="8ecc0-233">TTL 會指定 IP 封包可能傳遞的路由器數目，以在被捨棄之前抵達目的地。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-233">The TTL specifies the number of routers an IP packet may pass through to reach its destination before being discarded.</span></span> <span data-ttu-id="8ecc0-234">每個路由器會將封包的 TTL 計數遞減1，並捨棄 TTL 為 0 (零) 的封包。</span><span class="sxs-lookup"><span data-stu-id="8ecc0-234">Each router decrements the TTL count of a packet by one and discards the packets with a TTL of 0 (zero).</span></span>

## <a name="examples"></a><span data-ttu-id="8ecc0-235">範例</span><span class="sxs-lookup"><span data-stu-id="8ecc0-235">Examples</span></span>

<span data-ttu-id="8ecc0-236">[修改所有網路介面卡的預設存留時間（](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript）範例會使用 **SETDEFAULTTTL** 將傳出 IP 封包標頭中的預設存留時間值設定為64</span><span class="sxs-lookup"><span data-stu-id="8ecc0-236">The [Modify the Default Time-to-Live for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/scriptcenter/3a228fb8-5517-4e23-800e-2a15f427d05d) VBScript sample uses **SetDefaultTTL** to set the default time-to-live value in the header of outgoing IP packets to 64</span></span>

## <a name="requirements"></a><span data-ttu-id="8ecc0-237">規格需求</span><span class="sxs-lookup"><span data-stu-id="8ecc0-237">Requirements</span></span>



| <span data-ttu-id="8ecc0-238">需求</span><span class="sxs-lookup"><span data-stu-id="8ecc0-238">Requirement</span></span> | <span data-ttu-id="8ecc0-239">值</span><span class="sxs-lookup"><span data-stu-id="8ecc0-239">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8ecc0-240">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8ecc0-240">Minimum supported client</span></span><br/> | <span data-ttu-id="8ecc0-241">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8ecc0-241">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="8ecc0-242">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8ecc0-242">Minimum supported server</span></span><br/> | <span data-ttu-id="8ecc0-243">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8ecc0-243">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="8ecc0-244">命名空間</span><span class="sxs-lookup"><span data-stu-id="8ecc0-244">Namespace</span></span><br/>                | <span data-ttu-id="8ecc0-245">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="8ecc0-245">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="8ecc0-246">MOF</span><span class="sxs-lookup"><span data-stu-id="8ecc0-246">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8ecc0-247"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="8ecc0-247"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="8ecc0-248">DLL</span><span class="sxs-lookup"><span data-stu-id="8ecc0-248">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8ecc0-249"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8ecc0-249"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ecc0-250">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8ecc0-250">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ecc0-251">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="8ecc0-251">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="8ecc0-252">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="8ecc0-252">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="8ecc0-253">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="8ecc0-253">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="8ecc0-254">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="8ecc0-254">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="8ecc0-255">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="8ecc0-255">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

