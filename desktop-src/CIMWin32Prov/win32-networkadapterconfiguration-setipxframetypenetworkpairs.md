---
description: 為此網路介面卡設定網路封包交換 (IPX) 網路編號/框架配對。
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetIPXFrameTypeNetworkPairs 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: e4d53ec7b5600a767505e517a02fbf87b5a43d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111356"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="80dbf-103">Win32 >networkadapterconfiguration 類別的 SetIPXFrameTypeNetworkPairs 方法 \_</span><span class="sxs-lookup"><span data-stu-id="80dbf-103">SetIPXFrameTypeNetworkPairs method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="80dbf-104">為此網路介面卡設定網路封包交換 (IPX) 網路編號/框架配對。</span><span class="sxs-lookup"><span data-stu-id="80dbf-104">Sets the Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span>

<span data-ttu-id="80dbf-105">Windows 2000 和 Windows NT 3.51 和更新版本會使用 IPX 網路編號來進行路由。</span><span class="sxs-lookup"><span data-stu-id="80dbf-105">Windows 2000 and Windows NT 3.51 and higher use an IPX network number for routing purposes.</span></span> <span data-ttu-id="80dbf-106">它會指派給電腦系統上每個設定的畫面格類型/網路介面卡組合。</span><span class="sxs-lookup"><span data-stu-id="80dbf-106">It is assigned to each configured frame type/network adapter combination on your computer system.</span></span> <span data-ttu-id="80dbf-107">此數位有時稱為「外部網路編號」。</span><span class="sxs-lookup"><span data-stu-id="80dbf-107">This number is sometimes referred to as the "external network number."</span></span> <span data-ttu-id="80dbf-108">對於每個網路區段而言，它必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="80dbf-108">It must be unique for each network segment.</span></span> <span data-ttu-id="80dbf-109">如果畫面類型設定為 [自動]，則網路編號應為零。</span><span class="sxs-lookup"><span data-stu-id="80dbf-109">If the frame type is set to AUTO, the network number should to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="80dbf-110">語法</span><span class="sxs-lookup"><span data-stu-id="80dbf-110">Syntax</span></span>


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a><span data-ttu-id="80dbf-111">參數</span><span class="sxs-lookup"><span data-stu-id="80dbf-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="80dbf-112">*IPXNetworkNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80dbf-112">*IPXNetworkNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80dbf-113">字元陣列，可唯一識別電腦系統上的介面卡。</span><span class="sxs-lookup"><span data-stu-id="80dbf-113">An array of characters that uniquely identify an adapter on the computer system.</span></span> <span data-ttu-id="80dbf-114">在 Windows 2000 和 Windows NT 3.51 或更高版本中，NetWare 連結 (NWLink) IPX/SPX 相容傳輸會使用兩種不同類型的網路編號。</span><span class="sxs-lookup"><span data-stu-id="80dbf-114">The NetWare Link (NWLink) IPX/SPX-compatible transport in Windows 2000 and Windows NT 3.51 or higher, uses two different types of network numbers.</span></span> <span data-ttu-id="80dbf-115">此數位有時稱為外部網路編號。</span><span class="sxs-lookup"><span data-stu-id="80dbf-115">This number is sometimes referred to as the External Network Number.</span></span> <span data-ttu-id="80dbf-116">對於每個網路區段而言，它必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="80dbf-116">It must be unique for each network segment.</span></span> <span data-ttu-id="80dbf-117">此字串清單中的值必須在 IPXFrameType 參數中有對應的值，以識別用於此網路的封包框架類型。</span><span class="sxs-lookup"><span data-stu-id="80dbf-117">The values in this string list must have a corresponding value in the IPXFrameType parameter identifying the packet frame type used for this network.</span></span>

</dd> <dt>

<span data-ttu-id="80dbf-118">*IPXFrameType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="80dbf-118">*IPXFrameType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="80dbf-119">框架類型識別碼的整數陣列。</span><span class="sxs-lookup"><span data-stu-id="80dbf-119">An integer array of frame type identifiers.</span></span> <span data-ttu-id="80dbf-120">這個陣列中的值會對應到 *IPXNetworkNumber* 參數中的元素。</span><span class="sxs-lookup"><span data-stu-id="80dbf-120">The values in this array correspond to the elements in the *IPXNetworkNumber* parameter.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="80dbf-121">**ETHERNET II** (0) </span><span class="sxs-lookup"><span data-stu-id="80dbf-121">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="80dbf-122">**Ethernet 802.3** (1) </span><span class="sxs-lookup"><span data-stu-id="80dbf-122">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="80dbf-123">**Ethernet 802.2** (2) </span><span class="sxs-lookup"><span data-stu-id="80dbf-123">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="80dbf-124">**Ethernet 貼齊** (3) </span><span class="sxs-lookup"><span data-stu-id="80dbf-124">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="80dbf-125">**自動** (255) </span><span class="sxs-lookup"><span data-stu-id="80dbf-125">**AUTO** (255)</span></span>


<span data-ttu-id="80dbf-126"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="80dbf-126"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="80dbf-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="80dbf-127">Return value</span></span>

<dl> <dt>

<span data-ttu-id="80dbf-128">**成功完成，不需要重新開機** (0) </span><span class="sxs-lookup"><span data-stu-id="80dbf-128">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-129">**成功完成，需要重新開機** (1) </span><span class="sxs-lookup"><span data-stu-id="80dbf-129">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-130">**此平臺 (64) 不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="80dbf-130">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-131">**未知的失敗** (65) </span><span class="sxs-lookup"><span data-stu-id="80dbf-131">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-132">**不正確子網路遮罩** (66) </span><span class="sxs-lookup"><span data-stu-id="80dbf-132">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-133">**處理傳回的實例時發生錯誤** (67) </span><span class="sxs-lookup"><span data-stu-id="80dbf-133">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-134">**不正確輸入參數** (68) </span><span class="sxs-lookup"><span data-stu-id="80dbf-134">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-135"> (69) **指定超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="80dbf-135">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-136">**不正確 IP 位址** (70) </span><span class="sxs-lookup"><span data-stu-id="80dbf-136">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-137">**不正確閘道 IP 位址** (71) </span><span class="sxs-lookup"><span data-stu-id="80dbf-137">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-138">**存取所要求資訊** 的登錄時發生錯誤 (72) </span><span class="sxs-lookup"><span data-stu-id="80dbf-138">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-139">**不正確功能變數名稱** (73) </span><span class="sxs-lookup"><span data-stu-id="80dbf-139">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-140">**不正確主機名稱** (74) </span><span class="sxs-lookup"><span data-stu-id="80dbf-140">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-141">**未定義任何主要/次要 WINS 伺服器** (75) </span><span class="sxs-lookup"><span data-stu-id="80dbf-141">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-142">**不正確檔** (76) </span><span class="sxs-lookup"><span data-stu-id="80dbf-142">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-143">**不正確系統路徑** (77) </span><span class="sxs-lookup"><span data-stu-id="80dbf-143">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-144">檔案 **複製失敗** (78) </span><span class="sxs-lookup"><span data-stu-id="80dbf-144">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-145"> (79) 的 **安全性參數無效**</span><span class="sxs-lookup"><span data-stu-id="80dbf-145">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-146">**無法設定 tcp/ip 服務** (80) </span><span class="sxs-lookup"><span data-stu-id="80dbf-146">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-147">**無法設定 DHCP 服務** (81) </span><span class="sxs-lookup"><span data-stu-id="80dbf-147">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-148">**無法更新 DHCP 租用** (82) </span><span class="sxs-lookup"><span data-stu-id="80dbf-148">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-149">**無法釋放 DHCP 租用** (83) </span><span class="sxs-lookup"><span data-stu-id="80dbf-149">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-150">**介面卡上未啟用 IP** (84) </span><span class="sxs-lookup"><span data-stu-id="80dbf-150">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-151">**未在介面卡上啟用 IPX** (85) </span><span class="sxs-lookup"><span data-stu-id="80dbf-151">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-152">**畫面格/網路編號界限錯誤** (86) </span><span class="sxs-lookup"><span data-stu-id="80dbf-152">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-153">**不正確框架類型** (87) </span><span class="sxs-lookup"><span data-stu-id="80dbf-153">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-154"> (88) 的 **網路編號無效**</span><span class="sxs-lookup"><span data-stu-id="80dbf-154">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-155"> (89) **重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="80dbf-155">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-156">**參數超出範圍** (90) </span><span class="sxs-lookup"><span data-stu-id="80dbf-156">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-157">**拒絕存取** (91) </span><span class="sxs-lookup"><span data-stu-id="80dbf-157">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-158">**記憶體不足** (92) </span><span class="sxs-lookup"><span data-stu-id="80dbf-158">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-159">**已存在** (93) </span><span class="sxs-lookup"><span data-stu-id="80dbf-159">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-160">**找不到路徑、檔案或物件** (94) </span><span class="sxs-lookup"><span data-stu-id="80dbf-160">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-161">**無法通知服務** (95) </span><span class="sxs-lookup"><span data-stu-id="80dbf-161">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-162">**無法通知 DNS 服務** (96) </span><span class="sxs-lookup"><span data-stu-id="80dbf-162">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-163">**介面無法** 設定 (97) </span><span class="sxs-lookup"><span data-stu-id="80dbf-163">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-164">**並非所有 DHCP 租用都** 可以釋出/更新 (98) </span><span class="sxs-lookup"><span data-stu-id="80dbf-164">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-165">**未在介面卡上啟用 DHCP** (100) </span><span class="sxs-lookup"><span data-stu-id="80dbf-165">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="80dbf-166">**其他** (101 – 4294967295) </span><span class="sxs-lookup"><span data-stu-id="80dbf-166">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="80dbf-167">規格需求</span><span class="sxs-lookup"><span data-stu-id="80dbf-167">Requirements</span></span>



| <span data-ttu-id="80dbf-168">需求</span><span class="sxs-lookup"><span data-stu-id="80dbf-168">Requirement</span></span> | <span data-ttu-id="80dbf-169">值</span><span class="sxs-lookup"><span data-stu-id="80dbf-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="80dbf-170">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="80dbf-170">Minimum supported client</span></span><br/> | <span data-ttu-id="80dbf-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="80dbf-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="80dbf-172">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="80dbf-172">Minimum supported server</span></span><br/> | <span data-ttu-id="80dbf-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="80dbf-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="80dbf-174">命名空間</span><span class="sxs-lookup"><span data-stu-id="80dbf-174">Namespace</span></span><br/>                | <span data-ttu-id="80dbf-175">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="80dbf-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="80dbf-176">MOF</span><span class="sxs-lookup"><span data-stu-id="80dbf-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="80dbf-177"><dt>CimWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="80dbf-177"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="80dbf-178">DLL</span><span class="sxs-lookup"><span data-stu-id="80dbf-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="80dbf-179"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="80dbf-179"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="80dbf-180">另請參閱</span><span class="sxs-lookup"><span data-stu-id="80dbf-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="80dbf-181">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="80dbf-181">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




