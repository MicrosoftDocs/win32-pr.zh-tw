---
title: 'IVMVirtualMachine GetActivationValue 方法 (VPCCOMInterfaces .h) '
description: 抓取此虛擬機器之指定啟用設定的值。
ms.assetid: 9a6f138f-6a8a-4cdf-8fb3-83d541d88fba
keywords:
- GetActivationValue 方法 Virtual PC
- GetActivationValue 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，GetActivationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetActivationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e87b51e34feb654fa9c5ab00ed7906268cdc9ec3
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317103"
---
# <a name="ivmvirtualmachinegetactivationvalue-method"></a><span data-ttu-id="3550a-106">IVMVirtualMachine：： GetActivationValue 方法</span><span class="sxs-lookup"><span data-stu-id="3550a-106">IVMVirtualMachine::GetActivationValue method</span></span>

<span data-ttu-id="3550a-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="3550a-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="3550a-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="3550a-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="3550a-109">抓取此虛擬機器之指定啟用設定的值。</span><span class="sxs-lookup"><span data-stu-id="3550a-109">Retrieves the value of the specified activation setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="3550a-110">語法</span><span class="sxs-lookup"><span data-stu-id="3550a-110">Syntax</span></span>


```C++
HRESULT GetActivationValue(
  [in]          BSTR    activationKey,
  [out, retval] VARIANT *activationValue
);
```



## <a name="parameters"></a><span data-ttu-id="3550a-111">參數</span><span class="sxs-lookup"><span data-stu-id="3550a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3550a-112">*activationKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3550a-112">*activationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3550a-113">用來識別 .vmc 檔中所儲存之啟用值的索引鍵 \* 。</span><span class="sxs-lookup"><span data-stu-id="3550a-113">The key used to identify the activation value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="3550a-114">*activationValue* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="3550a-114">*activationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="3550a-115">啟用值。</span><span class="sxs-lookup"><span data-stu-id="3550a-115">The activation value.</span></span> <span data-ttu-id="3550a-116">這個值可以是下列其中一個 **VARIANT** 類型： **vt \_ ARRAY** \| **vt \_ UI1** (原始位元組) 、 **vt \_ BSTR** (string) 、 **vt \_ I4** (整數) 或 **vt \_ BOOL** (布林值) 。</span><span class="sxs-lookup"><span data-stu-id="3550a-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY** \| **VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3550a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="3550a-117">Return value</span></span>

<span data-ttu-id="3550a-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="3550a-118">This method can return one of these values.</span></span>



| <span data-ttu-id="3550a-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="3550a-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="3550a-120">Description</span><span class="sxs-lookup"><span data-stu-id="3550a-120">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="3550a-121"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="3550a-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="3550a-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="3550a-122">The operation was successful.</span></span><br/>                                                |
| <dl> <span data-ttu-id="3550a-123"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="3550a-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="3550a-124">*ActivationKey* 參數為 **Null** 或空白。</span><span class="sxs-lookup"><span data-stu-id="3550a-124">The *activationKey* parameter is **NULL** or empty.</span></span><br/>                          |
| <dl> <span data-ttu-id="3550a-125"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="3550a-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="3550a-126">*ActivationValue* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="3550a-126">The *activationValue* parameter is **NULL**.</span></span><br/>                                 |
| <dl> <span data-ttu-id="3550a-127"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="3550a-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="3550a-128">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="3550a-128">The configuration is unknown.</span></span><br/>                                                |
| <dl> <span data-ttu-id="3550a-129"><dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="3550a-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="3550a-130">找不到喜好設定，或此設定沒有有效的啟用。</span><span class="sxs-lookup"><span data-stu-id="3550a-130">The preference was not found, or this configuration has no valid activation.</span></span><br/> |
| <dl> <span data-ttu-id="3550a-131"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="3550a-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="3550a-132">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="3550a-132">An unexpected error has occurred.</span></span><br/>                                            |



 

## <a name="remarks"></a><span data-ttu-id="3550a-133">備註</span><span class="sxs-lookup"><span data-stu-id="3550a-133">Remarks</span></span>

<span data-ttu-id="3550a-134">此方法可提供任何啟用值的低層級存取權。</span><span class="sxs-lookup"><span data-stu-id="3550a-134">This method provides low-level access to any activation value.</span></span> <span data-ttu-id="3550a-135">可以用來設定客戶定義之索引鍵的啟用值。</span><span class="sxs-lookup"><span data-stu-id="3550a-135">It can be used to set activation values for customer-defined keys.</span></span> <span data-ttu-id="3550a-136">當虛擬機器啟動時，會建立其設定值的複本，以成為其啟用值的集合。</span><span class="sxs-lookup"><span data-stu-id="3550a-136">When a virtual machine is started, a copy is made of its configuration values, which becomes its set of activation values.</span></span> <span data-ttu-id="3550a-137">啟用值會維持，直到虛擬機器關閉或重新開機為止。</span><span class="sxs-lookup"><span data-stu-id="3550a-137">Activation values are maintained until the virtual machine is shut down or restarted.</span></span> <span data-ttu-id="3550a-138">請注意，Windows Virtual PC 可能只會使用設定來儲存特定金鑰的值，也就是可能永遠不會使用啟用值。</span><span class="sxs-lookup"><span data-stu-id="3550a-138">Note that Windows Virtual PC may only use the configuration to store values for certain keys, that is, the activation value may never be used.</span></span>

<span data-ttu-id="3550a-139">啟用金鑰會以階層方式儲存在內部，類似于 Windows 中的登錄機碼。</span><span class="sxs-lookup"><span data-stu-id="3550a-139">Activation keys are stored internally in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="3550a-140">若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="3550a-140">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="3550a-141">例如，若要讀取 \_ 位於下列金鑰樹狀結構中「預設動作」索引鍵的值：</span><span class="sxs-lookup"><span data-stu-id="3550a-141">For example, to read the value of the "default\_action" key located in the following key tree:</span></span>

``` syntax
<settings>
    <undo_drives>
        <default_action type="integer">1</default_action>
```

<span data-ttu-id="3550a-142">*ActivationKey* 路徑字串的指定方式如下：</span><span class="sxs-lookup"><span data-stu-id="3550a-142">The *activationKey* path string would be specified as follows:</span></span>

``` syntax
"settings/undo_drives/default_action"
```

## <a name="requirements"></a><span data-ttu-id="3550a-143">規格需求</span><span class="sxs-lookup"><span data-stu-id="3550a-143">Requirements</span></span>



| <span data-ttu-id="3550a-144">需求</span><span class="sxs-lookup"><span data-stu-id="3550a-144">Requirement</span></span> | <span data-ttu-id="3550a-145">值</span><span class="sxs-lookup"><span data-stu-id="3550a-145">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="3550a-146">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3550a-146">Minimum supported client</span></span><br/> | <span data-ttu-id="3550a-147">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3550a-147">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3550a-148">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3550a-148">Minimum supported server</span></span><br/> | <span data-ttu-id="3550a-149">都不支援</span><span class="sxs-lookup"><span data-stu-id="3550a-149">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="3550a-150">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="3550a-150">End of client support</span></span><br/>    | <span data-ttu-id="3550a-151">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3550a-151">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="3550a-152">產品</span><span class="sxs-lookup"><span data-stu-id="3550a-152">Product</span></span><br/>                  | <span data-ttu-id="3550a-153">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="3550a-153">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="3550a-154">標頭</span><span class="sxs-lookup"><span data-stu-id="3550a-154">Header</span></span><br/>                   | <dl> <span data-ttu-id="3550a-155"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="3550a-155"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="3550a-156">IID</span><span class="sxs-lookup"><span data-stu-id="3550a-156">IID</span></span><br/>                      | <span data-ttu-id="3550a-157">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="3550a-157">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="3550a-158">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3550a-158">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3550a-159">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="3550a-159">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

