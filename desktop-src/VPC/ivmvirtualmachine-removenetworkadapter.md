---
title: 'IVMVirtualMachine RemoveNetworkAdapter 方法 (VPCCOMInterfaces .h) '
description: 從虛擬機器移除網路介面。
ms.assetid: 25a5b172-55b8-4cbe-98aa-630148cf6b6d
keywords:
- RemoveNetworkAdapter 方法 Virtual PC
- RemoveNetworkAdapter 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，RemoveNetworkAdapter 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27424f7a3dc5445f56d960393aa12345fcf5f1cc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466396"
---
# <a name="ivmvirtualmachineremovenetworkadapter-method"></a><span data-ttu-id="57b2e-106">IVMVirtualMachine：： RemoveNetworkAdapter 方法</span><span class="sxs-lookup"><span data-stu-id="57b2e-106">IVMVirtualMachine::RemoveNetworkAdapter method</span></span>

<span data-ttu-id="57b2e-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="57b2e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="57b2e-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="57b2e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="57b2e-109">從虛擬機器移除網路介面。</span><span class="sxs-lookup"><span data-stu-id="57b2e-109">Removes a network interface from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="57b2e-110">語法</span><span class="sxs-lookup"><span data-stu-id="57b2e-110">Syntax</span></span>


```C++
HRESULT RemoveNetworkAdapter(
  [in] IVMNetworkAdapter *networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="57b2e-111">參數</span><span class="sxs-lookup"><span data-stu-id="57b2e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57b2e-112">*networkAdapter* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57b2e-112">*networkAdapter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57b2e-113">[**IVMNetworkAdapter**](ivmnetworkadapter.md)物件，代表要移除的網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="57b2e-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object that represents the network adapter to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57b2e-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="57b2e-114">Return value</span></span>

<span data-ttu-id="57b2e-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="57b2e-115">This method can return one of these values.</span></span>



| <span data-ttu-id="57b2e-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="57b2e-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="57b2e-117">Description</span><span class="sxs-lookup"><span data-stu-id="57b2e-117">Description</span></span>                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------|
| <dl> <span data-ttu-id="57b2e-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="57b2e-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="57b2e-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="57b2e-119">The operation was successful.</span></span><br/>                       |
| <dl> <span data-ttu-id="57b2e-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="57b2e-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="57b2e-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="57b2e-121">The parameter is **NULL**.</span></span><br/>                          |
| <dl> <span data-ttu-id="57b2e-122"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="57b2e-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="57b2e-123">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="57b2e-123">The configuration is unknown.</span></span><br/>                       |
| <dl> <span data-ttu-id="57b2e-124"><dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="57b2e-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="57b2e-125">虛擬機器處於執行中或已儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="57b2e-125">The virtual machine is in a running or saved state.</span></span><br/> |
| <dl> <span data-ttu-id="57b2e-126"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="57b2e-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="57b2e-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="57b2e-127">An unexpected error has occurred.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="57b2e-128">備註</span><span class="sxs-lookup"><span data-stu-id="57b2e-128">Remarks</span></span>

<span data-ttu-id="57b2e-129">您只能從已停止的虛擬機器中移除現有的網路介面。</span><span class="sxs-lookup"><span data-stu-id="57b2e-129">You can only remove an existing network interface from a virtual machine that is stopped.</span></span>

## <a name="requirements"></a><span data-ttu-id="57b2e-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="57b2e-130">Requirements</span></span>



| <span data-ttu-id="57b2e-131">需求</span><span class="sxs-lookup"><span data-stu-id="57b2e-131">Requirement</span></span> | <span data-ttu-id="57b2e-132">值</span><span class="sxs-lookup"><span data-stu-id="57b2e-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="57b2e-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57b2e-133">Minimum supported client</span></span><br/> | <span data-ttu-id="57b2e-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57b2e-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57b2e-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57b2e-135">Minimum supported server</span></span><br/> | <span data-ttu-id="57b2e-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="57b2e-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="57b2e-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="57b2e-137">End of client support</span></span><br/>    | <span data-ttu-id="57b2e-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="57b2e-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="57b2e-139">產品</span><span class="sxs-lookup"><span data-stu-id="57b2e-139">Product</span></span><br/>                  | <span data-ttu-id="57b2e-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="57b2e-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="57b2e-141">標頭</span><span class="sxs-lookup"><span data-stu-id="57b2e-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="57b2e-142"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="57b2e-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="57b2e-143">IID</span><span class="sxs-lookup"><span data-stu-id="57b2e-143">IID</span></span><br/>                      | <span data-ttu-id="57b2e-144">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="57b2e-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="57b2e-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57b2e-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57b2e-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="57b2e-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

