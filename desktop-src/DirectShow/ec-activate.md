---
description: 正在啟用或停用影片視窗。
ms.assetid: 2e004899-bb2b-4127-b606-e2a979275836
title: 'EC_ACTI加值稅E (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81e48adb3ae98af172664b807386c615d34b6b22
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977735"
---
# <a name="ec_activate"></a><span data-ttu-id="47a6f-103">EC \_ 啟用</span><span class="sxs-lookup"><span data-stu-id="47a6f-103">EC\_ACTIVATE</span></span>

<span data-ttu-id="47a6f-104">正在啟用或停用影片視窗。</span><span class="sxs-lookup"><span data-stu-id="47a6f-104">A video window is being activated or deactivated.</span></span>

## <a name="parameters"></a><span data-ttu-id="47a6f-105">參數</span><span class="sxs-lookup"><span data-stu-id="47a6f-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47a6f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="47a6f-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="47a6f-107">如果視窗已啟用，則 (**BOOL**) **TRUE** ; 如果停用視窗，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="47a6f-107">(**BOOL**) **TRUE** if the window is activated, or **FALSE** if the window is deactivated.</span></span>

</dd> <dt>

<span data-ttu-id="47a6f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="47a6f-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="47a6f-109"> (**IUnknown** \*) 轉譯器的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面指標。</span><span class="sxs-lookup"><span data-stu-id="47a6f-109">(**IUnknown**\*) Pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="47a6f-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="47a6f-110">Default Action</span></span>

<span data-ttu-id="47a6f-111">篩選圖形管理員會透過 [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) 介面設定焦點。</span><span class="sxs-lookup"><span data-stu-id="47a6f-111">The filter graph manager sets the focus, through the [**IResourceManager**](/windows/desktop/api/Strmif/nn-strmif-iresourcemanager) interface.</span></span> <span data-ttu-id="47a6f-112">它不會將事件通知傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="47a6f-112">It does not send the event notification to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="47a6f-113">備註</span><span class="sxs-lookup"><span data-stu-id="47a6f-113">Remarks</span></span>

<span data-ttu-id="47a6f-114">影片轉譯器會在每次啟動或停用其視窗時傳送此事件 (也就是在收到 WM \_ ACTI加值稅EAPP 訊息) 時。</span><span class="sxs-lookup"><span data-stu-id="47a6f-114">A video renderer sends this event whenever its window is activated or deactivated (that is, when it receives a WM\_ACTIVATEAPP message).</span></span> <span data-ttu-id="47a6f-115">視窗啟用或停用可能發生，因為視窗已取得或遺失焦點，或轉譯器在全螢幕模式與視窗模式之間切換。</span><span class="sxs-lookup"><span data-stu-id="47a6f-115">Window activation or deactivation can occur because the window has gained or lost focus, or because the renderer has switched between full-screen mode and windowed mode.</span></span>

<span data-ttu-id="47a6f-116">此事件可讓篩選圖形管理員配置相依于視窗焦點的資源，例如音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="47a6f-116">This event enables the filter graph manager to allocate resources that depend on window focus, such as audio devices.</span></span>

## <a name="requirements"></a><span data-ttu-id="47a6f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="47a6f-117">Requirements</span></span>



| <span data-ttu-id="47a6f-118">需求</span><span class="sxs-lookup"><span data-stu-id="47a6f-118">Requirement</span></span> | <span data-ttu-id="47a6f-119">值</span><span class="sxs-lookup"><span data-stu-id="47a6f-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="47a6f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="47a6f-120">Header</span></span><br/> | <dl> <span data-ttu-id="47a6f-121"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="47a6f-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="47a6f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47a6f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47a6f-123">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="47a6f-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="47a6f-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="47a6f-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




