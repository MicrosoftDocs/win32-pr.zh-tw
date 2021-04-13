---
title: IMsRdpClientAdvancedSettings3 ConnectionBarShowRestoreButton 屬性
description: 指定是否要在連接列上顯示 [還原] 按鈕。
ms.assetid: a56c3c05-d253-404a-bf49-9c1d804802e0
ms.tgt_platform: multiple
keywords:
- ConnectionBarShowRestoreButton 屬性遠端桌面服務
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
- ConnectionBarShowRestoreButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ConnectionBarShowRestoreButton 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowRestoreButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowRestoreButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ae83ecde31461eff9c553782b8bfa3ae760fb54
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384038"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowrestorebutton-property"></a><span data-ttu-id="44f60-116">IMsRdpClientAdvancedSettings3：： ConnectionBarShowRestoreButton 屬性</span><span class="sxs-lookup"><span data-stu-id="44f60-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowRestoreButton property</span></span>

<span data-ttu-id="44f60-117">指定是否要在連接列上顯示 [ **還原** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="44f60-117">Specifies whether to display the **Restore** button on the connection bar.</span></span>

<span data-ttu-id="44f60-118">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="44f60-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="44f60-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="44f60-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowRestoreButton(
  [in]  VARIANT_BOOL fShowRestore
);

HRESULT get_ConnectionBarShowRestoreButton(
  [out] VARIANT_BOOL *pfShowRestore
);
```



## <a name="property-value"></a><span data-ttu-id="44f60-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="44f60-120">Property value</span></span>

<span data-ttu-id="44f60-121">設定為 **[ \_ variant TRUE** ] 以顯示 [ **還原** ] 按鈕，並將設為 [ **variant \_ FALSE** ] 以停用 [ **還原** ] 按鈕的顯示。</span><span class="sxs-lookup"><span data-stu-id="44f60-121">Set to **VARIANT\_TRUE** to display the **Restore** button, and to **VARIANT\_FALSE** to disable the display of the **Restore** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="44f60-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="44f60-122">Error codes</span></span>

<span data-ttu-id="44f60-123">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="44f60-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="44f60-124">備註</span><span class="sxs-lookup"><span data-stu-id="44f60-124">Remarks</span></span>

<span data-ttu-id="44f60-125">連接控制項時無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="44f60-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="44f60-126">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="44f60-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="44f60-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="44f60-127">Requirements</span></span>



| <span data-ttu-id="44f60-128">需求</span><span class="sxs-lookup"><span data-stu-id="44f60-128">Requirement</span></span> | <span data-ttu-id="44f60-129">值</span><span class="sxs-lookup"><span data-stu-id="44f60-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44f60-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="44f60-130">Minimum supported client</span></span><br/> | <span data-ttu-id="44f60-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="44f60-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="44f60-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="44f60-132">Minimum supported server</span></span><br/> | <span data-ttu-id="44f60-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="44f60-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="44f60-134">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="44f60-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="44f60-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44f60-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="44f60-136">DLL</span><span class="sxs-lookup"><span data-stu-id="44f60-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="44f60-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="44f60-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="44f60-138">IID</span><span class="sxs-lookup"><span data-stu-id="44f60-138">IID</span></span><br/>                      | <span data-ttu-id="44f60-139">IID \_ IMsRdpClientAdvancedSettings3 定義為19cd856b-c542-4c53-acee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="44f60-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="44f60-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="44f60-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="44f60-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="44f60-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="44f60-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="44f60-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="44f60-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="44f60-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="44f60-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="44f60-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="44f60-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="44f60-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="44f60-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="44f60-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





