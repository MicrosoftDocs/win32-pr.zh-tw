---
title: 使用外掛程式嚮導搭配 Visual Studio
description: 使用外掛程式嚮導搭配 Visual Studio
ms.assetid: 5d5521b7-5cbc-4259-92b1-a7250853fa2e
keywords:
- Windows Media Player 外掛程式，Visual Studio
- 外掛程式，Visual Studio
- 建立外掛程式，Visual Studio
- Windows Media Player 外掛程式嚮導] 中 Visual Studio
- Visual Studio，Windows Media Player 外掛程式嚮導
- 外掛程式嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7f7db9bdc2a99a42f60c2faf38605e50e7dd3e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301235"
---
# <a name="using-the-plug-in-wizard-with-visual-studio"></a><span data-ttu-id="56599-109">使用外掛程式嚮導搭配 Visual Studio</span><span class="sxs-lookup"><span data-stu-id="56599-109">Using the Plug-in Wizard with Visual Studio</span></span>

<span data-ttu-id="56599-110">安裝必要的元件之後，您可以快速地建立將作為起點的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="56599-110">After you have installed the necessary components, you can quickly create a plug-in that will serve as a starting point.</span></span> <span data-ttu-id="56599-111">下列步驟將引導您。</span><span class="sxs-lookup"><span data-stu-id="56599-111">The following steps will guide you.</span></span>

1.  <span data-ttu-id="56599-112">啟動 Microsoft Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="56599-112">Start Microsoft Visual Studio.</span></span>
2.  <span data-ttu-id="56599-113">**在 [檔案**] 功能表中，指向 [**新增**]，然後按一下 [**專案**]。</span><span class="sxs-lookup"><span data-stu-id="56599-113">From the **File** menu, point to **New** and then click **Project**.</span></span>
3.  <span data-ttu-id="56599-114">在 [ **專案類型**] 中，選取 [ **Visual C++ 專案**]。</span><span class="sxs-lookup"><span data-stu-id="56599-114">In **Project Types**, select **Visual C++ Projects**.</span></span>
4.  <span data-ttu-id="56599-115">在 [ **範本**] 中，選取 **Windows Media Player 外掛程式]**。</span><span class="sxs-lookup"><span data-stu-id="56599-115">In **Templates**, select **Windows Media Player Plug-in Wizard**.</span></span>
5.  <span data-ttu-id="56599-116">輸入專案的名稱。</span><span class="sxs-lookup"><span data-stu-id="56599-116">Enter a name for your project.</span></span>
6.  <span data-ttu-id="56599-117">輸入專案的位置。</span><span class="sxs-lookup"><span data-stu-id="56599-117">Enter a location for your project.</span></span> <span data-ttu-id="56599-118">這是您的專案檔案將複製到其中的資料夾。</span><span class="sxs-lookup"><span data-stu-id="56599-118">This is the folder to which your project files will be copied.</span></span>
7.  <span data-ttu-id="56599-119">按一下 **[確定** ] 啟動精靈。</span><span class="sxs-lookup"><span data-stu-id="56599-119">Click **OK** to start the wizard.</span></span>
8.  <span data-ttu-id="56599-120">選取您要建立的外掛程式類型。</span><span class="sxs-lookup"><span data-stu-id="56599-120">Select the type of plug-in you want to create.</span></span>
9.  <span data-ttu-id="56599-121">完成嚮導中其餘的任何對話方塊。</span><span class="sxs-lookup"><span data-stu-id="56599-121">Complete any remaining dialog boxes in the wizard.</span></span>
10. <span data-ttu-id="56599-122">使用 Visual Studio 開發環境來建立您的專案。</span><span class="sxs-lookup"><span data-stu-id="56599-122">Use the Visual Studio development environment to build your project.</span></span>
    > [!Note]  
    > <span data-ttu-id="56599-123">在 Windows Vista 和更新版本中，除非您以完整系統管理員存取權杖執行 Visual Studio，否則專案將不會成功建立。</span><span class="sxs-lookup"><span data-stu-id="56599-123">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="56599-124">以滑鼠右鍵按一下 Visual Studio 名稱或圖示，然後按一下 [以 **系統管理員身分執行**]。</span><span class="sxs-lookup"><span data-stu-id="56599-124">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

     

<span data-ttu-id="56599-125">嘗試建立專案之前，請務必設定您的開發環境，以指向您安裝 Windows SDK 的名稱包括和 Lib 資料夾。</span><span class="sxs-lookup"><span data-stu-id="56599-125">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="56599-126">您的編譯器和連結器將需要存取這些資料夾中的某些檔案。</span><span class="sxs-lookup"><span data-stu-id="56599-126">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="56599-127">如果您執行 Windows SDK 隨附的 Visual Studio 註冊公用程式，您的開發環境可能已經設定為指向 Windows SDK Include 和 Lib 資料夾。</span><span class="sxs-lookup"><span data-stu-id="56599-127">If you ran the Visual Studio Registration utility that comes with the Windows SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="56599-128">否則，您必須手動設定開發環境。</span><span class="sxs-lookup"><span data-stu-id="56599-128">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="56599-129">若要手動設定 Visual Studio，請使用下列步驟。</span><span class="sxs-lookup"><span data-stu-id="56599-129">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="56599-130">在 **[工具]** 功能表上，按一下 **[選項]** 。</span><span class="sxs-lookup"><span data-stu-id="56599-130">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="56599-131">按一下 [ **專案和方案**]，然後按一下 [ **VC + + 目錄**]。</span><span class="sxs-lookup"><span data-stu-id="56599-131">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="56599-132">在 [ **顯示目錄**] 下，按一下 [ **包含** 檔案] 或 [文檔 **庫** 檔案]。</span><span class="sxs-lookup"><span data-stu-id="56599-132">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="56599-133">新增所需檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="56599-133">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="56599-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="56599-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="56599-135">建立外掛程式</span><span class="sxs-lookup"><span data-stu-id="56599-135">Building a Plug-in</span></span>](building-a-plug-in.md)
</dt> </dl>

 

 




