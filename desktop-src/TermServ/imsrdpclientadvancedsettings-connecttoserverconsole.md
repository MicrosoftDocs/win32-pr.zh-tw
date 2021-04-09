---
title: IMsRdpClientAdvancedSettings ConnectToServerConsole 屬性
description: 不支援這個屬性。 對 ConnectToServerConsole 的呼叫一律會傳回 \_ FALSE。
ms.assetid: 58f79085-4364-408f-8bf1-97a82ad68f4b
ms.tgt_platform: multiple
keywords:
- ConnectToServerConsole 屬性遠端桌面服務
- ConnectToServerConsole 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，ConnectToServerConsole 屬性
- ConnectToServerConsole 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，ConnectToServerConsole 屬性
- ConnectToServerConsole 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，ConnectToServerConsole 屬性
- ConnectToServerConsole 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，ConnectToServerConsole 屬性
- ConnectToServerConsole 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，ConnectToServerConsole 屬性
- ConnectToServerConsole 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ConnectToServerConsole 屬性
- ConnectToServerConsole 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ConnectToServerConsole 屬性
- ConnectToServerConsole 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ConnectToServerConsole 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.ConnectToServerConsole
- IMsRdpClientAdvancedSettings.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings2.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings3.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings4.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings5.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings6.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings7.put_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.get_ConnectToServerConsole
- IMsRdpClientAdvancedSettings8.put_ConnectToServerConsole
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18e3385b25a9dbe3e77085ae011b85e9be21b224
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934298"
---
# <a name="imsrdpclientadvancedsettingsconnecttoserverconsole-property"></a><span data-ttu-id="e6a7b-121">IMsRdpClientAdvancedSettings：： ConnectToServerConsole 屬性</span><span class="sxs-lookup"><span data-stu-id="e6a7b-121">IMsRdpClientAdvancedSettings::ConnectToServerConsole property</span></span>

<span data-ttu-id="e6a7b-122">不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="e6a7b-122">This property is not supported.</span></span> <span data-ttu-id="e6a7b-123">對 **ConnectToServerConsole** 的呼叫一律會傳回 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e6a7b-123">Calls to **ConnectToServerConsole** always return **S\_FALSE**.</span></span>

<span data-ttu-id="e6a7b-124">使用 [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) 屬性連接到用於管理用途的會話。</span><span class="sxs-lookup"><span data-stu-id="e6a7b-124">Use the [**ConnectToAdministerServer**](imsrdpclientadvancedsettings6-connecttoadministerserver.md) property to connect to the session that is used for administrative purposes.</span></span>

<span data-ttu-id="e6a7b-125">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e6a7b-125">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6a7b-126">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6a7b-126">Syntax</span></span>


```C++
HRESULT put_ConnectToServerConsole(
  [in]  VARIANT_BOOL connectToServerConsole
);

HRESULT get_ConnectToServerConsole(
  [out] VARIANT_BOOL *pconnectToServerConsole
);
```



## <a name="property-value"></a><span data-ttu-id="e6a7b-127">屬性值</span><span class="sxs-lookup"><span data-stu-id="e6a7b-127">Property value</span></span>

<span data-ttu-id="e6a7b-128">將此參數設定為 **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e6a7b-128">Set this parameter to **VARIANT\_FALSE**.</span></span> <span data-ttu-id="e6a7b-129">**變異 \_** 不支援 TRUE。</span><span class="sxs-lookup"><span data-stu-id="e6a7b-129">**VARIANT\_TRUE** is not supported.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e6a7b-130">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e6a7b-130">Error codes</span></span>

<span data-ttu-id="e6a7b-131">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="e6a7b-131">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="e6a7b-132">備註</span><span class="sxs-lookup"><span data-stu-id="e6a7b-132">Remarks</span></span>

<span data-ttu-id="e6a7b-133">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="e6a7b-133">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6a7b-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="e6a7b-134">Requirements</span></span>



| <span data-ttu-id="e6a7b-135">需求</span><span class="sxs-lookup"><span data-stu-id="e6a7b-135">Requirement</span></span> | <span data-ttu-id="e6a7b-136">值</span><span class="sxs-lookup"><span data-stu-id="e6a7b-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6a7b-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e6a7b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e6a7b-138">都不支援</span><span class="sxs-lookup"><span data-stu-id="e6a7b-138">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="e6a7b-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e6a7b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e6a7b-140">都不支援</span><span class="sxs-lookup"><span data-stu-id="e6a7b-140">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="e6a7b-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e6a7b-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="e6a7b-142"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6a7b-142"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e6a7b-143">DLL</span><span class="sxs-lookup"><span data-stu-id="e6a7b-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6a7b-144"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6a7b-144"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="e6a7b-145">IID</span><span class="sxs-lookup"><span data-stu-id="e6a7b-145">IID</span></span><br/>                      | <span data-ttu-id="e6a7b-146">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="e6a7b-146">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e6a7b-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e6a7b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6a7b-148">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="e6a7b-148">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="e6a7b-149">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="e6a7b-149">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="e6a7b-150">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="e6a7b-150">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="e6a7b-151">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="e6a7b-151">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="e6a7b-152">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="e6a7b-152">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="e6a7b-153">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="e6a7b-153">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="e6a7b-154">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="e6a7b-154">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="e6a7b-155">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="e6a7b-155">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





