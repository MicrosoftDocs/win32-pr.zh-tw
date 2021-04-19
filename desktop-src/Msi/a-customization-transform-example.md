---
description: 此範例說明如何使用自訂轉換來停用功能並新增資源。
ms.assetid: 028b1d01-3b66-4640-98f9-ca33f90ca516
title: 自訂轉換範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26ea655d1187b0271aba7ea56a46bacf95f5fb40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993098"
---
# <a name="a-customization-transform-example"></a><span data-ttu-id="fcbcc-103">自訂轉換範例</span><span class="sxs-lookup"><span data-stu-id="fcbcc-103">A Customization Transform Example</span></span>

<span data-ttu-id="fcbcc-104">此範例說明如何使用自訂轉換來停用功能並新增資源。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-104">This example illustrates how a customization transform may be used to disable features and add new resources.</span></span>

<span data-ttu-id="fcbcc-105">系統管理員可以使用自訂轉換，在 [功能資料表](feature-table.md)的 [層級] 資料行中輸入0，以永久停用功能。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-105">An administrator can permanently disable a feature by using a customization transform to enter a 0 into the Level column of the [Feature table](feature-table.md).</span></span> <span data-ttu-id="fcbcc-106">然後，如果使用者使用 UI 選取完整安裝，或在命令列上將 [ [**ADDLOCAL**](addlocal.md) ] 屬性設定為 [全部]，則應用程式的自訂轉換會防止安裝和顯示該功能。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-106">The application of the customization transform then prevents the installation and display of that feature even if the user selects a complete installation using the UI or by setting the [**ADDLOCAL**](addlocal.md) property to ALL on the command line.</span></span> <span data-ttu-id="fcbcc-107">如需安裝層級的討論，請參閱 [功能資料表](feature-table.md) 與 [**INSTALLLEVEL**](installlevel.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-107">For a discussion of installation level, see [Feature table](feature-table.md) and [**INSTALLLEVEL**](installlevel.md) property.</span></span>

<span data-ttu-id="fcbcc-108">您可以使用自訂轉換來部署自訂應用程式所需的資源，以新增一或多個新元件。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-108">The resources needed to customize an application can be deployed by using a customization transform to add one or more new components.</span></span> <span data-ttu-id="fcbcc-109">轉換必須加入一或多個新功能，以包含這些新元件。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-109">The transform must add one or more new features to contain these new components.</span></span> <span data-ttu-id="fcbcc-110">如需部署資源（例如檔案、登錄機碼或快捷方式）時應遵循的規則，請參閱 [使用轉換來新增資源](using-transforms-to-add-resources.md)。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-110">For the rules that should be followed when deploying resources, such as files, registry keys, or shortcuts, see [Using Transforms to Add Resources](using-transforms-to-add-resources.md).</span></span>

<span data-ttu-id="fcbcc-111">此範例說明如何建立 [轉換](transforms.md) 來自訂安裝 [範例](an-installation-example.md)中所述的應用程式安裝。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-111">This example illustrates how to create a [transform](transforms.md) to customize the installation of the application described in [An Installation Example](an-installation-example.md).</span></span> <span data-ttu-id="fcbcc-112">原始安裝套件會安裝範例應用程式的所有功能，包括功能閘道，可讓使用者查看 Red 公園的招生資訊。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-112">The original installation package installs all the features of the sample application, including the feature Gate, which enables users to view admissions information for the Red Park Arena.</span></span> <span data-ttu-id="fcbcc-113">某些使用者群組只需要提供事件排程資訊的應用程式功能，而且不需要閘道功能。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-113">Some groups of users only need the application features that give event scheduling information, and do not need the Gate feature.</span></span> <span data-ttu-id="fcbcc-114">這些群組也需要取得特殊的電話清單。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-114">These groups also need to get a special phone list.</span></span> <span data-ttu-id="fcbcc-115">因此轉換必須進行兩項作業： 1) 自訂安裝，讓此群組只會收到所需的應用程式功能，而 2) 為新的電話清單提供所需的資源。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-115">The transform must therefore do two things: 1) customize the installation so that this group only receives the application features they need and 2) provide the resources needed for the new phone list.</span></span>

<span data-ttu-id="fcbcc-116">此範例的最基本使用者介面範例，會在 [Windows Installer 開發人員的 Windows SDK 元件](platform-sdk-components-for-windows-installer-developers.md) 中提供，做為檔 Uisample.msi。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-116">An example of a minimal user interface for this sample is provided in the [Windows SDK Components for Windows Installer Developers](platform-sdk-components-for-windows-installer-developers.md) as the file Uisample.msi.</span></span> <span data-ttu-id="fcbcc-117">如果您有 SDK，就可以存取重現範例安裝套件、使用者介面和自訂轉換所需的所有工具和資料。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-117">If you have the SDK, you have access to all the tools and data necessary to reproduce the sample installation package, user interface, and customization transform.</span></span>

<span data-ttu-id="fcbcc-118">自訂轉換具有下列規格：</span><span class="sxs-lookup"><span data-stu-id="fcbcc-118">The customization transform has the following specifications:</span></span>

-   <span data-ttu-id="fcbcc-119">自訂轉換內嵌于 MNP2000.msi 檔案中，以確保它一律可供安裝資料庫使用。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-119">The customization transform is embedded inside the MNP2000.msi file to guarantee that it is always available with the installation database.</span></span>
-   <span data-ttu-id="fcbcc-120">使用自訂轉換安裝 MNP2000.msi 不會安裝閘道功能、閘道功能的子功能，或是閘道功能的任何元件（即使使用者選取完整的安裝類型）。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-120">Installing MNP2000.msi with the customization transform does not install the Gate feature, child features of the Gate feature, or any of the components of the Gate feature, even if the user selects the Complete type of installation.</span></span>
-   <span data-ttu-id="fcbcc-121">其他應用程式可能會共用閘道功能的部分或全部元件。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-121">Other applications may share some or all of the components of the Gate feature.</span></span> <span data-ttu-id="fcbcc-122">這些應用程式的安裝套件可能會將其所有元件安裝在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-122">The installation packages of these applications may install all their components on the user's computer.</span></span>
-   <span data-ttu-id="fcbcc-123">使用自訂轉換移除 MNP2000.msi 不會移除其他應用程式已安裝的任何閘道元件。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-123">Removing MNP2000.msi with the customization transform does not remove any of the Gate components that have been installed by other applications.</span></span>
-   <span data-ttu-id="fcbcc-124">使用自訂轉換安裝 MNP2000.msi 也會安裝新的最上層功能、電話 \_ 清單，以及需要安裝資源的新元件電話，Phone.txt。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-124">Installing MNP2000.msi with the customization transform also installs a new top level feature, Phone\_List, and a new component, phone, which requires the installation of the resource, Phone.txt.</span></span> <span data-ttu-id="fcbcc-125">使用者會 \_ 使用功能表目錄中的快捷方式來存取電話清單功能。</span><span class="sxs-lookup"><span data-stu-id="fcbcc-125">The user accesses the Phone\_List feature using a shortcut in the Menu directory.</span></span>

[<span data-ttu-id="fcbcc-126">繼續</span><span class="sxs-lookup"><span data-stu-id="fcbcc-126">Continue</span></span>](customizing-an-original-database.md)

 

 



