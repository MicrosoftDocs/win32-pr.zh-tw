---
description: 從筆墨屬性刪除 IInkStrokeDisp 物件之後發生。
ms.assetid: 395544e1-dc93-45d3-ac7a-d54712f3c027
title: 'InkPicture. StrokesDeleted 事件 (Msinkaut .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bf98e51196d760f467d507c133429201883b340e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975905"
---
# <a name="inkpicturestrokesdeleted-event"></a><span data-ttu-id="a4e98-103">InkPicture. StrokesDeleted 事件</span><span class="sxs-lookup"><span data-stu-id="a4e98-103">InkPicture.StrokesDeleted event</span></span>

<span data-ttu-id="a4e98-104">從 [**筆墨**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink)屬性刪除 [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp)物件之後發生。</span><span class="sxs-lookup"><span data-stu-id="a4e98-104">Occurs after [**IInkStrokeDisp**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkstrokedisp) objects have been deleted from the [**Ink**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkpicture-get_ink) property.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4e98-105">語法</span><span class="sxs-lookup"><span data-stu-id="a4e98-105">Syntax</span></span>


```C++
void StrokesDeleted();
```



## <a name="parameters"></a><span data-ttu-id="a4e98-106">參數</span><span class="sxs-lookup"><span data-stu-id="a4e98-106">Parameters</span></span>

<span data-ttu-id="a4e98-107">此事件沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="a4e98-107">This event has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="a4e98-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="a4e98-108">Return value</span></span>

<span data-ttu-id="a4e98-109">此事件不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="a4e98-109">This event does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a4e98-110">備註</span><span class="sxs-lookup"><span data-stu-id="a4e98-110">Remarks</span></span>

<span data-ttu-id="a4e98-111">沒有任何事件資料。</span><span class="sxs-lookup"><span data-stu-id="a4e98-111">There is no event data.</span></span>

<span data-ttu-id="a4e98-112">此事件方法是在 **\_ IInkOverlayEvents** 和僅 **\_ IInkPictureEvents** 分派介面中定義， (具有 DISPID IOEStrokesDeleted 識別碼的) \_ 。</span><span class="sxs-lookup"><span data-stu-id="a4e98-112">This event method is defined in the **\_IInkOverlayEvents** and **\_IInkPictureEvents** dispatch-only interfaces (dispinterfaces) with an ID of DISPID\_IOEStrokesDeleted.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4e98-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="a4e98-113">Requirements</span></span>



| <span data-ttu-id="a4e98-114">需求</span><span class="sxs-lookup"><span data-stu-id="a4e98-114">Requirement</span></span> | <span data-ttu-id="a4e98-115">值</span><span class="sxs-lookup"><span data-stu-id="a4e98-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4e98-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a4e98-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a4e98-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a4e98-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a4e98-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a4e98-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a4e98-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="a4e98-119">None supported</span></span><br/>                                                                                           |
| <span data-ttu-id="a4e98-120">標頭</span><span class="sxs-lookup"><span data-stu-id="a4e98-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4e98-121"><dt>Msinkaut (也需要 Msinkaut \_ c) </dt></span><span class="sxs-lookup"><span data-stu-id="a4e98-121"><dt>Msinkaut.h (also requires Msinkaut\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="a4e98-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="a4e98-122">Library</span></span><br/>                  | <dl> <span data-ttu-id="a4e98-123"><dt>InkObj.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a4e98-123"><dt>InkObj.dll</dt></span></span> </dl>                               |



## <a name="see-also"></a><span data-ttu-id="a4e98-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4e98-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4e98-125">InkPicture</span><span class="sxs-lookup"><span data-stu-id="a4e98-125">InkPicture</span></span>](inkpicture-control-reference.md)
</dt> </dl>

 

 




