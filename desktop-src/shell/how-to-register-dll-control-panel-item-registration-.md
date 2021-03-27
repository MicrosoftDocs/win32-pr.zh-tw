---
description: 在匯出 CPlApplet 函式的 DLL 中所執行的主控台專案，其註冊需求與 .exe 檔不同。
title: 如何註冊 DLL 主控台專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 37b82225dcb40487c60210752b2c15af23f95bd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103692979"
---
# <a name="how-to-register-dll-control-panel-items"></a><span data-ttu-id="05e39-103">如何註冊 DLL 主控台專案</span><span class="sxs-lookup"><span data-stu-id="05e39-103">How to Register DLL Control Panel Items</span></span>

> [!Note]  
> <span data-ttu-id="05e39-104">目前的執行指導方針指出新的主控台專案應該實作為 .exe 檔，而不是 cpl 檔。</span><span class="sxs-lookup"><span data-stu-id="05e39-104">Current implementation guidelines state that new Control Panel items should be implemented as .exe files rather than .cpl files.</span></span> <span data-ttu-id="05e39-105">下列資訊主要包含在舊版用途中。</span><span class="sxs-lookup"><span data-stu-id="05e39-105">The following information is included mainly for legacy purposes.</span></span>

 

<span data-ttu-id="05e39-106">在匯出 [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) 函式的 DLL 中所執行的主控台專案，其註冊需求與 .exe 檔不同。</span><span class="sxs-lookup"><span data-stu-id="05e39-106">Control Panel items that are implemented in a DLL that exports the [**CPlApplet**](/windows/win32/api/cpl/nc-cpl-applet_proc) function have different registration requirements than .exe files.</span></span> <span data-ttu-id="05e39-107">在 Windows XP 中，新主控台專案 Dll 應該安裝在 [Program Files] 資料夾下相關聯的應用程式資料夾中。</span><span class="sxs-lookup"><span data-stu-id="05e39-107">As of Windows XP, new Control Panel item DLLs should be installed in the associated application's folder under the Program Files folder.</span></span> <span data-ttu-id="05e39-108">使用 cpl 副檔名儲存在 System32 目錄中的專案不需要註冊;它們會自動顯示在主控台中。</span><span class="sxs-lookup"><span data-stu-id="05e39-108">Items that are stored in the System32 directory with a .cpl extension do not need to be registered; they are automatically shown in the Control Panel.</span></span> <span data-ttu-id="05e39-109">使用 **CPlApplet** 的所有其他主控台專案都必須以下列兩種方式之一進行註冊：</span><span class="sxs-lookup"><span data-stu-id="05e39-109">All other Control Panel items that use **CPlApplet** must be registered in one of two ways:</span></span>

-   <span data-ttu-id="05e39-110">如果要將主控台專案提供給所有使用者使用，請在每一部電腦上註冊路徑，方法是將 **REG \_ EXPAND \_ SZ** 值新增至 **HKEY \_ LOCAL \_ MACHINE** \\ **Software** \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **主控台** \\ **Cpls** 子機碼，並設定為 DLL 路徑。</span><span class="sxs-lookup"><span data-stu-id="05e39-110">If the Control Panel item is to be available to all users, register the path on a per-computer basis by adding a **REG\_EXPAND\_SZ** value to the **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Control Panel**\\**Cpls** subkey, set to the DLL path.</span></span>
-   <span data-ttu-id="05e39-111">如果主控台專案是以每個使用者為基礎，請使用 **HKEY \_ 目前 \_ 使用者** 做為根機碼，而不是 **HKEY \_ 本機 \_ 電腦**。</span><span class="sxs-lookup"><span data-stu-id="05e39-111">If the Control Panel item is to be available on a per-user basis, use **HKEY\_CURRENT\_USER** as the root key instead of **HKEY\_LOCAL\_MACHINE**.</span></span>

<span data-ttu-id="05e39-112">下列兩個範例會註冊 *MyCplApp* 主控台專案。</span><span class="sxs-lookup"><span data-stu-id="05e39-112">The following two examples register the *MyCplApp* Control Panel item.</span></span> <span data-ttu-id="05e39-113">DLL 的名稱為 MyCpl.cpl，位於 *MyCorp \\ MyApp* 應用程式目錄中。</span><span class="sxs-lookup"><span data-stu-id="05e39-113">The DLL is named MyCpl.cpl and is located in the *MyCorp\\MyApp* application directory.</span></span> <span data-ttu-id="05e39-114">第一個範例說明每一電腦的註冊。</span><span class="sxs-lookup"><span data-stu-id="05e39-114">This first example illustrates per-computer registration.</span></span>

## <a name="instructions"></a><span data-ttu-id="05e39-115">指示</span><span class="sxs-lookup"><span data-stu-id="05e39-115">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="05e39-116">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="05e39-116">Step 1:</span></span>

<span data-ttu-id="05e39-117">將這項資訊新增至登錄，以註冊 cpl 檔案的存在。</span><span class="sxs-lookup"><span data-stu-id="05e39-117">Add this information to the registry to register the existence of the .cpl file.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Cpls
                     MyCpl = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl
```

### <a name="step-2"></a><span data-ttu-id="05e39-118">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="05e39-118">Step 2:</span></span>

<span data-ttu-id="05e39-119">**Windows Vista 和更新版本：** 將此額外資訊新增至登錄，以提供主控台專案的 GUID。</span><span class="sxs-lookup"><span data-stu-id="05e39-119">**Windows Vista and later:** Add this additional information to the registry to provide a GUID for the Control Panel item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.AppId
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = {A newly generated GUID}
```

<span data-ttu-id="05e39-120">藉由產生可唯一識別主控台專案的 GUID，您可以將工作連結加入至主控台。</span><span class="sxs-lookup"><span data-stu-id="05e39-120">By generating a GUID to uniquely identify the Control Panel item, you can add task links to the Control Panel.</span></span> <span data-ttu-id="05e39-121">若沒有此 GUID，則無法將工作連結與主控台專案相關聯。</span><span class="sxs-lookup"><span data-stu-id="05e39-121">Without this GUID, there is no way for the task links to be associated with the Control Panel item.</span></span> <span data-ttu-id="05e39-122">請參閱 [建立主控台專案的可搜尋工作連結](creating-searchable-task-links.md)。</span><span class="sxs-lookup"><span data-stu-id="05e39-122">See [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

### <a name="step-3"></a><span data-ttu-id="05e39-123">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="05e39-123">Step 3:</span></span>

<span data-ttu-id="05e39-124">**Windows Vista 和更新版本：** 將下列資訊新增至登錄，以建立專案的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="05e39-124">**Windows Vista and later:** Add the following information to the registry to create a canonical name for the item.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ApplicationName
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] MyCorporation.MyCpl
```

<span data-ttu-id="05e39-125">藉由新增正式名稱，使用者可以輸入，從命令列啟動主控台專案 `control.exe /name MyCorporation.MyCpl` 。</span><span class="sxs-lookup"><span data-stu-id="05e39-125">By adding a canonical name, users can launch the Control Panel item from a command line by entering `control.exe /name MyCorporation.MyCpl`.</span></span> <span data-ttu-id="05e39-126">這也可以讓您稍後將某個專案的執行變更為 .exe 檔案，而不需要呼叫程式來進行任何變更，因為它們可以繼續透過其正式名稱開啟專案。</span><span class="sxs-lookup"><span data-stu-id="05e39-126">This also makes it possible to change an implementation from a .cpl file to a .exe file later, without requiring calling programs to make any changes since they can continue opening the item through its canonical name.</span></span> <span data-ttu-id="05e39-127">如需標準名稱的詳細資訊，請參閱 [執行主控台專案](executing-control-panel-items.md)。</span><span class="sxs-lookup"><span data-stu-id="05e39-127">For more information on canonical names, see [Executing Control Panel Items](executing-control-panel-items.md).</span></span>

### <a name="step-4"></a><span data-ttu-id="05e39-128">步驟 4：</span><span class="sxs-lookup"><span data-stu-id="05e39-128">Step 4:</span></span>

<span data-ttu-id="05e39-129">**Windows Vista 和更新版本：** 將下列資訊新增至登錄，以將主控台專案指派給一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="05e39-129">**Windows Vista and later:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.ControlPanel.Category
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="05e39-130">**WINDOWS XP：** 將下列資訊新增至登錄，以將主控台專案指派給一或多個類別。</span><span class="sxs-lookup"><span data-stu-id="05e39-130">**Windows XP:** Add the following information to the registry to assign a Control Panel item to one or more categories.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     {305CA226-D286-468e-B848-2B2E8E697B74} 2
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_DWORD] 3
```

<span data-ttu-id="05e39-131">此範例會將專案指派給類別3，也就是網路和網際網路。</span><span class="sxs-lookup"><span data-stu-id="05e39-131">This example assigns the item to category 3, which is Network and Internet.</span></span> <span data-ttu-id="05e39-132">若要將專案加入至多個類別，請以 \_ 逗號分隔的 REG SZ 值（例如 "3，8"）提供清單。</span><span class="sxs-lookup"><span data-stu-id="05e39-132">To add an item to multiple categories, provide the list as a REG\_SZ value separated by commas, such as "3,8".</span></span> <span data-ttu-id="05e39-133">值可以是十進位或十六進位。</span><span class="sxs-lookup"><span data-stu-id="05e39-133">Values can be provided as either decimal or hexadecimal.</span></span> <span data-ttu-id="05e39-134">請注意，只有在 Windows XP Service Pack 2 (SP2) 和更新版本中，才能將專案新增至多個類別目錄的功能。</span><span class="sxs-lookup"><span data-stu-id="05e39-134">Note that the ability to add an item to multiple categories is only possible in Windows XP Service Pack 2 (SP2) and later.</span></span> <span data-ttu-id="05e39-135">請參閱為所有可能的值 [指派主控台分類](assigning-control-panel-categories.md) 。</span><span class="sxs-lookup"><span data-stu-id="05e39-135">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for all possible values.</span></span>

### <a name="step-5"></a><span data-ttu-id="05e39-136">步驟 5：</span><span class="sxs-lookup"><span data-stu-id="05e39-136">Step 5:</span></span>

<span data-ttu-id="05e39-137">**Windows Vista 和更新版本：** 將下列資訊新增至登錄，以建立並指向 XML 檔案，以保存專案的工作連結。</span><span class="sxs-lookup"><span data-stu-id="05e39-137">**Windows Vista and later:** Add the following information to the registry to create and point to an XML file to hold task links for the item.</span></span> <span data-ttu-id="05e39-138">此值必須是 REG \_ SZ 路徑（如下所示）或模組和資源識別碼 (例如 "C： \\ Program Files \\ MyCorp \\ MyApp \\MyApp.exe，-31" ) （如果它是內嵌的資源）。</span><span class="sxs-lookup"><span data-stu-id="05e39-138">The value must be a REG\_SZ path as shown here or a module and resource ID (for example, "C:\\Program Files\\MyCorp\\MyApp\\MyApp.exe,-31") if it is an embedded resource.</span></span> <span data-ttu-id="05e39-139">應完整指定 XML 檔案的位置。</span><span class="sxs-lookup"><span data-stu-id="05e39-139">The location of the XML file should be fully specified.</span></span> <span data-ttu-id="05e39-140">它不能使用環境變數，例如% ProgramFiles%。</span><span class="sxs-lookup"><span data-stu-id="05e39-140">It cannot use an environment variable such as %ProgramFiles%.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows
            CurrentVersion
               Control Panel
                  Extended Properties
                     System.Software.TasksFileUrl
                        %ProgramFiles%\MyCorp\MyApp\MyCpl.cpl = [REG_SZ] C:\ProgramFiles\MyCorp\MyApp\MyTasks.xml
```

<span data-ttu-id="05e39-141">如需工作連結的詳細資訊，以及如何建立 XML 檔案來保存它們，請參閱 [建立主控台專案](creating-searchable-task-links.md)的可搜尋工作連結。</span><span class="sxs-lookup"><span data-stu-id="05e39-141">For more details on task links and how to create the XML file to hold them, see [Creating Searchable Task Links for a Control Panel Item](creating-searchable-task-links.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="05e39-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="05e39-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="05e39-143">註冊主控台專案</span><span class="sxs-lookup"><span data-stu-id="05e39-143">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="05e39-144">如何註冊可執行檔主控台專案</span><span class="sxs-lookup"><span data-stu-id="05e39-144">How To Register Executable Control Panel Items</span></span>](how-to-register-an-executable-control-panel-item-registration-.md)
</dt> </dl>

 

 
