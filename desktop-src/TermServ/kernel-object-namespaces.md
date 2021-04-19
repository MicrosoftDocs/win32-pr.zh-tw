---
title: 核心物件命名空間
description: 遠端桌面服務針對核心物件使用多個命名空間;全域命名空間主要是由用戶端/伺服器應用程式中的服務所使用。
ms.assetid: 771e0bbf-bd73-4e87-aa1e-945c1287b517
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 20680a32c8b35e3fa2f1ab15c732683d424550f0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106980279"
---
# <a name="kernel-object-namespaces"></a><span data-ttu-id="7852a-103">核心物件命名空間</span><span class="sxs-lookup"><span data-stu-id="7852a-103">Kernel object namespaces</span></span>

<span data-ttu-id="7852a-104">遠端桌面服務伺服器有多個命名空間，適用于下列命名核心物件：事件、信號、mutex、可等候計時器、檔案對應物件和工作物件。</span><span class="sxs-lookup"><span data-stu-id="7852a-104">A Remote Desktop Services server has multiple namespaces for the following named kernel objects: events, semaphores, mutexes, waitable timers, file-mapping objects, and job objects.</span></span> <span data-ttu-id="7852a-105">主要是由用戶端/伺服器應用程式中的服務所使用的全域命名空間。</span><span class="sxs-lookup"><span data-stu-id="7852a-105">There is a global namespace used primarily by services in client/server applications.</span></span> <span data-ttu-id="7852a-106">此外，每個用戶端會話對於這些物件都有個別的命名空間，例如在 Windows Vista 中。</span><span class="sxs-lookup"><span data-stu-id="7852a-106">In addition, each client session has a separate namespace for these objects, such as in Windows Vista.</span></span>

<span data-ttu-id="7852a-107">不同的用戶端會話命名空間可讓多個用戶端執行相同的應用程式，而不會干擾彼此。</span><span class="sxs-lookup"><span data-stu-id="7852a-107">The separate client session namespaces enable multiple clients to run the same applications without interfering with each other.</span></span> <span data-ttu-id="7852a-108">針對在用戶端會話下啟動的進程，系統預設會使用會話命名空間。</span><span class="sxs-lookup"><span data-stu-id="7852a-108">For processes started under a client session, the system uses the session namespace by default.</span></span> <span data-ttu-id="7852a-109">不過，這些進程可以在物件名稱前面加上 "Global" 前置詞，以使用全域命名空間 \\ 。</span><span class="sxs-lookup"><span data-stu-id="7852a-109">However, these processes can use the global namespace by prepending the "Global\\" prefix to the object name.</span></span> <span data-ttu-id="7852a-110">例如，下列程式碼會呼叫 [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) ，並在全域命名空間中建立名為 CSAPP 的事件物件：</span><span class="sxs-lookup"><span data-stu-id="7852a-110">For example, the following code calls [**CreateEvent**](/windows/desktop/api/synchapi/nf-synchapi-createeventa) and creates an event object named CSAPP in the global namespace:</span></span>

> [!Note]  
> <span data-ttu-id="7852a-111">全域命名空間不適用於 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="7852a-111">The global namespace is not available for Windows Store apps.</span></span>

 

`CreateEvent( NULL, FALSE, FALSE, "Global\\CSAPP" );`

<span data-ttu-id="7852a-112">遠端桌面服務環境中的服務應用程式預設會使用全域命名空間。</span><span class="sxs-lookup"><span data-stu-id="7852a-112">Service applications in a Remote Desktop Services environment use the global namespace by default.</span></span>

<span data-ttu-id="7852a-113">會話零隻用於裝載服務，且沒有主控台會話，與舊版 Windows 不同。</span><span class="sxs-lookup"><span data-stu-id="7852a-113">Session zero is only used for hosting services, and there is no console session, unlike previous versions of Windows.</span></span>

<span data-ttu-id="7852a-114">全域命名空間可讓多個用戶端會話上的進程與服務應用程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="7852a-114">The global namespace enables processes on multiple client sessions to communicate with a service application.</span></span> <span data-ttu-id="7852a-115">例如，用戶端/伺服器應用程式可能會使用 mutex 物件進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="7852a-115">For example, a client/server application might use a mutex object for synchronization.</span></span> <span data-ttu-id="7852a-116">伺服器模組可以在全域命名空間中建立 mutex 物件。</span><span class="sxs-lookup"><span data-stu-id="7852a-116">The server module can create the mutex object in the global namespace.</span></span> <span data-ttu-id="7852a-117">然後，用戶端會話可以使用 "Global \\ " 前置詞來開啟 mutex 物件。</span><span class="sxs-lookup"><span data-stu-id="7852a-117">Then a client session can use the "Global\\" prefix to open the mutex object.</span></span>

<span data-ttu-id="7852a-118">全域命名空間的另一個用法是，應用程式使用命名物件來偵測在所有會話的系統中已經有應用程式的實例。</span><span class="sxs-lookup"><span data-stu-id="7852a-118">Another use of the global namespace is for applications that use named objects to detect that there is already an instance of the application running in the system across all sessions.</span></span> <span data-ttu-id="7852a-119">您必須在全域命名空間中建立或開啟這個命名物件，而不是每個會話的命名空間。</span><span class="sxs-lookup"><span data-stu-id="7852a-119">This named object must be created or opened in the global namespace instead of the per-session namespace.</span></span> <span data-ttu-id="7852a-120">由於命名物件是在每個會話命名空間中建立，因此預設會支援每個會話執行一次應用程式的較常見案例。</span><span class="sxs-lookup"><span data-stu-id="7852a-120">The more common case of running the application once per session is supported by default because the named object is created in a per session namespace.</span></span>

<span data-ttu-id="7852a-121">除了 "Global \\ " 前置詞之外，用戶端進程還可以使用 "Local \\ " 前置詞，在其會話命名空間中明確建立物件。</span><span class="sxs-lookup"><span data-stu-id="7852a-121">In addition to the "Global\\" prefix, client processes can use the "Local\\" prefix to explicitly create an object in their session namespace.</span></span> <span data-ttu-id="7852a-122">這些關鍵字會區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="7852a-122">These keywords are case sensitive.</span></span>

<span data-ttu-id="7852a-123">「會話」 \\ 前置詞保留供系統使用，而且您不應該將它用於核心物件的名稱。</span><span class="sxs-lookup"><span data-stu-id="7852a-123">The "Session\\" prefix is reserved for system use and you should not use it in names of kernel objects.</span></span>

<span data-ttu-id="7852a-124">使用遠端桌面服務會話可執行快速切換使用者。</span><span class="sxs-lookup"><span data-stu-id="7852a-124">Fast user switching is implemented by using Remote Desktop Services sessions.</span></span> <span data-ttu-id="7852a-125">第一個登入的使用者會使用會話一，下一次登入的使用者會使用會話二，依此類推。</span><span class="sxs-lookup"><span data-stu-id="7852a-125">The first user to log on uses session one, the next user to log on uses session two, and so on.</span></span> <span data-ttu-id="7852a-126">核心物件名稱必須遵循遠端桌面服務所述的指導方針，讓應用程式能夠支援多個使用者。</span><span class="sxs-lookup"><span data-stu-id="7852a-126">Kernel object names must follow the guidelines outlined for Remote Desktop Services so that applications can support multiple users.</span></span>

<span data-ttu-id="7852a-127">從會話零以外的會話使用 [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga)，在全域命名空間中建立檔案對應物件是具有特殊許可權的作業。</span><span class="sxs-lookup"><span data-stu-id="7852a-127">The creation of a file-mapping object in the global namespace, by using [**CreateFileMapping**](/windows/desktop/api/winbase/nf-winbase-createfilemappinga), from a session other than session zero is a privileged operation.</span></span> <span data-ttu-id="7852a-128">因此，在任意遠端桌面工作階段主機 (RD 工作階段主機) 伺服器會話中執行的應用程式必須啟用 [SeCreateGlobalPrivilege](/windows/desktop/SecAuthZ/authorization-constants) ，才能成功地在全域命名空間中建立檔案對應物件。</span><span class="sxs-lookup"><span data-stu-id="7852a-128">Because of this, an application running in an arbitrary Remote Desktop Session Host (RD Session Host) server session must have [SeCreateGlobalPrivilege](/windows/desktop/SecAuthZ/authorization-constants) enabled in order to create a file-mapping object in the global namespace successfully.</span></span> <span data-ttu-id="7852a-129">許可權檢查僅限於建立檔案對應物件，並不適用于開啟現有的物件。</span><span class="sxs-lookup"><span data-stu-id="7852a-129">The privilege check is limited to the creation of file-mapping objects, and does not apply to opening existing ones.</span></span> <span data-ttu-id="7852a-130">例如，如果服務或系統建立檔案對應物件，則任何在任何會話中執行的進程都可以存取該檔案對應物件，前提是使用者具有必要的存取權。</span><span class="sxs-lookup"><span data-stu-id="7852a-130">For example, if a service or the system creates a file-mapping object, any process running in any session can access that file-mapping object provided that the user has the necessary access.</span></span>

 

 