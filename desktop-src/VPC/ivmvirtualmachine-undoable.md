---
title: IVMVirtualMachine (VPCCOMInterfaces) 的能撤銷屬性
description: 判斷是否已針對連接至 VM 的硬碟啟用復原磁片磁碟機。
ms.assetid: 4f591360-1229-46ae-9925-3a3d02ab3202
keywords:
- 虛擬 PC 的能撤銷
- 虛擬 PC、IVMVirtualMachine 介面、虛擬機器
- IVMVirtualMachine 介面虛擬 PC、能撤銷的屬性
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Undoable
- IVMVirtualMachine.get_Undoable
- IVMVirtualMachine.put_Undoable
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2cbc77f4d68fbdbfcc8d3998e3c207b8f4245c9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508627"
---
# <a name="ivmvirtualmachineundoable-property"></a><span data-ttu-id="1de3b-106">IVMVirtualMachine：：無法撤銷的屬性</span><span class="sxs-lookup"><span data-stu-id="1de3b-106">IVMVirtualMachine::Undoable property</span></span>

<span data-ttu-id="1de3b-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="1de3b-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1de3b-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="1de3b-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1de3b-109">判斷是否已針對連接到虛擬機器 (VM) 的硬碟啟用復原磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="1de3b-109">Determines whether undo drives are enabled for hard disks connected to the virtual machine (VM).</span></span>

<span data-ttu-id="1de3b-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="1de3b-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1de3b-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1de3b-111">Syntax</span></span>


```C++
HRESULT put_Undoable(
  [in]          VARIANT_BOOL enableUndo
);

HRESULT get_Undoable(
  [out, retval] VARIANT_BOOL *isUndoable
);
```



## <a name="property-value"></a><span data-ttu-id="1de3b-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="1de3b-112">Property value</span></span>

<span data-ttu-id="1de3b-113">如果已針對連接至 VM 的硬碟啟用復原磁片磁碟機， **則指定 variant \_ TRUE** ，否則為 **variant \_** 。</span><span class="sxs-lookup"><span data-stu-id="1de3b-113">Specifies **VARIANT\_TRUE** if undo drives are enabled for hard disks connected to the VM and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="1de3b-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="1de3b-114">Error codes</span></span>



| <span data-ttu-id="1de3b-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="1de3b-115">Name/value</span></span>                                                                                                                                                         | <span data-ttu-id="1de3b-116">意義</span><span class="sxs-lookup"><span data-stu-id="1de3b-116">Meaning</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="1de3b-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1de3b-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="1de3b-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="1de3b-118">The operation was successful.</span></span><br/>     |
| <dl> <span data-ttu-id="1de3b-119"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1de3b-119"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="1de3b-120">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1de3b-120">An unexpected error has occurred.</span></span><br/> |
| <dl> <span data-ttu-id="1de3b-121"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1de3b-121"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="1de3b-122">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1de3b-122">The parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="1de3b-123"><dt>VM \_E \_ VM \_ 不明</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="1de3b-123"><dt>VM\_E\_VM\_UNKNOWN</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="1de3b-124">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="1de3b-124">The configuration is unknown.</span></span><br/>     |
| <dl> <span data-ttu-id="1de3b-125"><dt>VM \_E \_ PREF \_ VM \_ ACTIVE</dt> <dt>0xA0040302</dt></span><span class="sxs-lookup"><span data-stu-id="1de3b-125"><dt>VM\_E\_PREF\_VM\_ACTIVE</dt> <dt>0xA0040302</dt></span></span> </dl> | <span data-ttu-id="1de3b-126">VM 正在執行或已儲存。</span><span class="sxs-lookup"><span data-stu-id="1de3b-126">The VM is running or saved.</span></span><br/>       |



## <a name="remarks"></a><span data-ttu-id="1de3b-127">備註</span><span class="sxs-lookup"><span data-stu-id="1de3b-127">Remarks</span></span>

<span data-ttu-id="1de3b-128">如果停用復原磁片磁碟機，將會刪除任何現有的復原磁片磁碟機檔案。</span><span class="sxs-lookup"><span data-stu-id="1de3b-128">If undo drives are disabled, any existing undo drive files will be deleted.</span></span>

<span data-ttu-id="1de3b-129">如果 VM 正在執行或已儲存，您就無法設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="1de3b-129">You cannot set this property if the VM is running or saved.</span></span>

## <a name="requirements"></a><span data-ttu-id="1de3b-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="1de3b-130">Requirements</span></span>



| <span data-ttu-id="1de3b-131">需求</span><span class="sxs-lookup"><span data-stu-id="1de3b-131">Requirement</span></span> | <span data-ttu-id="1de3b-132">值</span><span class="sxs-lookup"><span data-stu-id="1de3b-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1de3b-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1de3b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="1de3b-134">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1de3b-134">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1de3b-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1de3b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="1de3b-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="1de3b-136">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1de3b-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1de3b-137">End of client support</span></span><br/>    | <span data-ttu-id="1de3b-138">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1de3b-138">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1de3b-139">產品</span><span class="sxs-lookup"><span data-stu-id="1de3b-139">Product</span></span><br/>                  | <span data-ttu-id="1de3b-140">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1de3b-140">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1de3b-141">標頭</span><span class="sxs-lookup"><span data-stu-id="1de3b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="1de3b-142"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="1de3b-142"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1de3b-143">IID</span><span class="sxs-lookup"><span data-stu-id="1de3b-143">IID</span></span><br/>                      | <span data-ttu-id="1de3b-144">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="1de3b-144">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="1de3b-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1de3b-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1de3b-146">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="1de3b-146">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

