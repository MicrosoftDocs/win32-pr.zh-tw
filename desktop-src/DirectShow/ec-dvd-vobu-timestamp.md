---
description: EC_DVD_VOBU_Timestamp-當 DVD 導覽器剖析 PCI 封包時傳送。
ms.assetid: 25548c23-22f0-47cb-9062-273ad39d3007
title: 'EC_DVD_VOBU_Timestamp (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_VOBU_Timestamp
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 6bd06eb99cae60960db64a6f32df5e4c932b362f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108094616"
---
# <a name="ec_dvd_vobu_timestamp"></a><span data-ttu-id="da4ad-103">EC \_ DVD \_ VOBU \_ 時間戳記</span><span class="sxs-lookup"><span data-stu-id="da4ad-103">EC\_DVD\_VOBU\_Timestamp</span></span>

<span data-ttu-id="da4ad-104">當 DVD 導覽 [器](dvd-navigator-filter.md) 剖析 PCI 封包時傳送。</span><span class="sxs-lookup"><span data-stu-id="da4ad-104">Sent when the [DVD Navigator](dvd-navigator-filter.md) parses a PCI packet.</span></span>

<span data-ttu-id="da4ad-105">事件資料是最新影片物件單位的時間戳記 (VOBU) 。</span><span class="sxs-lookup"><span data-stu-id="da4ad-105">The event data is the time stamp of the most recent video object unit (VOBU).</span></span>

## <a name="parameters"></a><span data-ttu-id="da4ad-106">參數</span><span class="sxs-lookup"><span data-stu-id="da4ad-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da4ad-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="da4ad-107"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="da4ad-108">包含時間戳記的低序位 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="da4ad-108">Contains the low-order **DWORD** of the time stamp.</span></span>

</dd> <dt>

<span data-ttu-id="da4ad-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="da4ad-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="da4ad-110">包含時間戳記的高序位 **DWORD** 。</span><span class="sxs-lookup"><span data-stu-id="da4ad-110">Contains the high-order **DWORD** of the time stamp.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="da4ad-111">備註</span><span class="sxs-lookup"><span data-stu-id="da4ad-111">Remarks</span></span>

<span data-ttu-id="da4ad-112">此事件預設為停用。</span><span class="sxs-lookup"><span data-stu-id="da4ad-112">This event is disabled by default.</span></span> <span data-ttu-id="da4ad-113">若要啟用此事件，請呼叫 [**IDvdControl2：： SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) ，並將 **DVD \_ EnableLoggingEvents** 選項設定為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="da4ad-113">To enable this event, call [**IDvdControl2::SetOption**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-setoption) and set the **DVD\_EnableLoggingEvents** option to **TRUE**.</span></span>

<span data-ttu-id="da4ad-114">重建時間戳記，如下所示：</span><span class="sxs-lookup"><span data-stu-id="da4ad-114">Reconstruct the time stamp as follows:</span></span>


```C++
LARGE_INTEGER li;
li.LowPart = DWORD( lParam1 );
li.HighPart = DWORD( lParam2 );
```



## <a name="requirements"></a><span data-ttu-id="da4ad-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="da4ad-115">Requirements</span></span>



| <span data-ttu-id="da4ad-116">需求</span><span class="sxs-lookup"><span data-stu-id="da4ad-116">Requirement</span></span> | <span data-ttu-id="da4ad-117">值</span><span class="sxs-lookup"><span data-stu-id="da4ad-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="da4ad-118">標頭</span><span class="sxs-lookup"><span data-stu-id="da4ad-118">Header</span></span><br/> | <dl> <span data-ttu-id="da4ad-119"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="da4ad-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="da4ad-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="da4ad-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da4ad-121">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="da4ad-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="da4ad-122">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="da4ad-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="da4ad-123">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="da4ad-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




