---
title: IMsRdpClientAdvancedSettings5 PublicMode 屬性
description: 設定或抓取公用模式的設定。 公用模式防止用戶端將使用者資料快取到本機系統。
ms.assetid: dff6121a-b69c-411f-832b-29f9609f4230
ms.tgt_platform: multiple
keywords:
- PublicMode 屬性遠端桌面服務
- PublicMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，PublicMode 屬性
- PublicMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，PublicMode 屬性
- PublicMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，PublicMode 屬性
- PublicMode 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，PublicMode 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.PublicMode
- IMsRdpClientAdvancedSettings5.get_PublicMode
- IMsRdpClientAdvancedSettings5.put_PublicMode
- IMsRdpClientAdvancedSettings6.PublicMode
- IMsRdpClientAdvancedSettings6.get_PublicMode
- IMsRdpClientAdvancedSettings6.put_PublicMode
- IMsRdpClientAdvancedSettings7.PublicMode
- IMsRdpClientAdvancedSettings7.get_PublicMode
- IMsRdpClientAdvancedSettings7.put_PublicMode
- IMsRdpClientAdvancedSettings8.PublicMode
- IMsRdpClientAdvancedSettings8.get_PublicMode
- IMsRdpClientAdvancedSettings8.put_PublicMode
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9173b7685e77984a28d65129c79c9d1a09cf1458
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966495"
---
# <a name="imsrdpclientadvancedsettings5publicmode-property"></a><span data-ttu-id="72c72-113">IMsRdpClientAdvancedSettings5：:P ublicMode 屬性</span><span class="sxs-lookup"><span data-stu-id="72c72-113">IMsRdpClientAdvancedSettings5::PublicMode property</span></span>

<span data-ttu-id="72c72-114">設定或抓取公用模式的設定。</span><span class="sxs-lookup"><span data-stu-id="72c72-114">Sets or retrieves the configuration for public mode.</span></span> <span data-ttu-id="72c72-115">公用模式防止用戶端將使用者資料快取到本機系統。</span><span class="sxs-lookup"><span data-stu-id="72c72-115">Public mode prevents the client from caching user data to the local system.</span></span>

<span data-ttu-id="72c72-116">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="72c72-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="72c72-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="72c72-117">Syntax</span></span>


```C++
HRESULT put_PublicMode(
  [in]  VARIANT_BOOL fPublicMode
);

HRESULT get_PublicMode(
  [out] VARIANT_BOOL *pfPublicMode
);
```



## <a name="property-value"></a><span data-ttu-id="72c72-118">屬性值</span><span class="sxs-lookup"><span data-stu-id="72c72-118">Property value</span></span>

<span data-ttu-id="72c72-119">將公用模式設定設為 **VARIANT \_ TRUE** 或 **variant \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="72c72-119">Sets the public mode setting to **VARIANT\_TRUE** or **VARIANT\_FALSE**.</span></span> <span data-ttu-id="72c72-120">如果設定為 **VARIANT \_ TRUE**，就會啟用 public 模式設定。</span><span class="sxs-lookup"><span data-stu-id="72c72-120">If set to **VARIANT\_TRUE**, the public mode setting is enabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="72c72-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="72c72-121">Requirements</span></span>



| <span data-ttu-id="72c72-122">需求</span><span class="sxs-lookup"><span data-stu-id="72c72-122">Requirement</span></span> | <span data-ttu-id="72c72-123">值</span><span class="sxs-lookup"><span data-stu-id="72c72-123">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72c72-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72c72-124">Minimum supported client</span></span><br/> | <span data-ttu-id="72c72-125">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="72c72-125">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="72c72-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72c72-126">Minimum supported server</span></span><br/> | <span data-ttu-id="72c72-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="72c72-127">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="72c72-128">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="72c72-128">Type library</span></span><br/>             | <dl> <span data-ttu-id="72c72-129"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72c72-129"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="72c72-130">DLL</span><span class="sxs-lookup"><span data-stu-id="72c72-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72c72-131"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72c72-131"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="72c72-132">IID</span><span class="sxs-lookup"><span data-stu-id="72c72-132">IID</span></span><br/>                      | <span data-ttu-id="72c72-133">IID \_ IMsRdpClientAdvancedSettings5 定義為 FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="72c72-133">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="72c72-134">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72c72-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72c72-135">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="72c72-135">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="72c72-136">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="72c72-136">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="72c72-137">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="72c72-137">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="72c72-138">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="72c72-138">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





