---
title: IMsRdpClientAdvancedSettings InputEventsAtOnce 屬性
description: 不支援這個屬性。 |IMsRdpClientAdvancedSettings InputEventsAtOnce 屬性
ms.assetid: 2f24b2cd-136d-4bde-9808-e5cb02bd7ce8
ms.tgt_platform: multiple
keywords:
- InputEventsAtOnce 屬性遠端桌面服務
- InputEventsAtOnce 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，InputEventsAtOnce 屬性
- InputEventsAtOnce 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，InputEventsAtOnce 屬性
- InputEventsAtOnce 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，InputEventsAtOnce 屬性
- InputEventsAtOnce 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，InputEventsAtOnce 屬性
- InputEventsAtOnce 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，InputEventsAtOnce 屬性
- InputEventsAtOnce 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，InputEventsAtOnce 屬性
- InputEventsAtOnce 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，InputEventsAtOnce 屬性
- InputEventsAtOnce 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，InputEventsAtOnce 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.InputEventsAtOnce
- IMsRdpClientAdvancedSettings.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings2.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings3.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings4.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings5.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings6.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings7.put_InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.get_InputEventsAtOnce
- IMsRdpClientAdvancedSettings8.put_InputEventsAtOnce
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 999d00cb706e4fdd4cf0c9ed606c33de4a81e8d6
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106981784"
---
# <a name="imsrdpclientadvancedsettingsinputeventsatonce-property"></a><span data-ttu-id="9c94d-121">IMsRdpClientAdvancedSettings：： InputEventsAtOnce 屬性</span><span class="sxs-lookup"><span data-stu-id="9c94d-121">IMsRdpClientAdvancedSettings::InputEventsAtOnce property</span></span>

<span data-ttu-id="9c94d-122">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="9c94d-122">This property is not supported.</span></span>

<span data-ttu-id="9c94d-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="9c94d-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c94d-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="9c94d-124">Syntax</span></span>


```C++
HRESULT put_InputEventsAtOnce(
  [in]  LONG inputEventsAtOnce
);

HRESULT get_InputEventsAtOnce(
  [out] LONG *pinputEventsAtOnce
);
```



## <a name="property-value"></a><span data-ttu-id="9c94d-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="9c94d-125">Property value</span></span>

<span data-ttu-id="9c94d-126">新的輸入事件數目。</span><span class="sxs-lookup"><span data-stu-id="9c94d-126">The new number of input events.</span></span> <span data-ttu-id="9c94d-127">預設值為 10。</span><span class="sxs-lookup"><span data-stu-id="9c94d-127">The default is 10.</span></span>

## <a name="error-codes"></a><span data-ttu-id="9c94d-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="9c94d-128">Error codes</span></span>

<span data-ttu-id="9c94d-129">傳回 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="9c94d-129">Returns **S\_FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="9c94d-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="9c94d-130">Requirements</span></span>



| <span data-ttu-id="9c94d-131">需求</span><span class="sxs-lookup"><span data-stu-id="9c94d-131">Requirement</span></span> | <span data-ttu-id="9c94d-132">值</span><span class="sxs-lookup"><span data-stu-id="9c94d-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9c94d-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9c94d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="9c94d-134">都不支援</span><span class="sxs-lookup"><span data-stu-id="9c94d-134">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9c94d-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9c94d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="9c94d-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="9c94d-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9c94d-137">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9c94d-137">End of client support</span></span><br/>    | <span data-ttu-id="9c94d-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="9c94d-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9c94d-139">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9c94d-139">End of server support</span></span><br/>    | <span data-ttu-id="9c94d-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="9c94d-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="9c94d-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9c94d-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="9c94d-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c94d-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9c94d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="9c94d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9c94d-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9c94d-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="9c94d-145">IID</span><span class="sxs-lookup"><span data-stu-id="9c94d-145">IID</span></span><br/>                      | <span data-ttu-id="9c94d-146">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="9c94d-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="9c94d-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9c94d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9c94d-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="9c94d-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="9c94d-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="9c94d-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="9c94d-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="9c94d-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="9c94d-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="9c94d-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="9c94d-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="9c94d-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="9c94d-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="9c94d-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="9c94d-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="9c94d-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="9c94d-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="9c94d-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





