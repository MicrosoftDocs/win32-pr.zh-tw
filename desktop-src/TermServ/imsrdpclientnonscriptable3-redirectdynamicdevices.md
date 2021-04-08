---
title: IMsRdpClientNonScriptable3 RedirectDynamicDevices 屬性
description: 指定或抓取在會話中列舉的 PnP) 裝置上，是否有動態連接的隨插即用 (PnP 裝置可進行重新導向。
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- RedirectDynamicDevices 屬性遠端桌面服務
- RedirectDynamicDevices 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，RedirectDynamicDevices 屬性
- RedirectDynamicDevices 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，RedirectDynamicDevices 屬性
- RedirectDynamicDevices 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，RedirectDynamicDevices 屬性
- RedirectDynamicDevices 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、RedirectDynamicDevices 屬性
- RedirectDynamicDevices 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、RedirectDynamicDevices 屬性
- RedirectDynamicDevices 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、RedirectDynamicDevices 屬性
- RedirectDynamicDevices 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、RedirectDynamicDevices 屬性
- RedirectDynamicDevices 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、RedirectDynamicDevices 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685632"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a><span data-ttu-id="678d7-120">IMsRdpClientNonScriptable3：： RedirectDynamicDevices 屬性</span><span class="sxs-lookup"><span data-stu-id="678d7-120">IMsRdpClientNonScriptable3::RedirectDynamicDevices property</span></span>

<span data-ttu-id="678d7-121">指定或抓取在會話中列舉的 PnP) 裝置上，是否有動態連接的隨插即用 (PnP 裝置可進行重新導向。</span><span class="sxs-lookup"><span data-stu-id="678d7-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) devices that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="678d7-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="678d7-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="678d7-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="678d7-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a><span data-ttu-id="678d7-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="678d7-124">Property value</span></span>

<span data-ttu-id="678d7-125">指定是否可重新導向會話中所列舉的動態連接 PnP 裝置。</span><span class="sxs-lookup"><span data-stu-id="678d7-125">Specifies whether dynamically attached PnP devices that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="678d7-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="678d7-126">Requirements</span></span>



| <span data-ttu-id="678d7-127">需求</span><span class="sxs-lookup"><span data-stu-id="678d7-127">Requirement</span></span> | <span data-ttu-id="678d7-128">值</span><span class="sxs-lookup"><span data-stu-id="678d7-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="678d7-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="678d7-129">Minimum supported client</span></span><br/> | <span data-ttu-id="678d7-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="678d7-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="678d7-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="678d7-131">Minimum supported server</span></span><br/> | <span data-ttu-id="678d7-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="678d7-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="678d7-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="678d7-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="678d7-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="678d7-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="678d7-135">DLL</span><span class="sxs-lookup"><span data-stu-id="678d7-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="678d7-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="678d7-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="678d7-137">IID</span><span class="sxs-lookup"><span data-stu-id="678d7-137">IID</span></span><br/>                      | <span data-ttu-id="678d7-138">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="678d7-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="678d7-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="678d7-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="678d7-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="678d7-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="678d7-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="678d7-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="678d7-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="678d7-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





