---
description: WMI 提供統一的介面，可用於從電腦系統、網路或企業取得管理資料的任何本機或遠端應用程式或腳本。
ms.assetid: 41ba2a64-3322-48b8-a6ea-e468bfac06e2
ms.tgt_platform: multiple
title: WMI 架構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: b90ee4f81c2afdfc222dd7d5d824f88bda122b73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104571034"
---
# <a name="wmi-architecture"></a><span data-ttu-id="a3a79-103">WMI 架構</span><span class="sxs-lookup"><span data-stu-id="a3a79-103">WMI Architecture</span></span>

<span data-ttu-id="a3a79-104">WMI 提供統一的介面，可用於從電腦系統、網路或企業取得管理資料的任何本機或遠端應用程式或腳本。</span><span class="sxs-lookup"><span data-stu-id="a3a79-104">WMI provides a uniform interface for any local or remote applications or scripts that obtain management data from a computer system, a network, or an enterprise.</span></span> <span data-ttu-id="a3a79-105">統一介面的設計，是為了讓 WMI 用戶端應用程式和腳本不需要呼叫各種不同的操作系統應用程式設計介面， (Api) 。</span><span class="sxs-lookup"><span data-stu-id="a3a79-105">The uniform interface is designed such that WMI client applications and scripts do not have to call a wide variety of operating system application programming interfaces (APIs).</span></span> <span data-ttu-id="a3a79-106">許多 Api 都無法由腳本或 Visual Basic 應用程式等 automation 用戶端呼叫。</span><span class="sxs-lookup"><span data-stu-id="a3a79-106">Many APIs cannot be called by automation clients like scripts or Visual Basic applications.</span></span> <span data-ttu-id="a3a79-107">其他 Api 不會對遠端電腦進行呼叫。</span><span class="sxs-lookup"><span data-stu-id="a3a79-107">Other APIs do not make calls to remote computers.</span></span>

<span data-ttu-id="a3a79-108">若要從 WMI 取得資料，請撰寫可存取 [Wmi 類別](wmi-classes.md) 的用戶端腳本或應用程式，或撰寫 [*wmi 提供者*](gloss-p.md)以將資料提供給 WMI。</span><span class="sxs-lookup"><span data-stu-id="a3a79-108">To obtain data from WMI, write a client script or application that accesses [WMI Classes](wmi-classes.md) or provide data to WMI by writing a [*WMI provider*](gloss-p.md).</span></span> <span data-ttu-id="a3a79-109">如需詳細資訊，請參閱 [使用 WMI](using-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="a3a79-109">For more information, see [Using WMI](using-wmi.md).</span></span>

## <a name="objects-consumers-and-infrastructure-of-wmi"></a><span data-ttu-id="a3a79-110">WMI 的物件、取用者和基礎結構</span><span class="sxs-lookup"><span data-stu-id="a3a79-110">Objects, Consumers, and Infrastructure of WMI</span></span>

<span data-ttu-id="a3a79-111">下圖顯示 WMI 基礎結構與 WMI 提供者以及受管理物件之間的關聯性，同時也顯示 WMI 基礎結構與 WMI 取用者之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="a3a79-111">The following diagram shows the relationship between the WMI infrastructure and the WMI providers and managed objects, and it also shows the relationship between the WMI infrastructure and the WMI consumers.</span></span>

![wmi 基礎結構、wmi 提供者和 managed 物件之間的關聯性](images/wmi-architecture.png)

## <a name="wmi-components"></a><span data-ttu-id="a3a79-113">WMI 元件</span><span class="sxs-lookup"><span data-stu-id="a3a79-113">WMI Components</span></span>

<span data-ttu-id="a3a79-114">下列清單描述主要的 WMI 元件：</span><span class="sxs-lookup"><span data-stu-id="a3a79-114">The following list describes the key WMI components:</span></span>

-   <span data-ttu-id="a3a79-115">Managed 物件和 WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="a3a79-115">Managed objects and WMI providers</span></span>

    <span data-ttu-id="a3a79-116">WMI 提供者是一種 COM 物件，可監視一或多個 WMI 的 [*managed 物件*](gloss-m.md) 。</span><span class="sxs-lookup"><span data-stu-id="a3a79-116">A WMI provider is a COM object that monitors one or more [*managed objects*](gloss-m.md) for WMI.</span></span> <span data-ttu-id="a3a79-117">受管理物件是邏輯或實體的企業元件，例如硬碟、網路介面卡、資料庫系統、作業系統、進程或服務。</span><span class="sxs-lookup"><span data-stu-id="a3a79-117">A managed object is a logical or physical enterprise component, such as a hard disk drive, network adapter, database system, operating system, process, or service.</span></span>

    <span data-ttu-id="a3a79-118">與驅動程式類似，提供者會提供 WMI 和 managed 物件的資料，以及處理從 WMI 到 managed 物件的訊息。</span><span class="sxs-lookup"><span data-stu-id="a3a79-118">Similar to a driver, a provider supplies WMI with data from a managed object and handles messages from WMI to the managed object.</span></span> <span data-ttu-id="a3a79-119">WMI 提供者是由 DLL 檔和 [*受控物件格式 (MOF)*](gloss-m.md) 檔所組成，此檔案會定義提供者傳回資料並執行作業的類別。</span><span class="sxs-lookup"><span data-stu-id="a3a79-119">WMI providers consist of a DLL file and a [*Managed Object Format (MOF)*](gloss-m.md) file that defines the classes for which the provider returns data and performs operations.</span></span> <span data-ttu-id="a3a79-120">提供者（例如 WMI c + + 應用程式）會使用 [適用于 wmi 的 COM API](com-api-for-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="a3a79-120">Providers, like WMI C++ applications, use the [COM API for WMI](com-api-for-wmi.md).</span></span> <span data-ttu-id="a3a79-121">如需詳細資訊，請參閱 [將資料提供給 WMI](providing-data-to-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="a3a79-121">For more information, see [Providing Data to WMI](providing-data-to-wmi.md).</span></span>

    <span data-ttu-id="a3a79-122">提供者的範例是預先安裝的登錄 [提供者](/previous-versions/windows/desktop/regprov/system-registry-provider)，它會存取系統登錄中的資料。</span><span class="sxs-lookup"><span data-stu-id="a3a79-122">An example of a provider is the preinstalled [Registry provider](/previous-versions/windows/desktop/regprov/system-registry-provider), which accesses data in the system registry.</span></span> <span data-ttu-id="a3a79-123">登錄提供者有一個 [*WMI 類別*](gloss-w.md) [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov)，具有許多方法，但沒有屬性。</span><span class="sxs-lookup"><span data-stu-id="a3a79-123">The Registry provider has one [*WMI class*](gloss-w.md), [**StdRegProv**](/previous-versions/windows/desktop/regprov/stdregprov), with many methods but no properties.</span></span> <span data-ttu-id="a3a79-124">其他預先安裝的提供者（例如 [win32 提供者](/windows/desktop/CIMWin32Prov/win32-provider)）通常具有具有許多屬性的類別，但有少數方法（例如 [**Win32 \_ 進程**](/windows/desktop/CIMWin32Prov/win32-process) 或 [**win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)）。</span><span class="sxs-lookup"><span data-stu-id="a3a79-124">Other preinstalled providers, such as the [Win32 provider](/windows/desktop/CIMWin32Prov/win32-provider), usually have classes with many properties but few methods, such as [**Win32\_Process**](/windows/desktop/CIMWin32Prov/win32-process) or [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk).</span></span> <span data-ttu-id="a3a79-125">登錄提供者 DLL 檔案（Stdprov.dll）包含的程式碼會在用戶端腳本或應用程式要求時動態傳回資料。</span><span class="sxs-lookup"><span data-stu-id="a3a79-125">The Registry provider DLL file, Stdprov.dll, contains the code that dynamically returns data when requested by client scripts or applications.</span></span>

    <span data-ttu-id="a3a79-126">WMI MOF 和 DLL 檔案位於% WINDIR% \\ System32 \\ Wbem，以及 [wmi Command-Line 工具](wmi-command-line-tools.md)，例如 [**Winmgmt.exe**](winmgmt.md) 和 [**Mofcomp.exe**](mofcomp.md)。</span><span class="sxs-lookup"><span data-stu-id="a3a79-126">WMI MOF and DLL files are located in %WINDIR%\\System32\\Wbem, along with the [WMI Command-Line Tools](wmi-command-line-tools.md), such as [**Winmgmt.exe**](winmgmt.md) and [**Mofcomp.exe**](mofcomp.md).</span></span> <span data-ttu-id="a3a79-127">提供者類別（例如 [**Win32 \_ LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk)）是在 MOF 檔案中定義，然後在系統啟動時編譯成 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="a3a79-127">Provider classes, such as [**Win32\_LogicalDisk**](/windows/desktop/CIMWin32Prov/win32-logicaldisk), are defined in MOF files, and then compiled into the WMI repository at system startup.</span></span>

-   [<span data-ttu-id="a3a79-128">WMI 基礎結構</span><span class="sxs-lookup"><span data-stu-id="a3a79-128">WMI infrastructure</span></span>](wmi-infrastructure.md)

    <span data-ttu-id="a3a79-129">WMI 基礎結構是一種 Microsoft Windows 作業系統元件，也就是 (winmgmt) 的 WMI 服務。</span><span class="sxs-lookup"><span data-stu-id="a3a79-129">The WMI infrastructure is a Microsoft Windows operating system component know as the WMI service(winmgmt).</span></span> <span data-ttu-id="a3a79-130">WMI 基礎結構有兩個元件： WMI 核心和 Wmi 存放 [*庫*](gloss-w.md)。</span><span class="sxs-lookup"><span data-stu-id="a3a79-130">The WMI infrastructure has two components: the WMI Core, and the [*WMI repository*](gloss-w.md).</span></span>

    <span data-ttu-id="a3a79-131">WMI 存放庫是由 WMI [*命名空間*](gloss-n.md)所組成。</span><span class="sxs-lookup"><span data-stu-id="a3a79-131">The WMI repository is organized by WMI [*namespaces*](gloss-n.md).</span></span> <span data-ttu-id="a3a79-132">WMI 服務會在系統啟動時建立一些命名空間，例如根 \\ 預設、根 \\ cimv2 和根 \\ 訂用帳戶，並預先安裝一組預設的類別定義，包括 [Win32 類別](/windows/desktop/CIMWin32Prov/win32-provider)、 [WMI 系統類別](wmi-system-classes.md)和其他命名空間。</span><span class="sxs-lookup"><span data-stu-id="a3a79-132">The WMI service creates some namespaces such as root\\default, root\\cimv2, and root\\subscription at system startup and preinstalls a default set of class definitions, including the [Win32 Classes](/windows/desktop/CIMWin32Prov/win32-provider), the [WMI System Classes](wmi-system-classes.md), and others.</span></span> <span data-ttu-id="a3a79-133">在系統上找到的其餘命名空間是由作業系統或產品其他部分的提供者所建立。</span><span class="sxs-lookup"><span data-stu-id="a3a79-133">The remaining namespaces found on your system are created by providers for other parts of the operating system or products.</span></span> <span data-ttu-id="a3a79-134">如需詳細資訊和大部分作業系統版本中找到的 WMI 提供者清單，請參閱 [Wmi 提供者](wmi-providers.md)。</span><span class="sxs-lookup"><span data-stu-id="a3a79-134">For more information and a list of WMI providers found in most operating system versions, see [WMI Providers](wmi-providers.md).</span></span>

    <span data-ttu-id="a3a79-135">WMI 服務可作為提供者、管理應用程式和 WMI 儲存機制之間的媒介。</span><span class="sxs-lookup"><span data-stu-id="a3a79-135">The WMI service acts as an intermediary between the providers, management applications, and the WMI repository.</span></span> <span data-ttu-id="a3a79-136">只有有關物件的靜態資料會儲存在存放庫中，例如提供者所定義的類別。</span><span class="sxs-lookup"><span data-stu-id="a3a79-136">Only static data about objects is stored in the repository, such as the classes defined by providers.</span></span> <span data-ttu-id="a3a79-137">當用戶端要求時，WMI 會從提供者動態取得大部分的資料。</span><span class="sxs-lookup"><span data-stu-id="a3a79-137">WMI obtains most data dynamically from the provider when a client requests it.</span></span> <span data-ttu-id="a3a79-138">您也可以設定訂閱，以從提供者接收事件通知。</span><span class="sxs-lookup"><span data-stu-id="a3a79-138">You also can set up subscriptions to receive event notifications from a provider.</span></span> <span data-ttu-id="a3a79-139">如需詳細資訊，請參閱 [監視事件](monitoring-events.md)。</span><span class="sxs-lookup"><span data-stu-id="a3a79-139">For more information, see [Monitoring Events](monitoring-events.md).</span></span>

-   <span data-ttu-id="a3a79-140">WMI 取用者</span><span class="sxs-lookup"><span data-stu-id="a3a79-140">WMI consumers</span></span>

    <span data-ttu-id="a3a79-141">WMI 取用者是與 WMI 基礎結構互動的管理應用程式或腳本。</span><span class="sxs-lookup"><span data-stu-id="a3a79-141">A WMI consumer is a management application or script that interacts with the WMI infrastructure.</span></span> <span data-ttu-id="a3a79-142">管理應用程式可以透過呼叫 [適用于 wmi 的 COM API](com-api-for-wmi.md) 或 [適用于 WMI 的腳本 API](scripting-api-for-wmi.md)，來查詢、列舉資料、執行提供者方法或訂閱事件。</span><span class="sxs-lookup"><span data-stu-id="a3a79-142">A management application can query, enumerate data, run provider methods, or subscribe to events by calling either the [COM API for WMI](com-api-for-wmi.md) or the [Scripting API for WMI](scripting-api-for-wmi.md).</span></span> <span data-ttu-id="a3a79-143">受管理物件（例如磁片磁碟機或服務）唯一可用的資料或動作，就是提供者所提供的資料或動作。</span><span class="sxs-lookup"><span data-stu-id="a3a79-143">The only data or actions available for a managed object, such as a disk drive or a service, are those that a provider supplies.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3a79-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3a79-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3a79-145">使用 WMI</span><span class="sxs-lookup"><span data-stu-id="a3a79-145">Using WMI</span></span>](using-wmi.md)
</dt> <dt>

[<span data-ttu-id="a3a79-146">WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="a3a79-146">WMI Providers</span></span>](wmi-providers.md)
</dt> <dt>

[<span data-ttu-id="a3a79-147">建立 WMI 應用程式或腳本</span><span class="sxs-lookup"><span data-stu-id="a3a79-147">Creating a WMI Application or Script</span></span>](creating-a-wmi-application-or-script.md)
</dt> <dt>

[<span data-ttu-id="a3a79-148">腳本和應用程式的 WMI 工作</span><span class="sxs-lookup"><span data-stu-id="a3a79-148">WMI Tasks for Scripts and Applications</span></span>](wmi-tasks-for-scripts-and-applications.md)
</dt> <dt>

[<span data-ttu-id="a3a79-149">將資料提供給 WMI</span><span class="sxs-lookup"><span data-stu-id="a3a79-149">Providing Data to WMI</span></span>](providing-data-to-wmi.md)
</dt> <dt>

[<span data-ttu-id="a3a79-150">WMI 類別</span><span class="sxs-lookup"><span data-stu-id="a3a79-150">WMI Classes</span></span>](wmi-classes.md)
</dt> <dt>

[<span data-ttu-id="a3a79-151">監視事件</span><span class="sxs-lookup"><span data-stu-id="a3a79-151">Monitoring Events</span></span>](monitoring-events.md)
</dt> <dt>

[<span data-ttu-id="a3a79-152">呼叫方法</span><span class="sxs-lookup"><span data-stu-id="a3a79-152">Calling a Method</span></span>](calling-a-method.md)
</dt> </dl>

 

 
