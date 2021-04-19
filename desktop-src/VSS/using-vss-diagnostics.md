---
description: Vsdiagview 和 Vssagent 是您可用來對 VSS 應用程式進行疑難排解的工具。請注意，這些工具組含在適用于 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 中。
ms.assetid: 2c1270a6-38c7-40d5-a194-0a6795557b9f
title: 使用 VSS 診斷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f3d1733c2780670507b39c1db91cb3b2f7035a2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986350"
---
# <a name="using-vss-diagnostics"></a><span data-ttu-id="b9856-103">使用 VSS 診斷</span><span class="sxs-lookup"><span data-stu-id="b9856-103">Using VSS Diagnostics</span></span>

<span data-ttu-id="b9856-104">Vsdiagview 和 Vssagent 是您可用來對 VSS 應用程式進行疑難排解的工具。</span><span class="sxs-lookup"><span data-stu-id="b9856-104">Vsdiagview and Vssagent are tools that you can use to troubleshoot VSS applications.</span></span>

> [!Note]  
> <span data-ttu-id="b9856-105">這些工具組含在適用于 Windows Vista 和更新版本的 Microsoft Windows 軟體開發套件 (SDK) 中。</span><span class="sxs-lookup"><span data-stu-id="b9856-105">These tools are included in the Microsoft Windows Software Development Kit (SDK) for Windows Vista and later.</span></span> <span data-ttu-id="b9856-106">您可以從下載 Windows SDK [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx) 。</span><span class="sxs-lookup"><span data-stu-id="b9856-106">You can download the Windows SDK from [https://msdn.microsoft.com/windowsvista](https://msdn.microsoft.com/windows/default.aspx).</span></span>

 

<span data-ttu-id="b9856-107">在 Windows SDK 安裝中，您可以在 `%Program Files(x86)%\Windows Kits\8.1\bin\x64` 64 位 windows) 的 (和 `%Program Files(x86)%\Windows Kits\8.1\bin\x86` 32 位 windows) 的 (中找到這些工具。</span><span class="sxs-lookup"><span data-stu-id="b9856-107">In the Windows SDK installation, these tools can be found in `%Program Files(x86)%\Windows Kits\8.1\bin\x64` (for 64-bit Windows) and `%Program Files(x86)%\Windows Kits\8.1\bin\x86` (for 32-bit Windows).</span></span>

## <a name="gathering-data"></a><span data-ttu-id="b9856-108">正在收集資料</span><span class="sxs-lookup"><span data-stu-id="b9856-108">Gathering Data</span></span>

<span data-ttu-id="b9856-109">您可以使用 Vssagent 命令來收集資料。</span><span class="sxs-lookup"><span data-stu-id="b9856-109">You can gather data by using the Vssagent command.</span></span>

<span data-ttu-id="b9856-110">**使用 Vssagent 收集資料**</span><span class="sxs-lookup"><span data-stu-id="b9856-110">**To gather data using Vssagent**</span></span>

1.  <span data-ttu-id="b9856-111">若要從命令列收集資料，請使用 Vssagent 命令，如下所示：</span><span class="sxs-lookup"><span data-stu-id="b9856-111">To gather data from the command line, use the Vssagent command as follows:</span></span>

    <span data-ttu-id="b9856-112">**vssagent-收集** *XmlFileName \* \* \* .xml*\*</span><span class="sxs-lookup"><span data-stu-id="b9856-112">**vssagent -gather** *XmlFileName\*\*\*.xml*\*</span></span>

2.  <span data-ttu-id="b9856-113">若要查看輸出檔，請參閱下列「查看資料」一節。</span><span class="sxs-lookup"><span data-stu-id="b9856-113">To view the output file, see the following Viewing Data section.</span></span>

## <a name="viewing-data"></a><span data-ttu-id="b9856-114">查看資料</span><span class="sxs-lookup"><span data-stu-id="b9856-114">Viewing Data</span></span>

<span data-ttu-id="b9856-115">您可以使用 Vsdiagview 應用程式來查看使用 Vssagent 命令收集的資料。</span><span class="sxs-lookup"><span data-stu-id="b9856-115">The Vsdiagview application can be used to view data that was gathered by using the Vssagent command.</span></span> <span data-ttu-id="b9856-116">Vsdiagview 會顯示有關電腦的下列資訊：</span><span class="sxs-lookup"><span data-stu-id="b9856-116">Vsdiagview displays the following information about the computer:</span></span>

-   <span data-ttu-id="b9856-117">電腦的相關資訊，例如作業系統版本、可用記憶體總計和 CPU 速度</span><span class="sxs-lookup"><span data-stu-id="b9856-117">Information about the computer, such as the operating system version, total available memory, and CPU speed</span></span>
-   <span data-ttu-id="b9856-118">VSS 二進位檔的名稱和版本號碼</span><span class="sxs-lookup"><span data-stu-id="b9856-118">The names and version numbers of the VSS binaries</span></span>
-   <span data-ttu-id="b9856-119">磁片和磁片區裝置的名稱和屬性</span><span class="sxs-lookup"><span data-stu-id="b9856-119">The names and properties of the disk and volume devices</span></span>
-   <span data-ttu-id="b9856-120">任何 COM + 應用程式的名稱和屬性</span><span class="sxs-lookup"><span data-stu-id="b9856-120">The names and properties of any COM+ applications</span></span>
-   <span data-ttu-id="b9856-121">可以用來診斷 VSS 問題的事件記錄檔名稱</span><span class="sxs-lookup"><span data-stu-id="b9856-121">The names of event logs that can be used for diagnosing VSS problems</span></span>
-   <span data-ttu-id="b9856-122">任何 VSS 寫入器及其處理事件的名稱</span><span class="sxs-lookup"><span data-stu-id="b9856-122">The names of any VSS writers and the events that they handle</span></span>
-   <span data-ttu-id="b9856-123">其他作業系統檔案的相關資訊</span><span class="sxs-lookup"><span data-stu-id="b9856-123">Information about other operating system files</span></span>

<span data-ttu-id="b9856-124">**使用 Vsdiagview 來查看資料**</span><span class="sxs-lookup"><span data-stu-id="b9856-124">**To view data using Vsdiagview**</span></span>

1.  <span data-ttu-id="b9856-125">在 [檔案] 功能表中，選擇 [ **開啟** ] 以流覽檔案。</span><span class="sxs-lookup"><span data-stu-id="b9856-125">In the File menu, choose **Open** to browse for a file.</span></span> <span data-ttu-id="b9856-126"> (預設位置為 C： \\ vssdiag。 ) </span><span class="sxs-lookup"><span data-stu-id="b9856-126">(The default location is C:\\vssdiag.)</span></span>
2.  <span data-ttu-id="b9856-127">按一下 [ **開啟** ] 以查看資料。</span><span class="sxs-lookup"><span data-stu-id="b9856-127">Click **Open** to view the data.</span></span>

 

 



