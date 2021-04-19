---
description: 資料流程中發生錯誤，但是資料流程仍在播放中。
ms.assetid: ff155c01-22ba-46dd-85b8-05eabf956908
title: 'EC_STREAM_ERROR_STILLPLAYING (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5db74a9f16a0ca01ce74e6d94df50cc402221aaf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984026"
---
# <a name="ec_stream_error_stillplaying"></a><span data-ttu-id="69908-103">EC \_ 資料流程 \_ 錯誤 \_ STILLPLAYING</span><span class="sxs-lookup"><span data-stu-id="69908-103">EC\_STREAM\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="69908-104">資料流程中發生錯誤，但是資料流程仍在播放中。</span><span class="sxs-lookup"><span data-stu-id="69908-104">An error occurred in a stream, but the stream is still playing.</span></span>

## <a name="parameters"></a><span data-ttu-id="69908-105">參數</span><span class="sxs-lookup"><span data-stu-id="69908-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69908-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="69908-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="69908-107"> (**HRESULT**) 失敗之作業的失敗碼。</span><span class="sxs-lookup"><span data-stu-id="69908-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="69908-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="69908-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="69908-109"> (**DWORD**) 次要錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="69908-109">(**DWORD**) Minor error code.</span></span> <span data-ttu-id="69908-110">此值通常是零。</span><span class="sxs-lookup"><span data-stu-id="69908-110">This value is usually zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="69908-111">預設動作</span><span class="sxs-lookup"><span data-stu-id="69908-111">Default Action</span></span>

<span data-ttu-id="69908-112">無。</span><span class="sxs-lookup"><span data-stu-id="69908-112">None.</span></span> <span data-ttu-id="69908-113">應用程式必須決定是否要停止圖形。</span><span class="sxs-lookup"><span data-stu-id="69908-113">The application must decide whether to stop the graph.</span></span>

## <a name="requirements"></a><span data-ttu-id="69908-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="69908-114">Requirements</span></span>



| <span data-ttu-id="69908-115">需求</span><span class="sxs-lookup"><span data-stu-id="69908-115">Requirement</span></span> | <span data-ttu-id="69908-116">值</span><span class="sxs-lookup"><span data-stu-id="69908-116">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69908-117">標頭</span><span class="sxs-lookup"><span data-stu-id="69908-117">Header</span></span><br/> | <dl> <span data-ttu-id="69908-118"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="69908-118"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69908-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="69908-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69908-120">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="69908-120">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="69908-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="69908-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




