---
description: 已取代。 PenInputPanel 已由文字輸入面板取代 (提示) 。在 PenInputPanel 物件移動時發生。
ms.assetid: 0c51d875-cef9-4087-b17d-5c5af04f81a5
title: 'PenInputPanel. PanelMoving 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7be69e227188739cb656e6a1eb471716e1aa4feb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980070"
---
# <a name="peninputpanelpanelmoving-event"></a><span data-ttu-id="f269d-104">PenInputPanel. PanelMoving 事件</span><span class="sxs-lookup"><span data-stu-id="f269d-104">PenInputPanel.PanelMoving event</span></span>

<span data-ttu-id="f269d-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="f269d-105">Deprecated.</span></span> <span data-ttu-id="f269d-106">[**PenInputPanel**](peninputpanel-class.md)已由 [文字輸入面板取代 (提示)](text-input-panel-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="f269d-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="f269d-107">在 [**PenInputPanel**](peninputpanel-class.md) 物件移動時發生。</span><span class="sxs-lookup"><span data-stu-id="f269d-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object is moving.</span></span>

## <a name="syntax"></a><span data-ttu-id="f269d-108">語法</span><span class="sxs-lookup"><span data-stu-id="f269d-108">Syntax</span></span>


```C++
HRESULT PanelMoving(
  [in, out] long *Left,
  [in, out] long *Top
);
```



## <a name="parameters"></a><span data-ttu-id="f269d-109">參數</span><span class="sxs-lookup"><span data-stu-id="f269d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f269d-110">*左方* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f269d-110">*Left* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f269d-111">[**PenInputPanel**](peninputpanel-class.md)物件左邊緣的新水準或 X 軸位置（以螢幕座標表示）。</span><span class="sxs-lookup"><span data-stu-id="f269d-111">The new horizontal, or x-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="f269d-112">*頂端* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f269d-112">*Top* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f269d-113">[**PenInputPanel**](peninputpanel-class.md)物件左邊緣的新垂直軸（或 y 軸）位置（以螢幕座標為單位）。</span><span class="sxs-lookup"><span data-stu-id="f269d-113">The new vertical, or y-axis, position of the left edge of the [**PenInputPanel**](peninputpanel-class.md) object, in screen coordinates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f269d-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="f269d-114">Return value</span></span>

<span data-ttu-id="f269d-115">如果此事件成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f269d-115">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f269d-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f269d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="f269d-117">備註</span><span class="sxs-lookup"><span data-stu-id="f269d-117">Remarks</span></span>

<span data-ttu-id="f269d-118">**PanelMoving** 事件是設計用來變更 [畫筆輸入] 面板的位置，方法是變更 *左方* 和 *前幾* 個參數。</span><span class="sxs-lookup"><span data-stu-id="f269d-118">The **PanelMoving** event is designed to be used to change the position of the pen input panel by changing the *Left* and *Top* parameters.</span></span>

<span data-ttu-id="f269d-119">[**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto)和 [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh)方法會導致 [**PenInputPanel**](peninputpanel-class.md)物件呼叫其自動定位程式碼，以觸發 **PanelMoving** 事件。</span><span class="sxs-lookup"><span data-stu-id="f269d-119">The [**MoveTo**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-moveto) and [**Refresh**](/windows/desktop/api/peninputpanel/nf-peninputpanel-ipeninputpanel-refresh) methods cause the [**PenInputPanel**](peninputpanel-class.md) object to call its auto-positioning code which triggers a **PanelMoving** event.</span></span> <span data-ttu-id="f269d-120">因此，在 **PanelMoving** 處理常式中呼叫這些方法，可能會導致遞迴的無限迴圈。</span><span class="sxs-lookup"><span data-stu-id="f269d-120">Consequently, calling these methods inside a **PanelMoving** handler can result in a recursive endless loop.</span></span>

## <a name="requirements"></a><span data-ttu-id="f269d-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="f269d-121">Requirements</span></span>



| <span data-ttu-id="f269d-122">需求</span><span class="sxs-lookup"><span data-stu-id="f269d-122">Requirement</span></span> | <span data-ttu-id="f269d-123">值</span><span class="sxs-lookup"><span data-stu-id="f269d-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f269d-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f269d-124">Minimum supported client</span></span><br/> | <span data-ttu-id="f269d-125">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f269d-125">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="f269d-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f269d-126">Minimum supported server</span></span><br/> | <span data-ttu-id="f269d-127">都不支援</span><span class="sxs-lookup"><span data-stu-id="f269d-127">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="f269d-128">標頭</span><span class="sxs-lookup"><span data-stu-id="f269d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="f269d-129"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="f269d-129"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="f269d-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="f269d-130">Library</span></span><br/>                  | <dl> <span data-ttu-id="f269d-131"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f269d-131"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="f269d-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f269d-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f269d-133">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="f269d-133">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




