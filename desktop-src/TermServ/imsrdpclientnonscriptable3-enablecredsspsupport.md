---
title: IMsRdpClientNonScriptable3 EnableCredSspSupport 屬性
description: 指定或抓取是否已針對此連接啟用認證安全性服務提供者 (CredSSP) 。
ms.assetid: 770da50b-2a93-4274-9b6f-c24c13f08549
ms.tgt_platform: multiple
keywords:
- EnableCredSspSupport 屬性遠端桌面服務
- EnableCredSspSupport 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，EnableCredSspSupport 屬性
- EnableCredSspSupport 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，EnableCredSspSupport 屬性
- EnableCredSspSupport 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，EnableCredSspSupport 屬性
- EnableCredSspSupport 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、EnableCredSspSupport 屬性
- EnableCredSspSupport 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、EnableCredSspSupport 屬性
- EnableCredSspSupport 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、EnableCredSspSupport 屬性
- EnableCredSspSupport 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、EnableCredSspSupport 屬性
- EnableCredSspSupport 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、EnableCredSspSupport 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.EnableCredSspSupport
- IMsRdpClientNonScriptable3.get_EnableCredSspSupport
- IMsRdpClientNonScriptable3.put_EnableCredSspSupport
- IMsRdpClientNonScriptable4.EnableCredSspSupport
- IMsRdpClientNonScriptable4.get_EnableCredSspSupport
- IMsRdpClientNonScriptable4.put_EnableCredSspSupport
- IMsRdpClientNonScriptable5.EnableCredSspSupport
- IMsRdpClientNonScriptable5.get_EnableCredSspSupport
- IMsRdpClientNonScriptable5.put_EnableCredSspSupport
- MsRdpClient5.EnableCredSspSupport
- MsRdpClient6.EnableCredSspSupport
- MsRdpClient7.EnableCredSspSupport
- MsRdpClient8.EnableCredSspSupport
- MsRdpClient9.EnableCredSspSupport
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e2330b800d15f95a7b59a01735de971dd4b212d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094483"
---
# <a name="imsrdpclientnonscriptable3enablecredsspsupport-property"></a><span data-ttu-id="d5f32-120">IMsRdpClientNonScriptable3：： EnableCredSspSupport 屬性</span><span class="sxs-lookup"><span data-stu-id="d5f32-120">IMsRdpClientNonScriptable3::EnableCredSspSupport property</span></span>

<span data-ttu-id="d5f32-121">指定或抓取是否已針對此連接啟用認證安全性服務提供者 (CredSSP) 。</span><span class="sxs-lookup"><span data-stu-id="d5f32-121">Specifies or retrieves whether the Credential Security Service Provider (CredSSP) is enabled for this connection.</span></span>

<span data-ttu-id="d5f32-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="d5f32-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d5f32-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="d5f32-123">Syntax</span></span>


```C++
HRESULT put_EnableCredSspSupport(
  [in]  VARIANT_BOOL fEnableSupport
);

HRESULT get_EnableCredSspSupport(
  [out] VARIANT_BOOL *pfEnableSupport
);
```



## <a name="property-value"></a><span data-ttu-id="d5f32-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="d5f32-124">Property value</span></span>

<span data-ttu-id="d5f32-125">指定是否啟用此連接的 CredSSP。</span><span class="sxs-lookup"><span data-stu-id="d5f32-125">Specifies whether CredSSP is enabled for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="d5f32-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="d5f32-126">Requirements</span></span>



| <span data-ttu-id="d5f32-127">需求</span><span class="sxs-lookup"><span data-stu-id="d5f32-127">Requirement</span></span> | <span data-ttu-id="d5f32-128">值</span><span class="sxs-lookup"><span data-stu-id="d5f32-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="d5f32-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d5f32-129">Minimum supported client</span></span><br/> | <span data-ttu-id="d5f32-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d5f32-130">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="d5f32-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d5f32-131">Minimum supported server</span></span><br/> | <span data-ttu-id="d5f32-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d5f32-132">Windows Server 2008</span></span><br/>                                                                |
| <span data-ttu-id="d5f32-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="d5f32-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="d5f32-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5f32-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d5f32-135">DLL</span><span class="sxs-lookup"><span data-stu-id="d5f32-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d5f32-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d5f32-136"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="d5f32-137">IID</span><span class="sxs-lookup"><span data-stu-id="d5f32-137">IID</span></span><br/>                      | <span data-ttu-id="d5f32-138">IID \_ IMsRdpClientNonScriptable3 定義為 b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="d5f32-138">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d5f32-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d5f32-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d5f32-140">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="d5f32-140">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="d5f32-141">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="d5f32-141">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="d5f32-142">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="d5f32-142">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





