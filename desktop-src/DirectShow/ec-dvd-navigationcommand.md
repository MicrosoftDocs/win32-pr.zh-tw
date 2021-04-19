---
description: 當 DVD 導覽器處理 DVD 流覽命令時傳送。
ms.assetid: 95e502b6-330f-4bc7-8adc-851913987370
title: 'EC_DVD_NavigationCommand (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_NavigationCommand
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: e81dbf108868cbaec4c44a436f2c8271bb5f282a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107000008"
---
# <a name="ec_dvd_navigationcommand"></a><span data-ttu-id="30a4a-103">EC \_ DVD \_ NavigationCommand</span><span class="sxs-lookup"><span data-stu-id="30a4a-103">EC\_DVD\_NavigationCommand</span></span>

<span data-ttu-id="30a4a-104">當 Dvd 導覽 [器](dvd-navigator-filter.md) 處理 dvd 流覽命令時傳送。</span><span class="sxs-lookup"><span data-stu-id="30a4a-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) processes a DVD navigation command.</span></span>

## <a name="parameters"></a><span data-ttu-id="30a4a-105">參數</span><span class="sxs-lookup"><span data-stu-id="30a4a-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30a4a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="30a4a-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="30a4a-107">原始流覽命令的較低32位。</span><span class="sxs-lookup"><span data-stu-id="30a4a-107">The lower 32 bits of the raw navigation command.</span></span>

</dd> <dt>

<span data-ttu-id="30a4a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="30a4a-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="30a4a-109">原始流覽命令的最高32位。</span><span class="sxs-lookup"><span data-stu-id="30a4a-109">The upper 32 bits of the raw navigation command.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30a4a-110">備註</span><span class="sxs-lookup"><span data-stu-id="30a4a-110">Remarks</span></span>

<span data-ttu-id="30a4a-111">此事件預設為停用。</span><span class="sxs-lookup"><span data-stu-id="30a4a-111">This event is disabled by default.</span></span> <span data-ttu-id="30a4a-112">若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ EnableLoggingEvents** 選項設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="30a4a-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="30a4a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="30a4a-113">Requirements</span></span>



| <span data-ttu-id="30a4a-114">需求</span><span class="sxs-lookup"><span data-stu-id="30a4a-114">Requirement</span></span> | <span data-ttu-id="30a4a-115">值</span><span class="sxs-lookup"><span data-stu-id="30a4a-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30a4a-116">標頭</span><span class="sxs-lookup"><span data-stu-id="30a4a-116">Header</span></span><br/> | <dl> <span data-ttu-id="30a4a-117"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="30a4a-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30a4a-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="30a4a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30a4a-119">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="30a4a-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="30a4a-120">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="30a4a-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="30a4a-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="30a4a-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




