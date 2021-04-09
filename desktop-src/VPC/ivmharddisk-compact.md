---
title: 'IVMHardDisk Compact 方法 (VPCCOMInterfaces .h) '
description: 壓縮動態擴充的虛擬硬碟映射。
ms.assetid: bd3ec493-1bc0-4c28-8b41-56beac3d0d6d
keywords:
- Compact 方法 Virtual PC
- Compact 方法 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，Compact 方法
topic_type:
- apiref
api_name:
- IVMHardDisk.Compact
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 51b28b47709fdf956b679a4f16c50adde4a1b335
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686344"
---
# <a name="ivmharddiskcompact-method"></a><span data-ttu-id="a88c1-106">IVMHardDisk：： Compact 方法</span><span class="sxs-lookup"><span data-stu-id="a88c1-106">IVMHardDisk::Compact method</span></span>

<span data-ttu-id="a88c1-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="a88c1-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="a88c1-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="a88c1-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="a88c1-109">壓縮動態擴充的虛擬硬碟映射。</span><span class="sxs-lookup"><span data-stu-id="a88c1-109">Compacts a dynamically expanding virtual hard disk image.</span></span>

## <a name="syntax"></a><span data-ttu-id="a88c1-110">語法</span><span class="sxs-lookup"><span data-stu-id="a88c1-110">Syntax</span></span>


```C++
HRESULT Compact(
  [out, retval] IVMTask **compactTask
);
```



## <a name="parameters"></a><span data-ttu-id="a88c1-111">參數</span><span class="sxs-lookup"><span data-stu-id="a88c1-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a88c1-112">*compactTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="a88c1-112">*compactTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="a88c1-113">用來追蹤完成壓縮進程的 [**IVMTask**](ivmtask.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="a88c1-113">An [**IVMTask**](ivmtask.md) object that is used to track the completion the compaction process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a88c1-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="a88c1-114">Return value</span></span>

<span data-ttu-id="a88c1-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="a88c1-115">This method can return one of these values.</span></span>



| <span data-ttu-id="a88c1-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="a88c1-116">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="a88c1-117">Description</span><span class="sxs-lookup"><span data-stu-id="a88c1-117">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a88c1-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a88c1-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="a88c1-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="a88c1-119">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="a88c1-120"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="a88c1-120"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="a88c1-121">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="a88c1-121">An unexpected error has occurred.</span></span><br/>                                                                                                    |
| <dl> <span data-ttu-id="a88c1-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="a88c1-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="a88c1-123">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="a88c1-123">The parameter is **NULL**.</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="a88c1-124"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 共用 \_ 違規)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="a88c1-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="a88c1-125">這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟映射正在使用中。</span><span class="sxs-lookup"><span data-stu-id="a88c1-125">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is in use.</span></span><br/>                                  |
| <dl> <span data-ttu-id="a88c1-126"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 磁片已 \_ 滿)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="a88c1-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="a88c1-127">主機磁片區的空間不足，無法建立壓縮此虛擬硬碟映射所需的暫存檔案。</span><span class="sxs-lookup"><span data-stu-id="a88c1-127">The host volume does not have enough space to create a temporary file needed for the compaction of this virtual hard disk image.</span></span><br/>     |
| <dl> <span data-ttu-id="a88c1-128"><dt>**VM \_E \_ 應用 \_ 程式 \_ 關閉**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="a88c1-128"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="a88c1-129">無法壓縮虛擬硬碟映射，因為應用程式正在關閉。</span><span class="sxs-lookup"><span data-stu-id="a88c1-129">The virtual hard disk image cannot be compacted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="a88c1-130"><dt>**VM \_E \_ FILE \_ READ \_ ONLY**</dt> <dt>0xA004067A</dt></span><span class="sxs-lookup"><span data-stu-id="a88c1-130"><dt>**VM\_E\_FILE\_READ\_ONLY**</dt> <dt>0xA004067A</dt></span></span> </dl>                         | <span data-ttu-id="a88c1-131">這個 [**IVMHardDisk**](ivmharddisk.md) 物件所參考的虛擬硬碟映射會標示為唯讀。</span><span class="sxs-lookup"><span data-stu-id="a88c1-131">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is marked as read only.</span></span><br/>                     |
| <dl> <span data-ttu-id="a88c1-132"><dt>**VM \_E \_ 錯誤的 \_ HD \_ 映射 \_ 類型**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="a88c1-132"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="a88c1-133">這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟映射必須是 **vmDiskTypeDynamic** 映射類型。</span><span class="sxs-lookup"><span data-stu-id="a88c1-133">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object must be a **vmDiskTypeDynamic** image type.</span></span><br/> |
| <dl> <span data-ttu-id="a88c1-134"><dt>**VM \_E \_ 不正確 \_ HD \_ FILE**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="a88c1-134"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="a88c1-135">這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟映射似乎不是有效的映射。</span><span class="sxs-lookup"><span data-stu-id="a88c1-135">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |



 

## <a name="remarks"></a><span data-ttu-id="a88c1-136">備註</span><span class="sxs-lookup"><span data-stu-id="a88c1-136">Remarks</span></span>

<span data-ttu-id="a88c1-137">若要壓縮動態擴充的硬碟映射，應先將磁片映射上的可用空間清空。</span><span class="sxs-lookup"><span data-stu-id="a88c1-137">To compact a dynamically expanding hard disk image, free space on the disk image should first be zeroed.</span></span>

## <a name="requirements"></a><span data-ttu-id="a88c1-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="a88c1-138">Requirements</span></span>



| <span data-ttu-id="a88c1-139">需求</span><span class="sxs-lookup"><span data-stu-id="a88c1-139">Requirement</span></span> | <span data-ttu-id="a88c1-140">值</span><span class="sxs-lookup"><span data-stu-id="a88c1-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="a88c1-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a88c1-141">Minimum supported client</span></span><br/> | <span data-ttu-id="a88c1-142">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a88c1-142">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a88c1-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a88c1-143">Minimum supported server</span></span><br/> | <span data-ttu-id="a88c1-144">都不支援</span><span class="sxs-lookup"><span data-stu-id="a88c1-144">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="a88c1-145">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="a88c1-145">End of client support</span></span><br/>    | <span data-ttu-id="a88c1-146">Windows 7</span><span class="sxs-lookup"><span data-stu-id="a88c1-146">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="a88c1-147">產品</span><span class="sxs-lookup"><span data-stu-id="a88c1-147">Product</span></span><br/>                  | <span data-ttu-id="a88c1-148">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="a88c1-148">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="a88c1-149">標頭</span><span class="sxs-lookup"><span data-stu-id="a88c1-149">Header</span></span><br/>                   | <dl> <span data-ttu-id="a88c1-150"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="a88c1-150"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="a88c1-151">IID</span><span class="sxs-lookup"><span data-stu-id="a88c1-151">IID</span></span><br/>                      | <span data-ttu-id="a88c1-152">IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="a88c1-152">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="a88c1-153">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a88c1-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a88c1-154">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="a88c1-154">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

