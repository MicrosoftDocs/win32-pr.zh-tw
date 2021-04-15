---
description: SetIGMPLevel WMI 類別靜態方法是用來設定系統支援 IP 多播並參與網際網路群組管理通訊協定的範圍。
ms.assetid: 38877576-aa23-4841-b3ae-1a02bfdd70d8
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetIGMPLevel 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIGMPLevel
api_type:
- COM
api_location:
- CIMWin32.dll
ms.openlocfilehash: 97ead4df1d45b110c3d0a91976dc8eca6ffd72c7
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510608"
---
# <a name="setigmplevel-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="64c06-103">Win32 >networkadapterconfiguration 類別的 SetIGMPLevel 方法 \_</span><span class="sxs-lookup"><span data-stu-id="64c06-103">SetIGMPLevel method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="64c06-104">**SetIGMPLevel** [WMI 類別](/windows/desktop/WmiSdk/retrieving-a-class)靜態方法是用來設定系統支援 IP 多播並參與網際網路群組管理通訊協定的範圍。</span><span class="sxs-lookup"><span data-stu-id="64c06-104">The **SetIGMPLevel** [WMI class](/windows/desktop/WmiSdk/retrieving-a-class) static method is used to set the extent to which the system supports IP multicasting and participates in the Internet Group Management Protocol.</span></span>

<span data-ttu-id="64c06-105">本主題使用受控物件格式 (MOF) 語法。</span><span class="sxs-lookup"><span data-stu-id="64c06-105">This topic uses Managed Object Format (MOF) syntax.</span></span> <span data-ttu-id="64c06-106">如需使用此方法的詳細資訊，請參閱 [呼叫方法](/windows/desktop/WmiSdk/calling-a-method)。</span><span class="sxs-lookup"><span data-stu-id="64c06-106">For more information about using this method, see [Calling a Method](/windows/desktop/WmiSdk/calling-a-method).</span></span>

## <a name="syntax"></a><span data-ttu-id="64c06-107">語法</span><span class="sxs-lookup"><span data-stu-id="64c06-107">Syntax</span></span>


```mof
uint32 SetIGMPLevel(
  [in] uint8 IGMPLevel
);
```



## <a name="parameters"></a><span data-ttu-id="64c06-108">參數</span><span class="sxs-lookup"><span data-stu-id="64c06-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="64c06-109">*IGMPLevel* \[在\]</span><span class="sxs-lookup"><span data-stu-id="64c06-109">*IGMPLevel* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="64c06-110">資料類型： **整數**</span><span class="sxs-lookup"><span data-stu-id="64c06-110">Data type: **Integer**</span></span>

<span data-ttu-id="64c06-111">設定系統支援 IP 多播並參與網際網路群組管理通訊協定的層級。</span><span class="sxs-lookup"><span data-stu-id="64c06-111">Sets the level at which the system supports IP multicast and participates in the Internet Group Management Protocol.</span></span> <span data-ttu-id="64c06-112">在層級0，系統不會提供任何多播支援。</span><span class="sxs-lookup"><span data-stu-id="64c06-112">At level 0, the system provides no multicast support.</span></span> <span data-ttu-id="64c06-113">在層級1，系統可能只會傳送 IP 多播封包。</span><span class="sxs-lookup"><span data-stu-id="64c06-113">At level 1, the system may only send IP multicast packets.</span></span> <span data-ttu-id="64c06-114">在層級2，系統可能會傳送 IP 多播封包，並完整地參與 IGMP 以接收多播封包。</span><span class="sxs-lookup"><span data-stu-id="64c06-114">At level 2, the system may send IP multicast packets and fully participate in IGMP to receive multicast packets.</span></span>

<dt>

<span id="No_Multicast"></span><span id="no_multicast"></span><span id="NO_MULTICAST"></span>

<span data-ttu-id="64c06-115">**沒有多播** (0) </span><span class="sxs-lookup"><span data-stu-id="64c06-115">**No Multicast** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="IP_Multicast"></span><span id="ip_multicast"></span><span id="IP_MULTICAST"></span>

<span data-ttu-id="64c06-116">**IP 多播** (1) </span><span class="sxs-lookup"><span data-stu-id="64c06-116">**IP Multicast** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IP___IGMP_multicast"></span><span id="ip___igmp_multicast"></span><span id="IP___IGMP_MULTICAST"></span>

<span data-ttu-id="64c06-117">**IP & IGMP 多播** (2) </span><span class="sxs-lookup"><span data-stu-id="64c06-117">**IP & IGMP multicast** (2)</span></span>


<span data-ttu-id="64c06-118"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="64c06-118"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="64c06-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="64c06-119">Return value</span></span>

<span data-ttu-id="64c06-120">如果不需要重新開機，則會傳回 0 (零) 的值，1 (一個) 在需要重新開機時成功完成，而如果發生錯誤，則為不同的數位。</span><span class="sxs-lookup"><span data-stu-id="64c06-120">Returns a value of 0 (zero) for a successful completion when no reboot is required, 1 (one) for a successful completion when a reboot is required, and a different number if there is an error.</span></span> <span data-ttu-id="64c06-121">如需錯誤碼的詳細資訊，請參閱 [**WMI 錯誤常數**](/windows/desktop/WmiSdk/wmi-error-constants) 或 [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum)。</span><span class="sxs-lookup"><span data-stu-id="64c06-121">For more information on error codes, see [**WMI Error Constants**](/windows/desktop/WmiSdk/wmi-error-constants) or [**WbemErrorEnum**](/windows/desktop/api/wbemdisp/ne-wbemdisp-wbemerrorenum).</span></span> <span data-ttu-id="64c06-122">如需一般 **HRESULT** 值，請參閱 [系統錯誤碼](/windows/desktop/Debug/system-error-codes)。</span><span class="sxs-lookup"><span data-stu-id="64c06-122">For general **HRESULT** values, see [System Error Codes](/windows/desktop/Debug/system-error-codes).</span></span>

<dl> <dt>

<span data-ttu-id="64c06-123">**成功完成，不需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="64c06-123">**Successful completion, no reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-124">0</span><span class="sxs-lookup"><span data-stu-id="64c06-124">0</span></span>

<span data-ttu-id="64c06-125">成功完成，不需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="64c06-125">Successful completion, no reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-126">**成功完成，需要重新開機**</span><span class="sxs-lookup"><span data-stu-id="64c06-126">**Successful completion, reboot required**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-127">1</span><span class="sxs-lookup"><span data-stu-id="64c06-127">1</span></span>

<span data-ttu-id="64c06-128">成功完成，需要重新開機。</span><span class="sxs-lookup"><span data-stu-id="64c06-128">Successful completion, reboot required.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-129">**此平臺不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="64c06-129">**Method not supported on this platform**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-130">64</span><span class="sxs-lookup"><span data-stu-id="64c06-130">64</span></span>

<span data-ttu-id="64c06-131">此平臺不支援方法。</span><span class="sxs-lookup"><span data-stu-id="64c06-131">Method not supported on this platform.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-132">**未知的失敗**</span><span class="sxs-lookup"><span data-stu-id="64c06-132">**Unknown failure**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-133">65</span><span class="sxs-lookup"><span data-stu-id="64c06-133">65</span></span>

<span data-ttu-id="64c06-134">未知的失敗。</span><span class="sxs-lookup"><span data-stu-id="64c06-134">Unknown failure.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-135">**不正確子網路遮罩**</span><span class="sxs-lookup"><span data-stu-id="64c06-135">**Invalid subnet mask**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-136">66</span><span class="sxs-lookup"><span data-stu-id="64c06-136">66</span></span>

<span data-ttu-id="64c06-137">不正確子網路遮罩。</span><span class="sxs-lookup"><span data-stu-id="64c06-137">Invalid subnet mask.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-138">**處理傳回的實例時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="64c06-138">**An error occurred while processing an Instance that was returned**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-139">67</span><span class="sxs-lookup"><span data-stu-id="64c06-139">67</span></span>

<span data-ttu-id="64c06-140">處理傳回的實例時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="64c06-140">An error occurred while processing an instance that was returned.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-141">**不正確輸入參數**</span><span class="sxs-lookup"><span data-stu-id="64c06-141">**Invalid input parameter**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-142">68</span><span class="sxs-lookup"><span data-stu-id="64c06-142">68</span></span>

<span data-ttu-id="64c06-143">不正確輸入參數。</span><span class="sxs-lookup"><span data-stu-id="64c06-143">Invalid input parameter.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-144">**指定了超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="64c06-144">**More than 5 gateways specified**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-145">69</span><span class="sxs-lookup"><span data-stu-id="64c06-145">69</span></span>

<span data-ttu-id="64c06-146">指定了五個以上的閘道。</span><span class="sxs-lookup"><span data-stu-id="64c06-146">More than five gateways specified.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-147">**不正確 IP 位址**</span><span class="sxs-lookup"><span data-stu-id="64c06-147">**Invalid IP address**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-148">70</span><span class="sxs-lookup"><span data-stu-id="64c06-148">70</span></span>

<span data-ttu-id="64c06-149">IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="64c06-149">Invalid IP address.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-150">**閘道 IP 位址無效**</span><span class="sxs-lookup"><span data-stu-id="64c06-150">**Invalid gateway IP address**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-151">71</span><span class="sxs-lookup"><span data-stu-id="64c06-151">71</span></span>

<span data-ttu-id="64c06-152">閘道 IP 位址無效。</span><span class="sxs-lookup"><span data-stu-id="64c06-152">Invalid gateway IP address.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-153">**存取所要求資訊的登錄時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="64c06-153">**An error occurred while accessing the Registry for the requested information**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-154">72</span><span class="sxs-lookup"><span data-stu-id="64c06-154">72</span></span>

<span data-ttu-id="64c06-155">存取所要求資訊的登錄時發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="64c06-155">An error occurred while accessing the registry for the requested information.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-156">**不正確功能變數名稱**</span><span class="sxs-lookup"><span data-stu-id="64c06-156">**Invalid domain name**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-157">73</span><span class="sxs-lookup"><span data-stu-id="64c06-157">73</span></span>

<span data-ttu-id="64c06-158">功能變數名稱無效。</span><span class="sxs-lookup"><span data-stu-id="64c06-158">Invalid domain name.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-159">**不正確主機名稱**</span><span class="sxs-lookup"><span data-stu-id="64c06-159">**Invalid host name**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-160">74</span><span class="sxs-lookup"><span data-stu-id="64c06-160">74</span></span>

<span data-ttu-id="64c06-161">不正確主機名稱。</span><span class="sxs-lookup"><span data-stu-id="64c06-161">Invalid host name.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-162">**未定義主要/次要 WINS 伺服器**</span><span class="sxs-lookup"><span data-stu-id="64c06-162">**No primary/secondary WINS server defined**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-163">75</span><span class="sxs-lookup"><span data-stu-id="64c06-163">75</span></span>

<span data-ttu-id="64c06-164">未定義主要或次要 WINS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="64c06-164">No primary or secondary WINS server defined.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-165">**檔案無效**</span><span class="sxs-lookup"><span data-stu-id="64c06-165">**Invalid file**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-166">76</span><span class="sxs-lookup"><span data-stu-id="64c06-166">76</span></span>

<span data-ttu-id="64c06-167">檔案無效。</span><span class="sxs-lookup"><span data-stu-id="64c06-167">Invalid file.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-168">**系統路徑無效**</span><span class="sxs-lookup"><span data-stu-id="64c06-168">**Invalid system path**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-169">77</span><span class="sxs-lookup"><span data-stu-id="64c06-169">77</span></span>

<span data-ttu-id="64c06-170">不正確系統路徑。</span><span class="sxs-lookup"><span data-stu-id="64c06-170">Invalid system path.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-171">**檔案複製失敗**</span><span class="sxs-lookup"><span data-stu-id="64c06-171">**File copy failed**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-172">78</span><span class="sxs-lookup"><span data-stu-id="64c06-172">78</span></span>

<span data-ttu-id="64c06-173">檔案複製失敗。</span><span class="sxs-lookup"><span data-stu-id="64c06-173">File copy failed.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-174">**不正確安全性參數**</span><span class="sxs-lookup"><span data-stu-id="64c06-174">**Invalid security parameter**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-175">79</span><span class="sxs-lookup"><span data-stu-id="64c06-175">79</span></span>

<span data-ttu-id="64c06-176">不正確安全性參數。</span><span class="sxs-lookup"><span data-stu-id="64c06-176">Invalid security parameter.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-177">**無法設定 TCP/IP 服務**</span><span class="sxs-lookup"><span data-stu-id="64c06-177">**Unable to configure TCP/IP service**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-178">80</span><span class="sxs-lookup"><span data-stu-id="64c06-178">80</span></span>

<span data-ttu-id="64c06-179">無法設定 TCP/IP 服務。</span><span class="sxs-lookup"><span data-stu-id="64c06-179">Unable to configure TCP/IP service.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-180">**無法設定 DHCP 服務**</span><span class="sxs-lookup"><span data-stu-id="64c06-180">**Unable to configure DHCP service**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-181">81</span><span class="sxs-lookup"><span data-stu-id="64c06-181">81</span></span>

<span data-ttu-id="64c06-182">無法設定 DHCP 服務。</span><span class="sxs-lookup"><span data-stu-id="64c06-182">Unable to configure DHCP service.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-183">**無法更新 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="64c06-183">**Unable to renew DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-184">82</span><span class="sxs-lookup"><span data-stu-id="64c06-184">82</span></span>

<span data-ttu-id="64c06-185">無法更新 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="64c06-185">Unable to renew DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-186">**無法發行 DHCP 租用**</span><span class="sxs-lookup"><span data-stu-id="64c06-186">**Unable to release DHCP lease**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-187">83</span><span class="sxs-lookup"><span data-stu-id="64c06-187">83</span></span>

<span data-ttu-id="64c06-188">無法釋放 DHCP 租用。</span><span class="sxs-lookup"><span data-stu-id="64c06-188">Unable to release DHCP lease.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-189">**介面卡上未啟用 IP**</span><span class="sxs-lookup"><span data-stu-id="64c06-189">**IP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-190">84</span><span class="sxs-lookup"><span data-stu-id="64c06-190">84</span></span>

<span data-ttu-id="64c06-191">介面卡上未啟用 IP。</span><span class="sxs-lookup"><span data-stu-id="64c06-191">IP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-192">**未在介面卡上啟用 IPX**</span><span class="sxs-lookup"><span data-stu-id="64c06-192">**IPX not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-193">85</span><span class="sxs-lookup"><span data-stu-id="64c06-193">85</span></span>

<span data-ttu-id="64c06-194">未在介面卡上啟用 IPX。</span><span class="sxs-lookup"><span data-stu-id="64c06-194">IPX not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-195">**畫面格/網路編號界限錯誤**</span><span class="sxs-lookup"><span data-stu-id="64c06-195">**Frame/network number bounds error**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-196">86</span><span class="sxs-lookup"><span data-stu-id="64c06-196">86</span></span>

<span data-ttu-id="64c06-197">畫面格或網路編號界限錯誤。</span><span class="sxs-lookup"><span data-stu-id="64c06-197">Frame or network number bounds error.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-198">**不正確框架類型**</span><span class="sxs-lookup"><span data-stu-id="64c06-198">**Invalid frame type**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-199">87</span><span class="sxs-lookup"><span data-stu-id="64c06-199">87</span></span>

<span data-ttu-id="64c06-200">不正確畫面格類型。</span><span class="sxs-lookup"><span data-stu-id="64c06-200">Invalid frame type.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-201">**不正確網路編號**</span><span class="sxs-lookup"><span data-stu-id="64c06-201">**Invalid network number**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-202">88</span><span class="sxs-lookup"><span data-stu-id="64c06-202">88</span></span>

<span data-ttu-id="64c06-203">網路編號無效。</span><span class="sxs-lookup"><span data-stu-id="64c06-203">Invalid network number.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-204">**重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="64c06-204">**Duplicate network number**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-205">89</span><span class="sxs-lookup"><span data-stu-id="64c06-205">89</span></span>

<span data-ttu-id="64c06-206">網路編號重複。</span><span class="sxs-lookup"><span data-stu-id="64c06-206">Duplicate network number.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-207">**參數超出範圍**</span><span class="sxs-lookup"><span data-stu-id="64c06-207">**Parameter out of bounds**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-208">90</span><span class="sxs-lookup"><span data-stu-id="64c06-208">90</span></span>

<span data-ttu-id="64c06-209">參數超出範圍。</span><span class="sxs-lookup"><span data-stu-id="64c06-209">Parameter out of bounds.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-210">**拒絕存取**</span><span class="sxs-lookup"><span data-stu-id="64c06-210">**Access denied**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-211">91</span><span class="sxs-lookup"><span data-stu-id="64c06-211">91</span></span>

<span data-ttu-id="64c06-212">拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="64c06-212">Access denied.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-213">**記憶體不足**</span><span class="sxs-lookup"><span data-stu-id="64c06-213">**Out of memory**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-214">92</span><span class="sxs-lookup"><span data-stu-id="64c06-214">92</span></span>

<span data-ttu-id="64c06-215">記憶體不足。</span><span class="sxs-lookup"><span data-stu-id="64c06-215">Out of memory.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-216">**已經存在**</span><span class="sxs-lookup"><span data-stu-id="64c06-216">**Already exists**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-217">93</span><span class="sxs-lookup"><span data-stu-id="64c06-217">93</span></span>

<span data-ttu-id="64c06-218">已經存在。</span><span class="sxs-lookup"><span data-stu-id="64c06-218">Already exists.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-219">**找不到路徑、檔案或物件**</span><span class="sxs-lookup"><span data-stu-id="64c06-219">**Path, file or object not found**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-220">94</span><span class="sxs-lookup"><span data-stu-id="64c06-220">94</span></span>

<span data-ttu-id="64c06-221">找不到路徑、檔案或物件。</span><span class="sxs-lookup"><span data-stu-id="64c06-221">Path, file, or object not found.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-222">**無法通知服務**</span><span class="sxs-lookup"><span data-stu-id="64c06-222">**Unable to notify service**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-223">95</span><span class="sxs-lookup"><span data-stu-id="64c06-223">95</span></span>

<span data-ttu-id="64c06-224">無法通知服務。</span><span class="sxs-lookup"><span data-stu-id="64c06-224">Unable to notify service.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-225">**無法通知 DNS 服務**</span><span class="sxs-lookup"><span data-stu-id="64c06-225">**Unable to notify DNS service**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-226">96</span><span class="sxs-lookup"><span data-stu-id="64c06-226">96</span></span>

<span data-ttu-id="64c06-227">無法通知 DNS 服務。</span><span class="sxs-lookup"><span data-stu-id="64c06-227">Unable to notify DNS service.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-228">**介面無法設定**</span><span class="sxs-lookup"><span data-stu-id="64c06-228">**Interface not configurable**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-229">97</span><span class="sxs-lookup"><span data-stu-id="64c06-229">97</span></span>

<span data-ttu-id="64c06-230">介面無法設定。</span><span class="sxs-lookup"><span data-stu-id="64c06-230">Interface not configurable.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-231">**並非所有 DHCP 租用都可以釋出/更新**</span><span class="sxs-lookup"><span data-stu-id="64c06-231">**Not all DHCP leases could be released/renewed**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-232">98</span><span class="sxs-lookup"><span data-stu-id="64c06-232">98</span></span>

<span data-ttu-id="64c06-233">並非所有 DHCP 租用都可以釋出或更新。</span><span class="sxs-lookup"><span data-stu-id="64c06-233">Not all DHCP leases could be released or renewed.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-234">**未在介面卡上啟用 DHCP**</span><span class="sxs-lookup"><span data-stu-id="64c06-234">**DHCP not enabled on adapter**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-235">100</span><span class="sxs-lookup"><span data-stu-id="64c06-235">100</span></span>

<span data-ttu-id="64c06-236">未在介面卡上啟用 DHCP。</span><span class="sxs-lookup"><span data-stu-id="64c06-236">DHCP not enabled on adapter.</span></span>

</dd> <dt>

<span data-ttu-id="64c06-237">**其他**</span><span class="sxs-lookup"><span data-stu-id="64c06-237">**Other**</span></span>
</dt> <dd>

<span data-ttu-id="64c06-238">101 4294967295</span><span class="sxs-lookup"><span data-stu-id="64c06-238">101 4294967295</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="64c06-239">範例</span><span class="sxs-lookup"><span data-stu-id="64c06-239">Examples</span></span>

<span data-ttu-id="64c06-240">[修改所有網路介面卡的 Igmp 層級](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c)VBScript 範例會停用電腦上的 igmp 多播。</span><span class="sxs-lookup"><span data-stu-id="64c06-240">The [Modify the IGMP Level for All Network Adapters](https://Gallery.TechNet.Microsoft.Com/b92f894c-5cf8-4484-b5f0-d54761bacd5c) VBScript sample disables IGMP multicasting on a computer.</span></span>

## <a name="requirements"></a><span data-ttu-id="64c06-241">規格需求</span><span class="sxs-lookup"><span data-stu-id="64c06-241">Requirements</span></span>



| <span data-ttu-id="64c06-242">需求</span><span class="sxs-lookup"><span data-stu-id="64c06-242">Requirement</span></span> | <span data-ttu-id="64c06-243">值</span><span class="sxs-lookup"><span data-stu-id="64c06-243">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="64c06-244">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="64c06-244">Minimum supported client</span></span><br/> | <span data-ttu-id="64c06-245">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="64c06-245">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="64c06-246">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="64c06-246">Minimum supported server</span></span><br/> | <span data-ttu-id="64c06-247">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="64c06-247">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="64c06-248">命名空間</span><span class="sxs-lookup"><span data-stu-id="64c06-248">Namespace</span></span><br/>                | <span data-ttu-id="64c06-249">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="64c06-249">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="64c06-250">MOF</span><span class="sxs-lookup"><span data-stu-id="64c06-250">MOF</span></span><br/>                      | <dl> <span data-ttu-id="64c06-251"><dt>CIMWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="64c06-251"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="64c06-252">DLL</span><span class="sxs-lookup"><span data-stu-id="64c06-252">DLL</span></span><br/>                      | <dl> <span data-ttu-id="64c06-253"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="64c06-253"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="64c06-254">另請參閱</span><span class="sxs-lookup"><span data-stu-id="64c06-254">See also</span></span>

<dl> <dt>

[<span data-ttu-id="64c06-255">電腦系統硬體類別</span><span class="sxs-lookup"><span data-stu-id="64c06-255">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="64c06-256">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="64c06-256">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> <dt>

[<span data-ttu-id="64c06-257">WMI 工作：網路功能</span><span class="sxs-lookup"><span data-stu-id="64c06-257">WMI Tasks: Networking</span></span>](/windows/desktop/WmiSdk/wmi-tasks--networking)
</dt> <dt>

[<span data-ttu-id="64c06-258">WMI 工作：帳戶和網域</span><span class="sxs-lookup"><span data-stu-id="64c06-258">WMI Tasks: Accounts and Domains</span></span>](/windows/desktop/WmiSdk/wmi-tasks--accounts-and-domains)
</dt> <dt>

[<span data-ttu-id="64c06-259">WMI 中的 IPv6 和 IPv4 支援</span><span class="sxs-lookup"><span data-stu-id="64c06-259">IPv6 and IPv4 Support in WMI</span></span>](/windows/desktop/WmiSdk/ipv6-and-ipv4-support-in-wmi)
</dt> </dl>

 

