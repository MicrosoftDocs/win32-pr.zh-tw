---
description: 要求媒體基礎轉換 (MFT) 以排清所有儲存的資料。
ms.assetid: c799a962-da79-46df-a37f-4016c8c1701e
title: 'MFT_MESSAGE_COMMAND_FLUSH (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd68f5e52cda9cca3470fb1dd903b5083a0cbc4a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691652"
---
# <a name="mft_message_command_flush"></a><span data-ttu-id="f3cf9-103">MFT \_ 訊息 \_ 命令排清 \_</span><span class="sxs-lookup"><span data-stu-id="f3cf9-103">MFT\_MESSAGE\_COMMAND\_FLUSH</span></span>

<span data-ttu-id="f3cf9-104">要求媒體基礎轉換 (MFT) 以排清所有儲存的資料。</span><span class="sxs-lookup"><span data-stu-id="f3cf9-104">Requests a Media Foundation transform (MFT) to flush all stored data.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="f3cf9-105">Message 參數</span><span class="sxs-lookup"><span data-stu-id="f3cf9-105">Message Parameter</span></span>

<span data-ttu-id="f3cf9-106">無。</span><span class="sxs-lookup"><span data-stu-id="f3cf9-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="f3cf9-107">備註</span><span class="sxs-lookup"><span data-stu-id="f3cf9-107">Remarks</span></span>

<span data-ttu-id="f3cf9-108">若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。</span><span class="sxs-lookup"><span data-stu-id="f3cf9-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="f3cf9-109">傳送此訊息之後，MFT 可以接受新的輸入範例。</span><span class="sxs-lookup"><span data-stu-id="f3cf9-109">After this message is sent, the MFT can accept new input samples.</span></span> <span data-ttu-id="f3cf9-110">目前的媒體類型不會失效。</span><span class="sxs-lookup"><span data-stu-id="f3cf9-110">The current media types are not invalidated.</span></span>

### <a name="implementation"></a><span data-ttu-id="f3cf9-111">實作</span><span class="sxs-lookup"><span data-stu-id="f3cf9-111">Implementation</span></span>

<span data-ttu-id="f3cf9-112">所有 MFTs 都必須執行這則訊息。</span><span class="sxs-lookup"><span data-stu-id="f3cf9-112">All MFTs must implement this message.</span></span> <span data-ttu-id="f3cf9-113">當它接收到此訊息時，MFT 應捨棄它所持有的任何媒體範例。</span><span class="sxs-lookup"><span data-stu-id="f3cf9-113">When it receives this message, the MFT should discard any media samples it is holding.</span></span>

<span data-ttu-id="f3cf9-114">[非同步 MFTs](asynchronous-mfts.md)：從用戶端接收到來自用戶端 [**\_ \_ \_ \_ 的 \_**](mft-message-notify-start-of-stream.md)訊息訊息通知時，mft 不會傳送另一個 [METransformNeedInput](metransformneedinput.md)事件。</span><span class="sxs-lookup"><span data-stu-id="f3cf9-114">[Asynchronous MFTs](asynchronous-mfts.md): The MFT does not send another [METransformNeedInput](metransformneedinput.md) event until it receives an [**MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM**](mft-message-notify-start-of-stream.md) message from the client.</span></span>

## <a name="requirements"></a><span data-ttu-id="f3cf9-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f3cf9-115">Requirements</span></span>



| <span data-ttu-id="f3cf9-116">需求</span><span class="sxs-lookup"><span data-stu-id="f3cf9-116">Requirement</span></span> | <span data-ttu-id="f3cf9-117">值</span><span class="sxs-lookup"><span data-stu-id="f3cf9-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3cf9-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f3cf9-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f3cf9-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3cf9-119">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f3cf9-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f3cf9-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f3cf9-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f3cf9-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f3cf9-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f3cf9-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f3cf9-123"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="f3cf9-123"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f3cf9-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f3cf9-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f3cf9-125">**MFT \_ 訊息 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="f3cf9-125">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




