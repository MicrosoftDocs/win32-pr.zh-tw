---
title: 'IVMVirtualMachine RemoveConfigurationValue 方法 (VPCCOMInterfaces .h) '
description: 移除此虛擬機器的指定設定設定值。
ms.assetid: 2d75a667-9656-4d4c-bafe-f3f8be3763f5
keywords:
- RemoveConfigurationValue 方法 Virtual PC
- RemoveConfigurationValue 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，RemoveConfigurationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.RemoveConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 683cad2c7cce34822f6f5607ea2676902284baf0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466153"
---
# <a name="ivmvirtualmachineremoveconfigurationvalue-method"></a><span data-ttu-id="cec4d-106">IVMVirtualMachine：： RemoveConfigurationValue 方法</span><span class="sxs-lookup"><span data-stu-id="cec4d-106">IVMVirtualMachine::RemoveConfigurationValue method</span></span>

<span data-ttu-id="cec4d-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="cec4d-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="cec4d-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="cec4d-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="cec4d-109">移除此虛擬機器的指定設定設定值。</span><span class="sxs-lookup"><span data-stu-id="cec4d-109">Removes the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="cec4d-110">語法</span><span class="sxs-lookup"><span data-stu-id="cec4d-110">Syntax</span></span>


```C++
HRESULT RemoveConfigurationValue(
  [in] BSTR configurationKey
);
```



## <a name="parameters"></a><span data-ttu-id="cec4d-111">參數</span><span class="sxs-lookup"><span data-stu-id="cec4d-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cec4d-112">*configurationKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="cec4d-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cec4d-113">用來識別儲存在 ". .vmc" 檔案中之設定值的索引鍵 \* 。</span><span class="sxs-lookup"><span data-stu-id="cec4d-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cec4d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="cec4d-114">Return value</span></span>

<span data-ttu-id="cec4d-115">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="cec4d-115">This method can return one of these values.</span></span>



| <span data-ttu-id="cec4d-116">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="cec4d-116">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="cec4d-117">Description</span><span class="sxs-lookup"><span data-stu-id="cec4d-117">Description</span></span>                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <span data-ttu-id="cec4d-118"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="cec4d-118"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="cec4d-119">作業成功。</span><span class="sxs-lookup"><span data-stu-id="cec4d-119">The operation was successful.</span></span><br/>       |
| <dl> <span data-ttu-id="cec4d-120"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="cec4d-120"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="cec4d-121">參數為 **Null** 或空白。</span><span class="sxs-lookup"><span data-stu-id="cec4d-121">The parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="cec4d-122"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="cec4d-122"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="cec4d-123">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="cec4d-123">The configuration is unknown.</span></span><br/>       |
| <dl> <span data-ttu-id="cec4d-124"><dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="cec4d-124"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="cec4d-125">找不到喜好設定。</span><span class="sxs-lookup"><span data-stu-id="cec4d-125">The preference was not found.</span></span><br/>       |
| <dl> <span data-ttu-id="cec4d-126"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="cec4d-126"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="cec4d-127">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="cec4d-127">An unexpected error has occurred.</span></span><br/>   |



 

## <a name="remarks"></a><span data-ttu-id="cec4d-128">備註</span><span class="sxs-lookup"><span data-stu-id="cec4d-128">Remarks</span></span>

<span data-ttu-id="cec4d-129">這個方法會提供任何設定值的低層級存取權。</span><span class="sxs-lookup"><span data-stu-id="cec4d-129">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="cec4d-130">您可以使用它來移除客戶定義索引鍵的設定值。</span><span class="sxs-lookup"><span data-stu-id="cec4d-130">It can be used to remove configuration values for customer-defined keys.</span></span> <span data-ttu-id="cec4d-131">如果您使用此方法移除系統設定值，請務必小心，因為當虛擬機器正在執行時，無法變更部分值。</span><span class="sxs-lookup"><span data-stu-id="cec4d-131">Be careful if you use this method to remove system configuration values, since some values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="cec4d-132">設定金鑰位於虛擬機器的 " \* . .vmc" 檔案中（XML 格式）。</span><span class="sxs-lookup"><span data-stu-id="cec4d-132">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="cec4d-133">金鑰會以類似于 Windows 中登錄機碼的階層式方式儲存。</span><span class="sxs-lookup"><span data-stu-id="cec4d-133">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="cec4d-134">若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="cec4d-134">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="cec4d-135">例如，若要移除 \_ 位於下列金鑰樹狀結構中「ram 大小」機碼的值：</span><span class="sxs-lookup"><span data-stu-id="cec4d-135">For example, to remove the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="cec4d-136">*ConfigurationKey* 路徑字串的指定方式如下：</span><span class="sxs-lookup"><span data-stu-id="cec4d-136">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="cec4d-137">如果所需樹狀結構中的任何索引鍵具有 "id" 屬性值，則屬性和其值會在其相關聯的設定金鑰之後，緊接在 *configurationKey* 路徑字串中，並使用下列括弧格式： " \[ @id ="*id \_ value*" \] "。</span><span class="sxs-lookup"><span data-stu-id="cec4d-137">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="cec4d-138">例如，若要移除位於下列金鑰樹狀結構中的「絕對」索引鍵的值：</span><span class="sxs-lookup"><span data-stu-id="cec4d-138">For example, to remove the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="cec4d-139">*ConfigurationKey* 路徑字串的指定方式如下：</span><span class="sxs-lookup"><span data-stu-id="cec4d-139">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="cec4d-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="cec4d-140">Requirements</span></span>



| <span data-ttu-id="cec4d-141">需求</span><span class="sxs-lookup"><span data-stu-id="cec4d-141">Requirement</span></span> | <span data-ttu-id="cec4d-142">值</span><span class="sxs-lookup"><span data-stu-id="cec4d-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="cec4d-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cec4d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="cec4d-144">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cec4d-144">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cec4d-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cec4d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="cec4d-146">都不支援</span><span class="sxs-lookup"><span data-stu-id="cec4d-146">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="cec4d-147">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="cec4d-147">End of client support</span></span><br/>    | <span data-ttu-id="cec4d-148">Windows 7</span><span class="sxs-lookup"><span data-stu-id="cec4d-148">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="cec4d-149">產品</span><span class="sxs-lookup"><span data-stu-id="cec4d-149">Product</span></span><br/>                  | <span data-ttu-id="cec4d-150">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="cec4d-150">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="cec4d-151">標頭</span><span class="sxs-lookup"><span data-stu-id="cec4d-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="cec4d-152"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="cec4d-152"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="cec4d-153">IID</span><span class="sxs-lookup"><span data-stu-id="cec4d-153">IID</span></span><br/>                      | <span data-ttu-id="cec4d-154">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="cec4d-154">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="cec4d-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cec4d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cec4d-156">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="cec4d-156">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

