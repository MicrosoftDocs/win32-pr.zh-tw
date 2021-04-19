---
description: InkPicture 控制項內的筆墨選取範圍變更時發生，例如透過變更使用者介面、剪下和貼上程式，或選取專案屬性。
ms.assetid: e300ec91-e8f3-473f-b526-efeafafaa32a
title: 'InkPicture. SelectionChanged 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14594efe4e5ecda64167ec9a0e075fc60d8e9a19
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975907"
---
# <a name="inkpictureselectionchanged-event"></a><span data-ttu-id="8e711-103">InkPicture. SelectionChanged 事件</span><span class="sxs-lookup"><span data-stu-id="8e711-103">InkPicture.SelectionChanged event</span></span>

<span data-ttu-id="8e711-104">[InkPicture](inkpicture-control-reference.md)控制項內的筆墨選取範圍變更時發生，例如透過變更使用者介面、剪下和貼上程式，或 [**選取專案**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)屬性。</span><span class="sxs-lookup"><span data-stu-id="8e711-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control has changed, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="8e711-105">語法</span><span class="sxs-lookup"><span data-stu-id="8e711-105">Syntax</span></span>


```C++
void SelectionChanged();
```



## <a name="parameters"></a><span data-ttu-id="8e711-106">參數</span><span class="sxs-lookup"><span data-stu-id="8e711-106">Parameters</span></span>

<span data-ttu-id="8e711-107">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="8e711-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8e711-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="8e711-108">Return value</span></span>

<span data-ttu-id="8e711-109">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="8e711-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8e711-110">備註</span><span class="sxs-lookup"><span data-stu-id="8e711-110">Remarks</span></span>

<span data-ttu-id="8e711-111">如需此事件的進一步詳細資料，請參閱 [**InkOverlay**](inkoverlay-class.md) 物件的 [**SelectionChanged**](inkoverlay-selectionchanged.md) 事件，該事件具有相同的功能。</span><span class="sxs-lookup"><span data-stu-id="8e711-111">For further details about this event, refer to the [**InkOverlay**](inkoverlay-class.md) object's [**SelectionChanged**](inkoverlay-selectionchanged.md) event, which has the same functionality.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e711-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="8e711-112">Requirements</span></span>



| <span data-ttu-id="8e711-113">需求</span><span class="sxs-lookup"><span data-stu-id="8e711-113">Requirement</span></span> | <span data-ttu-id="8e711-114">值</span><span class="sxs-lookup"><span data-stu-id="8e711-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8e711-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8e711-115">Minimum supported client</span></span><br/> | <span data-ttu-id="8e711-116">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8e711-116">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="8e711-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8e711-117">Minimum supported server</span></span><br/> | <span data-ttu-id="8e711-118">都不支援</span><span class="sxs-lookup"><span data-stu-id="8e711-118">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="8e711-119">標頭</span><span class="sxs-lookup"><span data-stu-id="8e711-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e711-120"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="8e711-120"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="8e711-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="8e711-121">Library</span></span><br/>                  | <dl> <span data-ttu-id="8e711-122"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8e711-122"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="8e711-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8e711-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e711-124">InkPicture</span><span class="sxs-lookup"><span data-stu-id="8e711-124">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="8e711-125">[**選取專案屬性 \[ InkPicture 控制項\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="8e711-125">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

 




