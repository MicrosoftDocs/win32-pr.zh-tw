---
description: 通知媒體基礎轉換 (MFT) 第一個範例即將處理。
ms.assetid: 579df695-02c4-4332-b1b4-c7bd9da50c0f
title: 'MFT_MESSAGE_NOTIFY_START_OF_STREAM (Mftransform) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe0edefdecdf75afbe14c851f33e9726400e490d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026397"
---
# <a name="mft_message_notify_start_of_stream"></a><span data-ttu-id="c0109-103">MFT \_ 訊息 \_ 通知 \_ 開始 \_ \_ 資料流程</span><span class="sxs-lookup"><span data-stu-id="c0109-103">MFT\_MESSAGE\_NOTIFY\_START\_OF\_STREAM</span></span>

<span data-ttu-id="c0109-104">通知媒體基礎轉換 (MFT) 第一個範例即將處理。</span><span class="sxs-lookup"><span data-stu-id="c0109-104">Notifies a Media Foundation transform (MFT) that the first sample is about to be processed.</span></span>

## <a name="message-parameter"></a><span data-ttu-id="c0109-105">Message 參數</span><span class="sxs-lookup"><span data-stu-id="c0109-105">Message Parameter</span></span>

<span data-ttu-id="c0109-106">無。</span><span class="sxs-lookup"><span data-stu-id="c0109-106">None.</span></span>

## <a name="remarks"></a><span data-ttu-id="c0109-107">備註</span><span class="sxs-lookup"><span data-stu-id="c0109-107">Remarks</span></span>

<span data-ttu-id="c0109-108">若要傳送此訊息，請呼叫 [**IMFTransform：:P rocessmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)。</span><span class="sxs-lookup"><span data-stu-id="c0109-108">To send this message, call [**IMFTransform::ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage).</span></span>

<span data-ttu-id="c0109-109">針對同步 MFTs，您可以選擇是否要傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c0109-109">For synchronous MFTs, it is optional to send this message.</span></span>

<span data-ttu-id="c0109-110">針對非同步 MFTs，用戶端必須傳送此訊息。</span><span class="sxs-lookup"><span data-stu-id="c0109-110">For asynchronous MFTs, the client must send this message.</span></span>

### <a name="implementation"></a><span data-ttu-id="c0109-111">實作</span><span class="sxs-lookup"><span data-stu-id="c0109-111">Implementation</span></span>

<span data-ttu-id="c0109-112">不需要同步的 MFT 來回應訊息。</span><span class="sxs-lookup"><span data-stu-id="c0109-112">A synchronous MFT is not required to respond to the message.</span></span>

<span data-ttu-id="c0109-113">非同步 MFT 必須依照 [非同步 MFTs](asynchronous-mfts.md)中的說明，執行這則訊息。</span><span class="sxs-lookup"><span data-stu-id="c0109-113">An asynchronous MFT must implement this message, as described in [Asynchronous MFTs](asynchronous-mfts.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c0109-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="c0109-114">Requirements</span></span>



| <span data-ttu-id="c0109-115">需求</span><span class="sxs-lookup"><span data-stu-id="c0109-115">Requirement</span></span> | <span data-ttu-id="c0109-116">值</span><span class="sxs-lookup"><span data-stu-id="c0109-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0109-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c0109-117">Minimum supported client</span></span><br/> | <span data-ttu-id="c0109-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0109-118">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c0109-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c0109-119">Minimum supported server</span></span><br/> | <span data-ttu-id="c0109-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c0109-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c0109-121">標頭</span><span class="sxs-lookup"><span data-stu-id="c0109-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="c0109-122"><dt>Mftransform。h</dt></span><span class="sxs-lookup"><span data-stu-id="c0109-122"><dt>Mftransform.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c0109-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c0109-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c0109-124">**MFT \_ 訊息 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="c0109-124">**MFT\_MESSAGE\_TYPE**</span></span>](/windows/desktop/api/mftransform/ne-mftransform-mft_message_type)
</dt> </dl>

 

 




