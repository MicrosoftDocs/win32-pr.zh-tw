---
description: 已排入佇列的元件安全性
ms.assetid: 3fbeb81a-e3e4-495b-b891-896877fab92f
title: 已排入佇列的元件安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b51592f6216d7380e877f2cd582a277f1583b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111025"
---
# <a name="queued-components-security"></a><span data-ttu-id="29af5-103">已排入佇列的元件安全性</span><span class="sxs-lookup"><span data-stu-id="29af5-103">Queued Components Security</span></span>

<span data-ttu-id="29af5-104">當用戶端對已排入佇列的物件呼叫方法時，實際上會對記錄器進行呼叫，這會將它封裝成訊息的一部分。</span><span class="sxs-lookup"><span data-stu-id="29af5-104">When a client makes a method call to a queued object, the call is actually made to the recorder, which packages it as part of a message to the server.</span></span> <span data-ttu-id="29af5-105">接聽程式會從佇列讀取訊息，並將它傳遞給播放程式。</span><span class="sxs-lookup"><span data-stu-id="29af5-105">The listener reads the message from the queue and passes it to the player.</span></span> <span data-ttu-id="29af5-106">Player 會叫用實際的伺服器元件，並進行相同的方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="29af5-106">The player invokes the actual server component and makes the same method call.</span></span> <span data-ttu-id="29af5-107">當 player 進行方法呼叫時，伺服器元件必須觀察用戶端的安全性呼叫內容 (而不是播放程式的安全性呼叫內容) 。</span><span class="sxs-lookup"><span data-stu-id="29af5-107">The server component must observe the security call context of the client (not the player's security call context) when the player makes the method call.</span></span> <span data-ttu-id="29af5-108">錄製器會將用戶端的安全性呼叫內容封送處理到訊息中，然後播放程式會在伺服器上拆收它，然後再進行方法呼叫。</span><span class="sxs-lookup"><span data-stu-id="29af5-108">The recorder marshals the client's security call context into the message, and the player unmarshals it at the server before making the method call.</span></span> <span data-ttu-id="29af5-109">就伺服器物件而言，直接呼叫用戶端與播放程式的間接呼叫之間的安全性內容沒有任何差異。</span><span class="sxs-lookup"><span data-stu-id="29af5-109">As far as the server object is concerned, there is no difference in security context between a direct call from the client and an indirect call from the player.</span></span> <span data-ttu-id="29af5-110">尤其是，叫用的方法會以寄件者的許可權執行。</span><span class="sxs-lookup"><span data-stu-id="29af5-110">In particular, the methods invoked execute with the sender's privileges.</span></span>

<span data-ttu-id="29af5-111">COM + 佇列元件支援以角色為基礎的安全性語義，就像是為了與 COM + 應用程式一起使用而建立的其他元件一樣。</span><span class="sxs-lookup"><span data-stu-id="29af5-111">A COM+ queued component supports role-based security semantics just like other components built for use with COM+ applications.</span></span> <span data-ttu-id="29af5-112">因此，佇列應用程式的元件可以使用程式設計介面，來探索其呼叫端的角色成員資格 ([**ISecurityCallCoNtext：： IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) 或特定使用者 ([**ISecurityCallCoNtext：： IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)) 。</span><span class="sxs-lookup"><span data-stu-id="29af5-112">Components of a queued application can therefore use programmatic interfaces to discover the role membership of their caller ([**ISecurityCallContext::IsCallerInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-iscallerinrole)) or a specific user ([**ISecurityCallContext::IsUserInRole**](/windows/desktop/api/ComSvcs/nf-comsvcs-isecuritycallcontext-isuserinrole)).</span></span> <span data-ttu-id="29af5-113">建議任何有潛在安全性影響的已排入佇列元件，都使用這些介面明確檢查寄件者的認證。</span><span class="sxs-lookup"><span data-stu-id="29af5-113">It is recommended that any queued component with a potential security impact use these interfaces to explicitly check the sender's credentials.</span></span>

<span data-ttu-id="29af5-114">呼叫端身分識別是與方法呼叫相關聯的身分識別。</span><span class="sxs-lookup"><span data-stu-id="29af5-114">The caller identity is the identity associated with a method call.</span></span> <span data-ttu-id="29af5-115">以角色為基礎的安全性會使用呼叫端身分識別，並存在於安全性呼叫內容中。</span><span class="sxs-lookup"><span data-stu-id="29af5-115">Caller identity is used by role-based security and is present in the security call context.</span></span> <span data-ttu-id="29af5-116">在已排入佇列的元件中，呼叫端身分識別會表示為訊息佇列訊息中的資料。</span><span class="sxs-lookup"><span data-stu-id="29af5-116">In queued components, the caller identity is represented as data in the Message Queuing message.</span></span> <span data-ttu-id="29af5-117">訊息佇列會驗證訊息寄件者身分識別。</span><span class="sxs-lookup"><span data-stu-id="29af5-117">Message Queuing authenticates the message sender identity.</span></span> <span data-ttu-id="29af5-118">當呼叫端身分識別和訊息寄件者身分識別相同時，訊息佇列會驗證訊息和呼叫端。</span><span class="sxs-lookup"><span data-stu-id="29af5-118">When the caller identity and the message sender identity are the same, Message Queuing authenticates both the message and the caller.</span></span> <span data-ttu-id="29af5-119">這是一般情況。</span><span class="sxs-lookup"><span data-stu-id="29af5-119">This is the usual case.</span></span>

> [!Note]  
> <span data-ttu-id="29af5-120">COM + 佇列的元件不支援模擬樣式的安全性，可讓伺服器取得對應至用戶端身分識別的存取權杖，並使用它來執行存取控制檢查或在用戶端安全性內容下採取動作。</span><span class="sxs-lookup"><span data-stu-id="29af5-120">COM+ queued components does not support impersonation-style security, which allows a server to obtain an access token corresponding to the client identity and use it either to perform access control checks or to act under the client security context.</span></span>

 

<span data-ttu-id="29af5-121">當已排入佇列之元件的呼叫端透過跨進程的錄製器與元件互動時，呼叫端的身分識別和訊息傳送者 (記錄器) 可能會不同。</span><span class="sxs-lookup"><span data-stu-id="29af5-121">When the caller of a queued component is interacting with the component through an out-of-process recorder, the identities of the caller and message sender (recorder) can be different.</span></span> <span data-ttu-id="29af5-122">在此情況下，COM + 佇列的元件會確認訊息寄件者是伺服器上的「QC 信任的使用者」角色的成員。</span><span class="sxs-lookup"><span data-stu-id="29af5-122">In this case, COM+ queued components verifies that the message sender is a member of the QC Trusted User role on the server.</span></span> <span data-ttu-id="29af5-123">此外，跨進程記錄器需要驗證憑證，因為它是由訊息佇列進行驗證。</span><span class="sxs-lookup"><span data-stu-id="29af5-123">Additionally, the out-of-process recorder requires an authentication certificate because it is being authenticated by Message Queuing.</span></span>

<span data-ttu-id="29af5-124">QC 信任的使用者角色的成員可以指定任意的識別碼，這表示惡意的成員可以利用較高的權限來執行佇列元件呼叫。</span><span class="sxs-lookup"><span data-stu-id="29af5-124">Members of the QC Trusted User role are allowed to specify an arbitrary identity, which means that a malicious member could execute a queued component call with elevated privileges.</span></span> <span data-ttu-id="29af5-125">因此建議將這類使用者的數目保持在絕對最少數。</span><span class="sxs-lookup"><span data-stu-id="29af5-125">It is therefore recommended that the number of such users be kept to an absolute minimum.</span></span>

<span data-ttu-id="29af5-126">因為有一項複雜的攻擊與任何機制（會在網路上傳播身分識別）相關聯，以及藉由使用 unexecutable 要求淹沒佇列的簡單阻絕服務攻擊的風險，建議您只在信任的主機網路（例如，在私人網路或虛擬私人網路）上部署 COM + 佇列的元件服務或在適當設定的防火牆後方。</span><span class="sxs-lookup"><span data-stu-id="29af5-126">Because of the risk of a sophisticated attack associated with any mechanism which propagates identity across a network, as well as the risk of a simple denial of service attack by flooding the queues with unexecutable requests, it is recommended that you deploy the COM+ queued components service only on a network of trusted hosts—for example, on a private network or a virtual private network, or behind an appropriately configured firewall.</span></span>

<span data-ttu-id="29af5-127">COM + 佇列元件會透過 DCOM 執行，因此您可以在佇列應用程式的 [內容]**工作表的**[**安全性**] 索引標籤上，選取 [封 **包隱私權**] 作為 [**呼叫的驗證等級**] 設定，以協助保護佇列方法呼叫的完整性和機密性。</span><span class="sxs-lookup"><span data-stu-id="29af5-127">COM+ queued components runs over DCOM, so you can help protect the integrity and secrecy of queued method calls by selecting **Packet Privacy** as the **Authentication Level of Calls** setting on the **Security** tab of your queued application's **Properties** sheet.</span></span>

## <a name="related-topics"></a><span data-ttu-id="29af5-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="29af5-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="29af5-129">COM + 安全性</span><span class="sxs-lookup"><span data-stu-id="29af5-129">COM+ Security</span></span>](com--security.md)
</dt> <dt>

[<span data-ttu-id="29af5-130">工作組模式中的安全性限制</span><span class="sxs-lookup"><span data-stu-id="29af5-130">Security Limitations in Workgroup Mode</span></span>](security-limitations-in-workgroup-mode.md)
</dt> <dt>

[<span data-ttu-id="29af5-131">指定驗證通訊協定</span><span class="sxs-lookup"><span data-stu-id="29af5-131">Specifying the Authentication Protocol</span></span>](specifying-the-authentication-protocol.md)
</dt> </dl>

 

 



