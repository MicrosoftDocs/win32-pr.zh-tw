---
title: IMsRdpClient5 AdvancedSettings6 屬性
description: 捕獲 IMsRdpClientAdvancedSettings5 介面。
ms.assetid: b6a4efcf-87c3-438c-b6de-8a497ee5939d
ms.tgt_platform: multiple
keywords:
- AdvancedSettings6 屬性遠端桌面服務
- AdvancedSettings6 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，AdvancedSettings6 屬性
- AdvancedSettings6 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，AdvancedSettings6 屬性
- AdvancedSettings6 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，AdvancedSettings6 屬性
- AdvancedSettings6 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，AdvancedSettings6 屬性
- AdvancedSettings6 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，AdvancedSettings6 屬性
- AdvancedSettings6 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，AdvancedSettings6 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient5.AdvancedSettings6
- IMsRdpClient5.get_AdvancedSettings6
- IMsRdpClient6.AdvancedSettings6
- IMsRdpClient6.get_AdvancedSettings6
- IMsRdpClient7.AdvancedSettings6
- IMsRdpClient7.get_AdvancedSettings6
- IMsRdpClient8.AdvancedSettings6
- IMsRdpClient8.get_AdvancedSettings6
- IMsRdpClient9.AdvancedSettings6
- IMsRdpClient9.get_AdvancedSettings6
- IMsRdpClient10.AdvancedSettings6
- IMsRdpClient10.get_AdvancedSettings6
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b93d2395ec7e673e50023867f4602eea5c2d9fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844311"
---
# <a name="imsrdpclient5advancedsettings6-property"></a><span data-ttu-id="8a8f3-116">IMsRdpClient5：： AdvancedSettings6 屬性</span><span class="sxs-lookup"><span data-stu-id="8a8f3-116">IMsRdpClient5::AdvancedSettings6 property</span></span>

<span data-ttu-id="8a8f3-117">捕獲 [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="8a8f3-117">Retrieves the [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="8a8f3-118">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="8a8f3-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a8f3-119">語法</span><span class="sxs-lookup"><span data-stu-id="8a8f3-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings6(
  [out] IMsRdpClientAdvancedSettings5 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="8a8f3-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="8a8f3-120">Property value</span></span>

<span data-ttu-id="8a8f3-121">[**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="8a8f3-121">An [**IMsRdpClientAdvancedSettings5**](imsrdpclientadvancedsettings-interface.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a8f3-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a8f3-122">Requirements</span></span>



| <span data-ttu-id="8a8f3-123">需求</span><span class="sxs-lookup"><span data-stu-id="8a8f3-123">Requirement</span></span> | <span data-ttu-id="8a8f3-124">值</span><span class="sxs-lookup"><span data-stu-id="8a8f3-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8a8f3-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8a8f3-125">Minimum supported client</span></span><br/> | <span data-ttu-id="8a8f3-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="8a8f3-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="8a8f3-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8a8f3-127">Minimum supported server</span></span><br/> | <span data-ttu-id="8a8f3-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8a8f3-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="8a8f3-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="8a8f3-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="8a8f3-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a8f3-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a8f3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="8a8f3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8a8f3-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a8f3-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="8a8f3-133">IID</span><span class="sxs-lookup"><span data-stu-id="8a8f3-133">IID</span></span><br/>                      | <span data-ttu-id="8a8f3-134">IID \_ IMsRdpClient5 定義為4eb5335b-6429-477d-b922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="8a8f3-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="8a8f3-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a8f3-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a8f3-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="8a8f3-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="8a8f3-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="8a8f3-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="8a8f3-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="8a8f3-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="8a8f3-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="8a8f3-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="8a8f3-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="8a8f3-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="8a8f3-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="8a8f3-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





