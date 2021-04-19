---
title: IMsRdpClientNonScriptable4 RedirectionWarningType 屬性
description: 控制通知使用者重新導向之對話方塊的存在和外觀。
ms.assetid: 1aa79fc3-9620-466d-a93f-77a55ad76ede
ms.tgt_platform: multiple
keywords:
- RedirectionWarningType 屬性遠端桌面服務
- RedirectionWarningType 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，RedirectionWarningType 屬性
- RedirectionWarningType 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，RedirectionWarningType 屬性
- RedirectionWarningType 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、RedirectionWarningType 屬性
- RedirectionWarningType 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、RedirectionWarningType 屬性
- RedirectionWarningType 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、RedirectionWarningType 屬性
- RedirectionWarningType 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、RedirectionWarningType 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.RedirectionWarningType
- IMsRdpClientNonScriptable4.get_RedirectionWarningType
- IMsRdpClientNonScriptable4.put_RedirectionWarningType
- IMsRdpClientNonScriptable5.RedirectionWarningType
- IMsRdpClientNonScriptable5.get_RedirectionWarningType
- IMsRdpClientNonScriptable5.put_RedirectionWarningType
- MsRdpClient6.RedirectionWarningType
- MsRdpClient7.RedirectionWarningType
- MsRdpClient8.RedirectionWarningType
- MsRdpClient9.RedirectionWarningType
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077c8f78c61cc9b7dd090db26f58ca7e28c14abb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966126"
---
# <a name="imsrdpclientnonscriptable4redirectionwarningtype-property"></a><span data-ttu-id="97d44-116">IMsRdpClientNonScriptable4：： RedirectionWarningType 屬性</span><span class="sxs-lookup"><span data-stu-id="97d44-116">IMsRdpClientNonScriptable4::RedirectionWarningType property</span></span>

<span data-ttu-id="97d44-117">控制通知使用者重新導向之對話方塊的存在和外觀。</span><span class="sxs-lookup"><span data-stu-id="97d44-117">Controls the presence and appearance of the dialog box that notifies the user about redirection.</span></span>

<span data-ttu-id="97d44-118">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="97d44-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="97d44-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="97d44-119">Syntax</span></span>


```C++
HRESULT put_RedirectionWarningType(
  [in]  RedirectionWarningType wrnType
);

HRESULT get_RedirectionWarningType(
  [out] RedirectionWarningType *pWrnType
);
```



## <a name="property-value"></a><span data-ttu-id="97d44-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="97d44-120">Property value</span></span>

<span data-ttu-id="97d44-121">設定對話方塊的型別，此對話方塊會通知使用者重新導向。</span><span class="sxs-lookup"><span data-stu-id="97d44-121">Sets the type of the dialog box that notifies the user of redirection.</span></span>

<dt>

<span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>

<span data-ttu-id="97d44-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000) </span><span class="sxs-lookup"><span data-stu-id="97d44-122"><span id="RedirectionWarningTypeDefault"></span><span id="redirectionwarningtypedefault"></span><span id="REDIRECTIONWARNINGTYPEDEFAULT"></span>**RedirectionWarningTypeDefault** (0x0000)</span></span>


</dt> <dd>

<span data-ttu-id="97d44-123">對話方塊不是發行者特定的。</span><span class="sxs-lookup"><span data-stu-id="97d44-123">The dialog box is not publisher specific.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>

<span data-ttu-id="97d44-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001) </span><span class="sxs-lookup"><span data-stu-id="97d44-124"><span id="RedirectionWarningTypeUnsigned"></span><span id="redirectionwarningtypeunsigned"></span><span id="REDIRECTIONWARNINGTYPEUNSIGNED"></span>**RedirectionWarningTypeUnsigned** (0x0001)</span></span>


</dt> <dd>

<span data-ttu-id="97d44-125">對話方塊適用于未簽署的檔案。</span><span class="sxs-lookup"><span data-stu-id="97d44-125">The dialog box is for unsigned files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>

<span data-ttu-id="97d44-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002) </span><span class="sxs-lookup"><span data-stu-id="97d44-126"><span id="RedirectionWarningTypeUnknown"></span><span id="redirectionwarningtypeunknown"></span><span id="REDIRECTIONWARNINGTYPEUNKNOWN"></span>**RedirectionWarningTypeUnknown** (0x0002)</span></span>


</dt> <dd>

<span data-ttu-id="97d44-127">此對話方塊適用于未知的發行者。</span><span class="sxs-lookup"><span data-stu-id="97d44-127">The dialog box is for an unknown publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>

<span data-ttu-id="97d44-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003) </span><span class="sxs-lookup"><span data-stu-id="97d44-128"><span id="RedirectionWarningTypeUser"></span><span id="redirectionwarningtypeuser"></span><span id="REDIRECTIONWARNINGTYPEUSER"></span>**RedirectionWarningTypeUser** (0x0003)</span></span>


</dt> <dd>

<span data-ttu-id="97d44-129">對話方塊適用于使用者的檔案。</span><span class="sxs-lookup"><span data-stu-id="97d44-129">The dialog box is for the user's files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>

<span data-ttu-id="97d44-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004) </span><span class="sxs-lookup"><span data-stu-id="97d44-130"><span id="RedirectionWarningTypeThirdPartySigned"></span><span id="redirectionwarningtypethirdpartysigned"></span><span id="REDIRECTIONWARNINGTYPETHIRDPARTYSIGNED"></span>**RedirectionWarningTypeThirdPartySigned** (0x0004)</span></span>


</dt> <dd>

<span data-ttu-id="97d44-131">協力廠商認證的檔案會顯示此對話方塊。</span><span class="sxs-lookup"><span data-stu-id="97d44-131">The dialog box is displayed for third-party-certified, signed files.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>

<span data-ttu-id="97d44-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005) </span><span class="sxs-lookup"><span data-stu-id="97d44-132"><span id="RedirectionWarningTypeTrusted"></span><span id="redirectionwarningtypetrusted"></span><span id="REDIRECTIONWARNINGTYPETRUSTED"></span>**RedirectionWarningTypeTrusted** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="97d44-133">對話方塊不會顯示，因為應用程式是由受信任的發行者所發行。</span><span class="sxs-lookup"><span data-stu-id="97d44-133">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> <dt>

<span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>

<span data-ttu-id="97d44-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005) </span><span class="sxs-lookup"><span data-stu-id="97d44-134"><span id="RedirectionWarningTypeMax"></span><span id="redirectionwarningtypemax"></span><span id="REDIRECTIONWARNINGTYPEMAX"></span>**RedirectionWarningTypeMax** (0x0005)</span></span>


</dt> <dd>

<span data-ttu-id="97d44-135">對話方塊不會顯示，因為應用程式是由受信任的發行者所發行。</span><span class="sxs-lookup"><span data-stu-id="97d44-135">The dialog box is not displayed because the application is published by a trusted publisher.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="97d44-136">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="97d44-136">Error codes</span></span>

<span data-ttu-id="97d44-137">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="97d44-137">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="97d44-138">備註</span><span class="sxs-lookup"><span data-stu-id="97d44-138">Remarks</span></span>

<span data-ttu-id="97d44-139">值 **RedirectionWarningTypeDefault** 是這個屬性的預設值，對無法控制對話方塊。</span><span class="sxs-lookup"><span data-stu-id="97d44-139">The value **RedirectionWarningTypeDefault**, which is the default value of this property, exerts no control over the dialog box.</span></span> <span data-ttu-id="97d44-140">此案例中的控制屬性是在 [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)中 [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) 。</span><span class="sxs-lookup"><span data-stu-id="97d44-140">The controlling property in this case is [**ShowRedirectionWarningDialog**](imsrdpclientnonscriptable3-showredirectionwarningdialog.md) in [**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="97d44-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="97d44-141">Requirements</span></span>



| <span data-ttu-id="97d44-142">需求</span><span class="sxs-lookup"><span data-stu-id="97d44-142">Requirement</span></span> | <span data-ttu-id="97d44-143">值</span><span class="sxs-lookup"><span data-stu-id="97d44-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="97d44-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97d44-144">Minimum supported client</span></span><br/> | <span data-ttu-id="97d44-145">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="97d44-145">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="97d44-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97d44-146">Minimum supported server</span></span><br/> | <span data-ttu-id="97d44-147">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="97d44-147">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="97d44-148">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="97d44-148">Type library</span></span><br/>             | <dl> <span data-ttu-id="97d44-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97d44-149"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="97d44-150">DLL</span><span class="sxs-lookup"><span data-stu-id="97d44-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="97d44-151"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="97d44-151"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="97d44-152">IID</span><span class="sxs-lookup"><span data-stu-id="97d44-152">IID</span></span><br/>                      | <span data-ttu-id="97d44-153">IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="97d44-153">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="97d44-154">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97d44-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97d44-155">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="97d44-155">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="97d44-156">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="97d44-156">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





