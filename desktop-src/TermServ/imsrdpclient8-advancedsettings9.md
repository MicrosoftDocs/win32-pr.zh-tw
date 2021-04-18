---
title: IMsRdpClient8 AdvancedSettings9 屬性
description: 包含支援 IMsRdpClientAdvancedSettings8 介面的物件。
ms.assetid: eb7bf118-15e7-4a11-91b1-e48f18afb436
ms.tgt_platform: multiple
keywords:
- AdvancedSettings9 屬性遠端桌面服務
- AdvancedSettings9 屬性遠端桌面服務，IMsRdpClient8 介面
- IMsRdpClient8 介面遠端桌面服務，AdvancedSettings9 屬性
- AdvancedSettings9 屬性遠端桌面服務，IMsRdpClient9 介面
- IMsRdpClient9 介面遠端桌面服務，AdvancedSettings9 屬性
- AdvancedSettings9 屬性遠端桌面服務，IMsRdpClient10 介面
- IMsRdpClient10 介面遠端桌面服務，AdvancedSettings9 屬性
topic_type:
- apiref
api_name:
- IMsRdpClient8.AdvancedSettings9
- IMsRdpClient8.get_AdvancedSettings9
- IMsRdpClient9.AdvancedSettings9
- IMsRdpClient9.get_AdvancedSettings9
- IMsRdpClient10.AdvancedSettings9
- IMsRdpClient10.get_AdvancedSettings9
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5fce4c6f07b0c6c798d613e5312b3ae2b258c9c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969002"
---
# <a name="imsrdpclient8advancedsettings9-property"></a><span data-ttu-id="a74c6-110">IMsRdpClient8：： AdvancedSettings9 屬性</span><span class="sxs-lookup"><span data-stu-id="a74c6-110">IMsRdpClient8::AdvancedSettings9 property</span></span>

<span data-ttu-id="a74c6-111">包含支援 [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) 介面的物件。</span><span class="sxs-lookup"><span data-stu-id="a74c6-111">Contains an object that supports the [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface.</span></span>

<span data-ttu-id="a74c6-112">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="a74c6-112">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="a74c6-113">語法</span><span class="sxs-lookup"><span data-stu-id="a74c6-113">Syntax</span></span>


```C++
HRESULT get_AdvancedSettings9(
  [out, retval] IMsRdpClientAdvancedSettings8 **ppAdvSettings
);
```



## <a name="property-value"></a><span data-ttu-id="a74c6-114">屬性值</span><span class="sxs-lookup"><span data-stu-id="a74c6-114">Property value</span></span>

<span data-ttu-id="a74c6-115">表示 settings 物件的 [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="a74c6-115">An [**IMsRdpClientAdvancedSettings8**](imsrdpclientadvancedsettings8.md) interface that represents the settings object.</span></span>

## <a name="requirements"></a><span data-ttu-id="a74c6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a74c6-116">Requirements</span></span>



| <span data-ttu-id="a74c6-117">需求</span><span class="sxs-lookup"><span data-stu-id="a74c6-117">Requirement</span></span> | <span data-ttu-id="a74c6-118">值</span><span class="sxs-lookup"><span data-stu-id="a74c6-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a74c6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a74c6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a74c6-120">Windows 8</span><span class="sxs-lookup"><span data-stu-id="a74c6-120">Windows 8</span></span><br/>                                                                   |
| <span data-ttu-id="a74c6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a74c6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a74c6-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a74c6-122">Windows Server 2012</span></span><br/>                                                         |
| <span data-ttu-id="a74c6-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="a74c6-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="a74c6-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a74c6-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a74c6-125">DLL</span><span class="sxs-lookup"><span data-stu-id="a74c6-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a74c6-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a74c6-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="a74c6-127">IID</span><span class="sxs-lookup"><span data-stu-id="a74c6-127">IID</span></span><br/>                      | <span data-ttu-id="a74c6-128">IID \_ IMsRdpClient8 定義為4247E044-9271-43A9-BC49-E2AD9E855D62</span><span class="sxs-lookup"><span data-stu-id="a74c6-128">IID\_IMsRdpClient8 is defined as 4247E044-9271-43A9-BC49-E2AD9E855D62</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="a74c6-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a74c6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a74c6-130">**IMsRdpClient8**</span><span class="sxs-lookup"><span data-stu-id="a74c6-130">**IMsRdpClient8**</span></span>](imsrdpclient8.md)
</dt> <dt>

[<span data-ttu-id="a74c6-131">**IMsRdpClient9**</span><span class="sxs-lookup"><span data-stu-id="a74c6-131">**IMsRdpClient9**</span></span>](imsrdpclient9.md)
</dt> <dt>

[<span data-ttu-id="a74c6-132">**IMsRdpClient10**</span><span class="sxs-lookup"><span data-stu-id="a74c6-132">**IMsRdpClient10**</span></span>](imsrdpclient10.md)
</dt> </dl>

 

 





