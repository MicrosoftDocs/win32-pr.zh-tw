---
title: IMsRdpClient5 TransportSettings 屬性
description: 抓取透過腳本傳遞至 IMsRdpClientTransportSettings 介面的內容。
ms.assetid: 38f5a735-55c7-425a-835b-22f6e0900d57
ms.tgt_platform: multiple
keywords:
- TransportSettings 屬性遠端桌面服務
- TransportSettings 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，TransportSettings 屬性
- TransportSettings 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，TransportSettings 屬性
- TransportSettings 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，TransportSettings 屬性
- TransportSettings 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，TransportSettings 屬性
- TransportSettings 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，TransportSettings 屬性
- TransportSettings 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，TransportSettings 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient5.TransportSettings
- IMsRdpClient5.get_TransportSettings
- IMsRdpClient6.TransportSettings
- IMsRdpClient6.get_TransportSettings
- IMsRdpClient7.TransportSettings
- IMsRdpClient7.get_TransportSettings
- IMsRdpClient8.TransportSettings
- IMsRdpClient8.get_TransportSettings
- IMsRdpClient9.TransportSettings
- IMsRdpClient9.get_TransportSettings
- IMsRdpClient10.TransportSettings
- IMsRdpClient10.get_TransportSettings
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 077ed94253c0ebadeed775e54c4db2ae6cbacf13
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094112"
---
# <a name="imsrdpclient5transportsettings-property"></a><span data-ttu-id="28cde-116">IMsRdpClient5：： TransportSettings 屬性</span><span class="sxs-lookup"><span data-stu-id="28cde-116">IMsRdpClient5::TransportSettings property</span></span>

<span data-ttu-id="28cde-117">抓取透過腳本傳遞至 [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) 介面的內容。</span><span class="sxs-lookup"><span data-stu-id="28cde-117">Retrieves what was passed through a script to the [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface.</span></span>

<span data-ttu-id="28cde-118">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="28cde-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="28cde-119">語法</span><span class="sxs-lookup"><span data-stu-id="28cde-119">Syntax</span></span>


```C++
HRESULT get_TransportSettings(
  [out] IMsRdpClientTransportSettings **ppXportSet
);
```



## <a name="property-value"></a><span data-ttu-id="28cde-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="28cde-120">Property value</span></span>

<span data-ttu-id="28cde-121">[**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="28cde-121">An [**IMsRdpClientTransportSettings**](imsrdpclienttransportsettings.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="28cde-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="28cde-122">Requirements</span></span>



| <span data-ttu-id="28cde-123">需求</span><span class="sxs-lookup"><span data-stu-id="28cde-123">Requirement</span></span> | <span data-ttu-id="28cde-124">值</span><span class="sxs-lookup"><span data-stu-id="28cde-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="28cde-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="28cde-125">Minimum supported client</span></span><br/> | <span data-ttu-id="28cde-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="28cde-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="28cde-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="28cde-127">Minimum supported server</span></span><br/> | <span data-ttu-id="28cde-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="28cde-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="28cde-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="28cde-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="28cde-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28cde-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="28cde-131">DLL</span><span class="sxs-lookup"><span data-stu-id="28cde-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="28cde-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="28cde-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="28cde-133">IID</span><span class="sxs-lookup"><span data-stu-id="28cde-133">IID</span></span><br/>                      | <span data-ttu-id="28cde-134">IID \_ IMsRdpClient5 定義為4eb5335b-6429-477d-b922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="28cde-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="28cde-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28cde-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28cde-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="28cde-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="28cde-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="28cde-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="28cde-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="28cde-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="28cde-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="28cde-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="28cde-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="28cde-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="28cde-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="28cde-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





