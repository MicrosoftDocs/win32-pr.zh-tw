---
title: 'IVMVirtualPC SearchPaths 屬性 (VPCCOMInterfaces .h) '
description: 用來尋找與 Windows Virtual PC 相關聯之檔案的檔案系統路徑。
ms.assetid: 2a2deee5-7e6b-4b90-8ce9-0b0dbeef0f30
keywords:
- SearchPaths 屬性 Virtual PC
- SearchPaths 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，SearchPaths 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.SearchPaths
- IVMVirtualPC.get_SearchPaths
- IVMVirtualPC.put_SearchPaths
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 287eb07bc9205f9b6f0851bd8809f9a49dcf3242
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685469"
---
# <a name="ivmvirtualpcsearchpaths-property"></a><span data-ttu-id="8899e-106">IVMVirtualPC：： SearchPaths 屬性</span><span class="sxs-lookup"><span data-stu-id="8899e-106">IVMVirtualPC::SearchPaths property</span></span>

<span data-ttu-id="8899e-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="8899e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="8899e-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="8899e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="8899e-109">抓取並設定用來尋找與 Windows Virtual PC 相關聯之檔案的檔案系統路徑。</span><span class="sxs-lookup"><span data-stu-id="8899e-109">Retrieves and sets the file system paths that are used to find files associated with Windows Virtual PC.</span></span>

<span data-ttu-id="8899e-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="8899e-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8899e-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="8899e-111">Syntax</span></span>


```C++
HRESULT put_SearchPaths(
  [in]          VARIANT searchPaths
);

HRESULT get_SearchPaths(
  [out, retval] VARIANT *searchPaths
);
```



## <a name="property-value"></a><span data-ttu-id="8899e-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="8899e-112">Property value</span></span>

<span data-ttu-id="8899e-113">指定包含每個專案之檔案系統路徑的 safearray。</span><span class="sxs-lookup"><span data-stu-id="8899e-113">Specifies a safearray containing a file system path for each entry.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8899e-114">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8899e-114">Error codes</span></span>



| <span data-ttu-id="8899e-115">名稱/值</span><span class="sxs-lookup"><span data-stu-id="8899e-115">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="8899e-116">意義</span><span class="sxs-lookup"><span data-stu-id="8899e-116">Meaning</span></span>                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="8899e-117"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-117"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="8899e-118">作業成功。</span><span class="sxs-lookup"><span data-stu-id="8899e-118">The operation was successful.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8899e-119"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-119"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="8899e-120">參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8899e-120">The parameter is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="8899e-121"><dt>E \_INVALIDARG</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-121"><dt>E\_INVALIDARG</dt> <dt>0x80000003</dt></span></span> </dl>                                 | <span data-ttu-id="8899e-122">*SearchPaths* 參數無效，無法剖析為路徑的陣列。</span><span class="sxs-lookup"><span data-stu-id="8899e-122">The *searchPaths* parameter is not valid and could not be parsed into an array of paths.</span></span><br/>                                    |
| <dl> <span data-ttu-id="8899e-123"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-123"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="8899e-124">系統找不到在 *searchPaths* 參數中指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="8899e-124">The system cannot find a directory specified in the *searchPaths* parameter.</span></span><br/>                                                |
| <dl> <span data-ttu-id="8899e-125"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑) </dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-125"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="8899e-126">系統找不到 *searchPaths* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="8899e-126">The system cannot find a path specified by the *searchPaths* parameter.</span></span><br/>                                                     |
| <dl> <span data-ttu-id="8899e-127"><dt>HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效) </dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-127"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="8899e-128">*SearchPaths* 參數中指定的路徑包含不合法的字元。</span><span class="sxs-lookup"><span data-stu-id="8899e-128">A path specified in the *searchPaths* parameter contains illegal characters.</span></span> <span data-ttu-id="8899e-129">不合法的字元是 " \* ？ <>/ \| "： "。</span><span class="sxs-lookup"><span data-stu-id="8899e-129">The illegal characters are "\*?<>/\|":".</span></span><br/> |
| <dl> <span data-ttu-id="8899e-130"><dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤) </dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-130"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="8899e-131">包含在 *searchPaths* 參數中的路徑會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="8899e-131">A path contained in the *searchPaths* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="8899e-132">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="8899e-132">An absolute path is required.</span></span><br/>          |
| <dl> <span data-ttu-id="8899e-133"><dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出) </dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-133"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="8899e-134">*SearchPaths* 參數中指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="8899e-134">The path specified in the *searchPaths* parameter is too long.</span></span> <span data-ttu-id="8899e-135">路徑長度必須少於260個字元。</span><span class="sxs-lookup"><span data-stu-id="8899e-135">The length of the path must be less than 260 characters.</span></span><br/>     |
| <dl> <span data-ttu-id="8899e-136"><dt>VM \_E \_ PREF \_ \_ 找不到</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-136"><dt>VM\_E\_PREF\_NOT\_FOUND</dt> <dt>0xA0040300</dt></span></span> </dl>                       | <span data-ttu-id="8899e-137">找不到喜好設定。</span><span class="sxs-lookup"><span data-stu-id="8899e-137">The preference was not found.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="8899e-138"><dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-138"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="8899e-139">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="8899e-139">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                        |
| <dl> <span data-ttu-id="8899e-140"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-140"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="8899e-141">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="8899e-141">An unexpected error has occurred.</span></span><br/>                                                                                           |



## <a name="requirements"></a><span data-ttu-id="8899e-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="8899e-142">Requirements</span></span>



| <span data-ttu-id="8899e-143">需求</span><span class="sxs-lookup"><span data-stu-id="8899e-143">Requirement</span></span> | <span data-ttu-id="8899e-144">值</span><span class="sxs-lookup"><span data-stu-id="8899e-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="8899e-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8899e-145">Minimum supported client</span></span><br/> | <span data-ttu-id="8899e-146">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8899e-146">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="8899e-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8899e-147">Minimum supported server</span></span><br/> | <span data-ttu-id="8899e-148">都不支援</span><span class="sxs-lookup"><span data-stu-id="8899e-148">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="8899e-149">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="8899e-149">End of client support</span></span><br/>    | <span data-ttu-id="8899e-150">Windows 7</span><span class="sxs-lookup"><span data-stu-id="8899e-150">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="8899e-151">產品</span><span class="sxs-lookup"><span data-stu-id="8899e-151">Product</span></span><br/>                  | <span data-ttu-id="8899e-152">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="8899e-152">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="8899e-153">標頭</span><span class="sxs-lookup"><span data-stu-id="8899e-153">Header</span></span><br/>                   | <dl> <span data-ttu-id="8899e-154"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="8899e-154"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="8899e-155">IID</span><span class="sxs-lookup"><span data-stu-id="8899e-155">IID</span></span><br/>                      | <span data-ttu-id="8899e-156">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="8899e-156">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="8899e-157">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8899e-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8899e-158">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="8899e-158">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

