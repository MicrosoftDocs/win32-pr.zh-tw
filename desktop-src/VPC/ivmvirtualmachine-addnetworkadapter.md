---
title: 'IVMVirtualMachine AddNetworkAdapter 方法 (VPCCOMInterfaces .h) '
description: 將網路介面新增至虛擬機器。
ms.assetid: 1fa39d2c-4a5a-42cb-afa4-520bf19b8cc8
keywords:
- AddNetworkAdapter 方法 Virtual PC
- AddNetworkAdapter 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，AddNetworkAdapter 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.AddNetworkAdapter
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8d24351e5f5a32aff08e755329ac12baaaaf546
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966940"
---
# <a name="ivmvirtualmachineaddnetworkadapter-method"></a><span data-ttu-id="76253-106">IVMVirtualMachine：： AddNetworkAdapter 方法</span><span class="sxs-lookup"><span data-stu-id="76253-106">IVMVirtualMachine::AddNetworkAdapter method</span></span>

<span data-ttu-id="76253-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="76253-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="76253-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="76253-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="76253-109">將網路介面新增至虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="76253-109">Adds a network interface to the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="76253-110">語法</span><span class="sxs-lookup"><span data-stu-id="76253-110">Syntax</span></span>


```C++
HRESULT AddNetworkAdapter(
  [out, retval] IVMNetworkAdapter **networkAdapter
);
```



## <a name="parameters"></a><span data-ttu-id="76253-111">參數</span><span class="sxs-lookup"><span data-stu-id="76253-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="76253-112">*networkAdapter* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="76253-112">*networkAdapter* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="76253-113">[**IVMNetworkAdapter**](ivmnetworkadapter.md)物件。</span><span class="sxs-lookup"><span data-stu-id="76253-113">An [**IVMNetworkAdapter**](ivmnetworkadapter.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="76253-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="76253-114">Return value</span></span>

<span data-ttu-id="76253-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="76253-115">This method can return one of these values.</span></span>



| <span data-ttu-id="76253-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="76253-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="76253-117">Description</span><span class="sxs-lookup"><span data-stu-id="76253-117">Description</span></span>                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <span data-ttu-id="76253-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="76253-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="76253-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="76253-119">The operation was successful.</span></span><br/>                        |
| <dl> <span data-ttu-id="76253-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="76253-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="76253-121">*NetworkAdapter* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="76253-121">The *networkAdapter* parameter is **NULL**.</span></span><br/>          |
| <dl> <span data-ttu-id="76253-122"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="76253-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="76253-123">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="76253-123">The configuration is unknown.</span></span><br/>                        |
| <dl> <span data-ttu-id="76253-124"><dt>**VM \_E \_ PREF 不 \_ 合法的 \_ 值**</dt> <dt>0xA0040301</dt></span><span class="sxs-lookup"><span data-stu-id="76253-124"><dt>**VM\_E\_PREF\_ILLEGAL\_VALUE**</dt> <dt>0xA0040301</dt></span></span> </dl>   | <span data-ttu-id="76253-125">您可以新增四個以上的 (4) 網路介面卡。</span><span class="sxs-lookup"><span data-stu-id="76253-125">No more than four (4) network adapters can be added.</span></span><br/> |
| <dl> <span data-ttu-id="76253-126"><dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="76253-126"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="76253-127">虛擬機器處於執行中或已儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="76253-127">The virtual machine is in a running or saved state.</span></span><br/>  |
| <dl> <span data-ttu-id="76253-128"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="76253-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="76253-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="76253-129">An unexpected error has occurred.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="76253-130">備註</span><span class="sxs-lookup"><span data-stu-id="76253-130">Remarks</span></span>

<span data-ttu-id="76253-131">您只能將新的網路介面新增至已停止的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="76253-131">You can only add a new network interface to a stopped virtual machine.</span></span> <span data-ttu-id="76253-132">新建立的網路介面卡未連接至虛擬網路。</span><span class="sxs-lookup"><span data-stu-id="76253-132">The newly created network adapter is not connected to a virtual network.</span></span>

## <a name="requirements"></a><span data-ttu-id="76253-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="76253-133">Requirements</span></span>



| <span data-ttu-id="76253-134">需求</span><span class="sxs-lookup"><span data-stu-id="76253-134">Requirement</span></span> | <span data-ttu-id="76253-135">值</span><span class="sxs-lookup"><span data-stu-id="76253-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="76253-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="76253-136">Minimum supported client</span></span><br/> | <span data-ttu-id="76253-137">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="76253-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="76253-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="76253-138">Minimum supported server</span></span><br/> | <span data-ttu-id="76253-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="76253-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="76253-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="76253-140">End of client support</span></span><br/>    | <span data-ttu-id="76253-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="76253-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="76253-142">產品</span><span class="sxs-lookup"><span data-stu-id="76253-142">Product</span></span><br/>                  | <span data-ttu-id="76253-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="76253-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="76253-144">標頭</span><span class="sxs-lookup"><span data-stu-id="76253-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="76253-145"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="76253-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="76253-146">IID</span><span class="sxs-lookup"><span data-stu-id="76253-146">IID</span></span><br/>                      | <span data-ttu-id="76253-147">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="76253-147">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="76253-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="76253-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="76253-149">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="76253-149">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

