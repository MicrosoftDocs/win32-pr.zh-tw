---
title: 'IVMVirtualMachine SetConfigurationValue 方法 (VPCCOMInterfaces .h) '
description: 將此虛擬機器 (VM) 的指定設定值設定為。
ms.assetid: 43c3ac88-2e25-4c9e-a2ac-fcae5add62c5
keywords:
- SetConfigurationValue 方法 Virtual PC
- SetConfigurationValue 方法 Virtual PC，IVMVirtualMachine 介面
- IVMVirtualMachine 介面 Virtual PC，SetConfigurationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualMachine.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1ebafd53a2eb82ea1869b5522d0258ece67d110
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965513"
---
# <a name="ivmvirtualmachinesetconfigurationvalue-method"></a><span data-ttu-id="763b3-106">IVMVirtualMachine：： SetConfigurationValue 方法</span><span class="sxs-lookup"><span data-stu-id="763b3-106">IVMVirtualMachine::SetConfigurationValue method</span></span>

<span data-ttu-id="763b3-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="763b3-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="763b3-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="763b3-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="763b3-109">將此虛擬機器 (VM) 的指定設定值設定為。</span><span class="sxs-lookup"><span data-stu-id="763b3-109">Sets the value of the specified configuration setting for this virtual machine (VM).</span></span>

## <a name="syntax"></a><span data-ttu-id="763b3-110">語法</span><span class="sxs-lookup"><span data-stu-id="763b3-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    configurationKey,
  [in] VARIANT configurationValue
);
```



## <a name="parameters"></a><span data-ttu-id="763b3-111">參數</span><span class="sxs-lookup"><span data-stu-id="763b3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="763b3-112">*configurationKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="763b3-112">*configurationKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="763b3-113">用來識別儲存在 ". .vmc" 檔案中之設定值的索引鍵 \* 。</span><span class="sxs-lookup"><span data-stu-id="763b3-113">The key used to identify the configuration value as stored in the "\*.vmc" file.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="763b3-114">\*只有在使用 **SetConfigurationValue** 方法時，才應該對 ". .vmc" 進行變更。</span><span class="sxs-lookup"><span data-stu-id="763b3-114">Changes should be made to "\*.vmc" only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="763b3-115">\*不支援使用任何其他方法來變更 ". .vmc"。</span><span class="sxs-lookup"><span data-stu-id="763b3-115">Changing "\*.vmc" using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="763b3-116">*configurationValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="763b3-116">*configurationValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="763b3-117">組態值。</span><span class="sxs-lookup"><span data-stu-id="763b3-117">The configuration value.</span></span> <span data-ttu-id="763b3-118">這個值 cay 是下列其中一個 **VARIANT** 類型： **vt \_ ARRAY** \| **vt \_ UI1** (原始位元組) 、 **vt \_ BSTR** (string) 、 **vt \_ UI4** (整數) 或 **vt \_ BOOL** (布林值) 。</span><span class="sxs-lookup"><span data-stu-id="763b3-118">This value cay be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="763b3-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="763b3-119">Return value</span></span>

<span data-ttu-id="763b3-120">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="763b3-120">This method can return one of these values.</span></span>



| <span data-ttu-id="763b3-121">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="763b3-121">Return code/value</span></span>                                                                                                                                                 | <span data-ttu-id="763b3-122">Description</span><span class="sxs-lookup"><span data-stu-id="763b3-122">Description</span></span>                                                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="763b3-123"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="763b3-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                       | <span data-ttu-id="763b3-124">作業成功。</span><span class="sxs-lookup"><span data-stu-id="763b3-124">The operation was successful.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="763b3-125"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="763b3-125"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>      | <span data-ttu-id="763b3-126">*ConfigurationKey* 參數為 **Null** 或空白，或 *configurationValue* 參數不是有效的 variant 類型。</span><span class="sxs-lookup"><span data-stu-id="763b3-126">The *configurationKey* parameter is **NULL** or empty or the *configurationValue* parameter is not a valid variant type.</span></span><br/> |
| <dl> <span data-ttu-id="763b3-127"><dt>**VM \_E \_ VM \_ 不明**</dt> <dt>0xA0040207</dt></span><span class="sxs-lookup"><span data-stu-id="763b3-127"><dt>**VM\_E\_VM\_UNKNOWN**</dt> <dt>0xA0040207</dt></span></span> </dl> | <span data-ttu-id="763b3-128">未知的設定。</span><span class="sxs-lookup"><span data-stu-id="763b3-128">The configuration is unknown.</span></span><br/>                                                                                            |
| <dl> <span data-ttu-id="763b3-129"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="763b3-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl> | <span data-ttu-id="763b3-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="763b3-130">An unexpected error has occurred.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="763b3-131">備註</span><span class="sxs-lookup"><span data-stu-id="763b3-131">Remarks</span></span>

<span data-ttu-id="763b3-132">*ConfigurationKey* 參數支援下列值。</span><span class="sxs-lookup"><span data-stu-id="763b3-132">The following values are supported for the *configurationKey* parameter.</span></span>



| <span data-ttu-id="763b3-133">*configurationKey* 值</span><span class="sxs-lookup"><span data-stu-id="763b3-133">*configurationKey* value</span></span>                                     | <span data-ttu-id="763b3-134">Description</span><span class="sxs-lookup"><span data-stu-id="763b3-134">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="763b3-135">資料類型</span><span class="sxs-lookup"><span data-stu-id="763b3-135">Data type</span></span>            | <span data-ttu-id="763b3-136">預設值</span><span class="sxs-lookup"><span data-stu-id="763b3-136">Default value</span></span>     |
|--------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-------------------|
| <span data-ttu-id="763b3-137">「 \_ \_ 開機時的硬體/bios/時間同步」 \_</span><span class="sxs-lookup"><span data-stu-id="763b3-137">"hardware/bios/time\_sync\_at\_boot"</span></span><br/>              | <span data-ttu-id="763b3-138">如果 VM CMOS 時鐘要在開機時與主機時鐘同步處理，則為 "true";否則為 "false"。</span><span class="sxs-lookup"><span data-stu-id="763b3-138">"true" if the VM CMOS clock is to be synchronized with the host clock at boot; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         | <span data-ttu-id="763b3-139">布林</span><span class="sxs-lookup"><span data-stu-id="763b3-139">"boolean"</span></span><br/> | <span data-ttu-id="763b3-140">"true"</span><span class="sxs-lookup"><span data-stu-id="763b3-140">"true"</span></span><br/> |
| <span data-ttu-id="763b3-141">"integration/microsoft/host \_ time \_ sync/enabled" "</span><span class="sxs-lookup"><span data-stu-id="763b3-141">"integration/microsoft/host\_time\_sync/enabled""</span></span><br/> | <span data-ttu-id="763b3-142">如果在整合元件中啟用主機時間同步處理，則為 "true";否則為 "false"。</span><span class="sxs-lookup"><span data-stu-id="763b3-142">"true" if host time synchronization is enabled in the integration components; "false" otherwise.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                          | <span data-ttu-id="763b3-143">布林</span><span class="sxs-lookup"><span data-stu-id="763b3-143">"boolean"</span></span><br/> | <span data-ttu-id="763b3-144">"true"</span><span class="sxs-lookup"><span data-stu-id="763b3-144">"true"</span></span><br/> |
| <span data-ttu-id="763b3-145">「ui \_ 選項/自動 \_ 應用程式 \_ 發佈」</span><span class="sxs-lookup"><span data-stu-id="763b3-145">"ui\_options/auto\_app\_publish"</span></span><br/>                  | <span data-ttu-id="763b3-146">如果整合元件中已啟用自動發行應用程式，則為 "true";否則為 "false"。</span><span class="sxs-lookup"><span data-stu-id="763b3-146">"true" if automatic publishing of applications is enabled in the integration components; "false" otherwise.</span></span> <span data-ttu-id="763b3-147">這也稱為虛擬應用程式。</span><span class="sxs-lookup"><span data-stu-id="763b3-147">This is also called virtual applications.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     | <span data-ttu-id="763b3-148">布林</span><span class="sxs-lookup"><span data-stu-id="763b3-148">"boolean"</span></span><br/> | <span data-ttu-id="763b3-149">"true"</span><span class="sxs-lookup"><span data-stu-id="763b3-149">"true"</span></span><br/> |
| <span data-ttu-id="763b3-150">「 \_ \_ 要儲存的 ui 選項/秒」 \_</span><span class="sxs-lookup"><span data-stu-id="763b3-150">"ui\_options/seconds\_to\_save"</span></span><br/>                   | <span data-ttu-id="763b3-151">關閉所有應用程式之後，儲存 VM 之前等候的秒數。</span><span class="sxs-lookup"><span data-stu-id="763b3-151">Number of seconds to wait before saving the VM after all applications are closed.</span></span> <span data-ttu-id="763b3-152">不過，低於20但超過4294968的值具有特殊意義。</span><span class="sxs-lookup"><span data-stu-id="763b3-152">However, values below 20 and more than 4,294,968 have special meanings.</span></span> <span data-ttu-id="763b3-153">如需詳細資訊，請參閱下列清單</span><span class="sxs-lookup"><span data-stu-id="763b3-153">For details, see the following list</span></span><br/> <dl> <span data-ttu-id="763b3-154"><dt><span id="0"></span>0</dt></span><span class="sxs-lookup"><span data-stu-id="763b3-154"><dt><span id="0"></span>0</dt></span></span> <dd> <span data-ttu-id="763b3-155">請勿儲存 VM。</span><span class="sxs-lookup"><span data-stu-id="763b3-155">Never save the VM.</span></span><br/> </dd> <span data-ttu-id="763b3-156"><dt><span id="120"></span>1 20</dt></span><span class="sxs-lookup"><span data-stu-id="763b3-156"><dt><span id="120"></span>1 20</dt></span></span> <dd> <span data-ttu-id="763b3-157">請等候20秒再儲存 VM。</span><span class="sxs-lookup"><span data-stu-id="763b3-157">Wait 20 seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="763b3-158"><dt><span id="214_294_967"></span>21 4294967</dt></span><span class="sxs-lookup"><span data-stu-id="763b3-158"><dt><span id="214_294_967"></span>21 4,294,967</dt></span></span> <dd> <span data-ttu-id="763b3-159">請等候指定的秒數，然後再儲存 VM。</span><span class="sxs-lookup"><span data-stu-id="763b3-159">Wait the specified number of seconds before saving the VM.</span></span><br/> </dd> <span data-ttu-id="763b3-160"><dt><span id="4_294_9684_294_967_295"></span>4294968 4294967295</dt></span><span class="sxs-lookup"><span data-stu-id="763b3-160"><dt><span id="4_294_9684_294_967_295"></span>4,294,968 4,294,967,295</dt></span></span> <dd> <span data-ttu-id="763b3-161">請等候4294968秒，然後再儲存 VM。</span><span class="sxs-lookup"><span data-stu-id="763b3-161">Wait 4,294,968 seconds before saving the VM.</span></span><br/> </dd> </dl> | <span data-ttu-id="763b3-162">等效</span><span class="sxs-lookup"><span data-stu-id="763b3-162">"integer"</span></span><br/> | <span data-ttu-id="763b3-163">300</span><span class="sxs-lookup"><span data-stu-id="763b3-163">300</span></span><br/>    |



 

<span data-ttu-id="763b3-164">這個方法會提供任何設定值的低層級存取權。</span><span class="sxs-lookup"><span data-stu-id="763b3-164">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="763b3-165">可以用來設定客戶定義索引鍵的設定值。</span><span class="sxs-lookup"><span data-stu-id="763b3-165">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="763b3-166">如果您使用這個方法來設定系統組態值，請小心，因為設定值不會執行錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="763b3-166">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="763b3-167">此外，當虛擬機器正在執行時，某些設定值無法變更。</span><span class="sxs-lookup"><span data-stu-id="763b3-167">Also, some configuration values cannot be changed while the virtual machine is running.</span></span>

<span data-ttu-id="763b3-168">設定金鑰位於虛擬機器的 " \* . .vmc" 檔案中（XML 格式）。</span><span class="sxs-lookup"><span data-stu-id="763b3-168">Configuration keys are located in the virtual machine's "\*.vmc" file in XML format.</span></span> <span data-ttu-id="763b3-169">金鑰會以類似于 Windows 中登錄機碼的階層式方式儲存。</span><span class="sxs-lookup"><span data-stu-id="763b3-169">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="763b3-170">若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="763b3-170">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="763b3-171">例如，若要設定 \_ 位於下列金鑰樹狀結構中「ram 大小」機碼的值：</span><span class="sxs-lookup"><span data-stu-id="763b3-171">For example, to set the value of the "ram\_size" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <hardware>
    <bios>
      <time_sync_at_boot type="boolean">true</time_sync_at_boot>
```

<span data-ttu-id="763b3-172">*ConfigurationKey* 路徑字串的指定方式如下：</span><span class="sxs-lookup"><span data-stu-id="763b3-172">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"hardware/memory/ram_size"
```

<span data-ttu-id="763b3-173">如果所需樹狀結構中的任何索引鍵具有 "id" 屬性值，則屬性和其值會在其相關聯的設定金鑰之後，緊接在 *configurationKey* 路徑字串中，並使用下列括弧格式： " \[ @id ="*id \_ value*" \] "。</span><span class="sxs-lookup"><span data-stu-id="763b3-173">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *configurationKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="763b3-174">例如，若要設定位於下列金鑰樹狀結構中的 "高爾夫球" 索引鍵值：</span><span class="sxs-lookup"><span data-stu-id="763b3-174">For example, to set the value of the "golf" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <alpha>
    <bravo>
      <charlie>
        <delta id="1">
          <echo id="0">
            <foxtrot>
              <golf type="string">D</golf>
```

<span data-ttu-id="763b3-175">*ConfigurationKey* 路徑字串的指定方式如下：</span><span class="sxs-lookup"><span data-stu-id="763b3-175">The *configurationKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="763b3-176">規格需求</span><span class="sxs-lookup"><span data-stu-id="763b3-176">Requirements</span></span>



| <span data-ttu-id="763b3-177">需求</span><span class="sxs-lookup"><span data-stu-id="763b3-177">Requirement</span></span> | <span data-ttu-id="763b3-178">值</span><span class="sxs-lookup"><span data-stu-id="763b3-178">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="763b3-179">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="763b3-179">Minimum supported client</span></span><br/> | <span data-ttu-id="763b3-180">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="763b3-180">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="763b3-181">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="763b3-181">Minimum supported server</span></span><br/> | <span data-ttu-id="763b3-182">都不支援</span><span class="sxs-lookup"><span data-stu-id="763b3-182">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="763b3-183">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="763b3-183">End of client support</span></span><br/>    | <span data-ttu-id="763b3-184">Windows 7</span><span class="sxs-lookup"><span data-stu-id="763b3-184">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="763b3-185">產品</span><span class="sxs-lookup"><span data-stu-id="763b3-185">Product</span></span><br/>                  | <span data-ttu-id="763b3-186">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="763b3-186">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="763b3-187">標頭</span><span class="sxs-lookup"><span data-stu-id="763b3-187">Header</span></span><br/>                   | <dl> <span data-ttu-id="763b3-188"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="763b3-188"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="763b3-189">IID</span><span class="sxs-lookup"><span data-stu-id="763b3-189">IID</span></span><br/>                      | <span data-ttu-id="763b3-190">IID \_ IVMVirtualMachine 定義為 f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span><span class="sxs-lookup"><span data-stu-id="763b3-190">IID\_IVMVirtualMachine is defined as f7092aa1-33ed-4f78-a59f-c00adfc2edd7</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="763b3-191">另請參閱</span><span class="sxs-lookup"><span data-stu-id="763b3-191">See also</span></span>

<dl> <dt>

[<span data-ttu-id="763b3-192">**IVMVirtualMachine**</span><span class="sxs-lookup"><span data-stu-id="763b3-192">**IVMVirtualMachine**</span></span>](ivmvirtualmachine.md)
</dt> <dt>

[<span data-ttu-id="763b3-193">**IVMVirtualPC::SetConfigurationValue**</span><span class="sxs-lookup"><span data-stu-id="763b3-193">**IVMVirtualPC::SetConfigurationValue**</span></span>](ivmvirtualpc-setconfigurationvalue.md)
</dt> </dl>

 

