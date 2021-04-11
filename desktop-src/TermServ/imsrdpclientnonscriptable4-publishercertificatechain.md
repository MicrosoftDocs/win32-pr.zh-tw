---
title: IMsRdpClientNonScriptable4 PublisherCertificateChain 屬性
description: 控制發行者的憑證鏈。 此鏈會儲存在類型為 VT BYREF 的變數中 \_ ，其中包含指向 CERT \_ 鏈 \_ 內容結構的指標。 如需 VT BYREF 結構的詳細資訊 \_ ，請參閱 VARIANT 和 VARIANTARG。
ms.assetid: 27ab0aff-1aef-4701-abe0-849bf32c9773
ms.tgt_platform: multiple
keywords:
- PublisherCertificateChain 屬性遠端桌面服務
- PublisherCertificateChain 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，PublisherCertificateChain 屬性
- PublisherCertificateChain 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，PublisherCertificateChain 屬性
- PublisherCertificateChain 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、PublisherCertificateChain 屬性
- PublisherCertificateChain 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、PublisherCertificateChain 屬性
- PublisherCertificateChain 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、PublisherCertificateChain 屬性
- PublisherCertificateChain 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、PublisherCertificateChain 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.PublisherCertificateChain
- IMsRdpClientNonScriptable4.get_PublisherCertificateChain
- IMsRdpClientNonScriptable4.put_PublisherCertificateChain
- IMsRdpClientNonScriptable5.PublisherCertificateChain
- IMsRdpClientNonScriptable5.get_PublisherCertificateChain
- IMsRdpClientNonScriptable5.put_PublisherCertificateChain
- MsRdpClient6.PublisherCertificateChain
- MsRdpClient7.PublisherCertificateChain
- MsRdpClient8.PublisherCertificateChain
- MsRdpClient9.PublisherCertificateChain
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7552483c2fc651ace1a9401e0555f90fb2584423
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843852"
---
# <a name="imsrdpclientnonscriptable4publishercertificatechain-property"></a><span data-ttu-id="735ac-118">IMsRdpClientNonScriptable4：:P ublisherCertificateChain 屬性</span><span class="sxs-lookup"><span data-stu-id="735ac-118">IMsRdpClientNonScriptable4::PublisherCertificateChain property</span></span>

<span data-ttu-id="735ac-119">控制發行者的憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="735ac-119">Controls the publisher certificate chain.</span></span> <span data-ttu-id="735ac-120">此鏈會儲存在類型為 **VT \_ BYREF** 的變數中，其中包含指向 [**CERT \_ 鏈 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="735ac-120">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span> <span data-ttu-id="735ac-121">如需 **VT \_ BYREF** 結構的詳細資訊，請參閱 [VARIANT 和 VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant)。</span><span class="sxs-lookup"><span data-stu-id="735ac-121">For information about **VT\_BYREF** structures, see [VARIANT and VARIANTARG](/windows/win32/api/oaidl/ns-oaidl-variant).</span></span>

<span data-ttu-id="735ac-122">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="735ac-122">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="735ac-123">Syntax</span><span class="sxs-lookup"><span data-stu-id="735ac-123">Syntax</span></span>


```C++
HRESULT put_PublisherCertificateChain(
  [in]  VARIANT *pVarCert
);

HRESULT get_PublisherCertificateChain(
  [out] VARIANT *pVarCert
);
```



## <a name="property-value"></a><span data-ttu-id="735ac-124">屬性值</span><span class="sxs-lookup"><span data-stu-id="735ac-124">Property value</span></span>

<span data-ttu-id="735ac-125">設定發行者憑證鏈。</span><span class="sxs-lookup"><span data-stu-id="735ac-125">Sets the publisher certificate chain.</span></span> <span data-ttu-id="735ac-126">此鏈會儲存在類型為 **VT \_ BYREF** 的變數中，其中包含指向 [**CERT \_ 鏈 \_ 內容**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="735ac-126">The chain is stored in a variant of type **VT\_BYREF** that contains a pointer to a [**CERT\_CHAIN\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context) structure.</span></span>

## <a name="error-codes"></a><span data-ttu-id="735ac-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="735ac-127">Error codes</span></span>

<span data-ttu-id="735ac-128">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="735ac-128">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="735ac-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="735ac-129">Requirements</span></span>



| <span data-ttu-id="735ac-130">需求</span><span class="sxs-lookup"><span data-stu-id="735ac-130">Requirement</span></span> | <span data-ttu-id="735ac-131">值</span><span class="sxs-lookup"><span data-stu-id="735ac-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="735ac-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="735ac-132">Minimum supported client</span></span><br/> | <span data-ttu-id="735ac-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="735ac-133">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="735ac-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="735ac-134">Minimum supported server</span></span><br/> | <span data-ttu-id="735ac-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="735ac-135">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="735ac-136">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="735ac-136">Type library</span></span><br/>             | <dl> <span data-ttu-id="735ac-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="735ac-137"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="735ac-138">DLL</span><span class="sxs-lookup"><span data-stu-id="735ac-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="735ac-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="735ac-139"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="735ac-140">IID</span><span class="sxs-lookup"><span data-stu-id="735ac-140">IID</span></span><br/>                      | <span data-ttu-id="735ac-141">IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="735ac-141">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="735ac-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="735ac-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="735ac-143">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="735ac-143">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="735ac-144">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="735ac-144">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

