---
description: '>releasedhcpleaseall WMI 類別靜態方法會釋放系結至所有啟用 DHCP 之網路介面卡的 IP 位址。'
ms.assetid: d9f83953-f3da-419d-8c84-649c39b4945e
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 >releasedhcpleaseall 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.ReleaseDHCPLeaseAll
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3e7b1f7cf2f09fa20f7bf19b15e82f536ca0aa50
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970111"
---
# <a name="releasedhcpleaseall-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="a00a2-103">Win32 >networkadapterconfiguration 類別的 >releasedhcpleaseall 方法 \_</span><span class="sxs-lookup"><span data-stu-id="a00a2-103">ReleaseDHCPLeaseAll method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="a00a2-104">**>releasedhcpleaseall** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法會釋放系結至所有啟用 DHCP 之網路介面卡的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="a00a2-104">The **ReleaseDHCPLeaseAll** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method releases the IP addresses bound to all DHCP-enabled network adapters.</span></span>

> [!Note]  
> <span data-ttu-id="a00a2-105">警告：如果本機電腦系統上已啟用 DHCP，此選項將會終止所有的 DHCP TCP/IP 連接。</span><span class="sxs-lookup"><span data-stu-id="a00a2-105">Warning If DHCP is enabled on the local computer system, the option will terminate all DHCP TCP/IP connections.</span></span>

 

<span data-ttu-id="a00a2-106">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="a00a2-106">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="a00a2-107">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="a00a2-107">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="a00a2-108">語法</span><span class="sxs-lookup"><span data-stu-id="a00a2-108">Syntax</span></span>


```mof
uint32 ReleaseDHCPLeaseAll();
```



## <a name="parameters"></a><span data-ttu-id="a00a2-109">參數</span><span class="sxs-lookup"><span data-stu-id="a00a2-109">Parameters</span></span>

<span data-ttu-id="a00a2-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a00a2-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a00a2-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a00a2-111">Return value</span></span>

<span data-ttu-id="a00a2-112">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="a00a2-112">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="a00a2-113">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="a00a2-113">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="a00a2-114">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="a00a2-114">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="a00a2-115">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="a00a2-115">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-116">0</span><span class="sxs-lookup"><span data-stu-id="a00a2-116">0</span></span>

<span data-ttu-id="a00a2-117">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="a00a2-117">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-118">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="a00a2-118">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-119">1</span><span class="sxs-lookup"><span data-stu-id="a00a2-119">1</span></span>

<span data-ttu-id="a00a2-120">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="a00a2-120">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-121">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="a00a2-121">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-122">64</span><span class="sxs-lookup"><span data-stu-id="a00a2-122">64</span></span>

<span data-ttu-id="a00a2-123">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="a00a2-123">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-124">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="a00a2-124">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-125">65</span><span class="sxs-lookup"><span data-stu-id="a00a2-125">65</span></span>

<span data-ttu-id="a00a2-126">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="a00a2-126">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-127">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="a00a2-127">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-128">66</span><span class="sxs-lookup"><span data-stu-id="a00a2-128">66</span></span>

<span data-ttu-id="a00a2-129">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="a00a2-129">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-130">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="a00a2-130">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-131">67</span><span class="sxs-lookup"><span data-stu-id="a00a2-131">67</span></span>

<span data-ttu-id="a00a2-132">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a00a2-132">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-133">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="a00a2-133">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-134">68</span><span class="sxs-lookup"><span data-stu-id="a00a2-134">68</span></span>

<span data-ttu-id="a00a2-135">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="a00a2-135">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-136">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="a00a2-136">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-137">69</span><span class="sxs-lookup"><span data-stu-id="a00a2-137">69</span></span>

<span data-ttu-id="a00a2-138">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="a00a2-138">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-139">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="a00a2-139">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-140">70</span><span class="sxs-lookup"><span data-stu-id="a00a2-140">70</span></span>

<span data-ttu-id="a00a2-141">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="a00a2-141">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-142">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="a00a2-142">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-143">71</span><span class="sxs-lookup"><span data-stu-id="a00a2-143">71</span></span>

<span data-ttu-id="a00a2-144">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="a00a2-144">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-145">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="a00a2-145">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-146">72</span><span class="sxs-lookup"><span data-stu-id="a00a2-146">72</span></span>

<span data-ttu-id="a00a2-147">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="a00a2-147">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-148">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="a00a2-148">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-149">73</span><span class="sxs-lookup"><span data-stu-id="a00a2-149">73</span></span>

<span data-ttu-id="a00a2-150">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="a00a2-150">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-151">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="a00a2-151">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-152">74</span><span class="sxs-lookup"><span data-stu-id="a00a2-152">74</span></span>

<span data-ttu-id="a00a2-153">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="a00a2-153">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-154">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="a00a2-154">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-155">75</span><span class="sxs-lookup"><span data-stu-id="a00a2-155">75</span></span>

<span data-ttu-id="a00a2-156">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="a00a2-156">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-157">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="a00a2-157">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-158">76</span><span class="sxs-lookup"><span data-stu-id="a00a2-158">76</span></span>

<span data-ttu-id="a00a2-159">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="a00a2-159">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-160">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="a00a2-160">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-161">77</span><span class="sxs-lookup"><span data-stu-id="a00a2-161">77</span></span>

<span data-ttu-id="a00a2-162">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="a00a2-162">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-163">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="a00a2-163">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-164">78</span><span class="sxs-lookup"><span data-stu-id="a00a2-164">78</span></span>

<span data-ttu-id="a00a2-165">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="a00a2-165">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-166">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="a00a2-166">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-167">79</span><span class="sxs-lookup"><span data-stu-id="a00a2-167">79</span></span>

<span data-ttu-id="a00a2-168">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="a00a2-168">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-169">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="a00a2-169">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-170">80</span><span class="sxs-lookup"><span data-stu-id="a00a2-170">80</span></span>

<span data-ttu-id="a00a2-171">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="a00a2-171">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-172">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="a00a2-172">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-173">81</span><span class="sxs-lookup"><span data-stu-id="a00a2-173">81</span></span>

<span data-ttu-id="a00a2-174">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="a00a2-174">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-175">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="a00a2-175">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-176">82</span><span class="sxs-lookup"><span data-stu-id="a00a2-176">82</span></span>

<span data-ttu-id="a00a2-177">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="a00a2-177">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-178">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="a00a2-178">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-179">83</span><span class="sxs-lookup"><span data-stu-id="a00a2-179">83</span></span>

<span data-ttu-id="a00a2-180">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="a00a2-180">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-181">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="a00a2-181">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-182">84</span><span class="sxs-lookup"><span data-stu-id="a00a2-182">84</span></span>

<span data-ttu-id="a00a2-183">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="a00a2-183">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-184">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="a00a2-184">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-185">85</span><span class="sxs-lookup"><span data-stu-id="a00a2-185">85</span></span>

<span data-ttu-id="a00a2-186">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="a00a2-186">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-187">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="a00a2-187">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-188">86</span><span class="sxs-lookup"><span data-stu-id="a00a2-188">86</span></span>

<span data-ttu-id="a00a2-189">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="a00a2-189">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-190">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="a00a2-190">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-191">87</span><span class="sxs-lookup"><span data-stu-id="a00a2-191">87</span></span>

<span data-ttu-id="a00a2-192">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="a00a2-192">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-193">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="a00a2-193">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-194">88</span><span class="sxs-lookup"><span data-stu-id="a00a2-194">88</span></span>

<span data-ttu-id="a00a2-195">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="a00a2-195">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-196">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="a00a2-196">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-197">89</span><span class="sxs-lookup"><span data-stu-id="a00a2-197">89</span></span>

<span data-ttu-id="a00a2-198">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="a00a2-198">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-199">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="a00a2-199">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-200">90</span><span class="sxs-lookup"><span data-stu-id="a00a2-200">90</span></span>

<span data-ttu-id="a00a2-201">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="a00a2-201">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-202">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="a00a2-202">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-203">91</span><span class="sxs-lookup"><span data-stu-id="a00a2-203">91</span></span>

<span data-ttu-id="a00a2-204">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="a00a2-204">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-205">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="a00a2-205">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-206">92</span><span class="sxs-lookup"><span data-stu-id="a00a2-206">92</span></span>

<span data-ttu-id="a00a2-207">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="a00a2-207">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-208">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="a00a2-208">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-209">93</span><span class="sxs-lookup"><span data-stu-id="a00a2-209">93</span></span>

<span data-ttu-id="a00a2-210">已經存在。</span><span class="sxs-lookup"><span data-stu-id="a00a2-210">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-211">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="a00a2-211">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-212">94</span><span class="sxs-lookup"><span data-stu-id="a00a2-212">94</span></span>

<span data-ttu-id="a00a2-213">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="a00a2-213">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-214">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="a00a2-214">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-215">95</span><span class="sxs-lookup"><span data-stu-id="a00a2-215">95</span></span>

<span data-ttu-id="a00a2-216">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="a00a2-216">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-217">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="a00a2-217">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-218">96</span><span class="sxs-lookup"><span data-stu-id="a00a2-218">96</span></span>

<span data-ttu-id="a00a2-219">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="a00a2-219">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-220">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="a00a2-220">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-221">97</span><span class="sxs-lookup"><span data-stu-id="a00a2-221">97</span></span>

<span data-ttu-id="a00a2-222">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="a00a2-222">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-223">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="a00a2-223">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-224">98</span><span class="sxs-lookup"><span data-stu-id="a00a2-224">98</span></span>

<span data-ttu-id="a00a2-225">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="a00a2-225">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-226">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="a00a2-226">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-227">100</span><span class="sxs-lookup"><span data-stu-id="a00a2-227">100</span></span>

<span data-ttu-id="a00a2-228">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="a00a2-228">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="a00a2-229">**其他**</span><span class="sxs-lookup"><span data-stu-id="a00a2-229">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="a00a2-230">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="a00a2-230">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="a00a2-231">範例</span><span class="sxs-lookup"><span data-stu-id="a00a2-231">Examples</span></span>

<span data-ttu-id="a00a2-232">下列 VBScript 程式碼範例會釋放目前在電腦上使用的所有 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="a00a2-232">The following VBScript code sample releases all the DHCP leases currently in use on a computer.</span></span>


```VB
On Error Resume Next 
 
strComputer = "." 
Set objWMIService = GetObject("winmgmts:" _ 
    & "{impersonationLevel=impersonate}!\\" & strComputer & "\root\cimv2") 
 
Set objNetworkSettings = objWMIService.Get("Win32_NetworkAdapterConfiguration") 
objNetworkSettings.ReleaseDHCPLeaseAll() 
```



## <a name="requirements"></a><span data-ttu-id="a00a2-233">規格需求</span><span class="sxs-lookup"><span data-stu-id="a00a2-233">Requirements</span></span>



| <span data-ttu-id="a00a2-234">需求</span><span class="sxs-lookup"><span data-stu-id="a00a2-234">Requirement</span></span> | <span data-ttu-id="a00a2-235">值</span><span class="sxs-lookup"><span data-stu-id="a00a2-235">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a00a2-236">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a00a2-236">Minimum supported client</span></span><br/> | <span data-ttu-id="a00a2-237">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a00a2-237">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a00a2-238">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a00a2-238">Minimum supported server</span></span><br/> | <span data-ttu-id="a00a2-239">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a00a2-239">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a00a2-240">命名空間</span><span class="sxs-lookup"><span data-stu-id="a00a2-240">Namespace</span></span><br/>                | <span data-ttu-id="a00a2-241">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="a00a2-241">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a00a2-242">MOF</span><span class="sxs-lookup"><span data-stu-id="a00a2-242">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a00a2-243"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="a00a2-243"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a00a2-244">DLL</span><span class="sxs-lookup"><span data-stu-id="a00a2-244">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a00a2-245"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a00a2-245"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a00a2-246">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a00a2-246">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a00a2-247">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="a00a2-247">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="a00a2-248">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="a00a2-248">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="a00a2-249">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="a00a2-249">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="a00a2-250">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="a00a2-250">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="a00a2-251">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="a00a2-251">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

