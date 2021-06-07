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
ms.openlocfilehash: 09f6370dfb868ec386e05f361240a74412f13a7d
ms.sourcegitcommit: cb87082135319cbdc5df541e3071eebb83a58972
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/04/2021
ms.locfileid: "111387634"
---
# <a name="ivmvirtualpcdefaultvmconfigurationpath-property"></a><span data-ttu-id="bffe5-106">IVMVirtualPC：:D efaultVMConfigurationPath 屬性</span><span class="sxs-lookup"><span data-stu-id="bffe5-106">IVMVirtualPC::DefaultVMConfigurationPath property</span></span>

<span data-ttu-id="bffe5-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="bffe5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="bffe5-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="bffe5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="bffe5-109">抓取並設定要搜尋可用虛擬機器組態檔案的預設目錄。</span><span class="sxs-lookup"><span data-stu-id="bffe5-109">Retrieves and sets the default directory to be searched for available virtual machine configuration files.</span></span>

<span data-ttu-id="bffe5-110">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bffe5-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bffe5-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="bffe5-111">Syntax</span></span>


```C++
HRESULT put_DefaultVMConfigurationPath(
  [in]          BSTR configurationPath
);

HRESULT get_DefaultVMConfigurationPath(
  [out, retval] BSTR *configurationPath
);
```



## <a name="property-value"></a><span data-ttu-id="bffe5-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="bffe5-112">Property value</span></span>

<span data-ttu-id="bffe5-113">指定預設虛擬機器組態檔的目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="bffe5-113">Specifies the directory path for the default virtual machine configuration files.</span></span> <span data-ttu-id="bffe5-114">在路徑字串中，反斜線 (\\) 可能會緊接在終止的 null 字元之前出現。</span><span class="sxs-lookup"><span data-stu-id="bffe5-114">In the path string, a backslash (\\) may appear immediately before the terminating null character.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bffe5-115">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bffe5-115">Error codes</span></span>



| <span data-ttu-id="bffe5-116">名稱/值</span><span class="sxs-lookup"><span data-stu-id="bffe5-116">Name/value</span></span>                                                                                                                                                                               | <span data-ttu-id="bffe5-117">意義</span><span class="sxs-lookup"><span data-stu-id="bffe5-117">Meaning</span></span>                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bffe5-118"><dt>S \_確定</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="bffe5-118"><dt>S\_OK</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="bffe5-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="bffe5-119">The operation was successful.</span></span><br/>                                                                                                                 |
| <dl> <span data-ttu-id="bffe5-120"><dt>E \_指標</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="bffe5-120"><dt>E\_POINTER</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="bffe5-121">*ConfigurationPath* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="bffe5-121">The *configurationPath* parameter is **NULL**.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="bffe5-122"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案) </dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="bffe5-122"><dt>HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="bffe5-123">系統找不到 *configurationPath* 參數所指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="bffe5-123">The system cannot find the directory specified by the *configurationPath* parameter.</span></span><br/>                                                          |
| <dl> <span data-ttu-id="bffe5-124"><dt>HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑) </dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="bffe5-124"><dt>HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="bffe5-125">系統找不到 *configurationPath* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="bffe5-125">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                               |
| <dl> <span data-ttu-id="bffe5-126"><dt>HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效) </dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="bffe5-126"><dt>HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="bffe5-127">*ConfigurationPath* 參數包含不正確字元 (下列其中一項： " \* ？ <>/ \| "： ") 。</span><span class="sxs-lookup"><span data-stu-id="bffe5-127">The *configurationPath* parameter contains an invalid character (one of the following: "\*?<>/\|":").</span></span><br/>                                   |
| <dl> <span data-ttu-id="bffe5-128"><dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤) </dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="bffe5-128"><dt>HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="bffe5-129">*ConfigurationPath* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="bffe5-129">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="bffe5-130">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="bffe5-130">An absolute path is required.</span></span><br/>                                          |
| <dl> <span data-ttu-id="bffe5-131"><dt>HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出) </dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="bffe5-131"><dt>HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="bffe5-132">*ConfigurationPath* 參數所指定的路徑太長。</span><span class="sxs-lookup"><span data-stu-id="bffe5-132">The path specified by the *configurationPath* parameter is too long.</span></span> <span data-ttu-id="bffe5-133">路徑的長度必須小於 **最大 \_ 路徑** (260) 個字元。</span><span class="sxs-lookup"><span data-stu-id="bffe5-133">The length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="bffe5-134"><dt>會 \_E \_ 例外</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="bffe5-134"><dt>DISP\_E\_EXCEPTION</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="bffe5-135">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="bffe5-135">An unexpected error has occurred.</span></span><br/>                                                                                                             |
| <dl> <span data-ttu-id="bffe5-136"><dt>VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="bffe5-136"><dt>VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="bffe5-137">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="bffe5-137">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                          |



## <a name="remarks"></a><span data-ttu-id="bffe5-138">備註</span><span class="sxs-lookup"><span data-stu-id="bffe5-138">Remarks</span></span>

<span data-ttu-id="bffe5-139">根據預設，這個屬性值會設定為下列目錄： "% LocalAppData% \\ Microsoft \\ WINDOWS Virtual PC \\ 虛擬機器 \\ "。</span><span class="sxs-lookup"><span data-stu-id="bffe5-139">By default, this property value is set to the following directory: "%LocalAppData%\\Microsoft\\Windows Virtual PC\\Virtual Machines\\".</span></span>

## <a name="requirements"></a><span data-ttu-id="bffe5-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="bffe5-140">Requirements</span></span>



| <span data-ttu-id="bffe5-141">需求</span><span class="sxs-lookup"><span data-stu-id="bffe5-141">Requirement</span></span> | <span data-ttu-id="bffe5-142">值</span><span class="sxs-lookup"><span data-stu-id="bffe5-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bffe5-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bffe5-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bffe5-144">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bffe5-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bffe5-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bffe5-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bffe5-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="bffe5-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="bffe5-147">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="bffe5-147">End of client support</span></span><br/>    | <span data-ttu-id="bffe5-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="bffe5-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="bffe5-149">產品</span><span class="sxs-lookup"><span data-stu-id="bffe5-149">Product</span></span><br/>                  | <span data-ttu-id="bffe5-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="bffe5-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="bffe5-151">標頭</span><span class="sxs-lookup"><span data-stu-id="bffe5-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="bffe5-152"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="bffe5-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="bffe5-153">IID</span><span class="sxs-lookup"><span data-stu-id="bffe5-153">IID</span></span><br/>                      | <span data-ttu-id="bffe5-154">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="bffe5-154">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="bffe5-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bffe5-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bffe5-156">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="bffe5-156">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

