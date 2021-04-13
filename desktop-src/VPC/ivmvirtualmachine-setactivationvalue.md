---
title: 'IVMVirtualMachine SetActivationValue 方法 (VPCCOMInterfaces .h) '
description: 為此虛擬機器設定指定之啟用設定的值。
ms.assetid: 6d664a80-1777-42ca-8454-df84c64ab505
keywords:
- SetActivationValue 方法 Virtual PC
- SetActivationValue 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，SetActivationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c7cb48b5691a9ca99a0fca5b696d8b545a40e46
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466385"
---
# <a name="ivmvirtualmachinesetactivationvalue-method"></a><span data-ttu-id="400de-106">IVMVirtualMachine：： SetActivationValue 方法</span><span class="sxs-lookup"><span data-stu-id="400de-106">IVMVirtualMachine::SetActivationValue method</span></span>

<span data-ttu-id="400de-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="400de-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="400de-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="400de-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="400de-109">為此虛擬機器設定指定之啟用設定的值。</span><span class="sxs-lookup"><span data-stu-id="400de-109">Sets the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="400de-110">語法</span><span class="sxs-lookup"><span data-stu-id="400de-110">Syntax</span></span>


```C++
HRESULT SetActivationValue(
  [in] BSTR    activationKey,
  [in] VARIANT activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="400de-111">參數</span><span class="sxs-lookup"><span data-stu-id="400de-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="400de-112">*activationKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="400de-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="400de-113">用來識別 .vmc 檔中所儲存之啟用值的索引鍵 \* 。</span><span class="sxs-lookup"><span data-stu-id="400de-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="400de-114">*activationValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="400de-114">*activationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="400de-115">啟用值。</span><span class="sxs-lookup"><span data-stu-id="400de-115">The activation value.</span></span> <span data-ttu-id="400de-116">這個值可以是下列其中一個 **VARIANT** 類型： **vt \_ ARRAY** \| **vt \_ UI1** (原始位元組) 、 **vt \_ BSTR** (string) 、 **vt \_ UI4** (整數) 或 **vt \_ BOOL** (布林值) 。</span><span class="sxs-lookup"><span data-stu-id="400de-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="400de-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="400de-117">Return value</span></span>

<span data-ttu-id="400de-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="400de-118">This method can return one of these values.</span></span>



| <span data-ttu-id="400de-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="400de-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="400de-120">Description</span><span class="sxs-lookup"><span data-stu-id="400de-120">Description</span></span>                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="400de-121"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="400de-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="400de-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="400de-122">The operation was successful.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="400de-123"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="400de-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="400de-124">*ActivationKey* 參數為 **Null** 或空白，或 *activationValue* 參數不是有效的 variant 類型。</span><span class="sxs-lookup"><span data-stu-id="400de-124">The *activationKey* parameter is **NULL** or empty, or the *activationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="400de-125"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="400de-125"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="400de-126">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="400de-126">The configuration is unknown.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="400de-127"><dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="400de-127"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="400de-128">設定沒有有效的啟用。</span><span class="sxs-lookup"><span data-stu-id="400de-128">The configuration has no valid activation.</span></span><br/>                                                                          |
| <dl> <span data-ttu-id="400de-129"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="400de-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="400de-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="400de-130">An unexpected error has occurred.</span></span><br/>                                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="400de-131">備註</span><span class="sxs-lookup"><span data-stu-id="400de-131">Remarks</span></span>

<span data-ttu-id="400de-132">此方法可提供任何啟用值的低層級存取權。</span><span class="sxs-lookup"><span data-stu-id="400de-132">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="400de-133">可以用來設定客戶定義之索引鍵的啟用值。</span><span class="sxs-lookup"><span data-stu-id="400de-133">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="400de-134">如果您使用這個方法來設定系統啟用值，就必須小心，因為啟動值不會執行錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="400de-134">Be careful if you use this method to set system activation values, since no error checking is performed on the activation value.</span></span> <span data-ttu-id="400de-135">此外，當虛擬機器正在執行時，無法變更某些啟用值。</span><span class="sxs-lookup"><span data-stu-id="400de-135">Also, some activation values cannot be changed while the virtual machine is running.</span></span> <span data-ttu-id="400de-136">當虛擬機器啟動時，會建立其設定值的複本，以成為其啟用值的集合。</span><span class="sxs-lookup"><span data-stu-id="400de-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="400de-137">啟用值會維持，直到虛擬機器關閉或重新開機為止。</span><span class="sxs-lookup"><span data-stu-id="400de-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="400de-138">請注意，Windows Virtual PC 可能只會使用設定來儲存特定金鑰的值，也就是可能永遠不會使用啟用值。</span><span class="sxs-lookup"><span data-stu-id="400de-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

> [!Note]  
> <span data-ttu-id="400de-139">虛擬機器會話必須正在執行，才能變更任何啟用值。</span><span class="sxs-lookup"><span data-stu-id="400de-139">The virtual machine session must be running before any activation values can be changed.</span></span>

 

<span data-ttu-id="400de-140">啟用金鑰會以階層方式儲存在內部，類似于 Windows 中的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="400de-140">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="400de-141">若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="400de-141">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="400de-142">例如，若要設定 \_ 位於下列金鑰樹狀結構中「預設動作」索引鍵的值：</span><span class="sxs-lookup"><span data-stu-id="400de-142">For example, to set the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="400de-143">*ActivationKey* 路徑字串的指定方式如下：</span><span class="sxs-lookup"><span data-stu-id="400de-143">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="400de-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="400de-144">Requirements</span></span>



| <span data-ttu-id="400de-145">需求</span><span class="sxs-lookup"><span data-stu-id="400de-145">Requirement</span></span> | <span data-ttu-id="400de-146">值</span><span class="sxs-lookup"><span data-stu-id="400de-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="400de-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="400de-147">Minimum supported client</span></span><br/> | <span data-ttu-id="400de-148">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="400de-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="400de-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="400de-149">Minimum supported server</span></span><br/> | <span data-ttu-id="400de-150">都不支援</span><span class="sxs-lookup"><span data-stu-id="400de-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="400de-151">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="400de-151">End of client support</span></span><br/>    | <span data-ttu-id="400de-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="400de-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="400de-153">產品</span><span class="sxs-lookup"><span data-stu-id="400de-153">Product</span></span><br/>                  | <span data-ttu-id="400de-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="400de-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="400de-155">標頭</span><span class="sxs-lookup"><span data-stu-id="400de-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="400de-156"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="400de-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="400de-157">IID</span><span class="sxs-lookup"><span data-stu-id="400de-157">IID</span></span><br/>                      | <span data-ttu-id="400de-158">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="400de-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="400de-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="400de-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="400de-160">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="400de-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

