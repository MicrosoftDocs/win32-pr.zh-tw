---
description: 由增強影片轉譯器的串流接收器引發 (EVR) 如果影片裝置變更。
ms.assetid: 5b663d6b-5df8-4321-a6a5-a21b9810065a
title: 'MEStreamSinkDeviceChanged 事件 (Mfobjects) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 651fc34a56ca52cfb9e0b3f20e6e4d6b5366f541
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972254"
---
# <a name="mestreamsinkdevicechanged-event"></a><span data-ttu-id="0338f-103">MEStreamSinkDeviceChanged 事件</span><span class="sxs-lookup"><span data-stu-id="0338f-103">MEStreamSinkDeviceChanged event</span></span>

<span data-ttu-id="0338f-104">由增強影片轉譯器的串流接收器引發 (EVR) 如果影片裝置變更。</span><span class="sxs-lookup"><span data-stu-id="0338f-104">Raised by the stream sinks of the enhanced video renderer (EVR) if the video device changes.</span></span> <span data-ttu-id="0338f-105">例如，當 EVR 收到「 [**EC \_ 顯示器」 \_ 變更**](../directshow/ec-display-changed.md) 事件時，會引發此事件。</span><span class="sxs-lookup"><span data-stu-id="0338f-105">For example, the EVR raises this event when it receives an [**EC\_DISPLAY\_CHANGED**](../directshow/ec-display-changed.md) event.</span></span>

<span data-ttu-id="0338f-106">媒體基礎管線會在裝置變更時重新提交所有失敗的範例要求，以回應此事件。</span><span class="sxs-lookup"><span data-stu-id="0338f-106">The Media Foundation pipeline responds to this event by resubmitting all sample requests that failed while the device was changing.</span></span>

## <a name="event-values"></a><span data-ttu-id="0338f-107">事件值</span><span class="sxs-lookup"><span data-stu-id="0338f-107">Event values</span></span>

<span data-ttu-id="0338f-108">從 [**IMFMediaEvent：： GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) 取出的可能值包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="0338f-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0338f-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0338f-109">VARTYPE</span></span>              | <span data-ttu-id="0338f-110">Description</span><span class="sxs-lookup"><span data-stu-id="0338f-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="0338f-111">VT \_ 空白</span><span class="sxs-lookup"><span data-stu-id="0338f-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0338f-112">沒有事件資料。</span><span class="sxs-lookup"><span data-stu-id="0338f-112">No event data.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="0338f-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0338f-113">Requirements</span></span>



| <span data-ttu-id="0338f-114">需求</span><span class="sxs-lookup"><span data-stu-id="0338f-114">Requirement</span></span> | <span data-ttu-id="0338f-115">值</span><span class="sxs-lookup"><span data-stu-id="0338f-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0338f-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0338f-116">Minimum supported client</span></span><br/> | <span data-ttu-id="0338f-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0338f-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0338f-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0338f-118">Minimum supported server</span></span><br/> | <span data-ttu-id="0338f-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0338f-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0338f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="0338f-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="0338f-121"><dt>Mfobjects (包含 Mfidl) </dt></span><span class="sxs-lookup"><span data-stu-id="0338f-121"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0338f-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0338f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0338f-123">媒體基礎事件</span><span class="sxs-lookup"><span data-stu-id="0338f-123">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="0338f-124">媒體接收器</span><span class="sxs-lookup"><span data-stu-id="0338f-124">Media Sinks</span></span>](media-sinks.md)
</dt> </dl>

 

 
