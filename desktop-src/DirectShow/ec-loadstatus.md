---
description: 開啟網路檔案時，通知應用程式的進度。
ms.assetid: 022b87e5-76af-4253-9485-97140f294938
title: 'EC_LOADSTATUS (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc06022a9774d851cabff6a18c0f8808f62f14f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999685"
---
# <a name="ec_loadstatus"></a><span data-ttu-id="b4663-103">EC \_ LOADSTATUS</span><span class="sxs-lookup"><span data-stu-id="b4663-103">EC\_LOADSTATUS</span></span>

<span data-ttu-id="b4663-104">開啟網路檔案時，通知應用程式的進度。</span><span class="sxs-lookup"><span data-stu-id="b4663-104">Notifies the application of progress when opening a network file.</span></span>

## <a name="parameters"></a><span data-ttu-id="b4663-105">參數</span><span class="sxs-lookup"><span data-stu-id="b4663-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b4663-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="b4663-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="b4663-107">狀態碼。</span><span class="sxs-lookup"><span data-stu-id="b4663-107">Status code.</span></span> <span data-ttu-id="b4663-108">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="b4663-108">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="b4663-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="b4663-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="b4663-110">零個。</span><span class="sxs-lookup"><span data-stu-id="b4663-110">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="b4663-111">預設動作</span><span class="sxs-lookup"><span data-stu-id="b4663-111">Default Action</span></span>

<span data-ttu-id="b4663-112">無。</span><span class="sxs-lookup"><span data-stu-id="b4663-112">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="b4663-113">備註</span><span class="sxs-lookup"><span data-stu-id="b4663-113">Remarks</span></span>

<span data-ttu-id="b4663-114">[WM ASF 讀取](wm-asf-reader-filter.md)器篩選器和舊版[Windows Media 來源](windows-media-source-filter.md)篩選準則會傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="b4663-114">The [WM ASF Reader](wm-asf-reader-filter.md) filter and the legacy [Windows Media Source](windows-media-source-filter.md) filter send this event.</span></span> <span data-ttu-id="b4663-115">第一個事件參數具有下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="b4663-115">The first event parameter has one of the following values.</span></span>



| <span data-ttu-id="b4663-116">值</span><span class="sxs-lookup"><span data-stu-id="b4663-116">Value</span></span>                        | <span data-ttu-id="b4663-117">描述</span><span class="sxs-lookup"><span data-stu-id="b4663-117">Description</span></span>                                    |
|------------------------------|------------------------------------------------|
| <span data-ttu-id="b4663-118">\_LOADSTATUS \_ 已關閉</span><span class="sxs-lookup"><span data-stu-id="b4663-118">AM\_LOADSTATUS\_CLOSED</span></span>       | <span data-ttu-id="b4663-119">來源篩選器已關閉檔案。</span><span class="sxs-lookup"><span data-stu-id="b4663-119">The source filter has closed the file.</span></span>         |
| <span data-ttu-id="b4663-120">AM \_ LOADSTATUS \_ 連接</span><span class="sxs-lookup"><span data-stu-id="b4663-120">AM\_LOADSTATUS\_CONNECTING</span></span>   | <span data-ttu-id="b4663-121">來源篩選器正在連接到伺服器。</span><span class="sxs-lookup"><span data-stu-id="b4663-121">The source filter is connecting to the server.</span></span> |
| <span data-ttu-id="b4663-122">AM \_ LOADSTATUS \_ LOADINGDESCR</span><span class="sxs-lookup"><span data-stu-id="b4663-122">AM\_LOADSTATUS\_LOADINGDESCR</span></span> | <span data-ttu-id="b4663-123">未使用。</span><span class="sxs-lookup"><span data-stu-id="b4663-123">Not used.</span></span>                                      |
| <span data-ttu-id="b4663-124">AM \_ LOADSTATUS \_ LOADINGMCAST</span><span class="sxs-lookup"><span data-stu-id="b4663-124">AM\_LOADSTATUS\_LOADINGMCAST</span></span> | <span data-ttu-id="b4663-125">未使用</span><span class="sxs-lookup"><span data-stu-id="b4663-125">Not used</span></span>                                       |
| <span data-ttu-id="b4663-126">AM \_ LOADSTATUS \_ 尋找</span><span class="sxs-lookup"><span data-stu-id="b4663-126">AM\_LOADSTATUS\_LOCATING</span></span>     | <span data-ttu-id="b4663-127">來源篩選器正在尋找要求的資料。</span><span class="sxs-lookup"><span data-stu-id="b4663-127">The source filter is locating requested data.</span></span>  |
| <span data-ttu-id="b4663-128">\_LOADSTATUS \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="b4663-128">AM\_LOADSTATUS\_OPEN</span></span>         | <span data-ttu-id="b4663-129">來源篩選已開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="b4663-129">The source filter has opened the file.</span></span>         |
| <span data-ttu-id="b4663-130">AM \_ LOADSTATUS \_ 開啟</span><span class="sxs-lookup"><span data-stu-id="b4663-130">AM\_LOADSTATUS\_OPENING</span></span>      | <span data-ttu-id="b4663-131">來源篩選器正在開啟檔案。</span><span class="sxs-lookup"><span data-stu-id="b4663-131">The source filter is opening the file.</span></span>         |



 

## <a name="requirements"></a><span data-ttu-id="b4663-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="b4663-132">Requirements</span></span>



| <span data-ttu-id="b4663-133">需求</span><span class="sxs-lookup"><span data-stu-id="b4663-133">Requirement</span></span> | <span data-ttu-id="b4663-134">值</span><span class="sxs-lookup"><span data-stu-id="b4663-134">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="b4663-135">標頭</span><span class="sxs-lookup"><span data-stu-id="b4663-135">Header</span></span><br/> | <dl> <span data-ttu-id="b4663-136"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="b4663-136"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b4663-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b4663-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4663-138">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="b4663-138">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="b4663-139">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="b4663-139">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




