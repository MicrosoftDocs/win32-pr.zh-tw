---
description: 針對實作為 .exe 檔的主控台專案，不需要特殊的匯出或訊息處理。 您可以將任何 .exe 檔案註冊為命令物件，以在主控台資料夾中顯示進入點。
title: 如何註冊可執行檔主控台專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 778bac10fea661f73c0967401a7c708ebf6b8273
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026732"
---
# <a name="how-to-register-executable-control-panel-items"></a><span data-ttu-id="ef9ad-104">如何註冊可執行檔主控台專案</span><span class="sxs-lookup"><span data-stu-id="ef9ad-104">How to Register Executable Control Panel Items</span></span>

<span data-ttu-id="ef9ad-105">針對實作為 .exe 檔的主控台專案，不需要特殊的匯出或訊息處理。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-105">For Control Panel items that are implemented as .exe files, no special exports or message handling is required.</span></span> <span data-ttu-id="ef9ad-106">您可以將任何 .exe 檔案註冊為命令物件，以在主控台資料夾中顯示進入點。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-106">Any .exe file can be registered as a command object to appear with an entry point in the Control Panel folder.</span></span>

<span data-ttu-id="ef9ad-107">這裡使用範例來示範註冊需求。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-107">An example is used here to demonstrate the registration requirements.</span></span> <span data-ttu-id="ef9ad-108">此範例示範如何將稱為「 **我的設定** 」主控台專案註冊為命令物件，使其出現在 [主控台] 視窗中。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-108">The example shows how to register a Control Panel item called **My Settings** as a command object so that it appears in the Control Panel window.</span></span> <span data-ttu-id="ef9ad-109">當命令執行時，[ **我的設定** ] 視窗也會出現 `MyApp.exe /settings` 。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-109">The **My Settings** window also appears when the command `MyApp.exe /settings` is run.</span></span>

## <a name="instructions"></a><span data-ttu-id="ef9ad-110">指示</span><span class="sxs-lookup"><span data-stu-id="ef9ad-110">Instructions</span></span>

### <a name="step-1"></a><span data-ttu-id="ef9ad-111">步驟 1:</span><span class="sxs-lookup"><span data-stu-id="ef9ad-111">Step 1:</span></span>

<span data-ttu-id="ef9ad-112">產生主控台專案的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-112">Generate a GUID for the Control Panel item.</span></span> <span data-ttu-id="ef9ad-113">GUID 可唯一識別主控台專案。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-113">The GUID uniquely identifies the Control Panel item.</span></span> <span data-ttu-id="ef9ad-114">在此範例中， `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` 是主控台專案的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-114">In this example, `{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}` is the GUID of the Control Panel item.</span></span>

### <a name="step-2"></a><span data-ttu-id="ef9ad-115">步驟 2:</span><span class="sxs-lookup"><span data-stu-id="ef9ad-115">Step 2:</span></span>

<span data-ttu-id="ef9ad-116">使用 GUID 做為名稱，將子機碼新增到登錄中，如下所示。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-116">Using the GUID as a name, add a subkey to the registry as follows.</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               Explorer
                  ControlPanel
                     NameSpace
                        {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
                           (Default) = My Settings
```

<span data-ttu-id="ef9ad-117">預設專案的資料只是主控台專案的 REG \_ SZ 名稱。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-117">The data for the Default entry is simply the REG\_SZ name of the Control Panel item.</span></span> <span data-ttu-id="ef9ad-118">預設專案有助於識別 GUID 專案，但它是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-118">The Default entry can be useful to identify the GUID entry, but it is optional.</span></span>

### <a name="step-3"></a><span data-ttu-id="ef9ad-119">步驟 3：</span><span class="sxs-lookup"><span data-stu-id="ef9ad-119">Step 3:</span></span>

<span data-ttu-id="ef9ad-120">使用 GUID 做為名稱，將子機碼和其專案新增到登錄中，如下所示。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-120">Using the GUID as a name, add a subkey and its entries to the registry as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         (Default) = My Settings
         LocalizedString = @%ProgramFiles%\MyCorp\MyApp.exe,-9
         InfoTip = @%ProgramFiles%\MyCorp\MyApp.exe,-5
         System.ApplicationName = MyCorporation.MySettings
         System.ControlPanel.Category = 1,8
         System.Software.TasksFileUrl = %ProgramFiles%\MyCorp\MyApp\MyTaskLinks.xml
```

-   <span data-ttu-id="ef9ad-121">**Default**。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-121">**Default**.</span></span> <span data-ttu-id="ef9ad-122">REG \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-122">REG\_SZ.</span></span> <span data-ttu-id="ef9ad-123">主控台專案的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-123">The display name for the Control Panel item.</span></span>
-   <span data-ttu-id="ef9ad-124">**>localizedstring**。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-124">**LocalizedString**.</span></span> <span data-ttu-id="ef9ad-125">選擇性。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-125">Optional.</span></span> <span data-ttu-id="ef9ad-126">REG \_ sz 或 reg \_ 展開 \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-126">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="ef9ad-127">主控台專案之當地語系化名稱的模組名稱和字串資料表識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-127">The module name and string table ID of the localized name of the Control Panel item.</span></span> <span data-ttu-id="ef9ad-128">格式為 "at" 符號 ( @ ) 後面接著包含多語系消費者介面 (MUI) 字串資料表的 .exe 或 .dll 的名稱。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-128">The format is an "at" sign (@) followed by the name of the .exe or .dll that contains the Multilingual User Interface (MUI) string table.</span></span> <span data-ttu-id="ef9ad-129">環境變數可以用來取代路徑的一部分。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-129">Environment variables can be used as a substitute for a part of the path.</span></span> <span data-ttu-id="ef9ad-130">路徑和檔案名後面會接著逗號 (、) 和連字號 ( ) ，後面接著字串表中的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-130">The path and file name is followed by a comma (,) and a hyphen (-), followed by the ID in the string table.</span></span>

    <span data-ttu-id="ef9ad-131">如果模組沒有字串資料表，則此專案可以是顯示名稱字串。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-131">If the module does not have a string table, then this entry can simply be the display name string.</span></span> <span data-ttu-id="ef9ad-132">如果您只使用顯示名稱字串，而不是字串資料表，則名稱不會調整為目前的顯示語言。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-132">If you use only the display name string rather than a string table, the name does not adjust to the current display language.</span></span>

-   <span data-ttu-id="ef9ad-133">提示。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-133">**InfoTip**.</span></span> <span data-ttu-id="ef9ad-134">REG \_ sz 或 reg \_ 展開 \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-134">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="ef9ad-135">主控台專案的描述。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-135">A description of the Control Panel item.</span></span> <span data-ttu-id="ef9ad-136">這項資訊會顯示在滑鼠停留在專案的圖示上時所顯示的資訊提示中。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-136">This information is shown in an InfoTip that is displayed when the mouse hovers over the item's icon.</span></span> <span data-ttu-id="ef9ad-137">語法與用於 >localizedstring 的語法相同，包括只提供字串而非字串資料表參考的選項。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-137">The syntax is the same as that used for LocalizedString, including the option of simply providing a string rather than a string table reference.</span></span>
-   <span data-ttu-id="ef9ad-138">\*\*\*\* System.servicemodel。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-138">**System.ApplicationName**.</span></span> <span data-ttu-id="ef9ad-139">REG \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-139">REG\_SZ.</span></span> <span data-ttu-id="ef9ad-140">專案的正式名稱。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-140">The canonical name of the item.</span></span> <span data-ttu-id="ef9ad-141">Form 的命令 `control.exe /name System.ApplicationName` 會開啟此專案，例如 `control.exe /name MyCorporation.MySettings` 。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-141">The command of form `control.exe /name System.ApplicationName` opens the item; for example, `control.exe /name MyCorporation.MySettings`.</span></span> <span data-ttu-id="ef9ad-142">如需使用 Control.exe 的詳細資訊，請參閱 [執行主控台專案](executing-control-panel-items.md) 。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-142">See [Executing Control Panel Items](executing-control-panel-items.md) for more information on the use of Control.exe.</span></span>
-   <span data-ttu-id="ef9ad-143">**控制台類別**。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-143">**System.ControlPanel.Category**.</span></span> <span data-ttu-id="ef9ad-144">REG \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-144">REG\_SZ.</span></span> <span data-ttu-id="ef9ad-145">值，宣告出現專案的主控台類別目錄。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-145">A value that declares the Control Panel categories where the item appears.</span></span> <span data-ttu-id="ef9ad-146">多個類別會以逗號分隔。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-146">Multiple categories are separated by commas.</span></span> <span data-ttu-id="ef9ad-147">在上述範例的案例中，專案會指定 [我的 **設定** ] 專案應該出現在 [ **外觀] 和 [個人** 化] 和 [ **程式** ] 類別中。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-147">In the case of the example above, the entry specifies that the **My Settings** item should appear in both the **Appearance and Personalization** and **Programs** categories.</span></span> <span data-ttu-id="ef9ad-148">請參閱 [指派主控台類別](assigning-control-panel-categories.md) 以取得可能的類別值。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-148">See [Assigning Control Panel Categories](assigning-control-panel-categories.md) for possible category values.</span></span>
-   <span data-ttu-id="ef9ad-149">**System.software.tasksfileurl**。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-149">**System.Software.TasksFileUrl**.</span></span> <span data-ttu-id="ef9ad-150">REG \_ sz 或 reg \_ 展開 \_ SZ。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-150">REG\_SZ or REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="ef9ad-151">定義工作 [連結](creating-searchable-task-links.md)之 XML 檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-151">The path of the XML file that defines [task links](creating-searchable-task-links.md).</span></span> <span data-ttu-id="ef9ad-152">這可以是直接檔案路徑（如範例所示），或指定為模組名稱和資源識別碼（例如 "% ProgramFiles% \\ MyCorp \\ MyApp \\MyApp.exe，-31"）的內嵌資源。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-152">This can be a direct file path as shown in the example, or an embedded resource specified as a module name and resource ID such as "%ProgramFiles%\\MyCorp\\MyApp\\MyApp.exe,-31".</span></span>

### <a name="step-4"></a><span data-ttu-id="ef9ad-153">步驟 4：</span><span class="sxs-lookup"><span data-stu-id="ef9ad-153">Step 4:</span></span>

<span data-ttu-id="ef9ad-154">在相同的 GUID 子機碼下，將下列子機碼新增至登錄，以提供檔案的路徑，該檔案包含圖示和該檔案中映射的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-154">Under that same GUID subkey, add the following subkey to the registry to provide the path of the file that contains the icon and the resource ID of the image within that file.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         DefaultIcon
            (Default) = %ProgramFiles%\MyCorp\MyApp.exe,-2
```

<span data-ttu-id="ef9ad-155">請注意，雖然語法類似于稍早所討論的 >localizedstring 和提示專案，但不會使用 ' @ ' 字元做為 REG sz 中的前置詞， \_ 或 reg \_ EXPAND \_ 指定路徑的專案。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-155">Note that while the syntax is otherwise similar to the LocalizedString and InfoTip entries discussed earlier, no '@' character is used as a prefix in the REG\_SZ or REG\_EXPAND\_SZ entry that specifies the path.</span></span>

### <a name="step-5"></a><span data-ttu-id="ef9ad-156">步驟 5：</span><span class="sxs-lookup"><span data-stu-id="ef9ad-156">Step 5:</span></span>

<span data-ttu-id="ef9ad-157">將下列資訊新增至登錄，以提供使用者開啟主控台時由系統呼叫的命令。</span><span class="sxs-lookup"><span data-stu-id="ef9ad-157">Add the following information to the registry to provide the command that is called by the system when the user opens the Control Panel.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}
         Shell
            Open
               Command
                  (Default) = [REG_EXPAND_SZ] %ProgramFiles%\MyCorp\MyApp.exe /Settings
```

## <a name="related-topics"></a><span data-ttu-id="ef9ad-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="ef9ad-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ef9ad-159">註冊主控台專案</span><span class="sxs-lookup"><span data-stu-id="ef9ad-159">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="ef9ad-160">如何註冊 DLL 主控台專案</span><span class="sxs-lookup"><span data-stu-id="ef9ad-160">How To Register DLL Control Panel Items</span></span>](how-to-register-dll-control-panel-item-registration-.md)
</dt> </dl>

 

 



