---
title: 將 Microsoft Agent 功能新增至您的應用程式
description: 將 Microsoft Agent 功能新增至您的應用程式
ms.assetid: 2b4816dd-11bf-4c17-873e-4bdbb7fa1ccf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a2972b0251a4114e5d280d8f739d416ebc5dc1c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104314836"
---
# <a name="adding-microsoft-agent-functionality-to-your-application"></a><span data-ttu-id="e048a-103">將 Microsoft Agent 功能新增至您的應用程式</span><span class="sxs-lookup"><span data-stu-id="e048a-103">Adding Microsoft Agent Functionality to Your Application</span></span>

<span data-ttu-id="e048a-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="e048a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<span data-ttu-id="e048a-105">若要存取 Microsoft 代理程式的伺服器介面，必須已在目標系統上安裝代理程式。</span><span class="sxs-lookup"><span data-stu-id="e048a-105">To access Microsoft Agent's server interfaces, Agent must already be installed on the target system.</span></span> <span data-ttu-id="e048a-106">不支援使用代理程式自行安裝的可執行檔（例如嘗試複製和註冊代理程式元件檔）進行安裝。</span><span class="sxs-lookup"><span data-stu-id="e048a-106">Installation other than using Agent's self-installing executable file, such as attempting to copy and register Agent component files, is not supported.</span></span> <span data-ttu-id="e048a-107">這可確保一致且完全的安裝。</span><span class="sxs-lookup"><span data-stu-id="e048a-107">This ensures consistent and complete installation.</span></span> <span data-ttu-id="e048a-108">請注意，Microsoft 代理程式自行安裝檔案不會安裝在 Microsoft Windows 2000 和更新版本的作業系統上，因為這些版本的作業系統已經包含自己的代理程式版本。</span><span class="sxs-lookup"><span data-stu-id="e048a-108">Note that the Microsoft Agent self-installing file will not install on Microsoft Windows 2000 and later operating systems because these versions of the operating system already include their own version of Agent.</span></span>

<span data-ttu-id="e048a-109">若要在目標系統上成功安裝具有先前 Microsoft Windows 作業系統的代理程式，您也必須確定目標系統有最新版本的 Microsoft Visual C++ 執行時間 (Msvcrt.dll) 、Microsoft 註冊工具 (Regsvr32.dll) 和 Microsoft COM dll。</span><span class="sxs-lookup"><span data-stu-id="e048a-109">To successfully install Agent on a target system with a prior Microsoft Windows operating system, you must also ensure that the target system has a recent version of the Microsoft Visual C++ runtime (Msvcrt.dll), Microsoft registration tool (Regsvr32.dll), and Microsoft COM dlls.</span></span> <span data-ttu-id="e048a-110">若要確保目標系統上的必要元件，最簡單的方式就是要求安裝 Microsoft Internet Explorer 3.02 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="e048a-110">The easiest way to ensure that the necessary components are on the target system is to require that Microsoft Internet Explorer 3.02 or later is installed.</span></span> <span data-ttu-id="e048a-111">或者，您可以安裝 Microsoft Visual C++ 中提供的前兩個元件。</span><span class="sxs-lookup"><span data-stu-id="e048a-111">Alternatively, you can install the first two components which are available as part of Microsoft Visual C++.</span></span> <span data-ttu-id="e048a-112">必要的 COM dll 可以安裝為 Microsoft DCOM update 的一部分，可在 Microsoft 網站上取得。</span><span class="sxs-lookup"><span data-stu-id="e048a-112">The necessary COM dlls can be installed as part of the Microsoft DCOM update, available at the Microsoft website.</span></span> <span data-ttu-id="e048a-113">您可以在 Microsoft 網站上找到這些元件的進一步資訊和授權資訊。</span><span class="sxs-lookup"><span data-stu-id="e048a-113">You can find further information and licensing information for these components at the Microsoft website.</span></span>

<span data-ttu-id="e048a-114">代理程式的語言元件可以用同樣的方式來安裝。</span><span class="sxs-lookup"><span data-stu-id="e048a-114">Agent's language components can be installed the same way.</span></span> <span data-ttu-id="e048a-115">同樣地，您可以使用這項技術，來安裝可從 Microsoft 代理程式網站散發的 Microsoft 字元 ACS 格式。</span><span class="sxs-lookup"><span data-stu-id="e048a-115">Similarly, you can use this technique to install the ACS format of the Microsoft characters available for distribution from the Microsoft Agent website.</span></span> <span data-ttu-id="e048a-116">字元檔會自動安裝到 Microsoft 代理程式 \\ 字元子目錄。</span><span class="sxs-lookup"><span data-stu-id="e048a-116">The character files automatically install to the Microsoft Agent \\Chars subdirectory.</span></span>

<span data-ttu-id="e048a-117">因為 Microsoft 代理程式的元件是設計為作業系統元件，所以代理程式可能不會卸載。</span><span class="sxs-lookup"><span data-stu-id="e048a-117">Because Microsoft Agent's components are designed as operating system components, Agent may not be uninstalled.</span></span> <span data-ttu-id="e048a-118">同樣地，當代理程式已安裝為 Windows 作業系統的一部分時，代理程式自行安裝封包可能無法安裝。</span><span class="sxs-lookup"><span data-stu-id="e048a-118">Similarly, where Agent is already installed as part of the Windows operating system, the Agent self-installing cabinet may not install.</span></span>

<span data-ttu-id="e048a-119">一旦安裝之後，若要呼叫代理程式的介面，請建立伺服器的實例，並向伺服器支援使用標準 COM 慣例的特定介面要求指標。</span><span class="sxs-lookup"><span data-stu-id="e048a-119">Once installed, to call Agent's interfaces, create an instance of the server and request a pointer to a specific interface that the server supports using the standard COM convention.</span></span> <span data-ttu-id="e048a-120">尤其是，COM 程式庫會提供一個可建立物件實例的 API 函 [**式，並**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance)傳回物件的要求介面指標。</span><span class="sxs-lookup"><span data-stu-id="e048a-120">In particular, the COM library provides an API function, [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance), that creates an instance of the object and returns a pointer to the requested interface of the object.</span></span> <span data-ttu-id="e048a-121">要求 **CoCreateInstance** 呼叫中的 [**IAgent**](iagent.md)或 [**IAgentEx**](iagentex.md)介面指標，或在後續的 [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q))呼叫中要求指標。</span><span class="sxs-lookup"><span data-stu-id="e048a-121">Request a pointer to the [**IAgent**](iagent.md) or [**IAgentEx**](iagentex.md) interface in your **CoCreateInstance** call or in a subsequent call to [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)).</span></span>

<span data-ttu-id="e048a-122">下列程式碼將在 C/c + + 中說明這種情況。</span><span class="sxs-lookup"><span data-stu-id="e048a-122">The following code illustrates this in C/C++.</span></span>


```
hRes = CoCreateInstance(CLSID_AgentServer,
                     NULL,
                     CLSCTX_SERVER,
                     IID_IAgentEx,
                     (LPVOID *)&amp;pAgentEx);
```



<span data-ttu-id="e048a-123">如果 Microsoft 代理程式伺服器正在執行，此函式會連接到伺服器;否則，它會啟動伺服器。</span><span class="sxs-lookup"><span data-stu-id="e048a-123">If the Microsoft Agent server is running, this function connects to the server; otherwise, it starts up the server.</span></span>

<span data-ttu-id="e048a-124">請注意，Microsoft 代理程式伺服器介面通常會包含包含 "Ex" 尾碼的擴充介面。</span><span class="sxs-lookup"><span data-stu-id="e048a-124">Note that the Microsoft Agent server interfaces often include extended interfaces that include an "Ex" suffix.</span></span> <span data-ttu-id="e048a-125">這些介面衍生自，因此會包含其非 Ex 對應專案的所有功能。</span><span class="sxs-lookup"><span data-stu-id="e048a-125">These interfaces are derived from, and therefore include all the functionality of, their non-Ex counterparts.</span></span> <span data-ttu-id="e048a-126">如果您想要使用任何擴充功能，請使用 Ex 介面。</span><span class="sxs-lookup"><span data-stu-id="e048a-126">If you want to use any of the extended features, use the Ex interfaces.</span></span>

<span data-ttu-id="e048a-127">使用 [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring)來 bstr 配置記憶體之指標的函式。</span><span class="sxs-lookup"><span data-stu-id="e048a-127">Functions that take pointers to BSTRs allocate memory using [**SysAllocString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysallocstring).</span></span> <span data-ttu-id="e048a-128">呼叫者必須負責使用 [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring)釋放此記憶體。</span><span class="sxs-lookup"><span data-stu-id="e048a-128">It is the caller's responsibility to free this memory using [**SysFreeString**](/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring).</span></span>

 

 