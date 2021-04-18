---
title: 'IVMGuestOS IsUserLoggedOn 方法 (VPCCOMInterfaces .h) '
description: 判斷要求的會話是否存在。
ms.assetid: 28035e30-023a-4ec2-88ef-43fe22f6d14e
keywords:
- IsUserLoggedOn 方法 Virtual PC
- IsUserLoggedOn 方法 Virtual PC，IVMGuestOS 介面
- IVMGuestOS 介面 Virtual PC，IsUserLoggedOn 方法
topic_type:
- apiref
api_name:
- IVMGuestOS.IsUserLoggedOn
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4eeb0482d7d3ac45b67a863948526b57d6c6e412
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968740"
---
# <a name="ivmguestosisuserloggedon-method"></a><span data-ttu-id="300d9-106">IVMGuestOS：： IsUserLoggedOn 方法</span><span class="sxs-lookup"><span data-stu-id="300d9-106">IVMGuestOS::IsUserLoggedOn method</span></span>

<span data-ttu-id="300d9-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="300d9-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="300d9-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="300d9-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="300d9-109">判斷要求的會話是否存在。</span><span class="sxs-lookup"><span data-stu-id="300d9-109">Determines whether the requested session is present.</span></span>

## <a name="syntax"></a><span data-ttu-id="300d9-110">語法</span><span class="sxs-lookup"><span data-stu-id="300d9-110">Syntax</span></span>


```C++
HRESULT IsUserLoggedOn(
  [in]          long         inRailSession,
  [out, retval] VARIANT_BOOL *outSessionPresent
);
```



## <a name="parameters"></a><span data-ttu-id="300d9-111">參數</span><span class="sxs-lookup"><span data-stu-id="300d9-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="300d9-112">*inRailSession* \[在\]</span><span class="sxs-lookup"><span data-stu-id="300d9-112">*inRailSession* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="300d9-113">針對鐵路會話設定為0，或針對 RDP 會話設定為1。</span><span class="sxs-lookup"><span data-stu-id="300d9-113">Set to 0 for a Rail session or 1 for an RDP session.</span></span>

</dd> <dt>

<span data-ttu-id="300d9-114">*outSessionPresent* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="300d9-114">*outSessionPresent* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="300d9-115">如果會話存在，則設定為 **variant \_ TRUE** ，否則為 **variant \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="300d9-115">Set to **VARIANT\_TRUE** if the session is present and **VARIANT\_FALSE** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="300d9-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="300d9-116">Return value</span></span>

<span data-ttu-id="300d9-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="300d9-117">This method can return one of these values.</span></span>



| <span data-ttu-id="300d9-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="300d9-118">Return code/value</span></span>                                                                                                                                                                       | <span data-ttu-id="300d9-119">Description</span><span class="sxs-lookup"><span data-stu-id="300d9-119">Description</span></span>                                                                |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| <dl> <span data-ttu-id="300d9-120"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="300d9-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                             | <span data-ttu-id="300d9-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="300d9-121">The operation was successful.</span></span><br/>                                   |
| <dl> <span data-ttu-id="300d9-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="300d9-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                               | <span data-ttu-id="300d9-123">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="300d9-123">The parameter is **NULL**.</span></span><br/>                                      |
| <dl> <span data-ttu-id="300d9-124"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="300d9-124"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                            | <span data-ttu-id="300d9-125">*OutSessionPresent* 參數無效或為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="300d9-125">The *outSessionPresent* parameter is not valid or is **NULL**.</span></span><br/>  |
| <dl> <span data-ttu-id="300d9-126"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="300d9-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                       | <span data-ttu-id="300d9-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="300d9-127">An unexpected error has occurred.</span></span><br/>                               |
| <dl> <span data-ttu-id="300d9-128"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span><span class="sxs-lookup"><span data-stu-id="300d9-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_OUTOFMEMORY)**</dt> <dt>0x8007000e</dt></span></span> </dl> | <span data-ttu-id="300d9-129">沒有足夠的記憶體可完成此要求。</span><span class="sxs-lookup"><span data-stu-id="300d9-129">There is not enough memory available to complete this request.</span></span><br/>  |
| <dl> <span data-ttu-id="300d9-130"><dt>**VM \_E \_ 0xA0040202 \_ 計時**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="300d9-130"><dt>**VM\_E\_TIMED\_OUT**</dt> <dt>0xA0040202</dt></span></span> </dl>                        | <span data-ttu-id="300d9-131">作業未及時完成。</span><span class="sxs-lookup"><span data-stu-id="300d9-131">The operation did not complete in a timely manner.</span></span><br/>              |
| <dl> <span data-ttu-id="300d9-132"><dt>**VM \_E \_ VM \_ 未 \_**</dt>執行 <dt>0xA0040206</dt></span><span class="sxs-lookup"><span data-stu-id="300d9-132"><dt>**VM\_E\_VM\_NOT\_RUNNING**</dt> <dt>0xA0040206</dt></span></span> </dl>                  | <span data-ttu-id="300d9-133">虛擬機器 (VM) 必須針對此操作執行。</span><span class="sxs-lookup"><span data-stu-id="300d9-133">The virtual machine (VM) must be running for this operation.</span></span><br/>    |
| <dl> <span data-ttu-id="300d9-134"><dt>**VM \_E \_ 新增 \_ 功能 \_ 無法 \_**</dt> <dt>0xA0040505</dt></span><span class="sxs-lookup"><span data-stu-id="300d9-134"><dt>**VM\_E\_ADDITIONS\_FEATURE\_NOT\_AVAIL**</dt> <dt>0xA0040505</dt></span></span> </dl>    | <span data-ttu-id="300d9-135">此 VM 中未安裝整合元件功能。</span><span class="sxs-lookup"><span data-stu-id="300d9-135">The integration components feature is not installed in this VM.</span></span><br/> |
| <dl> <span data-ttu-id="300d9-136"><dt>**VM \_E \_ VM 已 \_ 暫停**</dt> <dt>0xA00400507</dt></span><span class="sxs-lookup"><span data-stu-id="300d9-136"><dt>**VM\_E\_VM\_PAUSED**</dt> <dt>0xA00400507</dt></span></span> </dl>                       | <span data-ttu-id="300d9-137">VM 已暫停。</span><span class="sxs-lookup"><span data-stu-id="300d9-137">The VM is paused.</span></span><br/>                                               |



 

## <a name="requirements"></a><span data-ttu-id="300d9-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="300d9-138">Requirements</span></span>



| <span data-ttu-id="300d9-139">需求</span><span class="sxs-lookup"><span data-stu-id="300d9-139">Requirement</span></span> | <span data-ttu-id="300d9-140">值</span><span class="sxs-lookup"><span data-stu-id="300d9-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="300d9-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="300d9-141">Minimum supported client</span></span><br/> | <span data-ttu-id="300d9-142">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="300d9-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="300d9-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="300d9-143">Minimum supported server</span></span><br/> | <span data-ttu-id="300d9-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="300d9-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="300d9-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="300d9-145">End of client support</span></span><br/>    | <span data-ttu-id="300d9-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="300d9-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="300d9-147">產品</span><span class="sxs-lookup"><span data-stu-id="300d9-147">Product</span></span><br/>                  | <span data-ttu-id="300d9-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="300d9-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="300d9-149">標頭</span><span class="sxs-lookup"><span data-stu-id="300d9-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="300d9-150"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="300d9-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="300d9-151">IID</span><span class="sxs-lookup"><span data-stu-id="300d9-151">IID</span></span><br/>                      | <span data-ttu-id="300d9-152">IID \_ IVMGuestOS 定義為99fea0db-4880-499a-b6d8-73dff9bc91be</span><span class="sxs-lookup"><span data-stu-id="300d9-152">IID\_IVMGuestOS is defined as 99fea0db-4880-499a-b6d8-73dff9bc91be</span></span><br/>                 |



## <a name="see-also"></a><span data-ttu-id="300d9-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="300d9-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="300d9-154">**IVMGuestOS**</span><span class="sxs-lookup"><span data-stu-id="300d9-154">**IVMGuestOS**</span></span>](ivmguestos.md)
</dt> </dl>

 

