---
description: CMSPThread 類別會實 Msp 背景工作執行緒。
ms.assetid: 9dc2373a-cdcf-4e60-95fa-56cb68bda15b
title: CMSPThread
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 17a12b71668e81688b5de7f41e188a51b88944d6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106984703"
---
# <a name="cmspthread"></a><span data-ttu-id="634b8-103">CMSPThread</span><span class="sxs-lookup"><span data-stu-id="634b8-103">CMSPThread</span></span>

<span data-ttu-id="634b8-104">**CMSPThread** 類別會執行 MSP 的背景工作執行緒。</span><span class="sxs-lookup"><span data-stu-id="634b8-104">The **CMSPThread** class implements the MSP's worker thread.</span></span> <span data-ttu-id="634b8-105">基類使用此背景工作執行緒有許多用途。</span><span class="sxs-lookup"><span data-stu-id="634b8-105">The base classes use this worker thread for a number of purposes.</span></span> <span data-ttu-id="634b8-106">系統會提供一般和輕量的工作專案機制，讓衍生的 MSP 可將此執行緒用於其本身的同步或非同步工作專案，不論它們可能是什麼。</span><span class="sxs-lookup"><span data-stu-id="634b8-106">A generic and lightweight work item mechanism is provided to allow the derived MSP to use this thread for its own synchronous or asynchronous work items, whatever they may be.</span></span> <span data-ttu-id="634b8-107">此執行緒也會提取訊息，並支援處理 Apc (雖然基類) 不會使用 Apc。</span><span class="sxs-lookup"><span data-stu-id="634b8-107">The thread also pumps messages and supports handling of APCs (although APCs are not used in the base classes).</span></span>

<span data-ttu-id="634b8-108">當有多個類似的位址存在時 (也就是，當相同 DLL 的相同 MSP 實) 具現化時，執行緒類別會自動針對所有位址使用單一執行緒，以確保可調整性。</span><span class="sxs-lookup"><span data-stu-id="634b8-108">When multiple like addresses are present (that is, when the same MSP implementation from the same DLL is instantiated multiple times), the thread class ensures scalability by automatically using a single thread for all the addresses.</span></span> <span data-ttu-id="634b8-109">執行緒類別的介面，就是 MSP 實可以將 thread 類別視為私用執行緒，而不需要在意可能共用的其他位址。</span><span class="sxs-lookup"><span data-stu-id="634b8-109">The interface to the thread class is such that the MSP implementation can think of the thread class as a private thread and need not care about the other addresses that may be sharing it.</span></span>

<span data-ttu-id="634b8-110">定義于 MSPthrd 中。</span><span class="sxs-lookup"><span data-stu-id="634b8-110">Defined in MSPthrd.h.</span></span>

 

 



