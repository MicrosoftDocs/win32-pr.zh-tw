---
description: 網路提供者 API 會指定單一功能功能。
ms.assetid: fc74a043-da13-485f-9f54-a43064add927
title: 功能功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83cde32ba0d3116ce83e7ca6621666f5e9a86650
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026502"
---
# <a name="capabilities-functions"></a><span data-ttu-id="35e50-103">功能功能</span><span class="sxs-lookup"><span data-stu-id="35e50-103">Capabilities Functions</span></span>

<span data-ttu-id="35e50-104">網路提供者 API 會指定單一功能功能。</span><span class="sxs-lookup"><span data-stu-id="35e50-104">The Network Provider API specifies a single capabilities function.</span></span> <span data-ttu-id="35e50-105">當作業系統要求有關網路提供者功能的資訊時， [*多個提供者路由器*](/windows/desktop/SecGloss/m-gly) (MPR) 會呼叫網路的每個網路提供者的 [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) 功能。</span><span class="sxs-lookup"><span data-stu-id="35e50-105">When the operating system requests information about a network provider's capabilities, the [*Multiple Provider Router*](/windows/desktop/SecGloss/m-gly) (MPR) calls the [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function of each network provider whose network is active.</span></span>

<span data-ttu-id="35e50-106">[**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps)函式會傳回一個位元遮罩，指出網路提供者所支援之網路提供者 API 的功能。</span><span class="sxs-lookup"><span data-stu-id="35e50-106">The [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) function returns a bitmask indicating which functions of the Network Provider API the network provider supports.</span></span> <span data-ttu-id="35e50-107">**NPGetCaps** 函式是網路提供者必須實行的唯一功能。</span><span class="sxs-lookup"><span data-stu-id="35e50-107">The **NPGetCaps** function is the only function that a network provider must implement.</span></span> <span data-ttu-id="35e50-108">作業系統會呼叫此函式，以判斷提供者支援的網路提供者 API 其他哪些功能。</span><span class="sxs-lookup"><span data-stu-id="35e50-108">The operating system calls this function to determine which other functions of the Network Provider API the provider supports.</span></span>

 

 
