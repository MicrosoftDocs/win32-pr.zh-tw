---
description: 系統會提供具有某些預設設定的 PGM 傳送者，這些設定會影響資料傳輸的效能，以及資料緩衝處理的時間長度，以考慮封包遺失以及相關聯的 PGM 用戶端重新傳輸要求。
ms.assetid: 56b15eac-ea0d-4d18-b5f6-2f1a7b1bb25f
title: PGM 寄件者選項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1c2e83ec7b098b9a82f74d4a3e0b6aa3ab03b63
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973266"
---
# <a name="pgm-sender-options"></a><span data-ttu-id="48d54-103">PGM 寄件者選項</span><span class="sxs-lookup"><span data-stu-id="48d54-103">PGM Sender Options</span></span>

<span data-ttu-id="48d54-104">系統會提供具有某些預設設定的 PGM 傳送者，這些設定會影響資料傳輸的效能，以及資料緩衝處理的時間長度，以考慮封包遺失以及相關聯的 PGM 用戶端重新傳輸要求。</span><span class="sxs-lookup"><span data-stu-id="48d54-104">PGM senders are provided with certain default settings that affect the performance of data transmission, and how long data is buffered to account for packet loss and associated PGM client retransmission requests.</span></span> <span data-ttu-id="48d54-105">下列段落描述這些預設設定。</span><span class="sxs-lookup"><span data-stu-id="48d54-105">The following paragraphs describe these default settings.</span></span>

## <a name="window-size-and-transmission-rate"></a><span data-ttu-id="48d54-106">視窗大小和傳輸速率</span><span class="sxs-lookup"><span data-stu-id="48d54-106">Window Size and Transmission Rate</span></span>

<span data-ttu-id="48d54-107">設定視窗大小和傳輸速率的功能，可讓應用程式控制傳輸緩衝區重新傳輸的資料量，以及傳輸位元組資料流程的速率。</span><span class="sxs-lookup"><span data-stu-id="48d54-107">The capability to set window size and transmission rate enables applications to control the amount of data the transport buffers for retransmission, and the rate at which the byte-stream is transmitted.</span></span>

<span data-ttu-id="48d54-108">重新傳輸資料會儲存在檔案中，因此最大視窗大小會受到傳輸可用磁碟空間的限制。</span><span class="sxs-lookup"><span data-stu-id="48d54-108">Retransmission data is stored in a file, therefore the maximum window size is limited by disk space usable by the transport.</span></span> <span data-ttu-id="48d54-109">預設視窗大小為10MB。</span><span class="sxs-lookup"><span data-stu-id="48d54-109">The default window size is 10MB.</span></span> <span data-ttu-id="48d54-110">雖然傳送或訊息大小可能會超過視窗或緩衝區大小，但資料串流仍不會中斷;傳送會暫止，直到所有資料都已送出為止。</span><span class="sxs-lookup"><span data-stu-id="48d54-110">Although it is possible for a send or message size to exceed the window or buffer size, the data stream remain uninterrupted; the send is pended until the all the data has been sent out.</span></span>

> [!Note]  
> <span data-ttu-id="48d54-111">緩衝區空間上限會受限於在任何指定時間（等於 2 ^ 31-1）可以保留在視窗中的封包數上限。</span><span class="sxs-lookup"><span data-stu-id="48d54-111">The maximum buffer space is limited by the maximum number of packets that can be held in the window at any given time, which is equal to 2^31 – 1.</span></span>

 

<span data-ttu-id="48d54-112">傳輸速率是原始資料封包的資料流程 (ODATA) 、重新傳輸的資料封包 (.RDATA) 和傳輸特定的簿記封包 (SPMs) （以碼錶示）。</span><span class="sxs-lookup"><span data-stu-id="48d54-112">The transmission rate is the combined outflow of original data packets (ODATA), retransmitted data packets (RDATA) and transport-specific bookkeeping packets (SPMs), expressed per second.</span></span> <span data-ttu-id="48d54-113">如果速率限制預設為每秒 56 kb。</span><span class="sxs-lookup"><span data-stu-id="48d54-113">If the rate limit is set to 56 kilobits per sec by default.</span></span> <span data-ttu-id="48d54-114">預設視窗大小為 10 mb，預設速率為每秒 56 kb。</span><span class="sxs-lookup"><span data-stu-id="48d54-114">The default window size is 10 megabytes, with a default rate of 56 kilobits per second.</span></span> <span data-ttu-id="48d54-115">由於 [**RM \_ 傳送 \_ 視窗**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) 結構的三個成員之間的關聯性，因此預設的視窗大小為1428秒。</span><span class="sxs-lookup"><span data-stu-id="48d54-115">Due to the relationship between the three members of the [**RM\_SEND\_WINDOW**](/windows/desktop/api/Wsrm/ns-wsrm-rm_send_window) structure, the default window size is therefore 1428 seconds.</span></span> <span data-ttu-id="48d54-116">如需詳細資訊，請參閱 **RM \_ 傳送 \_ 視窗** 。</span><span class="sxs-lookup"><span data-stu-id="48d54-116">See **RM\_SEND\_WINDOW** for more information.</span></span>

## <a name="window-advance-rate"></a><span data-ttu-id="48d54-117">視窗提前速率</span><span class="sxs-lookup"><span data-stu-id="48d54-117">Window Advance Rate</span></span>

<span data-ttu-id="48d54-118">視窗提前速率是由 RM 傳送者 [ \_ \_ 視窗 \_ 進階 \_ 率](socket-options.md) 通訊端選項設定。</span><span class="sxs-lookup"><span data-stu-id="48d54-118">The window advance rate is set by the [RM\_SENDER\_WINDOW\_ADV\_RATE](socket-options.md) socket option.</span></span> <span data-ttu-id="48d54-119">此選項可讓應用程式指定 PGM 傳送者視窗的遞增量（以非零百分比值的視窗大小表示）。</span><span class="sxs-lookup"><span data-stu-id="48d54-119">This option enables applications to specify the increment at which the PGM sender's window is advanced, expressed as a nonzero percentage value of the window size.</span></span> <span data-ttu-id="48d54-120">預設值為15%，最大速率為50%。</span><span class="sxs-lookup"><span data-stu-id="48d54-120">The default value is 15%, and the maximum rate is 50%.</span></span> <span data-ttu-id="48d54-121">如果 PGM 傳送者有擱置中的修復資料落在遞增視窗的空間中，則會在視窗中的每個修復封包送出時，將視窗部分設定為 advanced。</span><span class="sxs-lookup"><span data-stu-id="48d54-121">If the PGM sender has repair data pending that falls in the space of the increment window, the window is advanced partially as each repair packet in the window is sent out.</span></span>

## <a name="forward-error-correction-fec"></a><span data-ttu-id="48d54-122">轉寄錯誤更正 (FEC) </span><span class="sxs-lookup"><span data-stu-id="48d54-122">Forward Error Correction (FEC)</span></span>

<span data-ttu-id="48d54-123">轉寄錯誤更正是透過使用 RM \_ use \_ FEC socket 選項來設定。</span><span class="sxs-lookup"><span data-stu-id="48d54-123">Forward error correction is set through use of the RM\_USE\_FEC socket option.</span></span> <span data-ttu-id="48d54-124">此通訊端選項可讓 PGM 傳送者將修復封包當作同位封包傳送，而不是一般的資料封包。</span><span class="sxs-lookup"><span data-stu-id="48d54-124">This socket option enables the PGM sender to send repair packets as parity packets instead of regular data packets.</span></span> <span data-ttu-id="48d54-125">這樣做可將傳送的修復封包數目降至最低，以修復由相同資料群組內的多個接收者所遺失的不同序列。</span><span class="sxs-lookup"><span data-stu-id="48d54-125">Doing so minimizes the number of repair packets sent to repair different sequences lost by multiple receivers from within the same data group.</span></span> <span data-ttu-id="48d54-126">啟用 FEC 只會在 PGM 寄件者上設定。</span><span class="sxs-lookup"><span data-stu-id="48d54-126">Enabling FEC is only set on the PGM sender.</span></span> <span data-ttu-id="48d54-127">PGM 接收器會自動遵循寄件者所設定的原則。</span><span class="sxs-lookup"><span data-stu-id="48d54-127">PGM receivers automatically follow the policy set by the sender.</span></span> <span data-ttu-id="48d54-128">如需 FEC 的詳細討論，請參閱位於 [IETF](https://www.ietf.org/) 網站的 PGM RFC。</span><span class="sxs-lookup"><span data-stu-id="48d54-128">For a detailed discussion on FEC, refer to the PGM RFC located on the [IETF](https://www.ietf.org/) website.</span></span>

 

 



