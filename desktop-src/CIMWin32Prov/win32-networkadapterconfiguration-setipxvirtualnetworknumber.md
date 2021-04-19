---
description: 設定目的電腦系統上的封包交換 (IPX) 虛擬網路編號。
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Win32_NetworkAdapterConfiguration 類別的 SetIPXVirtualNetworkNumber 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: ed6e6802a17ef6ec4393d2ae0c5ec43f0e21d247
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967059"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="f165d-103">Win32 >networkadapterconfiguration 類別的 SetIPXVirtualNetworkNumber 方法 \_</span><span class="sxs-lookup"><span data-stu-id="f165d-103">SetIPXVirtualNetworkNumber method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="f165d-104">設定目的電腦系統上的封包交換 (IPX) 虛擬網路編號。</span><span class="sxs-lookup"><span data-stu-id="f165d-104">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span> <span data-ttu-id="f165d-105">Windows 2000 和 Windows NT 3.51 或更新版本使用內部網路編號進行內部路由。</span><span class="sxs-lookup"><span data-stu-id="f165d-105">Windows 2000 and Windows NT 3.51 or greater uses an internal network number for internal routing.</span></span> <span data-ttu-id="f165d-106">內部網路編號也稱為虛擬網路編號。</span><span class="sxs-lookup"><span data-stu-id="f165d-106">The internal network number is also known as a virtual network number.</span></span> <span data-ttu-id="f165d-107">它可唯一識別網路上的電腦系統。</span><span class="sxs-lookup"><span data-stu-id="f165d-107">It uniquely identifies the computer system on the network.</span></span> <span data-ttu-id="f165d-108">方法會傳回一個整數值，這個值的意義如下：</span><span class="sxs-lookup"><span data-stu-id="f165d-108">The method returns an integer value that can be interpretted as follows:</span></span>

## <a name="syntax"></a><span data-ttu-id="f165d-109">語法</span><span class="sxs-lookup"><span data-stu-id="f165d-109">Syntax</span></span>


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a><span data-ttu-id="f165d-110">參數</span><span class="sxs-lookup"><span data-stu-id="f165d-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f165d-111">*IPXVirtualNetNumber* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f165d-111">*IPXVirtualNetNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f165d-112">此系統的虛擬網路編號。</span><span class="sxs-lookup"><span data-stu-id="f165d-112">The virtual network number for this system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f165d-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="f165d-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="f165d-114">**成功完成，不需要重新開機** (0) </span><span class="sxs-lookup"><span data-stu-id="f165d-114">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-115">**成功完成，需要重新開機** (1) </span><span class="sxs-lookup"><span data-stu-id="f165d-115">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-116">**此平臺 (64) 不支援的方法**</span><span class="sxs-lookup"><span data-stu-id="f165d-116">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-117">**未知的失敗** (65) </span><span class="sxs-lookup"><span data-stu-id="f165d-117">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-118">**不正確子網路遮罩** (66) </span><span class="sxs-lookup"><span data-stu-id="f165d-118">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-119">**處理傳回的實例時發生錯誤** (67) </span><span class="sxs-lookup"><span data-stu-id="f165d-119">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-120">**不正確輸入參數** (68) </span><span class="sxs-lookup"><span data-stu-id="f165d-120">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-121"> (69) **指定超過5個閘道**</span><span class="sxs-lookup"><span data-stu-id="f165d-121">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-122">**不正確 IP 位址** (70) </span><span class="sxs-lookup"><span data-stu-id="f165d-122">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-123">**不正確閘道 IP 位址** (71) </span><span class="sxs-lookup"><span data-stu-id="f165d-123">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-124">**存取所要求資訊** 的登錄時發生錯誤 (72) </span><span class="sxs-lookup"><span data-stu-id="f165d-124">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-125">**不正確功能變數名稱** (73) </span><span class="sxs-lookup"><span data-stu-id="f165d-125">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-126">**不正確主機名稱** (74) </span><span class="sxs-lookup"><span data-stu-id="f165d-126">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-127">**未定義任何主要/次要 WINS 伺服器** (75) </span><span class="sxs-lookup"><span data-stu-id="f165d-127">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-128">**不正確檔** (76) </span><span class="sxs-lookup"><span data-stu-id="f165d-128">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-129">**不正確系統路徑** (77) </span><span class="sxs-lookup"><span data-stu-id="f165d-129">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-130">檔案 **複製失敗** (78) </span><span class="sxs-lookup"><span data-stu-id="f165d-130">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-131"> (79) 的 **安全性參數無效**</span><span class="sxs-lookup"><span data-stu-id="f165d-131">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-132">**無法設定 tcp/ip 服務** (80) </span><span class="sxs-lookup"><span data-stu-id="f165d-132">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-133">**無法設定 DHCP 服務** (81) </span><span class="sxs-lookup"><span data-stu-id="f165d-133">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-134">**無法更新 DHCP 租用** (82) </span><span class="sxs-lookup"><span data-stu-id="f165d-134">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-135">**無法釋放 DHCP 租用** (83) </span><span class="sxs-lookup"><span data-stu-id="f165d-135">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-136">**介面卡上未啟用 IP** (84) </span><span class="sxs-lookup"><span data-stu-id="f165d-136">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-137">**未在介面卡上啟用 IPX** (85) </span><span class="sxs-lookup"><span data-stu-id="f165d-137">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-138">**畫面格/網路編號界限錯誤** (86) </span><span class="sxs-lookup"><span data-stu-id="f165d-138">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-139">**不正確框架類型** (87) </span><span class="sxs-lookup"><span data-stu-id="f165d-139">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-140"> (88) 的 **網路編號無效**</span><span class="sxs-lookup"><span data-stu-id="f165d-140">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-141"> (89) **重複的網路編號**</span><span class="sxs-lookup"><span data-stu-id="f165d-141">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-142">**參數超出範圍** (90) </span><span class="sxs-lookup"><span data-stu-id="f165d-142">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-143">**拒絕存取** (91) </span><span class="sxs-lookup"><span data-stu-id="f165d-143">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-144">**記憶體不足** (92) </span><span class="sxs-lookup"><span data-stu-id="f165d-144">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-145">**已存在** (93) </span><span class="sxs-lookup"><span data-stu-id="f165d-145">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-146">**找不到路徑、檔案或物件** (94) </span><span class="sxs-lookup"><span data-stu-id="f165d-146">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-147">**無法通知服務** (95) </span><span class="sxs-lookup"><span data-stu-id="f165d-147">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-148">**無法通知 DNS 服務** (96) </span><span class="sxs-lookup"><span data-stu-id="f165d-148">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-149">**介面無法** 設定 (97) </span><span class="sxs-lookup"><span data-stu-id="f165d-149">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-150">**並非所有 DHCP 租用都** 可以釋出/更新 (98) </span><span class="sxs-lookup"><span data-stu-id="f165d-150">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-151">**未在介面卡上啟用 DHCP** (100) </span><span class="sxs-lookup"><span data-stu-id="f165d-151">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="f165d-152">**其他** (101 – 4294967295) </span><span class="sxs-lookup"><span data-stu-id="f165d-152">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="f165d-153">規格需求</span><span class="sxs-lookup"><span data-stu-id="f165d-153">Requirements</span></span>



| <span data-ttu-id="f165d-154">需求</span><span class="sxs-lookup"><span data-stu-id="f165d-154">Requirement</span></span> | <span data-ttu-id="f165d-155">值</span><span class="sxs-lookup"><span data-stu-id="f165d-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f165d-156">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f165d-156">Minimum supported client</span></span><br/> | <span data-ttu-id="f165d-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f165d-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f165d-158">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f165d-158">Minimum supported server</span></span><br/> | <span data-ttu-id="f165d-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f165d-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f165d-160">命名空間</span><span class="sxs-lookup"><span data-stu-id="f165d-160">Namespace</span></span><br/>                | <span data-ttu-id="f165d-161">根 \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="f165d-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f165d-162">MOF</span><span class="sxs-lookup"><span data-stu-id="f165d-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f165d-163"><dt>CimWin32 mof</dt></span><span class="sxs-lookup"><span data-stu-id="f165d-163"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f165d-164">DLL</span><span class="sxs-lookup"><span data-stu-id="f165d-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f165d-165"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f165d-165"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f165d-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f165d-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f165d-167">**Win32 \_ >networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="f165d-167">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




