---
title: 'IVMVirtualPC GetVirtualMachineFiles 方法 (VPCCOMInterfaces .h) '
description: 捕獲已知虛擬機器組態檔的陣列。
ms.assetid: 38771573-66fa-408a-95db-1281efdf8b73
keywords:
- GetVirtualMachineFiles 方法 Virtual PC
- GetVirtualMachineFiles 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，GetVirtualMachineFiles 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetVirtualMachineFiles
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c5d1fe248b76756b39846d181341278f669d2f5f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317467"
---
# <a name="ivmvirtualpcgetvirtualmachinefiles-method"></a><span data-ttu-id="57af5-106">IVMVirtualPC：： GetVirtualMachineFiles 方法</span><span class="sxs-lookup"><span data-stu-id="57af5-106">IVMVirtualPC::GetVirtualMachineFiles method</span></span>

<span data-ttu-id="57af5-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="57af5-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="57af5-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="57af5-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="57af5-109">捕獲已知虛擬機器組態檔的陣列。</span><span class="sxs-lookup"><span data-stu-id="57af5-109">Retrieves an array of known virtual machine configuration files.</span></span>

## <a name="syntax"></a><span data-ttu-id="57af5-110">語法</span><span class="sxs-lookup"><span data-stu-id="57af5-110">Syntax</span></span>


```C++
HRESULT GetVirtualMachineFiles(
  [in]          VARIANT      inAdditionalSearchPaths,
  [in]          VARIANT_BOOL inExcludedRegisteredVMs,
  [out, retval] VARIANT      *outVirtualMachineFileList
);
```



## <a name="parameters"></a><span data-ttu-id="57af5-111">參數</span><span class="sxs-lookup"><span data-stu-id="57af5-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57af5-112">*inAdditionalSearchPaths* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57af5-112">*inAdditionalSearchPaths* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57af5-113">將會搜尋這些路徑，以及在 [**IVMVirtualPC：： SearchPaths**](ivmvirtualpc-searchpaths.md) 和 [**IVMVirtualPC：:D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) 屬性中設定的路徑。</span><span class="sxs-lookup"><span data-stu-id="57af5-113">These paths will be searched along with the paths set in the [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) properties.</span></span>

</dd> <dt>

<span data-ttu-id="57af5-114">*inExcludedRegisteredVMs* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57af5-114">*inExcludedRegisteredVMs* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57af5-115">如果已註冊的虛擬機器應該從 *outVirtualMachineFileList* 參數的陣列傳回中排除，**則為 TRUE** ，否則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="57af5-115">**TRUE** if registered virtual machines should be excluded from the array return in the *outVirtualMachineFileList* parameter and **FALSE** otherwise.</span></span>

</dd> <dt>

<span data-ttu-id="57af5-116">*outVirtualMachineFileList* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="57af5-116">*outVirtualMachineFileList* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="57af5-117">在指定搜尋路徑中找到之虛擬機器組態檔案的路徑字串陣列。</span><span class="sxs-lookup"><span data-stu-id="57af5-117">An array of path strings for the virtual machine configuration files found in the specified search paths.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57af5-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="57af5-118">Return value</span></span>

<span data-ttu-id="57af5-119">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="57af5-119">This method can return one of these values.</span></span>



| <span data-ttu-id="57af5-120">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="57af5-120">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="57af5-121">Description</span><span class="sxs-lookup"><span data-stu-id="57af5-121">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="57af5-122"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="57af5-122"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="57af5-123">作業成功。</span><span class="sxs-lookup"><span data-stu-id="57af5-123">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="57af5-124"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="57af5-124"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="57af5-125">*OutVirtualMachineFileList* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="57af5-125">The *outVirtualMachineFileList* parameter is **NULL**.</span></span><br/>                               |
| <dl> <span data-ttu-id="57af5-126"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="57af5-126"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="57af5-127">*InAdditionalSearchPaths* 參數不是字串的陣列。</span><span class="sxs-lookup"><span data-stu-id="57af5-127">The *inAdditionalSearchPaths* parameter is not an array of strings.</span></span><br/>                  |
| <dl> <span data-ttu-id="57af5-128"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="57af5-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="57af5-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="57af5-129">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="57af5-130"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="57af5-130"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="57af5-131">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="57af5-131">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="57af5-132">備註</span><span class="sxs-lookup"><span data-stu-id="57af5-132">Remarks</span></span>

<span data-ttu-id="57af5-133">用來抓取設定檔案陣列的搜尋路徑將包含 [**IVMVirtualPC：： SearchPaths**](ivmvirtualpc-searchpaths.md) 和 [**IVMVirtualPC：:D efaultvmconfigurationpath**](ivmvirtualpc-defaultvmconfigurationpath.md) 之前的設定，除了 *inAdditionalSearchPaths* 參數所指定的路徑。</span><span class="sxs-lookup"><span data-stu-id="57af5-133">The search paths used to retrieve the array of configuration files will include those set previously by [**IVMVirtualPC::SearchPaths**](ivmvirtualpc-searchpaths.md) and [**IVMVirtualPC::DefaultVMConfigurationPath**](ivmvirtualpc-defaultvmconfigurationpath.md) in addition to those specified by the *inAdditionalSearchPaths* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="57af5-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="57af5-134">Requirements</span></span>



| <span data-ttu-id="57af5-135">需求</span><span class="sxs-lookup"><span data-stu-id="57af5-135">Requirement</span></span> | <span data-ttu-id="57af5-136">值</span><span class="sxs-lookup"><span data-stu-id="57af5-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="57af5-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57af5-137">Minimum supported client</span></span><br/> | <span data-ttu-id="57af5-138">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57af5-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="57af5-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57af5-139">Minimum supported server</span></span><br/> | <span data-ttu-id="57af5-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="57af5-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="57af5-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="57af5-141">End of client support</span></span><br/>    | <span data-ttu-id="57af5-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="57af5-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="57af5-143">產品</span><span class="sxs-lookup"><span data-stu-id="57af5-143">Product</span></span><br/>                  | <span data-ttu-id="57af5-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="57af5-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="57af5-145">標頭</span><span class="sxs-lookup"><span data-stu-id="57af5-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="57af5-146"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="57af5-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="57af5-147">IID</span><span class="sxs-lookup"><span data-stu-id="57af5-147">IID</span></span><br/>                      | <span data-ttu-id="57af5-148">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="57af5-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="57af5-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57af5-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57af5-150">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="57af5-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

