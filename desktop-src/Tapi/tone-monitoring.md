---
description: 色調監視會監視指定色調的媒體串流。
ms.assetid: c3218013-b71f-41cd-9397-ba717c0cf556
title: 語氣監視
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9a3275e5207999896792ee04dc1842b01f4ad0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104026860"
---
# <a name="tone-monitoring"></a><span data-ttu-id="e54f2-103">語氣監視</span><span class="sxs-lookup"><span data-stu-id="e54f2-103">Tone Monitoring</span></span>

<span data-ttu-id="e54f2-104">色調監視會監視指定色調的媒體串流。</span><span class="sxs-lookup"><span data-stu-id="e54f2-104">Tone monitoring monitors the media stream of a call for specified tones.</span></span> <span data-ttu-id="e54f2-105">色調是依元件的頻率和步調來描述。</span><span class="sxs-lookup"><span data-stu-id="e54f2-105">A tone is described by its component frequencies and cadence.</span></span> <span data-ttu-id="e54f2-106">API 的執行可能會允許同時監視數個不同的色調。</span><span class="sxs-lookup"><span data-stu-id="e54f2-106">An implementation of the API may allow several different tones to be monitored simultaneously.</span></span> <span data-ttu-id="e54f2-107">應用程式可以標記每個色調，以便區分它要求偵測的不同聲音。</span><span class="sxs-lookup"><span data-stu-id="e54f2-107">An application can tag each tone to be able to distinguish the different tones for which it requests detection.</span></span>

<span data-ttu-id="e54f2-108">應用程式可以使用 [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones)在指定的呼叫上啟用或停用語氣監視。</span><span class="sxs-lookup"><span data-stu-id="e54f2-108">An application can enable or disable tone monitoring on a specified call with [**lineMonitorTones**](/windows/desktop/api/Tapi/nf-tapi-linemonitortones).</span></span> <span data-ttu-id="e54f2-109">使用這個函式時，應用程式會指出要在指定的呼叫上偵測哪些色調。</span><span class="sxs-lookup"><span data-stu-id="e54f2-109">With this function, the application indicates which tones to detect on a specified call.</span></span> <span data-ttu-id="e54f2-110">啟用音調監視時，偵測到的數位會導致應用程式收到 [**行 \_ MONITORTONE**](line-monitortone.md) 訊息的通知。</span><span class="sxs-lookup"><span data-stu-id="e54f2-110">When tone monitoring is enabled, detected digits cause the application to be notified with the [**LINE\_MONITORTONE**](line-monitortone.md) message.</span></span> <span data-ttu-id="e54f2-111">此訊息提供偵測到其色調的呼叫控制碼，以及應用程式的音調標記。</span><span class="sxs-lookup"><span data-stu-id="e54f2-111">This message provides the call handle on which the tone was detected as well as the application's tag for the tone.</span></span>

<span data-ttu-id="e54f2-112">語氣監視的範圍是由呼叫的存留期所限制。</span><span class="sxs-lookup"><span data-stu-id="e54f2-112">The scope of tone monitoring is bound by the lifetime of the call.</span></span> <span data-ttu-id="e54f2-113">當通話 *中斷* 連線或 *閒置* 時，呼叫上的色調監視就會結束。</span><span class="sxs-lookup"><span data-stu-id="e54f2-113">Tone monitoring on a call ends as soon the call *disconnects* or goes *idle*.</span></span>

> [!Note]  
> <span data-ttu-id="e54f2-114">聲音、數位或媒體類型的監視通常需要使用服務提供者只能有有限數量的資源。</span><span class="sxs-lookup"><span data-stu-id="e54f2-114">The monitoring of tones, digits, or media types often requires the use of resources of which the service provider can only have a finite amount.</span></span> <span data-ttu-id="e54f2-115">如果無法使用資源，則可能會拒絕監視要求。</span><span class="sxs-lookup"><span data-stu-id="e54f2-115">A request for monitoring can be rejected if resources are not available.</span></span> <span data-ttu-id="e54f2-116">基於相同的理由，應用程式應該停用任何不必要的監視。</span><span class="sxs-lookup"><span data-stu-id="e54f2-116">For the same reason, an application should disable any unnecessary monitoring.</span></span>

 

 

 



