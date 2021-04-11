---
description: DLL/COM 重新導向是 Windows XP 上的公司系統管理員所採用的應用程式隔離策略。
ms.assetid: 5bbb0bee-d457-4dfa-93a0-82537fe11f2d
title: Windows 上的 DLL/COM 重新導向
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e356c7b4cc6e5616a03eba60439c7478d65e626a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851152"
---
# <a name="dllcom-redirection-on-windows"></a><span data-ttu-id="71f33-103">Windows 上的 DLL/COM 重新導向</span><span class="sxs-lookup"><span data-stu-id="71f33-103">DLL/COM Redirection on Windows</span></span>

<span data-ttu-id="71f33-104">DLL/COM 重新導向是 Windows XP 上的公司系統管理員所採用的應用程式隔離策略。</span><span class="sxs-lookup"><span data-stu-id="71f33-104">DLL/COM redirection is an application isolation strategy employed by corporate administrators on Windows XP.</span></span>

<span data-ttu-id="71f33-105">\* \* Windows Server 2008、Windows Vista、windows Server 2003 和 Windows XP 加裝 SP2： \* \* 不建議使用 DLL/COM 重新導向策略，因為使用資訊清單和 [並存元件](about-side-by-side-assemblies-.md) 的隔離應用程式可能更容易更新及服務。</span><span class="sxs-lookup"><span data-stu-id="71f33-105">\*\*Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP with SP2:  \*\* The use of DLL/COM redirection strategies is not recommended because isolated applications that use manifests and [side-by-side assemblies](about-side-by-side-assemblies-.md) can be easier to update and service.</span></span> <span data-ttu-id="71f33-106">如果有資訊清單，則會忽略本機檔案的存在。</span><span class="sxs-lookup"><span data-stu-id="71f33-106">The presence of a .local file is ignored if a manifest is present.</span></span> <span data-ttu-id="71f33-107">如果應用程式沒有資訊清單，則使用本機檔案的 DLL/COM 重新導向策略就會運作。</span><span class="sxs-lookup"><span data-stu-id="71f33-107">The DLL/COM Redirection strategy using .local files works if the application does not have a manifest.</span></span>

<span data-ttu-id="71f33-108">DLL/COM 重新導向會將應用程式系結至元件的本機版本。</span><span class="sxs-lookup"><span data-stu-id="71f33-108">DLL/COM redirection binds an application to a local version of a component.</span></span> <span data-ttu-id="71f33-109">本機組件的檔案可以與應用程式私用位置中的系統元件版本分開保存。</span><span class="sxs-lookup"><span data-stu-id="71f33-109">The local component's files can be kept separate from the system's version of the component in a location that is private to the application.</span></span> <span data-ttu-id="71f33-110">系統的元件版本是全域登錄的，且可供任何系結至該元件的任何其他應用程式使用。</span><span class="sxs-lookup"><span data-stu-id="71f33-110">The system's version of the component is globally registered and available to any other applications that bind to it.</span></span> <span data-ttu-id="71f33-111">元件的本機版本會保留給應用程式的專屬用途。</span><span class="sxs-lookup"><span data-stu-id="71f33-111">The local version of the component is reserved for the exclusive use of the application.</span></span> <span data-ttu-id="71f33-112">如有必要，應用程式所使用的元件檔案可以與系統的元件檔同時載入至記憶體。</span><span class="sxs-lookup"><span data-stu-id="71f33-112">If necessary, the component files used by the application can be loaded into memory at the same time as the system's component files.</span></span>

<span data-ttu-id="71f33-113">DLL/COM 重新導向的啟用方式是將特殊檔案連同本機組件檔案的複本安裝到與應用程式可執行檔相同的目錄中。</span><span class="sxs-lookup"><span data-stu-id="71f33-113">DLL/COM redirection is activated by installing a special file along with a copy of the local component file into the same directory as the application's executable file.</span></span> <span data-ttu-id="71f33-114">特殊檔案是以應用程式可執行檔名稱命名並以 local 附加的空白檔案。</span><span class="sxs-lookup"><span data-stu-id="71f33-114">The special file is an empty file named after the application executable's file name and appended with .local.</span></span> <span data-ttu-id="71f33-115">例如，若要針對名為 Myapp 的應用程式啟動 DLL/COM 重新導向，必須將本機版本的元件和名為 Myapp.exe 的空檔案複製到包含 Myapp.exe 的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="71f33-115">For example, to activate DLL/COM redirection for an application named Myapp, the local version of the component and an empty file named Myapp.exe.local must be copied into the folder containing Myapp.exe.</span></span> <span data-ttu-id="71f33-116">這會將應用程式系結至元件的本機版本，而不是元件的全域共用版本。</span><span class="sxs-lookup"><span data-stu-id="71f33-116">This binds the application to the local version of the component rather than the globally shared version of the component.</span></span>

<span data-ttu-id="71f33-117">當應用程式載入元件檔（例如 DLL 或 .ocx 檔案）時，Windows 會先在安裝應用程式的本機和可執行檔所在的資料夾中搜尋它。</span><span class="sxs-lookup"><span data-stu-id="71f33-117">When an application loads a component file, such as a DLL or .ocx file, Windows first searches for it in the folder where the application's .local and executable file is installed.</span></span> <span data-ttu-id="71f33-118">如果找到，則應用程式會使用該元件檔案，不論應用程式或登錄中定義了任何目錄搜尋路徑。</span><span class="sxs-lookup"><span data-stu-id="71f33-118">If found, the application uses that component file regardless of any directory search path defined in the application or the registry.</span></span> <span data-ttu-id="71f33-119">如果找不到，則會使用定義之搜尋路徑中的元件檔。</span><span class="sxs-lookup"><span data-stu-id="71f33-119">If not found, the component file in the defined search path is used.</span></span>

<span data-ttu-id="71f33-120">安裝公用程式必須執行下列動作，才能使用 DLL/COM 重新導向來安裝應用程式：</span><span class="sxs-lookup"><span data-stu-id="71f33-120">The installation utility must do the following to install the application with DLL/COM redirection:</span></span>

-   <span data-ttu-id="71f33-121">空白的本機檔案必須複製到與應用程式可執行檔相同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="71f33-121">An empty .local file must be copied into the same folder as the application's executable file.</span></span>
-   <span data-ttu-id="71f33-122">應用程式所使用的所有元件、DLL 和 .ocx 檔案都必須複製到與應用程式可執行檔相同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="71f33-122">All of the components, DLL, and .ocx files used by the application must be copied into the same folder as the application's executable file.</span></span>
-   <span data-ttu-id="71f33-123">隔離的 COM 元件必須向 Windows 註冊，如此一來，當元件的不同版本同時載入記憶體時，就不會彼此衝突。</span><span class="sxs-lookup"><span data-stu-id="71f33-123">Isolated COM components must be registered with Windows so that different versions of the assembly will not conflict with each other when loaded into memory at the same time.</span></span> <span data-ttu-id="71f33-124">註冊程式會要求，雖然元件的執行可以在版本之間變更，但某些 COM 中繼資料（例如 CLSID、ProgID、類型程式庫和執行緒模型）則不能。</span><span class="sxs-lookup"><span data-stu-id="71f33-124">The registration process requires that, while the implementation of the component can change between versions, certain COM metadata such as CLSID, ProgID, Type Library, and Threading Model cannot.</span></span>
-   <span data-ttu-id="71f33-125">如果使用 Windows Installer 安裝應用程式，則可以使用 LockPermissions 資料表來保護應用程式目錄。</span><span class="sxs-lookup"><span data-stu-id="71f33-125">If the application is installed using the Windows Installer, then the application directory can be secured by using the LockPermissions table.</span></span> <span data-ttu-id="71f33-126">一般而言，系統會提供讀取、寫入和執行存取權;所有其他進程僅提供執行和讀取存取權。</span><span class="sxs-lookup"><span data-stu-id="71f33-126">Typically, the system is given read, write, and execute access; all other processes are given only execute and read access.</span></span>

 

 



