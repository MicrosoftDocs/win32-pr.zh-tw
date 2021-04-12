---
title: 使用遠端桌面虛擬化 API
description: 開發人員可以使用此 API 來自訂 RD 連線代理人用來判斷連入用戶端連線最佳目的地的邏輯。
ms.assetid: b25eb87e-dac4-49ce-890e-b39c7e9e3408
ms.tgt_platform: multiple
keywords:
- 使用虛擬化 API 遠端桌面服務遠端桌面服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cda9ebfc014a2c8ec20d299bbb8be9183b25ce89
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375552"
---
# <a name="using-the-remote-desktop-virtualization-api"></a><span data-ttu-id="9c63b-104">使用遠端桌面虛擬化 API</span><span class="sxs-lookup"><span data-stu-id="9c63b-104">Using the Remote Desktop Virtualization API</span></span>

<span data-ttu-id="9c63b-105">終端機服務會話目錄 (TS 會話目錄) 角色服務可讓終端機伺服器將使用者和會話資訊儲存在稱為會話目錄的資料庫中。</span><span class="sxs-lookup"><span data-stu-id="9c63b-105">The Terminal Services Session Directory (TS  Session Directory) role service allows terminal servers to store user and session information in a database called a session directory.</span></span> <span data-ttu-id="9c63b-106">當使用者連線到伺服器陣列中的終端機伺服器時，TS 會話目錄會判斷使用者是否已在終端機伺服器上執行會話，如果是，則會將使用者重新導向至該終端機伺服器。</span><span class="sxs-lookup"><span data-stu-id="9c63b-106">When a user connects to a terminal server in a farm, TS Session Directory determines whether the user already has a session running on a terminal server and if so, it redirects the user to that terminal server.</span></span>

<span data-ttu-id="9c63b-107">在 Windows Server 2008 中，TS 會話目錄角色服務已展開並重新命名為「終端機服務會話代理人」 (TS 會話代理程式) 。</span><span class="sxs-lookup"><span data-stu-id="9c63b-107">In Windows Server 2008, the TS Session Directory role service was expanded and renamed Terminal Services Session Broker (TS Session Broker).</span></span> <span data-ttu-id="9c63b-108">除了維護現有會話的目錄之外，TS 會話代理人也可以 Broker 連入連線。</span><span class="sxs-lookup"><span data-stu-id="9c63b-108">In addition to maintaining a directory of existing sessions, TS Session Broker can also broker incoming connections.</span></span> <span data-ttu-id="9c63b-109">當 TS 會話代理人接收來自使用者的連入連線時，它會檢查其資料庫，以判斷使用者是否在終端機伺服器上有現有的會話。</span><span class="sxs-lookup"><span data-stu-id="9c63b-109">When TS Session Broker receives an incoming connection from a user, it checks its database to determine whether the user has an existing session on a terminal server.</span></span> <span data-ttu-id="9c63b-110">如果是，TS 會話代理人會將連線重新導向至相同的終端機伺服器。</span><span class="sxs-lookup"><span data-stu-id="9c63b-110">If so, TS Session Broker redirects the connection to that same terminal server.</span></span> <span data-ttu-id="9c63b-111">如果沒有，則 TS 會話代理人會判斷哪一個終端機伺服器的連線最少，並將連接重新導向至該伺服器。</span><span class="sxs-lookup"><span data-stu-id="9c63b-111">If not, TS Session Broker determines which terminal server has the fewest connections and redirects the connection to that server.</span></span>

<span data-ttu-id="9c63b-112">從 Windows Server 2008 開始，Microsoft 也發行了公用應用程式開發介面， (API) 來監視和與終端機伺服器上的會話互動。</span><span class="sxs-lookup"><span data-stu-id="9c63b-112">Beginning with Windows Server 2008, Microsoft also released a public application programming interface (API) for monitoring and interacting with sessions on terminal servers.</span></span> <span data-ttu-id="9c63b-113">[遠端桌面連線代理人外掛程式參考](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)中會說明此 API。</span><span class="sxs-lookup"><span data-stu-id="9c63b-113">This API is described in [Remote Desktop Connection Broker Plug-in Reference](/windows/desktop/TermServ/terminal-services-virtualization-api-reference).</span></span> <span data-ttu-id="9c63b-114">開發人員可以使用此 API 來建立自訂原則外掛程式，以覆寫 TS 會話代理人的標準重新導向邏輯。</span><span class="sxs-lookup"><span data-stu-id="9c63b-114">Using this API, developers can create custom policy plug-ins that override the standard redirection logic of TS Session Broker.</span></span> <span data-ttu-id="9c63b-115">自訂外掛程式可將會話重新導向到終端機伺服器，以及虛擬機器、虛擬桌面、blade 伺服器和實體桌面。</span><span class="sxs-lookup"><span data-stu-id="9c63b-115">The custom plug-ins can redirect sessions to terminal servers, as well as virtual machines, virtual desktops, blade servers, and physical desktops.</span></span>

<span data-ttu-id="9c63b-116">在 Windows Server 2008 R2 中，遠端桌面連線代理人 (RD 連線代理人)  (先前稱為「TS 會話代理人) 」的架構已擴充為支援虛擬機器的連線。</span><span class="sxs-lookup"><span data-stu-id="9c63b-116">In Windows Server 2008 R2, the architecture of Remote Desktop Connection Broker (RD Connection Broker) (formerly known as TS Session Broker) was expanded to support connections to virtual machines.</span></span> <span data-ttu-id="9c63b-117">新的架構可透過遠端桌面虛擬化 API 支援虛擬機器的會話管理。</span><span class="sxs-lookup"><span data-stu-id="9c63b-117">The new architecture supports session management for virtual machines through the Remote Desktop Virtualization API.</span></span> <span data-ttu-id="9c63b-118">開發人員可以使用此 API 來自訂 RD 連線代理人用來判斷連入用戶端連線最佳目的地的邏輯。</span><span class="sxs-lookup"><span data-stu-id="9c63b-118">Developers can use this API to customize the logic that RD Connection Broker uses to determine the best destination for an incoming client connection.</span></span>

<span data-ttu-id="9c63b-119">遠端桌面虛擬化 API 為開發人員提供了多項優點：</span><span class="sxs-lookup"><span data-stu-id="9c63b-119">Remote Desktop Virtualization API offers several benefits to developers:</span></span>

-   <span data-ttu-id="9c63b-120">使用實體終端機伺服器的介面類別似于使用虛擬機器的介面。</span><span class="sxs-lookup"><span data-stu-id="9c63b-120">The interfaces for working with physical terminal servers are similar to those for working with virtual machines.</span></span>
-   <span data-ttu-id="9c63b-121">開發人員可以取代所有或部分的標準重新導向邏輯。</span><span class="sxs-lookup"><span data-stu-id="9c63b-121">Developers can replace all or part of the standard redirection logic.</span></span> <span data-ttu-id="9c63b-122">開發人員可以建立產品隨附的程式碼，而不需要從頭開始撰寫所有專案。</span><span class="sxs-lookup"><span data-stu-id="9c63b-122">Developers can build on the code that ships with the product and do not have to write everything from scratch.</span></span>
-   <span data-ttu-id="9c63b-123">管理伺服器或會話中不需要其他管理代理程式。</span><span class="sxs-lookup"><span data-stu-id="9c63b-123">No additional management agent is required on the managing server or within the session.</span></span>
-   <span data-ttu-id="9c63b-124">仍支援為了與 Windows Server 2008 一起使用而開發的 TS 會話代理人外掛程式。</span><span class="sxs-lookup"><span data-stu-id="9c63b-124">TS Session Broker plug-ins developed for use with Windows Server 2008 are still supported.</span></span>
-   <span data-ttu-id="9c63b-125">此 API 也可讓開發人員建立使用者介面，以管理遠端桌面工作階段主機 (RD 工作階段主機) 伺服器 (先前稱為「終端機伺服器」 ) 和虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="9c63b-125">The API also allows developers to create user interfaces for administration of both Remote Desktop Session Host (RD Session Host) servers (formerly known as "terminal servers") and virtual machines.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9c63b-126">相關主題</span><span class="sxs-lookup"><span data-stu-id="9c63b-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c63b-127">遠端桌面虛擬化 API 參考</span><span class="sxs-lookup"><span data-stu-id="9c63b-127">Remote Desktop Virtualization API Reference</span></span>](terminal-services-virtualization-api-reference.md)
</dt> <dt>

[<span data-ttu-id="9c63b-128">遠端桌面連線代理人外掛程式參考</span><span class="sxs-lookup"><span data-stu-id="9c63b-128">Remote Desktop Connection Broker Plug-in Reference</span></span>](/windows/desktop/TermServ/terminal-services-virtualization-api-reference)
</dt> </dl>

 

 