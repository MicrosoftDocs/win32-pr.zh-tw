---
title: 'IVMHardDisk MergeTo 方法 (VPCCOMInterfaces .h) '
description: 將差異虛擬硬碟與其所有父系合併。
ms.assetid: 3c63f892-7c05-4ed6-a59a-914a921ec391
keywords:
- MergeTo 方法 Virtual PC
- MergeTo 方法 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，MergeTo 方法
topic_type:
- apiref
api_name:
- IVMHardDisk.MergeTo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 13d0db44388c8ee021fa8cc8c8fdbfe2c434833f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103967"
---
# <a name="ivmharddiskmergeto-method"></a><span data-ttu-id="1d00f-106">IVMHardDisk：： MergeTo 方法</span><span class="sxs-lookup"><span data-stu-id="1d00f-106">IVMHardDisk::MergeTo method</span></span>

<span data-ttu-id="1d00f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="1d00f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="1d00f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="1d00f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="1d00f-109">將差異虛擬硬碟與其所有父系合併 (（包括根父系虛擬硬碟) ）至新的硬碟檔案。</span><span class="sxs-lookup"><span data-stu-id="1d00f-109">Merges a differencing virtual hard disk with all of its parents (up to and including the root parent virtual hard disk) to a new hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d00f-110">語法</span><span class="sxs-lookup"><span data-stu-id="1d00f-110">Syntax</span></span>


```C++
HRESULT MergeTo(
  [in]          BSTR           newDiskImagePath,
  [in]          VMHardDiskType newDiskImageType,
  [out, retval] IVMTask        **mergeTask
);
```



## <a name="parameters"></a><span data-ttu-id="1d00f-111">參數</span><span class="sxs-lookup"><span data-stu-id="1d00f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d00f-112">*newDiskImagePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d00f-112">*newDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d00f-113">新目標磁片映射的路徑，其中將會合並選取的磁片映射。</span><span class="sxs-lookup"><span data-stu-id="1d00f-113">The path to the new target disk image where the selected disk images will be merged.</span></span>

</dd> <dt>

<span data-ttu-id="1d00f-114">*newDiskImageType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1d00f-114">*newDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1d00f-115">新目標磁片映射的類型。</span><span class="sxs-lookup"><span data-stu-id="1d00f-115">The type of new target disk image.</span></span> <span data-ttu-id="1d00f-116">新目標磁片映射允許的映射類型為 **vmDiskType \_ Dynamic** 和 **vmDiskType \_ FixedSize**。</span><span class="sxs-lookup"><span data-stu-id="1d00f-116">The image types allowed for the new target disk image are **vmDiskType\_Dynamic** and **vmDiskType\_FixedSize**.</span></span> <span data-ttu-id="1d00f-117">如需詳細資訊，請參閱 [**VMHardDiskType**](vmharddisktype.md)。</span><span class="sxs-lookup"><span data-stu-id="1d00f-117">For more information, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d00f-118">*mergeTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="1d00f-118">*mergeTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="1d00f-119">[**IVMTask**](ivmtask.md)物件，用來追蹤合併進程的完成。</span><span class="sxs-lookup"><span data-stu-id="1d00f-119">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the merging process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d00f-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="1d00f-120">Return value</span></span>

<span data-ttu-id="1d00f-121">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1d00f-121">This method can return one of these values.</span></span>



| <span data-ttu-id="1d00f-122">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="1d00f-122">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="1d00f-123">Description</span><span class="sxs-lookup"><span data-stu-id="1d00f-123">Description</span></span>                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d00f-124"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="1d00f-125">作業成功。</span><span class="sxs-lookup"><span data-stu-id="1d00f-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="1d00f-126"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="1d00f-127">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="1d00f-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <dl> <span data-ttu-id="1d00f-128"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="1d00f-129">*NewDiskImagePath* 參數是空的。</span><span class="sxs-lookup"><span data-stu-id="1d00f-129">The *newDiskImagePath* parameter is empty.</span></span><br/>                                                                                                                                                                                                                                                         |
| <dl> <span data-ttu-id="1d00f-130"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl>   | <span data-ttu-id="1d00f-131">系統找不到 *newDiskImagePath* 參數所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="1d00f-131">The system cannot find the file specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="1d00f-132"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="1d00f-133">系統找不到 *newDiskImagePath* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="1d00f-133">The system cannot find the path specified by the *newDiskImagePath* parameter.</span></span><br/>                                                                                                                                                                                                                     |
| <dl> <span data-ttu-id="1d00f-134"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="1d00f-135">*NewDiskImagePath* 參數包含不正確字元 (下列其中一項： " \* ？ <>/ \| "： ") 。</span><span class="sxs-lookup"><span data-stu-id="1d00f-135">The *newDiskImagePath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                                                                                                                                                                         |
| <dl> <span data-ttu-id="1d00f-136"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="1d00f-137">*NewDiskImagePath* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="1d00f-137">The *newDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="1d00f-138">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="1d00f-138">An absolute path is required.</span></span><br/>                                                                                                                                                                                                |
| <dl> <span data-ttu-id="1d00f-139"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="1d00f-140">*NewDiskImagePath* 參數所指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="1d00f-140">The path specified by the *newDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="1d00f-141">路徑必須少於260個字元。</span><span class="sxs-lookup"><span data-stu-id="1d00f-141">The path must be less than 260 characters.</span></span><br/>                                                                                                                                                                                     |
| <dl> <span data-ttu-id="1d00f-142"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 共用 \_ 違規)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="1d00f-143">此物件參考的虛擬硬碟正在使用中，或此虛擬硬碟的父系正在使用中。</span><span class="sxs-lookup"><span data-stu-id="1d00f-143">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                                                                                                                                                                                |
| <dl> <span data-ttu-id="1d00f-144"><dt>**VM \_E \_ 錯誤的 \_ HD \_ 映射 \_ 類型**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-144"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="1d00f-145">此錯誤的原因是因為這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟映射不是差異磁片映射，或是因為參數 *newDiskImageType* 不是其中一個可接受的值 **vmDiskType \_ Dynamic** 或 **vmDiskType \_ FixedSize**。</span><span class="sxs-lookup"><span data-stu-id="1d00f-145">This error is caused either because the virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object is not a differencing disk image or because the parameter *newDiskImageType* is not one of the accepted values, **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/> |
| <dl> <span data-ttu-id="1d00f-146"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-146"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="1d00f-147">*NewDiskImagePath* 參數所參考的檔案已經存在。</span><span class="sxs-lookup"><span data-stu-id="1d00f-147">The file referenced by the *newDiskImagePath* parameter already exists.</span></span><br/>                                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="1d00f-148"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 磁片已 \_ 滿)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-148"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="1d00f-149">主機磁片區的空間不足，無法合併此虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="1d00f-149">The host volume does not have enough space to merge this virtual hard disk.</span></span><br/>                                                                                                                                                                                                                        |
| <dl> <span data-ttu-id="1d00f-150"><dt>**VM \_E \_ \_ \_ \_ 找不到父路徑**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-150"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="1d00f-151">此物件參考的虛擬硬碟父系不存在。</span><span class="sxs-lookup"><span data-stu-id="1d00f-151">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                                                                                                                                                                                      |
| <dl> <span data-ttu-id="1d00f-152"><dt>**VM \_E \_ 應用 \_ 程式 \_ 關閉**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-152"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="1d00f-153">無法合併虛擬硬碟映射，因為應用程式正在關閉。</span><span class="sxs-lookup"><span data-stu-id="1d00f-153">The virtual hard disk image cannot be merged because the application is shutting down.</span></span><br/>                                                                                                                                                                                                             |
| <dl> <span data-ttu-id="1d00f-154"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-154"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="1d00f-155">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="1d00f-155">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                                                                                  |



 

## <a name="requirements"></a><span data-ttu-id="1d00f-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="1d00f-156">Requirements</span></span>



| <span data-ttu-id="1d00f-157">需求</span><span class="sxs-lookup"><span data-stu-id="1d00f-157">Requirement</span></span> | <span data-ttu-id="1d00f-158">值</span><span class="sxs-lookup"><span data-stu-id="1d00f-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d00f-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1d00f-159">Minimum supported client</span></span><br/> | <span data-ttu-id="1d00f-160">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1d00f-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1d00f-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1d00f-161">Minimum supported server</span></span><br/> | <span data-ttu-id="1d00f-162">都不支援</span><span class="sxs-lookup"><span data-stu-id="1d00f-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="1d00f-163">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="1d00f-163">End of client support</span></span><br/>    | <span data-ttu-id="1d00f-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="1d00f-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="1d00f-165">產品</span><span class="sxs-lookup"><span data-stu-id="1d00f-165">Product</span></span><br/>                  | <span data-ttu-id="1d00f-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="1d00f-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="1d00f-167">標頭</span><span class="sxs-lookup"><span data-stu-id="1d00f-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="1d00f-168"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="1d00f-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="1d00f-169">IID</span><span class="sxs-lookup"><span data-stu-id="1d00f-169">IID</span></span><br/>                      | <span data-ttu-id="1d00f-170">IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="1d00f-170">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="1d00f-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1d00f-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d00f-172">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="1d00f-172">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

