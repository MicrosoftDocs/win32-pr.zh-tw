---
description: 通知媒體基礎轉換 (MFT) 資料流程即將開始。
ms.assetid: a7f02e92-a747-4ac6-aa83-60897acb2bc5
title: 'MFT_MESSAGE_NOTIFY_BEGIN_STREAMING (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1aa67f58c7246b50292f4b34711e0149eb8f3377
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191779"
---
# <a name="mft_message_notify_begin_streaming"></a><span data-ttu-id="48156-103">MFT \_ 訊息 \_ 通知 \_ 開始 \_ 串流</span><span class="sxs-lookup"><span data-stu-id="48156-103">MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING</span></span>

<span data-ttu-id="48156-104">通知媒體基礎轉換 (MFT) 資料流程即將開始。</span><span class="sxs-lookup"><span data-stu-id="48156-104">Notifies a Media Foundation transform (MFT) that streaming is about to begin.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="48156-105">Message 參數</span><span class="sxs-lookup"><span data-stu-id="48156-105">Message Parameter</span></span>

<span data-ttu-id="48156-106">無。</span><span class="sxs-lookup"><span data-stu-id="48156-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="48156-107">備註</span><span class="sxs-lookup"><span data-stu-id="48156-107">Remarks</span></span>

<span data-ttu-id="48156-108">若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。</span><span class="sxs-lookup"><span data-stu-id="48156-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="48156-109">用戶端不需要傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="48156-109">The client is not required to send this message.</span></span> <span data-ttu-id="48156-110">如果用戶端傳送此訊息，則必須在設定所有在 MFT 上的媒體類型之後，以及在呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)之前這麼做。</span><span class="sxs-lookup"><span data-stu-id="48156-110">If the client sends this message, it must do so after setting all of the media types on the MFT, and before calling [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span> <span data-ttu-id="48156-111">MFT 可透過配置緩衝區或其他資源來回應。</span><span class="sxs-lookup"><span data-stu-id="48156-111">The MFT can respond by allocating buffers or other resources.</span></span> <span data-ttu-id="48156-112">如果用戶端未傳送此訊息，則在第一次呼叫 **ProcessInput** 時，MFT 會配置資源。</span><span class="sxs-lookup"><span data-stu-id="48156-112">If the client does not send this message, the MFT allocates resources on the first call to **ProcessInput**.</span></span> <span data-ttu-id="48156-113">因此，傳送此訊息可減少串流開始時的初始延遲。</span><span class="sxs-lookup"><span data-stu-id="48156-113">Therefore, sending this message can reduce the initial latency when streaming begins.</span></span>

### <a name="implementation"></a><span data-ttu-id="48156-114">實作</span><span class="sxs-lookup"><span data-stu-id="48156-114">Implementation</span></span>

<span data-ttu-id="48156-115">不需要使用 MFT 來回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="48156-115">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="48156-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="48156-116">Requirements</span></span>



| <span data-ttu-id="48156-117">需求</span><span class="sxs-lookup"><span data-stu-id="48156-117">Requirement</span></span> | <span data-ttu-id="48156-118">值</span><span class="sxs-lookup"><span data-stu-id="48156-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="48156-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="48156-119">Minimum supported client</span></span><br/> | <span data-ttu-id="48156-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48156-120">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="48156-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="48156-121">Minimum supported server</span></span><br/> | <span data-ttu-id="48156-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="48156-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="48156-123">標頭</span><span class="sxs-lookup"><span data-stu-id="48156-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="48156-124"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="48156-124"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48156-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="48156-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48156-126">**MFT \_ 訊息 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="48156-126">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




