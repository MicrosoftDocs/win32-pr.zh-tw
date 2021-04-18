---
title: IMsRdpClientNonScriptable3 WarnAboutSendingCredentials 屬性
description: 指定或抓取安全性警告對話方塊是否應該包含在啟動會話之前，將認證傳送至遠端伺服器的警告。
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- WarnAboutSendingCredentials 屬性遠端桌面服務
- WarnAboutSendingCredentials 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，WarnAboutSendingCredentials 屬性
- WarnAboutSendingCredentials 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，WarnAboutSendingCredentials 屬性
- WarnAboutSendingCredentials 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，WarnAboutSendingCredentials 屬性
- WarnAboutSendingCredentials 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、WarnAboutSendingCredentials 屬性
- WarnAboutSendingCredentials 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、WarnAboutSendingCredentials 屬性
- WarnAboutSendingCredentials 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、WarnAboutSendingCredentials 屬性
- WarnAboutSendingCredentials 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、WarnAboutSendingCredentials 屬性
- WarnAboutSendingCredentials 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、WarnAboutSendingCredentials 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106968751"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a><span data-ttu-id="d4abb-120">IMsRdpClientNonScriptable3：： WarnAboutSendingCredentials 屬性</span><span class="sxs-lookup"><span data-stu-id="d4abb-120">IMsRdpClientNonScriptable3::WarnAboutSendingCredentials property</span></span>

<span data-ttu-id="d4abb-121">指定或抓取安全性警告對話方塊是否應該包含在啟動會話之前，將認證傳送至遠端伺服器的警告。</span><span class="sxs-lookup"><span data-stu-id="d4abb-121">Specifies or retrieves whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

<span data-ttu-id="d4abb-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d4abb-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4abb-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4abb-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="d4abb-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="d4abb-124">Property value</span></span>

<span data-ttu-id="d4abb-125">指定在啟動會話之前，安全性警告對話方塊是否應包含有關將認證傳送至遠端伺服器的警告。</span><span class="sxs-lookup"><span data-stu-id="d4abb-125">Specifies whether the security warning dialog box should include a warning about sending credentials to the remote server before starting a session.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4abb-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4abb-126">Requirements</span></span>



| <span data-ttu-id="d4abb-127">需求</span><span class="sxs-lookup"><span data-stu-id="d4abb-127">Requirement</span></span> | <span data-ttu-id="d4abb-128">值</span><span class="sxs-lookup"><span data-stu-id="d4abb-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4abb-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d4abb-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d4abb-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4abb-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d4abb-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d4abb-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d4abb-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4abb-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="d4abb-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d4abb-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="d4abb-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4abb-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d4abb-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d4abb-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4abb-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4abb-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d4abb-137">IID</span><span class="sxs-lookup"><span data-stu-id="d4abb-137">IID</span></span><br/>                      | <span data-ttu-id="d4abb-138">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="d4abb-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d4abb-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d4abb-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4abb-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="d4abb-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="d4abb-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="d4abb-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="d4abb-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="d4abb-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





