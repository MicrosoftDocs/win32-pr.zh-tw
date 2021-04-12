---
description: 從 InkStrokes 集合中刪除一或多個筆劃時發生。
ms.assetid: 58d78143-c733-45dc-ae5f-fe13136010db
title: 'InkStrokes. StrokesRemoved 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86448f9676e07a11effe683ecd883874791ff3b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320932"
---
# <a name="inkstrokesstrokesremoved-event"></a><span data-ttu-id="21e56-103">InkStrokes. StrokesRemoved 事件</span><span class="sxs-lookup"><span data-stu-id="21e56-103">InkStrokes.StrokesRemoved event</span></span>

<span data-ttu-id="21e56-104">從 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合中刪除一或多個筆劃時發生。</span><span class="sxs-lookup"><span data-stu-id="21e56-104">Occurs when one or more strokes are deleted from the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="21e56-105">語法</span><span class="sxs-lookup"><span data-stu-id="21e56-105">Syntax</span></span>


```C++
void StrokesRemoved(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="21e56-106">參數</span><span class="sxs-lookup"><span data-stu-id="21e56-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21e56-107">*StrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="21e56-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="21e56-108">當此事件發生時，每個 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件所刪除之識別碼的整數陣列。</span><span class="sxs-lookup"><span data-stu-id="21e56-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object deleted when this event occurs.</span></span>

<span data-ttu-id="21e56-109">如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="21e56-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21e56-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="21e56-110">Return value</span></span>

<span data-ttu-id="21e56-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="21e56-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21e56-112">備註</span><span class="sxs-lookup"><span data-stu-id="21e56-112">Remarks</span></span>

<span data-ttu-id="21e56-113">此事件方法是在 \_ IInkEvents 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="21e56-113">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="21e56-114">\_IInkEvents 介面會以 DISPID SEStrokesRemoved 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="21e56-114">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesRemoved.</span></span>

## <a name="requirements"></a><span data-ttu-id="21e56-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="21e56-115">Requirements</span></span>



| <span data-ttu-id="21e56-116">需求</span><span class="sxs-lookup"><span data-stu-id="21e56-116">Requirement</span></span> | <span data-ttu-id="21e56-117">值</span><span class="sxs-lookup"><span data-stu-id="21e56-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21e56-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21e56-118">Minimum supported client</span></span><br/> | <span data-ttu-id="21e56-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="21e56-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="21e56-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21e56-120">Minimum supported server</span></span><br/> | <span data-ttu-id="21e56-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="21e56-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="21e56-122">標頭</span><span class="sxs-lookup"><span data-stu-id="21e56-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="21e56-123"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="21e56-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="21e56-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="21e56-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="21e56-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21e56-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="21e56-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21e56-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="21e56-127">[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="21e56-127">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="21e56-128">[**Remove Method \[ InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span><span class="sxs-lookup"><span data-stu-id="21e56-128">[**Remove Method \[InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-remove)</span></span>
</dt> <dt>

[<span data-ttu-id="21e56-129">**InkDisp 類別**</span><span class="sxs-lookup"><span data-stu-id="21e56-129">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> </dl>

 

