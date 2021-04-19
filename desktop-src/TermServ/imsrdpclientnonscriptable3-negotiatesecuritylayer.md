---
title: IMsRdpClientNonScriptable3 NegotiateSecurityLayer 屬性
description: 指定或抓取是否已啟用連線的協商安全性層級。
ms.assetid: 7fc9e3c7-0723-48c4-8d29-5f68a24a522c
ms.tgt_platform: multiple
keywords:
- NegotiateSecurityLayer 屬性遠端桌面服務
- NegotiateSecurityLayer 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、NegotiateSecurityLayer 屬性
- NegotiateSecurityLayer 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、NegotiateSecurityLayer 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable3.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable4.put_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.get_NegotiateSecurityLayer
- IMsRdpClientNonScriptable5.put_NegotiateSecurityLayer
- MsRdpClient5.NegotiateSecurityLayer
- MsRdpClient6.NegotiateSecurityLayer
- MsRdpClient7.NegotiateSecurityLayer
- MsRdpClient8.NegotiateSecurityLayer
- MsRdpClient9.NegotiateSecurityLayer
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e64533615c780cd6e3703be85363684e537b784a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967338"
---
# <a name="imsrdpclientnonscriptable3negotiatesecuritylayer-property"></a><span data-ttu-id="bbdb0-120">IMsRdpClientNonScriptable3：： NegotiateSecurityLayer 屬性</span><span class="sxs-lookup"><span data-stu-id="bbdb0-120">IMsRdpClientNonScriptable3::NegotiateSecurityLayer property</span></span>

<span data-ttu-id="bbdb0-121">指定或抓取是否已啟用連線的協商安全性層級。</span><span class="sxs-lookup"><span data-stu-id="bbdb0-121">Specifies or retrieves whether the negotiation security layer is enabled for the connection.</span></span>

<span data-ttu-id="bbdb0-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bbdb0-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bbdb0-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="bbdb0-123">Syntax</span></span>


```C++
HRESULT put_NegotiateSecurityLayer(
  [in]  VARIANT_BOOL fNegotiate
);

HRESULT get_NegotiateSecurityLayer(
  [out] VARIANT_BOOL *pfNegotiate
);
```



## <a name="property-value"></a><span data-ttu-id="bbdb0-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="bbdb0-124">Property value</span></span>

<span data-ttu-id="bbdb0-125">指定是否要啟用安全性層的協商。</span><span class="sxs-lookup"><span data-stu-id="bbdb0-125">Specifies whether to enable negotiation of the security layer.</span></span>

## <a name="remarks"></a><span data-ttu-id="bbdb0-126">備註</span><span class="sxs-lookup"><span data-stu-id="bbdb0-126">Remarks</span></span>

<span data-ttu-id="bbdb0-127">如果這個屬性設定為 **VARIANT \_ FALSE** ，且網路層級驗證在用戶端作業系統上啟用了 (NLA) ，用戶端將不會協商安全性層級，而是會使用 NLA 來保護 RDP 連接。</span><span class="sxs-lookup"><span data-stu-id="bbdb0-127">If this property is set to **VARIANT\_FALSE** and Network Level Authentication (NLA) is enabled on the client operating system, the client will not negotiate the security layer and instead, it will use NLA to secure the RDP connection.</span></span> <span data-ttu-id="bbdb0-128">如果這個屬性設定為 **VARIANT \_ TRUE**，用戶端就會在 NLA 和基本 RDP 安全性之間進行協調。</span><span class="sxs-lookup"><span data-stu-id="bbdb0-128">If this property is set to **VARIANT\_TRUE**, then the client will negotiate between NLA and basic RDP security.</span></span>

> [!Note]  
> <span data-ttu-id="bbdb0-129">只有在連接到執行 Windows Vista 或更新版本作業系統的遠端桌面工作階段主機 (RD 工作階段主機) 伺服器時，才可以停用安全性層級的協商。</span><span class="sxs-lookup"><span data-stu-id="bbdb0-129">Disabling security layer negotiation is only possible when connecting to a Remote Desktop Session Host (RD Session Host) server running Windows Vista or later operating systems.</span></span> <span data-ttu-id="bbdb0-130">如果已啟用此屬性，且用戶端嘗試連線到執行舊版作業系統的 RD 工作階段主機伺服器，連接將會失敗。</span><span class="sxs-lookup"><span data-stu-id="bbdb0-130">If this property is enabled and the client attempts to connect to an RD Session Host server running an earlier operating system, the connection will fail.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="bbdb0-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="bbdb0-131">Requirements</span></span>



| <span data-ttu-id="bbdb0-132">需求</span><span class="sxs-lookup"><span data-stu-id="bbdb0-132">Requirement</span></span> | <span data-ttu-id="bbdb0-133">值</span><span class="sxs-lookup"><span data-stu-id="bbdb0-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbdb0-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bbdb0-134">Minimum supported client</span></span><br/> | <span data-ttu-id="bbdb0-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bbdb0-135">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="bbdb0-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bbdb0-136">Minimum supported server</span></span><br/> | <span data-ttu-id="bbdb0-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bbdb0-137">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="bbdb0-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bbdb0-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="bbdb0-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbdb0-139"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="bbdb0-140">DLL</span><span class="sxs-lookup"><span data-stu-id="bbdb0-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bbdb0-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bbdb0-141"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="bbdb0-142">IID</span><span class="sxs-lookup"><span data-stu-id="bbdb0-142">IID</span></span><br/>                      | <span data-ttu-id="bbdb0-143">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="bbdb0-143">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bbdb0-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bbdb0-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bbdb0-145">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="bbdb0-145">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="bbdb0-146">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="bbdb0-146">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="bbdb0-147">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="bbdb0-147">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





