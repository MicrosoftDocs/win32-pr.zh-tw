---
title: IMsRdpClientAdvancedSettings LoadBalanceInfo 屬性
description: 指定將放置在遠端桌面工作階段主機 (RD 工作階段主機) server 通訊協定連接順序中的 x.500 連接要求封包中的負載平衡 cookie。
ms.assetid: 25f12a2e-00a2-42a8-afd3-81efcd94da94
ms.tgt_platform: multiple
keywords:
- LoadBalanceInfo 屬性遠端桌面服務
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，LoadBalanceInfo 屬性
- LoadBalanceInfo 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，LoadBalanceInfo 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.LoadBalanceInfo
- IMsRdpClientAdvancedSettings.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings2.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings3.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings4.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings5.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings6.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings7.put_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.get_LoadBalanceInfo
- IMsRdpClientAdvancedSettings8.put_LoadBalanceInfo
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a12112eb2a18d38993e905f8d36175f1ab15f58a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384309"
---
# <a name="imsrdpclientadvancedsettingsloadbalanceinfo-property"></a><span data-ttu-id="a8e8c-120">IMsRdpClientAdvancedSettings：： LoadBalanceInfo 屬性</span><span class="sxs-lookup"><span data-stu-id="a8e8c-120">IMsRdpClientAdvancedSettings::LoadBalanceInfo property</span></span>

<span data-ttu-id="a8e8c-121">指定將放置在遠端桌面工作階段主機 (RD 工作階段主機) server 通訊協定連接順序中的 x.500 連接要求封包中的負載平衡 cookie。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-121">Specifies the load balancing cookie that will be placed in the X.224 Connection Request packet in the Remote Desktop Session Host (RD Session Host) server protocol connection sequence.</span></span>

<span data-ttu-id="a8e8c-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8e8c-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="a8e8c-123">Syntax</span></span>


```C++
HRESULT put_LoadBalanceInfo(
  [in]  BSTR newLBInfo
);

HRESULT get_LoadBalanceInfo(
  [out] BSTR *pLBInfo
);
```



## <a name="property-value"></a><span data-ttu-id="a8e8c-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="a8e8c-124">Property value</span></span>

<span data-ttu-id="a8e8c-125">新 cookie 的指標。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-125">Pointer to the new cookie.</span></span> <span data-ttu-id="a8e8c-126">如需詳細資訊，請參閱「備註」一節。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-126">For more information, see the remarks section.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a8e8c-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a8e8c-127">Error codes</span></span>

<span data-ttu-id="a8e8c-128">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="a8e8c-129">備註</span><span class="sxs-lookup"><span data-stu-id="a8e8c-129">Remarks</span></span>

<span data-ttu-id="a8e8c-130">負載平衡路由器會使用負載平衡資訊，在使用 RD 工作階段主機伺服器的伺服器陣列時，為用戶端選擇最佳的伺服器。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-130">The load balancing information is used by load balancing routers to choose the best server for the client when using farms of RD Session Host servers.</span></span> <span data-ttu-id="a8e8c-131">RD 工作階段主機伺服器本身並不會使用此資訊，而且會捨棄它。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-131">The RD Session Host server itself does not use this information and will discard it.</span></span>

<span data-ttu-id="a8e8c-132">Cookie 會使用下列區分大小寫的語法：</span><span class="sxs-lookup"><span data-stu-id="a8e8c-132">The cookie uses the following, case-sensitive, syntax:</span></span>

<span data-ttu-id="a8e8c-133">**Cookie： msts =**_IpAddressAndPortNumber_ *_\\ r \\ n_*</span><span class="sxs-lookup"><span data-stu-id="a8e8c-133">**Cookie: msts=**_IpAddressAndPortNumber_*_\\r\\n_*</span></span>

<span data-ttu-id="a8e8c-134">其中 *IpAddressAndPortNumber* 是 IP 位址和埠號碼（以網路位元組順序排列）。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-134">Where *IpAddressAndPortNumber* is the IP address and port number, in network byte order.</span></span>

<span data-ttu-id="a8e8c-135">例如，用來存取 172.31.249.216 IP 位址的 cookie （埠號碼3389）如下所示：</span><span class="sxs-lookup"><span data-stu-id="a8e8c-135">For example, the cookie used to access the IP address of 172.31.249.216, port number 3389 is as follows:</span></span>

<span data-ttu-id="a8e8c-136">**Cookie： msts = 3640205228.15629.0000 \\ r \\ n**</span><span class="sxs-lookup"><span data-stu-id="a8e8c-136">**Cookie: msts=3640205228.15629.0000\\r\\n**</span></span>

<span data-ttu-id="a8e8c-137">最後四個零是選擇性的，並保留。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-137">The final four zeros are optional and are reserved.</span></span> <span data-ttu-id="a8e8c-138">最後一個小數點是必要的，如同尾端的回車和換行。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-138">The final decimal point is required, as are the trailing carriage return and linefeed.</span></span> <span data-ttu-id="a8e8c-139">字串的長度（以字元為單位）必須是2的偶數倍數，因此如有需要，請加上空格。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-139">The length of the string, in characters, must be an even multiple of 2, so add a space if necessary.</span></span>

<span data-ttu-id="a8e8c-140">如果未提供 cookie，預設值為 **cookie： mstshash =**_UserName_ *_\\ r \\ n_*。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-140">If no cookie is supplied, the default is **Cookie: mstshash=**_UserName_*_\\r\\n_*.</span></span>

<span data-ttu-id="a8e8c-141">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="a8e8c-141">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="a8e8c-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="a8e8c-142">Requirements</span></span>



| <span data-ttu-id="a8e8c-143">需求</span><span class="sxs-lookup"><span data-stu-id="a8e8c-143">Requirement</span></span> | <span data-ttu-id="a8e8c-144">值</span><span class="sxs-lookup"><span data-stu-id="a8e8c-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8e8c-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a8e8c-145">Minimum supported client</span></span><br/> | <span data-ttu-id="a8e8c-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a8e8c-146">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="a8e8c-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a8e8c-147">Minimum supported server</span></span><br/> | <span data-ttu-id="a8e8c-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a8e8c-148">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="a8e8c-149">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a8e8c-149">Type library</span></span><br/>             | <dl> <span data-ttu-id="a8e8c-150"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8e8c-150"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a8e8c-151">DLL</span><span class="sxs-lookup"><span data-stu-id="a8e8c-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8e8c-152"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8e8c-152"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="a8e8c-153">IID</span><span class="sxs-lookup"><span data-stu-id="a8e8c-153">IID</span></span><br/>                      | <span data-ttu-id="a8e8c-154">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="a8e8c-154">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a8e8c-155">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a8e8c-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a8e8c-156">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="a8e8c-156">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="a8e8c-157">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="a8e8c-157">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="a8e8c-158">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="a8e8c-158">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="a8e8c-159">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="a8e8c-159">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="a8e8c-160">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="a8e8c-160">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="a8e8c-161">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="a8e8c-161">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="a8e8c-162">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="a8e8c-162">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="a8e8c-163">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="a8e8c-163">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





