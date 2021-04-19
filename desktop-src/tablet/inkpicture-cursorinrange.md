---
description: 當游標進入 tablet 內容 (鄰近) 的實體偵測範圍時發生。
ms.assetid: e921e175-a2cf-45e6-bb81-dc82e384d3b1
title: 'InkPicture. CursorInRange 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab0dead1fa5bd89452af15a19f36a132c6843d67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985312"
---
# <a name="inkpicturecursorinrange-event"></a><span data-ttu-id="e2f61-103">InkPicture. CursorInRange 事件</span><span class="sxs-lookup"><span data-stu-id="e2f61-103">InkPicture.CursorInRange event</span></span>

<span data-ttu-id="e2f61-104">當游標進入 tablet 內容 (鄰近) 的實體偵測範圍時發生。</span><span class="sxs-lookup"><span data-stu-id="e2f61-104">Occurs when a cursor enters the physical detection range (proximity) of the tablet context.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2f61-105">語法</span><span class="sxs-lookup"><span data-stu-id="e2f61-105">Syntax</span></span>


```C++
void CursorInRange(
  [in] IInkCursor   *Cursor,
  [in] VARIANT_BOOL NewCursor,
  [in] VARIANT      ButtonsState
);
```



## <a name="parameters"></a><span data-ttu-id="e2f61-106">參數</span><span class="sxs-lookup"><span data-stu-id="e2f61-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2f61-107">資料 *指標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2f61-107">*Cursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f61-108">產生 **CursorInRange** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件。</span><span class="sxs-lookup"><span data-stu-id="e2f61-108">The [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event.</span></span>

</dd> <dt>

<span data-ttu-id="e2f61-109">*NewCursor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2f61-109">*NewCursor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f61-110">**變異 \_** 如果這是您第一次使用此筆墨收集器來與產生 **CursorInRange** 事件的 [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)物件，則為 TRUE;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="e2f61-110">**VARIANT\_TRUE** if this is the first time this ink collector has come in contact with the [**IInkCursor**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor) object that generated the **CursorInRange** event; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="e2f61-111">*ButtonsState* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2f61-111">*ButtonsState* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2f61-112">產生 **CursorInRange** 事件的資料指標之按鈕的狀態。</span><span class="sxs-lookup"><span data-stu-id="e2f61-112">The state of the buttons for the cursor that generated the **CursorInRange** event.</span></span>

<span data-ttu-id="e2f61-113">如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="e2f61-113">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2f61-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2f61-114">Return value</span></span>

<span data-ttu-id="e2f61-115">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="e2f61-115">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2f61-116">備註</span><span class="sxs-lookup"><span data-stu-id="e2f61-116">Remarks</span></span>

<span data-ttu-id="e2f61-117">此事件方法是在 **\_ IInkCollectorEvents**、 **\_ IInkOverlayEvents** 和 **\_ IInkPictureEvents** 分派專用介面中定義， (具有 DISPID ICECursorInRange 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="e2f61-117">This event method is defined in the **\_IInkCollectorEvents**, **\_IInkOverlayEvents**, and **\_IInkPictureEvents** dispatch-only interface (dispinterfaces) with an ID of DISPID\_ICECursorInRange.</span></span>

<span data-ttu-id="e2f61-118">即使在 [選取] 或 [清除] 模式中，也不只是在 [筆墨] 模式中，也會引發 **CursorInRange** 事件。</span><span class="sxs-lookup"><span data-stu-id="e2f61-118">The **CursorInRange** event is fired even when in select or erase mode, not just when in ink mode.</span></span> <span data-ttu-id="e2f61-119">這需要您監視編輯模式 (您負責設定) 並在解讀事件之前留意模式。</span><span class="sxs-lookup"><span data-stu-id="e2f61-119">This requires that you monitor the editing mode (which you are responsible for setting) and be aware of the mode before interpreting the event.</span></span> <span data-ttu-id="e2f61-120">這項需求的優點是透過更清楚地瞭解平臺事件，更能自由地在平臺上進行創新。</span><span class="sxs-lookup"><span data-stu-id="e2f61-120">The advantage of this requirement is greater freedom to innovate on the platform through greater awareness of platform events.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2f61-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2f61-121">Requirements</span></span>



| <span data-ttu-id="e2f61-122">需求</span><span class="sxs-lookup"><span data-stu-id="e2f61-122">Requirement</span></span> | <span data-ttu-id="e2f61-123">值</span><span class="sxs-lookup"><span data-stu-id="e2f61-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2f61-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e2f61-124">Minimum supported client</span></span><br/> | <span data-ttu-id="e2f61-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e2f61-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="e2f61-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e2f61-126">Minimum supported server</span></span><br/> | <span data-ttu-id="e2f61-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="e2f61-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="e2f61-128">標頭</span><span class="sxs-lookup"><span data-stu-id="e2f61-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="e2f61-129"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="e2f61-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="e2f61-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2f61-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="e2f61-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e2f61-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="e2f61-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2f61-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2f61-133">InkPicture</span><span class="sxs-lookup"><span data-stu-id="e2f61-133">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

[<span data-ttu-id="e2f61-134">**CursorOutOfRange 事件**</span><span class="sxs-lookup"><span data-stu-id="e2f61-134">**CursorOutOfRange Event**</span></span>](inkpicture-cursoroutofrange.md)
</dt> <dt>

[<span data-ttu-id="e2f61-135">**InkCursorButtonState 列舉**</span><span class="sxs-lookup"><span data-stu-id="e2f61-135">**InkCursorButtonState Enumeration**</span></span>](/windows/desktop/api/msinkaut/ne-msinkaut-inkcursorbuttonstate)
</dt> <dt>

[<span data-ttu-id="e2f61-136">**IInkCursor 介面**</span><span class="sxs-lookup"><span data-stu-id="e2f61-136">**IInkCursor Interface**</span></span>](/windows/desktop/api/msinkaut/nn-msinkaut-iinkcursor)
</dt> </dl>

 

 




