---
title: 'IVMHardDisk Merge 方法 (VPCCOMInterfaces .h) '
description: 合併差異虛擬硬碟與其父磁片映射。
ms.assetid: e2aca4d3-79c1-416a-b135-f4680c03d200
keywords:
- 合併方法虛擬電腦
- Merge 方法 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，Merge 方法
topic_type:
- apiref
api_name:
- IVMHardDisk.Merge
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bb5e4b32cb1df2f754463cee7f8275b00f86513b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934570"
---
# <a name="ivmharddiskmerge-method"></a><span data-ttu-id="f3393-106">IVMHardDisk：： Merge 方法</span><span class="sxs-lookup"><span data-stu-id="f3393-106">IVMHardDisk::Merge method</span></span>

<span data-ttu-id="f3393-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="f3393-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="f3393-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="f3393-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="f3393-109">合併差異虛擬硬碟與其父磁片映射。</span><span class="sxs-lookup"><span data-stu-id="f3393-109">Merges a differencing virtual hard disk with its parent disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3393-110">語法</span><span class="sxs-lookup"><span data-stu-id="f3393-110">Syntax</span></span>


```C++
HRESULT Merge(
  [out, retval] IVMTask **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="f3393-111">參數</span><span class="sxs-lookup"><span data-stu-id="f3393-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f3393-112">*mergeTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="f3393-112">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="f3393-113">[**IVMTask**](ivmtask.md)物件，用來追蹤合併進程的完成。</span><span class="sxs-lookup"><span data-stu-id="f3393-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f3393-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f3393-114">Return value</span></span>

<span data-ttu-id="f3393-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="f3393-115">This method can return one of these values.</span></span>



| <span data-ttu-id="f3393-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="f3393-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="f3393-117">Description</span><span class="sxs-lookup"><span data-stu-id="f3393-117">Description</span></span>                                                                                                                                                                                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f3393-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f3393-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="f3393-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="f3393-119">The operation was successful.</span></span><br/>                                                                                                                                                                                          |
| <dl> <span data-ttu-id="f3393-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="f3393-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="f3393-121">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="f3393-121">The parameter is **NULL**.</span></span><br/>                                                                                                                                                                                             |
| <dl> <span data-ttu-id="f3393-122"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 共用 \_ 違規)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="f3393-122"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="f3393-123">這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟映射正在使用中，或此虛擬硬碟映射的父系正在使用中。</span><span class="sxs-lookup"><span data-stu-id="f3393-123">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use or the parent of this virtual hard disk image is in use.</span></span> <span data-ttu-id="f3393-124">或者，這些硬碟映射可能是儲存狀態的一部分。</span><span class="sxs-lookup"><span data-stu-id="f3393-124">Or, these hard disk images could be part of a saved state.</span></span><br/> |
| <dl> <span data-ttu-id="f3393-125"><dt>**VM \_E \_ 錯誤的 \_ HD \_ 映射 \_ 類型**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="f3393-125"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="f3393-126">這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟映射必須是差異磁片映射。</span><span class="sxs-lookup"><span data-stu-id="f3393-126">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a differencing disk image.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="f3393-127"><dt>**VM \_E \_ FILE \_ READ \_ ONLY**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="f3393-127"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="f3393-128">這個 [**IVMHardDisk**](ivmharddisk.md) 物件所參考之虛擬硬碟映射的父系會標示為唯讀。</span><span class="sxs-lookup"><span data-stu-id="f3393-128">The parent of virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="f3393-129"><dt>**VM \_E \_ \_ \_ \_ 找不到父路徑**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="f3393-129"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="f3393-130">這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟父系不存在。</span><span class="sxs-lookup"><span data-stu-id="f3393-130">The parent of the virtual hard disk referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not exist.</span></span><br/>                                                                                                       |
| <dl> <span data-ttu-id="f3393-131"><dt>**VM \_E \_ 應用 \_ 程式 \_ 關閉**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="f3393-131"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="f3393-132">無法合併虛擬硬碟映射，因為應用程式正在關閉。</span><span class="sxs-lookup"><span data-stu-id="f3393-132">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                 |
| <dl> <span data-ttu-id="f3393-133"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="f3393-133"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="f3393-134">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="f3393-134">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                      |



 

## <a name="requirements"></a><span data-ttu-id="f3393-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3393-135">Requirements</span></span>



| <span data-ttu-id="f3393-136">需求</span><span class="sxs-lookup"><span data-stu-id="f3393-136">Requirement</span></span> | <span data-ttu-id="f3393-137">值</span><span class="sxs-lookup"><span data-stu-id="f3393-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3393-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3393-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f3393-139">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3393-139">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f3393-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3393-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f3393-141">都不支援</span><span class="sxs-lookup"><span data-stu-id="f3393-141">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="f3393-142">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="f3393-142">End of client support</span></span><br/>    | <span data-ttu-id="f3393-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="f3393-143">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="f3393-144">產品</span><span class="sxs-lookup"><span data-stu-id="f3393-144">Product</span></span><br/>                  | <span data-ttu-id="f3393-145">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="f3393-145">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="f3393-146">標頭</span><span class="sxs-lookup"><span data-stu-id="f3393-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3393-147"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3393-147"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="f3393-148">IID</span><span class="sxs-lookup"><span data-stu-id="f3393-148">IID</span></span><br/>                      | <span data-ttu-id="f3393-149">IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="f3393-149">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="f3393-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3393-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3393-151">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="f3393-151">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

