---
title: IMsRdpClientNonScriptable4 PromptForCredsOnClient 屬性
description: 指定用戶端控制項是否顯示提示輸入認證的對話方塊。
ms.assetid: 426676be-0150-4a33-acd0-26423966f32a
ms.tgt_platform: multiple
keywords:
- PromptForCredsOnClient 屬性遠端桌面服務
- PromptForCredsOnClient 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，PromptForCredsOnClient 屬性
- PromptForCredsOnClient 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，PromptForCredsOnClient 屬性
- PromptForCredsOnClient 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、PromptForCredsOnClient 屬性
- PromptForCredsOnClient 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、PromptForCredsOnClient 屬性
- PromptForCredsOnClient 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、PromptForCredsOnClient 屬性
- PromptForCredsOnClient 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、PromptForCredsOnClient 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PromptForCredsOnClient
- IMsRdpClientNonScriptable4.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable4.put_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.PromptForCredsOnClient
- IMsRdpClientNonScriptable5.get_PromptForCredsOnClient
- IMsRdpClientNonScriptable5.put_PromptForCredsOnClient
- MsRdpClient6.PromptForCredsOnClient
- MsRdpClient7.PromptForCredsOnClient
- MsRdpClient8.PromptForCredsOnClient
- MsRdpClient9.PromptForCredsOnClient
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6443c503e107bb2edb164a17beedddb1bbbc88a5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384894"
---
# <a name="imsrdpclientnonscriptable4promptforcredsonclient-property"></a><span data-ttu-id="a5fcc-116">IMsRdpClientNonScriptable4：:P romptForCredsOnClient 屬性</span><span class="sxs-lookup"><span data-stu-id="a5fcc-116">IMsRdpClientNonScriptable4::PromptForCredsOnClient property</span></span>

<span data-ttu-id="a5fcc-117">指定用戶端控制項是否顯示提示輸入認證的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a5fcc-117">Specifies whether the client control displays a dialog box that prompts for credentials.</span></span>

<span data-ttu-id="a5fcc-118">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="a5fcc-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5fcc-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="a5fcc-119">Syntax</span></span>


```C++
HRESULT put_PromptForCredsOnClient(
  [in]  VARIANT_BOOL fPromptForCredsOnClient
);

HRESULT get_PromptForCredsOnClient(
  [out] VARIANT_BOOL *pfPromptForCredsOnClient
);
```



## <a name="property-value"></a><span data-ttu-id="a5fcc-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="a5fcc-120">Property value</span></span>

<span data-ttu-id="a5fcc-121">設定用戶端控制項是否顯示提示輸入認證的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a5fcc-121">Sets whether the client control displays a dialog box that prompts for credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="a5fcc-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="a5fcc-122">Error codes</span></span>

<span data-ttu-id="a5fcc-123">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="a5fcc-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5fcc-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5fcc-124">Requirements</span></span>



| <span data-ttu-id="a5fcc-125">需求</span><span class="sxs-lookup"><span data-stu-id="a5fcc-125">Requirement</span></span> | <span data-ttu-id="a5fcc-126">值</span><span class="sxs-lookup"><span data-stu-id="a5fcc-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5fcc-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5fcc-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a5fcc-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a5fcc-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="a5fcc-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5fcc-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a5fcc-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a5fcc-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="a5fcc-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a5fcc-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="a5fcc-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5fcc-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="a5fcc-133">DLL</span><span class="sxs-lookup"><span data-stu-id="a5fcc-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a5fcc-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5fcc-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="a5fcc-135">IID</span><span class="sxs-lookup"><span data-stu-id="a5fcc-135">IID</span></span><br/>                      | <span data-ttu-id="a5fcc-136">IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="a5fcc-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a5fcc-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5fcc-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5fcc-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="a5fcc-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="a5fcc-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="a5fcc-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





