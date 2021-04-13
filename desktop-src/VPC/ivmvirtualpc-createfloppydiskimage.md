---
title: 'IVMVirtualPC CreateFloppyDiskImage 方法 (VPCCOMInterfaces .h) '
description: 建立磁片影像檔案。
ms.assetid: 474e86a4-2019-41bd-9361-e494291d1961
keywords:
- CreateFloppyDiskImage 方法 Virtual PC
- CreateFloppyDiskImage 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，CreateFloppyDiskImage 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateFloppyDiskImage
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ff94ba5cb922aeb75f4effac413bb83b080b3fd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466264"
---
# <a name="ivmvirtualpccreatefloppydiskimage-method"></a><span data-ttu-id="35403-106">IVMVirtualPC：： CreateFloppyDiskImage 方法</span><span class="sxs-lookup"><span data-stu-id="35403-106">IVMVirtualPC::CreateFloppyDiskImage method</span></span>

<span data-ttu-id="35403-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="35403-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="35403-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="35403-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="35403-109">建立磁片影像檔案。</span><span class="sxs-lookup"><span data-stu-id="35403-109">Creates a floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="35403-110">語法</span><span class="sxs-lookup"><span data-stu-id="35403-110">Syntax</span></span>


```C++
HRESULT CreateFloppyDiskImage(
  [in] BSTR                  imagePath,
  [in] VMFloppyDiskImageType imageType
);
```



## <a name="parameters"></a><span data-ttu-id="35403-111">參數</span><span class="sxs-lookup"><span data-stu-id="35403-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35403-112">*imagePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35403-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35403-113">新磁片影像檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="35403-113">The full path to the new disk image file.</span></span> <span data-ttu-id="35403-114">如果未存在，將會建立包含的資料夾。</span><span class="sxs-lookup"><span data-stu-id="35403-114">The containing folder will be created if it does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="35403-115">*imageType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="35403-115">*imageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35403-116">要建立的磁片映射類型。</span><span class="sxs-lookup"><span data-stu-id="35403-116">The type of floppy disk image to create.</span></span> <span data-ttu-id="35403-117">只支援 **vmFloppyDiskImage \_ LowDensity** (1) 和 **vmFloppyDiskImage \_ HighDensity** (2) 。</span><span class="sxs-lookup"><span data-stu-id="35403-117">Only **vmFloppyDiskImage\_LowDensity** (1) and **vmFloppyDiskImage\_HighDensity** (2) are supported.</span></span> <span data-ttu-id="35403-118">請參閱 [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md)。</span><span class="sxs-lookup"><span data-stu-id="35403-118">See [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35403-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="35403-119">Return value</span></span>

<span data-ttu-id="35403-120">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="35403-120">This method can return one of these values.</span></span>



| <span data-ttu-id="35403-121">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="35403-121">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="35403-122">Description</span><span class="sxs-lookup"><span data-stu-id="35403-122">Description</span></span>                                                                                                                                               |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35403-123"><dt>**S \_ 確定**</dt></span><span class="sxs-lookup"><span data-stu-id="35403-123"><dt>**S\_OK**</dt></span></span> </dl>                                                                                                         | <span data-ttu-id="35403-124">作業成功。</span><span class="sxs-lookup"><span data-stu-id="35403-124">The operation was successful.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="35403-125"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="35403-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="35403-126">*ImagePath* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="35403-126">The *imagePath* parameter is **NULL**.</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="35403-127"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="35403-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="35403-128">*ImageType* 參數不是 [**vmFloppyDiskImage \_ LowDensity**](vmfloppydiskimagetype.md) (1) 或 **vmFloppyDiskImage \_ HighDensity** (2) 。</span><span class="sxs-lookup"><span data-stu-id="35403-128">The *imageType* parameter is not [**vmFloppyDiskImage\_LowDensity**](vmfloppydiskimagetype.md) (1) or **vmFloppyDiskImage\_HighDensity** (2).</span></span><br/> |
| <dl> <span data-ttu-id="35403-129"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="35403-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="35403-130">系統找不到 *imagePath* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="35403-130">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                                                        |
| <dl> <span data-ttu-id="35403-131"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="35403-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="35403-132">*ImagePath* 參數包含不正確字元 (" \* ？： <>/ \| " ") 之一。</span><span class="sxs-lookup"><span data-stu-id="35403-132">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                           |
| <dl> <span data-ttu-id="35403-133"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="35403-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="35403-134">*ImagePath* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="35403-134">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="35403-135">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="35403-135">An absolute path is required.</span></span><br/>                                                   |
| <dl> <span data-ttu-id="35403-136"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="35403-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="35403-137">*ImagePath* 參數所指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="35403-137">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="35403-138">路徑長度必須少於260個字元。</span><span class="sxs-lookup"><span data-stu-id="35403-138">The length of the path must be less than 260 characters.</span></span><br/>                          |
| <dl> <span data-ttu-id="35403-139"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="35403-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="35403-140">參數 *imagePath* 所參考的檔案已經存在。</span><span class="sxs-lookup"><span data-stu-id="35403-140">The file referenced by the parameter *imagePath* already exists.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="35403-141"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 磁片已 \_ 滿)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="35403-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>       | <span data-ttu-id="35403-142">主機磁片區上的空間不足，無法建立虛擬磁片映射。</span><span class="sxs-lookup"><span data-stu-id="35403-142">There is insufficient space on the host volume to create the virtual floppy disk image.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="35403-143"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="35403-143"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="35403-144">發生意外錯誤。</span><span class="sxs-lookup"><span data-stu-id="35403-144">An unexpected error occurred.</span></span><br/>                                                                                                                  |
| <dl> <span data-ttu-id="35403-145"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="35403-145"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="35403-146">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="35403-146">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                           |



 

## <a name="requirements"></a><span data-ttu-id="35403-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="35403-147">Requirements</span></span>



| <span data-ttu-id="35403-148">需求</span><span class="sxs-lookup"><span data-stu-id="35403-148">Requirement</span></span> | <span data-ttu-id="35403-149">值</span><span class="sxs-lookup"><span data-stu-id="35403-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="35403-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="35403-150">Minimum supported client</span></span><br/> | <span data-ttu-id="35403-151">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="35403-151">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="35403-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="35403-152">Minimum supported server</span></span><br/> | <span data-ttu-id="35403-153">都不支援</span><span class="sxs-lookup"><span data-stu-id="35403-153">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="35403-154">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="35403-154">End of client support</span></span><br/>    | <span data-ttu-id="35403-155">Windows 7</span><span class="sxs-lookup"><span data-stu-id="35403-155">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="35403-156">產品</span><span class="sxs-lookup"><span data-stu-id="35403-156">Product</span></span><br/>                  | <span data-ttu-id="35403-157">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="35403-157">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="35403-158">標頭</span><span class="sxs-lookup"><span data-stu-id="35403-158">Header</span></span><br/>                   | <dl> <span data-ttu-id="35403-159"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="35403-159"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="35403-160">IID</span><span class="sxs-lookup"><span data-stu-id="35403-160">IID</span></span><br/>                      | <span data-ttu-id="35403-161">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="35403-161">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="35403-162">另請參閱</span><span class="sxs-lookup"><span data-stu-id="35403-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35403-163">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="35403-163">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

