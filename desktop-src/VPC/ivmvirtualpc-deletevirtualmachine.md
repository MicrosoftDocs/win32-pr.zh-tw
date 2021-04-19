---
title: 'IVMVirtualPC DeleteVirtualMachine 方法 (VPCCOMInterfaces .h) '
description: 刪除虛擬機器設定。
ms.assetid: fc2562f3-6a83-4a40-b800-0bc2692beae8
keywords:
- DeleteVirtualMachine 方法 Virtual PC
- DeleteVirtualMachine 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，DeleteVirtualMachine 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.DeleteVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee9c1591ccd736099fab04cce31c8a8b77b5fb06
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968189"
---
# <a name="ivmvirtualpcdeletevirtualmachine-method"></a><span data-ttu-id="66095-106">IVMVirtualPC：:D eleteVirtualMachine 方法</span><span class="sxs-lookup"><span data-stu-id="66095-106">IVMVirtualPC::DeleteVirtualMachine method</span></span>

<span data-ttu-id="66095-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="66095-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="66095-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="66095-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="66095-109">刪除虛擬機器設定。</span><span class="sxs-lookup"><span data-stu-id="66095-109">Deletes a virtual machine configuration.</span></span>

## <a name="syntax"></a><span data-ttu-id="66095-110">語法</span><span class="sxs-lookup"><span data-stu-id="66095-110">Syntax</span></span>


```C++
HRESULT DeleteVirtualMachine(
  [in] IVMVirtualMachine *virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="66095-111">參數</span><span class="sxs-lookup"><span data-stu-id="66095-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66095-112">*virtualMachine* \[在\]</span><span class="sxs-lookup"><span data-stu-id="66095-112">*virtualMachine* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66095-113">[**IVMVirtualMachine**](ivmvirtualmachine.md)物件的指標，代表要刪除的虛擬機器設定。</span><span class="sxs-lookup"><span data-stu-id="66095-113">A pointer to an [**IVMVirtualMachine**](ivmvirtualmachine.md) object representing the virtual machine configuration to be deleted.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66095-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="66095-114">Return value</span></span>

<span data-ttu-id="66095-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="66095-115">This method can return one of these values.</span></span>



| <span data-ttu-id="66095-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="66095-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="66095-117">Description</span><span class="sxs-lookup"><span data-stu-id="66095-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="66095-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="66095-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="66095-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="66095-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="66095-120"><dt>**S \_FALSE**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="66095-120"><dt>**S\_FALSE**</dt> <dt>1</dt></span></span> </dl>                                           | <span data-ttu-id="66095-121">找不到指定的設定。</span><span class="sxs-lookup"><span data-stu-id="66095-121">The specified configuration could not be found.</span></span><br/>                                      |
| <dl> <span data-ttu-id="66095-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="66095-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="66095-123">*VirtualMachine* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="66095-123">The *virtualMachine* parameter was **NULL**.</span></span><br/>                                         |
| <dl> <span data-ttu-id="66095-124"><dt>**VM \_E \_ VM \_ 正在**</dt>執行 <dt>0xA0040500</dt></span><span class="sxs-lookup"><span data-stu-id="66095-124"><dt>**VM\_E\_VM\_RUNNING**</dt> <dt>0xA0040500</dt></span></span> </dl>                        | <span data-ttu-id="66095-125">虛擬機器未執行。</span><span class="sxs-lookup"><span data-stu-id="66095-125">The virtual machine is running.</span></span><br/>                                                      |
| <dl> <span data-ttu-id="66095-126"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="66095-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="66095-127">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="66095-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="66095-128"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="66095-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="66095-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="66095-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="66095-130">備註</span><span class="sxs-lookup"><span data-stu-id="66095-130">Remarks</span></span>

<span data-ttu-id="66095-131">只有已停止的虛擬機器可以刪除。</span><span class="sxs-lookup"><span data-stu-id="66095-131">Only stopped virtual machines can be deleted.</span></span> <span data-ttu-id="66095-132">請注意，除了設定檔案之外，也會刪除此設定的任何現有儲存狀態或復原磁片磁碟機資料。</span><span class="sxs-lookup"><span data-stu-id="66095-132">Note that any existing saved state or undo drive data for this configuration will be deleted in addition to the configuration file.</span></span>

## <a name="requirements"></a><span data-ttu-id="66095-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="66095-133">Requirements</span></span>



| <span data-ttu-id="66095-134">需求</span><span class="sxs-lookup"><span data-stu-id="66095-134">Requirement</span></span> | <span data-ttu-id="66095-135">值</span><span class="sxs-lookup"><span data-stu-id="66095-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="66095-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="66095-136">Minimum supported client</span></span><br/> | <span data-ttu-id="66095-137">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="66095-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="66095-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="66095-138">Minimum supported server</span></span><br/> | <span data-ttu-id="66095-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="66095-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="66095-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="66095-140">End of client support</span></span><br/>    | <span data-ttu-id="66095-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="66095-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="66095-142">產品</span><span class="sxs-lookup"><span data-stu-id="66095-142">Product</span></span><br/>                  | <span data-ttu-id="66095-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="66095-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="66095-144">標頭</span><span class="sxs-lookup"><span data-stu-id="66095-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="66095-145"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="66095-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="66095-146">IID</span><span class="sxs-lookup"><span data-stu-id="66095-146">IID</span></span><br/>                      | <span data-ttu-id="66095-147">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="66095-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="66095-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="66095-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66095-149">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="66095-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

