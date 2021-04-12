---
title: IMsTscAxEvents OnAuthenticationWarningDismissed 方法
description: 在 ActiveX 控制項顯示驗證對話方塊之後呼叫 (例如，[憑證錯誤] 對話方塊) 。
ms.assetid: bf5dbe4a-9129-47b3-9808-ed09d9010099
ms.tgt_platform: multiple
keywords:
- OnAuthenticationWarningDismissed 方法遠端桌面服務
- OnAuthenticationWarningDismissed 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnAuthenticationWarningDismissed 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDismissed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86bdadfdbc8e0a1387a1f3aaf712188689d0f808
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384581"
---
# <a name="imstscaxeventsonauthenticationwarningdismissed-method"></a><span data-ttu-id="9eb1c-106">IMsTscAxEvents：： OnAuthenticationWarningDismissed 方法</span><span class="sxs-lookup"><span data-stu-id="9eb1c-106">IMsTscAxEvents::OnAuthenticationWarningDismissed method</span></span>

<span data-ttu-id="9eb1c-107">在 ActiveX 控制項顯示驗證對話方塊之後呼叫 (例如，[憑證錯誤] 對話方塊) 。</span><span class="sxs-lookup"><span data-stu-id="9eb1c-107">Called after an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="9eb1c-108">語法</span><span class="sxs-lookup"><span data-stu-id="9eb1c-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDismissed();
```



## <a name="parameters"></a><span data-ttu-id="9eb1c-109">參數</span><span class="sxs-lookup"><span data-stu-id="9eb1c-109">Parameters</span></span>

<span data-ttu-id="9eb1c-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="9eb1c-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9eb1c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9eb1c-111">Return value</span></span>

<span data-ttu-id="9eb1c-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="9eb1c-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9eb1c-113">備註</span><span class="sxs-lookup"><span data-stu-id="9eb1c-113">Remarks</span></span>

<span data-ttu-id="9eb1c-114">如有需要，您可以使用 [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)介面的 [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md)屬性來還原可能已在 [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md)方法中完成的任何父代。</span><span class="sxs-lookup"><span data-stu-id="9eb1c-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to revert any parenting that may have been done in the [**OnAuthenticationWarningDisplayed**](imstscaxevents-onauthenticationwarningdisplayed.md) method.</span></span>

<span data-ttu-id="9eb1c-115">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="9eb1c-115">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9eb1c-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9eb1c-116">Requirements</span></span>



| <span data-ttu-id="9eb1c-117">需求</span><span class="sxs-lookup"><span data-stu-id="9eb1c-117">Requirement</span></span> | <span data-ttu-id="9eb1c-118">值</span><span class="sxs-lookup"><span data-stu-id="9eb1c-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9eb1c-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9eb1c-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9eb1c-120">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9eb1c-120">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="9eb1c-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9eb1c-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9eb1c-122">Windows Server 2008、Windows Server 2008 SP1</span><span class="sxs-lookup"><span data-stu-id="9eb1c-122">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="9eb1c-123">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="9eb1c-123">Type library</span></span><br/>             | <dl> <span data-ttu-id="9eb1c-124"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb1c-124"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9eb1c-125">DLL</span><span class="sxs-lookup"><span data-stu-id="9eb1c-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9eb1c-126"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9eb1c-126"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="9eb1c-127">IID</span><span class="sxs-lookup"><span data-stu-id="9eb1c-127">IID</span></span><br/>                      | <span data-ttu-id="9eb1c-128">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="9eb1c-128">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="9eb1c-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9eb1c-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9eb1c-130">**OnAuthenticationWarningDisplayed**</span><span class="sxs-lookup"><span data-stu-id="9eb1c-130">**OnAuthenticationWarningDisplayed**</span></span>](imstscaxevents-onauthenticationwarningdisplayed.md)
</dt> <dt>

[<span data-ttu-id="9eb1c-131">**UIParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="9eb1c-131">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="9eb1c-132">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="9eb1c-132">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





