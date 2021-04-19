---
title: 'IVMGuestOS IsHeartbeating 屬性 (VPCCOMInterfaces .h) '
description: 判斷虛擬機器是否有信號。
ms.assetid: b1697a7b-6119-47aa-b261-6009f5287993
keywords:
- IsHeartbeating 屬性 Virtual PC
- IsHeartbeating 屬性 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，IsHeartbeating 屬性
topic_type:
- apiref
api_name:
- IVMGuestOS.IsHeartbeating
- IVMGuestOS.get_IsHeartbeating
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: faad446749cbf3cdb75d6e8fa7469022cc004ea7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106979691"
---
# <a name="ivmguestosisheartbeating-property"></a><span data-ttu-id="27565-106">IVMGuestOS：： IsHeartbeating 屬性</span><span class="sxs-lookup"><span data-stu-id="27565-106">IVMGuestOS::IsHeartbeating property</span></span>

<span data-ttu-id="27565-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="27565-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="27565-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="27565-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="27565-109">判斷虛擬機器是否有信號。</span><span class="sxs-lookup"><span data-stu-id="27565-109">Determines whether the virtual machine has a heartbeat.</span></span>

<span data-ttu-id="27565-110">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="27565-110">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="27565-111">語法</span><span class="sxs-lookup"><span data-stu-id="27565-111">Syntax</span></span>


```C++
HRESULT get_IsHeartbeating(
  [out, retval] VARIANT_BOOL *heartBeating
);
```



## <a name="property-value"></a><span data-ttu-id="27565-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="27565-112">Property value</span></span>

<span data-ttu-id="27565-113">**變異 \_** 如果偵測到信號，則為 TRUE，否則為 **VARIANT \_** 。</span><span class="sxs-lookup"><span data-stu-id="27565-113">**VARIANT\_TRUE** if a heartbeat is detected, **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="27565-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="27565-114">Error codes</span></span>



| <span data-ttu-id="27565-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="27565-115">Name/value</span></span>                                                                                                                                                              | <span data-ttu-id="27565-116">意義</span><span class="sxs-lookup"><span data-stu-id="27565-116">Meaning</span></span>                                                                                                                                                          |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="27565-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="27565-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                 | <span data-ttu-id="27565-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="27565-118">The operation was successful.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="27565-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="27565-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                   | <span data-ttu-id="27565-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="27565-120">The parameter is **NULL**.</span></span><br/>                                                                                                                            |
| <dl> <span data-ttu-id="27565-121"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="27565-121"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>           | <span data-ttu-id="27565-122">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="27565-122">The configuration is unknown.</span></span><br/>                                                                                                                         |
| <dl> <span data-ttu-id="27565-123"><dt>VM \_E \_ VM \_ 未 \_ </dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="27565-123"><dt>VM\_E\_VM\_NOT\_RUNNING</dt> <dt>0xA0040206</dt></span></span> </dl>      | <span data-ttu-id="27565-124">虛擬機器必須正在執行，才能進行這種操作。</span><span class="sxs-lookup"><span data-stu-id="27565-124">The virtual machine must be running for this operation.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="27565-125"><dt>VM \_E \_ 新增 \_ 專案 \_ 無法</dt> <dt>0xA0040504</dt></span><span class="sxs-lookup"><span data-stu-id="27565-125"><dt>VM\_E\_ADDITIONS\_NOT\_AVAIL</dt> <dt>0xA0040504</dt></span></span> </dl> | <span data-ttu-id="27565-126">虛擬機器未完全啟動、未安裝整合元件功能，或安裝的版本不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="27565-126">The virtual machine is not fully booted, the integration components feature is not installed, or the installed version does not support this feature.</span></span><br/> |
| <dl> <span data-ttu-id="27565-127"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="27565-127"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>           | <span data-ttu-id="27565-128">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="27565-128">An unexpected error has occurred.</span></span><br/>                                                                                                                     |



## <a name="remarks"></a><span data-ttu-id="27565-129">備註</span><span class="sxs-lookup"><span data-stu-id="27565-129">Remarks</span></span>

<span data-ttu-id="27565-130">當整合元件安裝在客體作業系統時，系統會從虛擬機器會話將一般的「滴答」或心跳傳送至 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="27565-130">When integration components is installed in the guest operating system, a regular 'tick' or heartbeat is sent from the virtual machine session to Windows Virtual PC.</span></span> <span data-ttu-id="27565-131">如果虛擬電腦的負載很高，則虛擬電腦可能會收到比預期更少的心跳。</span><span class="sxs-lookup"><span data-stu-id="27565-131">If the guest operating system is heavily loaded, it's possible that Virtual PC will receive fewer heartbeats than expected.</span></span> <span data-ttu-id="27565-132">如果未偵測到任何偵測到的偵測，則可能是客體作業系統沒有回應或損毀。</span><span class="sxs-lookup"><span data-stu-id="27565-132">If no heartbeat is detected, it is possible that the guest operating system is not responding or is crashed.</span></span>

<span data-ttu-id="27565-133">根據預設，虛擬機器每分鐘會產生10個信號刻度。</span><span class="sxs-lookup"><span data-stu-id="27565-133">By default, a virtual machine produces ten heartbeat ticks per minute.</span></span> <span data-ttu-id="27565-134">如果未偵測到整分鐘的任何心跳滴答，Windows Virtual PC 會每十秒嘗試重新開機虛擬機器會話一次，最多兩分鐘。</span><span class="sxs-lookup"><span data-stu-id="27565-134">If no heartbeat ticks are detected for an entire minute, Windows Virtual PC will attempt to restart the virtual machine session once every ten seconds for up to two minutes.</span></span> <span data-ttu-id="27565-135">此行為是由虛擬機器會話設定檔中的下列索引鍵值所控制。</span><span class="sxs-lookup"><span data-stu-id="27565-135">This behavior is controlled by the following key values in the virtual machine session's configuration file.</span></span>



| <span data-ttu-id="27565-136">組態機碼</span><span class="sxs-lookup"><span data-stu-id="27565-136">Configuration key</span></span>                                            | <span data-ttu-id="27565-137">預設</span><span class="sxs-lookup"><span data-stu-id="27565-137">Default</span></span>       | <span data-ttu-id="27565-138">描述</span><span class="sxs-lookup"><span data-stu-id="27565-138">Description</span></span>                                                                                                                             |
|--------------------------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="27565-139">整合/microsoft/心跳/時間</span><span class="sxs-lookup"><span data-stu-id="27565-139">integration/microsoft/heartbeat/time</span></span><br/>              | <span data-ttu-id="27565-140">60</span><span class="sxs-lookup"><span data-stu-id="27565-140">60</span></span><br/> | <span data-ttu-id="27565-141">用來產生信號刻度的時間區塊長度（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="27565-141">The length of the block of time used to generate heartbeat ticks, in in seconds.</span></span><br/>                                             |
| <span data-ttu-id="27565-142">整合/microsoft/心跳/比率</span><span class="sxs-lookup"><span data-stu-id="27565-142">integration/microsoft/heartbeat/rate</span></span><br/>              | <span data-ttu-id="27565-143">10</span><span class="sxs-lookup"><span data-stu-id="27565-143">10</span></span><br/> | <span data-ttu-id="27565-144">每個信號時間區塊中產生的刻度數目。</span><span class="sxs-lookup"><span data-stu-id="27565-144">The number of ticks generated in each heartbeat time block.</span></span><br/>                                                                  |
| <span data-ttu-id="27565-145">整合/microsoft/信號/失敗 \_ 間隔</span><span class="sxs-lookup"><span data-stu-id="27565-145">integration/microsoft/heartbeat/failure\_interval</span></span><br/> | <span data-ttu-id="27565-146">10</span><span class="sxs-lookup"><span data-stu-id="27565-146">10</span></span><br/> | <span data-ttu-id="27565-147">在特定的時間區塊內未收到任何心跳滴答之後，重新開機嘗試之間的秒數。</span><span class="sxs-lookup"><span data-stu-id="27565-147">The number of seconds between restart attempts, once no heartbeat ticks are received within a specific heartbeat time block.</span></span><br/> |
| <span data-ttu-id="27565-148">整合/microsoft/信號/失敗 \_ 嘗試</span><span class="sxs-lookup"><span data-stu-id="27565-148">integration/microsoft/heartbeat/failure\_attempts</span></span><br/> | <span data-ttu-id="27565-149">12</span><span class="sxs-lookup"><span data-stu-id="27565-149">12</span></span><br/> | <span data-ttu-id="27565-150">嘗試重新開機的次數。</span><span class="sxs-lookup"><span data-stu-id="27565-150">The number of restart attempts made.</span></span><br/>                                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="27565-151">規格需求</span><span class="sxs-lookup"><span data-stu-id="27565-151">Requirements</span></span>



| <span data-ttu-id="27565-152">需求</span><span class="sxs-lookup"><span data-stu-id="27565-152">Requirement</span></span> | <span data-ttu-id="27565-153">值</span><span class="sxs-lookup"><span data-stu-id="27565-153">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="27565-154">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27565-154">Minimum supported client</span></span><br/> | <span data-ttu-id="27565-155">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27565-155">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="27565-156">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27565-156">Minimum supported server</span></span><br/> | <span data-ttu-id="27565-157">都不支援</span><span class="sxs-lookup"><span data-stu-id="27565-157">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="27565-158">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="27565-158">End of client support</span></span><br/>    | <span data-ttu-id="27565-159">Windows 7</span><span class="sxs-lookup"><span data-stu-id="27565-159">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="27565-160">產品</span><span class="sxs-lookup"><span data-stu-id="27565-160">Product</span></span><br/>                  | <span data-ttu-id="27565-161">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="27565-161">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="27565-162">標頭</span><span class="sxs-lookup"><span data-stu-id="27565-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="27565-163"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="27565-163"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="27565-164">IID</span><span class="sxs-lookup"><span data-stu-id="27565-164">IID</span></span><br/>                      | <span data-ttu-id="27565-165">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="27565-165">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="27565-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27565-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27565-167">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="27565-167">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

