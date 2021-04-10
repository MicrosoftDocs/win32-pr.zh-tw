---
title: IMsRdpClientAdvancedSettings RDPPort 屬性
description: 指定連接通訊埠。
ms.assetid: 15be7ef8-8ed2-46e0-8cc5-d5cf1642b79e
ms.tgt_platform: multiple
keywords:
- RDPPort 屬性遠端桌面服務
- RDPPort 屬性遠端桌面服務，IMsRdpClientAdvancedSettings 介面
- IMsRdpClientAdvancedSettings 介面遠端桌面服務，RDPPort 屬性
- RDPPort 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，RDPPort 屬性
- RDPPort 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，RDPPort 屬性
- RDPPort 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，RDPPort 屬性
- RDPPort 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，RDPPort 屬性
- RDPPort 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，RDPPort 屬性
- RDPPort 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，RDPPort 屬性
- RDPPort 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，RDPPort 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings.RDPPort
- IMsRdpClientAdvancedSettings.get_RDPPort
- IMsRdpClientAdvancedSettings.put_RDPPort
- IMsRdpClientAdvancedSettings2.RDPPort
- IMsRdpClientAdvancedSettings2.get_RDPPort
- IMsRdpClientAdvancedSettings2.put_RDPPort
- IMsRdpClientAdvancedSettings3.RDPPort
- IMsRdpClientAdvancedSettings3.get_RDPPort
- IMsRdpClientAdvancedSettings3.put_RDPPort
- IMsRdpClientAdvancedSettings4.RDPPort
- IMsRdpClientAdvancedSettings4.get_RDPPort
- IMsRdpClientAdvancedSettings4.put_RDPPort
- IMsRdpClientAdvancedSettings5.RDPPort
- IMsRdpClientAdvancedSettings5.get_RDPPort
- IMsRdpClientAdvancedSettings5.put_RDPPort
- IMsRdpClientAdvancedSettings6.RDPPort
- IMsRdpClientAdvancedSettings6.get_RDPPort
- IMsRdpClientAdvancedSettings6.put_RDPPort
- IMsRdpClientAdvancedSettings7.RDPPort
- IMsRdpClientAdvancedSettings7.get_RDPPort
- IMsRdpClientAdvancedSettings7.put_RDPPort
- IMsRdpClientAdvancedSettings8.RDPPort
- IMsRdpClientAdvancedSettings8.get_RDPPort
- IMsRdpClientAdvancedSettings8.put_RDPPort
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c8eafb3521d6338a0a2d469c813ff7ffa447a20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106175"
---
# <a name="imsrdpclientadvancedsettingsrdpport-property"></a><span data-ttu-id="78386-120">IMsRdpClientAdvancedSettings：： RDPPort 屬性</span><span class="sxs-lookup"><span data-stu-id="78386-120">IMsRdpClientAdvancedSettings::RDPPort property</span></span>

<span data-ttu-id="78386-121">指定連接通訊埠。</span><span class="sxs-lookup"><span data-stu-id="78386-121">Specifies the connection port.</span></span>

<span data-ttu-id="78386-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="78386-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="78386-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="78386-123">Syntax</span></span>


```C++
HRESULT put_RDPPort(
  [in]  LONG rdpPort
);

HRESULT get_RDPPort(
  [out] LONG *prdpPort
);
```



## <a name="property-value"></a><span data-ttu-id="78386-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="78386-124">Property value</span></span>

<span data-ttu-id="78386-125">新的埠。</span><span class="sxs-lookup"><span data-stu-id="78386-125">The new port.</span></span> <span data-ttu-id="78386-126">預設值為3389。</span><span class="sxs-lookup"><span data-stu-id="78386-126">The default value is 3389.</span></span>

## <a name="error-codes"></a><span data-ttu-id="78386-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="78386-127">Error codes</span></span>

<span data-ttu-id="78386-128">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="78386-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="78386-129">備註</span><span class="sxs-lookup"><span data-stu-id="78386-129">Remarks</span></span>

<span data-ttu-id="78386-130">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="78386-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78386-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="78386-131">Requirements</span></span>



| <span data-ttu-id="78386-132">需求</span><span class="sxs-lookup"><span data-stu-id="78386-132">Requirement</span></span> | <span data-ttu-id="78386-133">值</span><span class="sxs-lookup"><span data-stu-id="78386-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78386-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78386-134">Minimum supported client</span></span><br/> | <span data-ttu-id="78386-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="78386-135">Windows Vista</span></span><br/>                                                                        |
| <span data-ttu-id="78386-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78386-136">Minimum supported server</span></span><br/> | <span data-ttu-id="78386-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="78386-137">Windows Server 2008</span></span><br/>                                                                  |
| <span data-ttu-id="78386-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="78386-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="78386-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78386-139"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="78386-140">DLL</span><span class="sxs-lookup"><span data-stu-id="78386-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78386-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="78386-141"><dt>MsTscAx.dll</dt></span></span> </dl>          |
| <span data-ttu-id="78386-142">IID</span><span class="sxs-lookup"><span data-stu-id="78386-142">IID</span></span><br/>                      | <span data-ttu-id="78386-143">IID \_ IMsRdpClientAdvancedSettings 定義為3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span><span class="sxs-lookup"><span data-stu-id="78386-143">IID\_IMsRdpClientAdvancedSettings is defined as 3c65b4ab-12b3-465b-acd4-b8dad3bff9e2</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="78386-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78386-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78386-145">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="78386-145">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="78386-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="78386-146">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="78386-147">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="78386-147">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="78386-148">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="78386-148">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="78386-149">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="78386-149">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="78386-150">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="78386-150">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="78386-151">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="78386-151">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="78386-152">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="78386-152">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> </dl>

 

 





