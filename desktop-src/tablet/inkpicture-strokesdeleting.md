---
description: 發生于從 Ink 屬性中刪除 IInkStrokeDisp 物件之前。
ms.assetid: 747e0fdf-c68b-4805-bdc8-aa05e95ec0f7
title: 'InkPicture. StrokesDeleting 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aef70e8526798f306f99c17b511b5c18c502858a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027206"
---
# <a name="inkpicturestrokesdeleting-event"></a><span data-ttu-id="200e3-103">InkPicture. StrokesDeleting 事件</span><span class="sxs-lookup"><span data-stu-id="200e3-103">InkPicture.StrokesDeleting event</span></span>

<span data-ttu-id="200e3-104">發生于從 [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)屬性中刪除 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件之前。</span><span class="sxs-lookup"><span data-stu-id="200e3-104">Occurs before [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="200e3-105">語法</span><span class="sxs-lookup"><span data-stu-id="200e3-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="200e3-106">參數</span><span class="sxs-lookup"><span data-stu-id="200e3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="200e3-107">*筆觸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="200e3-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="200e3-108">引發 **StrokesDeleting** 事件時，會刪除 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。</span><span class="sxs-lookup"><span data-stu-id="200e3-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="200e3-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="200e3-109">Return value</span></span>

<span data-ttu-id="200e3-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="200e3-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="200e3-111">備註</span><span class="sxs-lookup"><span data-stu-id="200e3-111">Remarks</span></span>

<span data-ttu-id="200e3-112">此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOEStrokesDeleting 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="200e3-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="200e3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="200e3-113">Requirements</span></span>



| <span data-ttu-id="200e3-114">需求</span><span class="sxs-lookup"><span data-stu-id="200e3-114">Requirement</span></span> | <span data-ttu-id="200e3-115">值</span><span class="sxs-lookup"><span data-stu-id="200e3-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="200e3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="200e3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="200e3-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="200e3-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="200e3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="200e3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="200e3-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="200e3-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="200e3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="200e3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="200e3-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="200e3-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="200e3-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="200e3-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="200e3-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="200e3-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="200e3-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="200e3-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="200e3-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="200e3-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

