---
description: 當 DVD 導覽器剖析 PCI 封包時傳送。
ms.assetid: e2e65007-7c34-4be4-86b9-9491061891e5
title: 'EC_DVD_VOBU_Offset (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Offset
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 531207d4d8b0debb29dd5d02e01e400218e4a2bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977445"
---
# <a name="ec_dvd_vobu_offset"></a><span data-ttu-id="8fe16-103">EC \_ DVD \_ VOBU \_ 位移</span><span class="sxs-lookup"><span data-stu-id="8fe16-103">EC\_DVD\_VOBU\_Offset</span></span>

<span data-ttu-id="8fe16-104">當 DVD 導覽 [器](dvd-navigator-filter.md) 剖析 PCI 封包時傳送。</span><span class="sxs-lookup"><span data-stu-id="8fe16-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

## <a name="parameters"></a><span data-ttu-id="8fe16-105">參數</span><span class="sxs-lookup"><span data-stu-id="8fe16-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8fe16-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="8fe16-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="8fe16-107">最新影片物件單位的區塊位移 (VOBU) 。</span><span class="sxs-lookup"><span data-stu-id="8fe16-107">The block offset of the most recent video object unit (VOBU).</span></span>

</dd> <dt>

<span data-ttu-id="8fe16-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="8fe16-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="8fe16-109">目前的影片標題集號碼 (VTSN) 。</span><span class="sxs-lookup"><span data-stu-id="8fe16-109">The current video title set number (VTSN).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8fe16-110">備註</span><span class="sxs-lookup"><span data-stu-id="8fe16-110">Remarks</span></span>

<span data-ttu-id="8fe16-111">此事件預設為停用。</span><span class="sxs-lookup"><span data-stu-id="8fe16-111">This event is disabled by default.</span></span> <span data-ttu-id="8fe16-112">若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ EnableLoggingEvents** 選項設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="8fe16-112">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="8fe16-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="8fe16-113">Requirements</span></span>



| <span data-ttu-id="8fe16-114">需求</span><span class="sxs-lookup"><span data-stu-id="8fe16-114">Requirement</span></span> | <span data-ttu-id="8fe16-115">值</span><span class="sxs-lookup"><span data-stu-id="8fe16-115">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8fe16-116">標頭</span><span class="sxs-lookup"><span data-stu-id="8fe16-116">Header</span></span><br/> | <dl> <span data-ttu-id="8fe16-117"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="8fe16-117"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8fe16-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8fe16-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8fe16-119">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="8fe16-119">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="8fe16-120">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="8fe16-120">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="8fe16-121">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="8fe16-121">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




