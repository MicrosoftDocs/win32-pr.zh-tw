---
title: IMsRdpClientNonScriptable4 AllowCredentialSaving 屬性
description: 指定認證對話方塊是否顯示啟用儲存認證的核取方塊。
ms.assetid: c5148ff0-0d7f-413d-b2a8-ff942668bee6
ms.tgt_platform: multiple
keywords:
- AllowCredentialSaving 屬性遠端桌面服務
- AllowCredentialSaving 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，AllowCredentialSaving 屬性
- AllowCredentialSaving 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，AllowCredentialSaving 屬性
- AllowCredentialSaving 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、AllowCredentialSaving 屬性
- AllowCredentialSaving 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、AllowCredentialSaving 屬性
- AllowCredentialSaving 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、AllowCredentialSaving 屬性
- AllowCredentialSaving 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、AllowCredentialSaving 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.AllowCredentialSaving
- IMsRdpClientNonScriptable4.get_AllowCredentialSaving
- IMsRdpClientNonScriptable4.put_AllowCredentialSaving
- IMsRdpClientNonScriptable5.AllowCredentialSaving
- IMsRdpClientNonScriptable5.get_AllowCredentialSaving
- IMsRdpClientNonScriptable5.put_AllowCredentialSaving
- MsRdpClient6.AllowCredentialSaving
- MsRdpClient7.AllowCredentialSaving
- MsRdpClient8.AllowCredentialSaving
- MsRdpClient9.AllowCredentialSaving
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 240e2eb8e80209ee5c90d63f2996231cf84bb2dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106996581"
---
# <a name="imsrdpclientnonscriptable4allowcredentialsaving-property"></a><span data-ttu-id="8404d-116">IMsRdpClientNonScriptable4：： AllowCredentialSaving 屬性</span><span class="sxs-lookup"><span data-stu-id="8404d-116">IMsRdpClientNonScriptable4::AllowCredentialSaving property</span></span>

<span data-ttu-id="8404d-117">指定認證對話方塊是否顯示啟用儲存認證的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="8404d-117">Specifies whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

<span data-ttu-id="8404d-118">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="8404d-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="8404d-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="8404d-119">Syntax</span></span>


```C++
HRESULT put_AllowCredentialSaving(
  [in]  VARIANT_BOOL fAllowSave
);

HRESULT get_AllowCredentialSaving(
  [out] VARIANT_BOOL *pfAllowSave
);
```



## <a name="property-value"></a><span data-ttu-id="8404d-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="8404d-120">Property value</span></span>

<span data-ttu-id="8404d-121">設定認證對話方塊是否顯示啟用儲存認證的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="8404d-121">Sets whether the credentials dialog box displays a check box that enables the saving of credentials.</span></span>

## <a name="error-codes"></a><span data-ttu-id="8404d-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="8404d-122">Error codes</span></span>

<span data-ttu-id="8404d-123">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="8404d-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="8404d-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="8404d-124">Requirements</span></span>



| <span data-ttu-id="8404d-125">需求</span><span class="sxs-lookup"><span data-stu-id="8404d-125">Requirement</span></span> | <span data-ttu-id="8404d-126">值</span><span class="sxs-lookup"><span data-stu-id="8404d-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="8404d-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8404d-127">Minimum supported client</span></span><br/> | <span data-ttu-id="8404d-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8404d-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="8404d-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8404d-129">Minimum supported server</span></span><br/> | <span data-ttu-id="8404d-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8404d-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="8404d-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8404d-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="8404d-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8404d-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="8404d-133">DLL</span><span class="sxs-lookup"><span data-stu-id="8404d-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8404d-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8404d-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="8404d-135">IID</span><span class="sxs-lookup"><span data-stu-id="8404d-135">IID</span></span><br/>                      | <span data-ttu-id="8404d-136">IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="8404d-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8404d-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8404d-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8404d-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="8404d-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="8404d-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="8404d-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





