---
title: 連接點
description: 連接點物件包含網路上可用的一或多個服務實例的相關資料。
ms.assetid: eb810e6d-c220-4a24-ae12-b12ace237413
ms.tgt_platform: multiple
keywords:
- 連接點廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5cc61c4c5b7dd74626ab1f3884ad403cfa20b843
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023277"
---
# <a name="connection-points"></a><span data-ttu-id="7aba4-104">連接點</span><span class="sxs-lookup"><span data-stu-id="7aba4-104">Connection Points</span></span>

<span data-ttu-id="7aba4-105">連接點物件包含網路上可用的一或多個服務實例的相關資料。</span><span class="sxs-lookup"><span data-stu-id="7aba4-105">A connection point object contains data about one or more instances of a service available on the network.</span></span> <span data-ttu-id="7aba4-106">[**ConnectionPoint**](/windows/desktop/ADSchema/c-connectionpoint)物件類別是抽象基類，代表 Active Directory Domain Services 中可連接資源的物件。</span><span class="sxs-lookup"><span data-stu-id="7aba4-106">The [**connectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) object class is the abstract base class from which objects representing connectable resources in Active Directory Domain Services are derived.</span></span> <span data-ttu-id="7aba4-107">下圖顯示衍生自 **connectionPoint** 物件類別的部分物件類別。</span><span class="sxs-lookup"><span data-stu-id="7aba4-107">The following illustration shows some of the object classes derived from the **connectionPoint** object class.</span></span>

![衍生自 connectionpoint 物件類別的物件類別](images/connection-points.png)

<span data-ttu-id="7aba4-109">下表列出 [**connectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) 類別的直屬子類別。</span><span class="sxs-lookup"><span data-stu-id="7aba4-109">The following table lists immediate subclasses of the [**connectionPoint**](/windows/desktop/ADSchema/c-connectionpoint) class.</span></span>



| <span data-ttu-id="7aba4-110">物件類別</span><span class="sxs-lookup"><span data-stu-id="7aba4-110">Object Class</span></span>                                                    | <span data-ttu-id="7aba4-111">Description</span><span class="sxs-lookup"><span data-stu-id="7aba4-111">Description</span></span>                                                                                                                                                                                                                                                                                                              |
|-----------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7aba4-112">**serviceConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="7aba4-112">**serviceConnectionPoint**</span></span>](/windows/desktop/ADSchema/c-serviceconnectionpoint) | <span data-ttu-id="7aba4-113">服務連接點 (SCP) 物件，用來發佈用戶端應用程式用來系結至服務的資料。</span><span class="sxs-lookup"><span data-stu-id="7aba4-113">Service connection point (SCP) objects for publishing data that client applications use to bind to a service.</span></span> <span data-ttu-id="7aba4-114">如需詳細資訊，請參閱 [使用服務連接點發行 (scp) ](publishing-with-service-connection-points.md)。</span><span class="sxs-lookup"><span data-stu-id="7aba4-114">For more information, see [Publishing with Service Connection Points (SCPs)](publishing-with-service-connection-points.md).</span></span>                                                                               |
| [<span data-ttu-id="7aba4-115">**rpcEntry**</span><span class="sxs-lookup"><span data-stu-id="7aba4-115">**rpcEntry**</span></span>](/windows/desktop/ADSchema/c-rpcentry)                             | <span data-ttu-id="7aba4-116">由 RPC 名稱服務使用子類別的抽象類別 (Ns) 透過 WIN32 API 中的 **RpcNs \*** 函式存取。</span><span class="sxs-lookup"><span data-stu-id="7aba4-116">An abstract class whose subclasses are used by the RPC Name Service (Ns) accessed through the **RpcNs\*** functions in the Win32 API.</span></span> <span data-ttu-id="7aba4-117">如需詳細資訊，請參閱 [使用 RPC 名稱服務發行 (RpcNs) ](publishing-with-the-rpc-name-service-rpcns.md)。</span><span class="sxs-lookup"><span data-stu-id="7aba4-117">For more information, see [Publishing with the RPC Name Service (RpcNs)](publishing-with-the-rpc-name-service-rpcns.md).</span></span>                                                          |
| [<span data-ttu-id="7aba4-118">**serviceInstance**</span><span class="sxs-lookup"><span data-stu-id="7aba4-118">**serviceInstance**</span></span>](/windows/desktop/ADSchema/c-serviceinstance)               | <span data-ttu-id="7aba4-119">Windows 通訊端註冊和解析所使用的連接點物件 (RnR) 名稱服務，可透過 Windows 套 **接字 \* WSA** api 存取。</span><span class="sxs-lookup"><span data-stu-id="7aba4-119">Connection point object used by the Windows Sockets Registration and Resolution (RnR) name service, accessed through the Windows Sockets **WSA\*** APIs.</span></span> <span data-ttu-id="7aba4-120">如需詳細資訊，請參閱 [使用 Windows 通訊端註冊和解析發行 (RnR) ](publishing-with-windows-sockets-registration-and-resolution.md)。</span><span class="sxs-lookup"><span data-stu-id="7aba4-120">For more information, see [Publishing with Windows Sockets Registration and Resolution (RnR)](publishing-with-windows-sockets-registration-and-resolution.md).</span></span> |
| [<span data-ttu-id="7aba4-121">**列印**</span><span class="sxs-lookup"><span data-stu-id="7aba4-121">**printQueue**</span></span>](/windows/desktop/ADSchema/c-printqueue)                         | <span data-ttu-id="7aba4-122">用來發佈網路印表機的連接點物件。</span><span class="sxs-lookup"><span data-stu-id="7aba4-122">Connection point object used to publish network printers.</span></span> <span data-ttu-id="7aba4-123">如需詳細資訊，請參閱 [**IADsPrintQueue**](/windows/desktop/api/iads/nn-iads-iadsprintqueue)。</span><span class="sxs-lookup"><span data-stu-id="7aba4-123">For more information, see [**IADsPrintQueue**](/windows/desktop/api/iads/nn-iads-iadsprintqueue).</span></span>                                                                                                                                                                                           |
| [<span data-ttu-id="7aba4-124">**體積**</span><span class="sxs-lookup"><span data-stu-id="7aba4-124">**volume**</span></span>](/windows/desktop/ADSchema/c-volume)                                 | <span data-ttu-id="7aba4-125">用來發行檔案服務的連接點物件。</span><span class="sxs-lookup"><span data-stu-id="7aba4-125">Connection point object used to publish file services.</span></span>                                                                                                                                                                                                                                                                   |



 

<span data-ttu-id="7aba4-126">請注意，以 COM 為基礎的服務不會使用連接點物件來通告本身。</span><span class="sxs-lookup"><span data-stu-id="7aba4-126">Be aware that COM-based services do not use connection-point objects to advertise themselves.</span></span> <span data-ttu-id="7aba4-127">這些服務會在類別存放區中發行。</span><span class="sxs-lookup"><span data-stu-id="7aba4-127">These services are published in the class store.</span></span> <span data-ttu-id="7aba4-128">Windows 2000 類別存放區是以目錄為基礎的存放庫，適用于所有以 COM 為基礎的應用程式、介面，以及提供應用程式發行和指派的 Api。</span><span class="sxs-lookup"><span data-stu-id="7aba4-128">The Windows 2000 class store is a directory-based repository for all COM-based applications, interfaces, and APIs that provide for application publishing and assigning.</span></span> <span data-ttu-id="7aba4-129">如需詳細資訊，請參閱 [發行 COM + 服務](publishing-com-services.md)。</span><span class="sxs-lookup"><span data-stu-id="7aba4-129">For more information, see [Publishing COM+ Services](publishing-com-services.md).</span></span>

 

 