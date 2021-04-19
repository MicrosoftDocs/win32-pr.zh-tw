---
title: 'IVMVirtualPC RegisterVirtualMachine 方法 (VPCCOMInterfaces .h) '
description: 註冊現有的虛擬機器設定，並抓取虛擬機器物件。
ms.assetid: d3b13f1b-7537-4e3f-9bcc-98a6fe855f78
keywords:
- RegisterVirtualMachine 方法 Virtual PC
- RegisterVirtualMachine 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，RegisterVirtualMachine 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.RegisterVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72cc1e27a657eaad70aeec81c0216d1e707fa36b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965520"
---
# <a name="ivmvirtualpcregistervirtualmachine-method"></a><span data-ttu-id="b332c-106">IVMVirtualPC：： RegisterVirtualMachine 方法</span><span class="sxs-lookup"><span data-stu-id="b332c-106">IVMVirtualPC::RegisterVirtualMachine method</span></span>

<span data-ttu-id="b332c-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="b332c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b332c-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="b332c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b332c-109">註冊現有的虛擬機器設定，並抓取虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="b332c-109">Registers an existing virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="b332c-110">語法</span><span class="sxs-lookup"><span data-stu-id="b332c-110">Syntax</span></span>


```C++
HRESULT RegisterVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="b332c-111">參數</span><span class="sxs-lookup"><span data-stu-id="b332c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b332c-112">*configurationName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b332c-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b332c-113">要註冊之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="b332c-113">The name of the virtual machine to be registered.</span></span> <span data-ttu-id="b332c-114">名稱的長度不能超過80個字元，且名稱和路徑的加總長度不能超過 **最大 \_ 路徑** (260) 個字元。</span><span class="sxs-lookup"><span data-stu-id="b332c-114">The length of the name cannot exceed 80 characters and the combined length of the name and path cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="b332c-115">指定的名稱可能包含 .vmc 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="b332c-115">The specified name may contain the .vmc extension.</span></span> <span data-ttu-id="b332c-116">如果此參數為 **Null** 或空字串，則 *configurationPath* 參數必須指定設定檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b332c-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="b332c-117">*configurationPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b332c-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b332c-118">包含現有設定檔案的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="b332c-118">The path to the folder that contains the existing configuration file.</span></span> <span data-ttu-id="b332c-119">如果 *configurationName* 參數為 **Null** 或空字串，則必須指定現有設定檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="b332c-119">If the *configurationName* parameter is **NULL** or an empty string, this must specify the full path to the existing configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="b332c-120">*virtualMachine* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="b332c-120">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="b332c-121">代表此虛擬機器的新 [**IVMVirtualMachine**](ivmvirtualmachine.md) 物件指標。</span><span class="sxs-lookup"><span data-stu-id="b332c-121">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b332c-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="b332c-122">Return value</span></span>

<span data-ttu-id="b332c-123">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b332c-123">This method can return one of these values.</span></span>



| <span data-ttu-id="b332c-124">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="b332c-124">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="b332c-125">Description</span><span class="sxs-lookup"><span data-stu-id="b332c-125">Description</span></span>                                                                                                                                                                                                       |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="b332c-126"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-126"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="b332c-127">作業成功。</span><span class="sxs-lookup"><span data-stu-id="b332c-127">The operation was successful.</span></span><br/>                                                                                                                                                                          |
| <dl> <span data-ttu-id="b332c-128"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-128"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="b332c-129">*ConfigurationName* 或 *configurationPath* 參數無效，或 *virtualMachine* 為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b332c-129">The *configurationName* or *configurationPath* parameter is invalid, or *virtualMachine* is **NULL**.</span></span><br/>                                                                                                  |
| <dl> <span data-ttu-id="b332c-130"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-130"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="b332c-131">系統找不到 *configurationName* 和 *configurationPath* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="b332c-131">The system cannot find the path specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="b332c-132"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤檔案)**</dt> <dt>0x80070002</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-132"><dt>**HRESULT\_FROM\_WIN32(ERROR\_FILE\_NOT\_FOUND)**</dt> <dt>0x80070002</dt></span></span> </dl> | <span data-ttu-id="b332c-133">系統找不到 *configurationName* 和 *configurationPath* 參數所指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="b332c-133">The system cannot find the file specified by the *configurationName* and *configurationPath* parameters.</span></span><br/>                                                                                               |
| <dl> <span data-ttu-id="b332c-134"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-134"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="b332c-135">*ConfigurationPath* 參數包含不正確字元 (" \* ？： <>/ \| " ") 之一。</span><span class="sxs-lookup"><span data-stu-id="b332c-135">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                           |
| <dl> <span data-ttu-id="b332c-136"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-136"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="b332c-137">參數 *configurationPath* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="b332c-137">The parameter *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="b332c-138">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="b332c-138">An absolute path is required.</span></span><br/>                                                                                         |
| <dl> <span data-ttu-id="b332c-139"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-139"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="b332c-140">*ConfigurationName* 和 *configurationPath* 參數所指定的路徑會導致路徑太長。</span><span class="sxs-lookup"><span data-stu-id="b332c-140">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="b332c-141">路徑的加總長度必須小於 **最大 \_ 路徑** (260) 個字元。</span><span class="sxs-lookup"><span data-stu-id="b332c-141">The combined length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="b332c-142"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-142"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="b332c-143">此位置已有同名的設定檔。</span><span class="sxs-lookup"><span data-stu-id="b332c-143">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                   |
| <dl> <span data-ttu-id="b332c-144"><dt>**VM \_E \_ CONFIG \_ NAME \_ 太 \_ 長**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-144"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="b332c-145">*ConfigurationName* 參數的長度超過80個字元。</span><span class="sxs-lookup"><span data-stu-id="b332c-145">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                     |
| <dl> <span data-ttu-id="b332c-146"><dt>**VM \_E \_ CONFIG \_ NAME \_ 不正確 \_ CHAR**</dt> <dt>0xA0040402</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-146"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="b332c-147">*ConfigurationName* 參數包含不正確字元 (" \* ？： <>/ \| \\ " ") 之一。</span><span class="sxs-lookup"><span data-stu-id="b332c-147">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                         |
| <dl> <span data-ttu-id="b332c-148"><dt>**VM \_E \_ 設定 \_ 重複 \_ 名稱**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-148"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="b332c-149">已經有虛擬機器使用此名稱。</span><span class="sxs-lookup"><span data-stu-id="b332c-149">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                     |
| <dl> <span data-ttu-id="b332c-150"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-150"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="b332c-151">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="b332c-151">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                   |
| <dl> <span data-ttu-id="b332c-152"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-152"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="b332c-153">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="b332c-153">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="b332c-154">備註</span><span class="sxs-lookup"><span data-stu-id="b332c-154">Remarks</span></span>

<span data-ttu-id="b332c-155">虛擬機器名稱不區分大小寫，例如 "MyVM" 和 "MyVM" 指的是相同的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="b332c-155">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="b332c-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="b332c-156">Requirements</span></span>



| <span data-ttu-id="b332c-157">需求</span><span class="sxs-lookup"><span data-stu-id="b332c-157">Requirement</span></span> | <span data-ttu-id="b332c-158">值</span><span class="sxs-lookup"><span data-stu-id="b332c-158">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b332c-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b332c-159">Minimum supported client</span></span><br/> | <span data-ttu-id="b332c-160">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b332c-160">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b332c-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b332c-161">Minimum supported server</span></span><br/> | <span data-ttu-id="b332c-162">都不支援</span><span class="sxs-lookup"><span data-stu-id="b332c-162">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b332c-163">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="b332c-163">End of client support</span></span><br/>    | <span data-ttu-id="b332c-164">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b332c-164">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b332c-165">產品</span><span class="sxs-lookup"><span data-stu-id="b332c-165">Product</span></span><br/>                  | <span data-ttu-id="b332c-166">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b332c-166">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b332c-167">標頭</span><span class="sxs-lookup"><span data-stu-id="b332c-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="b332c-168"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="b332c-168"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="b332c-169">IID</span><span class="sxs-lookup"><span data-stu-id="b332c-169">IID</span></span><br/>                      | <span data-ttu-id="b332c-170">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="b332c-170">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="b332c-171">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b332c-171">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b332c-172">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="b332c-172">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

