---
description: 安裝程式群組中的資料表會控制在安裝期間依標準動作和自訂動作所執行的工作。
ms.assetid: dff7cf4a-89a2-47b0-9038-93b79c0d915a
title: 安裝程式資料表群組
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbb3c5eb0306941d3cdd02bf7f994270ca0d6490
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320879"
---
# <a name="installation-procedure-tables-group"></a><span data-ttu-id="2e3dd-103">安裝程式資料表群組</span><span class="sxs-lookup"><span data-stu-id="2e3dd-103">Installation Procedure Tables Group</span></span>

<span data-ttu-id="2e3dd-104">安裝程式群組中的資料表會控制在安裝期間依 [標準動作](standard-actions.md) 和 [自訂動作](custom-actions.md)所執行的工作。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-104">The tables in the Installation Procedure group control tasks performed during the installation by [standard actions](standard-actions.md) and [custom actions](custom-actions.md).</span></span>

<span data-ttu-id="2e3dd-105">此群組中的部分資料表會藉由提供一系列動作來控制高階動作。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-105">Some of the tables in this group control a high level action by providing a sequence of actions.</span></span> <span data-ttu-id="2e3dd-106">下列每一個順序資料表都會控制高階動作的一部分。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-106">Each of the following sequence tables controls a portion of a high level action.</span></span>

-   [<span data-ttu-id="2e3dd-107">InstallUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="2e3dd-107">InstallUISequence table</span></span>](installuisequence-table.md)
-   [<span data-ttu-id="2e3dd-108">InstallExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="2e3dd-108">InstallExecuteSequence table</span></span>](installexecutesequence-table.md)
-   [<span data-ttu-id="2e3dd-109">AdminUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="2e3dd-109">AdminUISequence table</span></span>](adminuisequence-table.md)
-   [<span data-ttu-id="2e3dd-110">AdminExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="2e3dd-110">AdminExecuteSequence table</span></span>](adminexecutesequence-table.md)
-   [<span data-ttu-id="2e3dd-111">AdvtUISequence 資料表</span><span class="sxs-lookup"><span data-stu-id="2e3dd-111">AdvtUISequence table</span></span>](advtuisequence-table.md)
-   [<span data-ttu-id="2e3dd-112">AdvtExecuteSequence 資料表</span><span class="sxs-lookup"><span data-stu-id="2e3dd-112">AdvtExecuteSequence table</span></span>](advtexecutesequence-table.md)

<span data-ttu-id="2e3dd-113">在某些情況下，安裝必須使用 [標準動作](standard-actions.md)來執行某些動作。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-113">There may be situations in which an installation needs to do something that is not possible using only [standard actions](standard-actions.md).</span></span> <span data-ttu-id="2e3dd-114">為了提供最大的彈性，安裝程式會讓安裝程式作者能夠建立自己的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-114">To provide the greatest degree of flexibility, the installer provides setup authors the ability to create their own custom actions.</span></span> <span data-ttu-id="2e3dd-115">如果您有任何自訂動作，您應該填入 CustomAction 資料表來向安裝程式註冊它們。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-115">If you have any custom actions, you should register them with the installer by populating the CustomAction Table.</span></span>

<span data-ttu-id="2e3dd-116">[CustomAction 資料表](customaction-table.md)提供將自訂程式碼和資料整合至安裝程式的方法。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-116">The [CustomAction table](customaction-table.md) provides the means of integrating custom code and data into the installation process.</span></span> <span data-ttu-id="2e3dd-117">執行的程式碼可以是包含在資料庫內的資料流程、最近安裝的檔案，或現有的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-117">The code that is executed can be a stream contained within the database, a recently installed file, or an existing executable.</span></span>

<span data-ttu-id="2e3dd-118">下表將在安裝期間擴充安裝程式的功能，以操作檔案和資料夾。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-118">The following tables extend the installer's capabilities to manipulate files and folders during the installation.</span></span>

-   <span data-ttu-id="2e3dd-119">[RemoveFile 資料表](removefile-table.md)包含在安裝期間移除的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-119">The [RemoveFile table](removefile-table.md) contains a list of files that are removed during the installation.</span></span>
-   <span data-ttu-id="2e3dd-120">[RemoveIniFile 資料表](removeinifile-table.md)包含應用程式需要從 .ini 檔案移除的資訊。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-120">The [RemoveIniFile table](removeinifile-table.md) contains the information an application needs to remove from .ini files.</span></span>
-   <span data-ttu-id="2e3dd-121">[RemoveRegistry 資料表](removeregistry-table.md)包含已選取要安裝的對應元件時，從系統登錄刪除的資訊。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-121">The [RemoveRegistry table](removeregistry-table.md) contains the information which is deleted from the system registry when the corresponding component is selected to be installed.</span></span>
-   <span data-ttu-id="2e3dd-122">[CreateFolder 資料表](createfolder-table.md)會列出在安裝期間必須建立的資料夾。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-122">The [CreateFolder table](createfolder-table.md) lists the folders that must be created during the installation.</span></span> <span data-ttu-id="2e3dd-123">雖然安裝程式會在需要時建立資料夾，但它們會在空白時立即移除。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-123">Although the installer creates folders as they are needed, these are removed as soon as they are empty.</span></span> <span data-ttu-id="2e3dd-124">在卸載元件之前，不會刪除 CreateFolder 資料表中的資料夾清單。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-124">Folders list in the CreateFolder table are not deleted until the component is uninstalled.</span></span>
-   <span data-ttu-id="2e3dd-125">[MoveFile 資料表](movefile-table.md)包含要從使用者電腦上指定的來原始目錄移動或複製到目的地目錄的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-125">The [MoveFile table](movefile-table.md) contains a list of files to be moved or copied from a specified source directory on the user's computer to a destination directory.</span></span> <span data-ttu-id="2e3dd-126">您不需要使用 MoveFile 資料表來描述與您要安裝之元件相關聯的檔案。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-126">It is not necessary to use the MoveFile table to describe the files associated with the components you are installing.</span></span>

<span data-ttu-id="2e3dd-127">若要設定必須符合才能起始安裝的必要條件，請填入 LaunchCondition 資料表。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-127">To set up necessary conditions that must be met to initiate the installation, populate the LaunchCondition table.</span></span>

<span data-ttu-id="2e3dd-128">[LaunchCondition 資料表](launchcondition-table.md)包含條件清單，必須滿足這些條件，動作才會成功。</span><span class="sxs-lookup"><span data-stu-id="2e3dd-128">The [LaunchCondition table](launchcondition-table.md) contains a list of conditions, all of which must be satisfied for the action to succeed.</span></span>

 

 



