---
title: IMsRdpClientAdvancedSettings5 RedirectPOSDevices 屬性
description: 設定或抓取服務裝置重新導向點的設定。
ms.assetid: 2614048e-244d-4dea-96fb-bb8c563a29f9
ms.tgt_platform: multiple
keywords:
- RedirectPOSDevices 屬性遠端桌面服務
- RedirectPOSDevices 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，RedirectPOSDevices 屬性
- RedirectPOSDevices 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，RedirectPOSDevices 屬性
- RedirectPOSDevices 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，RedirectPOSDevices 屬性
- RedirectPOSDevices 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，RedirectPOSDevices 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings5.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings6.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings7.put_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.get_RedirectPOSDevices
- IMsRdpClientAdvancedSettings8.put_RedirectPOSDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da5ceb0c1fb9751b137b5791ce9c8da1bd0cdbb9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104627"
---
# <a name="imsrdpclientadvancedsettings5redirectposdevices-property"></a><span data-ttu-id="59faa-112">IMsRdpClientAdvancedSettings5：： RedirectPOSDevices 屬性</span><span class="sxs-lookup"><span data-stu-id="59faa-112">IMsRdpClientAdvancedSettings5::RedirectPOSDevices property</span></span>

<span data-ttu-id="59faa-113">設定或抓取服務裝置重新導向點的設定。</span><span class="sxs-lookup"><span data-stu-id="59faa-113">Sets or retrieves the configuration for Point of Service device redirection.</span></span>

<span data-ttu-id="59faa-114">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="59faa-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="59faa-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="59faa-115">Syntax</span></span>


```C++
HRESULT put_RedirectPOSDevices(
  [in]  VARIANT_BOOL fRedirectPOSDevices
);

HRESULT get_RedirectPOSDevices(
  [out] VARIANT_BOOL *pfRedirectPOSDevices
);
```



## <a name="property-value"></a><span data-ttu-id="59faa-116">屬性值</span><span class="sxs-lookup"><span data-stu-id="59faa-116">Property value</span></span>

<span data-ttu-id="59faa-117">將服務裝置重新導向模式的點設定為 **TRUE** 或 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="59faa-117">Sets Point of Service device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="59faa-118">如果設定為 **TRUE**，則會啟用服務裝置重新導向模式的點。</span><span class="sxs-lookup"><span data-stu-id="59faa-118">If set to **TRUE**, Point of Service device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="59faa-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="59faa-119">Requirements</span></span>



| <span data-ttu-id="59faa-120">需求</span><span class="sxs-lookup"><span data-stu-id="59faa-120">Requirement</span></span> | <span data-ttu-id="59faa-121">值</span><span class="sxs-lookup"><span data-stu-id="59faa-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59faa-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59faa-122">Minimum supported client</span></span><br/> | <span data-ttu-id="59faa-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="59faa-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="59faa-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59faa-124">Minimum supported server</span></span><br/> | <span data-ttu-id="59faa-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="59faa-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="59faa-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="59faa-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="59faa-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59faa-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="59faa-128">DLL</span><span class="sxs-lookup"><span data-stu-id="59faa-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="59faa-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="59faa-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="59faa-130">IID</span><span class="sxs-lookup"><span data-stu-id="59faa-130">IID</span></span><br/>                      | <span data-ttu-id="59faa-131">IID \_ IMsRdpClientAdvancedSettings5 定義為 FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="59faa-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="59faa-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59faa-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59faa-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="59faa-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="59faa-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="59faa-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="59faa-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="59faa-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="59faa-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="59faa-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





