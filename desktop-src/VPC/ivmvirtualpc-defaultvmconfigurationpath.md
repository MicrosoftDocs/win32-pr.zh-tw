---
title: 'IVMVirtualPC DefaultVMConfigurationPath 屬性 (VPCCOMInterfaces .h) '
description: 要搜尋可用虛擬機器組態檔案的預設目錄。
ms.assetid: 9ae63198-e3f6-4dcb-8edb-85adfbbdca26
keywords:
- DefaultVMConfigurationPath 屬性 Virtual PC
- DefaultVMConfigurationPath 屬性 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，DefaultVMConfigurationPath 屬性
topic_type:
- apiref
api_name:
- IVMVirtualPC.DefaultVMConfigurationPath
- IVMVirtualPC.get_DefaultVMConfigurationPath
- IVMVirtualPC.put_DefaultVMConfigurationPath
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e13fc2323cb15bdbeb8c42e61810a376e49b3988
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686215"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a><span data-ttu-id="bb6d2-106">IVMVirtualPC：:D efaultVMConfigurationPath 屬性</span><span class="sxs-lookup"><span data-stu-id="bb6d2-106">IVMVirtualPC::DefaultVMConfigurationPath property</span></span>

<span data-ttu-id="bb6d2-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bb6d2-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="bb6d2-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bb6d2-109">抓取並設定要搜尋可用虛擬機器組態檔案的預設目錄。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-109">Retrieves and sets the default directory to be searched for available virtual machine configuration files.</span></span>

<span data-ttu-id="bb6d2-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb6d2-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="bb6d2-111">Syntax</span></span>


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a><span data-ttu-id="bb6d2-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="bb6d2-112">Property value</span></span>

<span data-ttu-id="bb6d2-113">指定預設虛擬機器組態檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-113">Specifies the directory path for the default virtual machine configuration files.</span></span> <span data-ttu-id="bb6d2-114">在路徑字串中，反斜線 (\) 可能會緊接在結尾的 null 字元之前出現。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-114">In the path string, a backslash (\) may appear immediately before the terminating null character.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bb6d2-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bb6d2-115">Error codes</span></span>



| <span data-ttu-id="bb6d2-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="bb6d2-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="bb6d2-117">意義</span><span class="sxs-lookup"><span data-stu-id="bb6d2-117">Meaning</span></span>                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bb6d2-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d2-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="bb6d2-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-119">The operation was successful.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="bb6d2-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d2-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="bb6d2-121">*ConfigurationPath* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-121">The *configurationPath* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="bb6d2-122"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d2-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="bb6d2-123">系統找不到 *configurationPath* 參數所指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-123">The system cannot find the directory specified by the *configurationPath* parameter.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="bb6d2-124"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑) </dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d2-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="bb6d2-125">系統找不到 *configurationPath* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-125">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="bb6d2-126"><dt>HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效) </dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d2-126"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="bb6d2-127">*ConfigurationPath* 參數包含不正確字元 (下列其中一項： " \* ？ <>/ \| "： ") 。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-127">The *configurationPath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                   |
| <dl> <span data-ttu-id="bb6d2-128"><dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤) </dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d2-128"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="bb6d2-129">*ConfigurationPath* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-129">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="bb6d2-130">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-130">An absolute path is required.</span></span><br/>                                          |
| <dl> <span data-ttu-id="bb6d2-131"><dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出) </dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d2-131"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="bb6d2-132">*ConfigurationPath* 參數所指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-132">The path specified by the *configurationPath* parameter is too long.</span></span> <span data-ttu-id="bb6d2-133">路徑的長度必須小於 **最大 \_ 路徑** (260) 個字元。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-133">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="bb6d2-134"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d2-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="bb6d2-135">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-135">An unexpected error has occurred.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="bb6d2-136"><dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d2-136"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="bb6d2-137">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-137">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                          |



## <a name="remarks"></a><span data-ttu-id="bb6d2-138">備註</span><span class="sxs-lookup"><span data-stu-id="bb6d2-138">Remarks</span></span>

<span data-ttu-id="bb6d2-139">根據預設，這個屬性值會設定為下列目錄： "% LocalAppData% \\ Microsoft \\ WINDOWS Virtual PC \\ 虛擬機器 \\ "。</span><span class="sxs-lookup"><span data-stu-id="bb6d2-139">By default, this property value is set to the following directory: "%LocalAppData%\\Microsoft\\Windows Virtual PC\\Virtual Machines\\".</span></span>

## <a name="requirements"></a><span data-ttu-id="bb6d2-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb6d2-140">Requirements</span></span>



| <span data-ttu-id="bb6d2-141">需求</span><span class="sxs-lookup"><span data-stu-id="bb6d2-141">Requirement</span></span> | <span data-ttu-id="bb6d2-142">值</span><span class="sxs-lookup"><span data-stu-id="bb6d2-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb6d2-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb6d2-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bb6d2-144">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb6d2-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bb6d2-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb6d2-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bb6d2-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="bb6d2-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bb6d2-147">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="bb6d2-147">End of client support</span></span><br/>    | <span data-ttu-id="bb6d2-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bb6d2-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bb6d2-149">產品</span><span class="sxs-lookup"><span data-stu-id="bb6d2-149">Product</span></span><br/>                  | <span data-ttu-id="bb6d2-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bb6d2-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bb6d2-151">標頭</span><span class="sxs-lookup"><span data-stu-id="bb6d2-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb6d2-152"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb6d2-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bb6d2-153">IID</span><span class="sxs-lookup"><span data-stu-id="bb6d2-153">IID</span></span><br/>                      | <span data-ttu-id="bb6d2-154">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="bb6d2-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="bb6d2-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb6d2-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb6d2-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="bb6d2-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

