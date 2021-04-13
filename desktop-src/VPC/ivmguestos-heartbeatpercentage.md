---
title: 'IVMGuestOS HeartbeatPercentage 屬性 (VPCCOMInterfaces .h) '
description: 過去一分鐘收到的預期心跳量百分比。
ms.assetid: 456dd8ae-e946-429d-98aa-5773362fdd4e
keywords:
- HeartbeatPercentage 屬性 Virtual PC
- HeartbeatPercentage 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，HeartbeatPercentage 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.HeartbeatPercentage
- IVMGuestOS.get_HeartbeatPercentage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 22d568ed85281e8940b69afd1c72e76e2f208a5a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509256"
---
# <a name="ivmguestosheartbeatpercentage-property"></a><span data-ttu-id="93560-106">IVMGuestOS：： HeartbeatPercentage 屬性</span><span class="sxs-lookup"><span data-stu-id="93560-106">IVMGuestOS::HeartbeatPercentage property</span></span>

<span data-ttu-id="93560-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="93560-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="93560-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="93560-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="93560-109">抓取過去一分鐘所收到的預期心跳量百分比。</span><span class="sxs-lookup"><span data-stu-id="93560-109">Retrieves the percentage of expected heartbeats received over the past minute.</span></span>

<span data-ttu-id="93560-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="93560-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="93560-111">語法</span><span class="sxs-lookup"><span data-stu-id="93560-111">Syntax</span></span>


```C++
HRESULT get_HeartbeatPercentage(
  [out, retval] long *heartbeatPercentage
);
```



## <a name="property-value"></a><span data-ttu-id="93560-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="93560-112">Property value</span></span>

<span data-ttu-id="93560-113">過去一分鐘收到的預期心跳量百分比。</span><span class="sxs-lookup"><span data-stu-id="93560-113">The percentage of expected heartbeats received over the past minute.</span></span>

## <a name="error-codes"></a><span data-ttu-id="93560-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="93560-114">Error codes</span></span>



| <span data-ttu-id="93560-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="93560-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="93560-116">意義</span><span class="sxs-lookup"><span data-stu-id="93560-116">Meaning</span></span>                                                                                                                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="93560-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="93560-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="93560-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="93560-118">The operation was successful.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="93560-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="93560-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="93560-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="93560-120">The parameter is **NULL**.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="93560-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="93560-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="93560-122">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="93560-122">The configuration is unknown.</span></span><br/>                                                                                                            |
| <dl> <span data-ttu-id="93560-123"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="93560-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="93560-124">虛擬機器 (VM) 必須針對此操作執行。</span><span class="sxs-lookup"><span data-stu-id="93560-124">The virtual machine (VM) must be running for this operation.</span></span><br/>                                                                             |
| <dl> <span data-ttu-id="93560-125"><dt>VM \_E \_ 新增 \_ 專案 \_ 無法</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="93560-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="93560-126">VM 未完全啟動、未安裝整合元件功能，或安裝的版本不支援這項功能。</span><span class="sxs-lookup"><span data-stu-id="93560-126">The VM is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="93560-127"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="93560-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="93560-128">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="93560-128">An unexpected error has occurred.</span></span><br/>                                                                                                        |



## <a name="remarks"></a><span data-ttu-id="93560-129">備註</span><span class="sxs-lookup"><span data-stu-id="93560-129">Remarks</span></span>

<span data-ttu-id="93560-130">當客體作業系統正在執行時，整合元件會將週期性心跳傳送至 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="93560-130">Integration components will send a periodic heartbeat to Windows Virtual PC while the guest operating system is running.</span></span> <span data-ttu-id="93560-131">如果虛擬作業系統的負載很高，Windows Virtual PC 可能會收到比預期更少的心跳。</span><span class="sxs-lookup"><span data-stu-id="93560-131">If the guest operating system is heavily loaded, it's possible that Windows Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="93560-132">如果心跳百分比降至零，表示客體作業系統可能沒有回應或損毀。</span><span class="sxs-lookup"><span data-stu-id="93560-132">If the heartbeat percentage drops to zero, it is possible that the guest operating system is not responding or is crashed.</span></span> <span data-ttu-id="93560-133">虛擬機器必須執行 (也就是，完全開機且未關閉) 而且必須在叫用這個屬性時安裝整合元件。</span><span class="sxs-lookup"><span data-stu-id="93560-133">The virtual machine must be running (that is, fully booted and not shutting down) and integration components must be installed when this property is invoked.</span></span>

## <a name="requirements"></a><span data-ttu-id="93560-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="93560-134">Requirements</span></span>



| <span data-ttu-id="93560-135">需求</span><span class="sxs-lookup"><span data-stu-id="93560-135">Requirement</span></span> | <span data-ttu-id="93560-136">值</span><span class="sxs-lookup"><span data-stu-id="93560-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="93560-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93560-137">Minimum supported client</span></span><br/> | <span data-ttu-id="93560-138">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93560-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="93560-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93560-139">Minimum supported server</span></span><br/> | <span data-ttu-id="93560-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="93560-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="93560-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="93560-141">End of client support</span></span><br/>    | <span data-ttu-id="93560-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="93560-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="93560-143">產品</span><span class="sxs-lookup"><span data-stu-id="93560-143">Product</span></span><br/>                  | <span data-ttu-id="93560-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="93560-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="93560-145">標頭</span><span class="sxs-lookup"><span data-stu-id="93560-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="93560-146"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="93560-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="93560-147">IID</span><span class="sxs-lookup"><span data-stu-id="93560-147">IID</span></span><br/>                      | <span data-ttu-id="93560-148">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="93560-148">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="93560-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93560-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93560-150">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="93560-150">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

