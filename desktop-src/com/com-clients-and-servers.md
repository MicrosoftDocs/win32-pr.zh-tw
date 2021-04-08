---
title: COM 用戶端和伺服器
description: COM 的重要層面是用戶端和伺服器之間的互動方式。
ms.assetid: 5d1d8613-3087-443d-8547-a767c8ba4959
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d7c3e29e4a4a3e2fcefe1c3473350d3423a8c24
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673512"
---
# <a name="com-clients-and-servers"></a><span data-ttu-id="2f0fe-103">COM 用戶端和伺服器</span><span class="sxs-lookup"><span data-stu-id="2f0fe-103">COM Clients and Servers</span></span>

<span data-ttu-id="2f0fe-104">COM 的重要層面是用戶端和伺服器之間的互動方式。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-104">A critical aspect of COM is how clients and servers interact.</span></span> <span data-ttu-id="2f0fe-105">*Com 用戶端* 是指任何程式碼或物件取得 COM 伺服器的指標，並藉由呼叫其介面的方法來使用其服務。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-105">A *COM client* is whatever code or object gets a pointer to a COM server and uses its services by calling the methods of its interfaces.</span></span> <span data-ttu-id="2f0fe-106">*COM 伺服器* 是提供服務給用戶端的任何物件;這些服務是 COM 介面實作為的形式，可讓能夠取得伺服器物件上其中一個介面指標的任何用戶端呼叫。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-106">A *COM server* is any object that provides services to clients; these services are in the form of COM interface implementations that can be called by any client that is able to get a pointer to one of the interfaces on the server object.</span></span>

<span data-ttu-id="2f0fe-107">有兩種主要類型的伺服器，同 *進程* 和跨 *進程*。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-107">There are two main types of servers, *in-process* and *out-of-process*.</span></span> <span data-ttu-id="2f0fe-108">同進程伺服器是在動態連結程式庫 (DLL) 中執行，而跨進程伺服器則是在可執行檔 (EXE) 中執行。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-108">In-process servers are implemented in a dynamic linked library (DLL), and out-of-process servers are implemented in an executable file (EXE).</span></span> <span data-ttu-id="2f0fe-109">跨進程伺服器可以位於本機電腦或遠端電腦上。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-109">Out-of-process servers can reside either on the local computer or on a remote computer.</span></span> <span data-ttu-id="2f0fe-110">此外，COM 也提供一種機制，可讓同進程伺服器 (DLL) 在代理 EXE 進程中執行，以取得能夠在遠端電腦上執行該處理常式的優點。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-110">In addition, COM provides a mechanism that allows an in-process server (a DLL) to run in a surrogate EXE process to gain the advantage of being able to run the process on a remote computer.</span></span> <span data-ttu-id="2f0fe-111">如需詳細資訊，請參閱 [DLL 代理](dll-surrogates.md)程式。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-111">For more information, see [DLL Surrogates](dll-surrogates.md).</span></span>

<span data-ttu-id="2f0fe-112">COM 程式設計模型和結構現在已經過擴充，因此 COM 用戶端和伺服器可以跨網路一起運作，而不只是在指定的電腦內。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-112">The COM programming model and constructs have now been extended so that COM clients and servers can work together across the network, not just within a given computer.</span></span> <span data-ttu-id="2f0fe-113">這可讓現有的應用程式與新的應用程式互動，並在具有適當管理的網路間彼此互動，而且可以撰寫新的應用程式來利用網路功能。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-113">This enables existing applications to interact with new applications and with each other across networks with proper administration, and new applications can be written to take advantage of networking features.</span></span>

<span data-ttu-id="2f0fe-114">COM 用戶端應用程式不需要知道伺服器物件的封裝方式、是否封裝為 Dll 中 (的同進程物件) ，或做為 Exe)  (的本機或遠端物件。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-114">COM client applications do not need to be aware of how server objects are packaged, whether they are packaged as in-process objects (in DLLs) or as local or remote objects (in EXEs).</span></span> <span data-ttu-id="2f0fe-115">分散式 COM 可進一步允許將物件封裝為服務應用程式，並以 Windows 的豐富系統管理和系統整合功能來同步處理 COM。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-115">Distributed COM further allows objects to be packaged as service applications, synchronizing COM with the rich administrative and system-integration capabilities of Windows.</span></span>

> [!Note]  
> <span data-ttu-id="2f0fe-116">在此檔中，會使用「縮寫」 COM 作為 DCOM 的喜好設定。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-116">Throughout this documentation the acronym COM is used in preference to DCOM.</span></span> <span data-ttu-id="2f0fe-117">這是因為 DCOM 不是分開的，它只是較長的網路的 COM。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-117">This is because DCOM is not separate;it is just COM with a longer wire.</span></span> <span data-ttu-id="2f0fe-118">如果所述的內容是遠端作業，則會使用 *分散式 COM* 一詞。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-118">In cases where what is being described is specifically a remote operation, the term *distributed COM* is used.</span></span>

 

<span data-ttu-id="2f0fe-119">COM 的設計目的是為了讓您能夠新增可延伸到網路的位置透明度支援。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-119">COM is designed to make it possible to add the support for location transparency that extends across a network.</span></span> <span data-ttu-id="2f0fe-120">它可讓針對單一電腦所撰寫的應用程式在網路上執行，並提供擴充這些功能的功能，並新增至網路所需的安全性。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-120">It allows applications written for single computers to run across a network and provides features that extend these capabilities and add to the security necessary in a network.</span></span> <span data-ttu-id="2f0fe-121"> (需詳細資訊，請參閱 [COM 中的安全性](security-in-com.md)) 。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-121">(For more information, see [Security in COM](security-in-com.md).)</span></span>

<span data-ttu-id="2f0fe-122">COM 會指定一種機制，讓許多不同的應用程式可以使用類別程式碼。</span><span class="sxs-lookup"><span data-stu-id="2f0fe-122">COM specifies a mechanism by which the class code can be used by many different applications.</span></span>

<span data-ttu-id="2f0fe-123">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="2f0fe-123">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="2f0fe-124">取得物件的指標</span><span class="sxs-lookup"><span data-stu-id="2f0fe-124">Getting a Pointer to an Object</span></span>](getting-a-pointer-to-an-object.md)
-   [<span data-ttu-id="2f0fe-125">透過類別物件建立物件</span><span class="sxs-lookup"><span data-stu-id="2f0fe-125">Creating an Object Through a Class Object</span></span>](creating-an-object-through-a-class-object.md)
-   [<span data-ttu-id="2f0fe-126">COM 伺服器責任</span><span class="sxs-lookup"><span data-stu-id="2f0fe-126">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
-   [<span data-ttu-id="2f0fe-127">持續性物件狀態</span><span class="sxs-lookup"><span data-stu-id="2f0fe-127">Persistent Object State</span></span>](persistent-object-state.md)
-   [<span data-ttu-id="2f0fe-128">提供類別資訊</span><span class="sxs-lookup"><span data-stu-id="2f0fe-128">Providing Class Information</span></span>](providing-class-information.md)
-   [<span data-ttu-id="2f0fe-129">物件間通訊</span><span class="sxs-lookup"><span data-stu-id="2f0fe-129">Inter-Object Communication</span></span>](inter-object-communication.md)

## <a name="related-topics"></a><span data-ttu-id="2f0fe-130">相關主題</span><span class="sxs-lookup"><span data-stu-id="2f0fe-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2f0fe-131">呼叫同步處理</span><span class="sxs-lookup"><span data-stu-id="2f0fe-131">Call Synchronization</span></span>](call-synchronization.md)
</dt> <dt>

[<span data-ttu-id="2f0fe-132">COM 中的安全性</span><span class="sxs-lookup"><span data-stu-id="2f0fe-132">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 




