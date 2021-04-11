---
description: 以標準使用者的形式執行的應用程式會使用遠端程序呼叫（ (RPC) ）與以系統執行的服務進行通訊。
ms.assetid: c0bcebe3-f7eb-471f-a21d-5840d2e26729
title: 作業系統服務模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ce545c60da8e480247c8fc8b02cfc01e4487340
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944635"
---
# <a name="operating-system-service-model"></a><span data-ttu-id="3c6c4-103">作業系統服務模型</span><span class="sxs-lookup"><span data-stu-id="3c6c4-103">Operating System Service Model</span></span>

<span data-ttu-id="3c6c4-104">在作業系統服務模型中，以標準使用者的形式執行的應用程式會使用 [遠端程序呼叫](/windows/desktop/Rpc/rpc-start-page)（ (RPC) ）與以 **系統** 執行的服務進行通訊。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-104">In the operating system service model, an application running as a standard user communicates with a service running as **SYSTEM** by using [Remote Procedure Call](/windows/desktop/Rpc/rpc-start-page) (RPC).</span></span>

<span data-ttu-id="3c6c4-105">標準使用者應用程式會在應用程式資訊清單中標示為並無 requestedexecutionlevel **asInvoker**。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-105">The standard user application is marked in the application manifest with a **requestedExecutionLevel** of **asInvoker**.</span></span> <span data-ttu-id="3c6c4-106">若要執行需要系統管理員許可權的作業，標準使用者應用程式會對服務提出要求。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-106">To perform an operation that requires administrator privilege, the standard user application makes a request to the service.</span></span>

<span data-ttu-id="3c6c4-107">作業系統服務模型的其中一種用途是管理可能會影響系統的應用程式，例如防毒軟體或其他垃圾軟體和間諜軟體。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-107">One use for the operating system service model is to manage applications that could impact the system, such as antivirus or other unwanted software and spyware.</span></span> <span data-ttu-id="3c6c4-108">標準使用者應用程式可讓登入的使用者控制服務的某些層面。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-108">The standard user application allows the logged on user to control some aspects of the service.</span></span> <span data-ttu-id="3c6c4-109">此服務負責判斷它針對標準使用者應用程式所執行的作業。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-109">The service is responsible for determining which operations it performs for a standard user application.</span></span> <span data-ttu-id="3c6c4-110">例如，防毒軟體服務可能會允許標準使用者啟動系統掃描，但可能不允許標準使用者停用即時病毒檢查。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-110">For example, an antivirus service might allow a standard user to start a scan of the system, but it might not allow a standard user to disable real-time virus checking.</span></span>

<span data-ttu-id="3c6c4-111">使用作業系統服務模型的主要優點是不需要提高許可權提示。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-111">A major benefit of using the operating system service model is that no elevation prompting is required.</span></span>

<span data-ttu-id="3c6c4-112">使用作業系統服務模型的其中一個缺點，就是在系統上執行的服務所使用的資源比工作還多，而且標準使用者無法停止服務。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-112">One drawback of using the operating system service model is that a service running on the system uses more resources than a task, and a service cannot be stopped by a standard user.</span></span> <span data-ttu-id="3c6c4-113">如果尾碼，請考慮使用 [提升許可權](elevated-task-model.md) 的工作模型。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-113">Consider using the [Elevated Task Model](elevated-task-model.md) if it suffices.</span></span>

<span data-ttu-id="3c6c4-114">若要執行作業系統服務模型，請建立標準使用者用戶端應用程式和作業系統服務。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-114">To implement the operating system service model, create a standard user client application and an operating system service.</span></span> <span data-ttu-id="3c6c4-115">在產品安裝期間，于作業系統中安裝此服務。</span><span class="sxs-lookup"><span data-stu-id="3c6c4-115">Install the service in the operating system during product installation time.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3c6c4-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="3c6c4-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c6c4-117">開發需要系統管理員許可權的應用程式</span><span class="sxs-lookup"><span data-stu-id="3c6c4-117">Developing Applications that Require Administrator Privilege</span></span>](developing-applications-that-require-administrator-privilege.md)
</dt> <dt>

[<span data-ttu-id="3c6c4-118">系統管理員訊息代理程式模型</span><span class="sxs-lookup"><span data-stu-id="3c6c4-118">Administrator Broker Model</span></span>](administrator-broker-model.md)
</dt> <dt>

[<span data-ttu-id="3c6c4-119">系統管理員 COM 物件模型</span><span class="sxs-lookup"><span data-stu-id="3c6c4-119">Administrator COM Object Model</span></span>](administrator-com-object-model.md)
</dt> <dt>

[<span data-ttu-id="3c6c4-120">提高許可權的工作模型</span><span class="sxs-lookup"><span data-stu-id="3c6c4-120">Elevated Task Model</span></span>](elevated-task-model.md)
</dt> </dl>

 

 
