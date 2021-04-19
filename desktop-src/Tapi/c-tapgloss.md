---
description: 下列詞彙有助於瞭解 TAPI 技術。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 23331332-38bc-41b9-84c4-281722ddf563
title: 'C (電話語音 API) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c6fade540235ef6c68b42a0aba364038d674e12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001359"
---
# <a name="c-telephony-api"></a><span data-ttu-id="0478c-103">C (電話語音 API) </span><span class="sxs-lookup"><span data-stu-id="0478c-103">C (Telephony API)</span></span>

<span data-ttu-id="0478c-104">[](a-tapgloss.md) [B](b-tapgloss.md) C [](u-tapgloss.md) [](v-tapgloss.md) [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [W](w-tapgloss.md) X Y Z</span><span class="sxs-lookup"><span data-stu-id="0478c-104">[A](a-tapgloss.md) [B](b-tapgloss.md) C [D](d-tapgloss.md) [E](e-tapgloss.md) F G [H](h-tapgloss.md) [I](i-tapgloss.md) J [K](k-tapgloss.md) [L](l-tapgloss.md) [M](m-tapgloss.md) N O [P](p-tapgloss.md) Q [R](r-tapgloss.md) [S](s-tapgloss.md) [T](t-tapgloss.md) [U](u-tapgloss.md) [V](v-tapgloss.md) [W](w-tapgloss.md) X Y Z</span></span>

<dl> <dt>

<span data-ttu-id="0478c-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**呼叫分類**</span><span class="sxs-lookup"><span data-stu-id="0478c-105"><span id="tapi2.call_classification_tapgloss"></span><span id="TAPI2.CALL_CLASSIFICATION_TAPGLOSS"></span>**call classification**</span></span>
</dt> <dd>

<span data-ttu-id="0478c-106">此 TAPI 程式會報告媒體資料流程類型的變更， (語音、傳真、資料數據機等等) 參與的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0478c-106">TAPI process that reports changes in the type of media stream (voice, fax, data modem, and so on) to participating applications.</span></span>

</dd> <dt>

<span data-ttu-id="0478c-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**通話進度監視**</span><span class="sxs-lookup"><span data-stu-id="0478c-107"><span id="tapi2.call_progress_monitoring_tapgloss"></span><span id="TAPI2.CALL_PROGRESS_MONITORING_TAPGLOSS"></span>**call progress monitoring**</span></span>
</dt> <dd>

<span data-ttu-id="0478c-108">接聽聲音音的程式，例如撥號音、特殊資訊語氣、忙碌信號，以及回電音，以判斷呼叫的狀態 (透過網路) 的進度。</span><span class="sxs-lookup"><span data-stu-id="0478c-108">The process of listening for audible tones such as a dial tone, special information tones, busy signals, and ringback tones to determine the state of a call (its progress through the network).</span></span>

</dd> <dt>

<span data-ttu-id="0478c-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**呼叫重新導向**</span><span class="sxs-lookup"><span data-stu-id="0478c-109"><span id="tapi2.call_redirection_tapgloss"></span><span id="TAPI2.CALL_REDIRECTION_TAPGLOSS"></span>**call redirection**</span></span>
</dt> <dd>

<span data-ttu-id="0478c-110">允許應用程式在沒有先接聽來電的情況下，將供應專案來電轉接至另一個位址的函式。</span><span class="sxs-lookup"><span data-stu-id="0478c-110">A function that allows an application to deflect an offering call to another address without first answering the call.</span></span> <span data-ttu-id="0478c-111">呼叫重新導向與呼叫轉送不同，因為交換器不需要應用程式就能執行呼叫轉送;重新導向可依應用程式逐一呼叫來完成，例如，由呼叫者識別碼資訊所驅動。</span><span class="sxs-lookup"><span data-stu-id="0478c-111">Call redirection differs from call forwarding in that call forwarding is performed by the switch without the involvement of the application; redirection can be done on a call-by-call basis by the application, for example, driven by caller ID information.</span></span> <span data-ttu-id="0478c-112">這與傳送呼叫的來電轉接不同，需要先回答呼叫。</span><span class="sxs-lookup"><span data-stu-id="0478c-112">It differs from call transfer in that transferring a call requires that the call first be answered.</span></span> <span data-ttu-id="0478c-113">請參閱呼叫 *識別碼*、 *呼叫者識別碼*、重新導向 [*識別碼*](r-tapgloss.md)、重新導向 [*識別碼*](r-tapgloss.md)。</span><span class="sxs-lookup"><span data-stu-id="0478c-113">See *called-ID*, *caller-ID*, [*redirecting ID*](r-tapgloss.md), [*redirection ID*](r-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="0478c-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**呼叫識別碼**</span><span class="sxs-lookup"><span data-stu-id="0478c-114"><span id="tapi2.called_id_tapgloss"></span><span id="TAPI2.CALLED_ID_TAPGLOSS"></span>**called-ID**</span></span>
</dt> <dd>

<span data-ttu-id="0478c-115">識別呼叫的原始目的地位址。</span><span class="sxs-lookup"><span data-stu-id="0478c-115">Identifies the original destination address of a call.</span></span> <span data-ttu-id="0478c-116">請參閱 *呼叫* 重新導向。</span><span class="sxs-lookup"><span data-stu-id="0478c-116">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="0478c-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**呼叫者識別碼**</span><span class="sxs-lookup"><span data-stu-id="0478c-117"><span id="tapi2.caller_id_tapgloss"></span><span id="TAPI2.CALLER_ID_TAPGLOSS"></span>**caller-ID**</span></span>
</dt> <dd>

<span data-ttu-id="0478c-118">識別呼叫的原始位址。</span><span class="sxs-lookup"><span data-stu-id="0478c-118">Identifies the originating address of a call.</span></span> <span data-ttu-id="0478c-119">請參閱 *呼叫* 重新導向。</span><span class="sxs-lookup"><span data-stu-id="0478c-119">See *call redirection*.</span></span>

</dd> <dt>

<span data-ttu-id="0478c-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**中央辦公室**</span><span class="sxs-lookup"><span data-stu-id="0478c-120"><span id="tapi2.central_office_tapgloss"></span><span id="TAPI2.CENTRAL_OFFICE_TAPGLOSS"></span>**central office**</span></span>
</dt> <dd>

<span data-ttu-id="0478c-121">電話公司的當地設施，可在特定區域中提供電話語音。</span><span class="sxs-lookup"><span data-stu-id="0478c-121">Telephone company's local facility that provides telephone service in a specific area.</span></span> <span data-ttu-id="0478c-122">通常，「訂閱者」的行會聯結至將其他「訂閱者」彼此連線、在本機和大量連接的設備。</span><span class="sxs-lookup"><span data-stu-id="0478c-122">Typically, subscribers' lines are joined to switching equipment that connects other subscribers to each other, locally and over long distance.</span></span> <span data-ttu-id="0478c-123">也稱為「 *共同*」。</span><span class="sxs-lookup"><span data-stu-id="0478c-123">Also called *CO*.</span></span>

</dd> <dt>

<span data-ttu-id="0478c-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span><span class="sxs-lookup"><span data-stu-id="0478c-124"><span id="tapi2.centrex_tapgloss"></span><span id="TAPI2.CENTREX_TAPGLOSS"></span>**Centrex**</span></span>
</dt> <dd>

<span data-ttu-id="0478c-125">由當地電話公司從當地的總公司提供的公司電話語音。</span><span class="sxs-lookup"><span data-stu-id="0478c-125">A business telephone service offered by a local telephone company from a local, central office.</span></span>

</dd> <dt>

<span data-ttu-id="0478c-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**以電腦為中心的連接**</span><span class="sxs-lookup"><span data-stu-id="0478c-126"><span id="tapi2.computer_centric_connection_tapgloss"></span><span id="TAPI2.COMPUTER_CENTRIC_CONNECTION_TAPGLOSS"></span>**computer-centric connection**</span></span>
</dt> <dd>

<span data-ttu-id="0478c-127">使用連接至電話網絡與電話組之電腦增益集卡片或外部方塊的連接。</span><span class="sxs-lookup"><span data-stu-id="0478c-127">A connection that uses a computer add-in card or external box that is connected to both the telephone network and the phone set.</span></span> <span data-ttu-id="0478c-128">比較以 [*電話為中心的連接*](p-tapgloss.md)。</span><span class="sxs-lookup"><span data-stu-id="0478c-128">Compare [*phone-centric connection*](p-tapgloss.md).</span></span>

</dd> <dt>

<span data-ttu-id="0478c-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**已連線-識別碼**</span><span class="sxs-lookup"><span data-stu-id="0478c-129"><span id="tapi2.connected_id_tapgloss"></span><span id="TAPI2.CONNECTED_ID_TAPGLOSS"></span>**connected-ID**</span></span>
</dt> <dd>

<span data-ttu-id="0478c-130">呼叫實際連接之合作物件的識別碼。</span><span class="sxs-lookup"><span data-stu-id="0478c-130">Identifier for the party to which the call was actually connected.</span></span> <span data-ttu-id="0478c-131">如果呼叫轉向，這可能與被呼叫的合作物件不同。</span><span class="sxs-lookup"><span data-stu-id="0478c-131">This may be different from the called party if the call was diverted.</span></span>

</dd> </dl>

 

 



