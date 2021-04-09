---
title: IMsRdpClientNonScriptable3 RedirectDynamicDrives 屬性
description: 指定或抓取是否可重新導向會話中所列舉的隨插即用 (PnP) 磁片磁碟機的動態連接。
ms.assetid: 11eb19fc-9711-4293-8054-f7975dadb492
ms.tgt_platform: multiple
keywords:
- RedirectDynamicDrives 屬性遠端桌面服務
- RedirectDynamicDrives 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、RedirectDynamicDrives 屬性
- RedirectDynamicDrives 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、RedirectDynamicDrives 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDrives
- IMsRdpClientNonScriptable3.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable3.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.RedirectDynamicDrives
- IMsRdpClientNonScriptable4.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable4.put_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.RedirectDynamicDrives
- IMsRdpClientNonScriptable5.get_RedirectDynamicDrives
- IMsRdpClientNonScriptable5.put_RedirectDynamicDrives
- MsRdpClient5.RedirectDynamicDrives
- MsRdpClient6.RedirectDynamicDrives
- MsRdpClient7.RedirectDynamicDrives
- MsRdpClient8.RedirectDynamicDrives
- MsRdpClient9.RedirectDynamicDrives
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b19c0e6e20f7f73481f6f2ecbc50ab0eda512ded
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686500"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdrives-property"></a><span data-ttu-id="d8594-120">IMsRdpClientNonScriptable3：： RedirectDynamicDrives 屬性</span><span class="sxs-lookup"><span data-stu-id="d8594-120">IMsRdpClientNonScriptable3::RedirectDynamicDrives property</span></span>

<span data-ttu-id="d8594-121">指定或抓取是否可重新導向會話中所列舉的隨插即用 (PnP) 磁片磁碟機的動態連接。</span><span class="sxs-lookup"><span data-stu-id="d8594-121">Specifies or retrieves whether dynamically attached Plug and Play (PnP) drives that are enumerated while in a session are available for redirection.</span></span>

<span data-ttu-id="d8594-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d8594-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8594-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d8594-123">Syntax</span></span>


```C++
HRESULT put_RedirectDynamicDrives(
  [in]  VARIANT_BOOL fRedirectDynamicDrives
);

HRESULT get_RedirectDynamicDrives(
  [out] VARIANT_BOOL *pfRedirectDynamicDrives
);
```



## <a name="property-value"></a><span data-ttu-id="d8594-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="d8594-124">Property value</span></span>

<span data-ttu-id="d8594-125">指定在會話中列舉的動態連接 PnP 磁片磁碟機是否可用於重新導向。</span><span class="sxs-lookup"><span data-stu-id="d8594-125">Specifies whether dynamically attached PnP drives that are enumerated while in a session are available for redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8594-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d8594-126">Requirements</span></span>



| <span data-ttu-id="d8594-127">需求</span><span class="sxs-lookup"><span data-stu-id="d8594-127">Requirement</span></span> | <span data-ttu-id="d8594-128">值</span><span class="sxs-lookup"><span data-stu-id="d8594-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8594-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d8594-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d8594-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d8594-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d8594-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d8594-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d8594-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d8594-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="d8594-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d8594-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="d8594-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8594-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d8594-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d8594-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d8594-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d8594-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d8594-137">IID</span><span class="sxs-lookup"><span data-stu-id="d8594-137">IID</span></span><br/>                      | <span data-ttu-id="d8594-138">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="d8594-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d8594-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d8594-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8594-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="d8594-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="d8594-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="d8594-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="d8594-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="d8594-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





