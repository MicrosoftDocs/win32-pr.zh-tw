---
description: 由封裝裝置的 IMFMediaSource 所傳送，表示已移除裝置。
ms.assetid: 107AFF19-B444-4B62-9217-46A99AC3632C
title: 'MEVideoCaptureDeviceRemoved 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e3276f53f86bdce78825b94828577eab9e40954
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992486"
---
# <a name="mevideocapturedeviceremoved-event"></a><span data-ttu-id="412e9-103">MEVideoCaptureDeviceRemoved 事件</span><span class="sxs-lookup"><span data-stu-id="412e9-103">MEVideoCaptureDeviceRemoved event</span></span>

<span data-ttu-id="412e9-104">由封裝裝置的 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 所傳送，表示已移除裝置。</span><span class="sxs-lookup"><span data-stu-id="412e9-104">Sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device to indicate that the device has been removed.</span></span>

## <a name="event-values"></a><span data-ttu-id="412e9-105">事件值</span><span class="sxs-lookup"><span data-stu-id="412e9-105">Event values</span></span>

<span data-ttu-id="412e9-106">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="412e9-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="412e9-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="412e9-107">VARTYPE</span></span>               | <span data-ttu-id="412e9-108">Description</span><span class="sxs-lookup"><span data-stu-id="412e9-108">Description</span></span>                           |
|-----------------------|---------------------------------------|
| <span data-ttu-id="412e9-109">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="412e9-109">VT\_EMPTY</span></span> <br/> | <span data-ttu-id="412e9-110">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="412e9-110">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="412e9-111">備註</span><span class="sxs-lookup"><span data-stu-id="412e9-111">Remarks</span></span>

<span data-ttu-id="412e9-112">此事件是由封裝裝置的 [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) 所傳送。</span><span class="sxs-lookup"><span data-stu-id="412e9-112">This event is sent by the [**IMFMediaSource**](/windows/desktop/api/mfidl/nn-mfidl-imfmediasource) that encapsulates the device.</span></span>

## <a name="requirements"></a><span data-ttu-id="412e9-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="412e9-113">Requirements</span></span>



| <span data-ttu-id="412e9-114">需求</span><span class="sxs-lookup"><span data-stu-id="412e9-114">Requirement</span></span> | <span data-ttu-id="412e9-115">值</span><span class="sxs-lookup"><span data-stu-id="412e9-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="412e9-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="412e9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="412e9-117">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="412e9-117">Windows 8 \[desktop apps only\]</span></span><br/>                                                               |
| <span data-ttu-id="412e9-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="412e9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="412e9-119">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="412e9-119">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="412e9-120">標頭</span><span class="sxs-lookup"><span data-stu-id="412e9-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="412e9-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="412e9-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="412e9-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="412e9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="412e9-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="412e9-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




