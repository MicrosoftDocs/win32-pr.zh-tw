---
title: IMsRdpClient5 RemoteProgram 屬性
description: 抓取支援 ITSRemoteProgram 介面的物件。
ms.assetid: 013f613b-af7b-4cc5-be1f-d45833806e3b
ms.tgt_platform: multiple
keywords:
- RemoteProgram 屬性遠端桌面服務
- RemoteProgram 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，RemoteProgram 屬性
- RemoteProgram 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，RemoteProgram 屬性
- RemoteProgram 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，RemoteProgram 屬性
- RemoteProgram 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，RemoteProgram 屬性
- RemoteProgram 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，RemoteProgram 屬性
- RemoteProgram 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，RemoteProgram 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient5.RemoteProgram
- IMsRdpClient5.get_RemoteProgram
- IMsRdpClient6.RemoteProgram
- IMsRdpClient6.get_RemoteProgram
- IMsRdpClient7.RemoteProgram
- IMsRdpClient7.get_RemoteProgram
- IMsRdpClient8.RemoteProgram
- IMsRdpClient8.get_RemoteProgram
- IMsRdpClient9.RemoteProgram
- IMsRdpClient9.get_RemoteProgram
- IMsRdpClient10.RemoteProgram
- IMsRdpClient10.get_RemoteProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 267e367af090a7fd70e9482406104fd0403d63f0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464689"
---
# <a name="imsrdpclient5remoteprogram-property"></a><span data-ttu-id="876a9-116">IMsRdpClient5：： RemoteProgram 屬性</span><span class="sxs-lookup"><span data-stu-id="876a9-116">IMsRdpClient5::RemoteProgram property</span></span>

<span data-ttu-id="876a9-117">抓取支援 [**ITSRemoteProgram**](itsremoteprogram.md) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="876a9-117">Retrieves an object that supports the [**ITSRemoteProgram**](itsremoteprogram.md) interface.</span></span>

<span data-ttu-id="876a9-118">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="876a9-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="876a9-119">語法</span><span class="sxs-lookup"><span data-stu-id="876a9-119">Syntax</span></span>


```C++
HRESULT get_RemoteProgram(
  [out] ITSRemoteProgram **ppRemoteProgram
);
```



## <a name="property-value"></a><span data-ttu-id="876a9-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="876a9-120">Property value</span></span>

<span data-ttu-id="876a9-121">[**ITSRemoteProgram**](itsremoteprogram.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="876a9-121">An [**ITSRemoteProgram**](itsremoteprogram.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="876a9-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="876a9-122">Requirements</span></span>



| <span data-ttu-id="876a9-123">需求</span><span class="sxs-lookup"><span data-stu-id="876a9-123">Requirement</span></span> | <span data-ttu-id="876a9-124">值</span><span class="sxs-lookup"><span data-stu-id="876a9-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="876a9-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="876a9-125">Minimum supported client</span></span><br/> | <span data-ttu-id="876a9-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="876a9-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="876a9-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="876a9-127">Minimum supported server</span></span><br/> | <span data-ttu-id="876a9-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="876a9-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="876a9-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="876a9-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="876a9-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="876a9-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="876a9-131">DLL</span><span class="sxs-lookup"><span data-stu-id="876a9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="876a9-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="876a9-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="876a9-133">IID</span><span class="sxs-lookup"><span data-stu-id="876a9-133">IID</span></span><br/>                      | <span data-ttu-id="876a9-134">IID \_ IMsRdpClient5 定義為4eb5335b-6429-477d-b922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="876a9-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="876a9-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="876a9-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="876a9-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="876a9-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="876a9-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="876a9-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="876a9-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="876a9-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="876a9-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="876a9-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="876a9-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="876a9-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="876a9-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="876a9-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





