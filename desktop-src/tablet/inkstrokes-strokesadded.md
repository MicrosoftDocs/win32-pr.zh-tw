---
description: 當一或多個筆劃加入至 InkStrokes 集合時發生。
ms.assetid: d32dcaef-3beb-4ee1-84d6-5944278936f6
title: 'InkStrokes. StrokesAdded 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a53bf1f511b5809cfb9a6ca0a2f683f0e85540af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983743"
---
# <a name="inkstrokesstrokesadded-event"></a><span data-ttu-id="19883-103">InkStrokes. StrokesAdded 事件</span><span class="sxs-lookup"><span data-stu-id="19883-103">InkStrokes.StrokesAdded event</span></span>

<span data-ttu-id="19883-104">當一或多個筆劃加入至 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合時發生。</span><span class="sxs-lookup"><span data-stu-id="19883-104">Occurs when one or more strokes are added to the [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="19883-105">語法</span><span class="sxs-lookup"><span data-stu-id="19883-105">Syntax</span></span>


```C++
void StrokesAdded(
  [in] VARIANT StrokeIds
);
```



## <a name="parameters"></a><span data-ttu-id="19883-106">參數</span><span class="sxs-lookup"><span data-stu-id="19883-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="19883-107">*StrokeIds* \[在\]</span><span class="sxs-lookup"><span data-stu-id="19883-107">*StrokeIds* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="19883-108">當此事件發生時，所加入之每個 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) 物件的識別碼的整數陣列。</span><span class="sxs-lookup"><span data-stu-id="19883-108">The integer array of identifiers for every [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) object added when this event occurs.</span></span>

<span data-ttu-id="19883-109">如需 VARIANT 結構的詳細資訊，請參閱 [使用 COM 程式庫](using-the-com-library.md)。</span><span class="sxs-lookup"><span data-stu-id="19883-109">For more information about the VARIANT structure, see [Using the COM Library](using-the-com-library.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="19883-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="19883-110">Return value</span></span>

<span data-ttu-id="19883-111">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="19883-111">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="19883-112">備註</span><span class="sxs-lookup"><span data-stu-id="19883-112">Remarks</span></span>

<span data-ttu-id="19883-113">此事件方法是在 \_ IInkEvents 介面中定義。</span><span class="sxs-lookup"><span data-stu-id="19883-113">This event method is defined in the \_IInkEvents interface.</span></span> <span data-ttu-id="19883-114">\_IInkEvents 介面會以 DISPID SEStrokesAdded 的識別碼來實作為 [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch)介面 \_ 。</span><span class="sxs-lookup"><span data-stu-id="19883-114">The \_IInkEvents interface implements the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface with an identifier of DISPID\_SEStrokesAdded.</span></span>

## <a name="requirements"></a><span data-ttu-id="19883-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="19883-115">Requirements</span></span>



| <span data-ttu-id="19883-116">需求</span><span class="sxs-lookup"><span data-stu-id="19883-116">Requirement</span></span> | <span data-ttu-id="19883-117">值</span><span class="sxs-lookup"><span data-stu-id="19883-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="19883-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="19883-118">Minimum supported client</span></span><br/> | <span data-ttu-id="19883-119">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="19883-119">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="19883-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="19883-120">Minimum supported server</span></span><br/> | <span data-ttu-id="19883-121">都不支援</span><span class="sxs-lookup"><span data-stu-id="19883-121">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="19883-122">標頭</span><span class="sxs-lookup"><span data-stu-id="19883-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="19883-123"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="19883-123"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="19883-124">程式庫</span><span class="sxs-lookup"><span data-stu-id="19883-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="19883-125"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="19883-125"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="19883-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="19883-126">See also</span></span>

<dl> <dt>

<span data-ttu-id="19883-127">[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="19883-127">[InkStrokes Collection](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))</span></span>
</dt> <dt>

<span data-ttu-id="19883-128">[**新增方法 \[ InkStrokes 集合\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)</span><span class="sxs-lookup"><span data-stu-id="19883-128">[**Add Method \[InkStrokes Collection\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkstrokes-add)</span></span>
</dt> <dt>

[<span data-ttu-id="19883-129">**InkDisp 類別**</span><span class="sxs-lookup"><span data-stu-id="19883-129">**InkDisp Class**</span></span>](inkdisp-class.md)
</dt> </dl>

 

