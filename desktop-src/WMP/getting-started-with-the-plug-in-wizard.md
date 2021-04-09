---
title: 使用外掛程式 Wizard 開始使用
description: 使用外掛程式 Wizard 開始使用
ms.assetid: 77fc1b0c-20f5-434d-9142-f112489a7f08
keywords:
- Windows Media Player 外掛程式，安裝外掛程式嚮導
- 外掛程式，安裝外掛程式 wizard
- 建立外掛程式，安裝外掛程式 wizard
- Windows Media Player 外掛程式嚮導，安裝
- 安裝外掛程式嚮導
- 外掛程式嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a4feb9cfa60c120bfc5bb675ea8a8078b95ad14
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932422"
---
# <a name="getting-started-with-the-plug-in-wizard"></a><span data-ttu-id="43060-109">使用外掛程式 Wizard 開始使用</span><span class="sxs-lookup"><span data-stu-id="43060-109">Getting Started with the Plug-in Wizard</span></span>

<span data-ttu-id="43060-110">若要設定開發環境以建立 Windows Media Player 外掛程式，您必須安裝下列專案：</span><span class="sxs-lookup"><span data-stu-id="43060-110">To set up your development environment for creating Windows Media Player plug-ins, you must install the following items:</span></span>

-   <span data-ttu-id="43060-111">Microsoft Visual Studio .NET 2003 或更新版本</span><span class="sxs-lookup"><span data-stu-id="43060-111">Microsoft Visual Studio .NET 2003 or later</span></span>
-   <span data-ttu-id="43060-112">Windows Media Player 9 系列或更新版本</span><span class="sxs-lookup"><span data-stu-id="43060-112">Windows Media Player 9 Series or later</span></span>
-   <span data-ttu-id="43060-113">Windows SDK，其中包含 Windows Media Player SDK</span><span class="sxs-lookup"><span data-stu-id="43060-113">Windows SDK, which includes the Windows Media Player SDK</span></span>
-   <span data-ttu-id="43060-114">Windows Media Player 外掛程式嚮導</span><span class="sxs-lookup"><span data-stu-id="43060-114">Windows Media Player Plug-in Wizard</span></span>

## <a name="installing-the-wizard"></a><span data-ttu-id="43060-115">安裝精靈</span><span class="sxs-lookup"><span data-stu-id="43060-115">Installing the Wizard</span></span>

<span data-ttu-id="43060-116">請執行下列步驟來安裝 Windows Media Player 外掛程式 Wizard。</span><span class="sxs-lookup"><span data-stu-id="43060-116">Perform the following steps to install the Windows Media Player Plug-in Wizard.</span></span>

1.  <span data-ttu-id="43060-117">找出安裝 Windows SDK 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="43060-117">Locate the folder where you installed the Windows SDK.</span></span> <span data-ttu-id="43060-118">展開資料夾以查看其子資料夾，然後流覽至 [範例 \\ 多媒體 \\ WMP \\ \\ wmpwiz]。</span><span class="sxs-lookup"><span data-stu-id="43060-118">Expand the folder to view its subfolders, and navigate to Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span>
2.  <span data-ttu-id="43060-119">找出下列三個檔案：</span><span class="sxs-lookup"><span data-stu-id="43060-119">Locate the following three files:</span></span>
    -   <span data-ttu-id="43060-120">wmpwiz .vsz</span><span class="sxs-lookup"><span data-stu-id="43060-120">wmpwiz.vsz</span></span>
    -   <span data-ttu-id="43060-121">wmpwiz 的 vsdir</span><span class="sxs-lookup"><span data-stu-id="43060-121">wmpwiz.vsdir</span></span>
    -   <span data-ttu-id="43060-122">wmpwiz .ico</span><span class="sxs-lookup"><span data-stu-id="43060-122">wmpwiz.ico</span></span>
3.  <span data-ttu-id="43060-123">使用文字編輯器（例如 [記事本]）編輯 wmpwiz .vsz 檔。</span><span class="sxs-lookup"><span data-stu-id="43060-123">Using a text editor, such as Notepad, edit the wmpwiz.vsz file.</span></span>

    <span data-ttu-id="43060-124">尋找下列程式碼行：</span><span class="sxs-lookup"><span data-stu-id="43060-124">Locate the following line:</span></span>

    ```
    Wizard=VsWizard.<VsWizardEngine version goes here>
    ```

    

    <span data-ttu-id="43060-125">`<VsWizardEngine version goes here>`根據您已安裝的 Visual Studio 版本，變更為下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="43060-125">Change `<VsWizardEngine version goes here>` to one of the following values, depending on which version of Visual Studio you have installed.</span></span>

    

    | <span data-ttu-id="43060-126">值</span><span class="sxs-lookup"><span data-stu-id="43060-126">Value</span></span>              | <span data-ttu-id="43060-127">Visual Studio 版本</span><span class="sxs-lookup"><span data-stu-id="43060-127">Visual Studio version</span></span>   |
    |--------------------|-------------------------|
    | <span data-ttu-id="43060-128">VsWizardEngine 7。1</span><span class="sxs-lookup"><span data-stu-id="43060-128">VsWizardEngine.7.1</span></span> | <span data-ttu-id="43060-129">Visual Studio .NET 2003</span><span class="sxs-lookup"><span data-stu-id="43060-129">Visual Studio .NET 2003</span></span> |
    | <span data-ttu-id="43060-130">VsWizardEngine 8。0</span><span class="sxs-lookup"><span data-stu-id="43060-130">VsWizardEngine.8.0</span></span> | <span data-ttu-id="43060-131">Visual Studio 2005</span><span class="sxs-lookup"><span data-stu-id="43060-131">Visual Studio 2005</span></span>      |
    | <span data-ttu-id="43060-132">VsWizardEngine 9。0</span><span class="sxs-lookup"><span data-stu-id="43060-132">VsWizardEngine.9.0</span></span> | <span data-ttu-id="43060-133">Visual Studio 2008</span><span class="sxs-lookup"><span data-stu-id="43060-133">Visual Studio 2008</span></span>      |

    

     

    <span data-ttu-id="43060-134">尋找下列程式碼行：</span><span class="sxs-lookup"><span data-stu-id="43060-134">Locate the following line:</span></span>

    ```
    Param="ABSOLUTE_PATH = <path to wmpwiz directory goes here>"
    ```

    

    <span data-ttu-id="43060-135">切換 `<path to wmpwiz directory goes here>` 至 wizard 檔案所在的路徑。</span><span class="sxs-lookup"><span data-stu-id="43060-135">Change `<path to wmpwiz directory goes here>` to the path where the wizard files are located.</span></span>

    <span data-ttu-id="43060-136">例如，假設您有 Visual Studio 2008，而您的 wizard 檔案位於此處： C： \\ Program files \\ Microsoft sdk \\ Windows \\ 7.0 版 \\ 範例 \\ 多媒體 \\ WMP \\ \\ wmpwiz。</span><span class="sxs-lookup"><span data-stu-id="43060-136">For example, suppose you have Visual Studio 2008, and your wizard files are here: C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Samples\\Multimedia\\WMP\\wizards\\wmpwiz.</span></span> <span data-ttu-id="43060-137">然後您的 wmpwiz .vsz 檔案看起來會像這樣：</span><span class="sxs-lookup"><span data-stu-id="43060-137">Then your wmpwiz.vsz file would look like this:</span></span>

    ```
    VSWIZARD 7.0
    Wizard=VsWizard.VsWizardEngine.9.0

    Param="WIZARD_NAME = Windows Media Player Plug-in Wizard"
    Param="ABSOLUTE_PATH = C:\Program Files\Microsoft SDKs\Windows\v7.0\Samples\Multimedia\WMP\wizards\wmpwiz"
    Param="FALLBACK_LCID = 1033"
    ```

    

4.  <span data-ttu-id="43060-138">找出安裝 Visual Studio 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="43060-138">Locate the folder where you installed Visual Studio.</span></span> <span data-ttu-id="43060-139">展開資料夾以查看其子資料夾，並尋找名為 vcprojects 的資料夾。</span><span class="sxs-lookup"><span data-stu-id="43060-139">Expand the folder to view its subfolders, and locate a folder named vcprojects.</span></span>
5.  <span data-ttu-id="43060-140">將步驟2中列出的三個檔案複製到 vcprojects 資料夾。</span><span class="sxs-lookup"><span data-stu-id="43060-140">Copy the three files listed in step 2 to the vcprojects folder.</span></span> <span data-ttu-id="43060-141">現在已安裝精靈。</span><span class="sxs-lookup"><span data-stu-id="43060-141">The wizard is now installed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="43060-142">相關主題</span><span class="sxs-lookup"><span data-stu-id="43060-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43060-143">建立外掛程式</span><span class="sxs-lookup"><span data-stu-id="43060-143">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> <dt>

[<span data-ttu-id="43060-144">使用外掛程式嚮導搭配 Visual Studio</span><span class="sxs-lookup"><span data-stu-id="43060-144">Using the Plug-in Wizard with Visual Studio</span></span>](using-the-plug-in-wizard-with-visual-studio.md)
</dt> </dl>

 

 




