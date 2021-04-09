---
title: 註冊 COM 伺服器
description: 註冊 COM 伺服器
ms.assetid: aaa09a1b-deb8-424f-a911-ae22d39919d3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eefaa47d159d776a3c931ca48de0dd3161c29913
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104093336"
---
# <a name="registering-com-servers"></a><span data-ttu-id="c55fe-103">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="c55fe-103">Registering COM Servers</span></span>

<span data-ttu-id="c55fe-104">在程式碼中定義類別之後 (確定它會 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) 或 [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) 並指派 CLSID 給它，您必須將資訊放在登錄中，以允許 COM （要求用戶端具有 CLSID）建立其物件的實例。</span><span class="sxs-lookup"><span data-stu-id="c55fe-104">After you have defined a class in code (ensuring that it implements [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) or [**IClassFactory2**](/windows/desktop/api/OCIdl/nn-ocidl-iclassfactory2)) and assigned it a CLSID, you need to put information in the registry that will allow COM, on request of a client with the CLSID, to create instances of its objects.</span></span> <span data-ttu-id="c55fe-105">這項資訊會告訴系統，指定的 CLSID，也就是該類別的 DLL 或 EXE 程式碼所在的位置，以及其啟動方式。</span><span class="sxs-lookup"><span data-stu-id="c55fe-105">This information tells the system, for a given CLSID, where the DLL or EXE code for that class is located and how it is to be launched.</span></span>

<span data-ttu-id="c55fe-106">在登錄中註冊類別的方法不止一種。</span><span class="sxs-lookup"><span data-stu-id="c55fe-106">There is more than one way of registering a class in the registry.</span></span> <span data-ttu-id="c55fe-107">此外，還有其他方法可在執行的系統中「註冊」類別，讓系統知道正在執行的物件目前在系統中。</span><span class="sxs-lookup"><span data-stu-id="c55fe-107">In addition, there are other ways of "registering" a class with the system when it is running, so that the system is aware that a running object is currently in the system.</span></span>

<span data-ttu-id="c55fe-108">如需有關註冊的詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="c55fe-108">See the following topics for more information about registering:</span></span>

-   [<span data-ttu-id="c55fe-109">在安裝時註冊類別</span><span class="sxs-lookup"><span data-stu-id="c55fe-109">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
-   [<span data-ttu-id="c55fe-110">註冊正在執行的 EXE 伺服器</span><span class="sxs-lookup"><span data-stu-id="c55fe-110">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
-   [<span data-ttu-id="c55fe-111">在 ROT 中註冊物件</span><span class="sxs-lookup"><span data-stu-id="c55fe-111">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
-   [<span data-ttu-id="c55fe-112">自我註冊</span><span class="sxs-lookup"><span data-stu-id="c55fe-112">Self-Registration</span></span>](self-registration.md)
-   [<span data-ttu-id="c55fe-113">安裝為服務應用程式</span><span class="sxs-lookup"><span data-stu-id="c55fe-113">Installing as a Service Application</span></span>](installing-as-a-service-application.md)

## <a name="related-topics"></a><span data-ttu-id="c55fe-114">相關主題</span><span class="sxs-lookup"><span data-stu-id="c55fe-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c55fe-115">COM 伺服器責任</span><span class="sxs-lookup"><span data-stu-id="c55fe-115">COM Server Responsibilities</span></span>](com-server-responsibilities.md)
</dt> </dl>

 

 