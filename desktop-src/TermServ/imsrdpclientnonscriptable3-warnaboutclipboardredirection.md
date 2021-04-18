---
title: IMsRdpClientNonScriptable3 WarnAboutClipboardRedirection 屬性
description: 指定或抓取是否應顯示 [安全性警告] 對話方塊，以警告使用者剪貼簿重新導向。
ms.assetid: 2f3ca58b-3c89-4251-ae15-2c0aaf308893
ms.tgt_platform: multiple
keywords:
- WarnAboutClipboardRedirection 屬性遠端桌面服務
- WarnAboutClipboardRedirection 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，WarnAboutClipboardRedirection 屬性
- WarnAboutClipboardRedirection 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，WarnAboutClipboardRedirection 屬性
- WarnAboutClipboardRedirection 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，WarnAboutClipboardRedirection 屬性
- WarnAboutClipboardRedirection 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、WarnAboutClipboardRedirection 屬性
- WarnAboutClipboardRedirection 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、WarnAboutClipboardRedirection 屬性
- WarnAboutClipboardRedirection 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、WarnAboutClipboardRedirection 屬性
- WarnAboutClipboardRedirection 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、WarnAboutClipboardRedirection 屬性
- WarnAboutClipboardRedirection 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、WarnAboutClipboardRedirection 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable3.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutClipboardRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutClipboardRedirection
- MsRdpClient5.WarnAboutClipboardRedirection
- MsRdpClient6.WarnAboutClipboardRedirection
- MsRdpClient7.WarnAboutClipboardRedirection
- MsRdpClient8.WarnAboutClipboardRedirection
- MsRdpClient9.WarnAboutClipboardRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d8da6fa2f7fb36a110666c8b14a818264813d816
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508420"
---
# <a name="imsrdpclientnonscriptable3warnaboutclipboardredirection-property"></a><span data-ttu-id="13bb5-120">IMsRdpClientNonScriptable3：： WarnAboutClipboardRedirection 屬性</span><span class="sxs-lookup"><span data-stu-id="13bb5-120">IMsRdpClientNonScriptable3::WarnAboutClipboardRedirection property</span></span>

<span data-ttu-id="13bb5-121">指定或抓取是否應顯示 [安全性警告] 對話方塊，以警告使用者剪貼簿重新導向。</span><span class="sxs-lookup"><span data-stu-id="13bb5-121">Specifies or retrieves whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

<span data-ttu-id="13bb5-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="13bb5-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="13bb5-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="13bb5-123">Syntax</span></span>


```C++
HRESULT put_WarnAboutClipboardRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutClipboardRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="13bb5-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="13bb5-124">Property value</span></span>

<span data-ttu-id="13bb5-125">指定是否應顯示 [安全性警告] 對話方塊，以警告使用者剪貼簿重新導向。</span><span class="sxs-lookup"><span data-stu-id="13bb5-125">Specifies whether the security warning dialog box should be displayed to warn users about clipboard redirection.</span></span>

## <a name="requirements"></a><span data-ttu-id="13bb5-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="13bb5-126">Requirements</span></span>



| <span data-ttu-id="13bb5-127">需求</span><span class="sxs-lookup"><span data-stu-id="13bb5-127">Requirement</span></span> | <span data-ttu-id="13bb5-128">值</span><span class="sxs-lookup"><span data-stu-id="13bb5-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="13bb5-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="13bb5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="13bb5-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="13bb5-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="13bb5-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="13bb5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="13bb5-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="13bb5-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="13bb5-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="13bb5-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="13bb5-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13bb5-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="13bb5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="13bb5-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13bb5-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13bb5-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="13bb5-137">IID</span><span class="sxs-lookup"><span data-stu-id="13bb5-137">IID</span></span><br/>                      | <span data-ttu-id="13bb5-138">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="13bb5-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="13bb5-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13bb5-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13bb5-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="13bb5-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="13bb5-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="13bb5-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="13bb5-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="13bb5-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





