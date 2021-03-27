---
description: Windows 7 及更新版本系統中的工作列會廣泛使用 (AppUserModelIDs) 的應用程式使用者模型識別碼，以將處理常式、檔案和視窗與特定應用程式產生關聯。
ms.assetid: ebce2d99-6f20-4545-9f12-d79cd8d0828f
title: '應用程式使用者模型識別碼 (AppUserModelIDs) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46b79f0bdd7fb5e6c4d5c41caa3cd6be3f4fb57e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511067"
---
# <a name="application-user-model-ids-appusermodelids"></a><span data-ttu-id="62c20-103">應用程式使用者模型識別碼 (AppUserModelIDs) </span><span class="sxs-lookup"><span data-stu-id="62c20-103">Application User Model IDs (AppUserModelIDs)</span></span>

<span data-ttu-id="62c20-104">Windows 7 及更新版本系統中的工作列會廣泛使用 (AppUserModelIDs) 的應用程式使用者模型識別碼，以將處理常式、檔案和視窗與特定應用程式產生關聯。</span><span class="sxs-lookup"><span data-stu-id="62c20-104">Application User Model IDs (AppUserModelIDs) are used extensively by the taskbar in Windows 7 and later systems to associate processes, files, and windows with a particular application.</span></span> <span data-ttu-id="62c20-105">在某些情況下，就足以依賴系統指派給進程的內部 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-105">In some cases, it is sufficient to rely on the internal AppUserModelID assigned to a process by the system.</span></span> <span data-ttu-id="62c20-106">不過，擁有多個處理常式或在主機進程中執行之應用程式的應用程式可能需要明確地識別其本身，如此它就可以在單一工作列按鈕下將其另一個不同的視窗分組，並控制該應用程式捷徑清單的內容。</span><span class="sxs-lookup"><span data-stu-id="62c20-106">However, an application that owns multiple processes or an application that is running in a host process might need to explicitly identify itself so that it can group its otherwise disparate windows under a single taskbar button and control the contents of that application's Jump List.</span></span>

-   [<span data-ttu-id="62c20-107">應用程式定義和 System-Defined AppUserModelIDs</span><span class="sxs-lookup"><span data-stu-id="62c20-107">Application-Defined and System-Defined AppUserModelIDs</span></span>](#application-defined-and-system-defined-appusermodelids)
-   [<span data-ttu-id="62c20-108">如何形成 Application-Defined AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="62c20-108">How to Form an Application-Defined AppUserModelID</span></span>](#how-to-form-an-application-defined-appusermodelid)
-   [<span data-ttu-id="62c20-109">要在哪裡指派 AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="62c20-109">Where to Assign an AppUserModelID</span></span>](#where-to-assign-an-appusermodelid)
-   [<span data-ttu-id="62c20-110">將應用程式註冊為主機進程</span><span class="sxs-lookup"><span data-stu-id="62c20-110">Registering an Application as a Host Process</span></span>](#registering-an-application-as-a-host-process)
-   [<span data-ttu-id="62c20-111">工作列釘選和最近/頻繁清單的排除清單</span><span class="sxs-lookup"><span data-stu-id="62c20-111">Exclusion Lists for Taskbar Pinning and Recent/Frequent Lists</span></span>](#exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists)
-   [<span data-ttu-id="62c20-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="62c20-112">Related topics</span></span>](#related-topics)

## <a name="application-defined-and-system-defined-appusermodelids"></a><span data-ttu-id="62c20-113">Application-Defined 和 System-Defined AppUserModelIDs</span><span class="sxs-lookup"><span data-stu-id="62c20-113">Application-Defined and System-Defined AppUserModelIDs</span></span>

<span data-ttu-id="62c20-114">有些應用程式不會宣告明確的 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-114">Some applications do not declare an explicit AppUserModelID.</span></span> <span data-ttu-id="62c20-115">它們是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="62c20-115">They are optional.</span></span> <span data-ttu-id="62c20-116">在這種情況下，系統會使用一系列的啟發學習法來指派內部 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-116">In that case, the system uses a series of heuristics to assign an internal AppUserModelID.</span></span> <span data-ttu-id="62c20-117">但是，為了避免這些計算，有一個效能上的好處，而明確的 AppUserModelID 是保證確切使用者體驗的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="62c20-117">However, there is a performance benefit in avoiding those calculations and an explicit AppUserModelID is the only way to guarantee an exact user experience.</span></span> <span data-ttu-id="62c20-118">因此，強烈建議您設定明確的識別碼。</span><span class="sxs-lookup"><span data-stu-id="62c20-118">Therefore, it is strongly recommended that an explicit ID be set.</span></span> <span data-ttu-id="62c20-119">應用程式無法取出系統指派的 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-119">Applications cannot retrieve a system-assigned AppUserModelID.</span></span>

<span data-ttu-id="62c20-120">如果應用程式使用明確的 AppUserModelID，則也必須將相同的 AppUserModelID 指派給所有執行中的 windows 或進程、快捷方式和檔案關聯。</span><span class="sxs-lookup"><span data-stu-id="62c20-120">If an application uses an explicit AppUserModelID, it must also assign the same AppUserModelID to all running windows or processes, shortcuts, and file associations.</span></span> <span data-ttu-id="62c20-121">當您透過 [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)或 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)的任何呼叫自訂其捷徑清單時，也必須使用 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-121">It must also use that AppUserModelID when customizing its Jump List through [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist), and in any calls to [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span></span>

> [!Note]  
> <span data-ttu-id="62c20-122">如果應用程式沒有明確的 AppUserModelID，則必須呼叫 [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)、 [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)和 [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist) 方法，以及從應用程式內 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) 。</span><span class="sxs-lookup"><span data-stu-id="62c20-122">If applications do not have an explicit AppUserModelID, they must call [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations), [**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists), and [**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist) methods as well as [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) from within the application.</span></span> <span data-ttu-id="62c20-123">如果從另一個進程（例如安裝程式或卸載程式）呼叫這些方法，系統就無法產生正確的 AppUserModelID，而且這些呼叫將不會有任何作用。</span><span class="sxs-lookup"><span data-stu-id="62c20-123">If those methods are called from another process, such as an installer or uninstaller, the system cannot generate the correct AppUserModelID and those calls will have no effect.</span></span>

 

<span data-ttu-id="62c20-124">下列專案描述需要明確 AppUserModelID 的一般案例。</span><span class="sxs-lookup"><span data-stu-id="62c20-124">The following items describe common scenarios that require an explicit AppUserModelID.</span></span> <span data-ttu-id="62c20-125">它們也指出應該使用多個明確 AppUserModelIDs 的情況。</span><span class="sxs-lookup"><span data-stu-id="62c20-125">They also point out cases where multiple explicit AppUserModelIDs should be used.</span></span>

-   <span data-ttu-id="62c20-126">具有多個模式的 UI 的單一可執行檔，會以個別的應用程式顯示給使用者，應該將不同的 AppUserModelIDs 指派給每個模式。</span><span class="sxs-lookup"><span data-stu-id="62c20-126">A single executable file with a UI with multiple modes that appear to the user as separate applications should assign different AppUserModelIDs to each mode.</span></span> <span data-ttu-id="62c20-127">例如，使用者看到的部分應用程式，可以與應用程式的其餘部分分開釘選並從工作列啟動，而與主要體驗不同的是，它會有自己的 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-127">For instance, a portion of an application that users see as an independent experience that they can pin to and launch from the taskbar separately from the rest of the application should have its own AppUserModelID, separate from the main experience.</span></span>
-   <span data-ttu-id="62c20-128">具有不同引數的多個快捷方式，全都會導致使用者看到的相同應用程式，應該使用一個 AppUserModelID 來處理所有的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="62c20-128">Multiple shortcuts with different arguments that all lead to what the user sees as the same application should use one AppUserModelID for all of the shortcuts.</span></span> <span data-ttu-id="62c20-129">例如，Windows Internet Explorer 針對不同的模式有不同的快捷方式 (例如，啟動但不含附加元件) 但它們都應該以單一 Internet Explorer 實例的形式呈現給使用者。</span><span class="sxs-lookup"><span data-stu-id="62c20-129">For example, Windows Internet Explorer has different shortcuts for different modes (such as launching without add-ons) but they should all appear to the user as a single Internet Explorer instance.</span></span>
-   <span data-ttu-id="62c20-130">做為主機進程並以應用程式形式執行目標內容的可執行檔必須 [註冊為主應用程式](#registering-an-application-as-a-host-process)，之後才能將不同的 AppUserModelIDs 指派給它所裝載的每個察覺體驗。</span><span class="sxs-lookup"><span data-stu-id="62c20-130">An executable that acts as a host process and runs target content as an application must [register as a host application](#registering-an-application-as-a-host-process), after which it can assign different AppUserModelIDs to each perceived experience that it hosts.</span></span> <span data-ttu-id="62c20-131">或者，主機進程可以允許裝載的程式設定其 AppUserModelIDs。</span><span class="sxs-lookup"><span data-stu-id="62c20-131">Alternately, the host process can allow the hosted program to set its AppUserModelIDs.</span></span> <span data-ttu-id="62c20-132">無論是哪一種情況，主機進程都必須保留 AppUserModelIDs 來源（本身或裝載的應用程式）的記錄。</span><span class="sxs-lookup"><span data-stu-id="62c20-132">In either case, the host process must keep a record of the source of the AppUserModelIDs, either itself or the hosted application.</span></span> <span data-ttu-id="62c20-133">在此情況下，沒有目標內容的主機進程的主要使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="62c20-133">In this case, there is no primary user experience of the host process without the target content.</span></span> <span data-ttu-id="62c20-134">例如，Windows 遠端應用程式整合在本機 (滑軌) 應用程式、JAVA 執行時間、RunDLL32.exe 或 DLLHost.exe。</span><span class="sxs-lookup"><span data-stu-id="62c20-134">Examples are Windows Remote Applications Integrated Locally (RAIL) applications, the Java Runtime, RunDLL32.exe, or DLLHost.exe.</span></span>

    <span data-ttu-id="62c20-135">如果是現有的託管應用程式，系統會嘗試識別個別的體驗，但新的應用程式應該使用明確的 AppUserModelIDs 來保證預期的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="62c20-135">In the case of existing hosted applications, the system attempts to identify individual experiences, but new applications should use explicit AppUserModelIDs to guarantee the intended user experience.</span></span>

-   <span data-ttu-id="62c20-136">對使用者而言，合作或連鎖的程式必須套用至每個進程的相同 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-136">Cooperative or chained processes that to the user are part of the same application should have the same AppUserModelID applied to each process.</span></span> <span data-ttu-id="62c20-137">範例包括具有啟動器流程的遊戲 (連結) 和 Microsoft Windows Media Player，其中包含在一個進程中執行的第一次執行/安裝體驗，以及在另一個進程中執行的主要應用程式 (合作) 。</span><span class="sxs-lookup"><span data-stu-id="62c20-137">Examples include games with a launcher process (chained) and Microsoft Windows Media Player, which has a first-run/setup experience running in one process and the main application running in another process (cooperative).</span></span>
-   <span data-ttu-id="62c20-138">Shell 命名空間延伸模組可作為個別的應用程式，而不是流覽和管理 Windows 檔案總管中的內容，應該在其資料夾屬性中指派 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-138">A Shell namespace extension that acts as a separate application for more than browsing and managing content in Windows Explorer should assign an AppUserModelID in its folder properties.</span></span> <span data-ttu-id="62c20-139">主控台的範例。</span><span class="sxs-lookup"><span data-stu-id="62c20-139">An example is the Control Panel.</span></span>
-   <span data-ttu-id="62c20-140">在部署架構之類的虛擬化環境中，虛擬化環境應該將不同的 AppUserModelIDs 指派給其所管理的每個應用程式。</span><span class="sxs-lookup"><span data-stu-id="62c20-140">In a virtualization environment such as a deployment framework, the virtualization environment should assign different AppUserModelIDs to each application that it manages.</span></span> <span data-ttu-id="62c20-141">在這些情況下，應用程式啟動器會使用中繼程式來設定環境，然後將作業交給不同的進程來執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="62c20-141">In these cases, an application launcher uses an intermediary process to set up the environment and then hands off the operation to a different process to run the application.</span></span> <span data-ttu-id="62c20-142">請注意，這會導致系統無法使執行中的目標進程與快捷方式產生關聯，因為快捷方式指向中繼進程。</span><span class="sxs-lookup"><span data-stu-id="62c20-142">Note that this causes the system to be unable to relate the running target process back to the shortcut because the shortcut points to the intermediary process.</span></span>

    <span data-ttu-id="62c20-143">如果有任何應用程式有多個視窗、快捷方式或程式，該應用程式指派的 AppUserModelID 也應套用至虛擬化環境中的每個部分。</span><span class="sxs-lookup"><span data-stu-id="62c20-143">If any application has multiple windows, shortcuts, or processes, that application's assigned AppUserModelID should also be applied to each of those pieces by the virtualization environment.</span></span>

    <span data-ttu-id="62c20-144">這種情況的其中一個範例是 ClickOnce 架構，它會代表它所管理的應用程式，正確指派 AppUserModelIDs。</span><span class="sxs-lookup"><span data-stu-id="62c20-144">An example of this situation is the ClickOnce framework, which properly assigns AppUserModelIDs on behalf of the applications that it manages.</span></span> <span data-ttu-id="62c20-145">如同在所有這類環境中，ClickOnce 部署及管理的應用程式不應該指派明確的 AppUserModelIDs，因為這樣做會與 ClickOnce 指派的 AppUserModelIDs 發生衝突，並導致非預期的結果。</span><span class="sxs-lookup"><span data-stu-id="62c20-145">As in all such environments, applications deployed and managed by ClickOnce should not assign explicit AppUserModelIDs themselves, because doing so will conflict with the AppUserModelIDs assigned by ClickOnce and lead to unexpected results.</span></span>

## <a name="how-to-form-an-application-defined-appusermodelid"></a><span data-ttu-id="62c20-146">如何形成 Application-Defined AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="62c20-146">How to Form an Application-Defined AppUserModelID</span></span>

<span data-ttu-id="62c20-147">應用程式必須以下列格式提供其 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-147">An application must provide its AppUserModelID in the following form.</span></span> <span data-ttu-id="62c20-148">它不能超過128個字元，而且不能包含空格。</span><span class="sxs-lookup"><span data-stu-id="62c20-148">It can have no more than 128 characters and cannot contain spaces.</span></span> <span data-ttu-id="62c20-149">每個區段的大小寫都應該是 pascal。</span><span class="sxs-lookup"><span data-stu-id="62c20-149">Each section should be pascal-cased.</span></span>

`CompanyName.ProductName.SubProduct.VersionInformation`

<span data-ttu-id="62c20-150">`CompanyName` 和都 `ProductName` 應該使用，而且 `SubProduct` 和 `VersionInformation` 部分是選擇性的，且取決於應用程式的需求。</span><span class="sxs-lookup"><span data-stu-id="62c20-150">`CompanyName` and `ProductName` should always be used, while the `SubProduct` and `VersionInformation` portions are optional and depend on the application's requirements.</span></span> <span data-ttu-id="62c20-151">`SubProduct` 允許包含數個 subapplications 的主要應用程式，為每個 subapplication 和其相關聯的視窗提供個別的工作列按鈕。</span><span class="sxs-lookup"><span data-stu-id="62c20-151">`SubProduct` allows a main application that consists of several subapplications to provide a separate taskbar button for each subapplication and its associated windows.</span></span> <span data-ttu-id="62c20-152">`VersionInformation` 允許兩個版本的應用程式在視為離散實體時並存。</span><span class="sxs-lookup"><span data-stu-id="62c20-152">`VersionInformation` allows two versions of an application to coexist while being seen as discrete entities.</span></span> <span data-ttu-id="62c20-153">如果應用程式不是以這種方式使用，則 `VersionInformation` 應該省略，使升級的版本可以使用與所取代版本相同的 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-153">If an application is not intended to be used in that way, the `VersionInformation` should be omitted so that an upgraded version can use the same AppUserModelID as the version that it replaced.</span></span>

## <a name="where-to-assign-an-appusermodelid"></a><span data-ttu-id="62c20-154">要在哪裡指派 AppUserModelID</span><span class="sxs-lookup"><span data-stu-id="62c20-154">Where to Assign an AppUserModelID</span></span>

<span data-ttu-id="62c20-155">當應用程式使用一或多個明確的 AppUserModelIDs 時，應該將這些 AppUserModelIDs 套用至下列位置和情況：</span><span class="sxs-lookup"><span data-stu-id="62c20-155">When an application uses one or more explicit AppUserModelIDs, it should apply those AppUserModelIDs in the following locations and situations:</span></span>

-   <span data-ttu-id="62c20-156">在應用程式快捷方式檔案的 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) 屬性中。</span><span class="sxs-lookup"><span data-stu-id="62c20-156">In the [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property of the application's shortcut file.</span></span> <span data-ttu-id="62c20-157">快速鍵 (為 [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka)、CLSID \_ ShellLink 或 .lnk 檔案) 透過 [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) 和整個 Shell 中使用的其他屬性設定機制來支援屬性。</span><span class="sxs-lookup"><span data-stu-id="62c20-157">A shortcut (as an [**IShellLink**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ishelllinka), CLSID\_ShellLink, or a .lnk file) supports properties through [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) and other property-setting mechanisms used throughout the Shell.</span></span> <span data-ttu-id="62c20-158">這可讓工作列識別適當的快捷方式來釘選，並確保屬於該進程的 windows 會適當地與工作列按鈕相關聯。</span><span class="sxs-lookup"><span data-stu-id="62c20-158">This allows the taskbar to identify the proper shortcut to pin and ensures that windows belonging to the process are appropriately associated with that taskbar button.</span></span>
    > [!Note]  
    > <span data-ttu-id="62c20-159">建立快捷方式時，應將 [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) 屬性套用至快捷方式。</span><span class="sxs-lookup"><span data-stu-id="62c20-159">The [System.AppUserModel.ID](../properties/props-system-appusermodel-id.md) property should be applied to a shortcut when that shortcut is created.</span></span> <span data-ttu-id="62c20-160">使用 Microsoft Windows Installer (MSI) 安裝應用程式時， [MsiShortcutProperty](../msi/msishortcutproperty-table.md) 表格可在安裝期間建立 AppUserModelID 以套用至快捷方式。</span><span class="sxs-lookup"><span data-stu-id="62c20-160">When using the Microsoft Windows Installer (MSI) to install the application, the [MsiShortcutProperty](../msi/msishortcutproperty-table.md) table allows the AppUserModelID to be applied to the shortcut when it is created during installation.</span></span>

     

-   <span data-ttu-id="62c20-161">做為任何應用程式執行中視窗的屬性。</span><span class="sxs-lookup"><span data-stu-id="62c20-161">As a property of any of the application's running windows.</span></span> <span data-ttu-id="62c20-162">這可以透過下列兩種方式之一來設定：</span><span class="sxs-lookup"><span data-stu-id="62c20-162">This can be set in one of two ways:</span></span>

    1.  <span data-ttu-id="62c20-163">如果一個進程擁有不同的視窗需要不同的 AppUserModelIDs 來控制工作列群組，請使用 [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)) 取出視窗的屬性存放區，並將 AppUserModelID 設定為視窗屬性。</span><span class="sxs-lookup"><span data-stu-id="62c20-163">If different windows owned by one process require different AppUserModelIDs to control taskbar grouping, use [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)) to retrieve the window's property store and set the AppUserModelID as a window property.</span></span>
    2.  <span data-ttu-id="62c20-164">如果程式中的所有視窗都使用相同的 AppUserModelID，請在 [**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid)上設定流程的 appusermodelid。</span><span class="sxs-lookup"><span data-stu-id="62c20-164">If all windows in the process use the same AppUserModelID, set the AppUserModelID on the process though [**SetCurrentProcessExplicitAppUserModelID**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid).</span></span> <span data-ttu-id="62c20-165">應用程式必須呼叫 **SetCurrentProcessExplicitAppUserModelID** ，以在應用程式呈現任何 UI 之前，在應用程式的初始啟動常式中設定其 AppUserModelID、對其跳躍清單進行任何操作，或 (，或讓系統) 任何對 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)的呼叫。</span><span class="sxs-lookup"><span data-stu-id="62c20-165">An application must call **SetCurrentProcessExplicitAppUserModelID** to set its AppUserModelID during an application's initial startup routine before the application presents any UI, makes any manipulation of its Jump Lists, or makes (or causes the system to make) any call to [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span></span>

    <span data-ttu-id="62c20-166">視窗層級 AppUserModelID 會覆寫進程層級的 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-166">A window-level AppUserModelID overrides a process-level AppUserModelID.</span></span>

    <span data-ttu-id="62c20-167">當應用程式在視窗層級設定明確的 AppUserModelID 時，應用程式可以為其工作列按鈕提供其重新開機命令的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="62c20-167">When an application sets an explicit AppUserModelID at the window level, the application can provide the specifics of its relaunch command for its taskbar button.</span></span> <span data-ttu-id="62c20-168">若要提供該資訊，請使用下列屬性：</span><span class="sxs-lookup"><span data-stu-id="62c20-168">To supply that information, the following properties are used:</span></span>

    -   [<span data-ttu-id="62c20-169">AppUserModel. RelaunchCommand</span><span class="sxs-lookup"><span data-stu-id="62c20-169">System.AppUserModel.RelaunchCommand</span></span>](../properties/props-system-appusermodel-relaunchcommand.md)
    -   [<span data-ttu-id="62c20-170">AppUserModel. RelaunchDisplayNameResource</span><span class="sxs-lookup"><span data-stu-id="62c20-170">System.AppUserModel.RelaunchDisplayNameResource</span></span>](../properties/props-system-appusermodel-relaunchdisplaynameresource.md)
    -   [<span data-ttu-id="62c20-171">AppUserModel. RelaunchIconResource</span><span class="sxs-lookup"><span data-stu-id="62c20-171">System.AppUserModel.RelaunchIconResource</span></span>](../properties/props-system-appusermodel-relaunchiconresource.md)

    > [!Note]  
    > <span data-ttu-id="62c20-172">如果有啟動應用程式的快捷方式，應用程式應該將 AppUserModelID 套用為快捷方式的屬性，而不是使用重新開機屬性。</span><span class="sxs-lookup"><span data-stu-id="62c20-172">If a shortcut exists to launch the application, an application should apply the AppUserModelID as a property of the shortcut instead of using the relaunch properties.</span></span> <span data-ttu-id="62c20-173">在此情況下，會使用命令列、圖示和快捷方式的文字來提供與重新開機屬性相同的資訊。</span><span class="sxs-lookup"><span data-stu-id="62c20-173">In that case, the command line, icon, and text of the shortcut are used to supply the same information as the relaunch properties.</span></span>

     

    <span data-ttu-id="62c20-174">視窗層級的明確 AppUserModelID 也可以使用 [AppUserModel. PreventPinning](../properties/props-system-appusermodel-preventpinning.md) 屬性來指定它不應該用於釘選或重新執行。</span><span class="sxs-lookup"><span data-stu-id="62c20-174">A window-level explicit AppUserModelID can also use the [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) property to specify that it should not be available for pinning or relaunching.</span></span>

-   <span data-ttu-id="62c20-175">在自訂或更新 ([**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)) 的呼叫中，取得 ([**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)) ，或清除 (應用程式) 的捷徑清單 [**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations) 。</span><span class="sxs-lookup"><span data-stu-id="62c20-175">In a call to customize or update ([**ICustomDestinationList**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icustomdestinationlist)), retrieve ([**IApplicationDocumentLists**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdocumentlists)), or clear ([**IApplicationDestinations**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iapplicationdestinations)) the application's Jump List.</span></span>
-   <span data-ttu-id="62c20-176">在檔案關聯註冊 (透過其 [ProgID](fa-progids.md)) 如果應用程式使用系統自動產生的 **最新** 或 **經常** 的目的地清單。</span><span class="sxs-lookup"><span data-stu-id="62c20-176">In file association registration (through its [ProgID](fa-progids.md)) if the application uses the system's automatically generated **Recent** or **Frequent** destination lists.</span></span> <span data-ttu-id="62c20-177">[**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)會參考此關聯資訊。</span><span class="sxs-lookup"><span data-stu-id="62c20-177">This association information is referenced by [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span></span> <span data-ttu-id="62c20-178">這項資訊也會在透過 [**ICustomDestinationList：： AppendCategory**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory)將 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)目的地新增至自訂跳躍清單時使用。</span><span class="sxs-lookup"><span data-stu-id="62c20-178">This information is also used when adding [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem) destinations to custom Jump Lists through [**ICustomDestinationList::AppendCategory**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-appendcategory).</span></span>
-   <span data-ttu-id="62c20-179">在任何呼叫中，應用程式會直接進行 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs)。</span><span class="sxs-lookup"><span data-stu-id="62c20-179">In any call the application makes directly to [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs).</span></span> <span data-ttu-id="62c20-180">如果應用程式相依于 [一般檔案] 對話方塊來代表其呼叫 **SHAddToRecentDocs** ，則只有在整個進程已設定 AppUserModelID 時，這些呼叫才可以推算明確的 appusermodelid。</span><span class="sxs-lookup"><span data-stu-id="62c20-180">If the application depends on the common file dialog to make calls to **SHAddToRecentDocs** on its behalf, those calls can deduce the explicit AppUserModelID only if the AppUserModelID is set for the entire process.</span></span> <span data-ttu-id="62c20-181">如果應用程式在其視窗上設定 AppUserModelIDs，而不是在處理常式上，則應用程式必須使用其明確的 AppUserModelID 來進行 **SHAddToRecentDocs** 本身的所有呼叫，以及防止 [一般檔案] 對話方塊進行自己的呼叫。</span><span class="sxs-lookup"><span data-stu-id="62c20-181">If the application sets AppUserModelIDs on its windows instead of on the process, the application must make all calls to **SHAddToRecentDocs** itself, with its explicit AppUserModelID, as well as preventing the common file dialog from making its own calls.</span></span> <span data-ttu-id="62c20-182">您必須在開啟專案時完成這項操作，以確保應用程式捷徑清單的 **最新** 或 **經常** 區段正確無誤。</span><span class="sxs-lookup"><span data-stu-id="62c20-182">This must be done any time an item is opened, to ensure the **Recent** or **Frequent** sections of the application's Jump List are accurate.</span></span>

<span data-ttu-id="62c20-183">下列專案描述常見的案例，以及在這些案例中套用明確 AppUserModelIDs 的位置。</span><span class="sxs-lookup"><span data-stu-id="62c20-183">The following items describe common scenarios and where to apply explicit AppUserModelIDs in those scenarios.</span></span>

-   <span data-ttu-id="62c20-184">當單一進程包含多個應用程式時，請使用 [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow) 來取出視窗的屬性存放區，並將 AppUserModelID 設定為視窗屬性。</span><span class="sxs-lookup"><span data-stu-id="62c20-184">When a single process contains multiple applications, use [**SHGetPropertyStoreForWindow**](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow) to retrieve the window's property store and set the AppUserModelID as a window property.</span></span>
-   <span data-ttu-id="62c20-185">當應用程式使用多個進程時，請將 AppUserModelID 套用至每個進程。</span><span class="sxs-lookup"><span data-stu-id="62c20-185">When an application uses multiple processes, apply the AppUserModelID to each process.</span></span> <span data-ttu-id="62c20-186">您是否在每個程式上使用相同的 AppUserModelID，取決於您想要每個進程顯示為主要應用程式的一部分或個別實體。</span><span class="sxs-lookup"><span data-stu-id="62c20-186">Whether you use the same AppUserModelID on each process depends on whether you want each process to appear as part of the main application or as individual entities.</span></span>
-   <span data-ttu-id="62c20-187">若要將特定視窗與相同程式中的集合分開，請使用視窗的屬性存放區，將單一 AppUserModelID 套用至您想要分隔的視窗，然後將不同的 AppUserModelID 套用至該流程。</span><span class="sxs-lookup"><span data-stu-id="62c20-187">To separate certain windows from a set in the same process, use the window's property store to apply a single AppUserModelID to those windows you want to separate, and then apply a different AppUserModelID to the process.</span></span> <span data-ttu-id="62c20-188">該進程中未以視窗層級的 AppUserModelID 明確標示的任何視窗，會繼承程式的 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-188">Any window in that process that was not explicitly labeled with the window-level AppUserModelID inherits the AppUserModelID of the process.</span></span>
-   <span data-ttu-id="62c20-189">如果檔案類型與應用程式相關聯，請在檔案類型的 [ProgID](fa-progids.md) 註冊中指派 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-189">If a file type is associated with an application, assign the AppUserModelID in the file type's [ProgID](fa-progids.md) registration.</span></span> <span data-ttu-id="62c20-190">如果單一可執行檔以不同的模式啟動，並以不同的應用程式形式出現，則每種模式都需要個別的 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-190">If a single executable file is launched in different modes that appear to the user as distinct applications, a separate AppUserModelID is required for each mode.</span></span> <span data-ttu-id="62c20-191">在這種情況下，檔案類型必須有多個 ProgID 註冊，每個都有不同的 AppUserModelID 註冊。</span><span class="sxs-lookup"><span data-stu-id="62c20-191">In that case, there must be multiple ProgID registrations for the file type, each with a different AppUserModelID.</span></span>
-   <span data-ttu-id="62c20-192">當有多個快捷方式位置可讓使用者啟動應用程式時， (在 [ **開始** ] 功能表、桌面上或其他地方) 抓取快捷方式的屬性存放區，將單一 AppUserModelID 套用至所有快速鍵做為快捷方式屬性。</span><span class="sxs-lookup"><span data-stu-id="62c20-192">When there are multiple shortcut locations from which a user can launch an application (in the **Start** menu, on the desktop, or elsewhere) retrieve the shortcut's property store to apply a single AppUserModelID to all of the shortcuts as shortcut properties.</span></span>
-   <span data-ttu-id="62c20-193">當應用程式對 [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) 進行明確呼叫時，請在呼叫中使用 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-193">When an explicit call is made to [**SHAddToRecentDocs**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shaddtorecentdocs) by an application, use the AppUserModelID in the call.</span></span> <span data-ttu-id="62c20-194">當使用 [一般檔案] 對話方塊來開啟或儲存檔案時，對話方塊會代表應用程式呼叫 **SHAddToRecentDocs** 。</span><span class="sxs-lookup"><span data-stu-id="62c20-194">When the common file dialog is used to open or save files, **SHAddToRecentDocs** is called by the dialog on behalf of the application.</span></span> <span data-ttu-id="62c20-195">該呼叫可以從流程推斷明確的 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-195">That call can infer the explicit AppUserModelID from the process.</span></span> <span data-ttu-id="62c20-196">但是，如果將明確的 AppUserModelID 套用為視窗屬性，則 [一般檔案] 對話方塊無法判斷正確的 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-196">However, if an explicit AppUserModelID is applied as a window property, the common file dialog cannot determine the correct AppUserModelID.</span></span> <span data-ttu-id="62c20-197">在這種情況下，應用程式本身必須明確呼叫 **SHAddToRecentDocs** ，並提供正確的 AppUserModelID。</span><span class="sxs-lookup"><span data-stu-id="62c20-197">In that case, the application itself must explicitly call **SHAddToRecentDocs** and provide it with the correct AppUserModelID.</span></span> <span data-ttu-id="62c20-198">此外，應用程式必須藉由在 \_ [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog)或 [**IFILESAVEDIALOG**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog)的 **GetOptions** 方法中設定 FOS DONTADDTORECENT 旗標，來防止 [一般檔案] 對話方塊代表其呼叫 SHAddToRecentDocs。</span><span class="sxs-lookup"><span data-stu-id="62c20-198">Additionally, the application must prevent the common file dialog from calling **SHAddToRecentDocs** on its behalf by setting the FOS\_DONTADDTORECENT flag in the **GetOptions** method of [**IFileOpenDialog**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ifileopendialog) or [**IFileSaveDialog**](/windows/desktop/api/Shobjidl_core/nn-shobjidl_core-ifilesavedialog).</span></span>

## <a name="registering-an-application-as-a-host-process"></a><span data-ttu-id="62c20-199">將應用程式註冊為主機進程</span><span class="sxs-lookup"><span data-stu-id="62c20-199">Registering an Application as a Host Process</span></span>

<span data-ttu-id="62c20-200">應用程式可以設定 IsHostApp 登錄專案，讓工作列能夠將可執行檔的進程視為主機進程。</span><span class="sxs-lookup"><span data-stu-id="62c20-200">An application can set the IsHostApp registry entry to cause that executable's process to be considered a host process by the taskbar.</span></span> <span data-ttu-id="62c20-201">這會影響其群組和預設捷徑清單專案。</span><span class="sxs-lookup"><span data-stu-id="62c20-201">This affects its grouping and default Jump List entries.</span></span>

<span data-ttu-id="62c20-202">下列範例顯示必要的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="62c20-202">The following example shows the required registry entry.</span></span> <span data-ttu-id="62c20-203">請注意，不會指派值給專案。其目前狀態是必要的。</span><span class="sxs-lookup"><span data-stu-id="62c20-203">Note that the entry is not assigned a value; its presence is all that is required.</span></span> <span data-ttu-id="62c20-204">它是 REG \_ Null 值。</span><span class="sxs-lookup"><span data-stu-id="62c20-204">It is a REG\_NULL value.</span></span>

```
HKEY_CLASSES_ROOT
   Applications
      example.exe
         IsHostApp
```

<span data-ttu-id="62c20-205">如果處理常式本身或用來啟動進程的快捷方式檔案有明確的 AppUserModelID，則會忽略主機進程清單，並將應用程式視為一般的應用程式。</span><span class="sxs-lookup"><span data-stu-id="62c20-205">If either the process itself or the shortcut file used to launch the process has an explicit AppUserModelID, then the host process list is ignored and the application is treated as a normal application by the taskbar.</span></span> <span data-ttu-id="62c20-206">應用程式的執行中視窗會以單一工作列按鈕分組，並將應用程式釘選到工作列。</span><span class="sxs-lookup"><span data-stu-id="62c20-206">The application's running windows are grouped together under a single taskbar button and the application can be pinned to the taskbar.</span></span>

<span data-ttu-id="62c20-207">如果只知道執行中進程的可執行檔名稱（沒有明確的 AppUserModelID），而且該可執行檔位於主機進程清單中，則會將進程的每個實例視為工作列群組的個別實體。</span><span class="sxs-lookup"><span data-stu-id="62c20-207">If only the running process' executable name is known, without an explicit AppUserModelID, and that executable is in the host process list, then each instance of the process is treated as a separate entity for taskbar grouping.</span></span> <span data-ttu-id="62c20-208">與進程之任何特定實例相關聯的工作列按鈕，不會顯示 [釘選/取消釘選] 選項，也不會顯示新進程實例的啟動圖示。</span><span class="sxs-lookup"><span data-stu-id="62c20-208">The taskbar button associated with any specific instance of the process does not display a pin/unpin option or a launch icon for a new instance of the process.</span></span> <span data-ttu-id="62c20-209">此程式也不符合在 [ **開始** ] 功能表中最常使用的 (MFU) 清單中包含的資格。</span><span class="sxs-lookup"><span data-stu-id="62c20-209">The process is also not eligible for inclusion in the **Start** menu's Most Frequently Used (MFU) list.</span></span> <span data-ttu-id="62c20-210">但是，如果程式是透過包含啟動引數的快捷方式來啟動， (通常是以「應用程式」 ) 的目標內容，系統就會判斷身分識別，而且可以釘選和 relaunched 應用程式。</span><span class="sxs-lookup"><span data-stu-id="62c20-210">However, if the process was launched through a shortcut that contains launch arguments (usually the target content to host as the "application"), the system can determine identity and the application can be pinned and relaunched.</span></span>

## <a name="exclusion-lists-for-taskbar-pinning-and-recentfrequent-lists"></a><span data-ttu-id="62c20-211">工作列釘選和最近/頻繁清單的排除清單</span><span class="sxs-lookup"><span data-stu-id="62c20-211">Exclusion Lists for Taskbar Pinning and Recent/Frequent Lists</span></span>

<span data-ttu-id="62c20-212">應用程式、處理常式和 windows 可以選擇使其無法釘選到工作列，或包含在 [ **開始** ] 功能表的 最常使用清單中。</span><span class="sxs-lookup"><span data-stu-id="62c20-212">Applications, processes, and windows can choose to make themselves unavailable for pinning to the taskbar or for inclusion in the **Start** menu's MFU list.</span></span> <span data-ttu-id="62c20-213">有三種機制可達成此目的：</span><span class="sxs-lookup"><span data-stu-id="62c20-213">There are three mechanisms to accomplish this:</span></span>

1.  <span data-ttu-id="62c20-214">將 NoStartPage 專案新增至應用程式的註冊，如下所示：</span><span class="sxs-lookup"><span data-stu-id="62c20-214">Add the NoStartPage entry to the application's registration as shown here:</span></span>

    ```
    HKEY_CLASSES_ROOT
       Applications
          Example.exe
             NoStartPage
    ```

    <span data-ttu-id="62c20-215">與 NoStartPage 專案相關聯的資料會被忽略。</span><span class="sxs-lookup"><span data-stu-id="62c20-215">The data associated with the NoStartPage entry is ignored.</span></span> <span data-ttu-id="62c20-216">只需要存在專案。</span><span class="sxs-lookup"><span data-stu-id="62c20-216">Only the presence of the entry is required.</span></span> <span data-ttu-id="62c20-217">因此，NoStartPage 的理想型別為 REG \_ NONE。</span><span class="sxs-lookup"><span data-stu-id="62c20-217">Therefore, the ideal type for NoStartPage is REG\_NONE.</span></span>

    <span data-ttu-id="62c20-218">請注意，任何使用明確的 AppUserModelID 都會覆寫 NoStartPage 專案。</span><span class="sxs-lookup"><span data-stu-id="62c20-218">Note that any use of an explicit AppUserModelID overrides the NoStartPage entry.</span></span> <span data-ttu-id="62c20-219">如果已將明確的 AppUserModelID 套用至快捷方式、程式或視窗，它就會變成可釘選，而且符合 [ **開始** ] 功能表的 最常使用清單的資格。</span><span class="sxs-lookup"><span data-stu-id="62c20-219">If an explicit AppUserModelID is applied to a shortcut, process, or window, it becomes pinnable and eligible for the **Start** menu MFU list.</span></span>

2.  <span data-ttu-id="62c20-220">在 windows 和快捷方式上設定 [AppUserModel PreventPinning](../properties/props-system-appusermodel-preventpinning.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="62c20-220">Set the [System.AppUserModel.PreventPinning](../properties/props-system-appusermodel-preventpinning.md) property on windows and shortcuts.</span></span> <span data-ttu-id="62c20-221">您必須在 [PKEY \_ AppUserModel \_ ID](../properties/props-system-appusermodel-id.md) 屬性之前的視窗上設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="62c20-221">This property must be set on a window before the [PKEY\_AppUserModel\_ID](../properties/props-system-appusermodel-id.md) property.</span></span>
3.  <span data-ttu-id="62c20-222">將明確的 AppUserModelID 新增為下列登錄子機碼底下的值，如下所示：</span><span class="sxs-lookup"><span data-stu-id="62c20-222">Add an explicit AppUserModelID as a value under the following registry subkey as shown here:</span></span>

    ```
    HKEY_LOCAL_MACHINE
       Software
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      FileAssociation
                         NoStartPageAppUserModelIDs
                            AppUserModelID1
                            AppUserModelID2
                            AppUserModelID3
    ```

    <span data-ttu-id="62c20-223">每個專案都是 \_ 具有 AppUserModelID 名稱的 REG Null 值。</span><span class="sxs-lookup"><span data-stu-id="62c20-223">Each entry is a REG\_NULL value with the name of the AppUserModelID.</span></span> <span data-ttu-id="62c20-224">這份清單中所找到的任何 AppUserModelID 都不會可釘選，也不適合包含在 [ **開始** ] 功能表的 最常使用清單中。</span><span class="sxs-lookup"><span data-stu-id="62c20-224">Any AppUserModelID found in this list is not pinnable and not eligible for inclusion in the **Start** menu MFU list.</span></span>

<span data-ttu-id="62c20-225">請注意，某些可執行檔以及包含其名稱中特定字串的快捷方式，會自動排除，不要釘選和包含在 最常使用清單中。</span><span class="sxs-lookup"><span data-stu-id="62c20-225">Be aware that certain executable files as well as shortcuts that contain certain strings in their name are automatically excluded from pinning and inclusion in the MFU list.</span></span>

> [!Note]  
> <span data-ttu-id="62c20-226">您可以套用明確的 AppUserModelID 來覆寫此自動排除。</span><span class="sxs-lookup"><span data-stu-id="62c20-226">This automatic exclusion can be overridden by applying an explicit AppUserModelID.</span></span>

 

<span data-ttu-id="62c20-227">如果下列任何一個字串（不論大小寫）都包含在快捷方式名稱中，則不會可釘選程式，也不會顯示在最常使用的清單中 (不適用於 Windows 10) ：</span><span class="sxs-lookup"><span data-stu-id="62c20-227">If any of the following strings, regardless of case, are included in the shortcut name, the program is not pinnable and is not displayed in the most frequently used list (not applicable to Windows 10):</span></span>

-   <span data-ttu-id="62c20-228">文件</span><span class="sxs-lookup"><span data-stu-id="62c20-228">Documentation</span></span>
-   <span data-ttu-id="62c20-229">Help</span><span class="sxs-lookup"><span data-stu-id="62c20-229">Help</span></span>
-   <span data-ttu-id="62c20-230">安裝</span><span class="sxs-lookup"><span data-stu-id="62c20-230">Install</span></span>
-   <span data-ttu-id="62c20-231">其他資訊</span><span class="sxs-lookup"><span data-stu-id="62c20-231">More Info</span></span>
-   <span data-ttu-id="62c20-232">自述</span><span class="sxs-lookup"><span data-stu-id="62c20-232">Read me</span></span>
-   <span data-ttu-id="62c20-233">先閱讀</span><span class="sxs-lookup"><span data-stu-id="62c20-233">Read First</span></span>
-   <span data-ttu-id="62c20-234">讀我檔案</span><span class="sxs-lookup"><span data-stu-id="62c20-234">Readme</span></span>
-   <span data-ttu-id="62c20-235">移除</span><span class="sxs-lookup"><span data-stu-id="62c20-235">Remove</span></span>
-   <span data-ttu-id="62c20-236">設定</span><span class="sxs-lookup"><span data-stu-id="62c20-236">Setup</span></span>
-   <span data-ttu-id="62c20-237">支援</span><span class="sxs-lookup"><span data-stu-id="62c20-237">Support</span></span>
-   <span data-ttu-id="62c20-238">新功能</span><span class="sxs-lookup"><span data-stu-id="62c20-238">What's New</span></span>

<span data-ttu-id="62c20-239">下列程式清單不是可釘選，而且會從最常使用的清單中排除。</span><span class="sxs-lookup"><span data-stu-id="62c20-239">The following list of programs are not pinnable and are excluded from the most frequently used list.</span></span>

-   <span data-ttu-id="62c20-240">Applaunch.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-240">Applaunch.exe</span></span>
-   <span data-ttu-id="62c20-241">Control.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-241">Control.exe</span></span>
-   <span data-ttu-id="62c20-242">Dfsvc.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-242">Dfsvc.exe</span></span>
-   <span data-ttu-id="62c20-243">Dllhost.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-243">Dllhost.exe</span></span>
-   <span data-ttu-id="62c20-244">Guestmodemsg.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-244">Guestmodemsg.exe</span></span>
-   <span data-ttu-id="62c20-245">Hh.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-245">Hh.exe</span></span>
-   <span data-ttu-id="62c20-246">Install.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-246">Install.exe</span></span>
-   <span data-ttu-id="62c20-247">Isuninst.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-247">Isuninst.exe</span></span>
-   <span data-ttu-id="62c20-248">Lnkstub.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-248">Lnkstub.exe</span></span>
-   <span data-ttu-id="62c20-249">Mmc.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-249">Mmc.exe</span></span>
-   <span data-ttu-id="62c20-250">Mshta.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-250">Mshta.exe</span></span>
-   <span data-ttu-id="62c20-251">Msiexec.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-251">Msiexec.exe</span></span>
-   <span data-ttu-id="62c20-252">Msoobe.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-252">Msoobe.exe</span></span>
-   <span data-ttu-id="62c20-253">Rundll32.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-253">Rundll32.exe</span></span>
-   <span data-ttu-id="62c20-254">Setup.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-254">Setup.exe</span></span>
-   <span data-ttu-id="62c20-255">St5unst.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-255">St5unst.exe</span></span>
-   <span data-ttu-id="62c20-256">Unwise.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-256">Unwise.exe</span></span>
-   <span data-ttu-id="62c20-257">Unwise32.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-257">Unwise32.exe</span></span>
-   <span data-ttu-id="62c20-258">Werfault.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-258">Werfault.exe</span></span>
-   <span data-ttu-id="62c20-259">Winhlp32.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-259">Winhlp32.exe</span></span>
-   <span data-ttu-id="62c20-260">Wlrmdr.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-260">Wlrmdr.exe</span></span>
-   <span data-ttu-id="62c20-261">Wuapp.exe</span><span class="sxs-lookup"><span data-stu-id="62c20-261">Wuapp.exe</span></span>

<span data-ttu-id="62c20-262">上述的清單會儲存在下列登錄值中。</span><span class="sxs-lookup"><span data-stu-id="62c20-262">The preceding lists are stored in the following registry values.</span></span>

> [!Note]  
> <span data-ttu-id="62c20-263">應用程式不應修改這些清單。</span><span class="sxs-lookup"><span data-stu-id="62c20-263">These lists should not be modified by applications.</span></span> <span data-ttu-id="62c20-264">使用先前所列的其中一個排除清單方法來獲得相同的體驗。</span><span class="sxs-lookup"><span data-stu-id="62c20-264">Use one of the exclusion list methods listed previously for the same experience.</span></span>

 

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  FileAssociation
                     AddRemoveApps
                     HostApps
```

## <a name="related-topics"></a><span data-ttu-id="62c20-265">相關主題</span><span class="sxs-lookup"><span data-stu-id="62c20-265">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62c20-266">**SetCurrentProcessExplicitAppUserModelID**</span><span class="sxs-lookup"><span data-stu-id="62c20-266">**SetCurrentProcessExplicitAppUserModelID**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-setcurrentprocessexplicitappusermodelid)
</dt> <dt>

[<span data-ttu-id="62c20-267">**GetCurrentProcessExplicitAppUserModelID**</span><span class="sxs-lookup"><span data-stu-id="62c20-267">**GetCurrentProcessExplicitAppUserModelID**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-getcurrentprocessexplicitappusermodelid)
</dt> <dt>

[<span data-ttu-id="62c20-268">工作列擴充功能</span><span class="sxs-lookup"><span data-stu-id="62c20-268">Taskbar Extensions</span></span>](taskbar-extensions.md)
</dt> <dt>

[<span data-ttu-id="62c20-269">**ICustomDestinationList::SetAppID**</span><span class="sxs-lookup"><span data-stu-id="62c20-269">**ICustomDestinationList::SetAppID**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icustomdestinationlist-setappid)
</dt> <dt>

[<span data-ttu-id="62c20-270">**IApplicationDocumentLists::SetAppID**</span><span class="sxs-lookup"><span data-stu-id="62c20-270">**IApplicationDocumentLists::SetAppID**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdocumentlists-setappid)
</dt> <dt>

[<span data-ttu-id="62c20-271">**IApplicationDestinations::SetAppID**</span><span class="sxs-lookup"><span data-stu-id="62c20-271">**IApplicationDestinations::SetAppID**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iapplicationdestinations-setappid)
</dt> <dt>

[<span data-ttu-id="62c20-272">**SHGetPropertyStoreForWindow**</span><span class="sxs-lookup"><span data-stu-id="62c20-272">**SHGetPropertyStoreForWindow**</span></span>](/windows/win32/api/shellapi/nf-shellapi-shgetpropertystoreforwindow)
</dt> </dl>

 

 
