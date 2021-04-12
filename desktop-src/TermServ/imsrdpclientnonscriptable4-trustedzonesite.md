---
title: IMsRdpClientNonScriptable4 TrustedZoneSite 屬性
description: 指定使用者啟動連線的網站是否位於使用者用戶端電腦的 [信任的網站] 清單中。
ms.assetid: cb7efacc-b13b-494c-ab02-35c4f914744c
ms.tgt_platform: multiple
keywords:
- TrustedZoneSite 屬性遠端桌面服務
- TrustedZoneSite 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，TrustedZoneSite 屬性
- TrustedZoneSite 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，TrustedZoneSite 屬性
- TrustedZoneSite 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、TrustedZoneSite 屬性
- TrustedZoneSite 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、TrustedZoneSite 屬性
- TrustedZoneSite 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、TrustedZoneSite 屬性
- TrustedZoneSite 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、TrustedZoneSite 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.TrustedZoneSite
- IMsRdpClientNonScriptable4.get_TrustedZoneSite
- IMsRdpClientNonScriptable4.put_TrustedZoneSite
- IMsRdpClientNonScriptable5.TrustedZoneSite
- IMsRdpClientNonScriptable5.get_TrustedZoneSite
- IMsRdpClientNonScriptable5.put_TrustedZoneSite
- MsRdpClient6.TrustedZoneSite
- MsRdpClient7.TrustedZoneSite
- MsRdpClient8.TrustedZoneSite
- MsRdpClient9.TrustedZoneSite
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d791b5eff3346f61f999ea1f4f78bc41a5acea0e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384893"
---
# <a name="imsrdpclientnonscriptable4trustedzonesite-property"></a><span data-ttu-id="5c998-116">IMsRdpClientNonScriptable4：： TrustedZoneSite 屬性</span><span class="sxs-lookup"><span data-stu-id="5c998-116">IMsRdpClientNonScriptable4::TrustedZoneSite property</span></span>

<span data-ttu-id="5c998-117">指定使用者啟動連線的網站是否位於使用者用戶端電腦的 [信任的網站] 清單中。</span><span class="sxs-lookup"><span data-stu-id="5c998-117">Specifies whether the website from which the user launched the connection is in the trusted sites list of the user's client computer.</span></span>

<span data-ttu-id="5c998-118">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5c998-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5c998-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c998-119">Syntax</span></span>


```C++
HRESULT put_TrustedZoneSite(
  [in]  VARIANT_BOOL fIsTrustedZone
);

HRESULT get_TrustedZoneSite(
  [out] VARIANT_BOOL *pfIsTrustedZone
);
```



## <a name="property-value"></a><span data-ttu-id="5c998-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="5c998-120">Property value</span></span>

<span data-ttu-id="5c998-121">設定 TrustedZoneSite 屬性。</span><span class="sxs-lookup"><span data-stu-id="5c998-121">Sets the TrustedZoneSite property.</span></span> <span data-ttu-id="5c998-122">這個方法不會影響使用者啟動連線的網站是否位於用戶端電腦的 [信任的網站] 清單中。</span><span class="sxs-lookup"><span data-stu-id="5c998-122">This method has no effect on whether the website from which the user launched the connection is in the trusted sites list of the client computer.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5c998-123">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5c998-123">Error codes</span></span>

<span data-ttu-id="5c998-124">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="5c998-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="5c998-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="5c998-125">Requirements</span></span>



| <span data-ttu-id="5c998-126">需求</span><span class="sxs-lookup"><span data-stu-id="5c998-126">Requirement</span></span> | <span data-ttu-id="5c998-127">值</span><span class="sxs-lookup"><span data-stu-id="5c998-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c998-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5c998-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5c998-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5c998-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="5c998-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5c998-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5c998-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="5c998-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="5c998-132">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5c998-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="5c998-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c998-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="5c998-134">DLL</span><span class="sxs-lookup"><span data-stu-id="5c998-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5c998-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5c998-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="5c998-136">IID</span><span class="sxs-lookup"><span data-stu-id="5c998-136">IID</span></span><br/>                      | <span data-ttu-id="5c998-137">IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="5c998-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5c998-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5c998-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5c998-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="5c998-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="5c998-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="5c998-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





