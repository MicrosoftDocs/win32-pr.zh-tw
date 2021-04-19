---
title: IMsRdpClientAdvancedSettings NumBitmapCaches 屬性
description: 不支援這個屬性。 |IMsRdpClientAdvancedSettings NumBitmapCaches 屬性
ms.assetid: a413b2c0-7661-415d-bc38-e8fd55006e8c
ms.tgt_platform: multiple
keywords:
- NumBitmapCaches 屬性遠端桌面服務
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，NumBitmapCaches 屬性
- NumBitmapCaches 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，NumBitmapCaches 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.NumBitmapCaches
- IMsRdpClientAdvancedSettings.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.NumBitmapCaches
- IMsRdpClientAdvancedSettings2.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings2.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.NumBitmapCaches
- IMsRdpClientAdvancedSettings3.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings3.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.NumBitmapCaches
- IMsRdpClientAdvancedSettings4.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings4.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.NumBitmapCaches
- IMsRdpClientAdvancedSettings5.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings5.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.NumBitmapCaches
- IMsRdpClientAdvancedSettings6.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings6.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.NumBitmapCaches
- IMsRdpClientAdvancedSettings7.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings7.put_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.NumBitmapCaches
- IMsRdpClientAdvancedSettings8.get_NumBitmapCaches
- IMsRdpClientAdvancedSettings8.put_NumBitmapCaches
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5ae60423287da041e3f84b28d8d51388e9a4050b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106976669"
---
# <a name="imsrdpclientadvancedsettingsnumbitmapcaches-property"></a><span data-ttu-id="5462e-121">IMsRdpClientAdvancedSettings：： NumBitmapCaches 屬性</span><span class="sxs-lookup"><span data-stu-id="5462e-121">IMsRdpClientAdvancedSettings::NumBitmapCaches property</span></span>

<span data-ttu-id="5462e-122">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="5462e-122">This property is not supported.</span></span>

<span data-ttu-id="5462e-123">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5462e-123">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5462e-124">Syntax</span><span class="sxs-lookup"><span data-stu-id="5462e-124">Syntax</span></span>


```C++
HRESULT put_NumBitmapCaches(
  [in]  LONG numBitmapCaches
);

HRESULT get_NumBitmapCaches(
  [out] LONG *pnumBitmapCaches
);
```



## <a name="property-value"></a><span data-ttu-id="5462e-125">屬性值</span><span class="sxs-lookup"><span data-stu-id="5462e-125">Property value</span></span>

<span data-ttu-id="5462e-126">新的快取數目。</span><span class="sxs-lookup"><span data-stu-id="5462e-126">The new number of caches.</span></span> <span data-ttu-id="5462e-127">預設值為3，這會產生最佳效能。</span><span class="sxs-lookup"><span data-stu-id="5462e-127">The default value is 3, which results in the best performance.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5462e-128">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5462e-128">Error codes</span></span>

<span data-ttu-id="5462e-129">傳回 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="5462e-129">Returns **S\_FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="5462e-130">備註</span><span class="sxs-lookup"><span data-stu-id="5462e-130">Remarks</span></span>

<span data-ttu-id="5462e-131">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="5462e-131">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5462e-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="5462e-132">Requirements</span></span>



| <span data-ttu-id="5462e-133">需求</span><span class="sxs-lookup"><span data-stu-id="5462e-133">Requirement</span></span> | <span data-ttu-id="5462e-134">值</span><span class="sxs-lookup"><span data-stu-id="5462e-134">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5462e-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5462e-135">Minimum supported client</span></span><br/> | <span data-ttu-id="5462e-136">都不支援</span><span class="sxs-lookup"><span data-stu-id="5462e-136">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="5462e-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5462e-137">Minimum supported server</span></span><br/> | <span data-ttu-id="5462e-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="5462e-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="5462e-139">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="5462e-139">End of client support</span></span><br/>    | <span data-ttu-id="5462e-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="5462e-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="5462e-141">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="5462e-141">End of server support</span></span><br/>    | <span data-ttu-id="5462e-142">都不支援</span><span class="sxs-lookup"><span data-stu-id="5462e-142">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="5462e-143">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5462e-143">Type library</span></span><br/>             | <dl> <span data-ttu-id="5462e-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5462e-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="5462e-145">DLL</span><span class="sxs-lookup"><span data-stu-id="5462e-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5462e-146"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5462e-146"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="5462e-147">IID</span><span class="sxs-lookup"><span data-stu-id="5462e-147">IID</span></span><br/>                      | <span data-ttu-id="5462e-148">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="5462e-148">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5462e-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5462e-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5462e-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="5462e-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="5462e-151">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="5462e-151">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="5462e-152">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="5462e-152">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="5462e-153">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="5462e-153">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="5462e-154">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="5462e-154">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="5462e-155">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="5462e-155">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="5462e-156">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="5462e-156">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="5462e-157">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="5462e-157">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





