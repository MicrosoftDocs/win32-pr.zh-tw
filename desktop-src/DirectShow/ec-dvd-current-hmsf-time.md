---
description: 以 DVD \_ HMSF 時間 \_ 碼格式，表示與標題開頭相關的目前時間。 此事件會在每個 VOBU 的開頭觸發，每隔0.4 到1.0 秒就會發生一次。
ms.assetid: 7c81a09a-21f3-49b2-b90a-7cbc9c815bad
title: 'EC_DVD_CURRENT_HMSF_TIME (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_CURRENT_HMSF_TIME
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 36306b95682e62ffebf8fb819dcc4b7c5185493c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997633"
---
# <a name="ec_dvd_current_hmsf_time"></a><span data-ttu-id="bb759-104">EC \_ DVD \_ 目前 \_ HMSF \_ 時間</span><span class="sxs-lookup"><span data-stu-id="bb759-104">EC\_DVD\_CURRENT\_HMSF\_TIME</span></span>

<span data-ttu-id="bb759-105">以 [**DVD \_ HMSF 時間 \_ 碼**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) 格式，表示與標題開頭相關的目前時間。</span><span class="sxs-lookup"><span data-stu-id="bb759-105">Signals the current time, in [**DVD\_HMSF\_TIMECODE**](/windows/win32/api/strmif/ns-strmif-dvd_hmsf_timecode) format, relative to the start of the title.</span></span> <span data-ttu-id="bb759-106">此事件會在每個 VOBU 的開頭觸發，每隔0.4 到1.0 秒就會發生一次。</span><span class="sxs-lookup"><span data-stu-id="bb759-106">This event is triggered at the beginning of every VOBU, which occurs every 0.4 to 1.0 seconds.</span></span>

## <a name="parameters"></a><span data-ttu-id="bb759-107">參數</span><span class="sxs-lookup"><span data-stu-id="bb759-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bb759-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="bb759-108"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="bb759-109">包含 DVD HMSF 時間碼結構的 ULONG 值 \_ \_ 。</span><span class="sxs-lookup"><span data-stu-id="bb759-109">A ULONG value that contains the DVD\_HMSF\_TIMECODE structure.</span></span> <span data-ttu-id="bb759-110">將 lParam1 指派給 ULONG 變數，然後將該變數轉換成 DVD \_ HMSF 時間 \_ 碼，以存取其值。</span><span class="sxs-lookup"><span data-stu-id="bb759-110">Assign lParam1 to a ULONG variable and then cast that variable to a DVD\_HMSF\_TIMECODE to access its values.</span></span>

</dd> <dt>

<span data-ttu-id="bb759-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="bb759-111"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="bb759-112">包含 [**DVD 時間 \_ 碼 \_ 旗標**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags)聯集的 ULONG 值。</span><span class="sxs-lookup"><span data-stu-id="bb759-112">A ULONG value containing a union of [**DVD\_TIMECODE\_FLAGS**](/windows/win32/api/strmif/ne-strmif-dvd_timecode_flags).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="bb759-113">備註</span><span class="sxs-lookup"><span data-stu-id="bb759-113">Remarks</span></span>

<span data-ttu-id="bb759-114">DVD \_ HMSF \_ 時間碼格式的目的是要取代在 EC \_ DVD \_ 目前時間事件中傳回的舊 BCD 格式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bb759-114">The DVD\_HMSF\_TIMECODE format is intended to replace the old BCD format that is returned in EC\_DVD\_CURRENT\_TIME events.</span></span> <span data-ttu-id="bb759-115">HMSF 的時間碼比較容易使用。</span><span class="sxs-lookup"><span data-stu-id="bb759-115">The HMSF timecodes are easier to work with.</span></span> <span data-ttu-id="bb759-116">若要讓 Navigator 傳送 EC \_ dvd \_ 目前 \_ HMSF \_ 時間事件，而不是 ec \_ dvd \_ 目前 \_ 時間事件，應用程式必須呼叫 `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)` 。</span><span class="sxs-lookup"><span data-stu-id="bb759-116">To have the Navigator send EC\_DVD\_CURRENT\_HMSF\_TIME events instead of EC\_DVD\_CURRENT\_TIME events, an application must call `IDvdControl2::SetOption(DVD_HMSF_TimeCodeEvents, TRUE)`.</span></span> <span data-ttu-id="bb759-117">設定此旗標時，導覽器也會預期 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 和 [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) 方法中的所有時間參數都必須以 DVD HMSF 時間 \_ 碼傳遞 \_ 。</span><span class="sxs-lookup"><span data-stu-id="bb759-117">When this flag is set, the Navigator will also expect all time parameters in the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) and [**IDvdInfo2**](/windows/desktop/api/Strmif/nn-strmif-idvdinfo2) methods to be passed as DVD\_HMSF\_TIMECODEs.</span></span>

<span data-ttu-id="bb759-118">此事件會在標題網域中引發。</span><span class="sxs-lookup"><span data-stu-id="bb759-118">This event is raised in the title domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb759-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb759-119">Requirements</span></span>



| <span data-ttu-id="bb759-120">需求</span><span class="sxs-lookup"><span data-stu-id="bb759-120">Requirement</span></span> | <span data-ttu-id="bb759-121">值</span><span class="sxs-lookup"><span data-stu-id="bb759-121">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bb759-122">標頭</span><span class="sxs-lookup"><span data-stu-id="bb759-122">Header</span></span><br/> | <dl> <span data-ttu-id="bb759-123"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="bb759-123"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb759-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb759-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb759-125">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="bb759-125">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="bb759-126">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="bb759-126">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="bb759-127">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="bb759-127">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




