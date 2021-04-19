---
description: 表示 DVD 主要標題的目前音訊串流號碼已變更。
ms.assetid: ab626c6b-765a-4b2e-be96-f45260d1a078
title: 'EC_DVD_AUDIO_STREAM_CHANGE (Dvdevcode) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- EC_DVD_AUDIO_STREAM_CHANGE
api_type:
- HeaderDef
api_location:
- dvdevcode.h
ms.openlocfilehash: 947e19310a77869dbff97851e1ffa0684a3e43a7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106993218"
---
# <a name="ec_dvd_audio_stream_change"></a><span data-ttu-id="e7b3d-103">EC \_ DVD \_ 音訊 \_ 串流 \_ 變更</span><span class="sxs-lookup"><span data-stu-id="e7b3d-103">EC\_DVD\_AUDIO\_STREAM\_CHANGE</span></span>

<span data-ttu-id="e7b3d-104">表示 DVD 主要標題的目前音訊串流號碼已變更。</span><span class="sxs-lookup"><span data-stu-id="e7b3d-104">Signals that the current audio stream number changed for the DVD main title.</span></span>

## <a name="parameters"></a><span data-ttu-id="e7b3d-105">參數</span><span class="sxs-lookup"><span data-stu-id="e7b3d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e7b3d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="e7b3d-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="e7b3d-107">**DWORD** 值，指出新的使用者音訊串流號碼。</span><span class="sxs-lookup"><span data-stu-id="e7b3d-107">**DWORD** value indicating the new user audio stream number.</span></span> <span data-ttu-id="e7b3d-108">音訊串流數位的範圍是從0到7。</span><span class="sxs-lookup"><span data-stu-id="e7b3d-108">Audio stream numbers range from 0 to 7.</span></span> <span data-ttu-id="e7b3d-109">Stream 0xFFFFFFFF 表示未選取任何資料流程。</span><span class="sxs-lookup"><span data-stu-id="e7b3d-109">Stream 0xFFFFFFFF indicates that no stream is selected.</span></span>

</dd> <dt>

<span data-ttu-id="e7b3d-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="e7b3d-110"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="e7b3d-111">零個。</span><span class="sxs-lookup"><span data-stu-id="e7b3d-111">Zero.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e7b3d-112">備註</span><span class="sxs-lookup"><span data-stu-id="e7b3d-112">Remarks</span></span>

<span data-ttu-id="e7b3d-113">目前的音訊串流可以使用在光碟上撰寫的流覽命令，以及透過使用 [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) 介面的應用程式控制，自動變更。</span><span class="sxs-lookup"><span data-stu-id="e7b3d-113">The current audio stream can change automatically with a navigation command authored on the disc as well as through application control by using the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) interface.</span></span>

<span data-ttu-id="e7b3d-114">此事件會在所有網域中引發。</span><span class="sxs-lookup"><span data-stu-id="e7b3d-114">This event is raised in all domains.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7b3d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7b3d-115">Requirements</span></span>



| <span data-ttu-id="e7b3d-116">需求</span><span class="sxs-lookup"><span data-stu-id="e7b3d-116">Requirement</span></span> | <span data-ttu-id="e7b3d-117">值</span><span class="sxs-lookup"><span data-stu-id="e7b3d-117">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7b3d-118">標頭</span><span class="sxs-lookup"><span data-stu-id="e7b3d-118">Header</span></span><br/> | <dl> <span data-ttu-id="e7b3d-119"><dt>Dvdevcode (包含 Dshow) </dt></span><span class="sxs-lookup"><span data-stu-id="e7b3d-119"><dt>Dvdevcode.h (include Dshow.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e7b3d-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e7b3d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e7b3d-121">DVD 應用程式</span><span class="sxs-lookup"><span data-stu-id="e7b3d-121">DVD Applications</span></span>](dvd-applications.md)
</dt> <dt>

[<span data-ttu-id="e7b3d-122">DVD 事件通知碼</span><span class="sxs-lookup"><span data-stu-id="e7b3d-122">DVD Event Notification Codes</span></span>](dvd-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="e7b3d-123">DirectShow 中的事件通知</span><span class="sxs-lookup"><span data-stu-id="e7b3d-123">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

 




