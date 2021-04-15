---
title: IMsRdpClientNonScriptable2 UIParentWindowHandle 屬性
description: 設定或抓取視窗控制碼，使其成為控制項所顯示之任何對話方塊的父視窗。 如此一來，控制項所顯示的任何視窗都能針對父應用程式所顯示的任何視窗適當地進行模式回應。
ms.assetid: 5ecf1fc3-492e-4faf-89c5-7f7abb3778a0
ms.tgt_platform: multiple
keywords:
- UIParentWindowHandle 屬性遠端桌面服務
- UIParentWindowHandle 屬性遠端桌面服務，IMsRdpClientNonScriptable2 介面
- IMsRdpClientNonScriptable2 介面遠端桌面服務，UIParentWindowHandle 屬性
- UIParentWindowHandle 屬性遠端桌面服務，IMsRdpClientNonScriptable3 介面
- IMsRdpClientNonScriptable3 介面遠端桌面服務，UIParentWindowHandle 屬性
- UIParentWindowHandle 屬性遠端桌面服務，IMsRdpClientNonScriptable4 介面
- IMsRdpClientNonScriptable4 介面遠端桌面服務，UIParentWindowHandle 屬性
- UIParentWindowHandle 屬性遠端桌面服務，IMsRdpClientNonScriptable5 介面
- IMsRdpClientNonScriptable5 介面遠端桌面服務，UIParentWindowHandle 屬性
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable2.UIParentWindowHandle
- IMsRdpClientNonScriptable2.get_UIParentWindowHandle
- IMsRdpClientNonScriptable2.put_UIParentWindowHandle
- IMsRdpClientNonScriptable3.UIParentWindowHandle
- IMsRdpClientNonScriptable3.get_UIParentWindowHandle
- IMsRdpClientNonScriptable3.put_UIParentWindowHandle
- IMsRdpClientNonScriptable4.UIParentWindowHandle
- IMsRdpClientNonScriptable4.get_UIParentWindowHandle
- IMsRdpClientNonScriptable4.put_UIParentWindowHandle
- IMsRdpClientNonScriptable5.UIParentWindowHandle
- IMsRdpClientNonScriptable5.get_UIParentWindowHandle
- IMsRdpClientNonScriptable5.put_UIParentWindowHandle
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5526fd1a699c87e32c6acadd238c2144d00a10be
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464313"
---
# <a name="imsrdpclientnonscriptable2uiparentwindowhandle-property"></a><span data-ttu-id="5a625-113">IMsRdpClientNonScriptable2：： UIParentWindowHandle 屬性</span><span class="sxs-lookup"><span data-stu-id="5a625-113">IMsRdpClientNonScriptable2::UIParentWindowHandle property</span></span>

<span data-ttu-id="5a625-114">設定或抓取視窗控制碼，使其成為控制項所顯示之任何對話方塊的父視窗。</span><span class="sxs-lookup"><span data-stu-id="5a625-114">Sets or retrieves the window handle to be the parent window for any dialog boxes displayed by the control.</span></span> <span data-ttu-id="5a625-115">如此一來，控制項所顯示的任何視窗都能針對父應用程式所顯示的任何視窗適當地進行模式回應。</span><span class="sxs-lookup"><span data-stu-id="5a625-115">This allows any windows displayed by the control to be properly modal with respect to any windows displayed by the parent application.</span></span>

<span data-ttu-id="5a625-116">這是可讀寫的屬性。</span><span class="sxs-lookup"><span data-stu-id="5a625-116">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a625-117">Syntax</span><span class="sxs-lookup"><span data-stu-id="5a625-117">Syntax</span></span>


```C++
HRESULT put_UIParentWindowHandle(
  [in]  HWND hwndUIParentWindowHandle
);

HRESULT get_UIParentWindowHandle(
  [out] HWND *phwndUIParentWindowHandle
);
```



## <a name="property-value"></a><span data-ttu-id="5a625-118">屬性值</span><span class="sxs-lookup"><span data-stu-id="5a625-118">Property value</span></span>

<span data-ttu-id="5a625-119">新的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="5a625-119">The new window handle.</span></span>

## <a name="error-codes"></a><span data-ttu-id="5a625-120">錯誤碼</span><span class="sxs-lookup"><span data-stu-id="5a625-120">Error codes</span></span>

<span data-ttu-id="5a625-121">如果成功，則傳回 **S \_ OK** 。</span><span class="sxs-lookup"><span data-stu-id="5a625-121">Returns **S\_OK** if successful.</span></span>

## <a name="remarks"></a><span data-ttu-id="5a625-122">備註</span><span class="sxs-lookup"><span data-stu-id="5a625-122">Remarks</span></span>

<span data-ttu-id="5a625-123">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="5a625-123">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5a625-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a625-124">Requirements</span></span>



| <span data-ttu-id="5a625-125">需求</span><span class="sxs-lookup"><span data-stu-id="5a625-125">Requirement</span></span> | <span data-ttu-id="5a625-126">值</span><span class="sxs-lookup"><span data-stu-id="5a625-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a625-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a625-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5a625-128">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="5a625-128">Windows Vista</span></span><br/>                                                                      |
| <span data-ttu-id="5a625-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a625-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5a625-130">Windows Server 2008、Windows Server 2008 SP1</span><span class="sxs-lookup"><span data-stu-id="5a625-130">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                                  |
| <span data-ttu-id="5a625-131">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="5a625-131">Type library</span></span><br/>             | <dl> <span data-ttu-id="5a625-132"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a625-132"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5a625-133">DLL</span><span class="sxs-lookup"><span data-stu-id="5a625-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a625-134"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a625-134"><dt>MsTscAx.dll</dt></span></span> </dl>        |
| <span data-ttu-id="5a625-135">IID</span><span class="sxs-lookup"><span data-stu-id="5a625-135">IID</span></span><br/>                      | <span data-ttu-id="5a625-136">IID \_ IMsRdpClientNonScriptable2 定義為17a5e535-4072-4fa4-af32-c8d0d47345e9</span><span class="sxs-lookup"><span data-stu-id="5a625-136">IID\_IMsRdpClientNonScriptable2 is defined as 17a5e535-4072-4fa4-af32-c8d0d47345e9</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="5a625-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a625-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a625-138">**IMsRdpClientNonScriptable3**</span><span class="sxs-lookup"><span data-stu-id="5a625-138">**IMsRdpClientNonScriptable3**</span></span>](imsrdpclientnonscriptable3.md)
</dt> <dt>

[<span data-ttu-id="5a625-139">**IMsRdpClientNonScriptable4**</span><span class="sxs-lookup"><span data-stu-id="5a625-139">**IMsRdpClientNonScriptable4**</span></span>](imsrdpclientnonscriptable4.md)
</dt> <dt>

[<span data-ttu-id="5a625-140">**IMsRdpClientNonScriptable5**</span><span class="sxs-lookup"><span data-stu-id="5a625-140">**IMsRdpClientNonScriptable5**</span></span>](imsrdpclientnonscriptable5.md)
</dt> <dt>

[<span data-ttu-id="5a625-141">**OnAuthenticationWarningDisplayed**</span><span class="sxs-lookup"><span data-stu-id="5a625-141">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="5a625-142">**OnAuthenticationWarningDismissed**</span><span class="sxs-lookup"><span data-stu-id="5a625-142">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="5a625-143">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="5a625-143">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> </dl>

 

 





