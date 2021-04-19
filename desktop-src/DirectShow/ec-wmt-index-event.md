---
description: 當應用程式使用 WM ASF 寫入器篩選器來編制 Windows Media 視訊檔案的索引時傳送。
ms.assetid: e5f69aa1-f9b0-4403-acab-25d1f971a876
title: 'EC_WMT_INDEX_EVENT (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dc28e10b1d0e4a559bb10fbc521e232d08e08b54
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977507"
---
# <a name="ec_wmt_index_event-dshowh"></a><span data-ttu-id="dd91b-103">EC_WMT_INDEX_EVENT (Dshow) </span><span class="sxs-lookup"><span data-stu-id="dd91b-103">EC_WMT_INDEX_EVENT (Dshow.h)</span></span>

<span data-ttu-id="dd91b-104">當應用程式使用 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器來編制 Windows Media 視訊檔案的索引時傳送。</span><span class="sxs-lookup"><span data-stu-id="dd91b-104">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) filter to index Windows Media Video files.</span></span>

## <a name="parameters"></a><span data-ttu-id="dd91b-105">參數</span><span class="sxs-lookup"><span data-stu-id="dd91b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dd91b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="dd91b-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="dd91b-107">可以是下列其中一項 **WMT \_ 狀態** 消息。</span><span class="sxs-lookup"><span data-stu-id="dd91b-107">Can be one of the following **WMT\_STATUS** messages.</span></span>



| <span data-ttu-id="dd91b-108">值</span><span class="sxs-lookup"><span data-stu-id="dd91b-108">Value</span></span>                | <span data-ttu-id="dd91b-109">描述</span><span class="sxs-lookup"><span data-stu-id="dd91b-109">Description</span></span>              |
|----------------------|--------------------------|
| <span data-ttu-id="dd91b-110">WMT \_ 已開始</span><span class="sxs-lookup"><span data-stu-id="dd91b-110">WMT\_STARTED</span></span>         | <span data-ttu-id="dd91b-111">索引已開始。</span><span class="sxs-lookup"><span data-stu-id="dd91b-111">Indexing has begun.</span></span>      |
| <span data-ttu-id="dd91b-112">WMT \_ 已關閉</span><span class="sxs-lookup"><span data-stu-id="dd91b-112">WMT\_CLOSED</span></span>          | <span data-ttu-id="dd91b-113">索引已完成。</span><span class="sxs-lookup"><span data-stu-id="dd91b-113">Indexing has completed.</span></span>  |
| <span data-ttu-id="dd91b-114">WMT \_ 索引 \_ 進度</span><span class="sxs-lookup"><span data-stu-id="dd91b-114">WMT\_INDEX\_PROGRESS</span></span> | <span data-ttu-id="dd91b-115">正在編制索引。</span><span class="sxs-lookup"><span data-stu-id="dd91b-115">Indexing is in progress.</span></span> |



 

</dd> <dt>

<span data-ttu-id="dd91b-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="dd91b-116"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="dd91b-117">如果 *lParam1* 是 WMT \_ CLOSED 或 WMT \_ 開始，則 *lParam2* 為零。</span><span class="sxs-lookup"><span data-stu-id="dd91b-117">If *lParam1* is WMT\_CLOSED or WMT\_STARTED, then *lParam2* is zero.</span></span> <span data-ttu-id="dd91b-118">如果 *lParam1* 是 WMT \_ INDEX \_ 進度，則 *lParam2* 為 **DWORD** ，會以總下載大小的百分比指定目前的進度。</span><span class="sxs-lookup"><span data-stu-id="dd91b-118">If *lParam1* is WMT\_INDEX\_PROGRESS, then *lParam2* is a **DWORD** that specifies the current progress as a percentage of the total download size.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="dd91b-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd91b-119">Requirements</span></span>



| <span data-ttu-id="dd91b-120">需求</span><span class="sxs-lookup"><span data-stu-id="dd91b-120">Requirement</span></span> | <span data-ttu-id="dd91b-121">值</span><span class="sxs-lookup"><span data-stu-id="dd91b-121">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="dd91b-122">標頭</span><span class="sxs-lookup"><span data-stu-id="dd91b-122">Header</span></span><br/> | <dl> <span data-ttu-id="dd91b-123"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="dd91b-123"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dd91b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dd91b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd91b-125">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="dd91b-125">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="dd91b-126">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="dd91b-126">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




