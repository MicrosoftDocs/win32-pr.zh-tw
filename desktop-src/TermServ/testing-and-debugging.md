---
title: 測試和偵錯
description: 有 \ 0034; echo \ 0034;由遠端桌面連線 (RDC) 用戶端所執行的接聽程式，一律存在並接聽連入連線。
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965564"
---
# <a name="testing-and-debugging"></a><span data-ttu-id="3e6c3-103">測試和偵錯</span><span class="sxs-lookup"><span data-stu-id="3e6c3-103">Testing and Debugging</span></span>

<span data-ttu-id="3e6c3-104">有一個由遠端桌面連線 (RDC) 用戶端所執行的「echo」接聽程式，其一律存在並接聽連入連線。</span><span class="sxs-lookup"><span data-stu-id="3e6c3-104">There is an "echo" listener that is implemented by the Remote Desktop Connection (RDC) client, which is always present and listening for incoming connections.</span></span> <span data-ttu-id="3e6c3-105">當您撰寫動態虛擬通道的伺服器端 (DVC) 模組時，若要快速測試，您可以開啟名為 "ECHO" 的端點。</span><span class="sxs-lookup"><span data-stu-id="3e6c3-105">When you are writing the server side of a dynamic virtual channel (DVC) module, as a quick test you can open an endpoint named "ECHO".</span></span> <span data-ttu-id="3e6c3-106">從這個端點具現化之通道的任何寫入，都會導致收到相同的資料。</span><span class="sxs-lookup"><span data-stu-id="3e6c3-106">Any write to a channel that is instantiated from this endpoint will result in the receipt of the same data.</span></span>

<span data-ttu-id="3e6c3-107">您可以使用這項技術來測試伺服器端模組的輸入/輸出 (i/o) 執行、測量遠端桌面連線 (RDC) 用戶端外掛程式的回應時間，或測量遠端桌面連線 (RDC) 用戶端的網路延遲。</span><span class="sxs-lookup"><span data-stu-id="3e6c3-107">You can use this technique to test an input/output (I/O) implementation of the server-side module, to measure the response time for a Remote Desktop Connection (RDC) client plug-in, or to measure the network delay for the Remote Desktop Connection (RDC) client.</span></span> <span data-ttu-id="3e6c3-108">可透過此通道傳送的資料量沒有任何限制。</span><span class="sxs-lookup"><span data-stu-id="3e6c3-108">There is no limitation on the amount of data that can be sent over this channel.</span></span>

 

 




