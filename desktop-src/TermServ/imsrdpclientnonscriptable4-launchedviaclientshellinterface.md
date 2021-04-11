---
title: IMsRdpClientNonScriptable4 LaunchedViaClientShellInterface 屬性
description: 指定使用者是否使用遠端桌面 Web 存取 (RD Web 存取) 介面啟動用戶端控制項。
ms.assetid: bf72c375-0eec-49c7-9f9a-c7545a95bdce
ms.tgt_platform: multiple
keywords:
- LaunchedViaClientShellInterface 屬性遠端桌面服務
- LaunchedViaClientShellInterface 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，MsRdpClient5 物件
- MsRdpClient5 物件遠端桌面服務、LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，MsRdpClient6 物件
- MsRdpClient6 物件遠端桌面服務、LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，MsRdpClient7 物件
- MsRdpClient7 物件遠端桌面服務、LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，MsRdpClient8 物件
- MsRdpClient8 物件遠端桌面服務、LaunchedViaClientShellInterface 屬性
- LaunchedViaClientShellInterface 屬性遠端桌面服務，MsRdpClient9 物件
- MsRdpClient9 物件遠端桌面服務、LaunchedViaClientShellInterface 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable4.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable4.put_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.get_LaunchedViaClientShellInterface
- IMsRdpClientNonScriptable5.put_LaunchedViaClientShellInterface
- MsRdpClient5.LaunchedViaClientShellInterface
- MsRdpClient6.LaunchedViaClientShellInterface
- MsRdpClient7.LaunchedViaClientShellInterface
- MsRdpClient8.LaunchedViaClientShellInterface
- MsRdpClient9.LaunchedViaClientShellInterface
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d5854a4e75be455035fd9a123418bd486932379
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934580"
---
# <a name="imsrdpclientnonscriptable4launchedviaclientshellinterface-property"></a><span data-ttu-id="73fd9-118">IMsRdpClientNonScriptable4：： LaunchedViaClientShellInterface 屬性</span><span class="sxs-lookup"><span data-stu-id="73fd9-118">IMsRdpClientNonScriptable4::LaunchedViaClientShellInterface property</span></span>

<span data-ttu-id="73fd9-119">指定使用者是否使用遠端桌面 Web 存取 (RD Web 存取) 介面啟動用戶端控制項。</span><span class="sxs-lookup"><span data-stu-id="73fd9-119">Specifies whether the user launched the client control by using the Remote Desktop Web Access (RD Web Access) interface.</span></span>

<span data-ttu-id="73fd9-120">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="73fd9-120">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="73fd9-121">Syntax</span><span class="sxs-lookup"><span data-stu-id="73fd9-121">Syntax</span></span>


```C++
HRESULT put_LaunchedViaClientShellInterface(
  [in]  VARIANT_BOOL fLaunchedViaClientShellInterface
);

HRESULT get_LaunchedViaClientShellInterface(
  [out]  VARIANT_BOOL *pfLaunchedViaClientShellInterface
);
```



## <a name="property-value"></a><span data-ttu-id="73fd9-122">屬性值</span><span class="sxs-lookup"><span data-stu-id="73fd9-122">Property value</span></span>

<span data-ttu-id="73fd9-123">設定 **LaunchedViaClientShellInterface** 屬性。</span><span class="sxs-lookup"><span data-stu-id="73fd9-123">Sets the **LaunchedViaClientShellInterface** property.</span></span>

## <a name="error-codes"></a><span data-ttu-id="73fd9-124">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="73fd9-124">Error codes</span></span>

<span data-ttu-id="73fd9-125">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="73fd9-125">Returns **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="73fd9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="73fd9-126">Requirements</span></span>



| <span data-ttu-id="73fd9-127">需求</span><span class="sxs-lookup"><span data-stu-id="73fd9-127">Requirement</span></span> | <span data-ttu-id="73fd9-128">值</span><span class="sxs-lookup"><span data-stu-id="73fd9-128">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="73fd9-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="73fd9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="73fd9-130">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="73fd9-130">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="73fd9-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="73fd9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="73fd9-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="73fd9-132">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="73fd9-133">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="73fd9-133">Type library</span></span><br/>             | <dl> <span data-ttu-id="73fd9-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73fd9-134"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="73fd9-135">DLL</span><span class="sxs-lookup"><span data-stu-id="73fd9-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73fd9-136"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="73fd9-136"><dt>MsTscAx.dll</dt></span></span> </dl>   |
| <span data-ttu-id="73fd9-137">IID</span><span class="sxs-lookup"><span data-stu-id="73fd9-137">IID</span></span><br/>                      | <span data-ttu-id="73fd9-138">IMsRdpClientNonScriptable4 定義為 f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span><span class="sxs-lookup"><span data-stu-id="73fd9-138">IMsRdpClientNonScriptable4 is defined as f50fa8aa-1c7d-4f59-b15c-a90cacae1fcb</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="73fd9-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="73fd9-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73fd9-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="73fd9-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="73fd9-141">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="73fd9-141">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> </dl>

 

 





