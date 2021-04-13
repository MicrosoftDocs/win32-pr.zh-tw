---
title: " (網路管理) 的訊息函數"
description: 網路管理訊息功能會傳送訊息並維護訊息別名。 訊息函數如下所示。
ms.assetid: 9face737-3472-4a53-97b6-e861a60ee96a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3629a281637fe4ecd0c937ce0c7504beac8e11d2
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383706"
---
# <a name="message-functions-network-management"></a><span data-ttu-id="dca0f-104"> (網路管理) 的訊息函數</span><span class="sxs-lookup"><span data-stu-id="dca0f-104">Message Functions (Network Management)</span></span>

<span data-ttu-id="dca0f-105">\[由於不支援「警報器」和「messenger」服務，因此 Windows Vista 不支援訊息功能。\]</span><span class="sxs-lookup"><span data-stu-id="dca0f-105">\[The message functions are not supported as of Windows Vista because the alerter and messenger services are not supported.\]</span></span>

<span data-ttu-id="dca0f-106">網路管理訊息功能會傳送訊息並維護訊息別名。</span><span class="sxs-lookup"><span data-stu-id="dca0f-106">The network management message functions send messages and maintain message aliases.</span></span> <span data-ttu-id="dca0f-107">訊息函數如下所示。</span><span class="sxs-lookup"><span data-stu-id="dca0f-107">The message functions are listed following.</span></span>

<span data-ttu-id="dca0f-108">**Windows Server 2003：** 預設會停用警報器和 messenger 服務。</span><span class="sxs-lookup"><span data-stu-id="dca0f-108">**Windows Server 2003:** The alerter and messenger services are disabled by default.</span></span> <span data-ttu-id="dca0f-109">您必須重新啟用服務，才能呼叫網路管理 [警示功能](alert-functions.md) 或網路管理訊息功能。</span><span class="sxs-lookup"><span data-stu-id="dca0f-109">You must re-enable the services before calling the network management [Alert functions](alert-functions.md) or the network management Message functions.</span></span>



| <span data-ttu-id="dca0f-110">函式</span><span class="sxs-lookup"><span data-stu-id="dca0f-110">Function</span></span>                                               | <span data-ttu-id="dca0f-111">描述</span><span class="sxs-lookup"><span data-stu-id="dca0f-111">Description</span></span>                                                                     |
|--------------------------------------------------------|---------------------------------------------------------------------------------|
| [<span data-ttu-id="dca0f-112">**NetMessageBufferSend**</span><span class="sxs-lookup"><span data-stu-id="dca0f-112">**NetMessageBufferSend**</span></span>](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagebuffersend)   | <span data-ttu-id="dca0f-113">將訊息傳送至已註冊的訊息別名。</span><span class="sxs-lookup"><span data-stu-id="dca0f-113">Sends a message to a registered message alias.</span></span>                                  |
| [<span data-ttu-id="dca0f-114">**NetMessageNameAdd**</span><span class="sxs-lookup"><span data-stu-id="dca0f-114">**NetMessageNameAdd**</span></span>](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd)         | <span data-ttu-id="dca0f-115">在訊息名稱資料表中註冊訊息別名。</span><span class="sxs-lookup"><span data-stu-id="dca0f-115">Registers a message alias in the message name table.</span></span>                            |
| [<span data-ttu-id="dca0f-116">**NetMessageNameDel**</span><span class="sxs-lookup"><span data-stu-id="dca0f-116">**NetMessageNameDel**</span></span>](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamedel)         | <span data-ttu-id="dca0f-117">從訊息名稱資料表刪除訊息別名。</span><span class="sxs-lookup"><span data-stu-id="dca0f-117">Deletes a message alias from the message name table.</span></span>                            |
| [<span data-ttu-id="dca0f-118">**NetMessageNameEnum**</span><span class="sxs-lookup"><span data-stu-id="dca0f-118">**NetMessageNameEnum**</span></span>](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameenum)       | <span data-ttu-id="dca0f-119">列出儲存在訊息名稱資料表中的所有訊息別名。</span><span class="sxs-lookup"><span data-stu-id="dca0f-119">Lists all the message aliases stored in the message name table.</span></span>                 |
| [<span data-ttu-id="dca0f-120">**NetMessageNameGetInfo**</span><span class="sxs-lookup"><span data-stu-id="dca0f-120">**NetMessageNameGetInfo**</span></span>](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenamegetinfo) | <span data-ttu-id="dca0f-121">傳回訊息名稱資料表中特定訊息別名的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="dca0f-121">Returns information about a particular message alias in the message name table.</span></span> |



 

<span data-ttu-id="dca0f-122">*訊息* 是傳送給網路上的使用者或應用程式之文字資料的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="dca0f-122">A *message* is a buffer of text data sent to a user or application on the network.</span></span> <span data-ttu-id="dca0f-123">若要接收訊息，使用者或應用程式必須在電腦的訊息名稱表格中註冊訊息別名。</span><span class="sxs-lookup"><span data-stu-id="dca0f-123">To receive a message, a user or application must register a message alias in a computer's table of message names.</span></span> <span data-ttu-id="dca0f-124">預設會註冊下列別名：「使用者」、「電腦」、「網域」或「」 \* (電腦) 的目前網域。</span><span class="sxs-lookup"><span data-stu-id="dca0f-124">The following aliases are registered by default: "user", "machine", "domain", or "\*" (the current domain of the computer).</span></span> <span data-ttu-id="dca0f-125">"Domain" 別名指定一組電腦，這些電腦的功能變數名稱定義為其網域或其工作組，並接聽相同子網的廣播。</span><span class="sxs-lookup"><span data-stu-id="dca0f-125">The "domain" alias specifies the set of computers that have the same domain name defined as their domain or as their workgroup and listen to broadcasts on the same subnet.</span></span> <span data-ttu-id="dca0f-126">針對 NetBIOS over TCP/IP，如果名稱伺服器解析功能變數名稱，或在路由器之間轉送 NetBIOS 資料包廣播，則指定 "domain" 別名也可以跨子網成功。</span><span class="sxs-lookup"><span data-stu-id="dca0f-126">For NetBIOS over TCP/IP, specifying the "domain" alias can also succeed across subnets if the domain name is resolved by a name server, or if NetBIOS datagram broadcasts are forwarded across routers.</span></span> <span data-ttu-id="dca0f-127">因此，傳送至網域的訊息無法保證傳遞至網域的所有成員。</span><span class="sxs-lookup"><span data-stu-id="dca0f-127">Therefore, messages sent to a domain do not have guaranteed delivery to all members of the domain.</span></span> <span data-ttu-id="dca0f-128">如果某些網域成員已安裝多個支援 NetBIOS 的傳輸，也可能會多次接收訊息。</span><span class="sxs-lookup"><span data-stu-id="dca0f-128">It is also possible for some domain members to receive the message multiple times if they have multiple transports installed that support NetBIOS.</span></span>

<span data-ttu-id="dca0f-129">您也可以藉由呼叫 [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) 函數來註冊訊息別名。</span><span class="sxs-lookup"><span data-stu-id="dca0f-129">You can also register a message alias by calling the [**NetMessageNameAdd**](/windows/desktop/api/Lmmsg/nf-lmmsg-netmessagenameadd) function.</span></span> <span data-ttu-id="dca0f-130">*訊息名稱表* 包含已註冊的訊息別名清單 (使用者和應用程式) 允許接收訊息。</span><span class="sxs-lookup"><span data-stu-id="dca0f-130">A *message name table* contains a list of registered message aliases (users and applications) permitted to receive messages.</span></span> <span data-ttu-id="dca0f-131">在訊息名稱表格中註冊的別名不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="dca0f-131">The aliases registered in the message name table are case insensitive.</span></span>

<span data-ttu-id="dca0f-132">接收端電腦上必須執行 messenger 服務，才能在接收到訊息時顯示快顯視窗訊息。</span><span class="sxs-lookup"><span data-stu-id="dca0f-132">The messenger service must be running on the receiving computer to display a pop-up message when the message is received.</span></span> <span data-ttu-id="dca0f-133">此外，工作站服務必須在本機電腦上執行。</span><span class="sxs-lookup"><span data-stu-id="dca0f-133">In addition, the Workstation service must be running on the local computer.</span></span> <span data-ttu-id="dca0f-134">NetBIOS 是在傳送者與接收者之間使用的傳輸機制。</span><span class="sxs-lookup"><span data-stu-id="dca0f-134">NetBIOS is the transport mechanism used between the sender and receiver.</span></span>

<span data-ttu-id="dca0f-135">訊息函數可在兩個資訊層級取得：</span><span class="sxs-lookup"><span data-stu-id="dca0f-135">Message functions are available at two information levels:</span></span>

-   [<span data-ttu-id="dca0f-136">**MSG \_ 資訊 \_ 0**</span><span class="sxs-lookup"><span data-stu-id="dca0f-136">**MSG\_INFO\_0**</span></span>](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_0)
-   [<span data-ttu-id="dca0f-137">**MSG \_ 資訊 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="dca0f-137">**MSG\_INFO\_1**</span></span>](/windows/desktop/api/Lmmsg/ns-lmmsg-msg_info_1)

<span data-ttu-id="dca0f-138">**MSG \_ INFO \_ 1** 資訊層級只存在於相容性。</span><span class="sxs-lookup"><span data-stu-id="dca0f-138">The **MSG\_INFO\_1** information level exists only for compatibility.</span></span> <span data-ttu-id="dca0f-139">Messenger 服務不會轉寄名稱或允許名稱轉寄給它。</span><span class="sxs-lookup"><span data-stu-id="dca0f-139">The messenger service does not forward names or allow names to be forwarded to it.</span></span>

 

 




