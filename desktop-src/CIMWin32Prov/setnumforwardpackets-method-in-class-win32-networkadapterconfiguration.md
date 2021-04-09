---
description: SetNumForwardPackets WMI 類別靜態方法是用來設定為路由器封包佇列配置的 IP 封包標頭數目。 當所有標頭都在使用中時，路由器會開始隨機捨棄佇列中的封包。
ms.assetid: cadc7565-4cad-4e0f-a1eb-bf99d333bb28
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetNumForwardPackets 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetNumForwardPackets
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: f46ecd62766b5df642dff1e52614171a513a8fca
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103688960"
---
# <a name="setnumforwardpackets-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="10e1f-104">Win32 >networkadapterconfiguration 類別的 SetNumForwardPackets 方法 \_</span><span class="sxs-lookup"><span data-stu-id="10e1f-104">SetNumForwardPackets method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="10e1f-105">**SetNumForwardPackets** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定為路由器封包佇列配置的 IP 封包標頭數目。</span><span class="sxs-lookup"><span data-stu-id="10e1f-105">The **SetNumForwardPackets** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="10e1f-106">當所有標頭都在使用中時，路由器會開始隨機捨棄佇列中的封包。</span><span class="sxs-lookup"><span data-stu-id="10e1f-106">When all headers are in use, the router will begin to discard packets from the queue at random.</span></span>

<span data-ttu-id="10e1f-107">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="10e1f-107">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="10e1f-108">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="10e1f-108">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="10e1f-109">語法</span><span class="sxs-lookup"><span data-stu-id="10e1f-109">Syntax</span></span>


```mof
uint32 SetNumForwardPackets(
  [in] uint32 NumForwardPackets
);
```



## <a name="parameters"></a><span data-ttu-id="10e1f-110">參數</span><span class="sxs-lookup"><span data-stu-id="10e1f-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="10e1f-111">*NumForwardPackets* \[在\]</span><span class="sxs-lookup"><span data-stu-id="10e1f-111">*NumForwardPackets* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-112">配置給路由器封包佇列的 IP 封包標頭數目。</span><span class="sxs-lookup"><span data-stu-id="10e1f-112">Number of IP packet headers allocated for the router packet queue.</span></span> <span data-ttu-id="10e1f-113">這應該至少等於 [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) 屬性的值除以連線到路由器的網路 IP 資料大小上限。</span><span class="sxs-lookup"><span data-stu-id="10e1f-113">This should be at least as large as the value of the [**ForwardBufferMemory**](win32-networkadapterconfiguration.md) property divided by the maximum IP data size of the networks connected to the router.</span></span> <span data-ttu-id="10e1f-114">它應該不會大於 **ForwardBufferMemory** 值除以256，因為每個封包都需要至少256個位元組的轉送緩衝區記憶體。</span><span class="sxs-lookup"><span data-stu-id="10e1f-114">It should be no larger than the **ForwardBufferMemory** value divided by 256, since at least 256 bytes of forward buffer memory are required by each packet.</span></span> <span data-ttu-id="10e1f-115">給定 **ForwardBufferMemory** 大小的最佳轉寄封包數目，取決於網路上所傳送的流量類型，而且會在這兩個值之間的某處。</span><span class="sxs-lookup"><span data-stu-id="10e1f-115">The optimal number of forward packets for a given **ForwardBufferMemory** size depends on the type of traffic carried on the network, and will be somewhere between these two values.</span></span> <span data-ttu-id="10e1f-116">如果路由器已停用，則會忽略此參數，且不會配置任何標頭。</span><span class="sxs-lookup"><span data-stu-id="10e1f-116">If the router is disabled, this parameter is ignored and no headers are allocated.</span></span> <span data-ttu-id="10e1f-117">有效範圍： 1-0xFFFFFFFE。</span><span class="sxs-lookup"><span data-stu-id="10e1f-117">Valid range: 1 - 0xFFFFFFFE.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="10e1f-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="10e1f-118">Return value</span></span>

<span data-ttu-id="10e1f-119">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="10e1f-119">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="10e1f-120">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="10e1f-120">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="10e1f-121">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="10e1f-121">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="10e1f-122">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="10e1f-122">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-123">0</span><span class="sxs-lookup"><span data-stu-id="10e1f-123">0</span></span>

<span data-ttu-id="10e1f-124">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="10e1f-124">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-125">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="10e1f-125">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-126">1</span><span class="sxs-lookup"><span data-stu-id="10e1f-126">1</span></span>

<span data-ttu-id="10e1f-127">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="10e1f-127">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-128">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="10e1f-128">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-129">64</span><span class="sxs-lookup"><span data-stu-id="10e1f-129">64</span></span>

<span data-ttu-id="10e1f-130">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="10e1f-130">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-131">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="10e1f-131">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-132">65</span><span class="sxs-lookup"><span data-stu-id="10e1f-132">65</span></span>

<span data-ttu-id="10e1f-133">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="10e1f-133">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-134">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="10e1f-134">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-135">66</span><span class="sxs-lookup"><span data-stu-id="10e1f-135">66</span></span>

<span data-ttu-id="10e1f-136">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="10e1f-136">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-137">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="10e1f-137">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-138">67</span><span class="sxs-lookup"><span data-stu-id="10e1f-138">67</span></span>

<span data-ttu-id="10e1f-139">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="10e1f-139">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-140">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="10e1f-140">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-141">68</span><span class="sxs-lookup"><span data-stu-id="10e1f-141">68</span></span>

<span data-ttu-id="10e1f-142">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="10e1f-142">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-143">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="10e1f-143">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-144">69</span><span class="sxs-lookup"><span data-stu-id="10e1f-144">69</span></span>

<span data-ttu-id="10e1f-145">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="10e1f-145">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-146">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="10e1f-146">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-147">70</span><span class="sxs-lookup"><span data-stu-id="10e1f-147">70</span></span>

<span data-ttu-id="10e1f-148">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="10e1f-148">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-149">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="10e1f-149">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-150">71</span><span class="sxs-lookup"><span data-stu-id="10e1f-150">71</span></span>

<span data-ttu-id="10e1f-151">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="10e1f-151">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-152">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="10e1f-152">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-153">72</span><span class="sxs-lookup"><span data-stu-id="10e1f-153">72</span></span>

<span data-ttu-id="10e1f-154">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="10e1f-154">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-155">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="10e1f-155">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-156">73</span><span class="sxs-lookup"><span data-stu-id="10e1f-156">73</span></span>

<span data-ttu-id="10e1f-157">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="10e1f-157">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-158">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="10e1f-158">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-159">74</span><span class="sxs-lookup"><span data-stu-id="10e1f-159">74</span></span>

<span data-ttu-id="10e1f-160">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="10e1f-160">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-161">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="10e1f-161">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-162">75</span><span class="sxs-lookup"><span data-stu-id="10e1f-162">75</span></span>

<span data-ttu-id="10e1f-163">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="10e1f-163">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-164">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="10e1f-164">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-165">76</span><span class="sxs-lookup"><span data-stu-id="10e1f-165">76</span></span>

<span data-ttu-id="10e1f-166">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="10e1f-166">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-167">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="10e1f-167">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-168">77</span><span class="sxs-lookup"><span data-stu-id="10e1f-168">77</span></span>

<span data-ttu-id="10e1f-169">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="10e1f-169">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-170">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="10e1f-170">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-171">78</span><span class="sxs-lookup"><span data-stu-id="10e1f-171">78</span></span>

<span data-ttu-id="10e1f-172">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="10e1f-172">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-173">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="10e1f-173">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-174">79</span><span class="sxs-lookup"><span data-stu-id="10e1f-174">79</span></span>

<span data-ttu-id="10e1f-175">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="10e1f-175">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-176">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="10e1f-176">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-177">80</span><span class="sxs-lookup"><span data-stu-id="10e1f-177">80</span></span>

<span data-ttu-id="10e1f-178">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="10e1f-178">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-179">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="10e1f-179">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-180">81</span><span class="sxs-lookup"><span data-stu-id="10e1f-180">81</span></span>

<span data-ttu-id="10e1f-181">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="10e1f-181">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-182">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="10e1f-182">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-183">82</span><span class="sxs-lookup"><span data-stu-id="10e1f-183">82</span></span>

<span data-ttu-id="10e1f-184">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="10e1f-184">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-185">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="10e1f-185">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-186">83</span><span class="sxs-lookup"><span data-stu-id="10e1f-186">83</span></span>

<span data-ttu-id="10e1f-187">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="10e1f-187">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-188">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="10e1f-188">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-189">84</span><span class="sxs-lookup"><span data-stu-id="10e1f-189">84</span></span>

<span data-ttu-id="10e1f-190">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="10e1f-190">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-191">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="10e1f-191">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-192">85</span><span class="sxs-lookup"><span data-stu-id="10e1f-192">85</span></span>

<span data-ttu-id="10e1f-193">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="10e1f-193">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-194">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="10e1f-194">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-195">86</span><span class="sxs-lookup"><span data-stu-id="10e1f-195">86</span></span>

<span data-ttu-id="10e1f-196">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="10e1f-196">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-197">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="10e1f-197">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-198">87</span><span class="sxs-lookup"><span data-stu-id="10e1f-198">87</span></span>

<span data-ttu-id="10e1f-199">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="10e1f-199">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-200">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="10e1f-200">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-201">88</span><span class="sxs-lookup"><span data-stu-id="10e1f-201">88</span></span>

<span data-ttu-id="10e1f-202">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="10e1f-202">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-203">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="10e1f-203">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-204">89</span><span class="sxs-lookup"><span data-stu-id="10e1f-204">89</span></span>

<span data-ttu-id="10e1f-205">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="10e1f-205">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-206">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="10e1f-206">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-207">90</span><span class="sxs-lookup"><span data-stu-id="10e1f-207">90</span></span>

<span data-ttu-id="10e1f-208">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="10e1f-208">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-209">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="10e1f-209">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-210">91</span><span class="sxs-lookup"><span data-stu-id="10e1f-210">91</span></span>

<span data-ttu-id="10e1f-211">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="10e1f-211">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-212">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="10e1f-212">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-213">92</span><span class="sxs-lookup"><span data-stu-id="10e1f-213">92</span></span>

<span data-ttu-id="10e1f-214">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="10e1f-214">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-215">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="10e1f-215">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-216">93</span><span class="sxs-lookup"><span data-stu-id="10e1f-216">93</span></span>

<span data-ttu-id="10e1f-217">已經存在。</span><span class="sxs-lookup"><span data-stu-id="10e1f-217">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-218">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="10e1f-218">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-219">94</span><span class="sxs-lookup"><span data-stu-id="10e1f-219">94</span></span>

<span data-ttu-id="10e1f-220">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="10e1f-220">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-221">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="10e1f-221">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-222">95</span><span class="sxs-lookup"><span data-stu-id="10e1f-222">95</span></span>

<span data-ttu-id="10e1f-223">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="10e1f-223">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-224">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="10e1f-224">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-225">96</span><span class="sxs-lookup"><span data-stu-id="10e1f-225">96</span></span>

<span data-ttu-id="10e1f-226">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="10e1f-226">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-227">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="10e1f-227">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-228">97</span><span class="sxs-lookup"><span data-stu-id="10e1f-228">97</span></span>

<span data-ttu-id="10e1f-229">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="10e1f-229">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-230">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="10e1f-230">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-231">98</span><span class="sxs-lookup"><span data-stu-id="10e1f-231">98</span></span>

<span data-ttu-id="10e1f-232">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="10e1f-232">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-233">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="10e1f-233">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-234">100</span><span class="sxs-lookup"><span data-stu-id="10e1f-234">100</span></span>

<span data-ttu-id="10e1f-235">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="10e1f-235">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="10e1f-236">**其他**</span><span class="sxs-lookup"><span data-stu-id="10e1f-236">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="10e1f-237">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="10e1f-237">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="10e1f-238">範例</span><span class="sxs-lookup"><span data-stu-id="10e1f-238">Examples</span></span>

<span data-ttu-id="10e1f-239">[ [修改允許的轉寄封包數目](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) ] VBScript 範例會設定配置給路由器封包佇列的轉寄封包數目。</span><span class="sxs-lookup"><span data-stu-id="10e1f-239">The [Modify the Number of Allowed Forward Packets](https://Gallery.TechNet.Microsoft.Com/4123c28e-25c4-444e-818b-67bdbcc0cd4c) VBScript sample configures the number of forward packets allocated to the router packet queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="10e1f-240">規格需求</span><span class="sxs-lookup"><span data-stu-id="10e1f-240">Requirements</span></span>



| <span data-ttu-id="10e1f-241">需求</span><span class="sxs-lookup"><span data-stu-id="10e1f-241">Requirement</span></span> | <span data-ttu-id="10e1f-242">值</span><span class="sxs-lookup"><span data-stu-id="10e1f-242">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="10e1f-243">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10e1f-243">Minimum supported client</span></span><br/> | <span data-ttu-id="10e1f-244">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="10e1f-244">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="10e1f-245">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10e1f-245">Minimum supported server</span></span><br/> | <span data-ttu-id="10e1f-246">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="10e1f-246">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="10e1f-247">命名空間</span><span class="sxs-lookup"><span data-stu-id="10e1f-247">Namespace</span></span><br/>                | <span data-ttu-id="10e1f-248">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="10e1f-248">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="10e1f-249">MOF</span><span class="sxs-lookup"><span data-stu-id="10e1f-249">MOF</span></span><br/>                      | <dl> <span data-ttu-id="10e1f-250"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="10e1f-250"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="10e1f-251">DLL</span><span class="sxs-lookup"><span data-stu-id="10e1f-251">DLL</span></span><br/>                      | <dl> <span data-ttu-id="10e1f-252"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="10e1f-252"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="10e1f-253">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10e1f-253">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10e1f-254">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="10e1f-254">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="10e1f-255">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="10e1f-255">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="10e1f-256">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="10e1f-256">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="10e1f-257">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="10e1f-257">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="10e1f-258">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="10e1f-258">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

