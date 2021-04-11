---
description: 下列範例說明如何在安裝結束時啟動 HTML 檔案。
ms.assetid: 6b082559-bcfa-4098-b072-27ee78092833
title: 使用自訂動作在安裝結束時啟動已安裝的檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e5c039d58830ce6a01f76a0946bced474e5091b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193675"
---
# <a name="using-a-custom-action-to-launch-an-installed-file-at-the-end-of-the-installation"></a><span data-ttu-id="592d6-103">使用自訂動作在安裝結束時啟動已安裝的檔案</span><span class="sxs-lookup"><span data-stu-id="592d6-103">Using a Custom Action to Launch an Installed File at the End of the Installation</span></span>

<span data-ttu-id="592d6-104">下列範例說明如何在安裝結束時啟動 HTML 檔案。</span><span class="sxs-lookup"><span data-stu-id="592d6-104">The following example illustrates how to launch an HTML file at the end of an installation.</span></span> <span data-ttu-id="592d6-105">安裝程式會安裝包含該檔案的元件，然後在安裝結束時發佈控制項事件，以執行可開啟檔案的自訂動作。</span><span class="sxs-lookup"><span data-stu-id="592d6-105">The Installer installs the component that contains the file, and then publishes a control event at the end of the installation to run a custom action that opens the file.</span></span> <span data-ttu-id="592d6-106">這種方法可用來在應用程式第一次安裝結束時啟動說明教學課程。</span><span class="sxs-lookup"><span data-stu-id="592d6-106">This approach may be used to launch a help tutorial at the end of the first installation of an application.</span></span>

<span data-ttu-id="592d6-107">範例必須符合下列規格。</span><span class="sxs-lookup"><span data-stu-id="592d6-107">The sample must meet the following specifications.</span></span>

-   <span data-ttu-id="592d6-108">只有在使用 [*完整的 UI*](f-gly.md) 層級來安裝應用程式時，安裝程式才會執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="592d6-108">The Installer executes the custom action only if the [*full UI*](f-gly.md) level is used to install an application.</span></span>
-   <span data-ttu-id="592d6-109">只有當包含 HTML 檔案的元件安裝在本機電腦上執行時，安裝程式才會執行自訂動作。</span><span class="sxs-lookup"><span data-stu-id="592d6-109">The Installer executes the custom action only if the component that contains the HTML file is installed to run locally on the computer.</span></span>
-   <span data-ttu-id="592d6-110">自訂動作只會在第一次安裝應用程式時執行。</span><span class="sxs-lookup"><span data-stu-id="592d6-110">The custom action only runs on the first installation of the application.</span></span>
-   <span data-ttu-id="592d6-111">如果自訂動作失敗，安裝將不會失敗。</span><span class="sxs-lookup"><span data-stu-id="592d6-111">The installation does not fail if the custom action fails.</span></span>

<span data-ttu-id="592d6-112">此範例包含名為「教學課程」的假想元件，它會控制至少一個資源，一個名為 tutorial.htm 的檔案。</span><span class="sxs-lookup"><span data-stu-id="592d6-112">The sample includes a hypothetical component named Tutorial that controls at least one resource, a file named tutorial.htm.</span></span> <span data-ttu-id="592d6-113">在檔案資料表的 [檔案] 資料行中，這個檔案的識別碼是教學課程。</span><span class="sxs-lookup"><span data-stu-id="592d6-113">The identifier for this file in the File column of the File table is Tutorial.</span></span> <span data-ttu-id="592d6-114">下列討論假設您已經建立教學課程所需的資源，並已在[功能](feature-table.md)、[元件](component-table.md) [、檔案、](file-table.md)[目錄](directory-table.md)和[FeatureComponents](featurecomponents-table.md)資料表中完成所有必要的專案，以安裝此元件。</span><span class="sxs-lookup"><span data-stu-id="592d6-114">The following discussion assumes that you have already created the resources required by Tutorial, and have made all the necessary entries in the [Feature](feature-table.md), [Component](component-table.md), [File](file-table.md), [Directory](directory-table.md), and [FeatureComponents](featurecomponents-table.md) tables to install this component.</span></span> <span data-ttu-id="592d6-115">如需詳細資訊，請參閱 [安裝範例](an-installation-example.md)。</span><span class="sxs-lookup"><span data-stu-id="592d6-115">For more information, see [An Installation Example](an-installation-example.md).</span></span>

<span data-ttu-id="592d6-116">下列主題包含有關如何建立必要的自訂動作，並將其新增至安裝套件的資訊。</span><span class="sxs-lookup"><span data-stu-id="592d6-116">The following topics contain information about how to create required custom actions and add them to an installation package.</span></span>

-   [<span data-ttu-id="592d6-117">撰寫啟動自訂動作</span><span class="sxs-lookup"><span data-stu-id="592d6-117">Authoring the Launch Custom Action</span></span>](authoring-the-launch-custom-action.md)
-   [<span data-ttu-id="592d6-118">將啟動新增至 CustomAction 和二進位資料表</span><span class="sxs-lookup"><span data-stu-id="592d6-118">Adding Launch to the CustomAction and Binary Tables</span></span>](adding-launch-to-the-customaction-and-binary-tables.md)
-   [<span data-ttu-id="592d6-119">在安裝結束時新增控制項事件以執行啟動</span><span class="sxs-lookup"><span data-stu-id="592d6-119">Adding a Control Event at the End of the Installation to Run Launch</span></span>](adding-a-control-event-at-the-end-of-the-installation-to-run-launch.md)

 

 



