---
title: 'IVMVirtualPC RemoveConfigurationValue 方法 (VPCCOMInterfaces .h) '
description: 移除指定之設定的值。
ms.assetid: 07bafa5e-bf62-45bf-af4e-a66050f5afad
keywords:
- RemoveConfigurationValue 方法 Virtual PC
- RemoveConfigurationValue 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，RemoveConfigurationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73821657ed7983e2d92fc379c3222f343763b3ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844052"
---
# <a name="ivmvirtualpcremoveconfigurationvalue-method"></a><span data-ttu-id="e6f94-106">IVMVirtualPC：： RemoveConfigurationValue 方法</span><span class="sxs-lookup"><span data-stu-id="e6f94-106">IVMVirtualPC::RemoveConfigurationValue method</span></span>

<span data-ttu-id="e6f94-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="e6f94-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="e6f94-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="e6f94-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="e6f94-109">移除指定之設定的值。</span><span class="sxs-lookup"><span data-stu-id="e6f94-109">Removes the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6f94-110">語法</span><span class="sxs-lookup"><span data-stu-id="e6f94-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR preferenceKey
);
```



## <a name="parameters"></a><span data-ttu-id="e6f94-111">參數</span><span class="sxs-lookup"><span data-stu-id="e6f94-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6f94-112">*preferenceKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e6f94-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6f94-113">用來識別喜好設定的金鑰，儲存在設定檔中。</span><span class="sxs-lookup"><span data-stu-id="e6f94-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6f94-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e6f94-114">Return value</span></span>

<span data-ttu-id="e6f94-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="e6f94-115">This method can return one of these values.</span></span>



| <span data-ttu-id="e6f94-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="e6f94-116">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="e6f94-117">Description</span><span class="sxs-lookup"><span data-stu-id="e6f94-117">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="e6f94-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="e6f94-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="e6f94-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="e6f94-119">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e6f94-120"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="e6f94-120"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="e6f94-121">*PreferenceKey* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="e6f94-121">The *preferenceKey* parameter is **NULL**.</span></span><br/>                                           |
| <dl> <span data-ttu-id="e6f94-122"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="e6f94-122"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="e6f94-123">*PreferenceKey* 參數無效或為空字串。</span><span class="sxs-lookup"><span data-stu-id="e6f94-123">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="e6f94-124"><dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="e6f94-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl>                   | <span data-ttu-id="e6f94-125">找不到喜好設定。</span><span class="sxs-lookup"><span data-stu-id="e6f94-125">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="e6f94-126"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="e6f94-126"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="e6f94-127">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="e6f94-127">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="e6f94-128"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="e6f94-128"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="e6f94-129">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="e6f94-129">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="e6f94-130">備註</span><span class="sxs-lookup"><span data-stu-id="e6f94-130">Remarks</span></span>

<span data-ttu-id="e6f94-131">這個方法可為目前使用者的任何喜好設定值提供低層級的存取權。</span><span class="sxs-lookup"><span data-stu-id="e6f94-131">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="e6f94-132">可以用來移除客戶定義索引鍵的喜好設定值。</span><span class="sxs-lookup"><span data-stu-id="e6f94-132">It can be used to remove preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6f94-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6f94-133">Requirements</span></span>



| <span data-ttu-id="e6f94-134">需求</span><span class="sxs-lookup"><span data-stu-id="e6f94-134">Requirement</span></span> | <span data-ttu-id="e6f94-135">值</span><span class="sxs-lookup"><span data-stu-id="e6f94-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6f94-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6f94-136">Minimum supported client</span></span><br/> | <span data-ttu-id="e6f94-137">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e6f94-137">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e6f94-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6f94-138">Minimum supported server</span></span><br/> | <span data-ttu-id="e6f94-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="e6f94-139">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="e6f94-140">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e6f94-140">End of client support</span></span><br/>    | <span data-ttu-id="e6f94-141">Windows 7</span><span class="sxs-lookup"><span data-stu-id="e6f94-141">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="e6f94-142">產品</span><span class="sxs-lookup"><span data-stu-id="e6f94-142">Product</span></span><br/>                  | <span data-ttu-id="e6f94-143">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="e6f94-143">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="e6f94-144">標頭</span><span class="sxs-lookup"><span data-stu-id="e6f94-144">Header</span></span><br/>                   | <dl> <span data-ttu-id="e6f94-145"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="e6f94-145"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="e6f94-146">IID</span><span class="sxs-lookup"><span data-stu-id="e6f94-146">IID</span></span><br/>                      | <span data-ttu-id="e6f94-147">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="e6f94-147">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="e6f94-148">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6f94-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6f94-149">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="e6f94-149">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

