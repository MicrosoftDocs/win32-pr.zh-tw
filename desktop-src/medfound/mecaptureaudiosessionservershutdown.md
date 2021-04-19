---
description: 當捕捉音訊會話因為音訊伺服器關機而中斷連線時，由音訊捕獲來源傳送。
ms.assetid: 43284B3E-3018-44F3-8D6C-8C3041DCCD3E
title: 'MECaptureAudioSessionServerShutdown 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad934f6d60868c1db7c5b5b7907ff720312ea439
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984608"
---
# <a name="mecaptureaudiosessionservershutdown-event"></a><span data-ttu-id="d3da0-103">MECaptureAudioSessionServerShutdown 事件</span><span class="sxs-lookup"><span data-stu-id="d3da0-103">MECaptureAudioSessionServerShutdown event</span></span>

<span data-ttu-id="d3da0-104">當捕捉音訊會話因為音訊伺服器關機而中斷連線時，由音訊捕獲來源傳送。</span><span class="sxs-lookup"><span data-stu-id="d3da0-104">Sent by an audio capture source when the capture audio session is disconnected due to the audio server being shutdown.</span></span>

## <a name="event-values"></a><span data-ttu-id="d3da0-105">事件值</span><span class="sxs-lookup"><span data-stu-id="d3da0-105">Event values</span></span>

<span data-ttu-id="d3da0-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="d3da0-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d3da0-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d3da0-107">VARTYPE</span></span>               | <span data-ttu-id="d3da0-108">Description</span><span class="sxs-lookup"><span data-stu-id="d3da0-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="d3da0-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="d3da0-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="d3da0-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="d3da0-110">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="d3da0-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3da0-111">Requirements</span></span>



| <span data-ttu-id="d3da0-112">需求</span><span class="sxs-lookup"><span data-stu-id="d3da0-112">Requirement</span></span> | <span data-ttu-id="d3da0-113">值</span><span class="sxs-lookup"><span data-stu-id="d3da0-113">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3da0-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3da0-114">Minimum supported client</span></span><br/> | <span data-ttu-id="d3da0-115">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3da0-115">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="d3da0-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3da0-116">Minimum supported server</span></span><br/> | <span data-ttu-id="d3da0-117">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3da0-117">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d3da0-118">標頭</span><span class="sxs-lookup"><span data-stu-id="d3da0-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="d3da0-119"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="d3da0-119"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d3da0-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d3da0-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d3da0-121">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="d3da0-121">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




