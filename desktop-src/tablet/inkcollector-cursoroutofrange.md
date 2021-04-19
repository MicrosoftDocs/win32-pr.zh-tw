---
description: 當資料指標離開 tablet 內容 (鄰近) 的實體偵測範圍時發生。
ms.assetid: a3a570ed-570b-4579-b120-ed5457630bc2
title: 'InkCollector. CursorOutOfRange 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0e2d6ee30a60c260d861cdc5c24e22d7b4b43b0f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989908"
---
# <a name="inkcollectorcursoroutofrange-event"></a><span data-ttu-id="c491f-103">InkCollector. CursorOutOfRange 事件</span><span class="sxs-lookup"><span data-stu-id="c491f-103">InkCollector.CursorOutOfRange event</span></span>

<span data-ttu-id="c491f-104">當資料指標離開 tablet 內容 (鄰近) 的實體偵測範圍時發生。</span><span class="sxs-lookup"><span data-stu-id="c491f-104">Occurs when the cursor leaves the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="c491f-105">語法</span><span class="sxs-lookup"><span data-stu-id="c491f-105">Syntax</span></span>


```C++
void CursorOutOfRange(
  [in] IInkCursor *Cursor
);
```



## <a name="parameters"></a><span data-ttu-id="c491f-106">參數</span><span class="sxs-lookup"><span data-stu-id="c491f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c491f-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c491f-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c491f-108">產生 **CursorOutOfRange** 事件的 [**IInkCursor 介面**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="c491f-108">The [**IInkCursor Interface**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorOutOfRange** event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c491f-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="c491f-109">Return value</span></span>

<span data-ttu-id="c491f-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="c491f-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c491f-111">備註</span><span class="sxs-lookup"><span data-stu-id="c491f-111">Remarks</span></span>

<span data-ttu-id="c491f-112">此事件方法是在 \_ IInkCollectorEvents、 \_ IInkOverlayEvents 和 \_ IInkPictureEvents 分派專用介面中定義， (具有 DISPID ICECursorOutOfRange 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="c491f-112">This event method is defined in the \_IInkCollectorEvents, \_IInkOverlayEvents, and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_ICECursorOutOfRange.</span></span>

<span data-ttu-id="c491f-113">即使在 [選取] 或 [清除] 模式中，也不只是在 [筆墨] 模式中，也會引發 **CursorOutOfRange** 事件。</span><span class="sxs-lookup"><span data-stu-id="c491f-113">The **CursorOutOfRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="c491f-114">這需要您監視編輯模式 (您負責設定) 並在解讀事件之前留意模式。</span><span class="sxs-lookup"><span data-stu-id="c491f-114">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="c491f-115">這項需求的優點是透過更清楚地瞭解平臺事件，更能自由地在平臺上進行創新。</span><span class="sxs-lookup"><span data-stu-id="c491f-115">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="c491f-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c491f-116">Requirements</span></span>



| <span data-ttu-id="c491f-117">需求</span><span class="sxs-lookup"><span data-stu-id="c491f-117">Requirement</span></span> | <span data-ttu-id="c491f-118">值</span><span class="sxs-lookup"><span data-stu-id="c491f-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c491f-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c491f-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c491f-120">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c491f-120">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="c491f-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c491f-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c491f-122">都不支援</span><span class="sxs-lookup"><span data-stu-id="c491f-122">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="c491f-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c491f-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c491f-124"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="c491f-124"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="c491f-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="c491f-125">Library</span></span><br/>                  | <dl> <span data-ttu-id="c491f-126"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c491f-126"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="c491f-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c491f-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c491f-128">**InkCollector 類別**</span><span class="sxs-lookup"><span data-stu-id="c491f-128">**InkCollector Class**</span></span>](inkcollector-class.md)
</dt> <dt>

[<span data-ttu-id="c491f-129">**CursorInRange 事件**</span><span class="sxs-lookup"><span data-stu-id="c491f-129">**CursorInRange Event**</span></span>](inkcollector-cursorinrange.md)
</dt> <dt>

[<span data-ttu-id="c491f-130">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="c491f-130">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




