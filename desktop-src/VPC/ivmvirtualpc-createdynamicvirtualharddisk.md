---
title: 'IVMVirtualPC CreateDynamicVirtualHardDisk 方法 (VPCCOMInterfaces .h) '
description: 建立動態調整大小的虛擬硬碟。
ms.assetid: 2373ac41-c4c4-44c6-93e1-92814cd40b81
keywords:
- CreateDynamicVirtualHardDisk 方法 Virtual PC
- CreateDynamicVirtualHardDisk 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，CreateDynamicVirtualHardDisk 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateDynamicVirtualHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d245072fd5b3135decd814a29dd8a87d2b6a956
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385270"
---
# <a name="ivmvirtualpccreatedynamicvirtualharddisk-method"></a><span data-ttu-id="40f6c-106">IVMVirtualPC：： CreateDynamicVirtualHardDisk 方法</span><span class="sxs-lookup"><span data-stu-id="40f6c-106">IVMVirtualPC::CreateDynamicVirtualHardDisk method</span></span>

<span data-ttu-id="40f6c-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="40f6c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="40f6c-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="40f6c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="40f6c-109">建立動態調整大小的虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="40f6c-109">Creates a dynamically resizing virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="40f6c-110">語法</span><span class="sxs-lookup"><span data-stu-id="40f6c-110">Syntax</span></span>


```C++
HRESULT CreateDynamicVirtualHardDisk(
  [in]          BSTR    imagePath,
  [in]          long    size,
  [out, retval] IVMTask **diskTask
);
```



## <a name="parameters"></a><span data-ttu-id="40f6c-111">參數</span><span class="sxs-lookup"><span data-stu-id="40f6c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="40f6c-112">*imagePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40f6c-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40f6c-113">新磁片影像檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="40f6c-113">The full path to the new disk image file.</span></span> <span data-ttu-id="40f6c-114">如果未存在，將會建立包含的資料夾。</span><span class="sxs-lookup"><span data-stu-id="40f6c-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="40f6c-115">*大小* \[在\]</span><span class="sxs-lookup"><span data-stu-id="40f6c-115">*size* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="40f6c-116">影像的大小（以 mb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="40f6c-116">The size of the image, in megabytes.</span></span> <span data-ttu-id="40f6c-117">此值最多可有 2088960 MB 的 (2040GB) 。</span><span class="sxs-lookup"><span data-stu-id="40f6c-117">This value can be at most 2,088,960 MB (2040GB).</span></span>

</dd> <dt>

<span data-ttu-id="40f6c-118">*diskTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="40f6c-118">*diskTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="40f6c-119">用來追蹤影像建立的 [**IVMTask**](ivmtask.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="40f6c-119">An [**IVMTask**](ivmtask.md) object that is used to track the creation of the image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="40f6c-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="40f6c-120">Return value</span></span>

<span data-ttu-id="40f6c-121">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="40f6c-121">This method can return one of these values.</span></span>



| <span data-ttu-id="40f6c-122">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="40f6c-122">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="40f6c-123">Description</span><span class="sxs-lookup"><span data-stu-id="40f6c-123">Description</span></span>                                                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="40f6c-124"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-124"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="40f6c-125">作業成功。</span><span class="sxs-lookup"><span data-stu-id="40f6c-125">The operation was successful.</span></span><br/>                                                                                                                                                                                                       |
| <dl> <span data-ttu-id="40f6c-126"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-126"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="40f6c-127">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="40f6c-127">A parameter is **NULL**.</span></span><br/>                                                                                                                                                                                                            |
| <dl> <span data-ttu-id="40f6c-128"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-128"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="40f6c-129">*Size* 參數小於或等於0。</span><span class="sxs-lookup"><span data-stu-id="40f6c-129">The *size* parameter is less than or equal to 0.</span></span><br/>                                                                                                                                                                                    |
| <dl> <span data-ttu-id="40f6c-130"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="40f6c-131">系統找不到 *imagePath* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="40f6c-131">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                                                                                                             |
| <dl> <span data-ttu-id="40f6c-132"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 不正確 \_ 磁片磁碟機)**</dt> <dt>0x8007000f</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_DRIVE)**</dt> <dt>0x8007000f</dt></span></span> </dl>   | <span data-ttu-id="40f6c-133">*ImagePath* 參數所指定的檔案是在 CD-ROM 或 dvd-rom 上。</span><span class="sxs-lookup"><span data-stu-id="40f6c-133">The file specified by the *imagePath* parameter is on a CD-ROM or DVD-ROM.</span></span><br/>                                                                                                                                                          |
| <dl> <span data-ttu-id="40f6c-134"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="40f6c-135">*ImagePath* 參數包含不正確字元 (" \* ？： <>/ \| " ") 之一。</span><span class="sxs-lookup"><span data-stu-id="40f6c-135">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="40f6c-136"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="40f6c-137">這兩個 *imagePath* 參數都指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="40f6c-137">Both the *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="40f6c-138">至少有一個參數必須是絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="40f6c-138">At least one of the parameters must be an absolute path.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="40f6c-139"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="40f6c-140">*ImagePath* 參數所指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="40f6c-140">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="40f6c-141">路徑長度必須少於260個字元。</span><span class="sxs-lookup"><span data-stu-id="40f6c-141">The length of the path must be less than 260 characters.</span></span><br/>                                                                                                               |
| <dl> <span data-ttu-id="40f6c-142"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="40f6c-143">*ImagePath* 參數所參考的檔案已經存在。</span><span class="sxs-lookup"><span data-stu-id="40f6c-143">The file referenced by the *imagePath* parameter already exists.</span></span><br/>                                                                                                                                                                    |
| <dl> <span data-ttu-id="40f6c-144"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 磁片已 \_ 滿)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-144"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="40f6c-145">動態擴充的虛擬硬碟映射在主機磁片區上需要至少 8 MB 的可用空間。</span><span class="sxs-lookup"><span data-stu-id="40f6c-145">The dynamically expanding virtual hard disk image needs at least 8 MB free on the host volume.</span></span><br/>                                                                                                                                      |
| <dl> <span data-ttu-id="40f6c-146"><dt>**VM \_E \_ 影像 \_ 大小 \_ 太 \_ 大**</dt> <dt>0xA0040683</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-146"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_LARGE**</dt> <dt>0xA0040683</dt></span></span> </dl>                | <span data-ttu-id="40f6c-147">參數 *大小* 必須小於 2088960 MB。</span><span class="sxs-lookup"><span data-stu-id="40f6c-147">The parameter *size* must be less than 2,088,960 MB.</span></span> <span data-ttu-id="40f6c-148">如果格式為 FAT16，則大小必須小於 2000 MB。</span><span class="sxs-lookup"><span data-stu-id="40f6c-148">If the format is FAT16, then size must be less than 2000 MB.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="40f6c-149"><dt>**VM \_E \_ 影像 \_ 大小 \_ 太 \_ 小**</dt> <dt>0xA0040684</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-149"><dt>**VM\_E\_IMAGE\_SIZE\_TOO\_SMALL**</dt> <dt>0xA0040684</dt></span></span> </dl>                | <span data-ttu-id="40f6c-150">未格式化和 FAT16 格式化的虛擬硬碟映射必須至少為 3 MB。</span><span class="sxs-lookup"><span data-stu-id="40f6c-150">Unformatted and FAT16 formatted virtual hard disk images must be at least 3 MB.</span></span> <span data-ttu-id="40f6c-151">FAT32 格式化的虛擬硬碟映射必須至少為 514 MB。</span><span class="sxs-lookup"><span data-stu-id="40f6c-151">FAT32 formatted virtual hard disk images must be at least 514 MB.</span></span><br/>                                                                                   |
| <dl> <span data-ttu-id="40f6c-152"><dt>**VM \_E \_ 檔案 \_ 太 \_ 大 \_ ，無法進行 \_ 磁片**</dt>區 <dt>0xA0040679</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-152"><dt>**VM\_E\_FILE\_TOO\_LARGE\_FOR\_VOLUME**</dt> <dt>0xA0040679</dt></span></span> </dl>          | <span data-ttu-id="40f6c-153">如果動態擴充的虛擬硬碟映射擴展為其完整限制，則主機磁片區無法支援此大小的檔案。</span><span class="sxs-lookup"><span data-stu-id="40f6c-153">The host volume cannot support a file this size if the dynamically expanding virtual hard disk image expands to its full limit.</span></span> <span data-ttu-id="40f6c-154">FAT32 磁片區的檔案大小上限為 4 GB。</span><span class="sxs-lookup"><span data-stu-id="40f6c-154">The maximum file size for a FAT32 volume is 4 GB.</span></span> <span data-ttu-id="40f6c-155">FAT16 磁片區的檔案大小上限為 2 GB。</span><span class="sxs-lookup"><span data-stu-id="40f6c-155">The maximum file size for a FAT16 volume is 2 GB.</span></span><br/> |
| <dl> <span data-ttu-id="40f6c-156"><dt>**VM \_E \_ 應用 \_ 程式 \_ 關閉**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-156"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                    | <span data-ttu-id="40f6c-157">應用程式開始關機之後，無法建立虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="40f6c-157">The virtual hard disk cannot be created after the application has started shutting down.</span></span><br/>                                                                                                                                            |
| <dl> <span data-ttu-id="40f6c-158"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-158"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="40f6c-159">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="40f6c-159">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="40f6c-160"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-160"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="40f6c-161">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="40f6c-161">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                                                   |



 

## <a name="requirements"></a><span data-ttu-id="40f6c-162">規格需求</span><span class="sxs-lookup"><span data-stu-id="40f6c-162">Requirements</span></span>



| <span data-ttu-id="40f6c-163">需求</span><span class="sxs-lookup"><span data-stu-id="40f6c-163">Requirement</span></span> | <span data-ttu-id="40f6c-164">值</span><span class="sxs-lookup"><span data-stu-id="40f6c-164">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="40f6c-165">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="40f6c-165">Minimum supported client</span></span><br/> | <span data-ttu-id="40f6c-166">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="40f6c-166">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="40f6c-167">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="40f6c-167">Minimum supported server</span></span><br/> | <span data-ttu-id="40f6c-168">都不支援</span><span class="sxs-lookup"><span data-stu-id="40f6c-168">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="40f6c-169">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="40f6c-169">End of client support</span></span><br/>    | <span data-ttu-id="40f6c-170">Windows 7</span><span class="sxs-lookup"><span data-stu-id="40f6c-170">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="40f6c-171">產品</span><span class="sxs-lookup"><span data-stu-id="40f6c-171">Product</span></span><br/>                  | <span data-ttu-id="40f6c-172">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="40f6c-172">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="40f6c-173">標頭</span><span class="sxs-lookup"><span data-stu-id="40f6c-173">Header</span></span><br/>                   | <dl> <span data-ttu-id="40f6c-174"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="40f6c-174"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="40f6c-175">IID</span><span class="sxs-lookup"><span data-stu-id="40f6c-175">IID</span></span><br/>                      | <span data-ttu-id="40f6c-176">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="40f6c-176">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="40f6c-177">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40f6c-177">See also</span></span>

<dl> <dt>

[<span data-ttu-id="40f6c-178">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="40f6c-178">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

