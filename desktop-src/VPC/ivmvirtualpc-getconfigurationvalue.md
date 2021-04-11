---
title: 'IVMVirtualPC GetConfigurationValue 方法 (VPCCOMInterfaces .h) '
description: 擷取指定之組態設定的值。
ms.assetid: 4598b57c-9942-4b40-97b5-41ad9ec74bfa
keywords:
- GetConfigurationValue 方法 Virtual PC
- GetConfigurationValue 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，GetConfigurationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11851e2dc2e51c0dc5eed876fc755655ed488554
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105198"
---
# <a name="ivmvirtualpcgetconfigurationvalue-method"></a><span data-ttu-id="60947-106">IVMVirtualPC：： GetConfigurationValue 方法</span><span class="sxs-lookup"><span data-stu-id="60947-106">IVMVirtualPC::GetConfigurationValue method</span></span>

<span data-ttu-id="60947-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="60947-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="60947-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="60947-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="60947-109">擷取指定之組態設定的值。</span><span class="sxs-lookup"><span data-stu-id="60947-109">Retrieves the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="60947-110">語法</span><span class="sxs-lookup"><span data-stu-id="60947-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    preferenceKey,
  [out, retval] VARIANT *preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="60947-111">參數</span><span class="sxs-lookup"><span data-stu-id="60947-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="60947-112">*preferenceKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="60947-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="60947-113">用來識別喜好設定的金鑰，儲存在設定檔中。</span><span class="sxs-lookup"><span data-stu-id="60947-113">The key used to identify the preference, as stored in the configuration file.</span></span>

</dd> <dt>

<span data-ttu-id="60947-114">*preferenceValue* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="60947-114">*preferenceValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="60947-115">喜好設定值。</span><span class="sxs-lookup"><span data-stu-id="60947-115">The preference value.</span></span> <span data-ttu-id="60947-116">這個參數可以是下列其中一個 **VARIANT** 類型： **vt \_ ARRAY** \| **vt \_ UI1** (原始位元組) 、 **vt \_ BSTR** (string) 、 **vt \_ I4** (整數) 或 **vt \_ BOOL** (布林值) 。</span><span class="sxs-lookup"><span data-stu-id="60947-116">This parameter may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="60947-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="60947-117">Return value</span></span>

<span data-ttu-id="60947-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="60947-118">This method can return one of these values.</span></span>



| <span data-ttu-id="60947-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="60947-119">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="60947-120">Description</span><span class="sxs-lookup"><span data-stu-id="60947-120">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="60947-121"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="60947-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="60947-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="60947-122">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="60947-123"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="60947-123"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="60947-124">*PreferenceKey* 或 *PreferenceValue* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="60947-124">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="60947-125"><dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xa0040300</dt></span><span class="sxs-lookup"><span data-stu-id="60947-125"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xa0040300</dt></span></span> </dl>                   | <span data-ttu-id="60947-126">找不到喜好設定。</span><span class="sxs-lookup"><span data-stu-id="60947-126">The preference was not found.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="60947-127"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="60947-127"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="60947-128">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="60947-128">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |
| <dl> <span data-ttu-id="60947-129"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="60947-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="60947-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="60947-130">An unexpected error has occurred.</span></span><br/>                                                    |



 

## <a name="remarks"></a><span data-ttu-id="60947-131">備註</span><span class="sxs-lookup"><span data-stu-id="60947-131">Remarks</span></span>

<span data-ttu-id="60947-132">這個方法可為目前使用者的任何喜好設定值提供低層級的存取權。</span><span class="sxs-lookup"><span data-stu-id="60947-132">This method provides low-level access to any preference value for the current user.</span></span> <span data-ttu-id="60947-133">您可以使用它來抓取客戶定義索引鍵的喜好設定值。</span><span class="sxs-lookup"><span data-stu-id="60947-133">It can be used to retrieve preference values for customer-defined keys.</span></span>

## <a name="requirements"></a><span data-ttu-id="60947-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="60947-134">Requirements</span></span>



| <span data-ttu-id="60947-135">需求</span><span class="sxs-lookup"><span data-stu-id="60947-135">Requirement</span></span> | <span data-ttu-id="60947-136">值</span><span class="sxs-lookup"><span data-stu-id="60947-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="60947-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60947-137">Minimum supported client</span></span><br/> | <span data-ttu-id="60947-138">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60947-138">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="60947-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60947-139">Minimum supported server</span></span><br/> | <span data-ttu-id="60947-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="60947-140">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="60947-141">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="60947-141">End of client support</span></span><br/>    | <span data-ttu-id="60947-142">Windows 7</span><span class="sxs-lookup"><span data-stu-id="60947-142">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="60947-143">產品</span><span class="sxs-lookup"><span data-stu-id="60947-143">Product</span></span><br/>                  | <span data-ttu-id="60947-144">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="60947-144">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="60947-145">標頭</span><span class="sxs-lookup"><span data-stu-id="60947-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="60947-146"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="60947-146"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="60947-147">IID</span><span class="sxs-lookup"><span data-stu-id="60947-147">IID</span></span><br/>                      | <span data-ttu-id="60947-148">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="60947-148">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="60947-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="60947-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="60947-150">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="60947-150">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> </dl>

 

