---
title: LocalService
description: 將物件安裝為服務應用程式。
ms.assetid: e8086118-f956-4cc2-a0fb-3cebd2e66799
keywords:
- LocalService 登錄值 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31f630c7c0a6f5e3bbf4b9c26ad82e5a104be238
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103842795"
---
# <a name="localservice"></a><span data-ttu-id="6327a-104">LocalService</span><span class="sxs-lookup"><span data-stu-id="6327a-104">LocalService</span></span>

<span data-ttu-id="6327a-105">將物件安裝為服務應用程式。</span><span class="sxs-lookup"><span data-stu-id="6327a-105">Installs an object as a service application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="6327a-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="6327a-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\AppID
   {AppID_GUID}
      LocalService = name
```

## <a name="remarks"></a><span data-ttu-id="6327a-107">備註</span><span class="sxs-lookup"><span data-stu-id="6327a-107">Remarks</span></span>

<span data-ttu-id="6327a-108">除了以本機伺服器可執行檔的形式執行 (EXE) ，COM 物件也可以選擇將本身封裝成在本機或遠端用戶端啟動時，以服務應用程式的形式執行。</span><span class="sxs-lookup"><span data-stu-id="6327a-108">In addition to running as a local server executable (EXE), a COM object may also choose to package itself to run as a service application when activated by a local or remote client.</span></span> <span data-ttu-id="6327a-109">服務支援許多有用和 UI 整合的管理功能，包括本機和遠端啟動、停止、暫停和重新開機，以及能夠建立伺服器以在特定使用者帳戶和視窗工作站上執行。</span><span class="sxs-lookup"><span data-stu-id="6327a-109">Services support numerous useful and UI-integrated administrative features, including local and remote starting, stopping, pausing, and restarting, as well as the ability to establish the server to run under a specific user account and window station.</span></span>

<span data-ttu-id="6327a-110">藉由建立 **LocalService** 值並執行標準服務安裝，會安裝寫入為服務的物件以供 COM 使用。</span><span class="sxs-lookup"><span data-stu-id="6327a-110">An object written as a service is installed for use by COM by establishing a **LocalService** value and performing a standard service installation.</span></span> <span data-ttu-id="6327a-111">**LocalService** 值必須設定為 **HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Services** 中所設定的服務名稱，作為預設的 **REG \_ SZ** 值。</span><span class="sxs-lookup"><span data-stu-id="6327a-111">The **LocalService** value must be set to the service name, as configured in **HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Services**, as the default **REG\_SZ** value.</span></span>

<span data-ttu-id="6327a-112">設定 **LocalService** 時，任何指派給 [**ServiceParameters**](serviceparameters.md) 的字串都會作為命令列引數傳遞至服務，因為它正在啟動中。</span><span class="sxs-lookup"><span data-stu-id="6327a-112">When **LocalService** is set, any string assigned to [**ServiceParameters**](serviceparameters.md) is passed as a command-line argument to the service as it is being launched.</span></span>

<span data-ttu-id="6327a-113">在許多情況下，在本機和遠端服務管理 Api 和使用者介面的功能可能對物件提供的服務很有用時，就會偏好使用服務設定。</span><span class="sxs-lookup"><span data-stu-id="6327a-113">The service configuration is preferred in many situations where the capabilities of the local and remote service management APIs and user interface might be useful for the services that the object provides.</span></span> <span data-ttu-id="6327a-114">例如，如果物件的存留期很長，或是很容易支援啟動、停止、重設或暫停等概念，利用服務架構的現有系統管理架構應該是很明顯的選擇。</span><span class="sxs-lookup"><span data-stu-id="6327a-114">For example, leveraging the existing administrative framework of the service architecture should be an obvious choice if the object is long-lived or readily supports concepts such as starting, stopping, resetting, or pausing.</span></span>

<span data-ttu-id="6327a-115">服務可以動態設定，並可設定為在電腦開機時自動執行，或在用戶端應用程式要求時啟動。</span><span class="sxs-lookup"><span data-stu-id="6327a-115">Services can be dynamically configured and can be configured to run automatically when the machine boots, or to be launched when requested by a client application.</span></span>

<span data-ttu-id="6327a-116">如果您要將類別實作為服務，您應該注意下列幾點：</span><span class="sxs-lookup"><span data-stu-id="6327a-116">If you are implementing classes as services, you should be aware of the following points:</span></span>

-   <span data-ttu-id="6327a-117">本機和遠端啟用 requestsâ的 [**LocalServer32**](localserver32.md) 金鑰偏好使用此值。如果 **LocalService** 存在且參考有效的服務，則會忽略 **LocalServer32** 索引鍵。</span><span class="sxs-lookup"><span data-stu-id="6327a-117">This value is used in preference to the [**LocalServer32**](localserver32.md) key for local and remote activation requestsâ€”if **LocalService** exists and refers to a valid service, the **LocalServer32** key is ignored.</span></span>
-   <span data-ttu-id="6327a-118">目前，只有服務應用程式的單一實例可以在電腦上的指定時間執行。</span><span class="sxs-lookup"><span data-stu-id="6327a-118">Currently, only a single instance of a service application may be running at a given time on a computer.</span></span> <span data-ttu-id="6327a-119">因此，COM 服務必須在啟動時使用 REGCLS MULTIPLEUSE 註冊其類別物件 \_ ，以支援多個用戶端。</span><span class="sxs-lookup"><span data-stu-id="6327a-119">COM services must therefore register their class objects on launch using REGCLS\_MULTIPLEUSE to support multiple clients.</span></span>
-   <span data-ttu-id="6327a-120">若要正確啟動和初始化，設定為在電腦開機時自動執行的 COM 服務必須在其相依服務清單中包含 RPCSS。</span><span class="sxs-lookup"><span data-stu-id="6327a-120">To launch and initialize properly, COM services configured to run automatically when a machine boots must include RPCSS in their list of dependent services.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6327a-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="6327a-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6327a-122">註冊 COM 伺服器</span><span class="sxs-lookup"><span data-stu-id="6327a-122">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="6327a-123">**ServiceParameters**</span><span class="sxs-lookup"><span data-stu-id="6327a-123">**ServiceParameters**</span></span>](serviceparameters.md)
</dt> <dt>

[<span data-ttu-id="6327a-124">服務</span><span class="sxs-lookup"><span data-stu-id="6327a-124">Services</span></span>](/windows/desktop/Services/services)
</dt> </dl>

 

 