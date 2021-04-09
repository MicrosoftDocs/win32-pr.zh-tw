---
title: IMsRdpClientAdvancedSettings2 CanAutoReconnect 屬性
description: 指定當網路連線中斷時，用戶端控制項是否能夠自動重新連接到目前的會話。
ms.assetid: 0a7ecf90-832b-4ec1-990b-7fe26ff134b1
ms.tgt_platform: multiple
keywords:
- CanAutoReconnect 屬性遠端桌面服務
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings2 介面
- IMsRdpClientAdvancedSettings2 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，CanAutoReconnect 屬性
- CanAutoReconnect 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，CanAutoReconnect 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings2.CanAutoReconnect
- IMsRdpClientAdvancedSettings2.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings3.CanAutoReconnect
- IMsRdpClientAdvancedSettings3.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings4.CanAutoReconnect
- IMsRdpClientAdvancedSettings4.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings5.CanAutoReconnect
- IMsRdpClientAdvancedSettings5.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings6.CanAutoReconnect
- IMsRdpClientAdvancedSettings6.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings7.CanAutoReconnect
- IMsRdpClientAdvancedSettings7.get_CanAutoReconnect
- IMsRdpClientAdvancedSettings8.CanAutoReconnect
- IMsRdpClientAdvancedSettings8.get_CanAutoReconnect
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0d8c8f4113c39b79783978252136c50d2111ed0c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843108"
---
# <a name="imsrdpclientadvancedsettings2canautoreconnect-property"></a><span data-ttu-id="62a81-118">IMsRdpClientAdvancedSettings2：： CanAutoReconnect 屬性</span><span class="sxs-lookup"><span data-stu-id="62a81-118">IMsRdpClientAdvancedSettings2::CanAutoReconnect property</span></span>

<span data-ttu-id="62a81-119">指定當網路連線中斷時，用戶端控制項是否能夠自動重新連接到目前的會話。</span><span class="sxs-lookup"><span data-stu-id="62a81-119">Specifies whether the client control is able to reconnect automatically to the current session in the event of a network disconnection.</span></span>

<span data-ttu-id="62a81-120">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="62a81-120">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="62a81-121">語法</span><span class="sxs-lookup"><span data-stu-id="62a81-121">Syntax</span></span>


```C++
HRESULT get_CanAutoReconnect(
  [out] VARIANT_BOOL *pfCanAutoReconnect
);
```



## <a name="property-value"></a><span data-ttu-id="62a81-122">屬性值</span><span class="sxs-lookup"><span data-stu-id="62a81-122">Property value</span></span>

<span data-ttu-id="62a81-123">如果控制項能夠自動重新連接， **則接收 variant \_ TRUE** ，否則會傳回 **variant \_ FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="62a81-123">Receives **VARIANT\_TRUE** if the control is able to automatically reconnect, and **VARIANT\_FALSE** otherwise.</span></span>

## <a name="error-codes"></a><span data-ttu-id="62a81-124">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="62a81-124">Error codes</span></span>

<span data-ttu-id="62a81-125">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="62a81-125">Return **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="62a81-126">備註</span><span class="sxs-lookup"><span data-stu-id="62a81-126">Remarks</span></span>

<span data-ttu-id="62a81-127">可能未啟用自動重新連線的情況包括：系統管理員使用群組原則來停用自動重新連線，以及不支援自動重新連接的舊版環境。</span><span class="sxs-lookup"><span data-stu-id="62a81-127">Situations in which automatic reconnection might not be enabled include those in which an administrator uses group policy to disable autoreconnection, and legacy environments that do not support automatic reconnection.</span></span>

<span data-ttu-id="62a81-128">連接控制項時，無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="62a81-128">This property cannot be set when the control is connected.</span></span>

<span data-ttu-id="62a81-129">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="62a81-129">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="62a81-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="62a81-130">Requirements</span></span>



| <span data-ttu-id="62a81-131">需求</span><span class="sxs-lookup"><span data-stu-id="62a81-131">Requirement</span></span> | <span data-ttu-id="62a81-132">值</span><span class="sxs-lookup"><span data-stu-id="62a81-132">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62a81-133">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="62a81-133">Minimum supported client</span></span><br/> | <span data-ttu-id="62a81-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="62a81-134">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="62a81-135">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="62a81-135">Minimum supported server</span></span><br/> | <span data-ttu-id="62a81-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="62a81-136">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="62a81-137">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="62a81-137">Type library</span></span><br/>             | <dl> <span data-ttu-id="62a81-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62a81-138"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="62a81-139">DLL</span><span class="sxs-lookup"><span data-stu-id="62a81-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62a81-140"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62a81-140"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="62a81-141">IID</span><span class="sxs-lookup"><span data-stu-id="62a81-141">IID</span></span><br/>                      | <span data-ttu-id="62a81-142">IID \_ IMsRdpClientAdvancedSettings2 定義為9ac42117-2b76-4320-aa44-0e616ab8437b</span><span class="sxs-lookup"><span data-stu-id="62a81-142">IID\_IMsRdpClientAdvancedSettings2 is defined as 9ac42117-2b76-4320-aa44-0e616ab8437b</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62a81-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62a81-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62a81-144">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="62a81-144">**IMsRdpClientAdvancedSettings3**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="62a81-145">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="62a81-145">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="62a81-146">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="62a81-146">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="62a81-147">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="62a81-147">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="62a81-148">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="62a81-148">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="62a81-149">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="62a81-149">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="62a81-150">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="62a81-150">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> </dl>

 

 





