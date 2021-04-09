---
title: IMsRdpClientAdvancedSettings3 ConnectionBarShowMinimizeButton 屬性
description: 指定是否要在連接列上顯示 [最小化] 按鈕。
ms.assetid: 3ad89f25-f1ff-4bfc-ae86-09603058c9b5
ms.tgt_platform: multiple
keywords:
- ConnectionBarShowMinimizeButton 屬性遠端桌面服務
- ConnectionBarShowMinimizeButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings3 介面
- IMsRdpClientAdvancedSettings3 介面遠端桌面服務，ConnectionBarShowMinimizeButton 屬性
- ConnectionBarShowMinimizeButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，ConnectionBarShowMinimizeButton 屬性
- ConnectionBarShowMinimizeButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，ConnectionBarShowMinimizeButton 屬性
- ConnectionBarShowMinimizeButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，ConnectionBarShowMinimizeButton 屬性
- ConnectionBarShowMinimizeButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，ConnectionBarShowMinimizeButton 屬性
- ConnectionBarShowMinimizeButton 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，ConnectionBarShowMinimizeButton 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings3.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings3.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings4.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings5.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings6.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings7.put_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.get_ConnectionBarShowMinimizeButton
- IMsRdpClientAdvancedSettings8.put_ConnectionBarShowMinimizeButton
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3cb600a853e4bc2dea7c693e676f992db85f48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685535"
---
# <a name="imsrdpclientadvancedsettings3connectionbarshowminimizebutton-property"></a><span data-ttu-id="c7a07-116">IMsRdpClientAdvancedSettings3：： ConnectionBarShowMinimizeButton 屬性</span><span class="sxs-lookup"><span data-stu-id="c7a07-116">IMsRdpClientAdvancedSettings3::ConnectionBarShowMinimizeButton property</span></span>

<span data-ttu-id="c7a07-117">指定是否要在連接列上顯示 [ **最小化** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="c7a07-117">Specifies whether to display the **Minimize** button on the connection bar.</span></span>

<span data-ttu-id="c7a07-118">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a07-118">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7a07-119">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7a07-119">Syntax</span></span>


```C++
HRESULT put_ConnectionBarShowMinimizeButton(
  [in]  VARIANT_BOOL fShowMinimize
);

HRESULT get_ConnectionBarShowMinimizeButton(
  [out] VARIANT_BOOL *pfShowMinimize
);
```



## <a name="property-value"></a><span data-ttu-id="c7a07-120">屬性值</span><span class="sxs-lookup"><span data-stu-id="c7a07-120">Property value</span></span>

<span data-ttu-id="c7a07-121">將此參數設定 **為 variant \_ TRUE** 以顯示 **最小化** 按鈕，並將設為 **Variant \_ FALSE** 以停用 [ **最小化** ] 按鈕的顯示。</span><span class="sxs-lookup"><span data-stu-id="c7a07-121">Set this parameter to **VARIANT\_TRUE** to display the **Minimize** button, and to **VARIANT\_FALSE** to disable the display of the **Minimize** button.</span></span>

## <a name="error-codes"></a><span data-ttu-id="c7a07-122">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="c7a07-122">Error codes</span></span>

<span data-ttu-id="c7a07-123">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="c7a07-123">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="c7a07-124">備註</span><span class="sxs-lookup"><span data-stu-id="c7a07-124">Remarks</span></span>

<span data-ttu-id="c7a07-125">連接控制項時無法設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="c7a07-125">This property cannot be set while the control is connected.</span></span>

<span data-ttu-id="c7a07-126">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="c7a07-126">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c7a07-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c7a07-127">Requirements</span></span>



| <span data-ttu-id="c7a07-128">需求</span><span class="sxs-lookup"><span data-stu-id="c7a07-128">Requirement</span></span> | <span data-ttu-id="c7a07-129">值</span><span class="sxs-lookup"><span data-stu-id="c7a07-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c7a07-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c7a07-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c7a07-131">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c7a07-131">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="c7a07-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c7a07-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c7a07-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c7a07-133">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="c7a07-134">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="c7a07-134">Type library</span></span><br/>             | <dl> <span data-ttu-id="c7a07-135"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7a07-135"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c7a07-136">DLL</span><span class="sxs-lookup"><span data-stu-id="c7a07-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c7a07-137"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c7a07-137"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="c7a07-138">IID</span><span class="sxs-lookup"><span data-stu-id="c7a07-138">IID</span></span><br/>                      | <span data-ttu-id="c7a07-139">IID \_ IMsRdpClientAdvancedSettings3 定義為19cd856b-c542-4c53-acee-f127e3be1a59</span><span class="sxs-lookup"><span data-stu-id="c7a07-139">IID\_IMsRdpClientAdvancedSettings3 is defined as 19cd856b-c542-4c53-acee-f127e3be1a59</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="c7a07-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c7a07-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c7a07-141">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="c7a07-141">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="c7a07-142">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="c7a07-142">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="c7a07-143">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="c7a07-143">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="c7a07-144">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="c7a07-144">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="c7a07-145">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="c7a07-145">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="c7a07-146">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="c7a07-146">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> </dl>

 

 





