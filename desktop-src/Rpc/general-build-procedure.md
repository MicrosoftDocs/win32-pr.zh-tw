---
title: 一般組建程式
description: 使用遠端程序呼叫建立用戶端/伺服器應用程式之進程的流覽頁面 (RPC) 。
ms.assetid: 77fa9f30-c370-4ec2-8c23-6037ec520dc3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b223bf7482cd7cbb65f5b737c90502a6b6dd3de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021323"
---
# <a name="general-build-procedure"></a><span data-ttu-id="824fa-103">一般組建程式</span><span class="sxs-lookup"><span data-stu-id="824fa-103">General Build Procedure</span></span>

<span data-ttu-id="824fa-104">使用 Microsoft RPC 建立用戶端/伺服器應用程式的程式如下：</span><span class="sxs-lookup"><span data-stu-id="824fa-104">The process for creating a client/server application using Microsoft RPC is:</span></span>

-   <span data-ttu-id="824fa-105">開發介面。</span><span class="sxs-lookup"><span data-stu-id="824fa-105">Develop the interface.</span></span>
-   <span data-ttu-id="824fa-106">開發執行介面的伺服器。</span><span class="sxs-lookup"><span data-stu-id="824fa-106">Develop the server that implements the interface.</span></span>
-   <span data-ttu-id="824fa-107">開發使用介面的用戶端。</span><span class="sxs-lookup"><span data-stu-id="824fa-107">Develop the client that uses the interface.</span></span>

<span data-ttu-id="824fa-108">下圖說明這些步驟。</span><span class="sxs-lookup"><span data-stu-id="824fa-108">The following figure illustrates these steps.</span></span>

![使用 microsoft rpc 建立用戶端-伺服器應用程式的流程](images/appdev.png)

<span data-ttu-id="824fa-110">同時開發用戶端和伺服器應用程式是可行的。</span><span class="sxs-lookup"><span data-stu-id="824fa-110">It is feasible and common to develop the client and server applications concurrently.</span></span> <span data-ttu-id="824fa-111">不過，由於用戶端和伺服器程式都相依于介面，因此必須在開發用戶端和伺服器之前開發它們之間的介面，如上圖所示。</span><span class="sxs-lookup"><span data-stu-id="824fa-111">Since both the client and server programs are dependent on the interface, however, the interface between them must be developed before the client and server are developed, as shown in the preceding diagram.</span></span>

<span data-ttu-id="824fa-112">本節討論使用 RPC 建立用戶端/伺服器應用程式所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="824fa-112">This section discusses the steps required for building a client/server application with RPC.</span></span> <span data-ttu-id="824fa-113">下列主題將提供此資訊：</span><span class="sxs-lookup"><span data-stu-id="824fa-113">The information is presented in the following topics:</span></span>

-   [<span data-ttu-id="824fa-114">開發介面</span><span class="sxs-lookup"><span data-stu-id="824fa-114">Developing the Interface</span></span>](developing-the-interface.md)
-   [<span data-ttu-id="824fa-115">開發伺服器</span><span class="sxs-lookup"><span data-stu-id="824fa-115">Developing the Server</span></span>](developing-the-server.md)
-   [<span data-ttu-id="824fa-116">開發用戶端</span><span class="sxs-lookup"><span data-stu-id="824fa-116">Developing the Client</span></span>](developing-the-client.md)

 

 




