---
description: TAPI 3 秒會合 IP 電話語音會議中說明了使用以 IP 為基礎的網路的 Advanced 會議。 下列是基本會議的相關內容。
ms.assetid: f685097b-1b54-412b-999f-d9bdb3120ab9
title: 會議
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ace4cb45bf74335298a3d4d262d064eb85c547f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107000081"
---
# <a name="conference"></a><span data-ttu-id="2cc0c-104">會議</span><span class="sxs-lookup"><span data-stu-id="2cc0c-104">Conference</span></span>

<span data-ttu-id="2cc0c-105">使用以 IP 為基礎的網路的 Advanced 會議，說明于 TAPI 3 的會合 [IP 電話語音會議](rendezvous-ip-telephony-conferencing.md)中。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-105">Advanced conferencing using IP-based networks is described in TAPI 3's [Rendezvous IP Telephony Conferencing](rendezvous-ip-telephony-conferencing.md).</span></span> <span data-ttu-id="2cc0c-106">下列是基本會議的相關內容。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-106">The following material relates to basic conferencing.</span></span>

<span data-ttu-id="2cc0c-107">會議研討會是同時包含兩方以上的會話。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-107">Conference sessions are sessions that include more than two parties simultaneously.</span></span> <span data-ttu-id="2cc0c-108">您可以使用以外部伺服器為基礎的橋接器或以交換器為基礎的會議橋接器來設定它們。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-108">They can be set up using either an external server-based bridge or a switch-based conference bridge.</span></span>

<span data-ttu-id="2cc0c-109">在以伺服器為基礎的會議會話中，所有參與的合作物件都會撥入伺服器，該伺服器會將媒體串流混合在一起，並將混合的每個參與者傳送出去。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-109">In server-based conference sessions, all participating parties dial into the server, which mixes the media streams together and sends each participant the mix.</span></span> <span data-ttu-id="2cc0c-110">只有在應用程式和橋接器伺服器之間進行單一呼叫的情況下，才會有個別合作物件的概念。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-110">There may be no notion of individual parties in the conference call, only that of a single call between the application and the bridge server.</span></span> <span data-ttu-id="2cc0c-111">對 TAPI 而言，這種類型的會議呼叫似乎是正常的一對一連線。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-111">To TAPI, this type of conference call appears to be a normal one-to-one connection.</span></span>

<span data-ttu-id="2cc0c-112">以交換器為基礎的會議會進行階段，其中有些可能會在服務提供者支援時結合：</span><span class="sxs-lookup"><span data-stu-id="2cc0c-112">Switch-based conferencing proceeds in stages, some of which may be combined if the service provider supports it:</span></span>

1.  <span data-ttu-id="2cc0c-113">起始一般通訊會話。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-113">Initiate an ordinary communications session.</span></span>
2.  <span data-ttu-id="2cc0c-114">建立會議會話，其中第一個成員是起始會議的合作物件。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-114">Create a conference session with its first member the party that initiated conferencing.</span></span>
3.  <span data-ttu-id="2cc0c-115">在目前連接的另一端，與合作物件建立會議諮詢會話。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-115">Create a conference consultation session with the party at the other end of the current connection.</span></span>
4.  <span data-ttu-id="2cc0c-116">將諮詢會話新增至會議。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-116">Add the consultation session to the conference.</span></span>

<span data-ttu-id="2cc0c-117">當會話成為會議的成員之後，該成員的狀態就會還原為 conferenced。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-117">After a session becomes a member of a conference, the member's state reverts to conferenced.</span></span> <span data-ttu-id="2cc0c-118">會議會話的狀態通常會變成 [ *已連線*]。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-118">The state of the conference session typically becomes *connected*.</span></span> <span data-ttu-id="2cc0c-119">會議的會話識別碼和所有加入的合作物件都會保持有效。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-119">The session identifiers to the conference and all the added parties remain valid.</span></span> <span data-ttu-id="2cc0c-120">您可以接收所有呼叫的狀態事件。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-120">State events can be received about all calls.</span></span> <span data-ttu-id="2cc0c-121">例如，如果其中一個成員因為掛斷而中斷連線，則適當的狀態訊息會通知應用程式這項事實。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-121">For example, if one of the members disconnects by hanging up, an appropriate state message can inform the application of this fact.</span></span>

<span data-ttu-id="2cc0c-122">**TAPI 2.x：** 應用程式可以使用 LINECALLPARAMFLAGS NOHOLDCONFERENCE 選項來使用 Pbx 的「無保留會議」功能 \_ ; 這項功能可讓另一部裝置（例如監督員或錄製裝置）以無訊息模式附加至該行。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-122">**TAPI 2.x:** Applications can use the "no hold conference" feature of PBXs by using the LINECALLPARAMFLAGS\_NOHOLDCONFERENCE option; this feature allows another device, such as a supervisor or recording device, to be silently attached to the line.</span></span>

<span data-ttu-id="2cc0c-123">當您取消會議協力廠商的諮詢會話或在先前建立的會議中移除協力廠商時，服務提供者可能會釋出會議，並將會話還原為一般的兩方連線。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-123">When canceling the consultation session to the third party for a conference or when removing the third party in a previously established conference, the service provider may release the conference and revert the session back to a normal two-party connection.</span></span> <span data-ttu-id="2cc0c-124">如果是這種情況，會議會話將會轉換為 *閒置* 狀態，而唯一剩餘的參與會話將會從 conferenced 轉換為 *連線* 狀態。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-124">If this is the case, the conference session will transition to the *idle* state, and the only remaining participating session will transition from the conferenced to the *connected* state.</span></span>

<span data-ttu-id="2cc0c-125">並非所有服務提供者都支援會議。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-125">Not all service providers support conferencing.</span></span>

<span data-ttu-id="2cc0c-126">**TAPI 2.x：**[**LineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference)函式會接受原始的兩方呼叫做為輸入、配置會議通話、將原始呼叫連接到會議，以及配置將控制碼傳回給應用程式的諮詢通話。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-126">**TAPI 2.x:** The [**lineSetupConference**](/windows/win32/api/tapi/nf-tapi-linesetupconference) function takes the original two-party call as input, allocates a conference call, connects the original call to the conference, and allocates a consultation call whose handle is returned to the application.</span></span>

<span data-ttu-id="2cc0c-127">如果應用程式要將另一個成員新增至會議，可以在諮詢電話上執行撥號操作。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-127">If the application is going to add another member to the conference, a dial operation can be performed on the consultation call.</span></span> <span data-ttu-id="2cc0c-128">接著會在 [**lineAddToConference**](/windows/win32/api/tapi/nf-tapi-lineaddtoconference) 函式中使用會議通話控制碼和諮詢通話連接。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-128">The conference call handle and the consultation call connection are then used in the [**lineAddToConference**](/windows/win32/api/tapi/nf-tapi-lineaddtoconference) function.</span></span> <span data-ttu-id="2cc0c-129">如果服務提供者支援，也可以使用 [**linePrepareAddToConference**](/windows/win32/api/tapi/nf-tapi-lineprepareaddtoconference) 函數來新增會議成員。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-129">Conference members may also be added using [**linePrepareAddToConference**](/windows/win32/api/tapi/nf-tapi-lineprepareaddtoconference) function, if supported by the service provider.</span></span>

<span data-ttu-id="2cc0c-130">如果服務提供者支援，則會使用 [**lineRemoveFromConference**](/windows/win32/api/tapi/nf-tapi-lineremovefromconference) 函式移除會議成員。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-130">Conference members are removed using the [**lineRemoveFromConference**](/windows/win32/api/tapi/nf-tapi-lineremovefromconference) function, if the service provider supports it.</span></span>

<span data-ttu-id="2cc0c-131">或者，您也可以使用 [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer) 函式來建立會議，此函式會傳回諮詢通話控制碼，而 [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer) 函式會使用會議選項 (而非 [傳送](transfer-ovr.md) 選項) 。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-131">Alternatively, a conference may be created using the [**lineSetupTransfer**](/windows/win32/api/tapi/nf-tapi-linesetuptransfer) function, which returns a consultation call handle, and the [**lineCompleteTransfer**](/windows/win32/api/tapi/nf-tapi-linecompletetransfer) function with the conference option (instead of the [transfer](transfer-ovr.md) option).</span></span>

<span data-ttu-id="2cc0c-132">**TAPI 3.x：**[**ITBasicCallControl：：**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-conference) session 方法會將現有的會話作為輸入，並建立 [CallHub 物件](callhub-object.md)（如果尚未存在的話）。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-132">**TAPI 3.x:** The [**ITBasicCallControl::Conference**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-conference) method takes the existing session as input and creates a [CallHub object](callhub-object.md) if one does not already exist.</span></span> <span data-ttu-id="2cc0c-133">[**ITBasicCallControl：： Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish)方法會將諮詢呼叫加入至 CallHub。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-133">The [**ITBasicCallControl::Finish**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-finish) method adds the consultation call to the CallHub.</span></span> <span data-ttu-id="2cc0c-134">您可以使用 [**ITAddress：： CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall)建立其他諮詢會話，並使用「 **會議** 」和「 **完成** 」方法新增。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-134">Additional consultation sessions may be created using [**ITAddress::CreateCall**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-createcall), and added using the **Conference** and **Finish** methods.</span></span>

> [!Note]  
> <span data-ttu-id="2cc0c-135">定址線路裝置的功能可限制在單一呼叫中 conferenced 的合作物件數目，以及會議是否以一般的兩方電話開始。</span><span class="sxs-lookup"><span data-stu-id="2cc0c-135">The capabilities of the addressed line device can limit the number of parties conferenced in a single call and whether or not a conference starts out with a normal two-party call.</span></span>

 

 

 
