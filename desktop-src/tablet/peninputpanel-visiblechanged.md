---
description: 已取代。 PenInputPanel 已由文字輸入面板取代 (提示) 。在 PenInputPanel 物件顯示或隱藏本身時發生。
ms.assetid: bf4651f4-2cf4-4952-a93e-3c6ba4846722
title: 'PenInputPanel. VisibleChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2c739f3517ad9739f1d1ba95af9e5001dfbe659a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979840"
---
# <a name="peninputpanelvisiblechanged-event"></a><span data-ttu-id="92b97-104">PenInputPanel. VisibleChanged 事件</span><span class="sxs-lookup"><span data-stu-id="92b97-104">PenInputPanel.VisibleChanged event</span></span>

<span data-ttu-id="92b97-105">已取代。</span><span class="sxs-lookup"><span data-stu-id="92b97-105">Deprecated.</span></span> <span data-ttu-id="92b97-106">[**PenInputPanel**](peninputpanel-class.md)已由 [文字輸入面板取代 (提示)](text-input-panel-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="92b97-106">The [**PenInputPanel**](peninputpanel-class.md) has been replaced by the [Text Input Panel (TIP)](text-input-panel-reference.md).</span></span>

<span data-ttu-id="92b97-107">在 [**PenInputPanel**](peninputpanel-class.md) 物件顯示或隱藏本身時發生。</span><span class="sxs-lookup"><span data-stu-id="92b97-107">Occurs when the [**PenInputPanel**](peninputpanel-class.md) object has shown or hidden itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b97-108">語法</span><span class="sxs-lookup"><span data-stu-id="92b97-108">Syntax</span></span>


```C++
HRESULT VisibleChanged(
  [in] VARIANT_BOOL NewVisibility
);
```



## <a name="parameters"></a><span data-ttu-id="92b97-109">參數</span><span class="sxs-lookup"><span data-stu-id="92b97-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b97-110">*NewVisibility* \[在\]</span><span class="sxs-lookup"><span data-stu-id="92b97-110">*NewVisibility* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b97-111">**變異 \_TRUE** 表示讓 [**PenInputPanel**](peninputpanel-class.md) 物件變成可見;否則， **VARIANT \_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="92b97-111">**VARIANT\_TRUE** to cause the [**PenInputPanel**](peninputpanel-class.md) object to become visible; otherwise, **VARIANT\_FALSE**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b97-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="92b97-112">Return value</span></span>

<span data-ttu-id="92b97-113">如果此事件成功，則會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="92b97-113">If this event succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="92b97-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="92b97-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="92b97-115">備註</span><span class="sxs-lookup"><span data-stu-id="92b97-115">Remarks</span></span>

<span data-ttu-id="92b97-116">**VisibleChanged** 事件會套用至 Tablet PC 輸入面板的滑鼠停留目標。</span><span class="sxs-lookup"><span data-stu-id="92b97-116">The **VisibleChanged** event applies to the Tablet PC Input Panel hover target.</span></span> <span data-ttu-id="92b97-117">不過，當滑鼠停留目標展開以顯示完整的 Tablet PC 輸入面板時，不會引發此功能。</span><span class="sxs-lookup"><span data-stu-id="92b97-117">However, it is not raised when the hover target expands to show the full Tablet PC Input Panel.</span></span>

## <a name="requirements"></a><span data-ttu-id="92b97-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="92b97-118">Requirements</span></span>



| <span data-ttu-id="92b97-119">需求</span><span class="sxs-lookup"><span data-stu-id="92b97-119">Requirement</span></span> | <span data-ttu-id="92b97-120">值</span><span class="sxs-lookup"><span data-stu-id="92b97-120">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b97-121">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="92b97-121">Minimum supported client</span></span><br/> | <span data-ttu-id="92b97-122">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="92b97-122">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="92b97-123">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="92b97-123">Minimum supported server</span></span><br/> | <span data-ttu-id="92b97-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="92b97-124">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="92b97-125">標頭</span><span class="sxs-lookup"><span data-stu-id="92b97-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="92b97-126"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="92b97-126"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="92b97-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="92b97-127">Library</span></span><br/>                  | <dl> <span data-ttu-id="92b97-128"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92b97-128"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="92b97-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92b97-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b97-130">**PenInputPanel**</span><span class="sxs-lookup"><span data-stu-id="92b97-130">**PenInputPanel**</span></span>](peninputpanel-class.md)
</dt> </dl>

 

 




