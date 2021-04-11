---
description: 近端分享的 Windows 對等元件
ms.assetid: aa9e7d4d-4131-4578-8bd1-298f04b826f9
title: 近端分享的 Windows 對等元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc6c780ccad1abd5ce04c1672f66561285831e5a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103944270"
---
# <a name="windows-peer-components-for-people-near-me"></a><span data-ttu-id="06e7e-103">近端分享的 Windows 對等元件</span><span class="sxs-lookup"><span data-stu-id="06e7e-103">Windows Peer Components for People Near Me</span></span>

<span data-ttu-id="06e7e-104">在主要的 Windows 對等網路可執行檔 (P2phost.exe) 中， [近端分享架構](people-near-me-architecture.md) 會使用下列元件：</span><span class="sxs-lookup"><span data-stu-id="06e7e-104">Within the main Windows Peer Networking executable (P2phost.exe), the [People Near Me Architecture](people-near-me-architecture.md) uses the following components:</span></span>

### <a name="people-near-me"></a><span data-ttu-id="06e7e-105">近端分享</span><span class="sxs-lookup"><span data-stu-id="06e7e-105">People Near Me</span></span>

<span data-ttu-id="06e7e-106">近端分享 (PNM) 元件會針對支援 PNM 之電腦的使用者名稱，使用本機子網上的 Web 服務探索來起始探索。</span><span class="sxs-lookup"><span data-stu-id="06e7e-106">The People Near Me (PNM) component initiates discovery using Web Services Discovery on the local subnet for the user names of PNM-capable computers.</span></span>

### <a name="people-near-me-publisher"></a><span data-ttu-id="06e7e-107">近端分享發行者</span><span class="sxs-lookup"><span data-stu-id="06e7e-107">People Near Me Publisher</span></span>

<span data-ttu-id="06e7e-108">近端分享發行者元件會發佈已登入使用者的昵稱，以指出在本機子網上使用 PNM 的其他電腦可用性。</span><span class="sxs-lookup"><span data-stu-id="06e7e-108">The People Near Me Publisher component publishes the nicknames of logged-on users to indicate availability to other computers using PNM on the local subnet.</span></span> <span data-ttu-id="06e7e-109">登入的使用者必須選擇在公告昵稱之前發佈其昵稱。</span><span class="sxs-lookup"><span data-stu-id="06e7e-109">The logged-on user must elect to publish their nickname before it is advertised.</span></span> <span data-ttu-id="06e7e-110">昵稱是使用 Web 服務探索在子網上發佈的。</span><span class="sxs-lookup"><span data-stu-id="06e7e-110">The nickname is published on the subnet using Web Services Discovery.</span></span> <span data-ttu-id="06e7e-111">此外，也可以發行物件和應用程式。</span><span class="sxs-lookup"><span data-stu-id="06e7e-111">Additionally, objects and applications can also be published.</span></span> <span data-ttu-id="06e7e-112">但是，使用者必須為「**近端分享**」或「**全部**」範圍指定物件和應用程式發行。</span><span class="sxs-lookup"><span data-stu-id="06e7e-112">However, the user must specify object and application publication for the '**People Near Me**' or '**All**' scopes.</span></span>

### <a name="people-near-me-enumerator"></a><span data-ttu-id="06e7e-113">近端分享列舉值</span><span class="sxs-lookup"><span data-stu-id="06e7e-113">People Near Me Enumerator</span></span>

<span data-ttu-id="06e7e-114">近端分享枚舉器元件會列舉本機子網上的使用者清單。</span><span class="sxs-lookup"><span data-stu-id="06e7e-114">The People Near Me Enumerator component enumerates the list of users on the local subnet.</span></span> <span data-ttu-id="06e7e-115">使用此清單，Web 服務探索會傳送多播查詢並接收回應。</span><span class="sxs-lookup"><span data-stu-id="06e7e-115">Using this list, Web Services Discovery sends a multicast query and receives the responses.</span></span> <span data-ttu-id="06e7e-116">取得昵稱清單之後，應用程式就可以使用此 API 來取得使用者所發佈的更多資料 (使用 [SChannel](windows-vista-components-for-people-near-me.md)) 加密，例如已註冊的應用程式清單，以及任何要發行的物件。</span><span class="sxs-lookup"><span data-stu-id="06e7e-116">After the list of nicknames are obtained, an application can use the API to retrieve more data being published by the user (which is encrypted using [SChannel](windows-vista-components-for-people-near-me.md)), such as the list of applications registered and any objects being published.</span></span>

<span data-ttu-id="06e7e-117">搜尋和列舉程式不會自動發生，而是必須由使用者或應用程式以登入 PNM 來明確起始。</span><span class="sxs-lookup"><span data-stu-id="06e7e-117">The search and enumeration process does not happen automatically, but must be explicitly initiated by a user or an application by signing-in to PNM.</span></span> <span data-ttu-id="06e7e-118">搜尋結果是在相同子網上使用 PNM API 公告其昵稱的其他使用者的昵稱清單。</span><span class="sxs-lookup"><span data-stu-id="06e7e-118">The search results are the list of nicknames of other users on the same subnet that are advertising their nicknames using the PNM API.</span></span>

### <a name="publication-manager"></a><span data-ttu-id="06e7e-119">發行集管理員</span><span class="sxs-lookup"><span data-stu-id="06e7e-119">Publication Manager</span></span>

<span data-ttu-id="06e7e-120">發行集管理員元件負責將目前狀態、應用程式或物件更新發佈給訂閱或輪詢資料的連絡人或近端人員。</span><span class="sxs-lookup"><span data-stu-id="06e7e-120">The Publication Manager component is responsible for publishing presence, application, or object updates to contacts or people near me that are subscribed or poll for data.</span></span>

### <a name="peer-signaling"></a><span data-ttu-id="06e7e-121">對等信號</span><span class="sxs-lookup"><span data-stu-id="06e7e-121">Peer Signaling</span></span>

<span data-ttu-id="06e7e-122">對等信號元件會處理對等互連與 exchange 資料之間的連接建立。</span><span class="sxs-lookup"><span data-stu-id="06e7e-122">The Peer Signaling component handles the creation of connections between peers to exchange data.</span></span> <span data-ttu-id="06e7e-123">針對近端分享，當使用者或應用程式將單播查詢傳送至特定電腦以取得其公開金鑰、應用程式和物件時，就會使用對等信號。</span><span class="sxs-lookup"><span data-stu-id="06e7e-123">For People Near Me, Peer Signaling is used when a user or application sends the unicast query to a specific computer for its public key, applications, and objects.</span></span>

### <a name="receive-invitation-handlerux"></a><span data-ttu-id="06e7e-124">接收邀請處理常式/UX</span><span class="sxs-lookup"><span data-stu-id="06e7e-124">Receive Invitation Handler/UX</span></span>

<span data-ttu-id="06e7e-125">接收邀請處理常式/UX 元件接收來自其他人的傳入邀請，會提示使用者決定是否要啟動與邀請相關聯的應用程式，然後根據接受邀請的使用者來啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="06e7e-125">The Receive Invitation Handler/UX component receives an incoming invitation from another person, prompts the user to determine whether they want to launch the application associated with the invitation, and then launches the application based on the user accepting the invitation.</span></span> <span data-ttu-id="06e7e-126">邀請是來自其他人的訊息，可使用安裝在這兩個使用者電腦上的特定應用程式起始共同作業活動，並且由受邀的使用者進行公告。</span><span class="sxs-lookup"><span data-stu-id="06e7e-126">An invitation is a message from another person to initiate collaboration activity using a specific application that is installed on both user's computers and is advertised by the user being invited.</span></span>

### <a name="peer-security"></a><span data-ttu-id="06e7e-127">對等安全性</span><span class="sxs-lookup"><span data-stu-id="06e7e-127">Peer Security</span></span>

<span data-ttu-id="06e7e-128">傳送狀態、應用程式和物件時，會使用 SSL 通道 ([Schannel](windows-vista-components-for-people-near-me.md)) 來加密資訊。</span><span class="sxs-lookup"><span data-stu-id="06e7e-128">When presence, application, and object are sent, the information is encrypted using an SSL channel ([Schannel](windows-vista-components-for-people-near-me.md)).</span></span> <span data-ttu-id="06e7e-129">起始電腦使用受邀電腦的公開金鑰來協商秘密金鑰，該金鑰是用來加密在兩個對等之間傳送的後續資料。</span><span class="sxs-lookup"><span data-stu-id="06e7e-129">The initiating computer uses the public key of the invited computer to negotiate a secret key that is used for encrypting the subsequent data sent between the two peers.</span></span>

 

 



