---
title: 在安裝時註冊類別
description: 如果某個類別打算隨時供用戶端使用，則在大部分的應用程式中，您通常會透過安裝和安裝程式進行註冊。
ms.assetid: 6d78c2ce-56d8-4866-9801-35125ec9cac4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4253c40cb3feb7e737368c947c0b20715f5becbd
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104316552"
---
# <a name="registering-a-class-at-installation"></a><span data-ttu-id="27209-103">在安裝時註冊類別</span><span class="sxs-lookup"><span data-stu-id="27209-103">Registering a Class at Installation</span></span>

<span data-ttu-id="27209-104">如果某個類別打算隨時供用戶端使用，則在大部分的應用程式中，您通常會透過安裝和安裝程式進行註冊。</span><span class="sxs-lookup"><span data-stu-id="27209-104">If a class is intended to be available to clients at any time, as most applications are, you usually register it through an installation and setup program.</span></span> <span data-ttu-id="27209-105">這表示將應用程式的相關資訊放入登錄中，包括將應用程式的物件具現化的方式和位置。</span><span class="sxs-lookup"><span data-stu-id="27209-105">This means putting information about the application into the registry, including how and where its objects are to be instantiated.</span></span> <span data-ttu-id="27209-106">這是所有 Clsid 都必須註冊的資訊。</span><span class="sxs-lookup"><span data-stu-id="27209-106">This information must be registered for all CLSIDs.</span></span> <span data-ttu-id="27209-107">其他資訊則為選擇性。</span><span class="sxs-lookup"><span data-stu-id="27209-107">Other information is optional.</span></span> <span data-ttu-id="27209-108">Regsvr32 之類的工具可讓您輕鬆地撰寫安裝程式，以便在安裝時註冊伺服器。</span><span class="sxs-lookup"><span data-stu-id="27209-108">Tools such as Regsvr32 make it simple to write a setup program that registers servers at installation.</span></span>

<span data-ttu-id="27209-109">如果您不依賴系統預設值，登錄中會有兩個重要的金鑰： CLSID 和 AppID。</span><span class="sxs-lookup"><span data-stu-id="27209-109">If you are not relying on system defaults, there are two important keys in the registry: the CLSID and the AppID.</span></span> <span data-ttu-id="27209-110">這些機碼底下的重要資訊片段是物件的具現化方式。</span><span class="sxs-lookup"><span data-stu-id="27209-110">Among the important pieces of information under these keys is how the object is to be instantiated.</span></span> <span data-ttu-id="27209-111">物件可以指定為同進程、跨進程的本機或跨進程的遠端。</span><span class="sxs-lookup"><span data-stu-id="27209-111">Objects can be designated as in-process, out-of-process local, or out-of-process remote.</span></span>

<span data-ttu-id="27209-112">AppID 金鑰底下有幾個值，可定義該應用程式的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="27209-112">Under the AppID key are several values that define information specific to that application.</span></span> <span data-ttu-id="27209-113">這些都是 [RemoteServerName](remoteservername.md) 和 [ActivateAtStorage](activateatstorage.md)，這兩者都可以用來允許用戶端建立物件，而用戶端則沒有伺服器位置的內建知識。</span><span class="sxs-lookup"><span data-stu-id="27209-113">Among these are [RemoteServerName](remoteservername.md) and [ActivateAtStorage](activateatstorage.md), both of which can be used to permit a client to create an object, with the client having no built-in knowledge of the location of the server.</span></span> <span data-ttu-id="27209-114"> (如需有關遠端具現化的詳細資訊，請參閱 [尋找遠端物件](locating-a-remote-object.md) 和 [實例建立](instance-creation-helper-functions.md)協助程式函數。 ) </span><span class="sxs-lookup"><span data-stu-id="27209-114">(For more information about remote instantiation, see [Locating a Remote Object](locating-a-remote-object.md) and [Instance Creation Helper Functions](instance-creation-helper-functions.md).)</span></span>

<span data-ttu-id="27209-115">伺服器也可以安裝為服務，或是在特定使用者帳戶下執行。</span><span class="sxs-lookup"><span data-stu-id="27209-115">A server can also be installed as a service, or to run under a specific user account.</span></span> <span data-ttu-id="27209-116">如需詳細資訊，請參閱 [安裝為服務應用程式](installing-as-a-service-application.md)。</span><span class="sxs-lookup"><span data-stu-id="27209-116">For more information, see [Installing as a Service Application](installing-as-a-service-application.md).</span></span>

<span data-ttu-id="27209-117">不是服務或在特定使用者帳戶下執行的伺服器或 ROT 物件可以稱為「啟動為啟動項」伺服器。</span><span class="sxs-lookup"><span data-stu-id="27209-117">A server or ROT object that is not a service or running under a specific user account can be referred to as an "activate as activator" server.</span></span> <span data-ttu-id="27209-118">針對這些伺服器，安全性內容和用戶端的視窗工作站/桌面必須符合伺服器的。</span><span class="sxs-lookup"><span data-stu-id="27209-118">For these servers, the security context and the window station/desktop of the client must match the server's.</span></span> <span data-ttu-id="27209-119">嘗試連接到遠端伺服器的用戶端會被視為具有 **Null** 視窗工作站/桌上型電腦，因此在此實例中只會比較伺服器安全性內容。</span><span class="sxs-lookup"><span data-stu-id="27209-119">A client attempting to connect to a remote server is considered to have a **NULL** window station/desktop, so only the server security context is compared in this instance.</span></span> <span data-ttu-id="27209-120"> (如需 Sid 的詳細資訊，請參閱 [com 中的安全性](security-in-com.md)。 ) com 會在進程第一次連接到分散式 COM 服務時，快取進程的視窗站/桌面。</span><span class="sxs-lookup"><span data-stu-id="27209-120">(For more information about SIDs, see [Security in COM](security-in-com.md).) COM caches the window station/desktop of a process when the process first connects to the distributed COM service.</span></span> <span data-ttu-id="27209-121">因此，在呼叫 [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) 或 [**COINITIALIZEEX**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex)之後，COM 用戶端和伺服器不應該變更進程的視窗工作站或執行緒桌面。</span><span class="sxs-lookup"><span data-stu-id="27209-121">Therefore, COM clients and servers should not change their window station or thread desktops of the process after calling [**CoInitialize**](/windows/desktop/api/Objbase/nf-objbase-coinitialize) or [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span>

<span data-ttu-id="27209-122">當類別註冊為同進程時，COM 會將 [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) 的呼叫自動傳遞至 [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) 函式，該函式必須實作為呼叫物件，以提供其類別物件的指標。</span><span class="sxs-lookup"><span data-stu-id="27209-122">When a class is registered as in-process, a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) to create its class object is automatically passed by COM to the [**DllGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-dllgetclassobject) function, which the class must implement to give the calling object a pointer to its class object.</span></span>

<span data-ttu-id="27209-123">在可執行檔中執行的類別可指定 COM 應執行其進程，並等候進程透過呼叫 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject)函式來註冊其類別物件的 [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)介面。</span><span class="sxs-lookup"><span data-stu-id="27209-123">Classes implemented in executables can specify that COM should execute their process and wait for the process to register their class object's [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) interface through a call to the [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) function.</span></span>

## <a name="related-topics"></a><span data-ttu-id="27209-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="27209-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="27209-125">COM 登錄機碼</span><span class="sxs-lookup"><span data-stu-id="27209-125">COM Registry Keys</span></span>](com-registry-keys.md)
</dt> <dt>

[<span data-ttu-id="27209-126">安裝為服務應用程式</span><span class="sxs-lookup"><span data-stu-id="27209-126">Installing as a Service Application</span></span>](installing-as-a-service-application.md)
</dt> <dt>

[<span data-ttu-id="27209-127">註冊正在執行的 EXE 伺服器</span><span class="sxs-lookup"><span data-stu-id="27209-127">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="27209-128">註冊元件</span><span class="sxs-lookup"><span data-stu-id="27209-128">Registering Components</span></span>](registering-components.md)
</dt> <dt>

[<span data-ttu-id="27209-129">在 ROT 中註冊物件</span><span class="sxs-lookup"><span data-stu-id="27209-129">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="27209-130">自我註冊</span><span class="sxs-lookup"><span data-stu-id="27209-130">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 