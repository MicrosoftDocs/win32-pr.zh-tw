---
description: 要求媒體基礎轉換 (MFT) 至該資料流程即將結束。
ms.assetid: df313a66-e80f-499c-a9f2-a7cbaaf0a7d4
title: 'MFT_MESSAGE_NOTIFY_END_STREAMING (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad2f13635b97db0c6d7751d9648f42b2b4ed8acc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512604"
---
# <a name="mft_message_notify_end_streaming"></a><span data-ttu-id="e1833-103">MFT \_ 訊息 \_ 通知 \_ 結束 \_ 資料流程</span><span class="sxs-lookup"><span data-stu-id="e1833-103">MFT\_MESSAGE\_NOTIFY\_END\_STREAMING</span></span>

<span data-ttu-id="e1833-104">要求媒體基礎轉換 (MFT) 至該資料流程即將結束。</span><span class="sxs-lookup"><span data-stu-id="e1833-104">Requests a Media Foundation transform (MFT) to that streaming is about to end.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="e1833-105">Message 參數</span><span class="sxs-lookup"><span data-stu-id="e1833-105">Message Parameter</span></span>

<span data-ttu-id="e1833-106">無。</span><span class="sxs-lookup"><span data-stu-id="e1833-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1833-107">備註</span><span class="sxs-lookup"><span data-stu-id="e1833-107">Remarks</span></span>

<span data-ttu-id="e1833-108">若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。</span><span class="sxs-lookup"><span data-stu-id="e1833-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="e1833-109">用戶端不需要傳送此訊息，即使用戶端先前傳送的是 **MFT \_ 訊息 \_ 通知 \_ 開始 \_ 串流** 訊息也是如此。</span><span class="sxs-lookup"><span data-stu-id="e1833-109">The client is not required to send this message, even if the client previously sent the **MFT\_MESSAGE\_NOTIFY\_BEGIN\_STREAMING** message.</span></span>

### <a name="implementation"></a><span data-ttu-id="e1833-110">實作</span><span class="sxs-lookup"><span data-stu-id="e1833-110">Implementation</span></span>

<span data-ttu-id="e1833-111">藉由釋放緩衝區和其他資源，此 MFT 可以回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="e1833-111">The MFT can respond to this message by releasing buffers and other resources.</span></span> <span data-ttu-id="e1833-112">在回應此訊息時，MFT 不會排清輸入資料或重設媒體類型。</span><span class="sxs-lookup"><span data-stu-id="e1833-112">The MFT does not flush input data or reset the media types in response to this message.</span></span> <span data-ttu-id="e1833-113">不需要使用 MFT 來回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="e1833-113">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1833-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e1833-114">Requirements</span></span>



| <span data-ttu-id="e1833-115">需求</span><span class="sxs-lookup"><span data-stu-id="e1833-115">Requirement</span></span> | <span data-ttu-id="e1833-116">值</span><span class="sxs-lookup"><span data-stu-id="e1833-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1833-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e1833-117">Minimum supported client</span></span><br/> | <span data-ttu-id="e1833-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1833-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="e1833-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e1833-119">Minimum supported server</span></span><br/> | <span data-ttu-id="e1833-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e1833-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e1833-121">標頭</span><span class="sxs-lookup"><span data-stu-id="e1833-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="e1833-122"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="e1833-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1833-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e1833-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1833-124">**MFT \_ 訊息 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="e1833-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




