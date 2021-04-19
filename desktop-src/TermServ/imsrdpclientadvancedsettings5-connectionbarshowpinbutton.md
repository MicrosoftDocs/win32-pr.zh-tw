---
title: IMsRdpClientAdvancedSettings5 ConnectionBarShowPinButton 屬性
description: 設定或抓取連接列中 [釘選] 按鈕的設定。
ms.assetid: fbb2c19b-88a7-435b-86ef-4856e194b383
ms.tgt_platform: multiple
keywords:
- ConnectionBarShowPinButton 屬性遠端桌面服務
- ConnectionBarShowPinButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，ConnectionBarShowPinButton 屬性
- ConnectionBarShowPinButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ConnectionBarShowPinButton 屬性
- ConnectionBarShowPinButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ConnectionBarShowPinButton 屬性
- ConnectionBarShowPinButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ConnectionBarShowPinButton 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowPinButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowPinButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a766bc01bc5bf773fa03e788c3089441e6c3f6f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106980287"
---
# <a name="imsrdpclientadvancedsettings5connectionbarshowpinbutton-property"></a><span data-ttu-id="77132-112">IMsRdpClientAdvancedSettings5：： ConnectionBarShowPinButton 屬性</span><span class="sxs-lookup"><span data-stu-id="77132-112">IMsRdpClientAdvancedSettings5::ConnectionBarShowPinButton property</span></span>

<span data-ttu-id="77132-113">設定或抓取連接列中 [釘選] 按鈕的設定。</span><span class="sxs-lookup"><span data-stu-id="77132-113">Sets or retrieves the configuration for the pin button in the connection bar.</span></span>

<span data-ttu-id="77132-114">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="77132-114">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="77132-115">Syntax</span><span class="sxs-lookup"><span data-stu-id="77132-115">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowPinButton(
  [in]  VARIANT_BOOL fShowPin
);

HRESULT get_ConnectionBarShowPinButton(
  [out] VARIANT_BOOL *pfShowPin
);
```



## <a name="property-value"></a><span data-ttu-id="77132-116">屬性值</span><span class="sxs-lookup"><span data-stu-id="77132-116">Property value</span></span>

<span data-ttu-id="77132-117">**TRUE** 或 **FALSE** 的布林值。</span><span class="sxs-lookup"><span data-stu-id="77132-117">A Boolean value of **TRUE** or **FALSE**.</span></span> <span data-ttu-id="77132-118">值為 **TRUE** 時，會顯示連接列中的 [釘選] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="77132-118">A value of **TRUE** shows the pin button in the connection bar.</span></span> <span data-ttu-id="77132-119">值為 **FALSE** 時，會隱藏連接列中的 [釘選] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="77132-119">A value of **FALSE** hides the pin button in the connection bar.</span></span>

## <a name="requirements"></a><span data-ttu-id="77132-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="77132-120">Requirements</span></span>



| <span data-ttu-id="77132-121">需求</span><span class="sxs-lookup"><span data-stu-id="77132-121">Requirement</span></span> | <span data-ttu-id="77132-122">值</span><span class="sxs-lookup"><span data-stu-id="77132-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77132-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="77132-123">Minimum supported client</span></span><br/> | <span data-ttu-id="77132-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="77132-124">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="77132-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="77132-125">Minimum supported server</span></span><br/> | <span data-ttu-id="77132-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="77132-126">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="77132-127">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="77132-127">Type library</span></span><br/>             | <dl> <span data-ttu-id="77132-128"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77132-128"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="77132-129">DLL</span><span class="sxs-lookup"><span data-stu-id="77132-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="77132-130"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="77132-130"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="77132-131">IID</span><span class="sxs-lookup"><span data-stu-id="77132-131">IID</span></span><br/>                      | <span data-ttu-id="77132-132">IID \_ IMsRdpClientAdvancedSettings5 定義為 FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="77132-132">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="77132-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77132-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77132-134">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="77132-134">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="77132-135">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="77132-135">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="77132-136">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="77132-136">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="77132-137">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="77132-137">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> </dl>

 

 





