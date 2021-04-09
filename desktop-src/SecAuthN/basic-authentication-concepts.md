---
description: 在用戶端/伺服器應用程式模型中，用戶端是代表需要完成某些工作之使用者的程式。
ms.assetid: c3e38cd3-3749-4384-80ff-0551acfe1eec
title: 基本驗證概念
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723cf42913906435c8dbc3c41950da8db8ece0ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114313"
---
# <a name="basic-authentication-concepts"></a><span data-ttu-id="5c4d1-103">基本驗證概念</span><span class="sxs-lookup"><span data-stu-id="5c4d1-103">Basic Authentication Concepts</span></span>

<span data-ttu-id="5c4d1-104">在用戶端/伺服器應用程式模型中，用戶端是代表需要完成某些工作之使用者的程式。</span><span class="sxs-lookup"><span data-stu-id="5c4d1-104">In a client/server application model, clients are programs acting on behalf of users who need something done.</span></span> <span data-ttu-id="5c4d1-105">這可能是開啟和使用檔案、存取信箱、查詢資料庫或列印檔案。</span><span class="sxs-lookup"><span data-stu-id="5c4d1-105">This might be opening and using a file, accessing a mailbox, querying a database, or printing a document.</span></span> <span data-ttu-id="5c4d1-106">伺服器是提供服務給用戶端的程式，例如檔案儲存體、郵件處理、查詢處理和列印幕後處理。</span><span class="sxs-lookup"><span data-stu-id="5c4d1-106">Servers are programs providing services to clients such as file storage, mail handling, query processing, and print spooling.</span></span> <span data-ttu-id="5c4d1-107">用戶端會起始動作，而伺服器會回應。</span><span class="sxs-lookup"><span data-stu-id="5c4d1-107">Clients initiate action, servers respond.</span></span> <span data-ttu-id="5c4d1-108">一般來說，伺服器會在通訊埠上接聽，等候用戶端連接並要求服務。</span><span class="sxs-lookup"><span data-stu-id="5c4d1-108">Typically, a server listens at a communications port waiting for clients to connect and ask for service.</span></span>

<span data-ttu-id="5c4d1-109">在 Kerberos 通訊協定模型中，每個用戶端/伺服器連接一開始都會進行驗證。</span><span class="sxs-lookup"><span data-stu-id="5c4d1-109">In the Kerberos protocol model, every client/server connection begins with authentication.</span></span> <span data-ttu-id="5c4d1-110">用戶端和伺服器會依次逐步執行一系列動作，向連接的兩端驗證對端是真的。</span><span class="sxs-lookup"><span data-stu-id="5c4d1-110">Client and server, in turn, step through a sequence of actions designed to verify to the party on each end of the connection that the party on the other end is genuine.</span></span> <span data-ttu-id="5c4d1-111">如果驗證成功，工作階段的安裝隨即完成且建立安全的用戶端/伺服器工作階段。</span><span class="sxs-lookup"><span data-stu-id="5c4d1-111">If authentication is successful, session setup completes and a secure client/server session is established.</span></span>

<span data-ttu-id="5c4d1-112">Kerberos 通訊協定利用：</span><span class="sxs-lookup"><span data-stu-id="5c4d1-112">The Kerberos protocol makes use of:</span></span>

-   [<span data-ttu-id="5c4d1-113">金鑰驗證</span><span class="sxs-lookup"><span data-stu-id="5c4d1-113">Key authentication</span></span>](key-authentication.md)
-   [<span data-ttu-id="5c4d1-114">驗證器訊息</span><span class="sxs-lookup"><span data-stu-id="5c4d1-114">Authenticator messages</span></span>](authenticator-messages.md)
-   [<span data-ttu-id="5c4d1-115">金鑰散發</span><span class="sxs-lookup"><span data-stu-id="5c4d1-115">Key distribution</span></span>](key-distribution.md)
-   [<span data-ttu-id="5c4d1-116">會話票證</span><span class="sxs-lookup"><span data-stu-id="5c4d1-116">Session tickets</span></span>](session-tickets.md)
-   [<span data-ttu-id="5c4d1-117">票證授權票證</span><span class="sxs-lookup"><span data-stu-id="5c4d1-117">Ticket-granting tickets</span></span>](ticket-granting-tickets.md)

 

 



