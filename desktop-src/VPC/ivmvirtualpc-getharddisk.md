---
title: 'IVMVirtualPC GetHardDisk 方法 (VPCCOMInterfaces .h) '
description: 抓取對應于現有磁片影像檔案的物件。
ms.assetid: 648a3f8a-5114-4c14-b9a9-f175941333ab
keywords:
- GetHardDisk 方法 Virtual PC
- GetHardDisk 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，GetHardDisk 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetHardDisk
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 558d098b6745718830c63dd700c14febf4f6bed2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934858"
---
# <a name="ivmvirtualpcgetharddisk-method"></a><span data-ttu-id="94a95-106">IVMVirtualPC：： GetHardDisk 方法</span><span class="sxs-lookup"><span data-stu-id="94a95-106">IVMVirtualPC::GetHardDisk method</span></span>

<span data-ttu-id="94a95-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="94a95-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="94a95-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="94a95-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="94a95-109">抓取對應于現有磁片影像檔案的物件。</span><span class="sxs-lookup"><span data-stu-id="94a95-109">Retrieves an object corresponding to an existing disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="94a95-110">語法</span><span class="sxs-lookup"><span data-stu-id="94a95-110">Syntax</span></span>


```C++
HRESULT GetHardDisk(
  [in]          BSTR        imagePath,
  [out, retval] IVMHardDisk **hardDisk
);
```



## <a name="parameters"></a><span data-ttu-id="94a95-111">參數</span><span class="sxs-lookup"><span data-stu-id="94a95-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94a95-112">*imagePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="94a95-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="94a95-113">現有磁片影像檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="94a95-113">The full path to an existing disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="94a95-114">*硬碟* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="94a95-114">*hardDisk* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="94a95-115">對應至此磁片映射的 [**IVMHardDisk**](ivmharddisk.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="94a95-115">An [**IVMHardDisk**](ivmharddisk.md) object corresponding to this disk image.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="94a95-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="94a95-116">Return value</span></span>

<span data-ttu-id="94a95-117">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="94a95-117">This method can return one of these values.</span></span>



| <span data-ttu-id="94a95-118">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="94a95-118">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="94a95-119">Description</span><span class="sxs-lookup"><span data-stu-id="94a95-119">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="94a95-120"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="94a95-120"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="94a95-121">作業成功。</span><span class="sxs-lookup"><span data-stu-id="94a95-121">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="94a95-122"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="94a95-122"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="94a95-123">*ImagePath* 或 *硬碟* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="94a95-123">The *imagePath* or *hardDisk* parameter is **NULL**.</span></span><br/>                                                                  |
| <dl> <span data-ttu-id="94a95-124"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="94a95-124"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="94a95-125">系統找不到 *imagePath* 參數所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="94a95-125">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="94a95-126"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="94a95-126"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="94a95-127">系統找不到 *imagePath* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="94a95-127">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="94a95-128"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="94a95-128"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="94a95-129">*ImagePath* 參數包含不正確字元 (" \* ？： <>/ \| " ") 之一。</span><span class="sxs-lookup"><span data-stu-id="94a95-129">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="94a95-130"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="94a95-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="94a95-131">*ImagePath* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="94a95-131">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="94a95-132">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="94a95-132">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="94a95-133"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="94a95-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="94a95-134">*ImagePath* 參數所指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="94a95-134">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="94a95-135">路徑長度必須少於260個字元。</span><span class="sxs-lookup"><span data-stu-id="94a95-135">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="94a95-136"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="94a95-136"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="94a95-137">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="94a95-137">An unexpected error has occurred.</span></span><br/>                                                                                     |
| <dl> <span data-ttu-id="94a95-138"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="94a95-138"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="94a95-139">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="94a95-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="94a95-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="94a95-140">Requirements</span></span>



| <span data-ttu-id="94a95-141">需求</span><span class="sxs-lookup"><span data-stu-id="94a95-141">Requirement</span></span> | <span data-ttu-id="94a95-142">值</span><span class="sxs-lookup"><span data-stu-id="94a95-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="94a95-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="94a95-143">Minimum supported client</span></span><br/> | <span data-ttu-id="94a95-144">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="94a95-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="94a95-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="94a95-145">Minimum supported server</span></span><br/> | <span data-ttu-id="94a95-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="94a95-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="94a95-147">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="94a95-147">End of client support</span></span><br/>    | <span data-ttu-id="94a95-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="94a95-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="94a95-149">產品</span><span class="sxs-lookup"><span data-stu-id="94a95-149">Product</span></span><br/>                  | <span data-ttu-id="94a95-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="94a95-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="94a95-151">標頭</span><span class="sxs-lookup"><span data-stu-id="94a95-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="94a95-152"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="94a95-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="94a95-153">IID</span><span class="sxs-lookup"><span data-stu-id="94a95-153">IID</span></span><br/>                      | <span data-ttu-id="94a95-154">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="94a95-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="94a95-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94a95-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94a95-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="94a95-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

