---
title: IMsRdpClient6 AdvancedSettings7 屬性
description: 捕獲 IMsRdpClientAdvancedSettings6 介面。
ms.assetid: 64b05c66-ac6a-4190-9df8-4a88dbc46c3f
ms.tgt_platform: multiple
keywords:
- AdvancedSettings7 屬性遠端桌面服務
- AdvancedSettings7 屬性遠端桌面服務，IMsRdpClient6 介面
- IMsRdpClient6 介面遠端桌面服務，AdvancedSettings7 屬性
- AdvancedSettings7 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，AdvancedSettings7 屬性
- AdvancedSettings7 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，AdvancedSettings7 屬性
- AdvancedSettings7 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，AdvancedSettings7 屬性
- AdvancedSettings7 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，AdvancedSettings7 屬性
- AdvancedSettings7 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、AdvancedSettings7 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient6.AdvancedSettings7
- IMsRdpClient6.get_AdvancedSettings7
- IMsRdpClient7.AdvancedSettings7
- IMsRdpClient7.get_AdvancedSettings7
- IMsRdpClient8.AdvancedSettings7
- IMsRdpClient8.get_AdvancedSettings7
- IMsRdpClient9.AdvancedSettings7
- IMsRdpClient9.get_AdvancedSettings7
- IMsRdpClient10.AdvancedSettings7
- IMsRdpClient10.get_AdvancedSettings7
- MsRdpClient6.AdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f51d364c14be3311272455e040d55f277f3fb136
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384193"
---
# <a name="imsrdpclient6advancedsettings7-property"></a><span data-ttu-id="68c96-116">IMsRdpClient6：： AdvancedSettings7 屬性</span><span class="sxs-lookup"><span data-stu-id="68c96-116">IMsRdpClient6::AdvancedSettings7 property</span></span>

<span data-ttu-id="68c96-117">捕獲 [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="68c96-117">Retrieves the [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings5.md) interface.</span></span>

<span data-ttu-id="68c96-118">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="68c96-118">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="68c96-119">語法</span><span class="sxs-lookup"><span data-stu-id="68c96-119">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings7(
  [out] IMsRdpClientAdvancedSettings6 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="68c96-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="68c96-120">Property value</span></span>

<span data-ttu-id="68c96-121">[**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md)介面指標。</span><span class="sxs-lookup"><span data-stu-id="68c96-121">An [**IMsRdpClientAdvancedSettings6**](imsrdpclientadvancedsettings6.md) interface pointer.</span></span>

## <a name="requirements"></a><span data-ttu-id="68c96-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="68c96-122">Requirements</span></span>



| <span data-ttu-id="68c96-123">需求</span><span class="sxs-lookup"><span data-stu-id="68c96-123">Requirement</span></span> | <span data-ttu-id="68c96-124">值</span><span class="sxs-lookup"><span data-stu-id="68c96-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68c96-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="68c96-125">Minimum supported client</span></span><br/> | <span data-ttu-id="68c96-126">Windows Vista SP1</span><span class="sxs-lookup"><span data-stu-id="68c96-126">Windows Vista with SP1</span></span><br/>                                                      |
| <span data-ttu-id="68c96-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="68c96-127">Minimum supported server</span></span><br/> | <span data-ttu-id="68c96-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="68c96-128">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="68c96-129">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="68c96-129">Type library</span></span><br/>             | <dl> <span data-ttu-id="68c96-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68c96-130"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68c96-131">DLL</span><span class="sxs-lookup"><span data-stu-id="68c96-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="68c96-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="68c96-132"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="68c96-133">IID</span><span class="sxs-lookup"><span data-stu-id="68c96-133">IID</span></span><br/>                      | <span data-ttu-id="68c96-134">IID \_ IMsRdpClient6 定義為 d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span><span class="sxs-lookup"><span data-stu-id="68c96-134">IID\_IMsRdpClient6 is defined as d43b7d80-8517-4b6d-9eac-96ad6800d7f2</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="68c96-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68c96-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68c96-136">**IMsRdpClient6**</span><span class="sxs-lookup"><span data-stu-id="68c96-136">**IMsRdpClient6**</span></span>](imsrdpclient6.md)
</dt> <dt>

[<span data-ttu-id="68c96-137">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="68c96-137">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="68c96-138">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="68c96-138">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="68c96-139">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="68c96-139">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="68c96-140">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="68c96-140">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





