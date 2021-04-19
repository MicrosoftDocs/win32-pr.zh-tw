---
description: 通訊端網路應用程式有兩種不同的類型：伺服器和用戶端。
ms.assetid: 05e42384-1746-462d-82c7-8df848b4525e
title: 關於伺服器和用戶端
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a951d23ba1c6ad4f0f5ffd1f674b056a36c3f8dd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989914"
---
# <a name="about-servers-and-clients"></a><span data-ttu-id="b1e1f-103">關於伺服器和用戶端</span><span class="sxs-lookup"><span data-stu-id="b1e1f-103">About Servers and Clients</span></span>

<span data-ttu-id="b1e1f-104">通訊端網路應用程式有兩種不同的類型：伺服器和用戶端。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-104">There are two distinct types of socket network applications: Server and Client.</span></span>

<span data-ttu-id="b1e1f-105">伺服器和用戶端有不同的行為;因此，建立它們的程式不同。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-105">Servers and Clients have different behaviors; therefore, the process of creating them is different.</span></span> <span data-ttu-id="b1e1f-106">接下來是建立串流 TCP/IP 伺服器和用戶端的一般模型。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-106">What follows is the general model for creating a streaming TCP/IP Server and Client.</span></span>

## <a name="server"></a><span data-ttu-id="b1e1f-107">伺服器</span><span class="sxs-lookup"><span data-stu-id="b1e1f-107">Server</span></span>

1.  <span data-ttu-id="b1e1f-108">初始化 Winsock。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-108">Initialize Winsock.</span></span>
2.  <span data-ttu-id="b1e1f-109">建立通訊端。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-109">Create a socket.</span></span>
3.  <span data-ttu-id="b1e1f-110">系結通訊端。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-110">Bind the socket.</span></span>
4.  <span data-ttu-id="b1e1f-111">在用戶端上接聽通訊端。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-111">Listen on the socket for a client.</span></span>
5.  <span data-ttu-id="b1e1f-112">接受來自用戶端的連接。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-112">Accept a connection from a client.</span></span>
6.  <span data-ttu-id="b1e1f-113">接收和傳送資料。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-113">Receive and send data.</span></span>
7.  <span data-ttu-id="b1e1f-114">中斷連線。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-114">Disconnect.</span></span>

## <a name="client"></a><span data-ttu-id="b1e1f-115">用戶端</span><span class="sxs-lookup"><span data-stu-id="b1e1f-115">Client</span></span>

1.  <span data-ttu-id="b1e1f-116">初始化 Winsock。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-116">Initialize Winsock.</span></span>
2.  <span data-ttu-id="b1e1f-117">建立通訊端。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-117">Create a socket.</span></span>
3.  <span data-ttu-id="b1e1f-118">連接至伺服器。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-118">Connect to the server.</span></span>
4.  <span data-ttu-id="b1e1f-119">傳送和接收資料。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-119">Send and receive data.</span></span>
5.  <span data-ttu-id="b1e1f-120">中斷連線。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-120">Disconnect.</span></span>

> [!Note]  
> <span data-ttu-id="b1e1f-121">用戶端和伺服器的部分步驟是相同的。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-121">Some of the steps are the same for a client and a server.</span></span> <span data-ttu-id="b1e1f-122">這些步驟的執行方式幾乎完全相同。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-122">These steps are implemented almost exactly alike.</span></span> <span data-ttu-id="b1e1f-123">本指南中的某些步驟將會特定于所建立的應用程式類型。</span><span class="sxs-lookup"><span data-stu-id="b1e1f-123">Some of the steps in this guide will be specific to the type of application being created.</span></span>

 

<span data-ttu-id="b1e1f-124">第一個步驟： [建立基本 Winsock 應用程式](creating-a-basic-winsock-application.md)</span><span class="sxs-lookup"><span data-stu-id="b1e1f-124">First Step: [Creating a Basic Winsock Application](creating-a-basic-winsock-application.md)</span></span>

## <a name="related-topics"></a><span data-ttu-id="b1e1f-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="b1e1f-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b1e1f-126">使用 Winsock 開始使用</span><span class="sxs-lookup"><span data-stu-id="b1e1f-126">Getting Started With Winsock</span></span>](getting-started-with-winsock.md)
</dt> </dl>

 

 



