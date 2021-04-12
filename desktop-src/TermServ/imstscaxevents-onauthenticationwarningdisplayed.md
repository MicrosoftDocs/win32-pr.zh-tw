---
title: IMsTscAxEvents OnAuthenticationWarningDisplayed 方法
description: 在 ActiveX 控制項顯示驗證對話方塊之前呼叫 (例如，) [憑證錯誤] 對話方塊。
ms.assetid: ce307e5f-5e26-4041-bbd5-6871c0678da4
ms.tgt_platform: multiple
keywords:
- OnAuthenticationWarningDisplayed 方法遠端桌面服務
- OnAuthenticationWarningDisplayed 方法遠端桌面服務，IMsTscAxEvents 介面
- IMsTscAxEvents 介面遠端桌面服務，OnAuthenticationWarningDisplayed 方法
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAuthenticationWarningDisplayed
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 33307adf103536cce5841effe2843a7c48fda357
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094476"
---
# <a name="imstscaxeventsonauthenticationwarningdisplayed-method"></a><span data-ttu-id="802f6-106">IMsTscAxEvents：： OnAuthenticationWarningDisplayed 方法</span><span class="sxs-lookup"><span data-stu-id="802f6-106">IMsTscAxEvents::OnAuthenticationWarningDisplayed method</span></span>

<span data-ttu-id="802f6-107">在 ActiveX 控制項顯示驗證對話方塊之前呼叫 (例如，) [憑證錯誤] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="802f6-107">Called before an ActiveX control displays an authentication dialog box (for example, the certificate error dialog box).</span></span>

## <a name="syntax"></a><span data-ttu-id="802f6-108">語法</span><span class="sxs-lookup"><span data-stu-id="802f6-108">Syntax</span></span>


```C++
void OnAuthenticationWarningDisplayed();
```



## <a name="parameters"></a><span data-ttu-id="802f6-109">參數</span><span class="sxs-lookup"><span data-stu-id="802f6-109">Parameters</span></span>

<span data-ttu-id="802f6-110">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="802f6-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="802f6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="802f6-111">Return value</span></span>

<span data-ttu-id="802f6-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="802f6-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="802f6-113">備註</span><span class="sxs-lookup"><span data-stu-id="802f6-113">Remarks</span></span>

<span data-ttu-id="802f6-114">如有需要，您可以使用 [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md)介面的 [ [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) ] 屬性，以確保顯示的 [強制回應驗證] 對話方塊會以指定的視窗作為父系 (這可能是在 [驗證] 對話方塊顯示) 時，防止使用者使用其他對話方塊的必要動作。</span><span class="sxs-lookup"><span data-stu-id="802f6-114">If needed, the [**UIParentWindowHandle**](imsrdpclientnonscriptable2-uiparentwindowhandle.md) property of the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface can be used to ensure that the modal authentication dialog to be displayed will be parented by a specified window (this may be necessary to prevent users from using other dialog boxes while the authentication dialog box is displayed).</span></span> <span data-ttu-id="802f6-115">根據預設，父系是 ActiveX 控制項視窗。</span><span class="sxs-lookup"><span data-stu-id="802f6-115">By default, the parent is the ActiveX control window.</span></span>

<span data-ttu-id="802f6-116">如需遠端桌面網頁連線的詳細資訊，請參閱 [遠端桌面網頁連線的需求](requirements-for-remote-desktop-web-connection.md)。</span><span class="sxs-lookup"><span data-stu-id="802f6-116">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="802f6-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="802f6-117">Requirements</span></span>



| <span data-ttu-id="802f6-118">需求</span><span class="sxs-lookup"><span data-stu-id="802f6-118">Requirement</span></span> | <span data-ttu-id="802f6-119">值</span><span class="sxs-lookup"><span data-stu-id="802f6-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="802f6-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="802f6-120">Minimum supported client</span></span><br/> | <span data-ttu-id="802f6-121">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="802f6-121">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="802f6-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="802f6-122">Minimum supported server</span></span><br/> | <span data-ttu-id="802f6-123">Windows Server 2008、Windows Server 2008 SP1</span><span class="sxs-lookup"><span data-stu-id="802f6-123">Windows Server 2008, Windows Server 2008 with SP1</span></span><br/>                           |
| <span data-ttu-id="802f6-124">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="802f6-124">Type library</span></span><br/>             | <dl> <span data-ttu-id="802f6-125"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="802f6-125"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="802f6-126">DLL</span><span class="sxs-lookup"><span data-stu-id="802f6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="802f6-127"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="802f6-127"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="802f6-128">IID</span><span class="sxs-lookup"><span data-stu-id="802f6-128">IID</span></span><br/>                      | <span data-ttu-id="802f6-129">IMsTscAxEvents 定義為336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span><span class="sxs-lookup"><span data-stu-id="802f6-129">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="802f6-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="802f6-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="802f6-131">**OnAuthenticationWarningDismissed**</span><span class="sxs-lookup"><span data-stu-id="802f6-131">**OnAuthenticationWarningDismissed**</span></span>](imstscaxevents-onauthenticationwarningdismissed.md)
</dt> <dt>

[<span data-ttu-id="802f6-132">**UIParentWindowHandle**</span><span class="sxs-lookup"><span data-stu-id="802f6-132">**UIParentWindowHandle**</span></span>](imsrdpclientnonscriptable2-uiparentwindowhandle.md)
</dt> <dt>

[<span data-ttu-id="802f6-133">**IMsTscAxEvents**</span><span class="sxs-lookup"><span data-stu-id="802f6-133">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

 





