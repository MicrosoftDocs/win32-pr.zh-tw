---
title: 'IMsRdpClientNonScriptable3 PromptForCredentials 屬性 (Wuapi .h) '
description: 指定或抓取連接是否啟用 [提示輸入認證] 對話方塊。
ms.assetid: 252ec5bd-bd52-40d4-ae48-b2c00c0720c0
ms.tgt_platform: multiple
keywords:
- PromptForCredentials 屬性遠端桌面服務
- PromptForCredentials 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，PromptForCredentials 屬性
- PromptForCredentials 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，PromptForCredentials 屬性
- PromptForCredentials 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，PromptForCredentials 屬性
- PromptForCredentials 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、PromptForCredentials 屬性
- PromptForCredentials 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、PromptForCredentials 屬性
- PromptForCredentials 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、PromptForCredentials 屬性
- PromptForCredentials 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、PromptForCredentials 屬性
- PromptForCredentials 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、PromptForCredentials 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.PromptForCredentials
- IMsRdpClientNonScriptable3.get_PromptForCredentials
- IMsRdpClientNonScriptable3.put_PromptForCredentials
- IMsRdpClientNonScriptable4.PromptForCredentials
- IMsRdpClientNonScriptable4.get_PromptForCredentials
- IMsRdpClientNonScriptable4.put_PromptForCredentials
- IMsRdpClientNonScriptable5.PromptForCredentials
- IMsRdpClientNonScriptable5.get_PromptForCredentials
- IMsRdpClientNonScriptable5.put_PromptForCredentials
- MsRdpClient5.PromptForCredentials
- MsRdpClient6.PromptForCredentials
- MsRdpClient7.PromptForCredentials
- MsRdpClient8.PromptForCredentials
- MsRdpClient9.PromptForCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62f913937c9a2ff01d4aabeaba48dcbdc8ddb21d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317124"
---
# <a name="imsrdpclientnonscriptable3promptforcredentials-property"></a><span data-ttu-id="e8e3d-120">IMsRdpClientNonScriptable3：:P romptForCredentials 屬性</span><span class="sxs-lookup"><span data-stu-id="e8e3d-120">IMsRdpClientNonScriptable3::PromptForCredentials property</span></span>

<span data-ttu-id="e8e3d-121">指定或抓取連接是否啟用 [提示輸入認證] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e8e3d-121">Specifies or retrieves whether the prompt for credentials dialog is enabled for the connection.</span></span>

<span data-ttu-id="e8e3d-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="e8e3d-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e3d-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8e3d-123">Syntax</span></span>


```C++
HRESULT put_PromptForCredentials(
  [in]  VARIANT_BOOL fPrompt
);

HRESULT get_PromptForCredentials(
  [out] VARIANT_BOOL *pfPrompt
);
```



## <a name="property-value"></a><span data-ttu-id="e8e3d-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="e8e3d-124">Property value</span></span>

<span data-ttu-id="e8e3d-125">指定是否為連接啟用 [提示輸入認證] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e8e3d-125">Specifies whether the prompt for credentials dialog is enabled for the connection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="e8e3d-126">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="e8e3d-126">Error codes</span></span>

## <a name="requirements"></a><span data-ttu-id="e8e3d-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="e8e3d-127">Requirements</span></span>



| <span data-ttu-id="e8e3d-128">需求</span><span class="sxs-lookup"><span data-stu-id="e8e3d-128">Requirement</span></span> | <span data-ttu-id="e8e3d-129">值</span><span class="sxs-lookup"><span data-stu-id="e8e3d-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e3d-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e8e3d-130">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e3d-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e8e3d-131">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="e8e3d-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e8e3d-132">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e3d-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e8e3d-133">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="e8e3d-134">標頭</span><span class="sxs-lookup"><span data-stu-id="e8e3d-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e3d-135"><dt>Wuapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e3d-135"><dt>Wuapi.h</dt></span></span> </dl>            |
| <span data-ttu-id="e8e3d-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="e8e3d-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="e8e3d-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8e3d-137"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e8e3d-138">DLL</span><span class="sxs-lookup"><span data-stu-id="e8e3d-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e8e3d-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e8e3d-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="e8e3d-140">IID</span><span class="sxs-lookup"><span data-stu-id="e8e3d-140">IID</span></span><br/>                      | <span data-ttu-id="e8e3d-141">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="e8e3d-141">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="e8e3d-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e8e3d-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e3d-143">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="e8e3d-143">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="e8e3d-144">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="e8e3d-144">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="e8e3d-145">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="e8e3d-145">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





