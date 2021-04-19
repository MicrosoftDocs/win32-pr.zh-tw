---
title: IMsRdpClientAdvancedSettings DedicatedTerminal 屬性
description: 不支援這個屬性。 |IMsRdpClientAdvancedSettings DedicatedTerminal 屬性
ms.assetid: 40d54c88-dcac-4e7d-b389-a65caeb6960e
ms.tgt_platform: multiple
keywords:
- DedicatedTerminal 屬性遠端桌面服務
- DedicatedTerminal 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，DedicatedTerminal 屬性
- DedicatedTerminal 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，DedicatedTerminal 屬性
- DedicatedTerminal 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，DedicatedTerminal 屬性
- DedicatedTerminal 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，DedicatedTerminal 屬性
- DedicatedTerminal 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，DedicatedTerminal 屬性
- DedicatedTerminal 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，DedicatedTerminal 屬性
- DedicatedTerminal 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，DedicatedTerminal 屬性
- DedicatedTerminal 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，DedicatedTerminal 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.DedicatedTerminal
- IMsRdpClientAdvancedSettings.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings2.DedicatedTerminal
- IMsRdpClientAdvancedSettings2.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings2.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings3.DedicatedTerminal
- IMsRdpClientAdvancedSettings3.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings3.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings4.DedicatedTerminal
- IMsRdpClientAdvancedSettings4.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings4.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings5.DedicatedTerminal
- IMsRdpClientAdvancedSettings5.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings5.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings6.DedicatedTerminal
- IMsRdpClientAdvancedSettings6.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings6.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings7.DedicatedTerminal
- IMsRdpClientAdvancedSettings7.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings7.put_DedicatedTerminal
- IMsRdpClientAdvancedSettings8.DedicatedTerminal
- IMsRdpClientAdvancedSettings8.get_DedicatedTerminal
- IMsRdpClientAdvancedSettings8.put_DedicatedTerminal
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee005439b38e21c5ed05d035545cc5600993cd5c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106992685"
---
# <a name="imsrdpclientadvancedsettingsdedicatedterminal-property"></a><span data-ttu-id="bc2af-121">IMsRdpClientAdvancedSettings：:D edicatedTerminal 屬性</span><span class="sxs-lookup"><span data-stu-id="bc2af-121">IMsRdpClientAdvancedSettings::DedicatedTerminal property</span></span>

<span data-ttu-id="bc2af-122">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="bc2af-122">This property is not supported.</span></span>

<span data-ttu-id="bc2af-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bc2af-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc2af-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="bc2af-124">Syntax</span></span>


```C++
HRESULT put_DedicatedTerminal(
  [in]  LONG dedicatedTerminal
);

HRESULT get_DedicatedTerminal(
  [out] LONG *pdedicatedTerminal
);
```



## <a name="property-value"></a><span data-ttu-id="bc2af-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="bc2af-125">Property value</span></span>

<span data-ttu-id="bc2af-126">將此參數設定為0，以停用此功能或非零值以啟用此功能。</span><span class="sxs-lookup"><span data-stu-id="bc2af-126">Set this parameter to 0 to disable the feature or a nonzero value to enable the feature.</span></span>

## <a name="error-codes"></a><span data-ttu-id="bc2af-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="bc2af-127">Error codes</span></span>

<span data-ttu-id="bc2af-128">傳回 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="bc2af-128">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc2af-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="bc2af-129">Requirements</span></span>



| <span data-ttu-id="bc2af-130">需求</span><span class="sxs-lookup"><span data-stu-id="bc2af-130">Requirement</span></span> | <span data-ttu-id="bc2af-131">值</span><span class="sxs-lookup"><span data-stu-id="bc2af-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc2af-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bc2af-132">Minimum supported client</span></span><br/> | <span data-ttu-id="bc2af-133">都不支援</span><span class="sxs-lookup"><span data-stu-id="bc2af-133">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="bc2af-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bc2af-134">Minimum supported server</span></span><br/> | <span data-ttu-id="bc2af-135">都不支援</span><span class="sxs-lookup"><span data-stu-id="bc2af-135">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="bc2af-136">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="bc2af-136">End of client support</span></span><br/>    | <span data-ttu-id="bc2af-137">都不支援</span><span class="sxs-lookup"><span data-stu-id="bc2af-137">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="bc2af-138">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="bc2af-138">End of server support</span></span><br/>    | <span data-ttu-id="bc2af-139">都不支援</span><span class="sxs-lookup"><span data-stu-id="bc2af-139">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="bc2af-140">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bc2af-140">Type library</span></span><br/>             | <dl> <span data-ttu-id="bc2af-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc2af-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="bc2af-142">DLL</span><span class="sxs-lookup"><span data-stu-id="bc2af-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bc2af-143"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bc2af-143"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="bc2af-144">IID</span><span class="sxs-lookup"><span data-stu-id="bc2af-144">IID</span></span><br/>                      | <span data-ttu-id="bc2af-145">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="bc2af-145">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bc2af-146">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bc2af-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc2af-147">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="bc2af-147">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="bc2af-148">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="bc2af-148">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="bc2af-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="bc2af-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="bc2af-150">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bc2af-150">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="bc2af-151">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bc2af-151">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bc2af-152">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bc2af-152">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bc2af-153">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bc2af-153">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bc2af-154">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="bc2af-154">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





