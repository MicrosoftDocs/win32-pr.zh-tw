---
title: 適用于遊戲開發人員的 Windows 遊戲瀏覽器
description: 本文概述使用新的 GDF 架構，在 Windows Vista 和 Windows 7 上向遊戲瀏覽器和家長監護註冊遊戲的流程。
ms.assetid: 628f14bf-2714-0d68-8267-4f7f48c2774a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7f59b90a23f407be3990a6a4e24b92d39e66852
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968103"
---
# <a name="windows-games-explorer-for-game-developers"></a><span data-ttu-id="18e5c-103">適用于遊戲開發人員的 Windows 遊戲瀏覽器</span><span class="sxs-lookup"><span data-stu-id="18e5c-103">Windows Games Explorer for Game Developers</span></span>

<span data-ttu-id="18e5c-104">Windows Vista 包含 [遊戲瀏覽器]，藉以改善 Windows 遊戲的使用者體驗。</span><span class="sxs-lookup"><span data-stu-id="18e5c-104">Windows Vista improves the user experience of gaming on Windows by including Games Explorer.</span></span> <span data-ttu-id="18e5c-105">Windows Vista [開始] 功能表中的 [遊戲瀏覽器] 會在 [遊戲] 資料夾中公開，並提供存取遊戲的集中位置。</span><span class="sxs-lookup"><span data-stu-id="18e5c-105">Games Explorer is exposed in the Windows Vista Start Menu as the Games folder and provides a central location for accessing games.</span></span>

<span data-ttu-id="18e5c-106">從 DirectX SDK 2009 年3月版本開始，新的遊戲定義檔 (GDF) 架構可用來支援 Windows 7、遊戲提供者和 RSS 摘要以及 IGameExplorer2 中的功能。</span><span class="sxs-lookup"><span data-stu-id="18e5c-106">Starting with the March 2009 release of the DirectX SDK, a new game definition file (GDF) schema is used to support features in Windows 7, Game Provider and RSS feed, and IGameExplorer2.</span></span> <span data-ttu-id="18e5c-107">IGameExplorer2 是 Windows 7 的新介面，可簡化將遊戲與遊戲瀏覽器整合的流程。</span><span class="sxs-lookup"><span data-stu-id="18e5c-107">IGameExplorer2 is a new interface on Windows 7 that simplifies the process of integrating a game with Games Explorer.</span></span>

<span data-ttu-id="18e5c-108">本文概述使用新的 GDF 架構，在 Windows Vista 和 Windows 7 上向遊戲瀏覽器和家長監護註冊遊戲的流程。</span><span class="sxs-lookup"><span data-stu-id="18e5c-108">This article outlines the process of registering a game with Games Explorer and parental controls on Windows Vista and Windows 7 by using the new GDF schema.</span></span>

<span data-ttu-id="18e5c-109">內容: </span><span class="sxs-lookup"><span data-stu-id="18e5c-109">Contents:</span></span>

-   [<span data-ttu-id="18e5c-110">先決條件</span><span class="sxs-lookup"><span data-stu-id="18e5c-110">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="18e5c-111">與安裝程式整合</span><span class="sxs-lookup"><span data-stu-id="18e5c-111">Integrating with an Installer</span></span>](#integrating-with-an-installer)
-   [<span data-ttu-id="18e5c-112">整合流程</span><span class="sxs-lookup"><span data-stu-id="18e5c-112">Integration Process</span></span>](#integration-process)
-   [<span data-ttu-id="18e5c-113">遊戲瀏覽器工作</span><span class="sxs-lookup"><span data-stu-id="18e5c-113">Games Explorer Tasks</span></span>](#games-explorer-tasks)
-   [<span data-ttu-id="18e5c-114">整合至 InstallScript</span><span class="sxs-lookup"><span data-stu-id="18e5c-114">Integrating into InstallScript</span></span>](#integrating-into-installscript)
-   [<span data-ttu-id="18e5c-115">整合至 MSI 套件</span><span class="sxs-lookup"><span data-stu-id="18e5c-115">Integrating into an MSI Package</span></span>](#integrating-into-an-msi-package)
-   [<span data-ttu-id="18e5c-116">調試秘訣</span><span class="sxs-lookup"><span data-stu-id="18e5c-116">Debugging Tips</span></span>](#debugging-tips)
    -   [<span data-ttu-id="18e5c-117">使用範例程式碼進行測試</span><span class="sxs-lookup"><span data-stu-id="18e5c-117">Test with sample code</span></span>](#test-with-sample-code)
    -   [<span data-ttu-id="18e5c-118">確定您的遊戲已正確移除</span><span class="sxs-lookup"><span data-stu-id="18e5c-118">Make sure that your game was removed properly</span></span>](#make-sure-that-your-game-was-removed-properly)
    -   [<span data-ttu-id="18e5c-119">務必使用 Authenticode 簽署</span><span class="sxs-lookup"><span data-stu-id="18e5c-119">Be sure to sign using Authenticode</span></span>](#be-sure-to-sign-using-authenticode)
    -   [<span data-ttu-id="18e5c-120">確定可以使用家長監護</span><span class="sxs-lookup"><span data-stu-id="18e5c-120">Be sure that parental controls are available</span></span>](#be-sure-that-parental-controls-are-available)
    -   [<span data-ttu-id="18e5c-121">確認工作的類型正確</span><span class="sxs-lookup"><span data-stu-id="18e5c-121">Verify that tasks are of the correct type</span></span>](#verify-that-tasks-are-of-the-correct-type)
    -   [<span data-ttu-id="18e5c-122">確認 GDF 二進位檔中的資料</span><span class="sxs-lookup"><span data-stu-id="18e5c-122">Verify the data in GDF binary</span></span>](#verify-the-data-in-gdf-binary)
-   [<span data-ttu-id="18e5c-123">總結</span><span class="sxs-lookup"><span data-stu-id="18e5c-123">Summary</span></span>](#summary)

## <a name="prerequisites"></a><span data-ttu-id="18e5c-124">必要條件</span><span class="sxs-lookup"><span data-stu-id="18e5c-124">Prerequisites</span></span>

<span data-ttu-id="18e5c-125">您必須先建立遊戲定義檔 (GDF) ，才能將遊戲整合至 [遊戲] Explorer。</span><span class="sxs-lookup"><span data-stu-id="18e5c-125">Before you can integrate a game into Games Explorer, you must create a game definition file (GDF).</span></span> <span data-ttu-id="18e5c-126">GDF 是一個 XML 檔案，其中包含描述遊戲的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="18e5c-126">A GDF is an XML file that contains metadata that describes the game.</span></span> <span data-ttu-id="18e5c-127">在2009年3月的 DirectX SDK 版本中，已將遊戲提供者、RSS 摘要和遊戲工作的區段新增至 GDF 架構。</span><span class="sxs-lookup"><span data-stu-id="18e5c-127">In the March 2009 release of the DirectX SDK, a section for game provider, RSS feed, and game task has been added to the GDF schema.</span></span> <span data-ttu-id="18e5c-128">若要使用本文中的指示，您必須使用這個新的 GDF 格式來建立您的 GDF 檔案。</span><span class="sxs-lookup"><span data-stu-id="18e5c-128">To use the instructions in this article, you must use this new GDF format to create your GDF file.</span></span>

<span data-ttu-id="18e5c-129">Microsoft 提供的工具可讓您在 DirectX SDK 的遊戲定義檔編輯器中撰寫 GDFs，讓此建立程式更容易。</span><span class="sxs-lookup"><span data-stu-id="18e5c-129">Microsoft provides a tool for authoring GDFs in the DirectX SDK, Game Definition File Editor, to make this creation process easier.</span></span> <span data-ttu-id="18e5c-130">這項工具也可協助您建立當地語系化版本的 GDF。</span><span class="sxs-lookup"><span data-stu-id="18e5c-130">This tool also helps you create localized versions of a GDF.</span></span>

<span data-ttu-id="18e5c-131">撰寫和當地語系化 GDF 之後，它必須封裝在二進位檔案的資源區段內， (可執行檔或 DLL) ，以及遊戲的縮圖和圖示。</span><span class="sxs-lookup"><span data-stu-id="18e5c-131">Once a GDF has been authored and localized, it must be encapsulated within a resource section of a binary file (either an executable or DLL), along with the game's thumbnail and icon.</span></span> <span data-ttu-id="18e5c-132">GDF 包含與遊戲相關聯的所有中繼資料，包括遊戲的評等。</span><span class="sxs-lookup"><span data-stu-id="18e5c-132">The GDF contains all of the metadata associated with the game, including the game's rating.</span></span> <span data-ttu-id="18e5c-133">Windows 家長監護會使用遊戲的評等來允許家長監護遊戲的存取。</span><span class="sxs-lookup"><span data-stu-id="18e5c-133">Windows Parental Controls use the game's rating to allow parents to control access to the game.</span></span> <span data-ttu-id="18e5c-134">包含 GDF 的二進位檔案必須使用有效的 Authenticode 憑證以數位方式簽署;否則，[遊戲瀏覽器] 和 [家長監護] 系統會忽略遊戲的評等，因為無法信任評等資訊而不需要認證。</span><span class="sxs-lookup"><span data-stu-id="18e5c-134">The binary file which contains the GDF must be digitally signed with a valid Authenticode certificate; otherwise, Games Explorer and the parental control system ignores the game's rating, because the rating information cannot be trusted without certification.</span></span> <span data-ttu-id="18e5c-135">如需使用 Authenticode 簽署程式碼的詳細資訊，請參閱 [遊戲開發人員的 Authenticode 簽署](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)。</span><span class="sxs-lookup"><span data-stu-id="18e5c-135">For more details about signing code with Authenticode, see [Authenticode Signing for Game Developers](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).</span></span>

## <a name="integrating-with-an-installer"></a><span data-ttu-id="18e5c-136">與安裝程式整合</span><span class="sxs-lookup"><span data-stu-id="18e5c-136">Integrating with an Installer</span></span>

<span data-ttu-id="18e5c-137">為了簡化遊戲瀏覽器整合，GameUXInstallHelper 範例提供可在 Windows XP、Windows Vista 和 Windows 7 上呼叫的通用 API。</span><span class="sxs-lookup"><span data-stu-id="18e5c-137">To simplify Games Explorer integration, the GameUXInstallHelper sample provides a common API that can be called on Windows XP, Windows Vista, and Windows 7.</span></span> <span data-ttu-id="18e5c-138">它是設計用來處理 InstallShield 和取向安裝系統，以及 MSI 自訂動作和自訂安裝工具的腳本。</span><span class="sxs-lookup"><span data-stu-id="18e5c-138">It is designed to work with scripts for InstallShield and Wise Installation System, as well as MSI custom actions and custom installation tools.</span></span> <span data-ttu-id="18e5c-139">系統會在此範例 DLL 內處理作業系統的偵測，因此呼叫端不需要擔心用戶端是否執行 Windows XP、Windows Vista 或 Windows 7。</span><span class="sxs-lookup"><span data-stu-id="18e5c-139">Detection of the operating system is handled inside this sample DLL, so the caller does not need to worry whether the client is running Windows XP, Windows Vista, or Windows 7.</span></span>

<span data-ttu-id="18e5c-140">此 DLL 匯出的函式如下：</span><span class="sxs-lookup"><span data-stu-id="18e5c-140">The functions exported by this DLL are the following:</span></span>

<dl> <dt>

<span data-ttu-id="18e5c-141"><span id="GameExplorerInstallW"></span><span id="gameexplorerinstallw"></span><span id="GAMEEXPLORERINSTALLW"></span>**GameExplorerInstallW**</span><span class="sxs-lookup"><span data-stu-id="18e5c-141"><span id="GameExplorerInstallW"></span><span id="gameexplorerinstallw"></span><span id="GAMEEXPLORERINSTALLW"></span>**GameExplorerInstallW**</span></span>
</dt> <dd>

<span data-ttu-id="18e5c-142">在指定 GDF 二進位檔的路徑、安裝遊戲之資料夾的完整路徑，以及安裝範圍的情況下，向遊戲瀏覽器註冊遊戲。</span><span class="sxs-lookup"><span data-stu-id="18e5c-142">Registers a game with Games Explorer, given a path to the GDF binary, a full path to the folder where the game is installed, and the installation scope.</span></span>

</dd> <dt>

<span data-ttu-id="18e5c-143"><span id="GameExplorerInstallA"></span><span id="gameexplorerinstalla"></span><span id="GAMEEXPLORERINSTALLA"></span>**GameExplorerInstallA**</span><span class="sxs-lookup"><span data-stu-id="18e5c-143"><span id="GameExplorerInstallA"></span><span id="gameexplorerinstalla"></span><span id="GAMEEXPLORERINSTALLA"></span>**GameExplorerInstallA**</span></span>
</dt> <dd>

<span data-ttu-id="18e5c-144">使用遊戲瀏覽器註冊遊戲;ANSI 版本的 **GameExplorerInstallW**。</span><span class="sxs-lookup"><span data-stu-id="18e5c-144">Registers a game with Games Explorer; ANSI version of **GameExplorerInstallW**.</span></span>

</dd> <dt>

<span data-ttu-id="18e5c-145"><span id="GameExplorerUninstallW"></span><span id="gameexploreruninstallw"></span><span id="GAMEEXPLORERUNINSTALLW"></span>**GameExplorerUninstallW**</span><span class="sxs-lookup"><span data-stu-id="18e5c-145"><span id="GameExplorerUninstallW"></span><span id="gameexploreruninstallw"></span><span id="GAMEEXPLORERUNINSTALLW"></span>**GameExplorerUninstallW**</span></span>
</dt> <dd>

<span data-ttu-id="18e5c-146">藉由指定 GDF 二進位檔的路徑，移除遊戲瀏覽器註冊的遊戲。</span><span class="sxs-lookup"><span data-stu-id="18e5c-146">Removes a game from registration with Games Explorer, given a path to the GDF binary.</span></span>

</dd> <dt>

<span data-ttu-id="18e5c-147"><span id="GameExplorerUninstallA"></span><span id="gameexploreruninstalla"></span><span id="GAMEEXPLORERUNINSTALLA"></span>**GameExplorerUninstallA**</span><span class="sxs-lookup"><span data-stu-id="18e5c-147"><span id="GameExplorerUninstallA"></span><span id="gameexploreruninstalla"></span><span id="GAMEEXPLORERUNINSTALLA"></span>**GameExplorerUninstallA**</span></span>
</dt> <dd>

<span data-ttu-id="18e5c-148">使用遊戲瀏覽器移除註冊遊戲;ANSI 版本的 **GameExplorerUninstallW**。</span><span class="sxs-lookup"><span data-stu-id="18e5c-148">Removes a game from registration with Games Explorer; ANSI version of **GameExplorerUninstallW**.</span></span>

</dd> <dt>

<span data-ttu-id="18e5c-149"><span id="GameExplorerSetMSIProperties"></span><span id="gameexplorersetmsiproperties"></span><span id="GAMEEXPLORERSETMSIPROPERTIES"></span>**GameExplorerSetMSIProperties**</span><span class="sxs-lookup"><span data-stu-id="18e5c-149"><span id="GameExplorerSetMSIProperties"></span><span id="gameexplorersetmsiproperties"></span><span id="GAMEEXPLORERSETMSIPROPERTIES"></span>**GameExplorerSetMSIProperties**</span></span>
</dt> <dd>

<span data-ttu-id="18e5c-150">針對 MSI 延後自訂安裝的動作設定 CustomActionData 屬性。</span><span class="sxs-lookup"><span data-stu-id="18e5c-150">Configures the CustomActionData properties for the actions of an MSI deferred custom installation.</span></span> <span data-ttu-id="18e5c-151">本文稍後會詳細說明此函數的使用方式。</span><span class="sxs-lookup"><span data-stu-id="18e5c-151">Usage of this function is described in detail later in this article.</span></span>

</dd> <dt>

<span data-ttu-id="18e5c-152"><span id="GameExplorerInstallUsingMSI"></span><span id="gameexplorerinstallusingmsi"></span><span id="GAMEEXPLORERINSTALLUSINGMSI"></span>**GameExplorerInstallUsingMSI**</span><span class="sxs-lookup"><span data-stu-id="18e5c-152"><span id="GameExplorerInstallUsingMSI"></span><span id="gameexplorerinstallusingmsi"></span><span id="GAMEEXPLORERINSTALLUSINGMSI"></span>**GameExplorerInstallUsingMSI**</span></span>
</dt> <dd>

<span data-ttu-id="18e5c-153">將遊戲新增至遊戲瀏覽器;供 MSI 自訂動作安裝期間使用。</span><span class="sxs-lookup"><span data-stu-id="18e5c-153">Adds a game to Games Explorer; for use during an MSI custom action installation.</span></span>

</dd> <dt>

<span data-ttu-id="18e5c-154"><span id="GameExplorerUninstallUsingMSI"></span><span id="gameexploreruninstallusingmsi"></span><span id="GAMEEXPLORERUNINSTALLUSINGMSI"></span>**GameExplorerUninstallUsingMSI**</span><span class="sxs-lookup"><span data-stu-id="18e5c-154"><span id="GameExplorerUninstallUsingMSI"></span><span id="gameexploreruninstallusingmsi"></span><span id="GAMEEXPLORERUNINSTALLUSINGMSI"></span>**GameExplorerUninstallUsingMSI**</span></span>
</dt> <dd>

<span data-ttu-id="18e5c-155">從遊戲瀏覽器移除遊戲;供 MSI 自訂動作安裝期間使用。</span><span class="sxs-lookup"><span data-stu-id="18e5c-155">Remove a game from Games Explorer; for use during an MSI custom action installation.</span></span>

</dd> </dl>

<span data-ttu-id="18e5c-156">這些函數會在 GameUXInstallHelper 標頭中進一步說明。</span><span class="sxs-lookup"><span data-stu-id="18e5c-156">These functions are further explained in the GameUXInstallHelper.h header.</span></span>

## <a name="integration-process"></a><span data-ttu-id="18e5c-157">整合流程</span><span class="sxs-lookup"><span data-stu-id="18e5c-157">Integration Process</span></span>

<span data-ttu-id="18e5c-158">一旦將 GDF 和相關的檔案新增至二進位資源之後，就可以將該遊戲與遊戲瀏覽器整合。</span><span class="sxs-lookup"><span data-stu-id="18e5c-158">Once the GDF and related files have been added to a binary resource, it is then possible to integrate the game with Games Explorer.</span></span> <span data-ttu-id="18e5c-159">使用 **GameUXInstallHelper** 將簡化整合程式。</span><span class="sxs-lookup"><span data-stu-id="18e5c-159">Using **GameUXInstallHelper** will simplify the integration process.</span></span> <span data-ttu-id="18e5c-160">若要向遊戲瀏覽器註冊遊戲，請使用 GDF 二進位檔的路徑來呼叫 **GameExplorerInstall** 、安裝遊戲之資料夾的完整路徑，以及安裝領域。</span><span class="sxs-lookup"><span data-stu-id="18e5c-160">To register the game with Games Explorer, call the **GameExplorerInstall** with a path to the GDF binary, a full path to the folder where the game is installed, and the installation scope.</span></span> <span data-ttu-id="18e5c-161">若要移除遊戲的註冊，請使用 GDF 二進位檔的路徑來呼叫 **GameExplorerUninstall** 。</span><span class="sxs-lookup"><span data-stu-id="18e5c-161">To remove the game's registration, call **GameExplorerUninstall** with a path to the GDF binary.</span></span>

<span data-ttu-id="18e5c-162">請注意，移除流程只會移除一個唯一的安裝。</span><span class="sxs-lookup"><span data-stu-id="18e5c-162">Note that the removal process only removes one unique installation.</span></span> <span data-ttu-id="18e5c-163">如果遊戲已安裝多次，則必須針對每個獨特的安裝重複此程式。</span><span class="sxs-lookup"><span data-stu-id="18e5c-163">If a game has been installed multiple times, this process must be repeated for each unique installation.</span></span>

## <a name="games-explorer-tasks"></a><span data-ttu-id="18e5c-164">遊戲瀏覽器工作</span><span class="sxs-lookup"><span data-stu-id="18e5c-164">Games Explorer Tasks</span></span>

<span data-ttu-id="18e5c-165">[遊戲瀏覽器] 工作將會出現在 [遊戲瀏覽器] 中專案的內容功能表中。</span><span class="sxs-lookup"><span data-stu-id="18e5c-165">Games Explorer tasks will appear in the context menu of an item in Games Explorer.</span></span> <span data-ttu-id="18e5c-166">工作分為「播放」工作和支援工作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-166">Tasks are divided into play tasks and support tasks.</span></span> <span data-ttu-id="18e5c-167">「播放」工作會將遊戲啟動為特定模式，而支援工作則提供任何其他用途，包括連結至網站。</span><span class="sxs-lookup"><span data-stu-id="18e5c-167">Play tasks launch a game into a particular mode, while support tasks serve any other purpose, including linking to web sites.</span></span>

<span data-ttu-id="18e5c-168">在 Windows Vista 中，工作只是位於特定資料夾中的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="18e5c-168">In Windows Vista, tasks are simply shortcuts that are located in specific folders.</span></span> <span data-ttu-id="18e5c-169">播放工作和支援工作會儲存在具有對應名稱 PlayTasks 和 SupportTasks 的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="18e5c-169">Play tasks and support tasks are stored in folders with the corresponding names PlayTasks and SupportTasks.</span></span> <span data-ttu-id="18e5c-170">GameUXInstallHelper 可以從 GDF 的二進位檔讀取遊戲的工作資訊，並自動建立所有的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="18e5c-170">GameUXInstallHelper can read the game's task information from the GDF binary file and create all of the shortcuts automatically.</span></span>

<span data-ttu-id="18e5c-171">在 Windows 7 中，不需要工作的快捷方式，因為遊戲瀏覽器會直接從 GDF 二進位檔案取得所有工作資訊。</span><span class="sxs-lookup"><span data-stu-id="18e5c-171">In Windows 7, the shortcuts to the tasks are not needed, because Games Explorer obtains all of the task information directly from the GDF binary file.</span></span>

## <a name="integrating-into-installscript"></a><span data-ttu-id="18e5c-172">整合至 InstallScript</span><span class="sxs-lookup"><span data-stu-id="18e5c-172">Integrating into InstallScript</span></span>

<span data-ttu-id="18e5c-173">使用 GameUXInstallHelper 範例，可讓您輕鬆地從 InstallShield 的 InstallScript 呼叫遊戲瀏覽器 Api。</span><span class="sxs-lookup"><span data-stu-id="18e5c-173">Calling Games Explorer APIs from InstallShield's InstallScript is made easy by using the GameUXInstallHelper sample.</span></span> <span data-ttu-id="18e5c-174">與 InstallShield 整合所需的步驟如下：</span><span class="sxs-lookup"><span data-stu-id="18e5c-174">The steps required to integrate with InstallShield are as follows:</span></span>

1.  <span data-ttu-id="18e5c-175">在 InstallShield 編輯器中開啟 InstallScript 專案。</span><span class="sxs-lookup"><span data-stu-id="18e5c-175">Open an InstallScript project in the InstallShield editor.</span></span>
2.  <span data-ttu-id="18e5c-176">將 GameUXInstallHelper.dll 新增至要安裝到目標目錄的專案。</span><span class="sxs-lookup"><span data-stu-id="18e5c-176">Add GameUXInstallHelper.dll to the project to be installed to the target directory.</span></span>

    <span data-ttu-id="18e5c-177">**若要將 GameUXInstallHelper.dll 加入至 InstallScript 專案：**</span><span class="sxs-lookup"><span data-stu-id="18e5c-177">**To add GameUXInstallHelper.dll to an InstallScript project:**</span></span>

    1.  <span data-ttu-id="18e5c-178">在 [ **安裝設計** 工具] 索引標籤上，按一下左側導覽窗格中的 [ **應用程式資料** ]。</span><span class="sxs-lookup"><span data-stu-id="18e5c-178">On the **Installation Designer** tab, click **Application Data** in the navigation pane on the left.</span></span>
    2.  <span data-ttu-id="18e5c-179">按一下 [檔案 **和資料夾** ]，然後在 **來源電腦的資料夾** 中流覽，以找出 **來源電腦** 檔案中的 GameUXInstallerHelper.dll。</span><span class="sxs-lookup"><span data-stu-id="18e5c-179">Click **Files and Folders** and browse in **Source computer's folders** to locate GameUXInstallerHelper.dll in **Source computer's files**.</span></span>

        <span data-ttu-id="18e5c-180">GameUXInstallerHelper.dll 的預設位置為 DirectX SDK 根 \\ 範例 \\ c + + \\ 其他 \\ Bin \\ x86。</span><span class="sxs-lookup"><span data-stu-id="18e5c-180">The default location for GameUXInstallerHelper.dll is DirectX SDK root\\Samples\\C++\\Misc\\Bin\\x86.</span></span>

    3.  <span data-ttu-id="18e5c-181">在 [ **目的地電腦的資料夾**] 下，按一下 [ **應用程式目的檔案夾**]。</span><span class="sxs-lookup"><span data-stu-id="18e5c-181">Under **Destination computer's folders**, click **Application Target Folder**.</span></span>
    4.  <span data-ttu-id="18e5c-182">將 GameUXInstallerHelper.dll 從 **來源電腦的** 檔案拖曳至 **目的地電腦的** 檔案。</span><span class="sxs-lookup"><span data-stu-id="18e5c-182">Drag GameUXInstallerHelper.dll from **Source computer's files** to **Destination computer's files**.</span></span>

3.  <span data-ttu-id="18e5c-183">在 [InstallScript explorer] 中，按一下 InstallScript 檔案， (通常是 rul) 呼叫 DLL 函式。</span><span class="sxs-lookup"><span data-stu-id="18e5c-183">In the InstallScript explorer, click the InstallScript file (usually setup.rul) that calls the DLL function.</span></span>
4.  <span data-ttu-id="18e5c-184">將下列 InstallScript 貼到檔案中：</span><span class="sxs-lookup"><span data-stu-id="18e5c-184">Paste the following InstallScript into the file:</span></span>

    ``` syntax
    typedef GUID
    begin
    LONG  Data1;
    SHORT Data2;
    SHORT Data3;
    CHAR  Data4(8);
    end;

    prototype LONG GameUXInstallHelper.GameExplorerInstallW(WSTRING, WSTRING, NUMBER);
    prototype LONG GameUXInstallHelper.GameExplorerUninstallW(WSTRING);

    function OnMoved()

    WSTRING gdfbin[256];
    WSTRING path[256];
    NUMBER scope;

    begin

    if !MAINTENANCE then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    path = TARGETDIR;
    gdfbin = TARGETDIR ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    if ALLUSERS == 1 then
    scope = 3;
    else
    scope = 2;
    endif;

    GameUXInstallHelper.GameExplorerInstallW( gdfbin, path, scope);

    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;

    function OnMoving()

    WSTRING gdfbin[256];

    begin

    if MAINTENANCE && UNINST != "" then

    UseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UseDLL( WINSYSDIR ^ "OLE32.dll" );

    gdfbin = path ^ "bin\\ExampleGame.exe";  // TODO: Change this to point to binary containing the GDF

    GameUXInstallHelper.GameExplorerUninstallW(gdfbin);
    UnUseDLL( TARGETDIR ^ "GameUXInstallHelper.dll" );
    UnUseDLL( WINSYSDIR ^ "OLE32.dll" );

    endif;

    end;
    ```

## <a name="integrating-into-an-msi-package"></a><span data-ttu-id="18e5c-185">整合至 MSI 套件</span><span class="sxs-lookup"><span data-stu-id="18e5c-185">Integrating into an MSI Package</span></span>

<span data-ttu-id="18e5c-186">以下是使用 MSI 自訂動作呼叫遊戲瀏覽器 Api 所需步驟的高階描述：</span><span class="sxs-lookup"><span data-stu-id="18e5c-186">The following is a high-level description of the steps required to call the Games Explorer APIs using MSI custom actions:</span></span>

1.  <span data-ttu-id="18e5c-187">將屬性新增至名為 "RelativePathToGDF" 的 MSI 屬性工作表，其中包含 GDF 二進位檔的相對路徑。</span><span class="sxs-lookup"><span data-stu-id="18e5c-187">Add a property to the MSI Property table called "RelativePathToGDF" containing the relative path to the GDF binary.</span></span>
2.  <span data-ttu-id="18e5c-188">在 CostFinalize 動作之後，請在立即自訂動作中呼叫 GameUXInstallHelper DLL 函式 **SetMSIGameExplorerProperties** ，以針對其他自訂動作設定適當的 MSI 屬性。</span><span class="sxs-lookup"><span data-stu-id="18e5c-188">After the CostFinalize action, call the GameUXInstallHelper DLL function **SetMSIGameExplorerProperties** in an immediate custom action to set the appropriate MSI properties for the other custom actions.</span></span>
3.  <span data-ttu-id="18e5c-189">在安裝時，會在呼叫 GameUXInstallHelper DLL 函式 **AddToGameExplorerUsingMSI** 的 InstallFiles 動作之後觸發延遲的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-189">Upon installation, trigger a deferred custom action after the InstallFiles action that calls the GameUXInstallHelper DLL function **AddToGameExplorerUsingMSI**.</span></span> <span data-ttu-id="18e5c-190">如果安裝適用于所有使用者，則自訂動作必須設定旗標 msidbCustomActionTypeNoImpersonate;否則，它不能設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="18e5c-190">If the installation is for all users, then the custom action must set the flag msidbCustomActionTypeNoImpersonate; otherwise, it must not set this flag.</span></span> <span data-ttu-id="18e5c-191">因此，會定義兩個幾乎相同的自訂動作： GameUXAddAsAdmin 和 GameUXAddAsCurUser。</span><span class="sxs-lookup"><span data-stu-id="18e5c-191">Therefore, two nearly identical custom actions are defined: GameUXAddAsAdmin and GameUXAddAsCurUser.</span></span>
4.  <span data-ttu-id="18e5c-192">移除安裝之後，在呼叫 GameUXInstallHelper DLL 函式 **RemoveFromGameExplorerUsingMSI** 的 RemoveFiles 動作之前觸發延遲的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-192">Upon removal of the installation, trigger a deferred custom action before the RemoveFiles action that calls the GameUXInstallHelper DLL function **RemoveFromGameExplorerUsingMSI**.</span></span> <span data-ttu-id="18e5c-193">如果是針對所有使用者進行安裝，則自訂動作必須設定旗標 msidbCustomActionTypeNoImpersonate;否則，它不能設定這個旗標。</span><span class="sxs-lookup"><span data-stu-id="18e5c-193">If the installation was for all users, then the custom action must set the flag msidbCustomActionTypeNoImpersonate; otherwise, it must not set this flag.</span></span> <span data-ttu-id="18e5c-194">因此，會定義兩個幾乎相同的自訂動作： GameUXRemoveAsAdmin 和 GameUXRemoveAsCurUser。</span><span class="sxs-lookup"><span data-stu-id="18e5c-194">Therefore, two nearly identical custom actions are defined: GameUXRemoveAsAdmin and GameUXRemoveAsCurUser.</span></span>
5.  <span data-ttu-id="18e5c-195">定義復原自訂動作，以處理使用者在其中一個自訂動作已發生之後取消安裝或移除的情況。</span><span class="sxs-lookup"><span data-stu-id="18e5c-195">Define rollback custom actions to handle the case where the user cancels installing or removing after one of the these custom actions has already happened.</span></span> <span data-ttu-id="18e5c-196">這會產生額外4個自訂動作： GameUXRollBackAddAsAdmin、GameUXRollBackAddAsCurUser、GameUXRollBackRemoveAsAdmin 和 GameUXRollBackRemoveAsCurUser。</span><span class="sxs-lookup"><span data-stu-id="18e5c-196">This results in an additional 4 custom actions: GameUXRollBackAddAsAdmin, GameUXRollBackAddAsCurUser, GameUXRollBackRemoveAsAdmin, and GameUXRollBackRemoveAsCurUser.</span></span>

<span data-ttu-id="18e5c-197">下列指示會詳細說明此程式，其描述可使用 MSI 編輯器（例如在 Platform SDK 中找到的 Orca 編輯器）完成的程式。</span><span class="sxs-lookup"><span data-stu-id="18e5c-197">This procedure is described in detail in the following instructions, which describe a process that can be done using an MSI editor, such as the Orca editor found in the Platform SDK.</span></span> <span data-ttu-id="18e5c-198">有些 MSI 編輯器具有可簡化其中一些設定步驟的嚮導。</span><span class="sxs-lookup"><span data-stu-id="18e5c-198">Some MSI editors have wizards which simplify some of these configuration steps.</span></span>

<span data-ttu-id="18e5c-199">**設定 MSI 套件以與遊戲瀏覽器整合**</span><span class="sxs-lookup"><span data-stu-id="18e5c-199">**To configure an MSI package for integration with Games Explorer**</span></span>

1.  <span data-ttu-id="18e5c-200">以 Orca 開啟 MSI 套件。</span><span class="sxs-lookup"><span data-stu-id="18e5c-200">Open the MSI package in Orca.</span></span>
2.  <span data-ttu-id="18e5c-201">將下表中顯示的資料列加入至 MSI 封裝中的 **二進位** 資料表。</span><span class="sxs-lookup"><span data-stu-id="18e5c-201">Add the row shown in the following table to the **Binary** table in the MSI package.</span></span> 

    | <span data-ttu-id="18e5c-202">Name</span><span class="sxs-lookup"><span data-stu-id="18e5c-202">Name</span></span>   | <span data-ttu-id="18e5c-203">資料</span><span class="sxs-lookup"><span data-stu-id="18e5c-203">Data</span></span>                                          |
    |--------|-----------------------------------------------|
    | <span data-ttu-id="18e5c-204">GAMEUX</span><span class="sxs-lookup"><span data-stu-id="18e5c-204">GAMEUX</span></span> | <span data-ttu-id="18e5c-205">DLL 的檔案路徑 \\GameUXInstallHelper.dll</span><span class="sxs-lookup"><span data-stu-id="18e5c-205">file path to the DLL\\GameUXInstallHelper.dll</span></span> |

    

     

    > [!Note]  
    > <span data-ttu-id="18e5c-206">此檔案將內嵌在 MSI 套件中，因此您必須在每次重新編譯 GameUXInstallHelper.dll 時執行此步驟。</span><span class="sxs-lookup"><span data-stu-id="18e5c-206">This file will be embedded in the MSI package, so you must do this step every time you recompile GameUXInstallHelper.dll.</span></span>

     

3.  <span data-ttu-id="18e5c-207">將下表中顯示的資料列加入至 MSI 封裝中的 **CustomAction** 資料表。</span><span class="sxs-lookup"><span data-stu-id="18e5c-207">Add the rows shown in the following table to the **CustomAction** table in the MSI package.</span></span>

    | <span data-ttu-id="18e5c-208">動作</span><span class="sxs-lookup"><span data-stu-id="18e5c-208">Action</span></span>                        | <span data-ttu-id="18e5c-209">類型</span><span class="sxs-lookup"><span data-stu-id="18e5c-209">Type</span></span>                                                                                                                                                                                                   | <span data-ttu-id="18e5c-210">來源</span><span class="sxs-lookup"><span data-stu-id="18e5c-210">Source</span></span> | <span data-ttu-id="18e5c-211">目標</span><span class="sxs-lookup"><span data-stu-id="18e5c-211">Target</span></span>                         |
    |-------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------|--------------------------------|
    | <span data-ttu-id="18e5c-212">GameUXSetMSIProperties</span><span class="sxs-lookup"><span data-stu-id="18e5c-212">GameUXSetMSIProperties</span></span>        | <span data-ttu-id="18e5c-213">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65</span><span class="sxs-lookup"><span data-stu-id="18e5c-213">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue = 65</span></span>                                                                                                        | <span data-ttu-id="18e5c-214">GAMEUX</span><span class="sxs-lookup"><span data-stu-id="18e5c-214">GAMEUX</span></span> | <span data-ttu-id="18e5c-215">SetMSIGameExplorerProperties</span><span class="sxs-lookup"><span data-stu-id="18e5c-215">SetMSIGameExplorerProperties</span></span>   |
    | <span data-ttu-id="18e5c-216">GameUXAddAsAdmin</span><span class="sxs-lookup"><span data-stu-id="18e5c-216">GameUXAddAsAdmin</span></span>              | <span data-ttu-id="18e5c-217">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137</span><span class="sxs-lookup"><span data-stu-id="18e5c-217">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137</span></span>                                 | <span data-ttu-id="18e5c-218">GAMEUX</span><span class="sxs-lookup"><span data-stu-id="18e5c-218">GAMEUX</span></span> | <span data-ttu-id="18e5c-219">AddToGameExplorerUsingMSI</span><span class="sxs-lookup"><span data-stu-id="18e5c-219">AddToGameExplorerUsingMSI</span></span>      |
    | <span data-ttu-id="18e5c-220">GameUXAddAsCurUser</span><span class="sxs-lookup"><span data-stu-id="18e5c-220">GameUXAddAsCurUser</span></span>            | <span data-ttu-id="18e5c-221">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089</span><span class="sxs-lookup"><span data-stu-id="18e5c-221">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089</span></span>                                                                      | <span data-ttu-id="18e5c-222">GAMEUX</span><span class="sxs-lookup"><span data-stu-id="18e5c-222">GAMEUX</span></span> | <span data-ttu-id="18e5c-223">AddToGameExplorerUsingMSI</span><span class="sxs-lookup"><span data-stu-id="18e5c-223">AddToGameExplorerUsingMSI</span></span>      |
    | <span data-ttu-id="18e5c-224">GameUXRollBackAddAsAdmin</span><span class="sxs-lookup"><span data-stu-id="18e5c-224">GameUXRollBackAddAsAdmin</span></span>      | <span data-ttu-id="18e5c-225">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393</span><span class="sxs-lookup"><span data-stu-id="18e5c-225">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393</span></span> | <span data-ttu-id="18e5c-226">GAMEUX</span><span class="sxs-lookup"><span data-stu-id="18e5c-226">GAMEUX</span></span> | <span data-ttu-id="18e5c-227">RemoveFromGameExplorerUsingMSI</span><span class="sxs-lookup"><span data-stu-id="18e5c-227">RemoveFromGameExplorerUsingMSI</span></span> |
    | <span data-ttu-id="18e5c-228">GameUXRollBackAddAsCurUser</span><span class="sxs-lookup"><span data-stu-id="18e5c-228">GameUXRollBackAddAsCurUser</span></span>    | <span data-ttu-id="18e5c-229">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345</span><span class="sxs-lookup"><span data-stu-id="18e5c-229">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345</span></span>                                      | <span data-ttu-id="18e5c-230">GAMEUX</span><span class="sxs-lookup"><span data-stu-id="18e5c-230">GAMEUX</span></span> | <span data-ttu-id="18e5c-231">RemoveFromGameExplorerUsingMSI</span><span class="sxs-lookup"><span data-stu-id="18e5c-231">RemoveFromGameExplorerUsingMSI</span></span> |
    | <span data-ttu-id="18e5c-232">GameUXRemoveAsAdmin</span><span class="sxs-lookup"><span data-stu-id="18e5c-232">GameUXRemoveAsAdmin</span></span>           | <span data-ttu-id="18e5c-233">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137</span><span class="sxs-lookup"><span data-stu-id="18e5c-233">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3137</span></span>                                 | <span data-ttu-id="18e5c-234">GAMEUX</span><span class="sxs-lookup"><span data-stu-id="18e5c-234">GAMEUX</span></span> | <span data-ttu-id="18e5c-235">RemoveFromGameExplorerUsingMSI</span><span class="sxs-lookup"><span data-stu-id="18e5c-235">RemoveFromGameExplorerUsingMSI</span></span> |
    | <span data-ttu-id="18e5c-236">GameUXRemoveAsCurUser</span><span class="sxs-lookup"><span data-stu-id="18e5c-236">GameUXRemoveAsCurUser</span></span>         | <span data-ttu-id="18e5c-237">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089</span><span class="sxs-lookup"><span data-stu-id="18e5c-237">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeInScript = 1089</span></span>                                                                      | <span data-ttu-id="18e5c-238">GAMEUX</span><span class="sxs-lookup"><span data-stu-id="18e5c-238">GAMEUX</span></span> | <span data-ttu-id="18e5c-239">RemoveFromGameExplorerUsingMSI</span><span class="sxs-lookup"><span data-stu-id="18e5c-239">RemoveFromGameExplorerUsingMSI</span></span> |
    | <span data-ttu-id="18e5c-240">GameUXRollBackRemoveAsAdmin</span><span class="sxs-lookup"><span data-stu-id="18e5c-240">GameUXRollBackRemoveAsAdmin</span></span>   | <span data-ttu-id="18e5c-241">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393</span><span class="sxs-lookup"><span data-stu-id="18e5c-241">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript + msidbCustomActionTypeNoImpersonate = 3393</span></span> | <span data-ttu-id="18e5c-242">GAMEUX</span><span class="sxs-lookup"><span data-stu-id="18e5c-242">GAMEUX</span></span> | <span data-ttu-id="18e5c-243">AddToGameExplorerUsingMSI</span><span class="sxs-lookup"><span data-stu-id="18e5c-243">AddToGameExplorerUsingMSI</span></span>      |
    | <span data-ttu-id="18e5c-244">GameUXRollBackRemoveAsCurUser</span><span class="sxs-lookup"><span data-stu-id="18e5c-244">GameUXRollBackRemoveAsCurUser</span></span> | <span data-ttu-id="18e5c-245">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345</span><span class="sxs-lookup"><span data-stu-id="18e5c-245">msidbCustomActionTypeDll + msidbCustomActionTypeBinaryData + msidbCustomActionTypeContinue + msidbCustomActionTypeRollback + msidbCustomActionTypeInScript = 1345</span></span>                                      | <span data-ttu-id="18e5c-246">GAMEUX</span><span class="sxs-lookup"><span data-stu-id="18e5c-246">GAMEUX</span></span> | <span data-ttu-id="18e5c-247">AddToGameExplorerUsingMSI</span><span class="sxs-lookup"><span data-stu-id="18e5c-247">AddToGameExplorerUsingMSI</span></span>      |

    

     

4.  <span data-ttu-id="18e5c-248">將下表中的 [動作]、[條件] 和 [順序] 所顯示的值，加入至 MSI 封裝中的 **InstallExecuteSequence** 資料表。</span><span class="sxs-lookup"><span data-stu-id="18e5c-248">Add the values shown for Action, Condition, and Sequence in the following table to the **InstallExecuteSequence** table in the MSI package.</span></span>

    | <span data-ttu-id="18e5c-249">動作</span><span class="sxs-lookup"><span data-stu-id="18e5c-249">Action</span></span>                        | <span data-ttu-id="18e5c-250">條件</span><span class="sxs-lookup"><span data-stu-id="18e5c-250">Condition</span></span>                      | <span data-ttu-id="18e5c-251">順序</span><span class="sxs-lookup"><span data-stu-id="18e5c-251">Sequence</span></span> | <span data-ttu-id="18e5c-252">備註</span><span class="sxs-lookup"><span data-stu-id="18e5c-252">Notes</span></span>                                                                                                                                                                                            |
    |-------------------------------|--------------------------------|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="18e5c-253">GameUXSetMSIProperties</span><span class="sxs-lookup"><span data-stu-id="18e5c-253">GameUXSetMSIProperties</span></span>        |                                | <span data-ttu-id="18e5c-254">1015</span><span class="sxs-lookup"><span data-stu-id="18e5c-254">1015</span></span>     | <span data-ttu-id="18e5c-255">序號會在 CostFinalize 之後立即放置動作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-255">The sequence number places the action soon after CostFinalize.</span></span>                                                                                                                                   |
    | <span data-ttu-id="18e5c-256">GameUXAddAsAdmin</span><span class="sxs-lookup"><span data-stu-id="18e5c-256">GameUXAddAsAdmin</span></span>              | <span data-ttu-id="18e5c-257">未安裝和 ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="18e5c-257">NOT Installed AND ALLUSERS</span></span>     | <span data-ttu-id="18e5c-258">4003</span><span class="sxs-lookup"><span data-stu-id="18e5c-258">4003</span></span>     | <span data-ttu-id="18e5c-259">此自訂動作只會在所有使用者的全新安裝期間發生。</span><span class="sxs-lookup"><span data-stu-id="18e5c-259">This custom action will only happen during a fresh installation for all users.</span></span> <span data-ttu-id="18e5c-260">序號會將動作放在 InstallFiles 之後和復原之後。</span><span class="sxs-lookup"><span data-stu-id="18e5c-260">The sequence number places the action after InstallFiles and after the rollbacks.</span></span>                                 |
    | <span data-ttu-id="18e5c-261">GameUXAddAsCurUser</span><span class="sxs-lookup"><span data-stu-id="18e5c-261">GameUXAddAsCurUser</span></span>            | <span data-ttu-id="18e5c-262">未安裝且未進行 ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="18e5c-262">NOT Installed AND NOT ALLUSERS</span></span> | <span data-ttu-id="18e5c-263">4004</span><span class="sxs-lookup"><span data-stu-id="18e5c-263">4004</span></span>     | <span data-ttu-id="18e5c-264">此自訂動作只會在目前使用者的全新安裝期間發生。</span><span class="sxs-lookup"><span data-stu-id="18e5c-264">This custom action will only happen during a fresh installation for the current user only.</span></span> <span data-ttu-id="18e5c-265">序號會將動作放在 InstallFiles 之後和復原之後。</span><span class="sxs-lookup"><span data-stu-id="18e5c-265">The sequence number places the action after InstallFiles and after the rollbacks.</span></span>                     |
    | <span data-ttu-id="18e5c-266">GameUXRollBackAddAsAdmin</span><span class="sxs-lookup"><span data-stu-id="18e5c-266">GameUXRollBackAddAsAdmin</span></span>      | <span data-ttu-id="18e5c-267">未安裝和 ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="18e5c-267">NOT Installed AND ALLUSERS</span></span>     | <span data-ttu-id="18e5c-268">4001</span><span class="sxs-lookup"><span data-stu-id="18e5c-268">4001</span></span>     | <span data-ttu-id="18e5c-269">只有在所有使用者的全新安裝都已取消時，才會發生這個自訂動作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-269">This custom action will only happen when a fresh installation for all users is cancelled.</span></span> <span data-ttu-id="18e5c-270">序號會將動作放在 InstallFiles 之後，以及加入自訂動作之前。</span><span class="sxs-lookup"><span data-stu-id="18e5c-270">The sequence number places the action after InstallFiles and before the Add custom action.</span></span>             |
    | <span data-ttu-id="18e5c-271">GameUXRollBackAddAsCurUser</span><span class="sxs-lookup"><span data-stu-id="18e5c-271">GameUXRollBackAddAsCurUser</span></span>    | <span data-ttu-id="18e5c-272">未安裝且未進行 ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="18e5c-272">NOT Installed AND NOT ALLUSERS</span></span> | <span data-ttu-id="18e5c-273">4002</span><span class="sxs-lookup"><span data-stu-id="18e5c-273">4002</span></span>     | <span data-ttu-id="18e5c-274">只有當目前使用者的全新安裝取消時，才會發生這個自訂動作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-274">This custom action will only happen when a fresh installation for the current user only is cancelled.</span></span> <span data-ttu-id="18e5c-275">序號會將動作放在 InstallFiles 之後，以及加入自訂動作之前。</span><span class="sxs-lookup"><span data-stu-id="18e5c-275">The sequence number places the action after InstallFiles and before the Add custom action.</span></span> |
    | <span data-ttu-id="18e5c-276">GameUXRemoveAsAdmin</span><span class="sxs-lookup"><span data-stu-id="18e5c-276">GameUXRemoveAsAdmin</span></span>           | <span data-ttu-id="18e5c-277">移除 ~ = "ALL" 和 ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="18e5c-277">REMOVE~="ALL" AND ALLUSERS</span></span>     | <span data-ttu-id="18e5c-278">3452</span><span class="sxs-lookup"><span data-stu-id="18e5c-278">3452</span></span>     | <span data-ttu-id="18e5c-279">此自訂動作只會在所有使用者的移除期間發生。</span><span class="sxs-lookup"><span data-stu-id="18e5c-279">This custom action will only happen during removal for all users.</span></span> <span data-ttu-id="18e5c-280">序號會在 RemoveFiles 之前和復原之後直接放置動作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-280">The sequence number places the action directly before RemoveFiles and after the rollbacks.</span></span>                                     |
    | <span data-ttu-id="18e5c-281">GameUXRemoveAsCurUser</span><span class="sxs-lookup"><span data-stu-id="18e5c-281">GameUXRemoveAsCurUser</span></span>         | <span data-ttu-id="18e5c-282">移除 ~ = "ALL" 而非 ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="18e5c-282">REMOVE~="ALL" AND NOT ALLUSERS</span></span> | <span data-ttu-id="18e5c-283">3453</span><span class="sxs-lookup"><span data-stu-id="18e5c-283">3453</span></span>     | <span data-ttu-id="18e5c-284">此自訂動作只會在移除目前使用者的期間發生。</span><span class="sxs-lookup"><span data-stu-id="18e5c-284">This custom action will only happen during removal for the current user.</span></span> <span data-ttu-id="18e5c-285">序號會在 RemoveFiles 之前和復原之後直接放置動作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-285">The sequence number places the action directly before RemoveFiles and after the rollbacks.</span></span>                              |
    | <span data-ttu-id="18e5c-286">GameUXRollBackRemoveAsAdmin</span><span class="sxs-lookup"><span data-stu-id="18e5c-286">GameUXRollBackRemoveAsAdmin</span></span>   | <span data-ttu-id="18e5c-287">移除 ~ = "ALL" 和 ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="18e5c-287">REMOVE~="ALL" AND ALLUSERS</span></span>     | <span data-ttu-id="18e5c-288">3450</span><span class="sxs-lookup"><span data-stu-id="18e5c-288">3450</span></span>     | <span data-ttu-id="18e5c-289">只有在所有使用者的移除動作都已取消時，才會發生這個自訂動作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-289">This custom action will only happen when removal for all users is cancelled.</span></span> <span data-ttu-id="18e5c-290">序號會在 RemoveFiles 之前，以及在移除自訂動作之前，直接放置動作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-290">The sequence number places the action directly before RemoveFiles and before the Remove custom action.</span></span>              |
    | <span data-ttu-id="18e5c-291">GameUXRollBackRemoveAsCurUser</span><span class="sxs-lookup"><span data-stu-id="18e5c-291">GameUXRollBackRemoveAsCurUser</span></span> | <span data-ttu-id="18e5c-292">移除 ~ = "ALL" 而非 ALLUSERS</span><span class="sxs-lookup"><span data-stu-id="18e5c-292">REMOVE~="ALL" AND NOT ALLUSERS</span></span> | <span data-ttu-id="18e5c-293">3451</span><span class="sxs-lookup"><span data-stu-id="18e5c-293">3451</span></span>     | <span data-ttu-id="18e5c-294">只有在取消目前使用者的移除時，才會發生這個自訂動作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-294">This custom action will only happen when removal for the current user is cancelled.</span></span> <span data-ttu-id="18e5c-295">序號會在 RemoveFiles 之前，以及在移除自訂動作之前，直接放置動作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-295">The sequence number places the action directly before RemoveFiles and before the Remove custom action.</span></span>       |

    

     

5.  <span data-ttu-id="18e5c-296">將下表中顯示的資料列加入至 MSI 封裝中的屬性資料表。</span><span class="sxs-lookup"><span data-stu-id="18e5c-296">Add the row shown in the following table to the Property table in the MSI package.</span></span>

    | <span data-ttu-id="18e5c-297">屬性</span><span class="sxs-lookup"><span data-stu-id="18e5c-297">Property</span></span>          | <span data-ttu-id="18e5c-298">值</span><span class="sxs-lookup"><span data-stu-id="18e5c-298">Value</span></span>                                                         |
    |-------------------|---------------------------------------------------------------|
    | <span data-ttu-id="18e5c-299">RelativePathToGDF</span><span class="sxs-lookup"><span data-stu-id="18e5c-299">RelativePathToGDF</span></span> | <span data-ttu-id="18e5c-300">\\包含 GDF 之二進位檔案的相對檔案路徑名稱</span><span class="sxs-lookup"><span data-stu-id="18e5c-300">relative file path\\name of binary file that contains the GDF</span></span> |

    

     

    > [!Note]  
    > <span data-ttu-id="18e5c-301">路徑所指定的位置是相對於安裝路徑所指定的位置。</span><span class="sxs-lookup"><span data-stu-id="18e5c-301">The location specified by the path is relative to the location specified by the installation path.</span></span> <span data-ttu-id="18e5c-302">例如，bin \\GDF.dll。</span><span class="sxs-lookup"><span data-stu-id="18e5c-302">For example, bin\\GDF.dll.</span></span>

     

6.  <span data-ttu-id="18e5c-303">儲存 MSI 套件。</span><span class="sxs-lookup"><span data-stu-id="18e5c-303">Save the MSI package.</span></span>

<span data-ttu-id="18e5c-304">如需有關 MSI 封裝和 Windows Installer 的詳細資訊，請參閱 [Windows Installer](/windows/desktop/Msi/windows-installer-portal)。</span><span class="sxs-lookup"><span data-stu-id="18e5c-304">For more detailed information about MSI packages and Windows Installer, see [Windows Installer](/windows/desktop/Msi/windows-installer-portal).</span></span>

## <a name="debugging-tips"></a><span data-ttu-id="18e5c-305">調試秘訣</span><span class="sxs-lookup"><span data-stu-id="18e5c-305">Debugging Tips</span></span>

<span data-ttu-id="18e5c-306">以下是一些秘訣，可協助您在呼叫遊戲瀏覽器 Api 時，偵測問題：</span><span class="sxs-lookup"><span data-stu-id="18e5c-306">The following are some tips to help debug issues when calling Games Explorer APIs:</span></span>

### <a name="test-with-sample-code"></a><span data-ttu-id="18e5c-307">使用範例程式碼進行測試</span><span class="sxs-lookup"><span data-stu-id="18e5c-307">Test with sample code</span></span>

<span data-ttu-id="18e5c-308">建立 GameUXInstallHelper 範例解決方案將會建立 GameUXInstallHelper.dll 和 GDFInstall.exe。</span><span class="sxs-lookup"><span data-stu-id="18e5c-308">Building the GameUXInstallHelper sample solution will create a GameUXInstallHelper.dll and a GDFInstall.exe.</span></span> <span data-ttu-id="18e5c-309">GDFInstall.exe 是使用 GameUXInstallHelper.dll 的範例應用程式。</span><span class="sxs-lookup"><span data-stu-id="18e5c-309">The GDFInstall.exe is a sample application that uses GameUXInstallHelper.dll.</span></span> <span data-ttu-id="18e5c-310">如果您想要從遊戲瀏覽器安裝或移除 GDF 二進位檔，執行 GDFInstall.exe 將會提示。</span><span class="sxs-lookup"><span data-stu-id="18e5c-310">Running GDFInstall.exe will prompt if you want install or remove a GDF binary from game explorer.</span></span> <span data-ttu-id="18e5c-311">您可以測試 GDF 二進位檔案，方法是將它傳入做為 GDFInstall.exe 的第一個命令列參數。</span><span class="sxs-lookup"><span data-stu-id="18e5c-311">You can test your GDF binary file by passing it in as the first command line arg to GDFInstall.exe.</span></span>

<span data-ttu-id="18e5c-312">如果您沒有 GDF 二進位檔或無法安裝，請嘗試使用 DirectX SDK 中的範例 GDF。</span><span class="sxs-lookup"><span data-stu-id="18e5c-312">If you don't have a GDF binary or yours fails to install, try using the sample GDF in the DirectX SDK.</span></span> <span data-ttu-id="18e5c-313">GDFExampleBinary 範例可在 DirectX SDK 中找到，而且只是一個只包含 GDF 檔案的 DLL。</span><span class="sxs-lookup"><span data-stu-id="18e5c-313">The GDFExampleBinary sample is found in the DirectX SDK and is just a DLL that only contains a GDF file.</span></span> <span data-ttu-id="18e5c-314">此外，來源中也包含它的 GDFMaker 專案。</span><span class="sxs-lookup"><span data-stu-id="18e5c-314">Also included in the source is its GDFMaker project.</span></span> <span data-ttu-id="18e5c-315">您可以使用 GDFInstall.exe 來建立並測試。</span><span class="sxs-lookup"><span data-stu-id="18e5c-315">You can build it and test it using GDFInstall.exe.</span></span> <span data-ttu-id="18e5c-316">您也可以將其 XML 與您的 XML 進行比較，以精確找出問題所在。</span><span class="sxs-lookup"><span data-stu-id="18e5c-316">You can also compare the its XML to yours to pinpoint exactly where the issue is.</span></span>

### <a name="make-sure-that-your-game-was-removed-properly"></a><span data-ttu-id="18e5c-317">確定您的遊戲已正確移除</span><span class="sxs-lookup"><span data-stu-id="18e5c-317">Make sure that your game was removed properly</span></span>

<span data-ttu-id="18e5c-318">如果遊戲已安裝在遊戲瀏覽器中，後續對 **IGameExplorer：： AddGame** 的呼叫將會傳回 E \_ 失敗，因此請確定您的遊戲未在測試之前安裝。</span><span class="sxs-lookup"><span data-stu-id="18e5c-318">If the game is already installed in Games Explorer, then subsequent calls to **IGameExplorer::AddGame** will return E\_FAIL so make sure your game isn't installed before testing.</span></span> <span data-ttu-id="18e5c-319">如果您只為目前的使用者安裝 GDF，然後嘗試為所有使用者安裝 GDF，這也適用。</span><span class="sxs-lookup"><span data-stu-id="18e5c-319">This also applies if you install the GDF for only the current user and then try to install the GDF for all users.</span></span> <span data-ttu-id="18e5c-320">您必須先移除目前使用者的遊戲， **IGameExplorer：： AddGame** 才會成功。</span><span class="sxs-lookup"><span data-stu-id="18e5c-320">You must first remove the game from the current users before **IGameExplorer::AddGame** will succeed.</span></span>

<span data-ttu-id="18e5c-321">如果您執行 **GDFInstall.exe enum**，範例應用程式將會進入不同的模式，以列舉所有已安裝的遊戲管理器遊戲並提示您移除它們。</span><span class="sxs-lookup"><span data-stu-id="18e5c-321">If you run **GDFInstall.exe enum**, the sample application will enter a different mode which will enumerate all of the installed Games Explorer games and prompt you to remove them.</span></span> <span data-ttu-id="18e5c-322">您也可以在 [HKEY \_ LOCAL MACHINE Software Microsoft Windows CurrentVersion GameUX] 中流覽和搜尋登錄， \_ \\ \\ \\ \\ \\ 確定未針對系統上的其他使用者安裝您的遊戲。</span><span class="sxs-lookup"><span data-stu-id="18e5c-322">You can also browse and search the registry in HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\GameUX to make sure that your game isn't installed for another user on the system.</span></span> <span data-ttu-id="18e5c-323">不過，請勿改變這些登錄設定的任何其他用途，因為它們在作業系統的未來版本中不保證會保持相容。</span><span class="sxs-lookup"><span data-stu-id="18e5c-323">However, do not alter these registry settings for any other purpose, as they are not guaranteed to remain compatible in future versions of the operating system.</span></span>

### <a name="be-sure-to-sign-using-authenticode"></a><span data-ttu-id="18e5c-324">務必使用 Authenticode 簽署</span><span class="sxs-lookup"><span data-stu-id="18e5c-324">Be sure to sign using Authenticode</span></span>

<span data-ttu-id="18e5c-325">如果您已提供評等，但未在 [遊戲] Explorer 中看到它，請確定您已使用 Authenticode 來簽署包含評等的可執行檔或 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="18e5c-325">If you have provided a rating, but are not seeing it in Games Explorer, make sure that you have used Authenticode to sign the executable or DLL file that contains the rating.</span></span> <span data-ttu-id="18e5c-326">遊戲瀏覽器會忽略未簽署檔案中的分級資訊。</span><span class="sxs-lookup"><span data-stu-id="18e5c-326">Games Explorer ignores ratings information in unsigned files.</span></span> <span data-ttu-id="18e5c-327">如需 Authenticode 的詳細資訊，請參閱 [遊戲開發人員的 Authenticode 簽署](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers)。</span><span class="sxs-lookup"><span data-stu-id="18e5c-327">For more information about Authenticode, see [Authenticode Signing for Game Developers](/windows/desktop/DxTechArts/authenticode-signing-for-game-developers).</span></span>

### <a name="be-sure-that-parental-controls-are-available"></a><span data-ttu-id="18e5c-328">確定可以使用家長監護</span><span class="sxs-lookup"><span data-stu-id="18e5c-328">Be sure that parental controls are available</span></span>

<span data-ttu-id="18e5c-329">確定您要在提供家長監護的 Windows Vista 版本上測試家長監護： Home Basic、Home Premium 或旗艦版。</span><span class="sxs-lookup"><span data-stu-id="18e5c-329">Ensure that you are testing parental controls on an edition of Windows Vista that provides parental controls: Home Basic, Home Premium, or Ultimate.</span></span> <span data-ttu-id="18e5c-330">Windows Vista Business 和 Windows Vista Enterprise 不提供家長監護，不過如果您是在 Windows Vista 旗艦版上進行測試，而且測試電腦已加入網域，您必須變更群組原則設定，讓家長監護成為可見的。</span><span class="sxs-lookup"><span data-stu-id="18e5c-330">Windows Vista Business and Windows Vista Enterprise do not provide parental controls however if you are testing on Windows Vista Ultimate, and the test computer is joined to a domain, you must change a group policy setting make parental controls visible.</span></span> <span data-ttu-id="18e5c-331">若要這樣做，請參閱 [使用遊戲瀏覽器開始使用](/previous-versions/windows/desktop/legacy/ee417682(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="18e5c-331">To do this, see [Getting Started with Games Explorer](/previous-versions/windows/desktop/legacy/ee417682(v=vs.85)).</span></span>

### <a name="verify-that-tasks-are-of-the-correct-type"></a><span data-ttu-id="18e5c-332">確認工作的類型正確</span><span class="sxs-lookup"><span data-stu-id="18e5c-332">Verify that tasks are of the correct type</span></span>

<span data-ttu-id="18e5c-333">如果您指定的支援工作並未出現在 [遊戲瀏覽器] 中，請確認它們都是網頁連結。</span><span class="sxs-lookup"><span data-stu-id="18e5c-333">If you have specified support tasks that do not appear in Games Explorer, verify that they are all Web links.</span></span> <span data-ttu-id="18e5c-334">任何其他快速鍵工作都必須建立為播放工作。</span><span class="sxs-lookup"><span data-stu-id="18e5c-334">Any other shortcut tasks must be created as play tasks.</span></span> <span data-ttu-id="18e5c-335">這些工作會在這篇文章的 [ [遊戲] Explorer](#games-explorer-tasks)工作中討論。</span><span class="sxs-lookup"><span data-stu-id="18e5c-335">Tasks are covered earlier in this article in [Games Explorer Tasks](#games-explorer-tasks).</span></span>

### <a name="verify-the-data-in-gdf-binary"></a><span data-ttu-id="18e5c-336">確認 GDF 二進位檔中的資料</span><span class="sxs-lookup"><span data-stu-id="18e5c-336">Verify the data in GDF binary</span></span>

<span data-ttu-id="18e5c-337">GDFTrace.exe 是在 DirectX SDK 中找到的工具。</span><span class="sxs-lookup"><span data-stu-id="18e5c-337">GDFTrace.exe is a tool found in the DirectX SDK.</span></span> <span data-ttu-id="18e5c-338">您可以在 GDF 二進位檔上執行 GDFTrace.exe，它會針對每個支援的語言輸出包含在二進位檔中的所有 GDF 中繼資料，以進行快速驗證。</span><span class="sxs-lookup"><span data-stu-id="18e5c-338">You can run GDFTrace.exe on your GDF binary and it will output all the GDF metadata contained in the binary for every supported language for quick validation.</span></span> <span data-ttu-id="18e5c-339">它也會顯示遺漏或過時資訊的任何警告。</span><span class="sxs-lookup"><span data-stu-id="18e5c-339">It also displays any warnings about missing or outdated information.</span></span>

## <a name="summary"></a><span data-ttu-id="18e5c-340">總結</span><span class="sxs-lookup"><span data-stu-id="18e5c-340">Summary</span></span>

<span data-ttu-id="18e5c-341">Windows Vista 中的遊戲瀏覽器提供簡單且可自訂的方式，讓您的遊戲對 Windows Vista 的使用者呈現，但也需要您在安裝過程中向系統註冊遊戲。</span><span class="sxs-lookup"><span data-stu-id="18e5c-341">Games Explorer in Windows Vista provides an easy, customizable way to present your game to users of Windows Vista, but it also requires you to register the game with the system during the installation process.</span></span> <span data-ttu-id="18e5c-342">GameUXInstallHelper 範例大幅簡化了開發人員的流程。</span><span class="sxs-lookup"><span data-stu-id="18e5c-342">The GameUXInstallHelper sample greatly simplifies this process for developers.</span></span>

 

 