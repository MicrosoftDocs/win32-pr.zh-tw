---
title: IMsRdpClient5 MsRdpClientShell 屬性
description: 抓取可編寫腳本的用戶端設定介面 IMsRdpClientShell。
ms.assetid: cc56cec4-779d-4b51-8e94-ae0dd9bae997
ms.tgt_platform: multiple
keywords:
- MsRdpClientShell 屬性遠端桌面服務
- MsRdpClientShell 屬性遠端桌面服務，IMsRdpClient5 介面
- IMsRdpClient5 介面遠端桌面服務，MsRdpClientShell 屬性
- MsRdpClientShell 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，MsRdpClientShell 屬性
- MsRdpClientShell 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，MsRdpClientShell 屬性
- MsRdpClientShell 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，MsRdpClientShell 屬性
- MsRdpClientShell 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，MsRdpClientShell 屬性
- MsRdpClientShell 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，MsRdpClientShell 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient5.MsRdpClientShell
- IMsRdpClient5.get_MsRdpClientShell
- IMsRdpClient6.MsRdpClientShell
- IMsRdpClient6.get_MsRdpClientShell
- IMsRdpClient7.MsRdpClientShell
- IMsRdpClient7.get_MsRdpClientShell
- IMsRdpClient8.MsRdpClientShell
- IMsRdpClient8.get_MsRdpClientShell
- IMsRdpClient9.MsRdpClientShell
- IMsRdpClient9.get_MsRdpClientShell
- IMsRdpClient10.MsRdpClientShell
- IMsRdpClient10.get_MsRdpClientShell
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 46129dc4736b50e8b6a650cc7a59f9b238da56e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106176"
---
# <a name="imsrdpclient5msrdpclientshell-property"></a><span data-ttu-id="68ae2-116">IMsRdpClient5：： MsRdpClientShell 屬性</span><span class="sxs-lookup"><span data-stu-id="68ae2-116">IMsRdpClient5::MsRdpClientShell property</span></span>

<span data-ttu-id="68ae2-117">抓取可編寫腳本的用戶端設定介面 [**IMsRdpClientShell**](imsrdpclientshell.md)。</span><span class="sxs-lookup"><span data-stu-id="68ae2-117">Retrieves the scriptable client setting interface [**IMsRdpClientShell**](imsrdpclientshell.md).</span></span>

<span data-ttu-id="68ae2-118">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="68ae2-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68ae2-119">語法</span><span class="sxs-lookup"><span data-stu-id="68ae2-119">Syntax</span></span>


```C++
HRESULT get_MsRdpClientShell(
  [out] IMsRdpClientShell **ppLauncher
);
```



## <a name="property-value"></a><span data-ttu-id="68ae2-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="68ae2-120">Property value</span></span>

<span data-ttu-id="68ae2-121">[**IMsRdpClientShell**](imsrdpclientshell.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="68ae2-121">An [**IMsRdpClientShell**](imsrdpclientshell.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="68ae2-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="68ae2-122">Requirements</span></span>



| <span data-ttu-id="68ae2-123">需求</span><span class="sxs-lookup"><span data-stu-id="68ae2-123">Requirement</span></span> | <span data-ttu-id="68ae2-124">值</span><span class="sxs-lookup"><span data-stu-id="68ae2-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68ae2-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68ae2-125">Minimum supported client</span></span><br/> | <span data-ttu-id="68ae2-126">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="68ae2-126">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="68ae2-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68ae2-127">Minimum supported server</span></span><br/> | <span data-ttu-id="68ae2-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68ae2-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="68ae2-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="68ae2-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="68ae2-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68ae2-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68ae2-131">DLL</span><span class="sxs-lookup"><span data-stu-id="68ae2-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68ae2-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68ae2-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68ae2-133">IID</span><span class="sxs-lookup"><span data-stu-id="68ae2-133">IID</span></span><br/>                      | <span data-ttu-id="68ae2-134">IID \_ IMsRdpClient5 定義為4eb5335b-6429-477d-b922-e06a28ecd8bf</span><span class="sxs-lookup"><span data-stu-id="68ae2-134">IID\_IMsRdpClient5 is defined as 4eb5335b-6429-477d-b922-e06a28ecd8bf</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="68ae2-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68ae2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68ae2-136">**IMsRdpClient5**</span><span class="sxs-lookup"><span data-stu-id="68ae2-136">**IMsRdpClient5**</span></span>](imsrdpclient5.md)
</dt> <dt>

[<span data-ttu-id="68ae2-137">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="68ae2-137">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="68ae2-138">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="68ae2-138">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="68ae2-139">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="68ae2-139">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="68ae2-140">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="68ae2-140">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="68ae2-141">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="68ae2-141">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





