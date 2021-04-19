---
description: 當通話處於已線上狀態之後，就可以將資訊傳送給它。
ms.assetid: a2afa7e9-c625-48ec-920b-0ae8c3e1b395
title: 產生 Inband 數位和音調
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8325087882f90ae175edfd27a9f75aab492969af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998447"
---
# <a name="generating-inband-digits-and-tones"></a><span data-ttu-id="cd494-103">產生 Inband 數位和音調</span><span class="sxs-lookup"><span data-stu-id="cd494-103">Generating Inband Digits and Tones</span></span>

<span data-ttu-id="cd494-104">當通話處於 *已連線* 狀態之後，就可以將資訊傳送給它。</span><span class="sxs-lookup"><span data-stu-id="cd494-104">After a call is in the *connected* state, information can be transmitted over it.</span></span> <span data-ttu-id="cd494-105">提供了兩個函式，可允許應用程式與遠端工作站設備（例如，回應機器）之間的端對端 inband 信號。</span><span class="sxs-lookup"><span data-stu-id="cd494-105">Two functions are provided that allow end-to-end inband signaling between the application and remote station equipment such as an answering machine.</span></span> <span data-ttu-id="cd494-106">其中一個函式是 [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits)，它會在呼叫上產生 inband 位數，並透過語音通道來發出信號。</span><span class="sxs-lookup"><span data-stu-id="cd494-106">One function is [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits), which generates inband digits on a call, signaling them over the voice channel.</span></span> <span data-ttu-id="cd494-107">數位可以是旋轉/脈衝序列或 DTMF 聲。</span><span class="sxs-lookup"><span data-stu-id="cd494-107">Digits can be signaled as either rotary/pulse sequences or as DTMF tones.</span></span> <span data-ttu-id="cd494-108">另一個函式是 [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone)，可讓應用程式透過媒體串流) 來產生各種 multifrequency 聲 inband (。</span><span class="sxs-lookup"><span data-stu-id="cd494-108">The other function is [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone), which enables the application to generate one of a variety of multifrequency tones inband (over the media stream).</span></span> <span data-ttu-id="cd494-109">這會產生電話語音聲，例如回電、嗶聲和忙碌，以及任意 multifrequency、multicadenced 音。</span><span class="sxs-lookup"><span data-stu-id="cd494-109">This generates telephony tones, such as ringback, beep, and busy, as well as arbitrary multifrequency, multicadenced tones.</span></span>

<span data-ttu-id="cd494-110">在一次呼叫時，一次只能進行一個數位或語氣產生。</span><span class="sxs-lookup"><span data-stu-id="cd494-110">Only one digit or tone generation can be in progress on a call at any one time.</span></span> <span data-ttu-id="cd494-111">當數位或語氣產生完成時，會將 [**行 \_ 產生**](line-generate.md) 訊息傳送至要求產生的應用程式。</span><span class="sxs-lookup"><span data-stu-id="cd494-111">When digit or tone generation completes, a [**LINE\_GENERATE**](line-generate.md) message is sent to the application that requested the generation.</span></span> <span data-ttu-id="cd494-112">在產生多個數位的情況下，只會在產生所有數位之後傳回單一訊息。</span><span class="sxs-lookup"><span data-stu-id="cd494-112">In the case where multiple digits are generated, only a single message is sent back after all digits have been generated.</span></span> <span data-ttu-id="cd494-113">在數位或語氣產生過程中呼叫 [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) 或 [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) ，將會中止目前進行中的產生作業，並將產生的行 \_ 產生訊息傳送至應用程式，而該應用程式的產生會以取消指示中止。</span><span class="sxs-lookup"><span data-stu-id="cd494-113">Calling [**lineGenerateDigits**](/windows/desktop/api/Tapi/nf-tapi-linegeneratedigits) or [**lineGenerateTone**](/windows/desktop/api/Tapi/nf-tapi-linegeneratetone) while digit or tone generation is in progress will abort the generation currently in progress and send the LINE\_GENERATE message to the application whose generation was aborted with a cancel indication.</span></span>

 

 



