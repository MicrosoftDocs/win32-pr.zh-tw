---
title: 'IVMVirtualPC SetConfigurationValue 方法 (VPCCOMInterfaces .h) '
description: 設定指定之設定的值。
ms.assetid: 7760b81e-734d-4970-8875-f2d310ff6c5c
keywords:
- SetConfigurationValue 方法 Virtual PC
- SetConfigurationValue 方法 Virtual PC，IVMVirtualPC 介面
- IVMVirtualPC 介面 Virtual PC，SetConfigurationValue 方法
topic_type:
- apiref
api_name:
- IVMVirtualPC.SetConfigurationValue
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecb8ff3bb68829e944461cedb1c86904c7150593
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509035"
---
# <a name="ivmvirtualpcsetconfigurationvalue-method"></a><span data-ttu-id="5ab52-106">IVMVirtualPC：： SetConfigurationValue 方法</span><span class="sxs-lookup"><span data-stu-id="5ab52-106">IVMVirtualPC::SetConfigurationValue method</span></span>

<span data-ttu-id="5ab52-107">\[Windows 8 不能再使用 Windows Virtual PC。</span><span class="sxs-lookup"><span data-stu-id="5ab52-107">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="5ab52-108">請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]</span><span class="sxs-lookup"><span data-stu-id="5ab52-108">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="5ab52-109">設定指定之設定的值。</span><span class="sxs-lookup"><span data-stu-id="5ab52-109">Sets the value of the specified configuration setting.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ab52-110">語法</span><span class="sxs-lookup"><span data-stu-id="5ab52-110">Syntax</span></span>


```C++
HRESULT SetConfigurationValue(
  [in] BSTR    preferenceKey,
  [in] VARIANT preferenceValue
);
```



## <a name="parameters"></a><span data-ttu-id="5ab52-111">參數</span><span class="sxs-lookup"><span data-stu-id="5ab52-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ab52-112">*preferenceKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ab52-112">*preferenceKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab52-113">用來識別喜好設定的金鑰，會儲存在每個使用者的設定檔中， (Options.xml 于 "% LocalAppData% \\ Microsoft \\ WINDOWS Virtual PC" ) 。</span><span class="sxs-lookup"><span data-stu-id="5ab52-113">The key used to identify the preference, as stored in the per-user configuration file (Options.xml in "%LocalAppData%\\Microsoft\\Windows Virtual PC").</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5ab52-114">Options.xml 只能使用 **SetConfigurationValue** 方法進行變更。</span><span class="sxs-lookup"><span data-stu-id="5ab52-114">Changes should be made to Options.xml only using the **SetConfigurationValue** method.</span></span> <span data-ttu-id="5ab52-115">不支援使用任何其他方法來變更 Options.xml。</span><span class="sxs-lookup"><span data-stu-id="5ab52-115">Changing Options.xml using any other method is not supported.</span></span>

 

</dd> <dt>

<span data-ttu-id="5ab52-116">*preferenceValue* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5ab52-116">*preferenceValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ab52-117">喜好設定值。</span><span class="sxs-lookup"><span data-stu-id="5ab52-117">The preference value.</span></span> <span data-ttu-id="5ab52-118">這個值可以是下列其中一個 **VARIANT** 類型： **vt \_ ARRAY** \| **vt \_ UI1** (原始位元組) 、 **vt \_ BSTR** (string) 、 **vt \_ UI4** (整數) 或 **vt \_ BOOL** (布林值) 。</span><span class="sxs-lookup"><span data-stu-id="5ab52-118">This value may be one of the following **VARIANT** types: **VT\_ARRAY**\|**VT\_UI1** (raw bytes), **VT\_BSTR** (string), **VT\_UI4** (integer), or **VT\_BOOL** (Boolean).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ab52-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="5ab52-119">Return value</span></span>

<span data-ttu-id="5ab52-120">這個方法可以傳回其中一個值。</span><span class="sxs-lookup"><span data-stu-id="5ab52-120">This method can return one of these values.</span></span>



| <span data-ttu-id="5ab52-121">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="5ab52-121">Return code/value</span></span>                                                                                                                                                                        | <span data-ttu-id="5ab52-122">Description</span><span class="sxs-lookup"><span data-stu-id="5ab52-122">Description</span></span>                                                                                     |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="5ab52-123"><dt>**S \_確定**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="5ab52-123"><dt>**S\_OK**</dt> <dt>0</dt></span></span> </dl>                                              | <span data-ttu-id="5ab52-124">作業成功。</span><span class="sxs-lookup"><span data-stu-id="5ab52-124">The operation was successful.</span></span><br/>                                                        |
| <dl> <span data-ttu-id="5ab52-125"><dt>**E \_指標**</dt><dt>且顯示 0x80004003</dt></span><span class="sxs-lookup"><span data-stu-id="5ab52-125"><dt>**E\_POINTER**</dt> <dt>0x80004003</dt></span></span> </dl>                                | <span data-ttu-id="5ab52-126">*PreferenceKey* 或 *PreferenceValue* 參數為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5ab52-126">The *preferenceKey* or *preferenceValue* parameter is **NULL**.</span></span><br/>                      |
| <dl> <span data-ttu-id="5ab52-127"><dt>**E \_INVALIDARG**</dt> <dt>0x80000003</dt></span><span class="sxs-lookup"><span data-stu-id="5ab52-127"><dt>**E\_INVALIDARG**</dt> <dt>0x80000003</dt></span></span> </dl>                             | <span data-ttu-id="5ab52-128">*PreferenceKey* 參數無效或為空字串。</span><span class="sxs-lookup"><span data-stu-id="5ab52-128">The *preferenceKey* parameter is not valid or is an empty string.</span></span><br/>                    |
| <dl> <span data-ttu-id="5ab52-129"><dt>**會 \_E \_ 例外**</dt>狀況 <dt>0x80020009</dt></span><span class="sxs-lookup"><span data-stu-id="5ab52-129"><dt>**DISP\_E\_EXCEPTION**</dt> <dt>0x80020009</dt></span></span> </dl>                        | <span data-ttu-id="5ab52-130">已發生未預期的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5ab52-130">An unexpected error has occurred.</span></span><br/>                                                    |
| <dl> <span data-ttu-id="5ab52-131"><dt>**E \_ACCESSDENIED**</dt> <dt>0x80070005</dt></span><span class="sxs-lookup"><span data-stu-id="5ab52-131"><dt>**E\_ACCESSDENIED**</dt> <dt>0x80070005</dt></span></span> </dl>                           | <span data-ttu-id="5ab52-132">目前的使用者沒有設定檔的足夠存取權。</span><span class="sxs-lookup"><span data-stu-id="5ab52-132">The current user has insufficient access to the configuration file.</span></span><br/>                  |
| <dl> <span data-ttu-id="5ab52-133"><dt>**VM \_E \_ 硬體 \_ 虛擬化 \_ 已停用**</dt> <dt>0xA0040951</dt></span><span class="sxs-lookup"><span data-stu-id="5ab52-133"><dt>**VM\_E\_HARDWARE\_VIRTUALIZATION\_DISABLED**</dt> <dt>0xA0040951</dt></span></span> </dl> | <span data-ttu-id="5ab52-134">處理器不支援硬體加速虛擬化 (包含老舊) 擴充功能。</span><span class="sxs-lookup"><span data-stu-id="5ab52-134">The processor does not support Hardware Accelerated Virtualization (HAV) extensions.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ab52-135">備註</span><span class="sxs-lookup"><span data-stu-id="5ab52-135">Remarks</span></span>

<span data-ttu-id="5ab52-136">*PreferenceKey* 參數支援下列值。</span><span class="sxs-lookup"><span data-stu-id="5ab52-136">The following values are supported for the *preferenceKey* parameter.</span></span>



| <span data-ttu-id="5ab52-137">*preferenceKey* 值</span><span class="sxs-lookup"><span data-stu-id="5ab52-137">*preferenceKey* value</span></span>      | <span data-ttu-id="5ab52-138">Description</span><span class="sxs-lookup"><span data-stu-id="5ab52-138">Description</span></span>                                                                                                                                                                           | <span data-ttu-id="5ab52-139">資料類型</span><span class="sxs-lookup"><span data-stu-id="5ab52-139">Data type</span></span>            | <span data-ttu-id="5ab52-140">預設值</span><span class="sxs-lookup"><span data-stu-id="5ab52-140">Default value</span></span>   |
|----------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------|-----------------|
| <span data-ttu-id="5ab52-141">「閒置 \_ timeout」</span><span class="sxs-lookup"><span data-stu-id="5ab52-141">"idle\_timeout"</span></span><br/> | <span data-ttu-id="5ab52-142">如果沒有作用中的 Vm 或應用程式正在使用 [Windows VIRTUAL PC 介面](virtual-pc-interfaces.md)，vpc.exe 應等候的秒數。</span><span class="sxs-lookup"><span data-stu-id="5ab52-142">Number of seconds that vpc.exe should wait before exiting if there are no active VMs or applications using the [Windows Virtual PC Interfaces](virtual-pc-interfaces.md).</span></span><br/> | <span data-ttu-id="5ab52-143">等效</span><span class="sxs-lookup"><span data-stu-id="5ab52-143">"integer"</span></span><br/> | <span data-ttu-id="5ab52-144">30</span><span class="sxs-lookup"><span data-stu-id="5ab52-144">"30"</span></span><br/> |



 

<span data-ttu-id="5ab52-145">這個方法會提供任何設定值的低層級存取權。</span><span class="sxs-lookup"><span data-stu-id="5ab52-145">This method provides low-level access to any configuration value.</span></span> <span data-ttu-id="5ab52-146">可以用來設定客戶定義索引鍵的設定值。</span><span class="sxs-lookup"><span data-stu-id="5ab52-146">It can be used to set configuration values for customer-defined keys.</span></span> <span data-ttu-id="5ab52-147">如果您使用這個方法來設定系統組態值，請小心，因為設定值不會執行錯誤檢查。</span><span class="sxs-lookup"><span data-stu-id="5ab52-147">Be careful if you use this method to set system configuration values, because no error checking is performed on the configuration value.</span></span> <span data-ttu-id="5ab52-148">此外，當虛擬機器正在執行時，某些設定值無法變更。</span><span class="sxs-lookup"><span data-stu-id="5ab52-148">Also, some configuration values cannot be changed while a virtual machine is running.</span></span>

<span data-ttu-id="5ab52-149">設定金鑰位於虛擬機器的「Options.xml」檔案中（XML 格式）。</span><span class="sxs-lookup"><span data-stu-id="5ab52-149">Configuration keys are located in the virtual machine's "Options.xml" file in XML format.</span></span> <span data-ttu-id="5ab52-150">金鑰會以類似于 Windows 中登錄機碼的階層式方式儲存。</span><span class="sxs-lookup"><span data-stu-id="5ab52-150">The keys are stored in a hierarchical manner similar to the registry keys in Windows.</span></span> <span data-ttu-id="5ab52-151">若要指定特定的子機碼，會使用「金鑰路徑」來建立，並以斜線標記分隔格式來指定不同的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="5ab52-151">To specify a specific subkey, a "key path" is constructed which specifies the various keys in a slash mark delimited format.</span></span>

<span data-ttu-id="5ab52-152">例如，若要設定 \_ 位於下列金鑰樹狀結構中的「閒置 timeout」機碼值：</span><span class="sxs-lookup"><span data-stu-id="5ab52-152">For example, to set the value of the "idle\_timeout" key located in the following key tree:</span></span>

``` syntax
<preferences>
  <idle_timeout type="integer">60</idle_timeout>
```

<span data-ttu-id="5ab52-153">*PreferenceKey* 路徑字串的指定方式如下：</span><span class="sxs-lookup"><span data-stu-id="5ab52-153">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"idle_timeout"
```

<span data-ttu-id="5ab52-154">如果所需樹狀結構中的任何索引鍵具有 "id" 屬性值，則屬性和其值會在其相關聯的設定金鑰之後，緊接在 *preferenceKey* 路徑字串中，並使用下列括弧格式： " \[ @id ="*id \_ value*" \] "。</span><span class="sxs-lookup"><span data-stu-id="5ab52-154">If any of the keys in the desired tree have an "id" attribute value, the attribute and its value is embedded in the *preferenceKey* path string immediately after its associated configuration key using the following bracketed format: "\[@id="*id\_value*"\]".</span></span>

<span data-ttu-id="5ab52-155">例如，若要設定位於下列金鑰樹狀結構中的 "高爾夫球" 索引鍵值：</span><span class="sxs-lookup"><span data-stu-id="5ab52-155">For example, to set the value of the "golf" key located in the following key tree:</span></span>

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

<span data-ttu-id="5ab52-156">*PreferenceKey* 路徑字串的指定方式如下：</span><span class="sxs-lookup"><span data-stu-id="5ab52-156">The *preferenceKey* path string would be specified as follows:</span></span>

``` syntax
"alpha/bravo/charlie/delta[@id=1]/echo[@id=0]/foxtrot/golf"
```

## <a name="requirements"></a><span data-ttu-id="5ab52-157">規格需求</span><span class="sxs-lookup"><span data-stu-id="5ab52-157">Requirements</span></span>



| <span data-ttu-id="5ab52-158">需求</span><span class="sxs-lookup"><span data-stu-id="5ab52-158">Requirement</span></span> | <span data-ttu-id="5ab52-159">值</span><span class="sxs-lookup"><span data-stu-id="5ab52-159">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ab52-160">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5ab52-160">Minimum supported client</span></span><br/> | <span data-ttu-id="5ab52-161">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5ab52-161">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5ab52-162">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5ab52-162">Minimum supported server</span></span><br/> | <span data-ttu-id="5ab52-163">都不支援</span><span class="sxs-lookup"><span data-stu-id="5ab52-163">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="5ab52-164">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5ab52-164">End of client support</span></span><br/>    | <span data-ttu-id="5ab52-165">Windows 7</span><span class="sxs-lookup"><span data-stu-id="5ab52-165">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="5ab52-166">產品</span><span class="sxs-lookup"><span data-stu-id="5ab52-166">Product</span></span><br/>                  | <span data-ttu-id="5ab52-167">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="5ab52-167">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="5ab52-168">標頭</span><span class="sxs-lookup"><span data-stu-id="5ab52-168">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ab52-169"><dt>VPCCOMInterfaces。h</dt></span><span class="sxs-lookup"><span data-stu-id="5ab52-169"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |
| <span data-ttu-id="5ab52-170">IID</span><span class="sxs-lookup"><span data-stu-id="5ab52-170">IID</span></span><br/>                      | <span data-ttu-id="5ab52-171">IID \_ IVMVirtualPC 定義為 236ba0d9-a24a-4292-a132-27c1421dfd01</span><span class="sxs-lookup"><span data-stu-id="5ab52-171">IID\_IVMVirtualPC is defined as 236ba0d9-a24a-4292-a132-27c1421dfd01</span></span><br/>               |



## <a name="see-also"></a><span data-ttu-id="5ab52-172">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5ab52-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ab52-173">**IVMVirtualPC**</span><span class="sxs-lookup"><span data-stu-id="5ab52-173">**IVMVirtualPC**</span></span>](ivmvirtualpc.md)
</dt> <dt>

[<span data-ttu-id="5ab52-174">**IVMVirtualMachine::SetConfigurationValue**</span><span class="sxs-lookup"><span data-stu-id="5ab52-174">**IVMVirtualMachine::SetConfigurationValue**</span></span>](ivmvirtualmachine-setconfigurationvalue.md)
</dt> </dl>

 

