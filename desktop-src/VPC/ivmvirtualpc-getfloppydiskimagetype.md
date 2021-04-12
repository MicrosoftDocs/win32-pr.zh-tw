---
title: 'IVMVirtualPC GetFloppyDiskImageType 方法 (VPCCOMInterfaces .h) '
description: 抓取現有磁片影像檔的類型。
ms.assetid: 34956a0c-1da0-4968-9a6c-c114d7037da1
keywords:
- GetFloppyDiskImageType 方法 Virtual PC
- GetFloppyDiskImageType 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，GetFloppyDiskImageType 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetFloppyDiskImageType
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e5e2974f80865f8572f1153721cf10233fdb389
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106043"
---
# <a name="ivmvirtualpcgetfloppydiskimagetype-method"></a><span data-ttu-id="ca42f-106">IVMVirtualPC：： GetFloppyDiskImageType 方法</span><span class="sxs-lookup"><span data-stu-id="ca42f-106">IVMVirtualPC::GetFloppyDiskImageType method</span></span>

<span data-ttu-id="ca42f-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ca42f-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ca42f-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ca42f-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ca42f-109">抓取現有磁片影像檔的類型。</span><span class="sxs-lookup"><span data-stu-id="ca42f-109">Retrieves the type of an existing floppy disk image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca42f-110">語法</span><span class="sxs-lookup"><span data-stu-id="ca42f-110">Syntax</span></span>


```C++
HRESULT GetFloppyDiskImageType(
  [in]          BSTR                  imagePath,
  [out, retval] VMFloppyDiskImageType *imageType
);
```



## <a name="parameters"></a><span data-ttu-id="ca42f-111">參數</span><span class="sxs-lookup"><span data-stu-id="ca42f-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca42f-112">*imagePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ca42f-112">*imagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ca42f-113">磁片影像檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="ca42f-113">The full path to the disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="ca42f-114">*imageType* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="ca42f-114">*imageType* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="ca42f-115">磁片映射類型。</span><span class="sxs-lookup"><span data-stu-id="ca42f-115">The disk image type.</span></span> <span data-ttu-id="ca42f-116">如需值的清單，請參閱 [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md)。</span><span class="sxs-lookup"><span data-stu-id="ca42f-116">For a list of values, see [**VMFloppyDiskImageType**](vmfloppydiskimagetype.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca42f-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ca42f-117">Return value</span></span>

<span data-ttu-id="ca42f-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ca42f-118">This method can return one of these values.</span></span>



| <span data-ttu-id="ca42f-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="ca42f-119">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="ca42f-120">Description</span><span class="sxs-lookup"><span data-stu-id="ca42f-120">Description</span></span>                                                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ca42f-121"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ca42f-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="ca42f-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ca42f-122">The operation was successful.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="ca42f-123"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="ca42f-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="ca42f-124">*ImagePath* 或 *ImageType* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="ca42f-124">The *imagePath* or *imageType* parameter is **NULL**.</span></span><br/>                                                                 |
| <dl> <span data-ttu-id="ca42f-125"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="ca42f-125"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="ca42f-126">系統找不到 *imagePath* 參數所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="ca42f-126">The system cannot find the file specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="ca42f-127"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="ca42f-127"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="ca42f-128">系統找不到 *imagePath* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="ca42f-128">The system cannot find the path specified by the *imagePath* parameter.</span></span><br/>                                               |
| <dl> <span data-ttu-id="ca42f-129"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="ca42f-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="ca42f-130">*ImagePath* 參數包含不正確字元 (" \* ？： <>/ \| " ") 之一。</span><span class="sxs-lookup"><span data-stu-id="ca42f-130">The *imagePath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                  |
| <dl> <span data-ttu-id="ca42f-131"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="ca42f-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="ca42f-132">*ImagePath* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="ca42f-132">The *imagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="ca42f-133">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="ca42f-133">An absolute path is required.</span></span><br/>                          |
| <dl> <span data-ttu-id="ca42f-134"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="ca42f-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="ca42f-135">*ImagePath* 參數所指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="ca42f-135">The path specified by the *imagePath* parameter is too long.</span></span> <span data-ttu-id="ca42f-136">路徑長度必須少於260個字元。</span><span class="sxs-lookup"><span data-stu-id="ca42f-136">The length of the path must be less than 260 characters.</span></span><br/> |
| <dl> <span data-ttu-id="ca42f-137"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ca42f-137"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="ca42f-138">*ImagePath* 所指定的檔案不是軟碟影像，或發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ca42f-138">The file specified by *imagePath* is not a floppy image, or an unexpected error has occurred.</span></span><br/>                         |
| <dl> <span data-ttu-id="ca42f-139"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="ca42f-139"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="ca42f-140">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="ca42f-140">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                  |



 

## <a name="requirements"></a><span data-ttu-id="ca42f-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca42f-141">Requirements</span></span>



| <span data-ttu-id="ca42f-142">需求</span><span class="sxs-lookup"><span data-stu-id="ca42f-142">Requirement</span></span> | <span data-ttu-id="ca42f-143">值</span><span class="sxs-lookup"><span data-stu-id="ca42f-143">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca42f-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ca42f-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ca42f-145">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ca42f-145">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ca42f-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ca42f-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ca42f-147">都不支援</span><span class="sxs-lookup"><span data-stu-id="ca42f-147">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ca42f-148">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ca42f-148">End of client support</span></span><br/>    | <span data-ttu-id="ca42f-149">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ca42f-149">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ca42f-150">產品</span><span class="sxs-lookup"><span data-stu-id="ca42f-150">Product</span></span><br/>                  | <span data-ttu-id="ca42f-151">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ca42f-151">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ca42f-152">標頭</span><span class="sxs-lookup"><span data-stu-id="ca42f-152">Header</span></span><br/>                   | <dl> <span data-ttu-id="ca42f-153"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ca42f-153"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ca42f-154">IID</span><span class="sxs-lookup"><span data-stu-id="ca42f-154">IID</span></span><br/>                      | <span data-ttu-id="ca42f-155">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="ca42f-155">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="ca42f-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca42f-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca42f-157">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="ca42f-157">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

