---
description: 本節說明 Windows 中的實際一般多播 (PGM) 多播通訊協定（通常稱為可靠多播）。 可靠多播是透過 Windows Server 2003 和更新版本中的 Windows 通訊端來執行。
ms.assetid: 81c203ed-739f-4a06-99a1-9a99c6164edc
title: '可靠的多播程式設計 (PGM) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce57fcce7bf2faf471604bed97d345971801ca1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982360"
---
# <a name="reliable-multicast-programming-pgm"></a><span data-ttu-id="a8dce-104">可靠的多播程式設計 (PGM) </span><span class="sxs-lookup"><span data-stu-id="a8dce-104">Reliable Multicast Programming (PGM)</span></span>

<span data-ttu-id="a8dce-105">本節說明 Windows 中的實際一般多播 (PGM) 多播通訊協定（通常稱為可靠多播）。</span><span class="sxs-lookup"><span data-stu-id="a8dce-105">This section describes the Pragmatic General Multicast (PGM) multicast protocol implementation in Windows, often referred to as reliable multicast.</span></span> <span data-ttu-id="a8dce-106">可靠多播是透過 Windows Server 2003 和更新版本中的 Windows 通訊端來執行。</span><span class="sxs-lookup"><span data-stu-id="a8dce-106">Reliable multicast is implemented through Windows Sockets in Windows Server 2003 and later.</span></span>

<span data-ttu-id="a8dce-107">**WINDOWS XP：** 只有在安裝 Microsoft Message Queuing (MSMQ) 3.0 時，才支援 PGM。</span><span class="sxs-lookup"><span data-stu-id="a8dce-107">**Windows XP:** PGM is only supported when Microsoft Message Queuing (MSMQ) 3.0 is installed.</span></span>

<span data-ttu-id="a8dce-108">PGM 是可靠且可擴充的多播通訊協定，可讓接收者偵測遺失、要求重新傳輸遺失的資料，或通知應用程式無法復原的遺失。</span><span class="sxs-lookup"><span data-stu-id="a8dce-108">PGM is a reliable and scalable multicast protocol that enables receivers to detect loss, request retransmission of lost data, or notify an application of unrecoverable loss.</span></span> <span data-ttu-id="a8dce-109">PGM 是接收者可靠的通訊協定，這表示接收者負責確保收到所有資料，absolving 接收責任的寄件者。</span><span class="sxs-lookup"><span data-stu-id="a8dce-109">PGM is a receiver-reliable protocol, which means the receiver is responsible for ensuring all data is received, absolving the sender of reception responsibility.</span></span>

<span data-ttu-id="a8dce-110">PGM 適用于需要從多個來源將無重複的多播資料傳遞給多個接收者的應用程式。</span><span class="sxs-lookup"><span data-stu-id="a8dce-110">PGM is appropriate for applications that require duplicate-free multicast data delivery from multiple sources to multiple receivers.</span></span> <span data-ttu-id="a8dce-111">PGM 不支援認可的傳遞，也無法保證來自多個寄件者的封包順序。</span><span class="sxs-lookup"><span data-stu-id="a8dce-111">PGM does not support acknowledged delivery, nor does it guarantee ordering of packets from multiple senders.</span></span>

<span data-ttu-id="a8dce-112">如需有關 PGM 的詳細資訊，請參閱 [www.ietf.org](https://www.ietf.org/)提供的 RFC 3208。</span><span class="sxs-lookup"><span data-stu-id="a8dce-112">For more information about PGM, refer to RFC 3208 available at [www.ietf.org](https://www.ietf.org/).</span></span>

<span data-ttu-id="a8dce-113">本節說明如何在 Windows 上使用可靠的多播。</span><span class="sxs-lookup"><span data-stu-id="a8dce-113">This section describes how to use reliable multicast on Windows.</span></span> <span data-ttu-id="a8dce-114">下列主題說明使用 Windows 通訊端建立可靠多播應用程式的各個層面：</span><span class="sxs-lookup"><span data-stu-id="a8dce-114">The following topics explain the various aspects of creating a reliable multicast application using Windows Sockets:</span></span>

-   [<span data-ttu-id="a8dce-115">PGM 寄件者和接收者</span><span class="sxs-lookup"><span data-stu-id="a8dce-115">PGM Senders and Receivers</span></span>](pgm-senders-and-receivers.md)
-   [<span data-ttu-id="a8dce-116">PGM 寄件者選項</span><span class="sxs-lookup"><span data-stu-id="a8dce-116">PGM Sender Options</span></span>](pgm-sender-options.md)
-   [<span data-ttu-id="a8dce-117">傳送和接收 PGM 資料</span><span class="sxs-lookup"><span data-stu-id="a8dce-117">Sending and Receiving PGM Data</span></span>](sending-and-receiving-pgm-data.md)
-   [<span data-ttu-id="a8dce-118">多宿主和 PGM</span><span class="sxs-lookup"><span data-stu-id="a8dce-118">Multihoming and PGM</span></span>](multihoming-and-pgm.md)
-   [<span data-ttu-id="a8dce-119">PGM 通訊端選項</span><span class="sxs-lookup"><span data-stu-id="a8dce-119">PGM Socket Options</span></span>](pgm-socket-options.md)

 

 



