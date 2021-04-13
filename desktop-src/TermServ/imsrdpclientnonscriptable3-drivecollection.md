---
title: IMsRdpClientNonScriptable3 DriveCollection 屬性
description: 抓取要重新導向之磁片磁碟機物件的集合。
ms.assetid: 5aaac605-584b-442e-9d67-1cb8213a70b3
ms.tgt_platform: multiple
keywords:
- DriveCollection 屬性遠端桌面服務
- DriveCollection 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，DriveCollection 屬性
- DriveCollection 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，DriveCollection 屬性
- DriveCollection 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，DriveCollection 屬性
- DriveCollection 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、DriveCollection 屬性
- DriveCollection 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、DriveCollection 屬性
- DriveCollection 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、DriveCollection 屬性
- DriveCollection 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、DriveCollection 屬性
- DriveCollection 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、DriveCollection 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DriveCollection
- IMsRdpClientNonScriptable3.get_DriveCollection
- IMsRdpClientNonScriptable4.DriveCollection
- IMsRdpClientNonScriptable4.get_DriveCollection
- IMsRdpClientNonScriptable5.DriveCollection
- IMsRdpClientNonScriptable5.get_DriveCollection
- MsRdpClient5.DriveCollection
- MsRdpClient6.DriveCollection
- MsRdpClient7.DriveCollection
- MsRdpClient8.DriveCollection
- MsRdpClient9.DriveCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37d4bfcaa52d483adc8b0d0885d8316f10ce01d1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464685"
---
# <a name="imsrdpclientnonscriptable3drivecollection-property"></a><span data-ttu-id="bf27a-120">IMsRdpClientNonScriptable3：:D riveCollection 屬性</span><span class="sxs-lookup"><span data-stu-id="bf27a-120">IMsRdpClientNonScriptable3::DriveCollection property</span></span>

<span data-ttu-id="bf27a-121">抓取要重新導向之磁片磁碟機物件的集合。</span><span class="sxs-lookup"><span data-stu-id="bf27a-121">Retrieves the collection of drive objects to be redirected.</span></span>

<span data-ttu-id="bf27a-122">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="bf27a-122">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf27a-123">語法</span><span class="sxs-lookup"><span data-stu-id="bf27a-123">Syntax</span></span>


```C++
HRESULT get_DriveCollection(
  [out] IMsRdpDriveCollection **ppDriveCollection
);
```



## <a name="property-value"></a><span data-ttu-id="bf27a-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="bf27a-124">Property value</span></span>

<span data-ttu-id="bf27a-125">抓取 [**IMSRdpDrive**](imsrdpdrive.md)類型之磁片磁碟機物件的集合。</span><span class="sxs-lookup"><span data-stu-id="bf27a-125">Retrieves the collection of drive objects of type [**IMSRdpDrive**](imsrdpdrive.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bf27a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="bf27a-126">Requirements</span></span>



| <span data-ttu-id="bf27a-127">需求</span><span class="sxs-lookup"><span data-stu-id="bf27a-127">Requirement</span></span> | <span data-ttu-id="bf27a-128">值</span><span class="sxs-lookup"><span data-stu-id="bf27a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf27a-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bf27a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="bf27a-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bf27a-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="bf27a-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bf27a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="bf27a-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bf27a-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="bf27a-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bf27a-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="bf27a-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf27a-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="bf27a-135">DLL</span><span class="sxs-lookup"><span data-stu-id="bf27a-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf27a-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf27a-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="bf27a-137">IID</span><span class="sxs-lookup"><span data-stu-id="bf27a-137">IID</span></span><br/>                      | <span data-ttu-id="bf27a-138">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="bf27a-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bf27a-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bf27a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf27a-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="bf27a-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="bf27a-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="bf27a-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="bf27a-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="bf27a-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





