---
title: 'IVMVirtualPC CreateVirtualMachine 方法 (VPCCOMInterfaces .h) '
description: 建立新的虛擬機器設定，並捕獲虛擬機器物件。
ms.assetid: 35f7364f-debd-4b9c-8240-23c0512eb004
keywords:
- CreateVirtualMachine 方法 Virtual PC
- CreateVirtualMachine 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，CreateVirtualMachine 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.CreateVirtualMachine
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 494d5166271e6c4086b8dfee12deb61e32ae8a18
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466265"
---
# <a name="ivmvirtualpccreatevirtualmachine-method"></a><span data-ttu-id="7941e-106">IVMVirtualPC：： CreateVirtualMachine 方法</span><span class="sxs-lookup"><span data-stu-id="7941e-106">IVMVirtualPC::CreateVirtualMachine method</span></span>

<span data-ttu-id="7941e-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="7941e-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="7941e-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="7941e-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="7941e-109">建立新的虛擬機器設定，並捕獲虛擬機器物件。</span><span class="sxs-lookup"><span data-stu-id="7941e-109">Creates a new virtual machine configuration and retrieves the virtual machine object.</span></span>

## <a name="syntax"></a><span data-ttu-id="7941e-110">語法</span><span class="sxs-lookup"><span data-stu-id="7941e-110">Syntax</span></span>


```C++
HRESULT CreateVirtualMachine(
  [in]          BSTR              configurationName,
  [in]          BSTR              configurationPath,
  [out, retval] IVMVirtualMachine **virtualMachine
);
```



## <a name="parameters"></a><span data-ttu-id="7941e-111">參數</span><span class="sxs-lookup"><span data-stu-id="7941e-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7941e-112">*configurationName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7941e-112">*configurationName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7941e-113">要建立之虛擬機器的名稱。</span><span class="sxs-lookup"><span data-stu-id="7941e-113">The name of the virtual machine to be created.</span></span> <span data-ttu-id="7941e-114">名稱的長度不能超過80個字元，且 .VMC 和 >.VMCX 檔案的名稱和路徑的加總長度不能超過 **最大 \_ 路徑** (260) 個字元。</span><span class="sxs-lookup"><span data-stu-id="7941e-114">The length of the name cannot exceed 80 characters and the combined length of the name and path to VMC and VMCX files cannot exceed **MAX\_PATH** (260) characters.</span></span> <span data-ttu-id="7941e-115">建立設定檔時，會將副檔名 .vmc 和. >.vmcx 附加至虛擬機器名稱的結尾。</span><span class="sxs-lookup"><span data-stu-id="7941e-115">The file name extensions .vmc and .vmcx will be appended to the end of the virtual machine name when the configuration files are created.</span></span> <span data-ttu-id="7941e-116">如果此參數為 **Null** 或空字串，則 *configurationPath* 參數必須指定 .vmc 檔案的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="7941e-116">If this parameter is **NULL** or an empty string, the *configurationPath* parameter must specify the full path to the VMC file.</span></span>

</dd> <dt>

<span data-ttu-id="7941e-117">*configurationPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7941e-117">*configurationPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7941e-118">將包含 .VMC 檔案的資料夾路徑。</span><span class="sxs-lookup"><span data-stu-id="7941e-118">The path to the folder that will contain the VMC file.</span></span> <span data-ttu-id="7941e-119">如果這個資料夾不存在，就會建立此資料夾。</span><span class="sxs-lookup"><span data-stu-id="7941e-119">This folder will be created if it does not exist.</span></span> <span data-ttu-id="7941e-120">如果 *configurationName* 為 **Null** 或空字串，則必須指定新設定檔的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="7941e-120">If *configurationName* is **NULL** or an empty string, this must specify the full path of the new configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="7941e-121">*virtualMachine* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="7941e-121">*virtualMachine* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="7941e-122">代表此虛擬機器的新 [**IVMVirtualMachine**](ivmvirtualmachine.md) 物件指標。</span><span class="sxs-lookup"><span data-stu-id="7941e-122">A pointer to a new [**IVMVirtualMachine**](ivmvirtualmachine.md) object that represents this virtual machine.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7941e-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="7941e-123">Return value</span></span>

<span data-ttu-id="7941e-124">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7941e-124">This method can return one of these values.</span></span>



| <span data-ttu-id="7941e-125">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="7941e-125">Return code/value</span></span>                                                                                                                                                                            | <span data-ttu-id="7941e-126">Description</span><span class="sxs-lookup"><span data-stu-id="7941e-126">Description</span></span>                                                                                                                                                                                                    |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7941e-127"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-127"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                                  | <span data-ttu-id="7941e-128">作業成功。</span><span class="sxs-lookup"><span data-stu-id="7941e-128">The operation was successful.</span></span><br/>                                                                                                                                                                       |
| <dl> <span data-ttu-id="7941e-129"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-129"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                    | <span data-ttu-id="7941e-130">*ConfigurationName* 或 *configurationPath* 參數無效，或 *virtualMachine* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7941e-130">The *configurationName* or *configurationPath* parameter is not valid, or the *virtualMachine* parameter is **NULL**.</span></span><br/>                                                                               |
| <dl> <span data-ttu-id="7941e-131"><dt>**HRESULT \_從 \_ WIN32 (\_ \_ \_ 找不到錯誤路徑)**</dt> <dt>0x80070003</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-131"><dt>**HRESULT\_FROM\_WIN32(ERROR\_PATH\_NOT\_FOUND)**</dt> <dt>0x80070003</dt></span></span> </dl> | <span data-ttu-id="7941e-132">系統找不到 *configurationPath* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="7941e-132">The system cannot find the path specified by the *configurationPath* parameter.</span></span><br/>                                                                                                                     |
| <dl> <span data-ttu-id="7941e-133"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ \_ 名稱無效)**</dt> <dt>0x8007007b</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-133"><dt>**HRESULT\_FROM\_WIN32(ERROR\_INVALID\_NAME)**</dt> <dt>0x8007007b</dt></span></span> </dl>    | <span data-ttu-id="7941e-134">*ConfigurationPath* 參數包含不正確字元 (" \* ？： <>/ \| " ") 之一。</span><span class="sxs-lookup"><span data-stu-id="7941e-134">The *configurationPath* parameter contains an invalid character (one of "\*?:<>/\|"").</span></span><br/>                                                                                                        |
| <dl> <span data-ttu-id="7941e-135"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 的 \_ 路徑名稱錯誤)**</dt> <dt>0x800700a1</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-135"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BAD\_PATHNAME)**</dt> <dt>0x800700a1</dt></span></span> </dl>    | <span data-ttu-id="7941e-136">*ConfigurationPath* 參數會指定空的或相對路徑。</span><span class="sxs-lookup"><span data-stu-id="7941e-136">The *configurationPath* parameter specifies an empty or relative path.</span></span> <span data-ttu-id="7941e-137">需要絕對路徑。</span><span class="sxs-lookup"><span data-stu-id="7941e-137">An absolute path is required.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="7941e-138"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 緩衝區 \_ 溢出)**</dt> <dt>0x8007006f</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-138"><dt>**HRESULT\_FROM\_WIN32(ERROR\_BUFFER\_OVERFLOW)**</dt> <dt>0x8007006f</dt></span></span> </dl> | <span data-ttu-id="7941e-139">*ConfigurationName* 和 *configurationPath* 參數所指定的路徑會導致路徑太長。</span><span class="sxs-lookup"><span data-stu-id="7941e-139">The path specified by the *configurationName* and *configurationPath* parameters results in a path that is too long.</span></span> <span data-ttu-id="7941e-140">路徑的總長度必須小於 **最大 \_ 路徑** (260) 個字元。</span><span class="sxs-lookup"><span data-stu-id="7941e-140">The total length of the path must be less than **MAX\_PATH** (260) characters.</span></span><br/> |
| <dl> <span data-ttu-id="7941e-141"><dt>**HRESULT \_從 \_ WIN32 (錯誤 \_ 已 \_ 存在)**</dt> <dt>0x800700b7</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-141"><dt>**HRESULT\_FROM\_WIN32(ERROR\_ALREADY\_EXISTS)**</dt> <dt>0x800700b7</dt></span></span> </dl>  | <span data-ttu-id="7941e-142">此位置已有同名的設定檔。</span><span class="sxs-lookup"><span data-stu-id="7941e-142">A configuration file with this name already exists at this location.</span></span><br/>                                                                                                                                |
| <dl> <span data-ttu-id="7941e-143"><dt>**VM \_E \_ 設定 \_ 沒有 \_ 名稱**</dt> <dt>0xA0040400</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-143"><dt>**VM\_E\_CONFIG\_NO\_NAME**</dt> <dt>0xA0040400</dt></span></span> </dl>                       | <span data-ttu-id="7941e-144">*ConfigurationName* 參數是空的。</span><span class="sxs-lookup"><span data-stu-id="7941e-144">The *configurationName* parameter is empty.</span></span><br/>                                                                                                                                                         |
| <dl> <span data-ttu-id="7941e-145"><dt>**VM \_E \_ CONFIG \_ NAME \_ 太 \_ 長**</dt> <dt>0xA0040401</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-145"><dt>**VM\_E\_CONFIG\_NAME\_TOO\_LONG**</dt> <dt>0xA0040401</dt></span></span> </dl>                | <span data-ttu-id="7941e-146">*ConfigurationName* 參數的長度超過80個字元。</span><span class="sxs-lookup"><span data-stu-id="7941e-146">The *configurationName* parameter exceeds 80 characters in length.</span></span><br/>                                                                                                                                  |
| <dl> <span data-ttu-id="7941e-147"><dt>**VM \_E \_ CONFIG \_ NAME \_ 不正確 \_ CHAR**</dt> <dt>0xA0040402</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-147"><dt>**VM\_E\_CONFIG\_NAME\_INVALID\_CHAR**</dt> <dt>0xA0040402</dt></span></span> </dl>            | <span data-ttu-id="7941e-148">*ConfigurationName* 參數包含不正確字元 (" \* ？： <>/ \| \\ " ") 之一。</span><span class="sxs-lookup"><span data-stu-id="7941e-148">The *configurationName* parameter contains an invalid character (one of "\*?:<>/\|\\"").</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="7941e-149"><dt>**VM \_E \_ 設定 \_ 重複 \_ 名稱**</dt> <dt>0xA0040403</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-149"><dt>**VM\_E\_CONFIG\_DUPLICATE\_NAME**</dt> <dt>0xA0040403</dt></span></span> </dl>                | <span data-ttu-id="7941e-150">已經有虛擬機器使用此名稱。</span><span class="sxs-lookup"><span data-stu-id="7941e-150">There is already a virtual machine with this name.</span></span><br/>                                                                                                                                                  |
| <dl> <span data-ttu-id="7941e-151"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-151"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl>     | <span data-ttu-id="7941e-152">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="7941e-152">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/>                                                                                                                |
| <dl> <span data-ttu-id="7941e-153"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-153"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                            | <span data-ttu-id="7941e-154">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="7941e-154">An unexpected error has occurred.</span></span><br/>                                                                                                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="7941e-155">備註</span><span class="sxs-lookup"><span data-stu-id="7941e-155">Remarks</span></span>

<span data-ttu-id="7941e-156">虛擬機器名稱不區分大小寫，例如 "MyVM" 和 "MyVM" 指的是相同的虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="7941e-156">Virtual machine names are case-insensitive, for example, "MyVM" and "myvm" refer to the same virtual machine.</span></span>

## <a name="requirements"></a><span data-ttu-id="7941e-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="7941e-157">Requirements</span></span>



| <span data-ttu-id="7941e-158">需求</span><span class="sxs-lookup"><span data-stu-id="7941e-158">Requirement</span></span> | <span data-ttu-id="7941e-159">值</span><span class="sxs-lookup"><span data-stu-id="7941e-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="7941e-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7941e-160">Minimum supported client</span></span><br/> | <span data-ttu-id="7941e-161">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7941e-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7941e-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7941e-162">Minimum supported server</span></span><br/> | <span data-ttu-id="7941e-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="7941e-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="7941e-164">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="7941e-164">End of client support</span></span><br/>    | <span data-ttu-id="7941e-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="7941e-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="7941e-166">產品</span><span class="sxs-lookup"><span data-stu-id="7941e-166">Product</span></span><br/>                  | <span data-ttu-id="7941e-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="7941e-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="7941e-168">標頭</span><span class="sxs-lookup"><span data-stu-id="7941e-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="7941e-169"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="7941e-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="7941e-170">IID</span><span class="sxs-lookup"><span data-stu-id="7941e-170">IID</span></span><br/>                      | <span data-ttu-id="7941e-171">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="7941e-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="7941e-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7941e-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7941e-173">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="7941e-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

