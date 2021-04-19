---
description: 標記資料流程中的點。 此訊息只適用于非同步 MFTs。
ms.assetid: eae1d066-64af-45e2-b8bb-eddf9147ad8b
title: 'MFT_MESSAGE_COMMAND_MARKER (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3802cb94c9183d4f392fbcedcf48c0c01071298e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992439"
---
# <a name="mft_message_command_marker"></a><span data-ttu-id="2b483-104">MFT \_ 訊息 \_ 命令 \_ 標記</span><span class="sxs-lookup"><span data-stu-id="2b483-104">MFT\_MESSAGE\_COMMAND\_MARKER</span></span>

<span data-ttu-id="2b483-105">標記資料流程中的點。</span><span class="sxs-lookup"><span data-stu-id="2b483-105">Marks a point in the stream.</span></span> <span data-ttu-id="2b483-106">此訊息只適用于 [非同步 MFTs](asynchronous-mfts.md)。</span><span class="sxs-lookup"><span data-stu-id="2b483-106">This message applies only to [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="message-parameter"></a><span data-ttu-id="2b483-107">Message 參數</span><span class="sxs-lookup"><span data-stu-id="2b483-107">Message Parameter</span></span>

<span data-ttu-id="2b483-108">任意值。</span><span class="sxs-lookup"><span data-stu-id="2b483-108">An arbitrary value.</span></span> <span data-ttu-id="2b483-109">在 [METransformMarker](metransformmarker.md) 事件中，MFT 會將值傳回給用戶端。</span><span class="sxs-lookup"><span data-stu-id="2b483-109">The MFT returns the value to the client in the [METransformMarker](metransformmarker.md) event.</span></span>

## <a name="remarks"></a><span data-ttu-id="2b483-110">備註</span><span class="sxs-lookup"><span data-stu-id="2b483-110">Remarks</span></span>

<span data-ttu-id="2b483-111">若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。</span><span class="sxs-lookup"><span data-stu-id="2b483-111">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="2b483-112">MFT 會回應此 messageas，如下所示：</span><span class="sxs-lookup"><span data-stu-id="2b483-112">The MFT responds to this messageas follows:</span></span>

1.  <span data-ttu-id="2b483-113">MFT 會從現有的輸入資料產生任意數量的輸出範例，並為每個輸出範例傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="2b483-113">The MFT generates as many output samples as it can from the existing input data, sending an [METransformHaveOutput](metransformhaveoutput.md) event for each output sample.</span></span>
2.  <span data-ttu-id="2b483-114">產生所有輸出之後，MFT 會傳送 [METransformMarker](metransformmarker.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="2b483-114">After all of the output is generated, the MFT sends an [METransformMarker](metransformmarker.md) event.</span></span> <span data-ttu-id="2b483-115">此事件必須在所有 [METransformHaveOutput](metransformhaveoutput.md) 事件之後傳送。</span><span class="sxs-lookup"><span data-stu-id="2b483-115">This event must be sent after all of the [METransformHaveOutput](metransformhaveoutput.md) events.</span></span>

<span data-ttu-id="2b483-116">用戶端不需要傳送此訊息，而且應該只傳送此訊息給非同步 MFTs。</span><span class="sxs-lookup"><span data-stu-id="2b483-116">The client is not required to send this message, and should send this message only to asynchronous MFTs.</span></span> <span data-ttu-id="2b483-117">同步的 MFT 不會傳送 [METransformMarker](metransformmarker.md) 事件以回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="2b483-117">A synchronous MFT will not send an [METransformMarker](metransformmarker.md) event in response to this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="2b483-118">實作</span><span class="sxs-lookup"><span data-stu-id="2b483-118">Implementation</span></span>

<span data-ttu-id="2b483-119">非同步 MFTs 必須如所述回應此訊息。</span><span class="sxs-lookup"><span data-stu-id="2b483-119">Asynchronous MFTs must respond to this message as described.</span></span> <span data-ttu-id="2b483-120">同步 MFTs 應該忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="2b483-120">Synchronous MFTs should ignore this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b483-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="2b483-121">Requirements</span></span>



| <span data-ttu-id="2b483-122">需求</span><span class="sxs-lookup"><span data-stu-id="2b483-122">Requirement</span></span> | <span data-ttu-id="2b483-123">值</span><span class="sxs-lookup"><span data-stu-id="2b483-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b483-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2b483-124">Minimum supported client</span></span><br/> | <span data-ttu-id="2b483-125">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b483-125">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="2b483-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2b483-126">Minimum supported server</span></span><br/> | <span data-ttu-id="2b483-127">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2b483-127">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="2b483-128">標頭</span><span class="sxs-lookup"><span data-stu-id="2b483-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b483-129"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="2b483-129"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b483-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2b483-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b483-131">**MFT \_ 訊息 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="2b483-131">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




