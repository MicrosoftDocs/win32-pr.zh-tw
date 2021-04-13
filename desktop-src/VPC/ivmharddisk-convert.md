---
title: 'IVMHardDisk Convert 方法 (VPCCOMInterfaces. h) '
description: 將固定大小的虛擬硬碟轉換成動態擴充的虛擬硬碟，或將動態擴充的虛擬硬碟轉換為固定大小的虛擬硬碟。
ms.assetid: 0dee802a-1cac-499e-918a-7dbb6c98415f
keywords:
- 轉換方法 Virtual PC
- Convert 方法 Virtual PC，IVMHardDisk 介面
- IVMHardDisk 介面 Virtual PC，Convert 方法
topic_type:
- apiref
api_name:
- IVMHardDisk.Convert
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2398cf4a2f3b366709c009885bf2c2767828fee1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466700"
---
# <a name="ivmharddiskconvert-method"></a><span data-ttu-id="19cd0-106">IVMHardDisk：： Convert 方法</span><span class="sxs-lookup"><span data-stu-id="19cd0-106">IVMHardDisk::Convert method</span></span>

<span data-ttu-id="19cd0-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="19cd0-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="19cd0-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="19cd0-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="19cd0-109">將固定大小的虛擬硬碟轉換成動態擴充的虛擬硬碟，或將動態擴充的虛擬硬碟轉換為固定大小的虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="19cd0-109">Converts a fixed-size virtual hard disk to a dynamically expanding virtual hard disk or converts a dynamically expanding virtual hard disk to a fixed-size virtual hard disk.</span></span>

## <a name="syntax"></a><span data-ttu-id="19cd0-110">語法</span><span class="sxs-lookup"><span data-stu-id="19cd0-110">Syntax</span></span>


```C++
HRESULT Convert(
  [in]          BSTR           convertedDiskImagePath,
  [in]          VMHardDiskType convertedDiskImageType,
  [out, retval] IVMTask        **convertTask
);
```



## <a name="parameters"></a><span data-ttu-id="19cd0-111">參數</span><span class="sxs-lookup"><span data-stu-id="19cd0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19cd0-112">*convertedDiskImagePath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19cd0-112">*convertedDiskImagePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cd0-113">目標磁片影像檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="19cd0-113">The path to the target disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="19cd0-114">*convertedDiskImageType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19cd0-114">*convertedDiskImageType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19cd0-115">目標磁片映射的類型。</span><span class="sxs-lookup"><span data-stu-id="19cd0-115">The type of the target disk image.</span></span> <span data-ttu-id="19cd0-116">如需值的清單，請參閱 [**VMHardDiskType**](vmharddisktype.md)。</span><span class="sxs-lookup"><span data-stu-id="19cd0-116">For a list of values, see [**VMHardDiskType**](vmharddisktype.md).</span></span>

</dd> <dt>

<span data-ttu-id="19cd0-117">*convertTask* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="19cd0-117">*convertTask* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="19cd0-118">[**IVMTask**](ivmtask.md)物件，用來追蹤轉換完成的轉換程式。</span><span class="sxs-lookup"><span data-stu-id="19cd0-118">An [**IVMTask**](ivmtask.md) object that is used to track the completion of the conversion process.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19cd0-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="19cd0-119">Return value</span></span>

<span data-ttu-id="19cd0-120">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="19cd0-120">This method can return one of these values.</span></span>



| <span data-ttu-id="19cd0-121">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="19cd0-121">Return code/value</span></span>                                                                                                                                                                              | <span data-ttu-id="19cd0-122">Description</span><span class="sxs-lookup"><span data-stu-id="19cd0-122">Description</span></span>                                                                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="19cd0-123"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                    | <span data-ttu-id="19cd0-124">作業成功。</span><span class="sxs-lookup"><span data-stu-id="19cd0-124">The operation was successful.</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="19cd0-125"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                                   | <span data-ttu-id="19cd0-126">*ConvertedDiskImagePath* 參數是空的，或在檔案名上缺少 .vhd 副檔名。</span><span class="sxs-lookup"><span data-stu-id="19cd0-126">The *convertedDiskImagePath* parameter is empty or missing the .vhd extension on the file name.</span></span><br/>                                      |
| <dl> <span data-ttu-id="19cd0-127"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-127"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                      | <span data-ttu-id="19cd0-128">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="19cd0-128">A parameter is **NULL**.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="19cd0-129"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-129"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl>   | <span data-ttu-id="19cd0-130">系統找不到 *convertedDiskImagePath* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="19cd0-130">The system cannot find the path specified by the *convertedDiskImagePath* parameter.</span></span><br/>                                                 |
| <dl> <span data-ttu-id="19cd0-131"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>      | <span data-ttu-id="19cd0-132">*ConvertedDiskImagePath* 參數包含不正確字元 (" \* ？ <>/ \| "： ") 之一。</span><span class="sxs-lookup"><span data-stu-id="19cd0-132">The *convertedDiskImagePath* parameter contains an invalid character (one of "\*?<>/\|":").</span></span><br/>                                    |
| <dl> <span data-ttu-id="19cd0-133"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>      | <span data-ttu-id="19cd0-134">*ConvertedDiskImagePath* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="19cd0-134">The *convertedDiskImagePath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="19cd0-135">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="19cd0-135">An absolute path is required.</span></span><br/>                            |
| <dl> <span data-ttu-id="19cd0-136"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl>   | <span data-ttu-id="19cd0-137">*ConvertedDiskImagePath* 參數所指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="19cd0-137">The path specified by the *convertedDiskImagePath* parameter is too long.</span></span> <span data-ttu-id="19cd0-138">路徑必須小於 **最大 \_ 路徑** (260) 個字元。</span><span class="sxs-lookup"><span data-stu-id="19cd0-138">The path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="19cd0-139"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 共用 \_ 違規)**</dt> <dt>0x80070020</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_SHARING\_VIOLATION)**</dt> <dt>0x80070020</dt></span></span> </dl> | <span data-ttu-id="19cd0-140">此物件參考的虛擬硬碟正在使用中，或此虛擬硬碟的父系正在使用中。</span><span class="sxs-lookup"><span data-stu-id="19cd0-140">Either the virtual hard disk referenced by this object is in use or the parent of this virtual hard disk is in use.</span></span><br/>                  |
| <dl> <span data-ttu-id="19cd0-141"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 磁片已 \_ 滿)**</dt> <dt>0x80070070</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_DISK\_FULL)**</dt> <dt>0x80070070</dt></span></span> </dl>         | <span data-ttu-id="19cd0-142">主機磁片區的空間不足，無法轉換此虛擬硬碟。</span><span class="sxs-lookup"><span data-stu-id="19cd0-142">The host volume does not have enough space to convert this virtual hard disk.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="19cd0-143"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-143"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>    | <span data-ttu-id="19cd0-144">*ConvertedDiskImagePath* 參數所參考的檔案已經存在。</span><span class="sxs-lookup"><span data-stu-id="19cd0-144">The file referenced by the *convertedDiskImagePath* parameter already exists.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="19cd0-145"><dt>**VM \_E \_ 錯誤的 \_ HD \_ 映射 \_ 類型**</dt> <dt>0xA004067B</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-145"><dt>**VM\_E\_WRONG\_HD\_IMAGE\_TYPE**</dt> <dt>0xA004067B</dt></span></span> </dl>                   | <span data-ttu-id="19cd0-146">*ConvertedDiskImagePath* 參數必須是 **VmDiskType \_ Dynamic** 或 **vmDiskType \_ FixedSize**。</span><span class="sxs-lookup"><span data-stu-id="19cd0-146">The *convertedDiskImagePath* parameter must be either **vmDiskType\_Dynamic** or **vmDiskType\_FixedSize**.</span></span><br/>                          |
| <dl> <span data-ttu-id="19cd0-147"><dt>**VM \_E \_ 不正確 \_ HD \_ FILE**</dt> <dt>0xA0040682</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-147"><dt>**VM\_E\_INVALID\_HD\_FILE**</dt> <dt>0xA0040682</dt></span></span> </dl>                        | <span data-ttu-id="19cd0-148">這個 [**IVMHardDisk**](ivmharddisk.md) 物件參考的虛擬硬碟映射似乎不是有效的映射。</span><span class="sxs-lookup"><span data-stu-id="19cd0-148">The virtual hard disk image referenced by this [**IVMHardDisk**](ivmharddisk.md) object does not seem to be a valid image.</span></span><br/>          |
| <dl> <span data-ttu-id="19cd0-149"><dt>**VM \_E \_ \_ \_ \_ 找不到父路徑**</dt> <dt>0xA0040677</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-149"><dt>**VM\_E\_PARENT\_PATH\_NOT\_FOUND**</dt> <dt>0xA0040677</dt></span></span> </dl>                 | <span data-ttu-id="19cd0-150">此物件參考的虛擬硬碟父系不存在。</span><span class="sxs-lookup"><span data-stu-id="19cd0-150">The parent of the virtual hard disk referenced by this object does not exist.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="19cd0-151"><dt>**VM \_E \_ 應用 \_ 程式 \_ 關閉**</dt> <dt>0xA0040209</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-151"><dt>**VM\_E\_APP\_SHUTTING\_DOWN**</dt> <dt>0xA0040209</dt></span></span> </dl>                      | <span data-ttu-id="19cd0-152">無法轉換虛擬硬碟映射，因為應用程式正在關閉。</span><span class="sxs-lookup"><span data-stu-id="19cd0-152">The virtual hard disk image cannot be converted because the application is shutting down.</span></span><br/>                                            |
| <dl> <span data-ttu-id="19cd0-153"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                              | <span data-ttu-id="19cd0-154">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="19cd0-154">An unexpected error has occurred.</span></span><br/>                                                                                                    |



 

## <a name="remarks"></a><span data-ttu-id="19cd0-155">備註</span><span class="sxs-lookup"><span data-stu-id="19cd0-155">Remarks</span></span>

<span data-ttu-id="19cd0-156">在轉換程式之後，來源檔案會保持不變。</span><span class="sxs-lookup"><span data-stu-id="19cd0-156">The source file is left intact after the conversion process.</span></span>

## <a name="requirements"></a><span data-ttu-id="19cd0-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="19cd0-157">Requirements</span></span>



| <span data-ttu-id="19cd0-158">需求</span><span class="sxs-lookup"><span data-stu-id="19cd0-158">Requirement</span></span> | <span data-ttu-id="19cd0-159">值</span><span class="sxs-lookup"><span data-stu-id="19cd0-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="19cd0-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19cd0-160">Minimum supported client</span></span><br/> | <span data-ttu-id="19cd0-161">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19cd0-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="19cd0-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19cd0-162">Minimum supported server</span></span><br/> | <span data-ttu-id="19cd0-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="19cd0-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="19cd0-164">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="19cd0-164">End of client support</span></span><br/>    | <span data-ttu-id="19cd0-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="19cd0-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="19cd0-166">產品</span><span class="sxs-lookup"><span data-stu-id="19cd0-166">Product</span></span><br/>                  | <span data-ttu-id="19cd0-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="19cd0-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="19cd0-168">標頭</span><span class="sxs-lookup"><span data-stu-id="19cd0-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="19cd0-169"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="19cd0-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="19cd0-170">IID</span><span class="sxs-lookup"><span data-stu-id="19cd0-170">IID</span></span><br/>                      | <span data-ttu-id="19cd0-171">IID \_ IVMHardDisk 定義為 ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span><span class="sxs-lookup"><span data-stu-id="19cd0-171">IID\_IVMHardDisk is defined as ffa14ae6-48f5-42a4-8a22-186f2e5c7db0</span></span><br/>                |



## <a name="see-also"></a><span data-ttu-id="19cd0-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19cd0-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="19cd0-173">**IVMHardDisk**</span><span class="sxs-lookup"><span data-stu-id="19cd0-173">**IVMHardDisk**</span></span>](ivmharddisk.md)
</dt> </dl>

 

