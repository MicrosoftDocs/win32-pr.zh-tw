---
description: 發生于 InkPicture 控制項內的筆墨選取即將變更時（例如，透過變更使用者介面、剪下和貼上程式或選取屬性）。
ms.assetid: a8ae30ff-fb0d-44cc-a5d3-295117addafd
title: 'InkPicture. SelectionChanging 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37b8a35d57aeb9367bb9d30647cb074a7e0e6fbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852172"
---
# <a name="inkpictureselectionchanging-event"></a><span data-ttu-id="6e4a2-103">InkPicture. SelectionChanging 事件</span><span class="sxs-lookup"><span data-stu-id="6e4a2-103">InkPicture.SelectionChanging event</span></span>

<span data-ttu-id="6e4a2-104">發生于 [InkPicture](inkpicture-control-reference.md) 控制項內的筆墨選取即將變更時（例如，透過變更使用者介面、剪下和貼上程式或 [**選取**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) 屬性）。</span><span class="sxs-lookup"><span data-stu-id="6e4a2-104">Occurs when the selection of ink within the [InkPicture](inkpicture-control-reference.md) control is about to change, such as through alterations to the user interface, cut-and-paste procedures, or the [**Selection**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e4a2-105">語法</span><span class="sxs-lookup"><span data-stu-id="6e4a2-105">Syntax</span></span>


```C++
void SelectionChanging(
  [in] IInkStrokes *NewSelection
);
```



## <a name="parameters"></a><span data-ttu-id="6e4a2-106">參數</span><span class="sxs-lookup"><span data-stu-id="6e4a2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e4a2-107">*NewSelection* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e4a2-107">*NewSelection* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e4a2-108">要選取的新 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) 集合。</span><span class="sxs-lookup"><span data-stu-id="6e4a2-108">The new collection of [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) that is being selected.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e4a2-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e4a2-109">Return value</span></span>

<span data-ttu-id="6e4a2-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6e4a2-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e4a2-111">備註</span><span class="sxs-lookup"><span data-stu-id="6e4a2-111">Remarks</span></span>

<span data-ttu-id="6e4a2-112">此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOESelectionChanging 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="6e4a2-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOESelectionChanging.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e4a2-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e4a2-113">Requirements</span></span>



| <span data-ttu-id="6e4a2-114">需求</span><span class="sxs-lookup"><span data-stu-id="6e4a2-114">Requirement</span></span> | <span data-ttu-id="6e4a2-115">值</span><span class="sxs-lookup"><span data-stu-id="6e4a2-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6e4a2-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e4a2-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6e4a2-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e4a2-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6e4a2-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e4a2-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6e4a2-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="6e4a2-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6e4a2-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6e4a2-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6e4a2-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="6e4a2-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6e4a2-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="6e4a2-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="6e4a2-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e4a2-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6e4a2-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e4a2-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e4a2-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="6e4a2-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> <dt>

<span data-ttu-id="6e4a2-126">[**選取專案屬性 \[ InkPicture 控制項\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span><span class="sxs-lookup"><span data-stu-id="6e4a2-126">[**Selection Property \[InkPicture Control\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_selection)</span></span>
</dt> </dl>

 

