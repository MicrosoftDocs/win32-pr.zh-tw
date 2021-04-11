---
description: 發生于從筆墨屬性刪除筆劃之前。
ms.assetid: 09468416-ad08-48ea-aa4a-3af0fe553f3d
title: 'StrokesDeleting 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64422e61869c633514c3e219e3d090476a693dd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944997"
---
# <a name="inkoverlaystrokesdeleting-event"></a><span data-ttu-id="6c5b1-103">StrokesDeleting 事件</span><span class="sxs-lookup"><span data-stu-id="6c5b1-103">InkOverlay.StrokesDeleting event</span></span>

<span data-ttu-id="6c5b1-104">發生于從 [**筆墨**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) 屬性刪除筆劃之前。</span><span class="sxs-lookup"><span data-stu-id="6c5b1-104">Occurs before strokes are deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6c5b1-105">語法</span><span class="sxs-lookup"><span data-stu-id="6c5b1-105">Syntax</span></span>


```C++
void StrokesDeleting(
  [in] IInkStrokes *Strokes
);
```



## <a name="parameters"></a><span data-ttu-id="6c5b1-106">參數</span><span class="sxs-lookup"><span data-stu-id="6c5b1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c5b1-107">*筆觸* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c5b1-107">*Strokes* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c5b1-108">引發 **StrokesDeleting** 事件時，會刪除 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。</span><span class="sxs-lookup"><span data-stu-id="6c5b1-108">The [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85)) collection deleted when the **StrokesDeleting** event fires.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c5b1-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c5b1-109">Return value</span></span>

<span data-ttu-id="6c5b1-110">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6c5b1-110">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c5b1-111">備註</span><span class="sxs-lookup"><span data-stu-id="6c5b1-111">Remarks</span></span>

<span data-ttu-id="6c5b1-112">此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOEStrokesDeleting 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="6c5b1-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleting.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c5b1-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c5b1-113">Requirements</span></span>



| <span data-ttu-id="6c5b1-114">需求</span><span class="sxs-lookup"><span data-stu-id="6c5b1-114">Requirement</span></span> | <span data-ttu-id="6c5b1-115">值</span><span class="sxs-lookup"><span data-stu-id="6c5b1-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5b1-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c5b1-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6c5b1-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c5b1-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6c5b1-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c5b1-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6c5b1-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="6c5b1-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6c5b1-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6c5b1-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c5b1-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="6c5b1-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6c5b1-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="6c5b1-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="6c5b1-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6c5b1-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6c5b1-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6c5b1-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5b1-125">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="6c5b1-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="6c5b1-126">[**Ink 屬性 \[ InkCollector/InkOverLay 類別\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="6c5b1-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

