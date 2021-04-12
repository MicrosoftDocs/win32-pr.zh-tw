---
title: IMsRdpClientNonScriptable4 MarkRdpSettingsSecure 屬性
description: 指定遠端桌面通訊協定 (RDP) 設定是否標記為安全。
ms.assetid: 04b419ed-821e-43e0-ac76-b8d6f6dfcc30
ms.tgt_platform: multiple
keywords:
- MarkRdpSettingsSecure 屬性遠端桌面服務
- MarkRdpSettingsSecure 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，MarkRdpSettingsSecure 屬性
- MarkRdpSettingsSecure 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，MarkRdpSettingsSecure 屬性
- MarkRdpSettingsSecure 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、MarkRdpSettingsSecure 屬性
- MarkRdpSettingsSecure 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、MarkRdpSettingsSecure 屬性
- MarkRdpSettingsSecure 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、MarkRdpSettingsSecure 屬性
- MarkRdpSettingsSecure 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、MarkRdpSettingsSecure 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable4.put_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.get_MarkRdpSettingsSecure
- IMsRdpClientNonScriptable5.put_MarkRdpSettingsSecure
- MsRdpClient6.MarkRdpSettingsSecure
- MsRdpClient7.MarkRdpSettingsSecure
- MsRdpClient8.MarkRdpSettingsSecure
- MsRdpClient9.MarkRdpSettingsSecure
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0b551e043432b6f6e66efbbe5a6e0f9095024a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508767"
---
# <a name="imsrdpclientnonscriptable4markrdpsettingssecure-property"></a><span data-ttu-id="0b216-116">IMsRdpClientNonScriptable4：： MarkRdpSettingsSecure 屬性</span><span class="sxs-lookup"><span data-stu-id="0b216-116">IMsRdpClientNonScriptable4::MarkRdpSettingsSecure property</span></span>

<span data-ttu-id="0b216-117">指定 [遠端桌面通訊協定](remote-desktop-protocol.md) (RDP) 設定是否標記為安全。</span><span class="sxs-lookup"><span data-stu-id="0b216-117">Specifies whether [Remote Desktop Protocol](remote-desktop-protocol.md) (RDP) settings are marked as secure.</span></span> <span data-ttu-id="0b216-118">這表示套用至控制項的設定已由協力廠商或受信任的發行者簽署。</span><span class="sxs-lookup"><span data-stu-id="0b216-118">This indicates that the settings applied to the control have been signed by a third-party or trusted publisher.</span></span>

<span data-ttu-id="0b216-119">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="0b216-119">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b216-120">Syntax</span><span class="sxs-lookup"><span data-stu-id="0b216-120">Syntax</span></span>


```C++
HRESULT put_MarkRdpSettingsSecure(
  [in]  VARIANT_BOOL fRdpSecure
);

HRESULT get_MarkRdpSettingsSecure(
  [out] VARIANT_BOOL *pfRdpSecure
);
```



## <a name="property-value"></a><span data-ttu-id="0b216-121">屬性值</span><span class="sxs-lookup"><span data-stu-id="0b216-121">Property value</span></span>

<span data-ttu-id="0b216-122">設定是否將 RDP 設定標示為安全。</span><span class="sxs-lookup"><span data-stu-id="0b216-122">Sets whether RDP settings are marked as secure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="0b216-123">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="0b216-123">Error codes</span></span>

<span data-ttu-id="0b216-124">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="0b216-124">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="0b216-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="0b216-125">Requirements</span></span>



| <span data-ttu-id="0b216-126">需求</span><span class="sxs-lookup"><span data-stu-id="0b216-126">Requirement</span></span> | <span data-ttu-id="0b216-127">值</span><span class="sxs-lookup"><span data-stu-id="0b216-127">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b216-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0b216-128">Minimum supported client</span></span><br/> | <span data-ttu-id="0b216-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0b216-129">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="0b216-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0b216-130">Minimum supported server</span></span><br/> | <span data-ttu-id="0b216-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0b216-131">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="0b216-132">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="0b216-132">Type library</span></span><br/>             | <dl> <span data-ttu-id="0b216-133"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b216-133"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="0b216-134">DLL</span><span class="sxs-lookup"><span data-stu-id="0b216-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b216-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b216-135"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="0b216-136">IID</span><span class="sxs-lookup"><span data-stu-id="0b216-136">IID</span></span><br/>                      | <span data-ttu-id="0b216-137">IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="0b216-137">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="0b216-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0b216-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b216-139">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="0b216-139">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="0b216-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="0b216-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





