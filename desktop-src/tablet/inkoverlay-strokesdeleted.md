---
description: 從筆墨屬性刪除筆劃之後發生。
ms.assetid: 60ee8bbd-9230-4b6a-a4b0-4783195e3173
title: 'StrokesDeleted 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc37b0de7f86f7d2b68df7074a0f3bb6c9e075e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193156"
---
# <a name="inkoverlaystrokesdeleted-event"></a><span data-ttu-id="6098a-103">StrokesDeleted 事件</span><span class="sxs-lookup"><span data-stu-id="6098a-103">InkOverlay.StrokesDeleted event</span></span>

<span data-ttu-id="6098a-104">從 [**筆墨**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) 屬性刪除筆劃之後發生。</span><span class="sxs-lookup"><span data-stu-id="6098a-104">Occurs after strokes have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="6098a-105">語法</span><span class="sxs-lookup"><span data-stu-id="6098a-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="6098a-106">參數</span><span class="sxs-lookup"><span data-stu-id="6098a-106">Parameters</span></span>

<span data-ttu-id="6098a-107">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="6098a-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6098a-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="6098a-108">Return value</span></span>

<span data-ttu-id="6098a-109">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="6098a-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6098a-110">備註</span><span class="sxs-lookup"><span data-stu-id="6098a-110">Remarks</span></span>

<span data-ttu-id="6098a-111">沒有任何事件資料。</span><span class="sxs-lookup"><span data-stu-id="6098a-111">There is no event data.</span></span>

<span data-ttu-id="6098a-112">此事件方法是在 \_ IInkOverlayEvents 和 \_ 僅 IInkPictureEvents 分派介面中定義， (具有 DISPID IOEStrokesDeleted 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="6098a-112">This event method is defined in the \_IInkOverlayEvents and \_IInkPictureEvents dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="6098a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="6098a-113">Requirements</span></span>



| <span data-ttu-id="6098a-114">需求</span><span class="sxs-lookup"><span data-stu-id="6098a-114">Requirement</span></span> | <span data-ttu-id="6098a-115">值</span><span class="sxs-lookup"><span data-stu-id="6098a-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6098a-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6098a-116">Minimum supported client</span></span><br/> | <span data-ttu-id="6098a-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6098a-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="6098a-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6098a-118">Minimum supported server</span></span><br/> | <span data-ttu-id="6098a-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="6098a-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="6098a-120">標頭</span><span class="sxs-lookup"><span data-stu-id="6098a-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="6098a-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="6098a-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="6098a-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="6098a-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="6098a-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6098a-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="6098a-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6098a-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6098a-125">**InkOverlay 類別**</span><span class="sxs-lookup"><span data-stu-id="6098a-125">**InkOverlay Class**</span></span>](inkoverlay-class.md)
</dt> <dt>

<span data-ttu-id="6098a-126">[**Ink 屬性 \[ InkCollector/InkOverLay 類別\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span><span class="sxs-lookup"><span data-stu-id="6098a-126">[**Ink Property \[InkCollector/InkOverLay Class\]**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkcollector-get_ink)</span></span>
</dt> </dl>

 

 




