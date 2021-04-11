---
description: Windows Installer 可以修復、取代和驗證應用程式中包含的檔案。 如果任何與任何功能相關聯的檔案或登錄專案遺失或損毀，可能需要重新安裝部分或完整的應用程式。
ms.assetid: fab23ab9-f1ab-4743-b883-cffc29b0124b
title: 重新安裝功能或應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 645f7dbf95204d96202c71a120eafb6e6e054ac6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104115497"
---
# <a name="reinstalling-a-feature-or-application"></a><span data-ttu-id="e2a58-104">重新安裝功能或應用程式</span><span class="sxs-lookup"><span data-stu-id="e2a58-104">Reinstalling a Feature or Application</span></span>

<span data-ttu-id="e2a58-105">Windows Installer 可以修復、取代和驗證應用程式中包含的檔案。</span><span class="sxs-lookup"><span data-stu-id="e2a58-105">Windows Installer can repair, replace, and verify files contained in an application.</span></span> <span data-ttu-id="e2a58-106">如果任何與任何功能相關聯的檔案或登錄專案遺失或損毀，可能需要重新安裝部分或完整的應用程式。</span><span class="sxs-lookup"><span data-stu-id="e2a58-106">A partial or complete application reinstallation might be required if any files or registry entries associated with any feature are missing or corrupt.</span></span>

<span data-ttu-id="e2a58-107">重新安裝功能或應用程式時，也會重新安裝屬於功能或應用程式的所有服務、環境變數和自訂動作。</span><span class="sxs-lookup"><span data-stu-id="e2a58-107">When a feature or application is reinstalled, all the services, environment variables, and custom actions belonging to the feature or application are reinstalled as well.</span></span> <span data-ttu-id="e2a58-108">請注意，這表示在原始安裝和重新安裝之間對環境變數所做的任何變更都會遺失。</span><span class="sxs-lookup"><span data-stu-id="e2a58-108">Note that this means that any changes made to environment variables between the original installation and the reinstallation are lost.</span></span>

<span data-ttu-id="e2a58-109">下列清單包含重新安裝功能或產品的方法。</span><span class="sxs-lookup"><span data-stu-id="e2a58-109">The following list contains methods of reinstalling a feature or product.</span></span> <span data-ttu-id="e2a58-110">前兩個方法已由安裝程式自動化：</span><span class="sxs-lookup"><span data-stu-id="e2a58-110">The first two methods have been automated by the installer:</span></span>

-   <span data-ttu-id="e2a58-111">藉由呼叫 [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) 函數來修復、取代或驗證檔案。</span><span class="sxs-lookup"><span data-stu-id="e2a58-111">Repair, replace, or verify files by calling the [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) function.</span></span>
-   <span data-ttu-id="e2a58-112">藉由呼叫 [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) 函數來重新安裝整個產品。</span><span class="sxs-lookup"><span data-stu-id="e2a58-112">Reinstall the entire product by calling the [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) function.</span></span>
-   <span data-ttu-id="e2a58-113">透過 [重新安裝 ControlEvent](reinstall-controlevent.md)，重新安裝、取代或確認具有安裝程式 UI 控制項按鈕的檔案。</span><span class="sxs-lookup"><span data-stu-id="e2a58-113">Reinstall, replace, or verify files with an installer UI control button through the [Reinstall ControlEvent](reinstall-controlevent.md).</span></span>
-   <span data-ttu-id="e2a58-114">藉由設定 [**重新安裝**](reinstall.md) 屬性和 [**REINSTALLMODE**](reinstallmode.md) 屬性，從命令列重新安裝、取代或驗證檔案。</span><span class="sxs-lookup"><span data-stu-id="e2a58-114">Reinstall, replace, or verify files from a command line by setting the [**REINSTALL**](reinstall.md) property and the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>

<span data-ttu-id="e2a58-115">如需重新安裝功能或應用程式的詳細資訊，請參閱 [復原](resiliency.md)。</span><span class="sxs-lookup"><span data-stu-id="e2a58-115">For more information on reinstalling a feature or application, see [Resiliency](resiliency.md).</span></span>

<span data-ttu-id="e2a58-116">**使用安裝程式重新安裝產品**</span><span class="sxs-lookup"><span data-stu-id="e2a58-116">**To reinstall a product using the installer**</span></span>

-   <span data-ttu-id="e2a58-117">呼叫 [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta)。</span><span class="sxs-lookup"><span data-stu-id="e2a58-117">Call [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta).</span></span>

<span data-ttu-id="e2a58-118">**使用安裝程式重新安裝功能**</span><span class="sxs-lookup"><span data-stu-id="e2a58-118">**To reinstall a feature using the installer**</span></span>

-   <span data-ttu-id="e2a58-119">呼叫 [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea)。</span><span class="sxs-lookup"><span data-stu-id="e2a58-119">Call [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea).</span></span>

<span data-ttu-id="e2a58-120">**使用安裝程式使用者介面重新安裝產品或功能**</span><span class="sxs-lookup"><span data-stu-id="e2a58-120">**To reinstall a product or feature with an installer user interface**</span></span>

1.  <span data-ttu-id="e2a58-121">將專案加入至 [控制項資料表](control-table.md)，以將按鈕加入至指定的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e2a58-121">Add a button to the specified dialog box by adding an entry to the [Control table](control-table.md).</span></span>
2.  <span data-ttu-id="e2a58-122">將 [ReinstallMode ControlEvent](reinstallmode-controlevent.md) 加入至 ControlEvent 資料表，而對話方塊 \_ 和控制項欄位則 \_ 參考在步驟1中建立的按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="e2a58-122">Add a [ReinstallMode ControlEvent](reinstallmode-controlevent.md) to the ControlEvent table, with the Dialog\_ and Control\_ fields referencing the button control created in step 1.</span></span> <span data-ttu-id="e2a58-123">在 [引數] 欄位中，輸入字串，其中包含與您想要的重新安裝模式相對應的字母 (此欄位可接受的值與 [**REINSTALLMODE**](reinstallmode.md) 屬性) 所接受的值相同。</span><span class="sxs-lookup"><span data-stu-id="e2a58-123">In the Argument field, enter a string containing the letters corresponding to the reinstall modes you want (the acceptable values for this field are identical to those accepted for the [**REINSTALLMODE**](reinstallmode.md) property).</span></span> <span data-ttu-id="e2a58-124">此事件之排序資料行中的值應該是1。</span><span class="sxs-lookup"><span data-stu-id="e2a58-124">The value in the Ordering column for this event should be 1.</span></span>
3.  <span data-ttu-id="e2a58-125">將 [重新安裝 ControlEvent](reinstall-controlevent.md) 事件新增至 [ControlEvent 資料表](controlevent-table.md)，並再次參考相同的按鈕控制項。</span><span class="sxs-lookup"><span data-stu-id="e2a58-125">Add a [Reinstall ControlEvent](reinstall-controlevent.md) event to the [ControlEvent table](controlevent-table.md), again referencing the same button control.</span></span> <span data-ttu-id="e2a58-126">此事件的 [引數] 欄位通常都是 [全部]，以強制重新安裝所有功能，但您可以在此放置特定功能的名稱。</span><span class="sxs-lookup"><span data-stu-id="e2a58-126">The Argument field for this event will normally be ALL, to force reinstallation of all features, but you can place the name of a specific feature here.</span></span> <span data-ttu-id="e2a58-127">此事件之排序資料行中的值應該是2。</span><span class="sxs-lookup"><span data-stu-id="e2a58-127">The value in the Ordering column for this event should be 2.</span></span>
4.  <span data-ttu-id="e2a58-128">再新增一個系結至相同按鈕控制項的事件，以實際起始重新安裝。</span><span class="sxs-lookup"><span data-stu-id="e2a58-128">Add one more event tied to the same button control, to actually initiate the reinstallation.</span></span> <span data-ttu-id="e2a58-129">這可以是 EndDialog 事件 (具有傳回) 的引數。</span><span class="sxs-lookup"><span data-stu-id="e2a58-129">This can be an EndDialog event (with an argument of Return).</span></span> <span data-ttu-id="e2a58-130">不過，NewDialog 事件通常是在這裡用來跳到 **您確定要重新安裝？** 確認對話方塊。</span><span class="sxs-lookup"><span data-stu-id="e2a58-130">More typically, however, a NewDialog event would be used here to jump to an **Are you sure you want to reinstall?** confirmation dialog box.</span></span> <span data-ttu-id="e2a58-131">此事件之排序資料行中的值應為3。</span><span class="sxs-lookup"><span data-stu-id="e2a58-131">The value in the Ordering column for this event should be 3.</span></span>

    <span data-ttu-id="e2a58-132">如有需要，可以為單一對話方塊建立數個 [**重新安裝**](reinstall.md) 按鈕，讓使用者選取執行的重新安裝類型。</span><span class="sxs-lookup"><span data-stu-id="e2a58-132">If desired, several [**REINSTALL**](reinstall.md) buttons can be created for a single dialog box, allowing the user to select the type of reinstallation performed.</span></span> <span data-ttu-id="e2a58-133">在此情況下，每個按鈕都會依照上述程式中的說明來撰寫，每個按鈕都有不同的 [ReinstallMode ControlEvent](reinstallmode-controlevent.md) 參數。</span><span class="sxs-lookup"><span data-stu-id="e2a58-133">In this case, each button is authored as outlined in the preceding procedure, with a different [ReinstallMode ControlEvent](reinstallmode-controlevent.md) parameter for each button.</span></span>

<span data-ttu-id="e2a58-134">一旦將特定產品安裝 (與部分或所有產品功能) ，就可以在命令列執行重新安裝：</span><span class="sxs-lookup"><span data-stu-id="e2a58-134">Once a particular product has been installed (with some or all of the product's features), a reinstallation can be performed at the command line:</span></span>

<span data-ttu-id="e2a58-135">**從命令列重新安裝產品或功能**</span><span class="sxs-lookup"><span data-stu-id="e2a58-135">**To reinstall a product or feature from a command line**</span></span>

1.  <span data-ttu-id="e2a58-136">從命令提示字元中，指定 [**重新安裝**](reinstall.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="e2a58-136">From the command prompt, specify the [**REINSTALL**](reinstall.md) property.</span></span>
2.  <span data-ttu-id="e2a58-137">從命令提示字元中，指定 [**REINSTALLMODE**](reinstallmode.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="e2a58-137">From the command prompt, specify the [**REINSTALLMODE**](reinstallmode.md) property.</span></span>

    <span data-ttu-id="e2a58-138">指定這些屬性可讓使用者重新安裝產品的任何或所有功能。</span><span class="sxs-lookup"><span data-stu-id="e2a58-138">Specifying these properties allows the user to reinstall any or all of the product's features.</span></span> <span data-ttu-id="e2a58-139">您也可以指定重新安裝類型。</span><span class="sxs-lookup"><span data-stu-id="e2a58-139">The type of reinstallation can also be specified.</span></span> <span data-ttu-id="e2a58-140">例如，您可以指定只重新安裝完全遺失的檔案，或是只有損毀的檔案 (例如，總和檢查碼不符合實際檔案內容的任何可執行檔) 被取代。</span><span class="sxs-lookup"><span data-stu-id="e2a58-140">For example, you can specify that only those files that are completely missing should be reinstalled, or that only corrupt files (for example, any executable file whose checksum does not match the actual file contents) be replaced.</span></span>

 

 



