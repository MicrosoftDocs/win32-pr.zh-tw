---
title: 使用具有虛擬通道的遠端桌面 ActiveX 控制項
description: 如果您已在遠端桌面服務部署中啟用虛擬通道應用程式，則可以將此應用程式提供給用戶端電腦使用。
ms.assetid: df537ffb-41dd-400e-8a49-9d8a10734eda
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 026c8fa23f1498270bd0d2a29c5f48d50f0b2463
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840172"
---
# <a name="using-the-remote-desktop-activex-control-with-virtual-channels"></a><span data-ttu-id="28956-103">使用具有虛擬通道的遠端桌面 ActiveX 控制項</span><span class="sxs-lookup"><span data-stu-id="28956-103">Using the Remote Desktop ActiveX control with virtual channels</span></span>

<span data-ttu-id="28956-104">如果您已在遠端桌面服務部署中啟用虛擬通道應用程式，可以透過遠端桌面 ActiveX 控制項，將此應用程式提供給存取遠端桌面工作階段主機 (RD 工作階段主機) server 的用戶端電腦使用。</span><span class="sxs-lookup"><span data-stu-id="28956-104">If you have enabled a virtual channels application in your Remote Desktop Services deployment, you can make this application available to client computers that access the Remote Desktop Session Host (RD Session Host) server by means of the Remote Desktop ActiveX control.</span></span>

<span data-ttu-id="28956-105">**讓虛擬通道應用程式可供使用**</span><span class="sxs-lookup"><span data-stu-id="28956-105">**To make a virtual channel application available**</span></span>

1.  <span data-ttu-id="28956-106">部署應用程式的伺服器端模組，並確定它正在 RD 工作階段主機伺服器上執行。</span><span class="sxs-lookup"><span data-stu-id="28956-106">Deploy the server-side module of the application and make sure it is running on the RD Session Host server.</span></span> <span data-ttu-id="28956-107">在 web 伺服器上執行之遠端桌面服務 web 應用程式的 [連接] 頁面中，存取 [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md)介面的 **PluginDlls** 屬性，以指定虛擬通道 DLL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="28956-107">In the connection page of the Remote Desktop Services web application running on your web server, access the **PluginDlls** property of the [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface to specify the name of your virtual channel DLL.</span></span> <span data-ttu-id="28956-108">如果您有一個以上的外掛程式，請指定以逗號分隔的 DLL 名稱清單。</span><span class="sxs-lookup"><span data-stu-id="28956-108">If you have more than one plug-in, specify a comma-delimited list of DLL names.</span></span> <span data-ttu-id="28956-109">比方說，如果您的虛擬通道外掛程式名為 "MyPlugin.dll"，請使用下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="28956-109">For instance, if your virtual channel plug-in is named "MyPlugin.dll", use the following code:</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll"
    ```

    <span data-ttu-id="28956-110">如果您有兩個虛擬通道 Dll，請使用下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="28956-110">Use the following code if you have two virtual channel DLLs.</span></span> <span data-ttu-id="28956-111">在此範例中，DLL 檔案名為 "MyPlugin.dll" 和 "Vdriver.dll"：</span><span class="sxs-lookup"><span data-stu-id="28956-111">In this example, the DLL file names are "MyPlugin.dll" and "Vdriver.dll":</span></span>

    ``` syntax
    MsRdpClient.AdvancedSettings.PluginDlls = "myplugin.dll,Vdriver.dll"
    ```

    <span data-ttu-id="28956-112">基於安全性理由， **PluginDlls** 屬性只接受虛擬通道 dll 的命名清單。</span><span class="sxs-lookup"><span data-stu-id="28956-112">For security reasons, the **PluginDlls** property only accepts a named list of virtual channel DLLs.</span></span> <span data-ttu-id="28956-113">如果指定了任何格式的檔案系統或 UNC 路徑，控制項就會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="28956-113">The control returns an error if any form of file system or UNC path is specified.</span></span> <span data-ttu-id="28956-114">此外，Dll 的名稱必須只包含英數位元。</span><span class="sxs-lookup"><span data-stu-id="28956-114">In addition, the names of the DLLs must contain only alphanumeric characters.</span></span>

2.  <span data-ttu-id="28956-115">確定已將用戶端模組安裝在% windir% \\ system32 目錄中。</span><span class="sxs-lookup"><span data-stu-id="28956-115">Ensure that the client-side module is installed in the %windir%\\system32 directory.</span></span>

<span data-ttu-id="28956-116">虛擬通道 API 不允許在單一進程內載入相同虛擬通道 DLL 的多個實例。</span><span class="sxs-lookup"><span data-stu-id="28956-116">The virtual channel API does not allow for multiple instances of the same virtual channel DLL to be loaded within a single process.</span></span> <span data-ttu-id="28956-117">基於這個原因，如果在相同進程中執行的遠端桌面 ActiveX 控制項有多個實例，則只有控制項的第一個實例才能載入虛擬通道 DLL。</span><span class="sxs-lookup"><span data-stu-id="28956-117">Because of this, if there are multiple instances of the Remote Desktop ActiveX control running within the same process, only the first instance of the control will be able to load the virtual channel DLL.</span></span> <span data-ttu-id="28956-118">如果您要設計的虛擬通道應用程式必須在單一進程內支援多個實例，您必須使用 [動態虛擬通道](dynamic-virtual-channels.md) API 來執行虛擬通道應用程式。</span><span class="sxs-lookup"><span data-stu-id="28956-118">If you are designing a virtual channel application that must support multiple instances within a single process, you must use the [Dynamic Virtual Channels](dynamic-virtual-channels.md) API to implement your virtual channel application.</span></span>

> [!Note]  
> <span data-ttu-id="28956-119">根據預設，遠端桌面 ActiveX 控制項會從% windir% system32 目錄載入虛擬通道用戶端 Dll \\ 。</span><span class="sxs-lookup"><span data-stu-id="28956-119">By default, the Remote Desktop ActiveX control loads virtual channel client DLLs from the %windir%\\system32 directory.</span></span> <span data-ttu-id="28956-120">系統管理員可以變更此預設用戶端外掛程式 DLL 目錄。</span><span class="sxs-lookup"><span data-stu-id="28956-120">It is possible for an administrator to change this default client plug-in DLL directory.</span></span> <span data-ttu-id="28956-121">若要這樣做，請在用戶端電腦上編輯 **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Terminal Server Client** \\ **vdllpath** registry key。</span><span class="sxs-lookup"><span data-stu-id="28956-121">To do so, edit the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Terminal Server Client**\\**vdllpath** registry key on the client computer.</span></span> <span data-ttu-id="28956-122">此目錄路徑不能以 UNC 格式指定。</span><span class="sxs-lookup"><span data-stu-id="28956-122">This directory path cannot be specified in the UNC format.</span></span>

 

 

 




