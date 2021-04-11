---
description: 此範例說明如何建立可安裝應用程式的簡單 Windows Installer 套件。
ms.assetid: eee1e3e6-74e9-41d0-b732-1f792a4df423
title: 安裝範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11eefaab2977bf7cc31e86ac7541b21b345c1aa1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848978"
---
# <a name="an-installation-example"></a><span data-ttu-id="72d78-103">安裝範例</span><span class="sxs-lookup"><span data-stu-id="72d78-103">An Installation Example</span></span>

<span data-ttu-id="72d78-104">此範例說明如何建立可安裝應用程式的簡單 Windows Installer 套件。</span><span class="sxs-lookup"><span data-stu-id="72d78-104">This example illustrates how to create a simple Windows Installer package that installs an application.</span></span> <span data-ttu-id="72d78-105">此範例會安裝「記事本」、Windows 隨附的文字編輯器，以及數個描述事件和招生的文字檔（在紅色公園的假想）。</span><span class="sxs-lookup"><span data-stu-id="72d78-105">The sample installs Notepad, a text editor included with Windows, and several text files describing events and admissions at the imaginary Red Park Arena.</span></span>

<span data-ttu-id="72d78-106">此範例具有下列規格：</span><span class="sxs-lookup"><span data-stu-id="72d78-106">The sample has the following specifications:</span></span>

-   <span data-ttu-id="72d78-107">應用程式會以自行安裝的 Windows Installer 套件的形式提供給使用者，以安裝所有必要的檔案、快捷方式和登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="72d78-107">The application is provided to users as a self-installing Windows Installer package that installs all the required files, shortcuts, and registry information.</span></span>
-   <span data-ttu-id="72d78-108">安裝套件可能會在安裝期間對使用者顯示 UI wizard，以收集使用者資訊。</span><span class="sxs-lookup"><span data-stu-id="72d78-108">The installation package may present a UI wizard to the user during setup to collect user information.</span></span>
-   <span data-ttu-id="72d78-109">在安裝期間，使用者可以選擇要安裝的個別功能，以在本機執行、從來源執行，或不安裝。</span><span class="sxs-lookup"><span data-stu-id="72d78-109">During setup, users have the option of selecting individual features to be installed to run-locally, to run-from-source, or to not be installed.</span></span>
-   <span data-ttu-id="72d78-110">您可以將其中一項功能提供給使用者，作為隨選安裝功能。</span><span class="sxs-lookup"><span data-stu-id="72d78-110">One of the features can be presented to users as an install-on-demand feature.</span></span>
-   <span data-ttu-id="72d78-111">相同的套件會卸載應用程式，並從使用者的電腦移除所有應用程式檔和登錄資訊。</span><span class="sxs-lookup"><span data-stu-id="72d78-111">The same package uninstalls the application and removes all the application files and registry information from the user's computer.</span></span>
-   <span data-ttu-id="72d78-112">封裝已準備好接收包含變更其產品代碼的主要升級。</span><span class="sxs-lookup"><span data-stu-id="72d78-112">The package is prepared to receive a major upgrade that includes changing its product code.</span></span>

<span data-ttu-id="72d78-113">若要重現範例，您需要能夠建立和編輯空白 Windows Installer 資料庫的軟體工具。</span><span class="sxs-lookup"><span data-stu-id="72d78-113">To reproduce the example, you need a software tool capable of creating and editing a blank Windows Installer database.</span></span> <span data-ttu-id="72d78-114">獨立軟體廠商提供數種套件建立工具。</span><span class="sxs-lookup"><span data-stu-id="72d78-114">Several package creation tools are available from independent software vendors.</span></span> <span data-ttu-id="72d78-115">[Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md)中提供稱為 Orca 的 Windows Installer 資料庫編輯器。</span><span class="sxs-lookup"><span data-stu-id="72d78-115">A Windows Installer database editor called Orca is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md).</span></span>

<span data-ttu-id="72d78-116">若要完成此範例，請遵循下列步驟：</span><span class="sxs-lookup"><span data-stu-id="72d78-116">To complete the example, follow these steps:</span></span>

[<span data-ttu-id="72d78-117">規劃安裝</span><span class="sxs-lookup"><span data-stu-id="72d78-117">Planning the Installation</span></span>](planning-the-installation.md)

[<span data-ttu-id="72d78-118">匯入空白資料庫</span><span class="sxs-lookup"><span data-stu-id="72d78-118">Importing a Blank Database</span></span>](importing-a-blank-database.md)

[<span data-ttu-id="72d78-119">指定目錄結構</span><span class="sxs-lookup"><span data-stu-id="72d78-119">Specifying Directory Structure</span></span>](specifying-directory-structure.md)

[<span data-ttu-id="72d78-120">指定元件</span><span class="sxs-lookup"><span data-stu-id="72d78-120">Specifying Components</span></span>](specifying-components.md)

[<span data-ttu-id="72d78-121">指定檔案和檔案屬性</span><span class="sxs-lookup"><span data-stu-id="72d78-121">Specifying Files and File Attributes</span></span>](specifying-files-and-file-attributes.md)

[<span data-ttu-id="72d78-122">指定來源媒體</span><span class="sxs-lookup"><span data-stu-id="72d78-122">Specifying Source Media</span></span>](specifying-source-media.md)

[<span data-ttu-id="72d78-123">指定功能</span><span class="sxs-lookup"><span data-stu-id="72d78-123">Specifying Features</span></span>](specifying-features.md)

[<span data-ttu-id="72d78-124">指定 Feature-Component 關聯性</span><span class="sxs-lookup"><span data-stu-id="72d78-124">Specifying Feature-Component Relationships</span></span>](specifying-feature-component-relationships.md)

[<span data-ttu-id="72d78-125">新增登錄資訊</span><span class="sxs-lookup"><span data-stu-id="72d78-125">Adding Registry Information</span></span>](adding-registry-information.md)

[<span data-ttu-id="72d78-126">指定快速鍵</span><span class="sxs-lookup"><span data-stu-id="72d78-126">Specifying Shortcuts</span></span>](specifying-shortcuts.md)

[<span data-ttu-id="72d78-127">指定屬性</span><span class="sxs-lookup"><span data-stu-id="72d78-127">Specifying Properties</span></span>](specifying-properties.md)

[<span data-ttu-id="72d78-128">匯入 InstallExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="72d78-128">Importing the InstallExecuteSequence</span></span>](importing-the-installexecutesequence.md)

[<span data-ttu-id="72d78-129">匯入 InstallUISequence</span><span class="sxs-lookup"><span data-stu-id="72d78-129">Importing the InstallUISequence</span></span>](importing-the-installuisequence.md)

[<span data-ttu-id="72d78-130">匯入 AdminExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="72d78-130">Importing the AdminExecuteSequence</span></span>](importing-the-adminexecutesequence.md)

[<span data-ttu-id="72d78-131">匯入 AdminUISequence</span><span class="sxs-lookup"><span data-stu-id="72d78-131">Importing the AdminUISequence</span></span>](importing-the-adminuisequence.md)

[<span data-ttu-id="72d78-132">匯入 AdvtExecuteSequence</span><span class="sxs-lookup"><span data-stu-id="72d78-132">Importing the AdvtExecuteSequence</span></span>](importing-the-advtexecutesequence.md)

[<span data-ttu-id="72d78-133">新增摘要資訊</span><span class="sxs-lookup"><span data-stu-id="72d78-133">Adding Summary Information</span></span>](adding-summary-information.md)

[<span data-ttu-id="72d78-134">匯入消費者介面</span><span class="sxs-lookup"><span data-stu-id="72d78-134">Importing the User Interface</span></span>](importing-the-user-interface.md)

[<span data-ttu-id="72d78-135">驗證安裝資料庫</span><span class="sxs-lookup"><span data-stu-id="72d78-135">Validating an Installation Database</span></span>](validating-an-installation-database.md)

 

 



