---
title: 'IVMVirtualMachine RemoveDVDROMDrive 方法 (VPCCOMInterfaces .h) '
description: 從虛擬機器移除指定的 CD 或 DVD 光碟機。
ms.assetid: 1c45c271-bead-41f6-8371-448d385a1288
keywords:
- RemoveDVDROMDrive 方法 Virtual PC
- RemoveDVDROMDrive 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，RemoveDVDROMDrive 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveDVDROMDrive
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf0962b388c318d5abebdbd7a021a4466e644a28
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104099"
---
# <a name="ivmvirtualmachineremovedvdromdrive-method"></a><span data-ttu-id="97ca3-106">IVMVirtualMachine：： RemoveDVDROMDrive 方法</span><span class="sxs-lookup"><span data-stu-id="97ca3-106">IVMVirtualMachine::RemoveDVDROMDrive method</span></span>

<span data-ttu-id="97ca3-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="97ca3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="97ca3-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="97ca3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="97ca3-109">從虛擬機器移除指定的 CD 或 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="97ca3-109">Removes the specified CD or DVD drive from the virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="97ca3-110">語法</span><span class="sxs-lookup"><span data-stu-id="97ca3-110">Syntax</span></span>


```C++
HRESULT RemoveDVDROMDrive(
  [in] IVMDVDDrive *dvdDrive
);
```



## <a name="parameters"></a><span data-ttu-id="97ca3-111">參數</span><span class="sxs-lookup"><span data-stu-id="97ca3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="97ca3-112">*dvdDrive* \[在\]</span><span class="sxs-lookup"><span data-stu-id="97ca3-112">*dvdDrive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="97ca3-113">要移除的磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="97ca3-113">The drive to be removed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="97ca3-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="97ca3-114">Return value</span></span>

<span data-ttu-id="97ca3-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="97ca3-115">This method can return one of these values.</span></span>



| <span data-ttu-id="97ca3-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="97ca3-116">Return code/value</span></span>                                                                                                                                                            | <span data-ttu-id="97ca3-117">Description</span><span class="sxs-lookup"><span data-stu-id="97ca3-117">Description</span></span>                                                           |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <span data-ttu-id="97ca3-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="97ca3-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                  | <span data-ttu-id="97ca3-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="97ca3-119">The operation was successful.</span></span><br/>                              |
| <dl> <span data-ttu-id="97ca3-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="97ca3-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                    | <span data-ttu-id="97ca3-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="97ca3-121">The parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="97ca3-122"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="97ca3-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>            | <span data-ttu-id="97ca3-123">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="97ca3-123">The configuration is unknown.</span></span><br/>                              |
| <dl> <span data-ttu-id="97ca3-124"><dt>**VM \_E \_ VM \_ 正在執行 \_ 或 \_ 已儲存的**</dt> <dt>0xA004020B</dt></span><span class="sxs-lookup"><span data-stu-id="97ca3-124"><dt>**VM\_E\_VM\_RUNNING\_OR\_SAVED**</dt> <dt>0xA004020B</dt></span></span> </dl> | <span data-ttu-id="97ca3-125">虛擬機器處於執行中或已儲存狀態。</span><span class="sxs-lookup"><span data-stu-id="97ca3-125">The virtual machine is in a running or saved state.</span></span><br/>        |
| <dl> <span data-ttu-id="97ca3-126"><dt>**VM \_E \_ 磁片磁碟機 \_ 無效**</dt>的 <dt>0xA0040502</dt></span><span class="sxs-lookup"><span data-stu-id="97ca3-126"><dt>**VM\_E\_DRIVE\_INVALID**</dt> <dt>0xA0040502</dt></span></span> </dl>         | <span data-ttu-id="97ca3-127">指定的磁片磁碟機未連接到此匯流排位置。</span><span class="sxs-lookup"><span data-stu-id="97ca3-127">The drive specified is not connected to this bus location.</span></span><br/> |
| <dl> <span data-ttu-id="97ca3-128"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="97ca3-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>            | <span data-ttu-id="97ca3-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="97ca3-129">An unexpected error has occurred.</span></span><br/>                          |



 

## <a name="remarks"></a><span data-ttu-id="97ca3-130">備註</span><span class="sxs-lookup"><span data-stu-id="97ca3-130">Remarks</span></span>

<span data-ttu-id="97ca3-131">您只能從已停止的虛擬機器中移除現有的 CD 或 DVD 光碟機。</span><span class="sxs-lookup"><span data-stu-id="97ca3-131">You can only remove an existing CD or DVD drive from a stopped virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="97ca3-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="97ca3-132">Requirements</span></span>



| <span data-ttu-id="97ca3-133">需求</span><span class="sxs-lookup"><span data-stu-id="97ca3-133">Requirement</span></span> | <span data-ttu-id="97ca3-134">值</span><span class="sxs-lookup"><span data-stu-id="97ca3-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="97ca3-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97ca3-135">Minimum supported client</span></span><br/> | <span data-ttu-id="97ca3-136">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97ca3-136">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="97ca3-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97ca3-137">Minimum supported server</span></span><br/> | <span data-ttu-id="97ca3-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="97ca3-138">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="97ca3-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="97ca3-139">End of client support</span></span><br/>    | <span data-ttu-id="97ca3-140">Windows 7</span><span class="sxs-lookup"><span data-stu-id="97ca3-140">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="97ca3-141">產品</span><span class="sxs-lookup"><span data-stu-id="97ca3-141">Product</span></span><br/>                  | <span data-ttu-id="97ca3-142">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="97ca3-142">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="97ca3-143">標頭</span><span class="sxs-lookup"><span data-stu-id="97ca3-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="97ca3-144"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="97ca3-144"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="97ca3-145">IID</span><span class="sxs-lookup"><span data-stu-id="97ca3-145">IID</span></span><br/>                      | <span data-ttu-id="97ca3-146">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="97ca3-146">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="97ca3-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97ca3-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97ca3-148">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="97ca3-148">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

