---
description: 當 WM ASF 寫入器篩選器完成 multipass 編碼的前置處理時傳送。
ms.assetid: 2029afc4-419c-494a-ae52-1f84b08bcb35
title: 'EC_PREPROCESS_COMPLETE (Dshow) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba13938ac848ef37f1a2a2826372d97ff5a5d716
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000371"
---
# <a name="ec_preprocess_complete"></a><span data-ttu-id="58661-103">EC 前置處理 \_ \_ 完成</span><span class="sxs-lookup"><span data-stu-id="58661-103">EC\_PREPROCESS\_COMPLETE</span></span>

<span data-ttu-id="58661-104">當 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器完成 multipass 編碼的前置處理時傳送。</span><span class="sxs-lookup"><span data-stu-id="58661-104">Sent by the [WM ASF Writer](wm-asf-writer-filter.md) filter when it completes the pre-processing for multipass encoding.</span></span>

## <a name="parameters"></a><span data-ttu-id="58661-105">參數</span><span class="sxs-lookup"><span data-stu-id="58661-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="58661-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="58661-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="58661-107">零個。</span><span class="sxs-lookup"><span data-stu-id="58661-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="58661-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="58661-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="58661-109"> (**IUnknown** \*) 指標指向篩選的 [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)介面。</span><span class="sxs-lookup"><span data-stu-id="58661-109">(**IUnknown**\*) Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="58661-110">預設動作</span><span class="sxs-lookup"><span data-stu-id="58661-110">Default Action</span></span>

<span data-ttu-id="58661-111">無。</span><span class="sxs-lookup"><span data-stu-id="58661-111">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="58661-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="58661-112">Requirements</span></span>



| <span data-ttu-id="58661-113">需求</span><span class="sxs-lookup"><span data-stu-id="58661-113">Requirement</span></span> | <span data-ttu-id="58661-114">值</span><span class="sxs-lookup"><span data-stu-id="58661-114">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="58661-115">標頭</span><span class="sxs-lookup"><span data-stu-id="58661-115">Header</span></span><br/> | <dl> <span data-ttu-id="58661-116"><dt>Dshow。h</dt></span><span class="sxs-lookup"><span data-stu-id="58661-116"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58661-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58661-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58661-118">事件通知碼</span><span class="sxs-lookup"><span data-stu-id="58661-118">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="58661-119">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="58661-119">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




