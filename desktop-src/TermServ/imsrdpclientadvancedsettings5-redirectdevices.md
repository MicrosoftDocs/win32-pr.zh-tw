---
title: IMsRdpClientAdvancedSettings5 RedirectDevices 屬性
description: 設定或抓取裝置重新導向的設定。
ms.assetid: bf989ca0-5c79-4a73-a32b-51ef97ca0dff
ms.tgt_platform: multiple
keywords:
- RedirectDevices 屬性遠端桌面服務
- RedirectDevices 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，RedirectDevices 屬性
- RedirectDevices 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，RedirectDevices 屬性
- RedirectDevices 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，RedirectDevices 屬性
- RedirectDevices 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，RedirectDevices 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.RedirectDevices
- IMsRdpClientAdvancedSettings5.get_RedirectDevices
- IMsRdpClientAdvancedSettings5.put_RedirectDevices
- IMsRdpClientAdvancedSettings6.RedirectDevices
- IMsRdpClientAdvancedSettings6.get_RedirectDevices
- IMsRdpClientAdvancedSettings6.put_RedirectDevices
- IMsRdpClientAdvancedSettings7.RedirectDevices
- IMsRdpClientAdvancedSettings7.get_RedirectDevices
- IMsRdpClientAdvancedSettings7.put_RedirectDevices
- IMsRdpClientAdvancedSettings8.RedirectDevices
- IMsRdpClientAdvancedSettings8.get_RedirectDevices
- IMsRdpClientAdvancedSettings8.put_RedirectDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab1eec96b5d4fde20add891cc742c76c14ebe7ed
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106967529"
---
# <a name="imsrdpclientadvancedsettings5redirectdevices-property"></a><span data-ttu-id="bd545-112">IMsRdpClientAdvancedSettings5：： RedirectDevices 屬性</span><span class="sxs-lookup"><span data-stu-id="bd545-112">IMsRdpClientAdvancedSettings5::RedirectDevices property</span></span>

<span data-ttu-id="bd545-113">設定或抓取裝置重新導向的設定。</span><span class="sxs-lookup"><span data-stu-id="bd545-113">Sets or retrieves the configuration for device redirection.</span></span>

<span data-ttu-id="bd545-114">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="bd545-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="bd545-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="bd545-115">Syntax</span></span>


```C++
HRESULT put_RedirectDevices(
  [in]  VARIANT_BOOL fRedirectPnPDevices
);

HRESULT get_RedirectDevices(
  [out] VARIANT_BOOL *pfRedirectPnPDevices
);
```



## <a name="property-value"></a><span data-ttu-id="bd545-116">屬性值</span><span class="sxs-lookup"><span data-stu-id="bd545-116">Property value</span></span>

<span data-ttu-id="bd545-117">將裝置重新導向模式設定為 [ **TRUE** ] 或 [ **FALSE**]。</span><span class="sxs-lookup"><span data-stu-id="bd545-117">Sets the device redirection mode to **TRUE** or **FALSE**.</span></span> <span data-ttu-id="bd545-118">如果設定為 **TRUE**，則會啟用裝置重新導向模式。</span><span class="sxs-lookup"><span data-stu-id="bd545-118">If set to **TRUE**, device redirection mode is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd545-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd545-119">Requirements</span></span>



| <span data-ttu-id="bd545-120">需求</span><span class="sxs-lookup"><span data-stu-id="bd545-120">Requirement</span></span> | <span data-ttu-id="bd545-121">值</span><span class="sxs-lookup"><span data-stu-id="bd545-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd545-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bd545-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bd545-123">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="bd545-123">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="bd545-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bd545-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bd545-125">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="bd545-125">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="bd545-126">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="bd545-126">Type library</span></span><br/>             | <dl> <span data-ttu-id="bd545-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd545-127"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bd545-128">DLL</span><span class="sxs-lookup"><span data-stu-id="bd545-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bd545-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bd545-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="bd545-130">IID</span><span class="sxs-lookup"><span data-stu-id="bd545-130">IID</span></span><br/>                      | <span data-ttu-id="bd545-131">IID \_ IMsRdpClientAdvancedSettings5 定義為 FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="bd545-131">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd545-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd545-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd545-133">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="bd545-133">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="bd545-134">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="bd545-134">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="bd545-135">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="bd545-135">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="bd545-136">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="bd545-136">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





