---
description: 發生于控制項內的筆墨選取變更時（例如，透過對使用者介面的變化、剪下和貼上程式或選取屬性）。
ms.assetid: 6b4cd9fe-b09f-4a70-9aa5-92ef9409ff1b
title: 'SelectionChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 997e0c8e9620b0a269ff8cd97ff04aa3abfb1df0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980666"
---
# <a name="inkoverlayselectionchanged-event"></a><span data-ttu-id="a5b0b-103">SelectionChanged 事件</span><span class="sxs-lookup"><span data-stu-id="a5b0b-103">InkOverlay.SelectionChanged event</span></span>

<span data-ttu-id="a5b0b-104">發生于控制項內的筆墨選取變更時（例如，透過對使用者介面的變化、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) 屬性）。</span><span class="sxs-lookup"><span data-stu-id="a5b0b-104">Occurs when the selection of ink within the control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a5b0b-105">語法</span><span class="sxs-lookup"><span data-stu-id="a5b0b-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="a5b0b-106">參數</span><span class="sxs-lookup"><span data-stu-id="a5b0b-106">Parameters</span></span>

<span data-ttu-id="a5b0b-107">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a5b0b-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a5b0b-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a5b0b-108">Return value</span></span>

<span data-ttu-id="a5b0b-109">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a5b0b-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a5b0b-110">備註</span><span class="sxs-lookup"><span data-stu-id="a5b0b-110">Remarks</span></span>

<span data-ttu-id="a5b0b-111">沒有任何事件資料。</span><span class="sxs-lookup"><span data-stu-id="a5b0b-111">There are no event data.</span></span>

<span data-ttu-id="a5b0b-112">此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOESelectionChanged 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="a5b0b-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanged.</span></span>

## <a name="requirements"></a><span data-ttu-id="a5b0b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a5b0b-113">Requirements</span></span>



| <span data-ttu-id="a5b0b-114">需求</span><span class="sxs-lookup"><span data-stu-id="a5b0b-114">Requirement</span></span> | <span data-ttu-id="a5b0b-115">值</span><span class="sxs-lookup"><span data-stu-id="a5b0b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a5b0b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a5b0b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a5b0b-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a5b0b-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a5b0b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a5b0b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a5b0b-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="a5b0b-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a5b0b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a5b0b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a5b0b-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="a5b0b-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a5b0b-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="a5b0b-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="a5b0b-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a5b0b-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a5b0b-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a5b0b-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a5b0b-125">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="a5b0b-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

[<span data-ttu-id="a5b0b-126">**Selection 屬性**</span><span class="sxs-lookup"><span data-stu-id="a5b0b-126">**Selection Property**</span></span>](/windows/desktop/api/msinkaut/nf-msinkaut-iinkoverlay-get_selection)
</dt> </dl>

 

 




