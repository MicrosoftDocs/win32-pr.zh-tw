---
description: ReleaseDHCPLease WMI 類別方法會釋放系結至已啟用 DHCP 之特定網路介面卡的 IP 位址。
ms.assetid: 0cf4b531-8626-4388-bffa-e16a4aa8c794
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 ReleaseDHCPLease 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLease
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5520a6b2d0960c1d4258b19f8cd4d600c9b8fe34
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972784"
---
# <a name="releasedhcplease-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="774a3-103">Win32 >networkadapterconfiguration 類別的 ReleaseDHCPLease 方法 \_</span><span class="sxs-lookup"><span data-stu-id="774a3-103">ReleaseDHCPLease method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="774a3-104">**ReleaseDHCPLease** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)方法會釋放系結至已啟用 DHCP 之特定網路介面卡的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="774a3-104">The **ReleaseDHCPLease** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) method releases the IP address bound to a specific DHCP-enabled network adapter.</span></span>

<span data-ttu-id="774a3-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="774a3-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="774a3-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="774a3-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="774a3-107">語法</span><span class="sxs-lookup"><span data-stu-id="774a3-107">Syntax</span></span>


```mof
uint32 ReleaseDHCPLease();
```



## <a name="parameters"></a><span data-ttu-id="774a3-108">參數</span><span class="sxs-lookup"><span data-stu-id="774a3-108">Parameters</span></span>

<span data-ttu-id="774a3-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="774a3-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="774a3-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="774a3-110">Return value</span></span>

<span data-ttu-id="774a3-111">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="774a3-111">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="774a3-112">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="774a3-112">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="774a3-113">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="774a3-113">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="774a3-114">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="774a3-114">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-115">0</span><span class="sxs-lookup"><span data-stu-id="774a3-115">0</span></span>

<span data-ttu-id="774a3-116">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="774a3-116">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-117">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="774a3-117">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-118">1</span><span class="sxs-lookup"><span data-stu-id="774a3-118">1</span></span>

<span data-ttu-id="774a3-119">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="774a3-119">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-120">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="774a3-120">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-121">64</span><span class="sxs-lookup"><span data-stu-id="774a3-121">64</span></span>

<span data-ttu-id="774a3-122">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="774a3-122">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-123">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="774a3-123">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-124">65</span><span class="sxs-lookup"><span data-stu-id="774a3-124">65</span></span>

<span data-ttu-id="774a3-125">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="774a3-125">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-126">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="774a3-126">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-127">66</span><span class="sxs-lookup"><span data-stu-id="774a3-127">66</span></span>

<span data-ttu-id="774a3-128">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="774a3-128">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-129">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="774a3-129">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-130">67</span><span class="sxs-lookup"><span data-stu-id="774a3-130">67</span></span>

<span data-ttu-id="774a3-131">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="774a3-131">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-132">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="774a3-132">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-133">68</span><span class="sxs-lookup"><span data-stu-id="774a3-133">68</span></span>

<span data-ttu-id="774a3-134">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="774a3-134">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-135">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="774a3-135">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-136">69</span><span class="sxs-lookup"><span data-stu-id="774a3-136">69</span></span>

<span data-ttu-id="774a3-137">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="774a3-137">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-138">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="774a3-138">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-139">70</span><span class="sxs-lookup"><span data-stu-id="774a3-139">70</span></span>

<span data-ttu-id="774a3-140">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="774a3-140">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-141">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="774a3-141">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-142">71</span><span class="sxs-lookup"><span data-stu-id="774a3-142">71</span></span>

<span data-ttu-id="774a3-143">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="774a3-143">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-144">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="774a3-144">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-145">72</span><span class="sxs-lookup"><span data-stu-id="774a3-145">72</span></span>

<span data-ttu-id="774a3-146">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="774a3-146">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-147">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="774a3-147">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-148">73</span><span class="sxs-lookup"><span data-stu-id="774a3-148">73</span></span>

<span data-ttu-id="774a3-149">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="774a3-149">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-150">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="774a3-150">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-151">74</span><span class="sxs-lookup"><span data-stu-id="774a3-151">74</span></span>

<span data-ttu-id="774a3-152">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="774a3-152">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-153">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="774a3-153">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-154">75</span><span class="sxs-lookup"><span data-stu-id="774a3-154">75</span></span>

<span data-ttu-id="774a3-155">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="774a3-155">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-156">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="774a3-156">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-157">76</span><span class="sxs-lookup"><span data-stu-id="774a3-157">76</span></span>

<span data-ttu-id="774a3-158">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="774a3-158">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-159">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="774a3-159">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-160">77</span><span class="sxs-lookup"><span data-stu-id="774a3-160">77</span></span>

<span data-ttu-id="774a3-161">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="774a3-161">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-162">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="774a3-162">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-163">78</span><span class="sxs-lookup"><span data-stu-id="774a3-163">78</span></span>

<span data-ttu-id="774a3-164">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="774a3-164">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-165">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="774a3-165">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-166">79</span><span class="sxs-lookup"><span data-stu-id="774a3-166">79</span></span>

<span data-ttu-id="774a3-167">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="774a3-167">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-168">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="774a3-168">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-169">80</span><span class="sxs-lookup"><span data-stu-id="774a3-169">80</span></span>

<span data-ttu-id="774a3-170">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="774a3-170">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-171">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="774a3-171">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-172">81</span><span class="sxs-lookup"><span data-stu-id="774a3-172">81</span></span>

<span data-ttu-id="774a3-173">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="774a3-173">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-174">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="774a3-174">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-175">82</span><span class="sxs-lookup"><span data-stu-id="774a3-175">82</span></span>

<span data-ttu-id="774a3-176">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="774a3-176">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-177">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="774a3-177">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-178">83</span><span class="sxs-lookup"><span data-stu-id="774a3-178">83</span></span>

<span data-ttu-id="774a3-179">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="774a3-179">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-180">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="774a3-180">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-181">84</span><span class="sxs-lookup"><span data-stu-id="774a3-181">84</span></span>

<span data-ttu-id="774a3-182">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="774a3-182">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-183">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="774a3-183">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-184">85</span><span class="sxs-lookup"><span data-stu-id="774a3-184">85</span></span>

<span data-ttu-id="774a3-185">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="774a3-185">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-186">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="774a3-186">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-187">86</span><span class="sxs-lookup"><span data-stu-id="774a3-187">86</span></span>

<span data-ttu-id="774a3-188">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="774a3-188">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-189">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="774a3-189">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-190">87</span><span class="sxs-lookup"><span data-stu-id="774a3-190">87</span></span>

<span data-ttu-id="774a3-191">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="774a3-191">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-192">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="774a3-192">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-193">88</span><span class="sxs-lookup"><span data-stu-id="774a3-193">88</span></span>

<span data-ttu-id="774a3-194">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="774a3-194">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-195">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="774a3-195">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-196">89</span><span class="sxs-lookup"><span data-stu-id="774a3-196">89</span></span>

<span data-ttu-id="774a3-197">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="774a3-197">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-198">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="774a3-198">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-199">90</span><span class="sxs-lookup"><span data-stu-id="774a3-199">90</span></span>

<span data-ttu-id="774a3-200">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="774a3-200">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-201">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="774a3-201">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-202">91</span><span class="sxs-lookup"><span data-stu-id="774a3-202">91</span></span>

<span data-ttu-id="774a3-203">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="774a3-203">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-204">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="774a3-204">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-205">92</span><span class="sxs-lookup"><span data-stu-id="774a3-205">92</span></span>

<span data-ttu-id="774a3-206">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="774a3-206">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-207">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="774a3-207">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-208">93</span><span class="sxs-lookup"><span data-stu-id="774a3-208">93</span></span>

<span data-ttu-id="774a3-209">已經存在。</span><span class="sxs-lookup"><span data-stu-id="774a3-209">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-210">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="774a3-210">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-211">94</span><span class="sxs-lookup"><span data-stu-id="774a3-211">94</span></span>

<span data-ttu-id="774a3-212">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="774a3-212">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-213">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="774a3-213">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-214">95</span><span class="sxs-lookup"><span data-stu-id="774a3-214">95</span></span>

<span data-ttu-id="774a3-215">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="774a3-215">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-216">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="774a3-216">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-217">96</span><span class="sxs-lookup"><span data-stu-id="774a3-217">96</span></span>

<span data-ttu-id="774a3-218">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="774a3-218">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-219">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="774a3-219">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-220">97</span><span class="sxs-lookup"><span data-stu-id="774a3-220">97</span></span>

<span data-ttu-id="774a3-221">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="774a3-221">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-222">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="774a3-222">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-223">98</span><span class="sxs-lookup"><span data-stu-id="774a3-223">98</span></span>

<span data-ttu-id="774a3-224">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="774a3-224">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-225">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="774a3-225">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-226">100</span><span class="sxs-lookup"><span data-stu-id="774a3-226">100</span></span>

<span data-ttu-id="774a3-227">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="774a3-227">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="774a3-228">**其他**</span><span class="sxs-lookup"><span data-stu-id="774a3-228">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="774a3-229">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="774a3-229">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="774a3-230">備註</span><span class="sxs-lookup"><span data-stu-id="774a3-230">Remarks</span></span>

> [!Caution]  
> <span data-ttu-id="774a3-231">如果本機電腦系統上已啟用 DHCP，此選項會停用此特定網路介面卡上的 TCP/IP。</span><span class="sxs-lookup"><span data-stu-id="774a3-231">If DHCP is enabled on the local computer system, the option disables TCP/IP on this specific network adapter.</span></span> <span data-ttu-id="774a3-232">除非您有目標系統的替代路徑，也就是另一個 TCP/IP 系結的網路介面卡，所有 TCP/IP 通訊都將遺失。</span><span class="sxs-lookup"><span data-stu-id="774a3-232">Unless you have an alternate path to the target system, that is, another TCP/IP bound network adapter, all TCP/IP communications will be lost.</span></span>

 

## <a name="examples"></a><span data-ttu-id="774a3-233">範例</span><span class="sxs-lookup"><span data-stu-id="774a3-233">Examples</span></span>

<span data-ttu-id="774a3-234">在 TechNet 資源庫上使用 PowerShell powershell 範例的 [發行更新 Ip 位址](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) ，會使用 **ReleaseDHCPLease** 來釋放和更新 ip 位址。</span><span class="sxs-lookup"><span data-stu-id="774a3-234">The [Release Renew IP Adresses Using PowerShell](https://Gallery.TechNet.Microsoft.Com/Renew-IP-Adresses-Using-365f6bfa) PowerShell example on TechNet Gallery uses **ReleaseDHCPLease** to release and renew an IP address.</span></span>

<span data-ttu-id="774a3-235">下列 VBScript 程式碼會針對電腦上所有 TCP/IP 系結的網路介面卡，釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="774a3-235">The following VBScript code releases the DHCP leases for all TCP/IP-bound network adapters on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set colNetCards = objWMIService.ExecQuery _ 
    ("Select * From Win32_NetworkAdapterConfiguration Where IPEnabled = True") 
 
For Each objNetCard in colNetCards 
    objNetCard.ReleaseDHCPLease() 
Next 
```



## <a name="requirements"></a><span data-ttu-id="774a3-236">規格需求</span><span class="sxs-lookup"><span data-stu-id="774a3-236">Requirements</span></span>



| <span data-ttu-id="774a3-237">需求</span><span class="sxs-lookup"><span data-stu-id="774a3-237">Requirement</span></span> | <span data-ttu-id="774a3-238">值</span><span class="sxs-lookup"><span data-stu-id="774a3-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="774a3-239">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="774a3-239">Minimum supported client</span></span><br/> | <span data-ttu-id="774a3-240">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="774a3-240">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="774a3-241">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="774a3-241">Minimum supported server</span></span><br/> | <span data-ttu-id="774a3-242">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="774a3-242">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="774a3-243">命名空間</span><span class="sxs-lookup"><span data-stu-id="774a3-243">Namespace</span></span><br/>                | <span data-ttu-id="774a3-244">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="774a3-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="774a3-245">MOF</span><span class="sxs-lookup"><span data-stu-id="774a3-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="774a3-246"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="774a3-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="774a3-247">DLL</span><span class="sxs-lookup"><span data-stu-id="774a3-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="774a3-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="774a3-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="774a3-249">另請參閱</span><span class="sxs-lookup"><span data-stu-id="774a3-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="774a3-250">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="774a3-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="774a3-251">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="774a3-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="774a3-252">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="774a3-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="774a3-253">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="774a3-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="774a3-254">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="774a3-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

