---
description: 連接到特定的智慧卡並與其通訊。
ms.assetid: 37d92491-174b-471e-b36e-46d9285dd404
title: 智慧卡與讀者存取功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d7202b2d6165b49bfe80e55f15c4d69cb4a6909a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980596"
---
# <a name="smart-card-and-reader-access-functions"></a><span data-ttu-id="c7f03-103">智慧卡與讀者存取功能</span><span class="sxs-lookup"><span data-stu-id="c7f03-103">Smart Card and Reader Access Functions</span></span>

<span data-ttu-id="c7f03-104">下列函式會連接到特定的 [*智慧卡*](../secgloss/s-gly.md)，並與之通訊。</span><span class="sxs-lookup"><span data-stu-id="c7f03-104">The following functions connect to and communicate with a specific [*smart card*](../secgloss/s-gly.md).</span></span> <span data-ttu-id="c7f03-105">卡片的 i/o 作業會使用緩衝區來傳送或接收資料，並使用包含通訊協定控制資訊的結構。</span><span class="sxs-lookup"><span data-stu-id="c7f03-105">I/O operations to the card use a buffer for sending or receiving data and a structure that contains protocol control information.</span></span> <span data-ttu-id="c7f03-106">通訊協定控制資訊結構的開頭一律為 [**捨棄 \_ IO \_ 要求**](scard-io-request.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="c7f03-106">The protocol control information structure always begins with an [**SCARD\_IO\_REQUEST**](scard-io-request.md) structure.</span></span>



| <span data-ttu-id="c7f03-107">主題</span><span class="sxs-lookup"><span data-stu-id="c7f03-107">Topic</span></span>                                                  | <span data-ttu-id="c7f03-108">描述</span><span class="sxs-lookup"><span data-stu-id="c7f03-108">Description</span></span>                                                                                                                                                                                                                                |
|--------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c7f03-109">**SCardConnect**</span><span class="sxs-lookup"><span data-stu-id="c7f03-109">**SCardConnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardconnecta)                   | <span data-ttu-id="c7f03-110">連接到卡片。</span><span class="sxs-lookup"><span data-stu-id="c7f03-110">Connect to a card.</span></span>                                                                                                                                                                                                                         |
| [<span data-ttu-id="c7f03-111">**SCardReconnect**</span><span class="sxs-lookup"><span data-stu-id="c7f03-111">**SCardReconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardreconnect)               | <span data-ttu-id="c7f03-112">重新建立連接。</span><span class="sxs-lookup"><span data-stu-id="c7f03-112">Reestablish a connection.</span></span>                                                                                                                                                                                                                  |
| [<span data-ttu-id="c7f03-113">**SCardDisconnect**</span><span class="sxs-lookup"><span data-stu-id="c7f03-113">**SCardDisconnect**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scarddisconnect)             | <span data-ttu-id="c7f03-114">終止連接。</span><span class="sxs-lookup"><span data-stu-id="c7f03-114">Terminate a connection.</span></span>                                                                                                                                                                                                                    |
| [<span data-ttu-id="c7f03-115">**SCardBeginTransaction**</span><span class="sxs-lookup"><span data-stu-id="c7f03-115">**SCardBeginTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardbegintransaction) | <span data-ttu-id="c7f03-116">啟動 [*交易*](../secgloss/t-gly.md)，封鎖其他應用程式存取卡片。</span><span class="sxs-lookup"><span data-stu-id="c7f03-116">Start a [*transaction*](../secgloss/t-gly.md), blocking other applications from accessing a card.</span></span>                                                                                            |
| [<span data-ttu-id="c7f03-117">**SCardEndTransaction**</span><span class="sxs-lookup"><span data-stu-id="c7f03-117">**SCardEndTransaction**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardendtransaction)     | <span data-ttu-id="c7f03-118">結束交易，讓其他應用程式存取卡片。</span><span class="sxs-lookup"><span data-stu-id="c7f03-118">End a transaction, allowing other applications to access a card.</span></span>                                                                                                                                                                           |
| [<span data-ttu-id="c7f03-119">**SCardStatus**</span><span class="sxs-lookup"><span data-stu-id="c7f03-119">**SCardStatus**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardstatusa)                     | <span data-ttu-id="c7f03-120">提供讀取器的目前狀態。</span><span class="sxs-lookup"><span data-stu-id="c7f03-120">Provide the current status of the reader.</span></span>                                                                                                                                                                                                  |
| [<span data-ttu-id="c7f03-121">**SCardTransmit**</span><span class="sxs-lookup"><span data-stu-id="c7f03-121">**SCardTransmit**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardtransmit)                 | <span data-ttu-id="c7f03-122">使用 [*t = 0*](../secgloss/t-gly.md)、 [*T = 1*](../secgloss/t-gly.md)和未經處理的通訊協定，要求服務並從卡片收到資料。</span><span class="sxs-lookup"><span data-stu-id="c7f03-122">Requests service and receives data back from a card using [*T=0*](../secgloss/t-gly.md), [*T=1*](../secgloss/t-gly.md), and raw protocols.</span></span> |



 

 

 
