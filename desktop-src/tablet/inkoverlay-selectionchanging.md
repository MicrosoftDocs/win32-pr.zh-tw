---
description: 發生于控制項內的筆墨選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式，或選取屬性）。
ms.assetid: dffdb183-d363-40d3-81a2-d496433f7075
title: 'SelectionChanging 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e830a9ea97f6722dd8ab9bdb782e4ae4ac5f44fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975442"
---
# <a name="inkoverlayselectionchanging-event"></a><span data-ttu-id="ab80c-103">SelectionChanging 事件</span><span class="sxs-lookup"><span data-stu-id="ab80c-103">InkOverlay.SelectionChanging event</span></span>

<span data-ttu-id="ab80c-104">發生于控制項內的筆墨選取範圍即將變更時（例如，透過變更使用者介面、剪下和貼上程式，或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性）。</span><span class="sxs-lookup"><span data-stu-id="ab80c-104">Occurs when the selection of ink within the control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab80c-105">語法</span><span class="sxs-lookup"><span data-stu-id="ab80c-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="ab80c-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab80c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab80c-107">*NewSelection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab80c-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab80c-108">要選取的新 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。</span><span class="sxs-lookup"><span data-stu-id="ab80c-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab80c-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab80c-109">Return value</span></span>

<span data-ttu-id="ab80c-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ab80c-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab80c-111">備註</span><span class="sxs-lookup"><span data-stu-id="ab80c-111">Remarks</span></span>

<span data-ttu-id="ab80c-112">此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOESelectionChanging 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="ab80c-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab80c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab80c-113">Requirements</span></span>



| <span data-ttu-id="ab80c-114">需求</span><span class="sxs-lookup"><span data-stu-id="ab80c-114">Requirement</span></span> | <span data-ttu-id="ab80c-115">值</span><span class="sxs-lookup"><span data-stu-id="ab80c-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab80c-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab80c-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ab80c-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab80c-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="ab80c-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab80c-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ab80c-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="ab80c-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="ab80c-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ab80c-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab80c-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="ab80c-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="ab80c-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="ab80c-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab80c-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab80c-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="ab80c-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab80c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab80c-125">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="ab80c-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="ab80c-126">**Selection 屬性**</span><span class="sxs-lookup"><span data-stu-id="ab80c-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

