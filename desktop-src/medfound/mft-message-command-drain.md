---
description: MFT_MESSAGE_COMMAND_DRAIN-要求媒體基礎轉換 (MFT) 以排清所有儲存的資料。
ms.assetid: c48f3a88-a007-4f30-ac60-9e5a8c24e1ee
title: 'MFT_MESSAGE_COMMAND_DRAIN (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 907bfbd888b1eccbe7336c0d8f386d3266fd8e9b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092746"
---
# <a name="mft_message_command_drain"></a><span data-ttu-id="56764-103">MFT \_ 訊息 \_ 命令 \_ 清空</span><span class="sxs-lookup"><span data-stu-id="56764-103">MFT\_MESSAGE\_COMMAND\_DRAIN</span></span>

<span data-ttu-id="56764-104">要求媒體基礎轉換 (MFT) 以排清所有儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="56764-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="56764-105">Message 參數</span><span class="sxs-lookup"><span data-stu-id="56764-105">Message Parameter</span></span>

<span data-ttu-id="56764-106">無。</span><span class="sxs-lookup"><span data-stu-id="56764-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="56764-107">備註</span><span class="sxs-lookup"><span data-stu-id="56764-107">Remarks</span></span>

<span data-ttu-id="56764-108">若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。</span><span class="sxs-lookup"><span data-stu-id="56764-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="56764-109">傳送此訊息之後，指定的輸入資料流程不接受輸入，直到 MFT 處理來自先前呼叫 [**IMFTransform：:P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)的所有資料為止。</span><span class="sxs-lookup"><span data-stu-id="56764-109">After this message is sent, the specified input stream does not accept input until the MFT processes all data from previous calls to [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput).</span></span>

<span data-ttu-id="56764-110">在同步 MFTs 與非同步 MFTs 之間，清空程式會稍有不同：</span><span class="sxs-lookup"><span data-stu-id="56764-110">The draining process varies slightly between synchronous MFTs and asynchronous MFTs:</span></span>

<span data-ttu-id="56764-111">**同步 MFTs**</span><span class="sxs-lookup"><span data-stu-id="56764-111">**Synchronous MFTs**</span></span>

1.  <span data-ttu-id="56764-112">用戶端傳送此訊息之後，它會在迴圈中呼叫 [**IMFTransform：:P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) ，直到 **ProcessOutput** 傳回錯誤碼 **MF \_ E \_ 轉換 \_ 需要 \_ 更多 \_ 輸入**。</span><span class="sxs-lookup"><span data-stu-id="56764-112">After the client sends this message, it calls [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) in a loop, until **ProcessOutput** returns the error code **MF\_E\_TRANSFORM\_NEED\_MORE\_INPUT**.</span></span>
2.  <span data-ttu-id="56764-113">只要 MFT 仍有要處理的資料， [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) 的後續呼叫就會失敗。</span><span class="sxs-lookup"><span data-stu-id="56764-113">As long as the MFT still has data to process, further calls to [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) will fail.</span></span> <span data-ttu-id="56764-114">MFT 會繼續產生輸出，直到它使用所有儲存的資料為止。</span><span class="sxs-lookup"><span data-stu-id="56764-114">The MFT continues to produce output until it uses all stored data.</span></span> <span data-ttu-id="56764-115">MFT 會捨棄無法處理為完整輸出範例的任何資料。</span><span class="sxs-lookup"><span data-stu-id="56764-115">The MFT discards any data that cannot be processed into a complete output sample.</span></span> <span data-ttu-id="56764-116"> (例如，它應該卸載部分影片框架。 ) </span><span class="sxs-lookup"><span data-stu-id="56764-116">(For example, it should drop a partial video frame.)</span></span>

<span data-ttu-id="56764-117">**非同步 MFTs**</span><span class="sxs-lookup"><span data-stu-id="56764-117">**Asynchronous MFTs**</span></span>

1.  <span data-ttu-id="56764-118">MFT 會繼續傳送 [METransformHaveOutput](metransformhaveoutput.md) 事件，直到它沒有其他要處理的資料為止。</span><span class="sxs-lookup"><span data-stu-id="56764-118">The MFT continues to send [METransformHaveOutput](metransformhaveoutput.md) events until it has no more data to process.</span></span> <span data-ttu-id="56764-119">它不會在這段時間內傳送 [METransformNeedInput](metransformneedinput.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="56764-119">It does not send [METransformNeedInput](metransformneedinput.md) events during this time.</span></span>
2.  <span data-ttu-id="56764-120">在 MFT 傳送最後一個 [METransformHaveOutput](metransformhaveoutput.md) 事件之後，它會傳送 [METransformDrainComplete](metransformdraincomplete.md) 事件。</span><span class="sxs-lookup"><span data-stu-id="56764-120">After the MFT sends the last [METransformHaveOutput](metransformhaveoutput.md) event, it sends an [METransformDrainComplete](metransformdraincomplete.md) event.</span></span>
3.  <span data-ttu-id="56764-121">完成清空之後，除非從用戶端接收到來自用戶端 [**\_ \_ \_ \_ 的 \_ 訊息訊息通知**](mft-message-notify-start-of-stream.md)，否則 mft 不會傳送另一個 [METransformNeedInput](metransformneedinput.md)事件。</span><span class="sxs-lookup"><span data-stu-id="56764-121">After draining is complete, the MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

<span data-ttu-id="56764-122">在用戶端清空 MFT 之後，用戶端就可以傳送更多輸入資料。</span><span class="sxs-lookup"><span data-stu-id="56764-122">After the client has drained the MFT, the client can send more input data.</span></span> <span data-ttu-id="56764-123">清空作業之後的第一個範例必須具有不連續屬性 ([**MFSampleExtension \_**](mfsampleextension-discontinuity-attribute.md) 不連續屬性) 。</span><span class="sxs-lookup"><span data-stu-id="56764-123">The first sample after the drain operation must have the discontinuity attribute ([**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute).</span></span>

> [!Note]  
> <span data-ttu-id="56764-124">本檔的先前版本指出 *ulParam* 事件參數是 [**\_ MFT \_ 清空 \_ 類型**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type)列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="56764-124">Earlier versions of this documentation stated that the *ulParam* event parameter is a member of the [**\_MFT\_DRAIN\_TYPE**](/windows/win32/api/mftransform/ne-mftransform-_mft_drain_type) enumeration.</span></span> <span data-ttu-id="56764-125">不正確。</span><span class="sxs-lookup"><span data-stu-id="56764-125">That is not correct.</span></span> <span data-ttu-id="56764-126">*UlParam* 包含資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="56764-126">The *ulParam* contains a stream identifier.</span></span>

 

### <a name="implementation"></a><span data-ttu-id="56764-127">實作</span><span class="sxs-lookup"><span data-stu-id="56764-127">Implementation</span></span>

<span data-ttu-id="56764-128">非同步 MFT 在 [METransformDrainComplete](metransformdraincomplete.md) 之後必須一律傳回。</span><span class="sxs-lookup"><span data-stu-id="56764-128">An asynchronous MFT must always return [METransformDrainComplete](metransformdraincomplete.md) after it has drained.</span></span>

<span data-ttu-id="56764-129">如果下列條件成立，同步的 MFT 可以忽略此訊息並傳回 S \_ OK：</span><span class="sxs-lookup"><span data-stu-id="56764-129">A synchronous MFT can ignore this message and return S\_OK if the following conditions are true:</span></span>

-   <span data-ttu-id="56764-130">此 MFT 一次絕不會儲存一個以上的輸入範例。</span><span class="sxs-lookup"><span data-stu-id="56764-130">The MFT never stores more than one input sample at a time.</span></span>
-   <span data-ttu-id="56764-131">每個輸入範例都會產生單一輸出範例。</span><span class="sxs-lookup"><span data-stu-id="56764-131">Each input sample produces a single output sample.</span></span>

<span data-ttu-id="56764-132">否則，同步的 MFT 必須執行此訊息。</span><span class="sxs-lookup"><span data-stu-id="56764-132">Otherwise, a synchronous MFT must implement this message.</span></span>

## <a name="requirements"></a><span data-ttu-id="56764-133">規格需求</span><span class="sxs-lookup"><span data-stu-id="56764-133">Requirements</span></span>



| <span data-ttu-id="56764-134">需求</span><span class="sxs-lookup"><span data-stu-id="56764-134">Requirement</span></span> | <span data-ttu-id="56764-135">值</span><span class="sxs-lookup"><span data-stu-id="56764-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="56764-136">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56764-136">Minimum supported client</span></span><br/> | <span data-ttu-id="56764-137">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56764-137">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="56764-138">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56764-138">Minimum supported server</span></span><br/> | <span data-ttu-id="56764-139">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56764-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="56764-140">標頭</span><span class="sxs-lookup"><span data-stu-id="56764-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="56764-141"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="56764-141"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56764-142">另請參閱</span><span class="sxs-lookup"><span data-stu-id="56764-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56764-143">**MFT \_ 訊息 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="56764-143">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> <dt>

[<span data-ttu-id="56764-144">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="56764-144">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> </dl>

 

 




