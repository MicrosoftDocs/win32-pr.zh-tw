---
description: 在一組 DVD 流覽命令開始時傳送。
ms.assetid: 9cdcb211-a9e3-4a15-81bd-7ada2b9d823a
title: 'EC_DVD_BeginNavigationCommands (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_BeginNavigationCommands
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: cda904c4fcc0b1acdd16c8fc4596eef332140ec4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106996429"
---
# <a name="ec_dvd_beginnavigationcommands"></a><span data-ttu-id="7d147-103">EC \_ DVD \_ BeginNavigationCommands</span><span class="sxs-lookup"><span data-stu-id="7d147-103">EC\_DVD\_BeginNavigationCommands</span></span>

<span data-ttu-id="7d147-104">在一組 DVD 流覽命令開始時傳送。</span><span class="sxs-lookup"><span data-stu-id="7d147-104">Sent when a set of DVD navigation commands are starting.</span></span>

## <a name="parameters"></a><span data-ttu-id="7d147-105">參數</span><span class="sxs-lookup"><span data-stu-id="7d147-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7d147-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="7d147-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="7d147-107">來自 [**DVD \_ NavCmdType**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) 列舉的值。</span><span class="sxs-lookup"><span data-stu-id="7d147-107">A value from the [**DVD\_NavCmdType**](/windows/win32/api/strmif/ne-strmif-dvd_navcmdtype) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="7d147-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="7d147-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="7d147-109">零個。</span><span class="sxs-lookup"><span data-stu-id="7d147-109">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7d147-110">備註</span><span class="sxs-lookup"><span data-stu-id="7d147-110">Remarks</span></span>

<span data-ttu-id="7d147-111">此事件預設為停用。</span><span class="sxs-lookup"><span data-stu-id="7d147-111">This event is disabled by default.</span></span> <span data-ttu-id="7d147-112">若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ EnableLoggingEvents** 選項設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="7d147-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="7d147-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="7d147-113">Requirements</span></span>



| <span data-ttu-id="7d147-114">需求</span><span class="sxs-lookup"><span data-stu-id="7d147-114">Requirement</span></span> | <span data-ttu-id="7d147-115">值</span><span class="sxs-lookup"><span data-stu-id="7d147-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7d147-116">標頭</span><span class="sxs-lookup"><span data-stu-id="7d147-116">Header</span></span><br/> | <dl> <span data-ttu-id="7d147-117"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="7d147-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7d147-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7d147-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7d147-119">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="7d147-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="7d147-120">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="7d147-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="7d147-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="7d147-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




