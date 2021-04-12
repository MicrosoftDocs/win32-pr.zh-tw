---
title: 'IVMVirtualMachine RemoveActivationValue 方法 (VPCCOMInterfaces .h) '
description: 移除此虛擬機器之指定啟用設定的值。
ms.assetid: 8e9b9d95-aec9-4b73-afc3-cd0d7300f40f
keywords:
- RemoveActivationValue 方法 Virtual PC
- RemoveActivationValue 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，RemoveActivationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b0461b27e43066f32c25663e3b38dab9b3b71b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025189"
---
# <a name="ivmvirtualmachineremoveactivationvalue-method"></a><span data-ttu-id="ce22c-106">IVMVirtualMachine：： RemoveActivationValue 方法</span><span class="sxs-lookup"><span data-stu-id="ce22c-106">IVMVirtualMachine::RemoveActivationValue method</span></span>

<span data-ttu-id="ce22c-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="ce22c-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="ce22c-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="ce22c-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="ce22c-109">移除此虛擬機器之指定啟用設定的值。</span><span class="sxs-lookup"><span data-stu-id="ce22c-109">Removes the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="ce22c-110">語法</span><span class="sxs-lookup"><span data-stu-id="ce22c-110">Syntax</span></span>


```C++
HRESULT RemoveActivationValue(
  [in] BSTR activationKey
);
```



## <a name="parameters"></a><span data-ttu-id="ce22c-111">參數</span><span class="sxs-lookup"><span data-stu-id="ce22c-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ce22c-112">*activationKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ce22c-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ce22c-113">用來識別 .vmc 檔中所儲存之啟用值的索引鍵 \* 。</span><span class="sxs-lookup"><span data-stu-id="ce22c-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ce22c-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="ce22c-114">Return value</span></span>

<span data-ttu-id="ce22c-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="ce22c-115">This method can return one of these values.</span></span>



| <span data-ttu-id="ce22c-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="ce22c-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="ce22c-117">Description</span><span class="sxs-lookup"><span data-stu-id="ce22c-117">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="ce22c-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ce22c-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="ce22c-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ce22c-119">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="ce22c-120"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="ce22c-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="ce22c-121">參數為 **Null** 或空白。</span><span class="sxs-lookup"><span data-stu-id="ce22c-121">The parameter is **NULL** or empty.</span></span><br/>                                          |
| <dl> <span data-ttu-id="ce22c-122"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="ce22c-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="ce22c-123">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="ce22c-123">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="ce22c-124"><dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="ce22c-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="ce22c-125">找不到喜好設定，或此設定沒有有效的啟用。</span><span class="sxs-lookup"><span data-stu-id="ce22c-125">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="ce22c-126"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="ce22c-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="ce22c-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="ce22c-127">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="ce22c-128">備註</span><span class="sxs-lookup"><span data-stu-id="ce22c-128">Remarks</span></span>

<span data-ttu-id="ce22c-129">此方法可提供任何啟用值的低層級存取權。</span><span class="sxs-lookup"><span data-stu-id="ce22c-129">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="ce22c-130">您可以使用它來移除客戶定義索引鍵的啟用值。</span><span class="sxs-lookup"><span data-stu-id="ce22c-130">It can be used to remove activation values for customer-defined keys.</span></span> <span data-ttu-id="ce22c-131">如果您使用此方法移除系統啟用值，請務必小心，因為當虛擬機器正在執行時，無法變更部分值。</span><span class="sxs-lookup"><span data-stu-id="ce22c-131">Be careful if you use this method to remove system activation values, since some values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="ce22c-132">當虛擬機器啟動時，會建立其設定值的複本，以成為其啟用值的集合。</span><span class="sxs-lookup"><span data-stu-id="ce22c-132">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="ce22c-133">啟用值會維持，直到虛擬機器關閉或重新開機為止。</span><span class="sxs-lookup"><span data-stu-id="ce22c-133">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="ce22c-134">請注意，Windows Virtual PC 可能只會使用設定來儲存特定金鑰的值，也就是可能永遠不會使用啟用值。</span><span class="sxs-lookup"><span data-stu-id="ce22c-134">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="ce22c-135">虛擬機器會話必須正在執行，才能變更任何啟用值。</span><span class="sxs-lookup"><span data-stu-id="ce22c-135">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="ce22c-136">啟用金鑰會以階層方式儲存在內部，類似于 Windows 中的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="ce22c-136">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="ce22c-137">若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="ce22c-137">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="ce22c-138">例如，若要移除 \_ 位於下列金鑰樹狀結構中「預設動作」索引鍵的值：</span><span class="sxs-lookup"><span data-stu-id="ce22c-138">For example, to remove the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="ce22c-139">*ActivationKey* 路徑字串的指定方式如下：</span><span class="sxs-lookup"><span data-stu-id="ce22c-139">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="ce22c-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="ce22c-140">Requirements</span></span>



| <span data-ttu-id="ce22c-141">需求</span><span class="sxs-lookup"><span data-stu-id="ce22c-141">Requirement</span></span> | <span data-ttu-id="ce22c-142">值</span><span class="sxs-lookup"><span data-stu-id="ce22c-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce22c-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ce22c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="ce22c-144">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ce22c-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ce22c-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ce22c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="ce22c-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="ce22c-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="ce22c-147">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="ce22c-147">End of client support</span></span><br/>    | <span data-ttu-id="ce22c-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="ce22c-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="ce22c-149">產品</span><span class="sxs-lookup"><span data-stu-id="ce22c-149">Product</span></span><br/>                  | <span data-ttu-id="ce22c-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="ce22c-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="ce22c-151">標頭</span><span class="sxs-lookup"><span data-stu-id="ce22c-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="ce22c-152"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="ce22c-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="ce22c-153">IID</span><span class="sxs-lookup"><span data-stu-id="ce22c-153">IID</span></span><br/>                      | <span data-ttu-id="ce22c-154">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="ce22c-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="ce22c-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ce22c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ce22c-156">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="ce22c-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

