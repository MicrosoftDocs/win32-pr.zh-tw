---
description: 圖形正在緩衝處理資料，或已停止緩衝資料。
ms.assetid: 39e8b151-0323-42b3-99f0-3dcd230925c8
title: 'EC_BUFFERING_DATA (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1395a10458abd7a29fdb65e7ab55fba62328d6d5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994306"
---
# <a name="ec_buffering_data"></a><span data-ttu-id="08a44-103">EC \_ 緩衝 \_ 資料</span><span class="sxs-lookup"><span data-stu-id="08a44-103">EC\_BUFFERING\_DATA</span></span>

<span data-ttu-id="08a44-104">圖形正在緩衝處理資料，或已停止緩衝資料。</span><span class="sxs-lookup"><span data-stu-id="08a44-104">The graph is buffering data, or has stopped buffering data.</span></span>

## <a name="parameters"></a><span data-ttu-id="08a44-105">參數</span><span class="sxs-lookup"><span data-stu-id="08a44-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08a44-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="08a44-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="08a44-107">如果圖形正在開始緩衝區， (**BOOL**) **TRUE** ; 如果圖形已停止緩衝，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="08a44-107">(**BOOL**) **TRUE** if the graph is starting to buffer, or **FALSE** if the graph has stopped buffering.</span></span>

</dd> <dt>

<span data-ttu-id="08a44-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="08a44-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="08a44-109">零個。</span><span class="sxs-lookup"><span data-stu-id="08a44-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="08a44-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="08a44-110">Default Action</span></span>

<span data-ttu-id="08a44-111">無。</span><span class="sxs-lookup"><span data-stu-id="08a44-111">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="08a44-112">備註</span><span class="sxs-lookup"><span data-stu-id="08a44-112">Remarks</span></span>

<span data-ttu-id="08a44-113">如果篩選準則需要從外部來源緩衝資料，則可以傳送此事件。</span><span class="sxs-lookup"><span data-stu-id="08a44-113">A filter can send this event if it needs to buffer data from an external source.</span></span> <span data-ttu-id="08a44-114"> (例如，可能是從網路載入資料。 ) 應用程式可以使用此事件來調整其使用者介面。</span><span class="sxs-lookup"><span data-stu-id="08a44-114">(For example, it might be loading data from a network.) The application can use this event to adjust its user interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="08a44-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="08a44-115">Requirements</span></span>



| <span data-ttu-id="08a44-116">需求</span><span class="sxs-lookup"><span data-stu-id="08a44-116">Requirement</span></span> | <span data-ttu-id="08a44-117">值</span><span class="sxs-lookup"><span data-stu-id="08a44-117">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="08a44-118">標頭</span><span class="sxs-lookup"><span data-stu-id="08a44-118">Header</span></span><br/> | <dl> <span data-ttu-id="08a44-119"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="08a44-119"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08a44-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="08a44-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08a44-121">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="08a44-121">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="08a44-122">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="08a44-122">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




