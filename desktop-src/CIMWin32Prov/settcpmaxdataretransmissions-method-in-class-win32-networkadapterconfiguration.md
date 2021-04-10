---
description: SetTcpMaxDataRetransmissions WMI 類別靜態方法是用來設定在中止連接之前 TCP 重新傳輸個別資料區段的次數。
ms.assetid: 1b5407ee-8e2b-4aed-a17a-58d960f976f2
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetTcpMaxDataRetransmissions 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetTcpMaxDataRetransmissions
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 59998888eb2aed170b626fb4cb61780cbe0cb6e4
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111613"
---
# <a name="settcpmaxdataretransmissions-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="c5220-103">Win32 >networkadapterconfiguration 類別的 SetTcpMaxDataRetransmissions 方法 \_</span><span class="sxs-lookup"><span data-stu-id="c5220-103">SetTcpMaxDataRetransmissions method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="c5220-104">**SetTcpMaxDataRetransmissions** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定在中止連接之前 TCP 重新傳輸個別資料區段的次數。</span><span class="sxs-lookup"><span data-stu-id="c5220-104">The **SetTcpMaxDataRetransmissions** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of times TCP retransmits an individual data segment before aborting the connection.</span></span>

<span data-ttu-id="c5220-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="c5220-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="c5220-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="c5220-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="c5220-107">語法</span><span class="sxs-lookup"><span data-stu-id="c5220-107">Syntax</span></span>


```mof
uint32 SetTcpMaxDataRetransmissions(
  [in] uint32 TcpMaxDataRetransmissions
);
```



## <a name="parameters"></a><span data-ttu-id="c5220-108">參數</span><span class="sxs-lookup"><span data-stu-id="c5220-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5220-109">*TcpMaxDataRetransmissions* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5220-109">*TcpMaxDataRetransmissions* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5220-110">在中止連接之前 TCP 重新傳輸個別資料區段的次數。</span><span class="sxs-lookup"><span data-stu-id="c5220-110">Number of times TCP retransmits an individual data segment before aborting the connection.</span></span> <span data-ttu-id="c5220-111">有效範圍： 0-0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="c5220-111">Valid range: 0 - 0xFFFFFFFF.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5220-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5220-112">Return value</span></span>

<span data-ttu-id="c5220-113">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="c5220-113">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="c5220-114">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="c5220-114">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="c5220-115">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="c5220-115">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="c5220-116">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="c5220-116">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-117">0</span><span class="sxs-lookup"><span data-stu-id="c5220-117">0</span></span>

<span data-ttu-id="c5220-118">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="c5220-118">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-119">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="c5220-119">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-120">1</span><span class="sxs-lookup"><span data-stu-id="c5220-120">1</span></span>

<span data-ttu-id="c5220-121">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="c5220-121">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-122">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="c5220-122">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-123">64</span><span class="sxs-lookup"><span data-stu-id="c5220-123">64</span></span>

<span data-ttu-id="c5220-124">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="c5220-124">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-125">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="c5220-125">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-126">65</span><span class="sxs-lookup"><span data-stu-id="c5220-126">65</span></span>

<span data-ttu-id="c5220-127">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="c5220-127">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-128">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="c5220-128">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-129">66</span><span class="sxs-lookup"><span data-stu-id="c5220-129">66</span></span>

<span data-ttu-id="c5220-130">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="c5220-130">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-131">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="c5220-131">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-132">67</span><span class="sxs-lookup"><span data-stu-id="c5220-132">67</span></span>

<span data-ttu-id="c5220-133">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="c5220-133">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-134">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="c5220-134">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-135">68</span><span class="sxs-lookup"><span data-stu-id="c5220-135">68</span></span>

<span data-ttu-id="c5220-136">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="c5220-136">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-137">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="c5220-137">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-138">69</span><span class="sxs-lookup"><span data-stu-id="c5220-138">69</span></span>

<span data-ttu-id="c5220-139">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="c5220-139">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-140">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="c5220-140">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-141">70</span><span class="sxs-lookup"><span data-stu-id="c5220-141">70</span></span>

<span data-ttu-id="c5220-142">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="c5220-142">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-143">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="c5220-143">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-144">71</span><span class="sxs-lookup"><span data-stu-id="c5220-144">71</span></span>

<span data-ttu-id="c5220-145">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="c5220-145">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-146">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="c5220-146">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-147">72</span><span class="sxs-lookup"><span data-stu-id="c5220-147">72</span></span>

<span data-ttu-id="c5220-148">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="c5220-148">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-149">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="c5220-149">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-150">73</span><span class="sxs-lookup"><span data-stu-id="c5220-150">73</span></span>

<span data-ttu-id="c5220-151">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="c5220-151">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-152">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="c5220-152">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-153">74</span><span class="sxs-lookup"><span data-stu-id="c5220-153">74</span></span>

<span data-ttu-id="c5220-154">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="c5220-154">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-155">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="c5220-155">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-156">75</span><span class="sxs-lookup"><span data-stu-id="c5220-156">75</span></span>

<span data-ttu-id="c5220-157">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="c5220-157">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-158">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="c5220-158">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-159">76</span><span class="sxs-lookup"><span data-stu-id="c5220-159">76</span></span>

<span data-ttu-id="c5220-160">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="c5220-160">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-161">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="c5220-161">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-162">77</span><span class="sxs-lookup"><span data-stu-id="c5220-162">77</span></span>

<span data-ttu-id="c5220-163">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="c5220-163">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-164">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="c5220-164">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-165">78</span><span class="sxs-lookup"><span data-stu-id="c5220-165">78</span></span>

<span data-ttu-id="c5220-166">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="c5220-166">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-167">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="c5220-167">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-168">79</span><span class="sxs-lookup"><span data-stu-id="c5220-168">79</span></span>

<span data-ttu-id="c5220-169">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="c5220-169">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-170">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="c5220-170">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-171">80</span><span class="sxs-lookup"><span data-stu-id="c5220-171">80</span></span>

<span data-ttu-id="c5220-172">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="c5220-172">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-173">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="c5220-173">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-174">81</span><span class="sxs-lookup"><span data-stu-id="c5220-174">81</span></span>

<span data-ttu-id="c5220-175">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="c5220-175">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-176">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="c5220-176">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-177">82</span><span class="sxs-lookup"><span data-stu-id="c5220-177">82</span></span>

<span data-ttu-id="c5220-178">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="c5220-178">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-179">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="c5220-179">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-180">83</span><span class="sxs-lookup"><span data-stu-id="c5220-180">83</span></span>

<span data-ttu-id="c5220-181">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="c5220-181">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-182">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="c5220-182">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-183">84</span><span class="sxs-lookup"><span data-stu-id="c5220-183">84</span></span>

<span data-ttu-id="c5220-184">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="c5220-184">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-185">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="c5220-185">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-186">85</span><span class="sxs-lookup"><span data-stu-id="c5220-186">85</span></span>

<span data-ttu-id="c5220-187">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="c5220-187">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-188">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="c5220-188">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-189">86</span><span class="sxs-lookup"><span data-stu-id="c5220-189">86</span></span>

<span data-ttu-id="c5220-190">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="c5220-190">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-191">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="c5220-191">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-192">87</span><span class="sxs-lookup"><span data-stu-id="c5220-192">87</span></span>

<span data-ttu-id="c5220-193">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="c5220-193">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-194">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="c5220-194">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-195">88</span><span class="sxs-lookup"><span data-stu-id="c5220-195">88</span></span>

<span data-ttu-id="c5220-196">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="c5220-196">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-197">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="c5220-197">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-198">89</span><span class="sxs-lookup"><span data-stu-id="c5220-198">89</span></span>

<span data-ttu-id="c5220-199">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="c5220-199">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-200">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="c5220-200">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-201">90</span><span class="sxs-lookup"><span data-stu-id="c5220-201">90</span></span>

<span data-ttu-id="c5220-202">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="c5220-202">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-203">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="c5220-203">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-204">91</span><span class="sxs-lookup"><span data-stu-id="c5220-204">91</span></span>

<span data-ttu-id="c5220-205">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="c5220-205">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-206">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="c5220-206">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-207">92</span><span class="sxs-lookup"><span data-stu-id="c5220-207">92</span></span>

<span data-ttu-id="c5220-208">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="c5220-208">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-209">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="c5220-209">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-210">93</span><span class="sxs-lookup"><span data-stu-id="c5220-210">93</span></span>

<span data-ttu-id="c5220-211">已經存在。</span><span class="sxs-lookup"><span data-stu-id="c5220-211">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-212">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="c5220-212">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-213">94</span><span class="sxs-lookup"><span data-stu-id="c5220-213">94</span></span>

<span data-ttu-id="c5220-214">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="c5220-214">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-215">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="c5220-215">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-216">95</span><span class="sxs-lookup"><span data-stu-id="c5220-216">95</span></span>

<span data-ttu-id="c5220-217">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="c5220-217">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-218">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="c5220-218">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-219">96</span><span class="sxs-lookup"><span data-stu-id="c5220-219">96</span></span>

<span data-ttu-id="c5220-220">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="c5220-220">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-221">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="c5220-221">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-222">97</span><span class="sxs-lookup"><span data-stu-id="c5220-222">97</span></span>

<span data-ttu-id="c5220-223">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="c5220-223">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-224">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="c5220-224">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-225">98</span><span class="sxs-lookup"><span data-stu-id="c5220-225">98</span></span>

<span data-ttu-id="c5220-226">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="c5220-226">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-227">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="c5220-227">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-228">100</span><span class="sxs-lookup"><span data-stu-id="c5220-228">100</span></span>

<span data-ttu-id="c5220-229">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="c5220-229">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="c5220-230">**其他**</span><span class="sxs-lookup"><span data-stu-id="c5220-230">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="c5220-231">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="c5220-231">101 4294967295</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c5220-232">備註</span><span class="sxs-lookup"><span data-stu-id="c5220-232">Remarks</span></span>

<span data-ttu-id="c5220-233">重新傳輸超時會加倍，並在連線上每次重新傳輸。</span><span class="sxs-lookup"><span data-stu-id="c5220-233">The retransmission timeout doubles with each successive retransmission on a connection.</span></span>

## <a name="examples"></a><span data-ttu-id="c5220-234">範例</span><span class="sxs-lookup"><span data-stu-id="c5220-234">Examples</span></span>

<span data-ttu-id="c5220-235">[ [修改允許的 TCP 資料重新傳輸的最大值](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) ] VBScript 範例會設定 tcp 在放棄工作之前，會嘗試重新傳輸個別資料區段的次數。</span><span class="sxs-lookup"><span data-stu-id="c5220-235">The [Modify the Maximum Allowed TCP Data Retransmissions](https://Gallery.TechNet.Microsoft.Com/8a581692-7950-412e-bd28-74f223b27827) VBScript sample configures the number of times TCP will attempt to retransmit an individual data segment before abandoning the effort.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5220-236">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5220-236">Requirements</span></span>



| <span data-ttu-id="c5220-237">需求</span><span class="sxs-lookup"><span data-stu-id="c5220-237">Requirement</span></span> | <span data-ttu-id="c5220-238">值</span><span class="sxs-lookup"><span data-stu-id="c5220-238">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5220-239">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5220-239">Minimum supported client</span></span><br/> | <span data-ttu-id="c5220-240">Windows Vista、Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c5220-240">Windows Vista, Windows Vista</span></span><br/>                                                 |
| <span data-ttu-id="c5220-241">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5220-241">Minimum supported server</span></span><br/> | <span data-ttu-id="c5220-242">Windows Server 2008、Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c5220-242">Windows Server 2008, Windows Server 2008</span></span><br/>                                     |
| <span data-ttu-id="c5220-243">命名空間</span><span class="sxs-lookup"><span data-stu-id="c5220-243">Namespace</span></span><br/>                | <span data-ttu-id="c5220-244">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="c5220-244">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c5220-245">MOF</span><span class="sxs-lookup"><span data-stu-id="c5220-245">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c5220-246"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="c5220-246"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c5220-247">DLL</span><span class="sxs-lookup"><span data-stu-id="c5220-247">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5220-248"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5220-248"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5220-249">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5220-249">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5220-250">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="c5220-250">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="c5220-251">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="c5220-251">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="c5220-252">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="c5220-252">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="c5220-253">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="c5220-253">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="c5220-254">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="c5220-254">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

