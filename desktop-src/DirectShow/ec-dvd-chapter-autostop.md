---
description: 指出由於呼叫 IDvdControl2：:P layChaptersAutoStop 方法而停止播放 DVD。
ms.assetid: ccafaf76-ec8c-4d67-9b29-565f3ed6593b
title: 'EC_DVD_CHAPTER_AUTOSTOP (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CHAPTER_AUTOSTOP
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 43e1414c0f9cee7e8daf37b87d5f0c3d0599a017
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995998"
---
# <a name="ec_dvd_chapter_autostop"></a><span data-ttu-id="0f041-103">EC \_ DVD \_ 章節 \_ AUTOSTOP</span><span class="sxs-lookup"><span data-stu-id="0f041-103">EC\_DVD\_CHAPTER\_AUTOSTOP</span></span>

<span data-ttu-id="0f041-104">指出由於呼叫 [**IDvdControl2：:P laychaptersautostop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) 方法而停止播放 DVD。</span><span class="sxs-lookup"><span data-stu-id="0f041-104">Indicates that DVD playback stopped as the result of a call to the [**IDvdControl2::PlayChaptersAutoStop**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-playchaptersautostop) method.</span></span>

## <a name="parameters"></a><span data-ttu-id="0f041-105">參數</span><span class="sxs-lookup"><span data-stu-id="0f041-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f041-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0f041-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0f041-107">零個。</span><span class="sxs-lookup"><span data-stu-id="0f041-107">Zero.</span></span>

</dd> <dt>

<span data-ttu-id="0f041-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0f041-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0f041-109">零個。</span><span class="sxs-lookup"><span data-stu-id="0f041-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0f041-110">備註</span><span class="sxs-lookup"><span data-stu-id="0f041-110">Remarks</span></span>

<span data-ttu-id="0f041-111">此事件會在標題網域中引發。</span><span class="sxs-lookup"><span data-stu-id="0f041-111">This event is raised in the title domain.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f041-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f041-112">Requirements</span></span>



| <span data-ttu-id="0f041-113">需求</span><span class="sxs-lookup"><span data-stu-id="0f041-113">Requirement</span></span> | <span data-ttu-id="0f041-114">值</span><span class="sxs-lookup"><span data-stu-id="0f041-114">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f041-115">標頭</span><span class="sxs-lookup"><span data-stu-id="0f041-115">Header</span></span><br/> | <dl> <span data-ttu-id="0f041-116"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="0f041-116"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f041-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f041-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f041-118">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="0f041-118">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="0f041-119">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="0f041-119">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0f041-120">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="0f041-120">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




