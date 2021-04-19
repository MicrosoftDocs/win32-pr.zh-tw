---
description: 通知媒體基礎轉換 (MFT) 輸入資料流程已結束。
ms.assetid: 2d6cdf45-1bb4-4915-bd27-efa041089100
title: 'MFT_MESSAGE_NOTIFY_END_OF_STREAM (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 476781b149553bec1d48632e0621ff0a38ad8d21
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974206"
---
# <a name="mft_message_notify_end_of_stream"></a><span data-ttu-id="59d0b-103">MFT \_ 訊息 \_ 通知 \_ 結束 \_ \_ 資料流程</span><span class="sxs-lookup"><span data-stu-id="59d0b-103">MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM</span></span>

<span data-ttu-id="59d0b-104">通知媒體基礎轉換 (MFT) 輸入資料流程已結束。</span><span class="sxs-lookup"><span data-stu-id="59d0b-104">Notifies a Media Foundation transform (MFT) that an input stream has ended.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="59d0b-105">Message 參數</span><span class="sxs-lookup"><span data-stu-id="59d0b-105">Message Parameter</span></span>

<span data-ttu-id="59d0b-106">*UlParam* 參數包含輸入資料流程的識別碼，指定為 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="59d0b-106">The *ulParam* parameter contains the identifier of the input stream, specified as a **DWORD** value.</span></span> <span data-ttu-id="59d0b-107">在64位應用程式中，將此值放在 **ULONG \_ PTR** 的較低32位。</span><span class="sxs-lookup"><span data-stu-id="59d0b-107">In 64-bit applications, place this value in the lower 32-bits of the **ULONG\_PTR**.</span></span>

## <a name="remarks"></a><span data-ttu-id="59d0b-108">備註</span><span class="sxs-lookup"><span data-stu-id="59d0b-108">Remarks</span></span>

<span data-ttu-id="59d0b-109">若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。</span><span class="sxs-lookup"><span data-stu-id="59d0b-109">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="59d0b-110">用戶端不需要傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="59d0b-110">The client is not required to send this message.</span></span>

<span data-ttu-id="59d0b-111">資料流程結束後，用戶端可以再次呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) ，以傳送該資料流程的新資料。</span><span class="sxs-lookup"><span data-stu-id="59d0b-111">After a stream ends, the client may call [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) again to send new data for that stream.</span></span> <span data-ttu-id="59d0b-112">如果是的話，用戶端必須在資料流程結束後的第一個輸入範例中，將不中斷屬性 (MFSampleExtension 不中斷屬性) 。 [**\_**](mfsampleextension-discontinuity-attribute.md)</span><span class="sxs-lookup"><span data-stu-id="59d0b-112">If so, the client must set the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute) on the first input sample after the stream ends.</span></span> <span data-ttu-id="59d0b-113"> (用戶端應該一律在資料流程結束後的第一個新範例上設定此屬性，不論用戶端是否傳送了 **訊息 \_ 通知的訊息 \_ 通知 \_ 結尾 \_ \_** 。</span><span class="sxs-lookup"><span data-stu-id="59d0b-113">(The client should always set this attribute on the first new sample after a stream ends, regardless of whether the client sent the **MFT\_MESSAGE\_NOTIFY\_END\_OF\_STREAM** message.</span></span> <span data-ttu-id="59d0b-114">如需處理不連續的詳細資訊，請參閱 [基本的 MFT 處理模型](basic-mft-processing-model.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="59d0b-114">For more information about handling discontinuities, see [Basic MFT Processing Model](basic-mft-processing-model.md).)</span></span>

<span data-ttu-id="59d0b-115">針對每個輸入資料流程傳送此訊息之後，用戶端通常會傳送 **MFT \_ 訊息 \_ 命令 \_ 清空** 命令，然後收集剩餘的輸出。</span><span class="sxs-lookup"><span data-stu-id="59d0b-115">After sending this message for every input stream, the client typically sends an **MFT\_MESSAGE\_COMMAND\_DRAIN** command and then collects the remaining output.</span></span> <span data-ttu-id="59d0b-116">不過，用戶端不需要清空 MFT。</span><span class="sxs-lookup"><span data-stu-id="59d0b-116">However, the client is not required to drain the MFT.</span></span> <span data-ttu-id="59d0b-117">如果用戶端未清空 MFT，則在下次呼叫 [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)時，MFT 通常會捨棄任何未處理的資料（當偵測到資料流程不連續時）。</span><span class="sxs-lookup"><span data-stu-id="59d0b-117">If the client does not drain the MFT, the MFT will typically discard any unprocessed data on the next call to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput), when it detects the stream discontinuity.</span></span> <span data-ttu-id="59d0b-118">或者，用戶端可能會在呼叫 **ProcessInput** 之前排清 MFT。</span><span class="sxs-lookup"><span data-stu-id="59d0b-118">Alternatively, the client might flush the MFT before calling **ProcessInput**.</span></span>

<span data-ttu-id="59d0b-119">此訊息不會移除輸入資料流程或重設媒體類型。</span><span class="sxs-lookup"><span data-stu-id="59d0b-119">This message does not remove the input stream or reset the media type.</span></span>

### <a name="implementation"></a><span data-ttu-id="59d0b-120">實作</span><span class="sxs-lookup"><span data-stu-id="59d0b-120">Implementation</span></span>

<span data-ttu-id="59d0b-121">不需要使用 MFT 來回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="59d0b-121">An MFT is not required to respond to this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="59d0b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="59d0b-122">Requirements</span></span>



| <span data-ttu-id="59d0b-123">需求</span><span class="sxs-lookup"><span data-stu-id="59d0b-123">Requirement</span></span> | <span data-ttu-id="59d0b-124">值</span><span class="sxs-lookup"><span data-stu-id="59d0b-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="59d0b-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="59d0b-125">Minimum supported client</span></span><br/> | <span data-ttu-id="59d0b-126">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59d0b-126">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="59d0b-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="59d0b-127">Minimum supported server</span></span><br/> | <span data-ttu-id="59d0b-128">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="59d0b-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="59d0b-129">標頭</span><span class="sxs-lookup"><span data-stu-id="59d0b-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="59d0b-130"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="59d0b-130"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="59d0b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="59d0b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59d0b-132">**MFT \_ 訊息 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="59d0b-132">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




