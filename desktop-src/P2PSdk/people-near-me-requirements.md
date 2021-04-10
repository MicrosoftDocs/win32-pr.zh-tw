---
description: 近端分享需求
ms.assetid: c7ab73fc-56a6-4b6c-820a-3f8e4a97cfaf
title: 近端分享需求
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff6afb97800041e0fcd9a10a6d95334b832fb363
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849306"
---
# <a name="people-near-me-requirements"></a><span data-ttu-id="66afa-103">近端分享需求</span><span class="sxs-lookup"><span data-stu-id="66afa-103">People Near Me Requirements</span></span>

<span data-ttu-id="66afa-104">為了讓 [近端分享](about-people-near-me.md) 為 Windows 對等網路應用程式提供順暢的連線能力和簡單的共同作業，請完成下列作業：</span><span class="sxs-lookup"><span data-stu-id="66afa-104">In order for [People Near Me](about-people-near-me.md) to provide seamless connectivity and easy collaboration to users for Windows Peer Networking applications, the following is accomplished:</span></span>

### <a name="people-discovery"></a><span data-ttu-id="66afa-105">人們探索</span><span class="sxs-lookup"><span data-stu-id="66afa-105">People Discovery</span></span>

<span data-ttu-id="66afa-106">人們探索可讓使用者探索和顯示位於本機子網上的一組對等。</span><span class="sxs-lookup"><span data-stu-id="66afa-106">People Discovery allows a user to discover and display the set of peers that are located on the local subnet.</span></span> <span data-ttu-id="66afa-107">本機子網上的任何電腦都必須通告登入對等的名稱。</span><span class="sxs-lookup"><span data-stu-id="66afa-107">Any computers on the local subnet must advertise the names of logged-on peers.</span></span> <span data-ttu-id="66afa-108">探索查詢之後所列的對等，是一組執行 Windows Vista 的使用者，已設定為使用 [近端分享](about-people-near-me.md)將昵稱通告給其他使用者。</span><span class="sxs-lookup"><span data-stu-id="66afa-108">The peers listed after a discovery query are the set of users running Windows Vista that are configured to advertise a nickname to other users using [People Near Me](about-people-near-me.md).</span></span> <span data-ttu-id="66afa-109">這項功能預設為停用，且必須由已登入的使用者啟用。</span><span class="sxs-lookup"><span data-stu-id="66afa-109">This capability is disabled by default and must be enabled by the logged-in user.</span></span>

> [!Note]  
> <span data-ttu-id="66afa-110">在「近端分享」探索程式期間探索到的遠端對等，不一定是與探索到之對等相關聯的預期使用者。</span><span class="sxs-lookup"><span data-stu-id="66afa-110">Remote peers discovered during the 'People Near Me' discovery process are not necessarily the anticipated users associated with the discovered peers.</span></span>

 

### <a name="extended-data-discovery"></a><span data-ttu-id="66afa-111">擴充資料探索</span><span class="sxs-lookup"><span data-stu-id="66afa-111">Extended Data Discovery</span></span>

<span data-ttu-id="66afa-112">擴充資料探索允許搜尋有特定興趣的使用者。</span><span class="sxs-lookup"><span data-stu-id="66afa-112">Extended Data Discovery allows searches for users that have specific interests.</span></span> <span data-ttu-id="66afa-113">使用者也可以指定他們想要通告本身的其他資料。</span><span class="sxs-lookup"><span data-stu-id="66afa-113">It is also possible for users to specify that they want to advertise additional data about themselves.</span></span> <span data-ttu-id="66afa-114">例如，除了已登入之使用者的昵稱之外，資料也可以在產業會議上概述特定的專業興趣。</span><span class="sxs-lookup"><span data-stu-id="66afa-114">For example the data could outline specific professional interests at an industry conference, in addition to the nickname of the logged in user.</span></span>

### <a name="application-discovery"></a><span data-ttu-id="66afa-115">應用程式探索</span><span class="sxs-lookup"><span data-stu-id="66afa-115">Application Discovery</span></span>

<span data-ttu-id="66afa-116">近端分享啟用的臨機操作共同作業的確切本質是應用程式所特有。</span><span class="sxs-lookup"><span data-stu-id="66afa-116">The exact nature of the ad hoc collaboration enabled by People Near Me is specific to applications.</span></span> <span data-ttu-id="66afa-117">例如，共同作業可能正在聊天或共用相片，而這兩者都需要特定的應用程式。</span><span class="sxs-lookup"><span data-stu-id="66afa-117">For example, the collaboration might be chatting or sharing photos, both requiring specific applications.</span></span> <span data-ttu-id="66afa-118">為了讓近端分享能夠啟用共同作業活動，一組適用于近端分享案例的應用程式也必須經過公告和探索。</span><span class="sxs-lookup"><span data-stu-id="66afa-118">In order for People Near Me to enable collaboration activities, the set of applications that are available for People Near Me scenarios must also be advertised and discoverable.</span></span>

### <a name="subscription"></a><span data-ttu-id="66afa-119">訂用帳戶</span><span class="sxs-lookup"><span data-stu-id="66afa-119">Subscription</span></span>

<span data-ttu-id="66afa-120">使用訂用帳戶，應用程式可以訂閱以追蹤人員的存在性、應用程式和物件變更。</span><span class="sxs-lookup"><span data-stu-id="66afa-120">Using a subscription, applications can subscribe to track a person's presence, applications, and object changes.</span></span>

### <a name="invitation"></a><span data-ttu-id="66afa-121">邀請</span><span class="sxs-lookup"><span data-stu-id="66afa-121">Invitation</span></span>

<span data-ttu-id="66afa-122">在探索到人員、興趣和應用程式之後，使用近端分享應用程式的對等共同作業，可以開始邀請和接受交換。</span><span class="sxs-lookup"><span data-stu-id="66afa-122">After the people, interests, and applications have been discovered, peer collaboration, using a People Near Me application, can begin an invitation and acceptance exchange.</span></span> <span data-ttu-id="66afa-123">初始化對等會將邀請訊息傳送給另一個對等。</span><span class="sxs-lookup"><span data-stu-id="66afa-123">The initiating peer sends an invitation message to another peer or peers.</span></span> <span data-ttu-id="66afa-124">收到邀請的使用者可以接受或拒絕邀請。</span><span class="sxs-lookup"><span data-stu-id="66afa-124">The users receiving the invitation can accept or decline the invitation.</span></span> <span data-ttu-id="66afa-125">接受邀請時，會啟動所要求活動的適當對等應用程式。</span><span class="sxs-lookup"><span data-stu-id="66afa-125">When the invitation is accepted the appropriate peer application for the requested activity is launched.</span></span>

### <a name="add-as-a-contact"></a><span data-ttu-id="66afa-126">新增為連絡人</span><span class="sxs-lookup"><span data-stu-id="66afa-126">Add As A Contact</span></span>

<span data-ttu-id="66afa-127">如果使用者透過近端分享建立共同作業活動，並且想要維護一段時間的連絡人，他們可以將彼此新增為連絡人。</span><span class="sxs-lookup"><span data-stu-id="66afa-127">If users establish a collaboration activity through People Near Me and want to maintain contact over time, they can add each other as a contact.</span></span> <span data-ttu-id="66afa-128">完成這項作業之後，他們就可以觀察使用者的目前狀態 (例如線上、離線或離開) ，並在網際網路上隨時邀請他們進入共同作業活動。</span><span class="sxs-lookup"><span data-stu-id="66afa-128">Once this is accomplished they can observe the presence status of a user (such as online, offline, or away) and invite them to a collaboration activity at any time across the Internet.</span></span> <span data-ttu-id="66afa-129">當人位於附近時，任何可能的活動也可以透過網際網路的連絡人進行。</span><span class="sxs-lookup"><span data-stu-id="66afa-129">Any activity that was possible with the person when they were located nearby is also possible with a contact over the Internet.</span></span>

### <a name="security"></a><span data-ttu-id="66afa-130">安全性</span><span class="sxs-lookup"><span data-stu-id="66afa-130">Security</span></span>

<span data-ttu-id="66afa-131">若要保護對等共同作業活動中所交換的使用者和資料，使用者可以對所公告的內容進行配置控制。</span><span class="sxs-lookup"><span data-stu-id="66afa-131">To protect the users and the data being exchanged in a peer collaboration activity, users have configuration control over what is being advertised.</span></span> <span data-ttu-id="66afa-132">使用者也必須接受邀請，才可開始對等共同作業。</span><span class="sxs-lookup"><span data-stu-id="66afa-132">Users must also accept an invitation before peer collaboration can begin.</span></span> <span data-ttu-id="66afa-133">共同作業活動會使用安全通訊端層 (SSL) 加密通道進行加密 (也稱為 Schannel) 。</span><span class="sxs-lookup"><span data-stu-id="66afa-133">The collaboration activity is encrypted with a Secure Sockets Layer (SSL)-encrypted channel (also known as Schannel).</span></span> <span data-ttu-id="66afa-134">SSL 是一種密碼編譯通訊協定，可保護以 TCP 為基礎的通訊。</span><span class="sxs-lookup"><span data-stu-id="66afa-134">SSL is a cryptographic protocol to protect TCP-based communications.</span></span> <span data-ttu-id="66afa-135">如需詳細資訊，請參閱 [SChannel](windows-vista-components-for-people-near-me.md)。</span><span class="sxs-lookup"><span data-stu-id="66afa-135">For more information, see [SChannel](windows-vista-components-for-people-near-me.md).</span></span> <span data-ttu-id="66afa-136">在 Windows Vista 中， [Windows 對等網路](what-is-peer-networking-.md)架構中的一組新元件支援這些需求。</span><span class="sxs-lookup"><span data-stu-id="66afa-136">These requirements are supported by a new set of components in the [Windows Peer Networking](what-is-peer-networking-.md)architecture in Windows Vista.</span></span>

 

 



