---
title: IMsRdpClientNonScriptable3 ConnectionBarText 屬性
description: 設定或抓取文字以更新連接列。
ms.assetid: 9671118d-ee7c-4077-be81-57655aff5e35
ms.tgt_platform: multiple
keywords:
- ConnectionBarText 屬性遠端桌面服務
- ConnectionBarText 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，ConnectionBarText 屬性
- ConnectionBarText 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，ConnectionBarText 屬性
- ConnectionBarText 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，ConnectionBarText 屬性
- ConnectionBarText 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、ConnectionBarText 屬性
- ConnectionBarText 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、ConnectionBarText 屬性
- ConnectionBarText 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、ConnectionBarText 屬性
- ConnectionBarText 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、ConnectionBarText 屬性
- ConnectionBarText 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、ConnectionBarText 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ConnectionBarText
- IMsRdpClientNonScriptable3.get_ConnectionBarText
- IMsRdpClientNonScriptable3.put_ConnectionBarText
- IMsRdpClientNonScriptable4.ConnectionBarText
- IMsRdpClientNonScriptable4.get_ConnectionBarText
- IMsRdpClientNonScriptable4.put_ConnectionBarText
- IMsRdpClientNonScriptable5.ConnectionBarText
- IMsRdpClientNonScriptable5.get_ConnectionBarText
- IMsRdpClientNonScriptable5.put_ConnectionBarText
- MsRdpClient5.ConnectionBarText
- MsRdpClient6.ConnectionBarText
- MsRdpClient7.ConnectionBarText
- MsRdpClient8.ConnectionBarText
- MsRdpClient9.ConnectionBarText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 76819dd28ffd8b2ee5e2dfb30017e341dd49db5b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686356"
---
# <a name="imsrdpclientnonscriptable3connectionbartext-property"></a><span data-ttu-id="be445-120">IMsRdpClientNonScriptable3：： ConnectionBarText 屬性</span><span class="sxs-lookup"><span data-stu-id="be445-120">IMsRdpClientNonScriptable3::ConnectionBarText property</span></span>

<span data-ttu-id="be445-121">設定或抓取文字以更新連接列。</span><span class="sxs-lookup"><span data-stu-id="be445-121">Sets or retrieves the text to update the connection bar.</span></span>

<span data-ttu-id="be445-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="be445-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="be445-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="be445-123">Syntax</span></span>


```C++
HRESULT put_ConnectionBarText(
  [in]  BSTR newVal
);

HRESULT get_ConnectionBarText(
  [out] BSTR *pConnectionBarText
);
```



## <a name="property-value"></a><span data-ttu-id="be445-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="be445-124">Property value</span></span>

<span data-ttu-id="be445-125">設定要在連接列上顯示的文字字串。</span><span class="sxs-lookup"><span data-stu-id="be445-125">Sets the text string to display on the connection bar.</span></span>

## <a name="remarks"></a><span data-ttu-id="be445-126">備註</span><span class="sxs-lookup"><span data-stu-id="be445-126">Remarks</span></span>

<span data-ttu-id="be445-127">您必須先呼叫 **IMsRdpClientNonScriptable3：:p 的 \_ ConnectionBarText** 方法，然後再呼叫 [**IMsTscSecuredSettings：:p 的 \_ 全像全螢幕**](imstscsecuredsettings-fullscreen.md) 方法或 [**IMsRdpClient：:p 的 ui \_ 全螢幕**](imsrdpclient-fullscreen.md) 方式。</span><span class="sxs-lookup"><span data-stu-id="be445-127">You must call the **IMsRdpClientNonScriptable3::put\_ConnectionBarText** method before you call the [**IMsTscSecuredSettings::put\_Fullscreen**](imstscsecuredsettings-fullscreen.md) method or the [**IMsRdpClient::put\_Fullscreen**](imsrdpclient-fullscreen.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="be445-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="be445-128">Requirements</span></span>



| <span data-ttu-id="be445-129">需求</span><span class="sxs-lookup"><span data-stu-id="be445-129">Requirement</span></span> | <span data-ttu-id="be445-130">值</span><span class="sxs-lookup"><span data-stu-id="be445-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="be445-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="be445-131">Minimum supported client</span></span><br/> | <span data-ttu-id="be445-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="be445-132">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="be445-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="be445-133">Minimum supported server</span></span><br/> | <span data-ttu-id="be445-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="be445-134">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="be445-135">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="be445-135">Type library</span></span><br/>             | <dl> <span data-ttu-id="be445-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be445-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="be445-137">DLL</span><span class="sxs-lookup"><span data-stu-id="be445-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="be445-138"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="be445-138"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="be445-139">IID</span><span class="sxs-lookup"><span data-stu-id="be445-139">IID</span></span><br/>                      | <span data-ttu-id="be445-140">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="be445-140">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="be445-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="be445-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="be445-142">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="be445-142">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="be445-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="be445-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="be445-144">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="be445-144">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





