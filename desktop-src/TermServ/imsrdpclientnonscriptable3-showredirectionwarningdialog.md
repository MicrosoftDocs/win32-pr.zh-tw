---
title: IMsRdpClientNonScriptable3 ShowRedirectionWarningDialog 屬性
description: 指定或抓取是否應顯示 [重新導向警告] 對話方塊。
ms.assetid: 7ed37288-77c3-4551-a553-1ca679e1047a
ms.tgt_platform: multiple
keywords:
- ShowRedirectionWarningDialog 屬性遠端桌面服務
- ShowRedirectionWarningDialog 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，ShowRedirectionWarningDialog 屬性
- ShowRedirectionWarningDialog 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，ShowRedirectionWarningDialog 屬性
- ShowRedirectionWarningDialog 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，ShowRedirectionWarningDialog 屬性
- ShowRedirectionWarningDialog 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、ShowRedirectionWarningDialog 屬性
- ShowRedirectionWarningDialog 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、ShowRedirectionWarningDialog 屬性
- ShowRedirectionWarningDialog 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、ShowRedirectionWarningDialog 屬性
- ShowRedirectionWarningDialog 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、ShowRedirectionWarningDialog 屬性
- ShowRedirectionWarningDialog 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、ShowRedirectionWarningDialog 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable3.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable4.put_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.get_ShowRedirectionWarningDialog
- IMsRdpClientNonScriptable5.put_ShowRedirectionWarningDialog
- MsRdpClient5.ShowRedirectionWarningDialog
- MsRdpClient6.ShowRedirectionWarningDialog
- MsRdpClient7.ShowRedirectionWarningDialog
- MsRdpClient8.ShowRedirectionWarningDialog
- MsRdpClient9.ShowRedirectionWarningDialog
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 468e1721de3395067ca570c2051f3906df626071
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024818"
---
# <a name="imsrdpclientnonscriptable3showredirectionwarningdialog-property"></a><span data-ttu-id="743dc-120">IMsRdpClientNonScriptable3：： ShowRedirectionWarningDialog 屬性</span><span class="sxs-lookup"><span data-stu-id="743dc-120">IMsRdpClientNonScriptable3::ShowRedirectionWarningDialog property</span></span>

<span data-ttu-id="743dc-121">指定或抓取是否應顯示 [重新導向警告] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="743dc-121">Specifies or retrieves whether the redirection warning dialog box should be shown.</span></span>

<span data-ttu-id="743dc-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="743dc-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="743dc-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="743dc-123">Syntax</span></span>


```C++
HRESULT put_ShowRedirectionWarningDialog(
  [in]  VARIANT_BOOL fShowRdrDlg
);

HRESULT get_ShowRedirectionWarningDialog(
  [out] VARIANT_BOOL *pfShowRdrDlg
);
```



## <a name="property-value"></a><span data-ttu-id="743dc-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="743dc-124">Property value</span></span>

<span data-ttu-id="743dc-125">指定是否應顯示 [重新導向警告] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="743dc-125">Specifies whether the redirection warning dialog box should be shown.</span></span>

## <a name="requirements"></a><span data-ttu-id="743dc-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="743dc-126">Requirements</span></span>



| <span data-ttu-id="743dc-127">需求</span><span class="sxs-lookup"><span data-stu-id="743dc-127">Requirement</span></span> | <span data-ttu-id="743dc-128">值</span><span class="sxs-lookup"><span data-stu-id="743dc-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="743dc-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="743dc-129">Minimum supported client</span></span><br/> | <span data-ttu-id="743dc-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="743dc-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="743dc-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="743dc-131">Minimum supported server</span></span><br/> | <span data-ttu-id="743dc-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="743dc-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="743dc-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="743dc-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="743dc-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="743dc-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="743dc-135">DLL</span><span class="sxs-lookup"><span data-stu-id="743dc-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="743dc-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="743dc-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="743dc-137">IID</span><span class="sxs-lookup"><span data-stu-id="743dc-137">IID</span></span><br/>                      | <span data-ttu-id="743dc-138">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="743dc-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="743dc-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="743dc-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="743dc-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="743dc-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="743dc-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="743dc-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="743dc-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="743dc-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





