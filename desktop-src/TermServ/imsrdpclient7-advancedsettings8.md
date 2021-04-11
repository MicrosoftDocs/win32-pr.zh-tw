---
title: IMsRdpClient7 AdvancedSettings8 屬性
description: 抓取支援 IMsRdpClientAdvancedSettings7 介面的物件。
ms.assetid: e3bb3b74-52db-4ec2-999c-9d12c24f65be
ms.tgt_platform: multiple
keywords:
- AdvancedSettings8 屬性遠端桌面服務
- AdvancedSettings8 屬性遠端桌面服務，IMsRdpClient7 介面
- IMsRdpClient7 介面遠端桌面服務，AdvancedSettings8 屬性
- AdvancedSettings8 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，AdvancedSettings8 屬性
- AdvancedSettings8 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，AdvancedSettings8 屬性
- AdvancedSettings8 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，AdvancedSettings8 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient7.AdvancedSettings8
- IMsRdpClient7.get_AdvancedSettings8
- IMsRdpClient8.AdvancedSettings8
- IMsRdpClient8.get_AdvancedSettings8
- IMsRdpClient9.AdvancedSettings8
- IMsRdpClient9.get_AdvancedSettings8
- IMsRdpClient10.AdvancedSettings8
- IMsRdpClient10.get_AdvancedSettings8
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 887306216682ba1555739a4258b8337694fabe0d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094039"
---
# <a name="imsrdpclient7advancedsettings8-property"></a><span data-ttu-id="03548-112">IMsRdpClient7：： AdvancedSettings8 屬性</span><span class="sxs-lookup"><span data-stu-id="03548-112">IMsRdpClient7::AdvancedSettings8 property</span></span>

<span data-ttu-id="03548-113">抓取支援 [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="03548-113">Retrieves an object that supports the [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface.</span></span>

<span data-ttu-id="03548-114">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="03548-114">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="03548-115">語法</span><span class="sxs-lookup"><span data-stu-id="03548-115">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings8(
  [out, retval] IMsRdpClientAdvancedSettings7 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="03548-116">屬性值</span><span class="sxs-lookup"><span data-stu-id="03548-116">Property value</span></span>

<span data-ttu-id="03548-117">接收物件之 [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) 介面指標的位址。</span><span class="sxs-lookup"><span data-stu-id="03548-117">The address of an [**IMsRdpClientAdvancedSettings7**](imsrdpclientadvancedsettings7.md) interface pointer that receives the object.</span></span>

## <a name="requirements"></a><span data-ttu-id="03548-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="03548-118">Requirements</span></span>



| <span data-ttu-id="03548-119">需求</span><span class="sxs-lookup"><span data-stu-id="03548-119">Requirement</span></span> | <span data-ttu-id="03548-120">值</span><span class="sxs-lookup"><span data-stu-id="03548-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="03548-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="03548-121">Minimum supported client</span></span><br/> | <span data-ttu-id="03548-122">Windows 7</span><span class="sxs-lookup"><span data-stu-id="03548-122">Windows 7</span></span><br/>                                                                   |
| <span data-ttu-id="03548-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="03548-123">Minimum supported server</span></span><br/> | <span data-ttu-id="03548-124">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="03548-124">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="03548-125">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="03548-125">Type library</span></span><br/>             | <dl> <span data-ttu-id="03548-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03548-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="03548-127">DLL</span><span class="sxs-lookup"><span data-stu-id="03548-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03548-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="03548-128"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="03548-129">IID</span><span class="sxs-lookup"><span data-stu-id="03548-129">IID</span></span><br/>                      | <span data-ttu-id="03548-130">IID \_ IMsRdpClient7 定義為 b2a5b5ce-3461-444a-91d4-add26d070638</span><span class="sxs-lookup"><span data-stu-id="03548-130">IID\_IMsRdpClient7 is defined as b2a5b5ce-3461-444a-91d4-add26d070638</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="03548-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="03548-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03548-132">**IMsRdpClient7**</span><span class="sxs-lookup"><span data-stu-id="03548-132">**IMsRdpClient7**</span></span>](imsrdpclient7.md)
</dt> <dt>

[<span data-ttu-id="03548-133">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="03548-133">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="03548-134">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="03548-134">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="03548-135">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="03548-135">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





