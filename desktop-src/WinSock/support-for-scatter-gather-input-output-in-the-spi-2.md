---
description: WSPSend、WSPSendTo、WSPRecv 和 WSPRecvFrom 常式全都採用用戶端緩衝區的陣列作為輸入參數，因此可用於散佈/收集 (或向量) i/o。
ms.assetid: ecd3d2f1-74b1-42f7-8402-3170112e3aca
title: 支援在 SPI 中散佈/收集輸入/輸出
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c3f32e016c5c2e9f990c334716d4177d477c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106975033"
---
# <a name="support-for-scattergather-inputoutput-in-the-spi"></a><span data-ttu-id="65344-103">支援在 SPI 中散佈/收集輸入/輸出</span><span class="sxs-lookup"><span data-stu-id="65344-103">Support for Scatter/Gather Input/Output in the SPI</span></span>

<span data-ttu-id="65344-104">[**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85))、 [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85))、 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85))和 [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85))常式全都採用用戶端緩衝區的陣列作為輸入參數，因此可用於散佈/收集 (或向量) i/o。</span><span class="sxs-lookup"><span data-stu-id="65344-104">The [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)), [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)), [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)), and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) routines all take an array of client buffers as input parameters and thus may be used for scatter/gather (or vectored) I/O.</span></span> <span data-ttu-id="65344-105">這在傳送的每個訊息的部分包含一或多個固定長度標頭元件（除了訊息內文）的情況下非常有用。</span><span class="sxs-lookup"><span data-stu-id="65344-105">This can be very useful in instances where portions of each message being transmitted consist of one or more fixed length header components in addition to a message body.</span></span> <span data-ttu-id="65344-106">在傳送之前，這類標頭元件不需要串連成單一連續緩衝區。</span><span class="sxs-lookup"><span data-stu-id="65344-106">Such header components need not be concatenated into a single contiguous buffer prior to sending.</span></span> <span data-ttu-id="65344-107">同樣地，在接收時，標頭元件可以自動分割成不同的緩衝區，讓訊息內文保持純訊息主體。</span><span class="sxs-lookup"><span data-stu-id="65344-107">Likewise on receiving, the header components can be automatically split off into separate buffers, leaving the message body pure.</span></span>

<span data-ttu-id="65344-108">使用緩衝區清單而不是單一緩衝區，並不會變更適用于接收作業的界限。</span><span class="sxs-lookup"><span data-stu-id="65344-108">Utilizing lists of buffers instead of a single buffer does not change the boundaries that apply to receive operations.</span></span> <span data-ttu-id="65344-109">針對訊息導向的通訊協定，每次收到單一訊息時都會完成接收作業，不論所使用的是多少個或幾個提供的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="65344-109">For message-oriented protocols, a receive operation completes whenever a single message has been received, regardless of how many or few of the supplied buffers were used.</span></span> <span data-ttu-id="65344-110">同樣地，對於資料流程導向的通訊協定，當未指定的位元組數量抵達網路時，接收就會完成，而不一定會在所有提供的緩衝區已滿時完成。</span><span class="sxs-lookup"><span data-stu-id="65344-110">Likewise for stream-oriented protocols, a receive completes when an unspecified quantity of bytes arrives over the network, not necessarily when all of the supplied buffers are full.</span></span>

 

 
