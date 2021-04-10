---
title: IMsRdpClientNonScriptable4 WarnAboutPrinterRedirection 屬性
description: 控制重新導向對話方塊是否會在啟動會話之前顯示有關印表機重新導向的訊息。
ms.assetid: 12c5bc8d-7bc1-4a94-a9b8-6b852772c936
ms.tgt_platform: multiple
keywords:
- WarnAboutPrinterRedirection 屬性遠端桌面服務
- WarnAboutPrinterRedirection 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，WarnAboutPrinterRedirection 屬性
- WarnAboutPrinterRedirection 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，WarnAboutPrinterRedirection 屬性
- WarnAboutPrinterRedirection 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、WarnAboutPrinterRedirection 屬性
- WarnAboutPrinterRedirection 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、WarnAboutPrinterRedirection 屬性
- WarnAboutPrinterRedirection 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、WarnAboutPrinterRedirection 屬性
- WarnAboutPrinterRedirection 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、WarnAboutPrinterRedirection 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable4.put_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.get_WarnAboutPrinterRedirection
- IMsRdpClientNonScriptable5.put_WarnAboutPrinterRedirection
- MsRdpClient6.WarnAboutPrinterRedirection
- MsRdpClient7.WarnAboutPrinterRedirection
- MsRdpClient8.WarnAboutPrinterRedirection
- MsRdpClient9.WarnAboutPrinterRedirection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24e2fa93995946e741caa76f1ee5b84be79d9c90
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317299"
---
# <a name="imsrdpclientnonscriptable4warnaboutprinterredirection-property"></a><span data-ttu-id="89a77-116">IMsRdpClientNonScriptable4：： WarnAboutPrinterRedirection 屬性</span><span class="sxs-lookup"><span data-stu-id="89a77-116">IMsRdpClientNonScriptable4::WarnAboutPrinterRedirection property</span></span>

<span data-ttu-id="89a77-117">控制重新導向對話方塊是否會在啟動會話之前顯示有關印表機重新導向的訊息。</span><span class="sxs-lookup"><span data-stu-id="89a77-117">Controls whether the redirection dialog box displays a message about printer redirection before starting a session.</span></span>

<span data-ttu-id="89a77-118">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="89a77-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="89a77-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="89a77-119">Syntax</span></span>


```C++
HRESULT put_WarnAboutPrinterRedirection(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutPrinterRedirection(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a><span data-ttu-id="89a77-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="89a77-120">Property value</span></span>

<span data-ttu-id="89a77-121">設定 [重新導向] 對話方塊是否顯示有關印表機重新導向的訊息。</span><span class="sxs-lookup"><span data-stu-id="89a77-121">Sets whether the redirection dialog box displays a message about printer redirection.</span></span>

## <a name="error-codes"></a><span data-ttu-id="89a77-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="89a77-122">Error codes</span></span>

<span data-ttu-id="89a77-123">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="89a77-123">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="89a77-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="89a77-124">Requirements</span></span>



| <span data-ttu-id="89a77-125">需求</span><span class="sxs-lookup"><span data-stu-id="89a77-125">Requirement</span></span> | <span data-ttu-id="89a77-126">值</span><span class="sxs-lookup"><span data-stu-id="89a77-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a77-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="89a77-127">Minimum supported client</span></span><br/> | <span data-ttu-id="89a77-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="89a77-128">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="89a77-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="89a77-129">Minimum supported server</span></span><br/> | <span data-ttu-id="89a77-130">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="89a77-130">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="89a77-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="89a77-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="89a77-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89a77-132"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="89a77-133">DLL</span><span class="sxs-lookup"><span data-stu-id="89a77-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89a77-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89a77-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="89a77-135">IID</span><span class="sxs-lookup"><span data-stu-id="89a77-135">IID</span></span><br/>                      | <span data-ttu-id="89a77-136">IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="89a77-136">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="89a77-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="89a77-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89a77-138">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="89a77-138">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="89a77-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="89a77-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





