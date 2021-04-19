---
title: IMsRdpClient6 TransportSettings2 屬性
description: 捕獲 IMsRdpClientTransportSettings2 介面。
ms.assetid: 5cd3c745-b360-43fb-b780-c526ed539db0
ms.tgt_platform: multiple
keywords:
- TransportSettings2 屬性遠端桌面服務
- TransportSettings2 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，TransportSettings2 屬性
- TransportSettings2 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，TransportSettings2 屬性
- TransportSettings2 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，TransportSettings2 屬性
- TransportSettings2 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，TransportSettings2 屬性
- TransportSettings2 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，TransportSettings2 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient6.TransportSettings2
- IMsRdpClient6.get_TransportSettings2
- IMsRdpClient7.TransportSettings2
- IMsRdpClient7.get_TransportSettings2
- IMsRdpClient8.TransportSettings2
- IMsRdpClient8.get_TransportSettings2
- IMsRdpClient9.TransportSettings2
- IMsRdpClient9.get_TransportSettings2
- IMsRdpClient10.TransportSettings2
- IMsRdpClient10.get_TransportSettings2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91ba11975e0e065e0cfcce91eb22402153acf236
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969961"
---
# <a name="imsrdpclient6transportsettings2-property"></a><span data-ttu-id="83818-114">IMsRdpClient6：： TransportSettings2 屬性</span><span class="sxs-lookup"><span data-stu-id="83818-114">IMsRdpClient6::TransportSettings2 property</span></span>

<span data-ttu-id="83818-115">捕獲 [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="83818-115">Retrieves the [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface.</span></span>

<span data-ttu-id="83818-116">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="83818-116">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="83818-117">語法</span><span class="sxs-lookup"><span data-stu-id="83818-117">Syntax</span></span>


```C++
HRESULT get_TransportSettings2(
  [out] IMsRdpClientTransportSettings2 **ppXportSet2
);
```



## <a name="property-value"></a><span data-ttu-id="83818-118">屬性值</span><span class="sxs-lookup"><span data-stu-id="83818-118">Property value</span></span>

<span data-ttu-id="83818-119">[**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="83818-119">An [**IMsRdpClientTransportSettings2**](imsrdpclienttransportsettings2.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="83818-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="83818-120">Requirements</span></span>



| <span data-ttu-id="83818-121">需求</span><span class="sxs-lookup"><span data-stu-id="83818-121">Requirement</span></span> | <span data-ttu-id="83818-122">值</span><span class="sxs-lookup"><span data-stu-id="83818-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="83818-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="83818-123">Minimum supported client</span></span><br/> | <span data-ttu-id="83818-124">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="83818-124">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="83818-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="83818-125">Minimum supported server</span></span><br/> | <span data-ttu-id="83818-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="83818-126">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="83818-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="83818-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="83818-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83818-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="83818-129">DLL</span><span class="sxs-lookup"><span data-stu-id="83818-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="83818-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="83818-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="83818-131">IID</span><span class="sxs-lookup"><span data-stu-id="83818-131">IID</span></span><br/>                      | <span data-ttu-id="83818-132">IID \_ IMsRdpClient6 定義為 d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span><span class="sxs-lookup"><span data-stu-id="83818-132">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="83818-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="83818-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="83818-134">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="83818-134">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="83818-135">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="83818-135">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="83818-136">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="83818-136">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="83818-137">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="83818-137">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="83818-138">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="83818-138">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





