---
description: 執行圖形的非同步命令失敗。
ms.assetid: 0bfcf4b4-b35a-4593-9956-8e1e8c9139cb
title: 'EC_ERROR_STILLPLAYING (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1d1c99db8c6b332ad4531f04171d960c5cfa9824
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989702"
---
# <a name="ec_error_stillplaying"></a><span data-ttu-id="731ce-103">EC \_ 錯誤 \_ STILLPLAYING</span><span class="sxs-lookup"><span data-stu-id="731ce-103">EC\_ERROR\_STILLPLAYING</span></span>

<span data-ttu-id="731ce-104">執行圖形的非同步命令失敗。</span><span class="sxs-lookup"><span data-stu-id="731ce-104">An asynchronous command to run the graph has failed.</span></span>

## <a name="parameters"></a><span data-ttu-id="731ce-105">參數</span><span class="sxs-lookup"><span data-stu-id="731ce-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="731ce-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="731ce-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="731ce-107"> (**HRESULT**) 失敗之作業的失敗碼。</span><span class="sxs-lookup"><span data-stu-id="731ce-107">(**HRESULT**) Failure code of the operation that failed.</span></span>

</dd> <dt>

<span data-ttu-id="731ce-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="731ce-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="731ce-109">零個。</span><span class="sxs-lookup"><span data-stu-id="731ce-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="731ce-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="731ce-110">Default Action</span></span>

<span data-ttu-id="731ce-111">無。</span><span class="sxs-lookup"><span data-stu-id="731ce-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="731ce-112">備註</span><span class="sxs-lookup"><span data-stu-id="731ce-112">Remarks</span></span>

<span data-ttu-id="731ce-113">如果篩選圖形管理員發出的非同步執行命令失敗，則會將此事件傳送至應用程式。</span><span class="sxs-lookup"><span data-stu-id="731ce-113">If the filter graph manager issues an asynchronous run command that fails, it sends this event to the application.</span></span> <span data-ttu-id="731ce-114">圖形仍處於執行中狀態。</span><span class="sxs-lookup"><span data-stu-id="731ce-114">The graph remains in a running state.</span></span> <span data-ttu-id="731ce-115">基礎篩選準則的狀態不確定。</span><span class="sxs-lookup"><span data-stu-id="731ce-115">The state of the underlying filters is indeterminate.</span></span> <span data-ttu-id="731ce-116">某些篩選器可能正在執行，其他篩選器可能不會執行。</span><span class="sxs-lookup"><span data-stu-id="731ce-116">Some filters might be running, others might not.</span></span>

## <a name="requirements"></a><span data-ttu-id="731ce-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="731ce-117">Requirements</span></span>



| <span data-ttu-id="731ce-118">需求</span><span class="sxs-lookup"><span data-stu-id="731ce-118">Requirement</span></span> | <span data-ttu-id="731ce-119">值</span><span class="sxs-lookup"><span data-stu-id="731ce-119">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="731ce-120">標頭</span><span class="sxs-lookup"><span data-stu-id="731ce-120">Header</span></span><br/> | <dl> <span data-ttu-id="731ce-121"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="731ce-121"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="731ce-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="731ce-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="731ce-123">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="731ce-123">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="731ce-124">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="731ce-124">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




