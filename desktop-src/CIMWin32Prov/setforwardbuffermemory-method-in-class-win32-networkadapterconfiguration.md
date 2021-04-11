---
description: SetForwardBufferMemory WMI 類別靜態方法是用來指定在路由器封包佇列中儲存封包資料所配置的記憶體數量。
ms.assetid: e76452e8-2ee8-4d39-9405-33b0aeeac74d
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetForwardBufferMemory 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetForwardBufferMemory
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 30179610e6eee121a86119fa347067b40ef04c2f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847391"
---
# <a name="setforwardbuffermemory-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="60b15-103">Win32 >networkadapterconfiguration 類別的 SetForwardBufferMemory 方法 \_</span><span class="sxs-lookup"><span data-stu-id="60b15-103">SetForwardBufferMemory method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="60b15-104">**SetForwardBufferMemory** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來指定在路由器封包佇列中儲存封包資料所配置的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="60b15-104">The **SetForwardBufferMemory** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to specify how much memory IP allocates to store packet data in the router packet queue.</span></span>

<span data-ttu-id="60b15-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="60b15-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="60b15-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="60b15-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="60b15-107">語法</span><span class="sxs-lookup"><span data-stu-id="60b15-107">Syntax</span></span>


```mof
uint32 SetForwardBufferMemory(
  [in] uint32 ForwardBufferMemory
);
```



## <a name="parameters"></a><span data-ttu-id="60b15-108">參數</span><span class="sxs-lookup"><span data-stu-id="60b15-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60b15-109">*ForwardBufferMemory* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60b15-109">*ForwardBufferMemory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60b15-110">用來儲存封包資料的路由器封包佇列大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="60b15-110">Size, in bytes, of the router packet queue used to store packet data.</span></span> <span data-ttu-id="60b15-111">預設值為 74240 (50 1480 位元組封包，四捨五入為 256) 的倍數。</span><span class="sxs-lookup"><span data-stu-id="60b15-111">The default value is 74240 (fifty 1480-byte packets, rounded to a multiple of 256).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60b15-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="60b15-112">Return value</span></span>

<span data-ttu-id="60b15-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="60b15-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="60b15-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="60b15-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="60b15-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="60b15-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="60b15-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="60b15-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-117">0</span><span class="sxs-lookup"><span data-stu-id="60b15-117">0</span></span>

<span data-ttu-id="60b15-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="60b15-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="60b15-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-120">1</span><span class="sxs-lookup"><span data-stu-id="60b15-120">1</span></span>

<span data-ttu-id="60b15-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="60b15-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="60b15-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-123">64</span><span class="sxs-lookup"><span data-stu-id="60b15-123">64</span></span>

<span data-ttu-id="60b15-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="60b15-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="60b15-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-126">65</span><span class="sxs-lookup"><span data-stu-id="60b15-126">65</span></span>

<span data-ttu-id="60b15-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="60b15-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="60b15-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-129">66</span><span class="sxs-lookup"><span data-stu-id="60b15-129">66</span></span>

<span data-ttu-id="60b15-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="60b15-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="60b15-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-132">67</span><span class="sxs-lookup"><span data-stu-id="60b15-132">67</span></span>

<span data-ttu-id="60b15-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="60b15-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="60b15-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-135">68</span><span class="sxs-lookup"><span data-stu-id="60b15-135">68</span></span>

<span data-ttu-id="60b15-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="60b15-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="60b15-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-138">69</span><span class="sxs-lookup"><span data-stu-id="60b15-138">69</span></span>

<span data-ttu-id="60b15-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="60b15-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="60b15-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-141">70</span><span class="sxs-lookup"><span data-stu-id="60b15-141">70</span></span>

<span data-ttu-id="60b15-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="60b15-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="60b15-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-144">71</span><span class="sxs-lookup"><span data-stu-id="60b15-144">71</span></span>

<span data-ttu-id="60b15-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="60b15-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="60b15-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-147">72</span><span class="sxs-lookup"><span data-stu-id="60b15-147">72</span></span>

<span data-ttu-id="60b15-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="60b15-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="60b15-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-150">73</span><span class="sxs-lookup"><span data-stu-id="60b15-150">73</span></span>

<span data-ttu-id="60b15-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="60b15-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="60b15-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-153">74</span><span class="sxs-lookup"><span data-stu-id="60b15-153">74</span></span>

<span data-ttu-id="60b15-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="60b15-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="60b15-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-156">75</span><span class="sxs-lookup"><span data-stu-id="60b15-156">75</span></span>

<span data-ttu-id="60b15-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="60b15-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="60b15-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-159">76</span><span class="sxs-lookup"><span data-stu-id="60b15-159">76</span></span>

<span data-ttu-id="60b15-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="60b15-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="60b15-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-162">77</span><span class="sxs-lookup"><span data-stu-id="60b15-162">77</span></span>

<span data-ttu-id="60b15-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="60b15-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="60b15-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-165">78</span><span class="sxs-lookup"><span data-stu-id="60b15-165">78</span></span>

<span data-ttu-id="60b15-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="60b15-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="60b15-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-168">79</span><span class="sxs-lookup"><span data-stu-id="60b15-168">79</span></span>

<span data-ttu-id="60b15-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="60b15-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="60b15-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-171">80</span><span class="sxs-lookup"><span data-stu-id="60b15-171">80</span></span>

<span data-ttu-id="60b15-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="60b15-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="60b15-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-174">81</span><span class="sxs-lookup"><span data-stu-id="60b15-174">81</span></span>

<span data-ttu-id="60b15-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="60b15-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="60b15-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-177">82</span><span class="sxs-lookup"><span data-stu-id="60b15-177">82</span></span>

<span data-ttu-id="60b15-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="60b15-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="60b15-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-180">83</span><span class="sxs-lookup"><span data-stu-id="60b15-180">83</span></span>

<span data-ttu-id="60b15-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="60b15-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="60b15-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-183">84</span><span class="sxs-lookup"><span data-stu-id="60b15-183">84</span></span>

<span data-ttu-id="60b15-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="60b15-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="60b15-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-186">85</span><span class="sxs-lookup"><span data-stu-id="60b15-186">85</span></span>

<span data-ttu-id="60b15-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="60b15-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="60b15-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-189">86</span><span class="sxs-lookup"><span data-stu-id="60b15-189">86</span></span>

<span data-ttu-id="60b15-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="60b15-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="60b15-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-192">87</span><span class="sxs-lookup"><span data-stu-id="60b15-192">87</span></span>

<span data-ttu-id="60b15-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="60b15-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="60b15-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-195">88</span><span class="sxs-lookup"><span data-stu-id="60b15-195">88</span></span>

<span data-ttu-id="60b15-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="60b15-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="60b15-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-198">89</span><span class="sxs-lookup"><span data-stu-id="60b15-198">89</span></span>

<span data-ttu-id="60b15-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="60b15-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="60b15-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-201">90</span><span class="sxs-lookup"><span data-stu-id="60b15-201">90</span></span>

<span data-ttu-id="60b15-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="60b15-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="60b15-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-204">91</span><span class="sxs-lookup"><span data-stu-id="60b15-204">91</span></span>

<span data-ttu-id="60b15-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="60b15-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="60b15-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-207">92</span><span class="sxs-lookup"><span data-stu-id="60b15-207">92</span></span>

<span data-ttu-id="60b15-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="60b15-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="60b15-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-210">93</span><span class="sxs-lookup"><span data-stu-id="60b15-210">93</span></span>

<span data-ttu-id="60b15-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="60b15-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="60b15-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-213">94</span><span class="sxs-lookup"><span data-stu-id="60b15-213">94</span></span>

<span data-ttu-id="60b15-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="60b15-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="60b15-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-216">95</span><span class="sxs-lookup"><span data-stu-id="60b15-216">95</span></span>

<span data-ttu-id="60b15-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="60b15-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="60b15-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-219">96</span><span class="sxs-lookup"><span data-stu-id="60b15-219">96</span></span>

<span data-ttu-id="60b15-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="60b15-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="60b15-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-222">97</span><span class="sxs-lookup"><span data-stu-id="60b15-222">97</span></span>

<span data-ttu-id="60b15-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="60b15-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="60b15-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-225">98</span><span class="sxs-lookup"><span data-stu-id="60b15-225">98</span></span>

<span data-ttu-id="60b15-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="60b15-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="60b15-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-228">100</span><span class="sxs-lookup"><span data-stu-id="60b15-228">100</span></span>

<span data-ttu-id="60b15-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="60b15-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="60b15-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="60b15-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="60b15-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="60b15-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60b15-232">備註</span><span class="sxs-lookup"><span data-stu-id="60b15-232">Remarks</span></span>

<span data-ttu-id="60b15-233">填滿此緩衝區空間時，路由器會開始從其佇列中隨機捨棄封包。</span><span class="sxs-lookup"><span data-stu-id="60b15-233">When this buffer space is filled, the router begins discarding packets at random from its queue.</span></span>

<span data-ttu-id="60b15-234">封包佇列資料緩衝區的長度為256個位元組，因此 *ForwardBufferMemory* 參數的值應該是256的倍數。</span><span class="sxs-lookup"><span data-stu-id="60b15-234">Packet queue data buffers are 256 bytes in length, so the value of the *ForwardBufferMemory* parameter should be a multiple of 256.</span></span> <span data-ttu-id="60b15-235">多個緩衝區會連結在一起，以取得較大的封包。</span><span class="sxs-lookup"><span data-stu-id="60b15-235">Multiple buffers are chained together for larger packets.</span></span> <span data-ttu-id="60b15-236">封包的 IP 標頭會分開儲存。</span><span class="sxs-lookup"><span data-stu-id="60b15-236">The IP header for a packet is stored separately.</span></span> <span data-ttu-id="60b15-237">如果未啟用 IP 路由器，則會忽略此參數，且不會配置任何緩衝區。</span><span class="sxs-lookup"><span data-stu-id="60b15-237">This parameter is ignored and no buffers are allocated if the IP router is not enabled.</span></span> <span data-ttu-id="60b15-238">緩衝區大小的範圍可以從網路的最大傳輸單位 (MTU) 到小於0xFFFFFFFF 的值。</span><span class="sxs-lookup"><span data-stu-id="60b15-238">The buffer size can range from the network Maximum Transmission Unit (MTU) to a value smaller than 0xFFFFFFFF.</span></span>

## <a name="examples"></a><span data-ttu-id="60b15-239">範例</span><span class="sxs-lookup"><span data-stu-id="60b15-239">Examples</span></span>

<span data-ttu-id="60b15-240">[修改所有網路介面卡的轉寄緩衝區記憶體](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524)VBScript 範例會設定電腦上所有網路介面卡的轉寄緩衝區記憶體。</span><span class="sxs-lookup"><span data-stu-id="60b15-240">The [Modify the Forward Buffer Memory for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/da5712dc-f854-4099-98a9-59c0ff20a524) VBScript sample configures the forward buffer memory for all network adapters on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="60b15-241">規格需求</span><span class="sxs-lookup"><span data-stu-id="60b15-241">Requirements</span></span>



| <span data-ttu-id="60b15-242">需求</span><span class="sxs-lookup"><span data-stu-id="60b15-242">Requirement</span></span> | <span data-ttu-id="60b15-243">值</span><span class="sxs-lookup"><span data-stu-id="60b15-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="60b15-244">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60b15-244">Minimum supported client</span></span><br/> | <span data-ttu-id="60b15-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="60b15-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="60b15-246">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60b15-246">Minimum supported server</span></span><br/> | <span data-ttu-id="60b15-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="60b15-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="60b15-248">命名空間</span><span class="sxs-lookup"><span data-stu-id="60b15-248">Namespace</span></span><br/>                | <span data-ttu-id="60b15-249">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="60b15-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="60b15-250">MOF</span><span class="sxs-lookup"><span data-stu-id="60b15-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="60b15-251"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="60b15-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="60b15-252">DLL</span><span class="sxs-lookup"><span data-stu-id="60b15-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="60b15-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="60b15-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="60b15-254">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60b15-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60b15-255">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="60b15-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="60b15-256">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="60b15-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="60b15-257">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="60b15-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="60b15-258">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="60b15-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="60b15-259">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="60b15-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

