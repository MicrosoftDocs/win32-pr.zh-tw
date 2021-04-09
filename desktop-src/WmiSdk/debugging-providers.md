---
description: 提供者（除非它們是在應用程式內執行的低耦合提供者）會載入 Wmiprvse.exe 進程，而不會透過 Winmgmt.exe 程式 Svchost.exe。 如需詳細資訊，請參閱提供者裝載和安全性。
ms.assetid: 8958669e-07e6-458c-a7f3-2df21cacc007
ms.tgt_platform: multiple
title: 偵錯工具
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d9cadb72f512c22c56db2b546b7920b96bfbd4d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943874"
---
# <a name="debugging-providers"></a><span data-ttu-id="68fd9-104">偵錯工具</span><span class="sxs-lookup"><span data-stu-id="68fd9-104">Debugging Providers</span></span>

<span data-ttu-id="68fd9-105">提供者（除非它們是在應用程式內執行的低 [*耦合提供者*](gloss-d.md) ）會載入 Wmiprvse.exe 進程，而不會透過 Winmgmt.exe 程式 Svchost.exe。</span><span class="sxs-lookup"><span data-stu-id="68fd9-105">Providers, unless they are [*decoupled providers*](gloss-d.md) running within an application, are loaded in a Wmiprvse.exe process, and not through Svchost.exe with a Winmgmt.exe process.</span></span> <span data-ttu-id="68fd9-106">如需詳細資訊，請參閱 [提供者裝載和安全性](provider-hosting-and-security.md)。</span><span class="sxs-lookup"><span data-stu-id="68fd9-106">For more information, see [Provider Hosting and Security](provider-hosting-and-security.md).</span></span>

<span data-ttu-id="68fd9-107">在中斷點停止時，Visual Studio 偵錯工具會凍結整個提供者主機進程，這通常是共用主控制項 Wmiprvse.exe。</span><span class="sxs-lookup"><span data-stu-id="68fd9-107">When stopping at a breakpoint, the Visual Studio debugger freezes the entire provider host process, which is usually the shared host Wmiprvse.exe.</span></span> <span data-ttu-id="68fd9-108">這可防止在該進程中裝載的任何其他元件（包括 WMI 伺服器總管擴充功能）進行操作。</span><span class="sxs-lookup"><span data-stu-id="68fd9-108">This prevents the operation of any other components hosted in that process, including the WMI Server Explorer extension.</span></span> <span data-ttu-id="68fd9-109">同時也會封鎖呼叫提供者的用戶端應用程式。</span><span class="sxs-lookup"><span data-stu-id="68fd9-109">Client applications that call into the provider are also blocked.</span></span> <span data-ttu-id="68fd9-110">由於提供者載入至 WMI 服務進程 (Winmgmt.exe) ，因此 Windows 2000 和更早版本中的問題會更糟。</span><span class="sxs-lookup"><span data-stu-id="68fd9-110">The problems that result are worse in Windows 2000 and earlier because the provider is loaded into the WMI service process (Winmgmt.exe).</span></span>

<span data-ttu-id="68fd9-111">如果您在另一個實例中執行 WMI 伺服器總管則 Visual Studio IDE 不會凍結，而且您可以釋放中斷點。</span><span class="sxs-lookup"><span data-stu-id="68fd9-111">If you run WMI Server Explorer in another instance then Visual Studio IDE does not freeze and you are able to release the breakpoint.</span></span> <span data-ttu-id="68fd9-112">建議您在開發階段期間，于不同的裝載進程中執行您的提供者，以便在中斷點停止時，只會凍結主控提供者的進程。</span><span class="sxs-lookup"><span data-stu-id="68fd9-112">It is recommended that you run your provider in a separate hosting process during the development phase, so that stopping at a breakpoint only freezes the process hosting your provider.</span></span> <span data-ttu-id="68fd9-113">Wmi 中的其他函式仍可繼續存取 wmi 伺服器總管以及任何其他 WMI 應用程式或腳本。</span><span class="sxs-lookup"><span data-stu-id="68fd9-113">The other functions in WMI continue to be accessible to WMI Server Explorer and any other WMI-based applications or scripts.</span></span> <span data-ttu-id="68fd9-114">此外，如果您的提供者損毀，就不會影響載入至相同主機進程的其他提供者作業。</span><span class="sxs-lookup"><span data-stu-id="68fd9-114">Also, if your provider crashes, it does not affect the operation of other providers loaded into the same host process.</span></span>

<span data-ttu-id="68fd9-115">若要讓提供者在自己的主機進程中載入，請修改提供者註冊，將 [**\_ \_ Win32Provider. HostingModel**](--win32provider.md)屬性設定為， `NetworkServiceHost:[MyProvider]` 其中 MyProvider 可以是可唯一識別提供者的任何字串。</span><span class="sxs-lookup"><span data-stu-id="68fd9-115">To make your provider load in its own host process, modify the provider registration to set the [**\_\_Win32Provider.HostingModel**](--win32provider.md) property to `NetworkServiceHost:[MyProvider]` where MyProvider can be any string that uniquely identifies your provider.</span></span> <span data-ttu-id="68fd9-116">例如，使用 Win32Provider 的 **\_ \_ ClsId** 值。</span><span class="sxs-lookup"><span data-stu-id="68fd9-116">For example, use the **\_\_Win32Provider.ClsId** value.</span></span> <span data-ttu-id="68fd9-117">當您的提供者已準備好寄送時，請將 **\_ \_ Win32Provider HostingModel** 回預期的值，例如 **NetworkServiceHost**。</span><span class="sxs-lookup"><span data-stu-id="68fd9-117">When your provider is ready to ship, return **\_\_Win32Provider.HostingModel** to the intended value, such as **NetworkServiceHost**.</span></span>

<span data-ttu-id="68fd9-118">如果您不是要對提供者載入進行偵錯工具，您可以呼叫 [**MSFT \_ 提供者類別的 load 方法**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) 來強制載入您的提供者，然後附加至已載入 DLL 的 Wmiprvse.exe 進程，然後視需要進行偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="68fd9-118">If you are not debugging provider loading, you can call the [**Load method of the MSFT\_Providers class**](/previous-versions/windows/desktop/wmisystemprov/load-method-in-class-msft-providers) to force your provider to load, then attach to the Wmiprvse.exe process that has the DLL loaded, and debug as needed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="68fd9-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="68fd9-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="68fd9-120">[WMI 疑難排解](wmi-troubleshooting.md) \(英文\)</span><span class="sxs-lookup"><span data-stu-id="68fd9-120">[WMI Troubleshooting](wmi-troubleshooting.md)</span></span>
</dt> <dt>

[<span data-ttu-id="68fd9-121">WMI 疑難排解類別</span><span class="sxs-lookup"><span data-stu-id="68fd9-121">WMI Troubleshooting Classes</span></span>](wmi-troubleshooting-classes.md)
</dt> </dl>

 

 
