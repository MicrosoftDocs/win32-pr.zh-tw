---
title: 安裝為服務應用程式
description: 安裝為服務應用程式
ms.assetid: 0dd4b348-3d12-49ba-8098-4adb9df01a0e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ed5c474d73c74b3be40bae773c3d51eadf6c69a
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104024140"
---
# <a name="installing-as-a-service-application"></a><span data-ttu-id="9693c-103">安裝為服務應用程式</span><span class="sxs-lookup"><span data-stu-id="9693c-103">Installing as a Service Application</span></span>

<span data-ttu-id="9693c-104">除了以本機伺服器可執行檔的形式執行 (EXE) ，COM 物件也可以自行封裝，以便在本機或遠端用戶端啟動時，以服務應用程式的形式執行。</span><span class="sxs-lookup"><span data-stu-id="9693c-104">In addition to running as a local server executable (EXE), a COM object may also package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="9693c-105">服務支援許多有用和使用者 interfaceâ的「整合式系統管理功能，包括本機和遠端啟動、停止、暫停和重新開機，以及建立伺服器以在特定 [使用者帳戶](/windows/desktop/Services/service-user-accounts) 和 [視窗工作站](/windows/desktop/winstation/window-stations)上執行的能力。</span><span class="sxs-lookup"><span data-stu-id="9693c-105">Services support numerous useful and user interfaceâ€“integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific [user account](/windows/desktop/Services/service-user-accounts) and [window station](/windows/desktop/winstation/window-stations).</span></span>

<span data-ttu-id="9693c-106">以服務方式撰寫的物件會透過在其[AppID](appid-key.md)金鑰底下建立[LocalService](localservice.md)值並執行標準服務安裝，來安裝供 COM 使用。</span><span class="sxs-lookup"><span data-stu-id="9693c-106">An object written as a service is installed for use by COM by establishing a [LocalService](localservice.md) value under its [AppID](appid-key.md) key and performing a standard service installation.</span></span>

<span data-ttu-id="9693c-107">當遠端用戶端啟動時，類別也可以設定為在特定使用者帳戶下執行，而不需要撰寫為服務應用程式。</span><span class="sxs-lookup"><span data-stu-id="9693c-107">Classes may also be configured to run under a specific user account when activated by a remote client without being written as a service application.</span></span> <span data-ttu-id="9693c-108">若要這樣做，類別會安裝當 SCM 啟動其本機伺服器進程時要使用的使用者名稱和密碼。</span><span class="sxs-lookup"><span data-stu-id="9693c-108">To do this, the class installs a user name and a password to be used when the SCM launches its local server process.</span></span>

<span data-ttu-id="9693c-109">以這種方式設定類別時，除非 COM 會代表實際的啟用要求啟動進程，否則使用此 CLSID 呼叫 [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="9693c-109">When a class is configured in this fashion, calls to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) with this CLSID will fail unless the process was launched by COM on behalf of an actual activation request.</span></span> <span data-ttu-id="9693c-110">換句話說，設定為以特定使用者身分執行的類別，可能無法在任何其他身分識別下註冊。</span><span class="sxs-lookup"><span data-stu-id="9693c-110">In other words, classes configured to run as a particular user may not be registered under any other identity.</span></span>

<span data-ttu-id="9693c-111">使用者名稱是取自類別的 APPID 金鑰底下的 [RunAs](runas.md) 命名值。</span><span class="sxs-lookup"><span data-stu-id="9693c-111">The user name is taken from the [RunAs](runas.md) named-value under the class's APPID key.</span></span> <span data-ttu-id="9693c-112">如果使用者名稱為「互動式使用者」，則類別程式碼會在目前登入之使用者的安全性內容中執行，並連接到互動式視窗工作站。</span><span class="sxs-lookup"><span data-stu-id="9693c-112">If the user name is "Interactive User", the class code is run in the security context of the currently logged on user and is connected to the interactive window station.</span></span>

<span data-ttu-id="9693c-113">否則，系統會從登錄的隱藏部分取得密碼，而只提供給電腦的系統管理員和系統的系統管理員。</span><span class="sxs-lookup"><span data-stu-id="9693c-113">Otherwise, the password is retrieved from a hidden portion of the registry available only to administrators of the machine and to the system.</span></span> <span data-ttu-id="9693c-114">接著會使用使用者名稱和密碼來建立執行類別程式碼的登入會話。</span><span class="sxs-lookup"><span data-stu-id="9693c-114">The user name and password are then used to create a logon session in which the class code is run.</span></span> <span data-ttu-id="9693c-115">以這種方式啟動時，類別程式碼會以自己的桌面和視窗來執行，且不會與互動式使用者或其他使用者帳戶中執行的其他類別共用視窗控制碼、剪貼簿或其他使用者介面元素。</span><span class="sxs-lookup"><span data-stu-id="9693c-115">When launched in this way, the class code runs with its own desktop and window-station and does not share window handles, the clipboard, or other user interface elements with the interactive user or other classes running in other user accounts.</span></span>

<span data-ttu-id="9693c-116">使用 **LocalService** 或 **RunAs** 註冊的伺服器，可以在執行中的物件資料表中註冊物件，以允許任何用戶端連接到該物件。</span><span class="sxs-lookup"><span data-stu-id="9693c-116">A server registered either with **LocalService** or **RunAs** can register an object in the running object table to allow any client to connect to it.</span></span> <span data-ttu-id="9693c-117">若要這樣做，伺服器對 [**IRunningObjectTable：： Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) 的呼叫必須設定 ROTFLAGS \_ ALLOWANYCLIENT 旗標。</span><span class="sxs-lookup"><span data-stu-id="9693c-117">To do so, the server's call to [**IRunningObjectTable::Register**](/windows/desktop/api/ObjIdl/nf-objidl-irunningobjecttable-register) must set the ROTFLAGS\_ALLOWANYCLIENT flag.</span></span> <span data-ttu-id="9693c-118">在參考可執行檔之 AppID 的登錄的 AppID 區段中，伺服器設定此位必須有其可執行檔名稱。</span><span class="sxs-lookup"><span data-stu-id="9693c-118">A server setting this bit must have its executable name in the AppID section of the registry that refers to the AppID for the executable.</span></span> <span data-ttu-id="9693c-119">"Activate as activator" 伺服器 (未註冊為 **LocalService** 或 **RunAs**) 可能不會使用此旗標注冊物件。</span><span class="sxs-lookup"><span data-stu-id="9693c-119">An "activate as activator" server (not registered as either **LocalService** or **RunAs**) may not register an object with this flag.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9693c-120">相關主題</span><span class="sxs-lookup"><span data-stu-id="9693c-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9693c-121">在安裝時註冊類別</span><span class="sxs-lookup"><span data-stu-id="9693c-121">Registering a Class at Installation</span></span>](registering-a-class-at-installation.md)
</dt> <dt>

[<span data-ttu-id="9693c-122">註冊正在執行的 EXE 伺服器</span><span class="sxs-lookup"><span data-stu-id="9693c-122">Registering a Running EXE Server</span></span>](registering-a-running-exe-server.md)
</dt> <dt>

[<span data-ttu-id="9693c-123">在 ROT 中註冊物件</span><span class="sxs-lookup"><span data-stu-id="9693c-123">Registering Objects in the ROT</span></span>](registering-objects-in-the-rot.md)
</dt> <dt>

[<span data-ttu-id="9693c-124">自我註冊</span><span class="sxs-lookup"><span data-stu-id="9693c-124">Self-Registration</span></span>](self-registration.md)
</dt> </dl>

 

 