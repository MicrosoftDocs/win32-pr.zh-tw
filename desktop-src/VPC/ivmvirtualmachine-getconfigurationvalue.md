---
title: 'IVMVirtualMachine GetConfigurationValue 方法 (VPCCOMInterfaces .h) '
description: 抓取此虛擬機器的指定設定設定值。
ms.assetid: fd3c509e-8a40-4828-b866-6bd2cb455ab2
keywords:
- GetConfigurationValue 方法 Virtual PC
- GetConfigurationValue 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，GetConfigurationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.GetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e98e37bd4bd5ec4ba9843ae2fdb33874a4303f1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384798"
---
# <a name="ivmvirtualmachinegetconfigurationvalue-method"></a><span data-ttu-id="39087-106">IVMVirtualMachine：： GetConfigurationValue 方法</span><span class="sxs-lookup"><span data-stu-id="39087-106">IVMVirtualMachine::GetConfigurationValue method</span></span>

<span data-ttu-id="39087-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="39087-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="39087-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="39087-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="39087-109">抓取此虛擬機器的指定設定設定值。</span><span class="sxs-lookup"><span data-stu-id="39087-109">Retrieves the value of the specified configuration setting for this virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="39087-110">語法</span><span class="sxs-lookup"><span data-stu-id="39087-110">Syntax</span></span>


```C++
HRESULT GetConfigurationValue(
  [in]          BSTR    configurationKey,
  [out, retval] VARIANT *configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="39087-111">參數</span><span class="sxs-lookup"><span data-stu-id="39087-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39087-112">*configurationKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="39087-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39087-113">用來識別儲存在 ". .vmc" 檔案中之設定值的索引鍵 \* 。</span><span class="sxs-lookup"><span data-stu-id="39087-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

</dd> <dt>

<span data-ttu-id="39087-114">*configurationValue* \[退出，retval\]</span><span class="sxs-lookup"><span data-stu-id="39087-114">*configurationValue* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="39087-115">組態值。</span><span class="sxs-lookup"><span data-stu-id="39087-115">The configuration value.</span></span> <span data-ttu-id="39087-116">這個值可以是下列其中一個 **VARIANT** 類型： **vt \_ ARRAY** \| **vt \_ UI1** (原始位元組) 、 **vt \_ BSTR** (string) 、 **vt \_ I4** (整數) 或 **vt \_ BOOL** (布林值) 。</span><span class="sxs-lookup"><span data-stu-id="39087-116">This value can be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_I4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39087-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="39087-117">Return value</span></span>

<span data-ttu-id="39087-118">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="39087-118">This method can return one of these values.</span></span>



| <span data-ttu-id="39087-119">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="39087-119">Return code/value</span></span>                                                                                                                                                      | <span data-ttu-id="39087-120">Description</span><span class="sxs-lookup"><span data-stu-id="39087-120">Description</span></span>                                                       |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="39087-121"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="39087-121"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                            | <span data-ttu-id="39087-122">作業成功。</span><span class="sxs-lookup"><span data-stu-id="39087-122">The operation was successful.</span></span><br/>                          |
| <dl> <span data-ttu-id="39087-123"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="39087-123"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>           | <span data-ttu-id="39087-124">*ConfigurationKey* 參數為 **Null** 或空白。</span><span class="sxs-lookup"><span data-stu-id="39087-124">The *configurationKey* parameter is **NULL** or empty.</span></span><br/> |
| <dl> <span data-ttu-id="39087-125"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="39087-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>              | <span data-ttu-id="39087-126">*ConfigurationValue* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="39087-126">The *configurationValue* parameter is **NULL**.</span></span><br/>        |
| <dl> <span data-ttu-id="39087-127"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="39087-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl>      | <span data-ttu-id="39087-128">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="39087-128">The configuration is unknown.</span></span><br/>                          |
| <dl> <span data-ttu-id="39087-129"><dt>**VM \_E \_ PREF \_ \_ 找不到**</dt> <dt>0xA0040300</dt></span><span class="sxs-lookup"><span data-stu-id="39087-129"><dt>**VM\_E\_PREF\_NOT\_FOUND**</dt> <dt>0xA0040300</dt></span></span> </dl> | <span data-ttu-id="39087-130">找不到喜好設定。</span><span class="sxs-lookup"><span data-stu-id="39087-130">The preference was not found.</span></span><br/>                          |
| <dl> <span data-ttu-id="39087-131"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="39087-131"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>      | <span data-ttu-id="39087-132">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="39087-132">An unexpected error has occurred.</span></span><br/>                      |



 

## <a name="remarks"></a><span data-ttu-id="39087-133">備註</span><span class="sxs-lookup"><span data-stu-id="39087-133">Remarks</span></span>

<span data-ttu-id="39087-134">這個方法會提供任何設定值的低層級存取權。</span><span class="sxs-lookup"><span data-stu-id="39087-134">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="39087-135">可以用來讀取客戶定義之索引鍵的設定值。</span><span class="sxs-lookup"><span data-stu-id="39087-135">It can be used to read configuration values for customer-defined keys.</span></span>

<span data-ttu-id="39087-136">設定金鑰位於虛擬機器的 " \* . .vmc" 檔案中（XML 格式）。</span><span class="sxs-lookup"><span data-stu-id="39087-136">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="39087-137">金鑰會以類似于 Windows 中登錄機碼的階層式方式儲存。</span><span class="sxs-lookup"><span data-stu-id="39087-137">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="39087-138">若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="39087-138">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="39087-139">例如，若要讀取 \_ 位於下列金鑰樹狀結構中「ram 大小」機碼的值：</span><span class="sxs-lookup"><span data-stu-id="39087-139">For example, to read the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <memory>
        <ram_size type="integer">128</ram_size>
```

<span data-ttu-id="39087-140">*ConfigurationKey* 路徑字串的指定方式如下：</span><span class="sxs-lookup"><span data-stu-id="39087-140">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="39087-141">如果所需樹狀結構中的任何索引鍵具有 "id" 屬性值，則屬性和其值會在其相關聯的設定金鑰之後，緊接在 *configurationKey* 路徑字串中，並使用下列括弧格式： " \[ @id ="*id \_ value*" \] "。</span><span class="sxs-lookup"><span data-stu-id="39087-141">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="39087-142">例如，若要讀取位於下列金鑰樹狀結構中「絕對」機碼的值：</span><span class="sxs-lookup"><span data-stu-id="39087-142">For example, to read the value of the "absolute" key located in the following key tree:</span></span>

``` syntax
<hardware>
    <pci_bus>
        <ide_adapter>
            <ide_controller id="1">
                <location id="0">
                    <pathname>
                        <absolute type="string">D</absolute>
```

<span data-ttu-id="39087-143">*ConfigurationKey* 路徑字串的指定方式如下：</span><span class="sxs-lookup"><span data-stu-id="39087-143">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/pci_bus/ide_adapter/ide_controller[@id=1]/location[@id=0]/pathname/absolute"
```

## <a name="requirements"></a><span data-ttu-id="39087-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="39087-144">Requirements</span></span>



| <span data-ttu-id="39087-145">需求</span><span class="sxs-lookup"><span data-stu-id="39087-145">Requirement</span></span> | <span data-ttu-id="39087-146">值</span><span class="sxs-lookup"><span data-stu-id="39087-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="39087-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="39087-147">Minimum supported client</span></span><br/> | <span data-ttu-id="39087-148">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="39087-148">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="39087-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="39087-149">Minimum supported server</span></span><br/> | <span data-ttu-id="39087-150">都不支援</span><span class="sxs-lookup"><span data-stu-id="39087-150">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="39087-151">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="39087-151">End of client support</span></span><br/>    | <span data-ttu-id="39087-152">Windows 7</span><span class="sxs-lookup"><span data-stu-id="39087-152">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="39087-153">產品</span><span class="sxs-lookup"><span data-stu-id="39087-153">Product</span></span><br/>                  | <span data-ttu-id="39087-154">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="39087-154">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="39087-155">標頭</span><span class="sxs-lookup"><span data-stu-id="39087-155">Header</span></span><br/>                   | <dl> <span data-ttu-id="39087-156"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="39087-156"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="39087-157">IID</span><span class="sxs-lookup"><span data-stu-id="39087-157">IID</span></span><br/>                      | <span data-ttu-id="39087-158">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="39087-158">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="39087-159">另請參閱</span><span class="sxs-lookup"><span data-stu-id="39087-159">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39087-160">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="39087-160">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> </dl>

 

