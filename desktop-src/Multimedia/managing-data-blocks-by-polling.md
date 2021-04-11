---
title: 藉由輪詢管理資料區塊
description: 藉由輪詢管理資料區塊
ms.assetid: 0a517f1d-4993-49b8-be86-bc63e5687cba
keywords:
- 波形音訊，輪詢資料區塊
- 音訊資料區塊，輪詢
- 輪詢音訊資料區塊
- WAVEHDR 結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7e5580ff64425eae1bc6650268b065e60b90f43
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104023337"
---
# <a name="managing-data-blocks-by-polling"></a><span data-ttu-id="90a4d-107">藉由輪詢管理資料區塊</span><span class="sxs-lookup"><span data-stu-id="90a4d-107">Managing Data Blocks by Polling</span></span>

<span data-ttu-id="90a4d-108">除了使用回呼函式，您還可以輪詢 [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr)結構的 **dwFlags** 成員，以判斷音訊裝置何時完成資料區塊。</span><span class="sxs-lookup"><span data-stu-id="90a4d-108">In addition to using a callback function, you can poll the **dwFlags** member of a [**WAVEHDR**](/windows/win32/api/mmeapi/ns-mmeapi-wavehdr) structure to determine when an audio device is finished with a data block.</span></span> <span data-ttu-id="90a4d-109">有時候最好是輪詢 **dwFlags** ，而不是等待其他機制從驅動程式接收訊息。</span><span class="sxs-lookup"><span data-stu-id="90a4d-109">Sometimes it is better to poll **dwFlags** than to wait for another mechanism to receive messages from the drivers.</span></span> <span data-ttu-id="90a4d-110">例如，在您呼叫 [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) 函式釋放暫止的資料區塊之後，您可以立即進行輪詢，以確定在呼叫 [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) 並釋出資料區塊的記憶體之前，已釋放資料區塊。</span><span class="sxs-lookup"><span data-stu-id="90a4d-110">For example, after you call the [**waveOutReset**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutreset) function to release pending data blocks, you can immediately poll to be sure that the data blocks have been released before calling [**waveOutUnprepareHeader**](/windows/win32/api/mmeapi/nf-mmeapi-waveoutunprepareheader) and freeing the memory for the data block.</span></span>

<span data-ttu-id="90a4d-111">您可以使用 [WHDR \_ 完成] 旗標來測試 **dwFlags** 成員。</span><span class="sxs-lookup"><span data-stu-id="90a4d-111">You can use the WHDR\_DONE flag to test the **dwFlags** member.</span></span> <span data-ttu-id="90a4d-112">一旦在 \_ **WAVEHDR** 結構的 **DWFLAGS** 成員中設定 WHDR 完成旗標，驅動程式就會使用資料區塊完成。</span><span class="sxs-lookup"><span data-stu-id="90a4d-112">As soon as the WHDR\_DONE flag is set in the **dwFlags** member of the **WAVEHDR** structure, the driver is finished with the data block.</span></span>

 

 