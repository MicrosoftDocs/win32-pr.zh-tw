---
title: IMsRdpClientNonScriptable3 DeviceCollection 屬性
description: 抓取要重新導向的隨插即用 (PnP) 裝置物件的集合。
ms.assetid: dd5fe4c7-58bf-4e7a-b066-59278419ea6f
ms.tgt_platform: multiple
keywords:
- DeviceCollection 屬性遠端桌面服務
- DeviceCollection 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，DeviceCollection 屬性
- DeviceCollection 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，DeviceCollection 屬性
- DeviceCollection 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，DeviceCollection 屬性
- DeviceCollection 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、DeviceCollection 屬性
- DeviceCollection 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、DeviceCollection 屬性
- DeviceCollection 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、DeviceCollection 屬性
- DeviceCollection 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、DeviceCollection 屬性
- DeviceCollection 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、DeviceCollection 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DeviceCollection
- IMsRdpClientNonScriptable3.get_DeviceCollection
- IMsRdpClientNonScriptable4.DeviceCollection
- IMsRdpClientNonScriptable4.get_DeviceCollection
- IMsRdpClientNonScriptable5.DeviceCollection
- IMsRdpClientNonScriptable5.get_DeviceCollection
- MsRdpClient5.DeviceCollection
- MsRdpClient6.DeviceCollection
- MsRdpClient7.DeviceCollection
- MsRdpClient8.DeviceCollection
- MsRdpClient9.DeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a545d2f4aaae2af68c14dd6531a2c57cf73711dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384178"
---
# <a name="imsrdpclientnonscriptable3devicecollection-property"></a><span data-ttu-id="2c28d-120">IMsRdpClientNonScriptable3：:D eviceCollection 屬性</span><span class="sxs-lookup"><span data-stu-id="2c28d-120">IMsRdpClientNonScriptable3::DeviceCollection property</span></span>

<span data-ttu-id="2c28d-121">抓取要重新導向的隨插即用 (PnP) 裝置物件的集合。</span><span class="sxs-lookup"><span data-stu-id="2c28d-121">Retrieves the collection of Plug and Play (PnP) device objects to be redirected.</span></span>

<span data-ttu-id="2c28d-122">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="2c28d-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="2c28d-123">語法</span><span class="sxs-lookup"><span data-stu-id="2c28d-123">Syntax</span></span>


```C++
HRESULT get_DeviceCollection(
  [out] IMSRdpDeviceCollection **ppDeviceCollection
);
```



## <a name="property-value"></a><span data-ttu-id="2c28d-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="2c28d-124">Property value</span></span>

<span data-ttu-id="2c28d-125">抓取 [**IMSRdpDevice**](imsrdpdevice.md)類型之 PnP 裝置物件的集合。</span><span class="sxs-lookup"><span data-stu-id="2c28d-125">Retrieves the collection of PnP device objects of type [**IMSRdpDevice**](imsrdpdevice.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2c28d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c28d-126">Requirements</span></span>



| <span data-ttu-id="2c28d-127">需求</span><span class="sxs-lookup"><span data-stu-id="2c28d-127">Requirement</span></span> | <span data-ttu-id="2c28d-128">值</span><span class="sxs-lookup"><span data-stu-id="2c28d-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="2c28d-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c28d-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2c28d-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2c28d-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="2c28d-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c28d-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2c28d-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2c28d-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="2c28d-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="2c28d-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="2c28d-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c28d-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="2c28d-135">DLL</span><span class="sxs-lookup"><span data-stu-id="2c28d-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2c28d-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2c28d-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="2c28d-137">IID</span><span class="sxs-lookup"><span data-stu-id="2c28d-137">IID</span></span><br/>                      | <span data-ttu-id="2c28d-138">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="2c28d-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c28d-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c28d-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c28d-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="2c28d-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="2c28d-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="2c28d-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="2c28d-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="2c28d-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





