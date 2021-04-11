---
title: IMsRdpClientAdvancedSettings4 AuthenticationLevel 屬性
description: 指定要用於連接的驗證層級。
ms.assetid: 09ff1508-f13d-4bb0-8458-6f5a5e099bae
ms.tgt_platform: multiple
keywords:
- AuthenticationLevel 屬性遠端桌面服務
- AuthenticationLevel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings4 介面
- IMsRdpClientAdvancedSettings4 介面遠端桌面服務，AuthenticationLevel 屬性
- AuthenticationLevel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings5 介面
- IMsRdpClientAdvancedSettings5 介面遠端桌面服務，AuthenticationLevel 屬性
- AuthenticationLevel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings6 介面
- IMsRdpClientAdvancedSettings6 介面遠端桌面服務，AuthenticationLevel 屬性
- AuthenticationLevel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings7 介面
- IMsRdpClientAdvancedSettings7 介面遠端桌面服務，AuthenticationLevel 屬性
- AuthenticationLevel 屬性遠端桌面服務，IMsRdpClientAdvancedSettings8 介面
- IMsRdpClientAdvancedSettings8 介面遠端桌面服務，AuthenticationLevel 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings4.AuthenticationLevel
- IMsRdpClientAdvancedSettings4.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings4.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.AuthenticationLevel
- IMsRdpClientAdvancedSettings5.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings5.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.AuthenticationLevel
- IMsRdpClientAdvancedSettings6.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings6.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.AuthenticationLevel
- IMsRdpClientAdvancedSettings7.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings7.put_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.AuthenticationLevel
- IMsRdpClientAdvancedSettings8.get_AuthenticationLevel
- IMsRdpClientAdvancedSettings8.put_AuthenticationLevel
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c748416650ec7e6ec3d26fe6236a254eb012d67
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843468"
---
# <a name="imsrdpclientadvancedsettings4authenticationlevel-property"></a><span data-ttu-id="18574-114">IMsRdpClientAdvancedSettings4：： AuthenticationLevel 屬性</span><span class="sxs-lookup"><span data-stu-id="18574-114">IMsRdpClientAdvancedSettings4::AuthenticationLevel property</span></span>

<span data-ttu-id="18574-115">指定要用於連接的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="18574-115">Specifies the authentication level to use for the connection.</span></span>

<span data-ttu-id="18574-116">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="18574-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="18574-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="18574-117">Syntax</span></span>


```C++
HRESULT put_AuthenticationLevel(
  [in]  UINT uiAuthLevel
);

HRESULT get_AuthenticationLevel(
  [out] UINT *puiAuthLevel
);
```



## <a name="property-value"></a><span data-ttu-id="18574-118">屬性值</span><span class="sxs-lookup"><span data-stu-id="18574-118">Property value</span></span>

<span data-ttu-id="18574-119">**AuthenticationLevel** 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="18574-119">The value of the **AuthenticationLevel** property.</span></span>

<dt>

<span data-ttu-id="18574-120">0</span><span class="sxs-lookup"><span data-stu-id="18574-120">0</span></span>
</dt> <dd>

<span data-ttu-id="18574-121">沒有伺服器的驗證。</span><span class="sxs-lookup"><span data-stu-id="18574-121">No authentication of the server.</span></span>

</dd> <dt>

<span data-ttu-id="18574-122">1</span><span class="sxs-lookup"><span data-stu-id="18574-122">1</span></span>
</dt> <dd>

<span data-ttu-id="18574-123">需要伺服器驗證，且必須順利完成，連接才能繼續。</span><span class="sxs-lookup"><span data-stu-id="18574-123">Server authentication is required and must complete successfully for the connection to proceed.</span></span>

</dd> <dt>

<span data-ttu-id="18574-124">2</span><span class="sxs-lookup"><span data-stu-id="18574-124">2</span></span>
</dt> <dd>

<span data-ttu-id="18574-125">嘗試驗證服務器。</span><span class="sxs-lookup"><span data-stu-id="18574-125">Attempt authentication of the server.</span></span> <span data-ttu-id="18574-126">如果驗證失敗，系統將會提示使用者取消連線的選項，或在沒有伺服器驗證的情況下繼續進行。</span><span class="sxs-lookup"><span data-stu-id="18574-126">If authentication fails, the user will be prompted with the option to cancel the connection or to proceed without server authentication.</span></span>

</dd> </dl>

## <a name="error-codes"></a><span data-ttu-id="18574-127">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="18574-127">Error codes</span></span>

<span data-ttu-id="18574-128">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="18574-128">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="18574-129">備註</span><span class="sxs-lookup"><span data-stu-id="18574-129">Remarks</span></span>

<span data-ttu-id="18574-130">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="18574-130">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="18574-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="18574-131">Requirements</span></span>



| <span data-ttu-id="18574-132">需求</span><span class="sxs-lookup"><span data-stu-id="18574-132">Requirement</span></span> | <span data-ttu-id="18574-133">值</span><span class="sxs-lookup"><span data-stu-id="18574-133">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="18574-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18574-134">Minimum supported client</span></span><br/> | <span data-ttu-id="18574-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="18574-135">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="18574-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18574-136">Minimum supported server</span></span><br/> | <span data-ttu-id="18574-137">Windows Server 2008、Windows Server 2008 SP1</span><span class="sxs-lookup"><span data-stu-id="18574-137">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                     |
| <span data-ttu-id="18574-138">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="18574-138">Type library</span></span><br/>             | <dl> <span data-ttu-id="18574-139"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18574-139"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="18574-140">DLL</span><span class="sxs-lookup"><span data-stu-id="18574-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18574-141"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18574-141"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="18574-142">IID</span><span class="sxs-lookup"><span data-stu-id="18574-142">IID</span></span><br/>                      | <span data-ttu-id="18574-143">IID \_ IMsRdpClientAdvancedSettings4 定義為 FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span><span class="sxs-lookup"><span data-stu-id="18574-143">IID\_IMsRdpClientAdvancedSettings4 is defined as FBA7F64E-7345-4405-AE50-FA4A763DC0DE</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="18574-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18574-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="18574-145">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="18574-145">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="18574-146">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="18574-146">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="18574-147">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="18574-147">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
</dt> <dt>

[<span data-ttu-id="18574-148">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="18574-148">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)
</dt> <dt>

[<span data-ttu-id="18574-149">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="18574-149">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> </dl>

 

 





