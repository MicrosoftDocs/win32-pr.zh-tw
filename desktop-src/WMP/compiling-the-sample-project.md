---
title: 編譯範例專案
description: 編譯範例專案
ms.assetid: c605042e-ec45-44c7-afca-42a874882eab
keywords:
- Windows Media Player 線上商店，編譯範例專案
- 線上商店，編譯範例專案
- 輸入2個線上商店，編譯範例專案
- Windows Media Player 線上商店、範例專案
- 線上商店、範例專案
- 類型2線上商店、範例專案
- 專案嚮導 Windows Media Player 線上商店
- project wizard、線上商店
- 輸入2線上商店、專案嚮導
- 外掛程式，專案嚮導
- 專案嚮導 Windows Media Player 外掛程式
- 編譯範例專案
- 範例，請輸入2個線上商店
- 專案嚮導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1ea2382e5852965b246f1ef303e5e70d160cb22
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968436"
---
# <a name="compiling-the-sample-project"></a><span data-ttu-id="1e55a-117">編譯範例專案</span><span class="sxs-lookup"><span data-stu-id="1e55a-117">Compiling the Sample Project</span></span>

<span data-ttu-id="1e55a-118">Wizard 會產生編譯範例專案所需的所有檔案，因此您不需要變更預設的專案設定。</span><span class="sxs-lookup"><span data-stu-id="1e55a-118">The wizard generates all the files you need to compile the sample project, so you shouldn't need to change the default project settings.</span></span> <span data-ttu-id="1e55a-119">在 Visual Studio 中，按一下 [ **組建** ] 功能表上的 [ **建立方案** ]，以建立並註冊 COM 元件。</span><span class="sxs-lookup"><span data-stu-id="1e55a-119">In Visual Studio, from the **Build** menu, click **Build Solution** to build and register the COM component.</span></span> <span data-ttu-id="1e55a-120">根據預設，偵錯工具設定為使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="1e55a-120">By default, the Debug configuration is active.</span></span>

> [!Note]  
> <span data-ttu-id="1e55a-121">在 Windows Vista 和更新版本中，除非您以完整系統管理員存取權杖執行 Visual Studio，否則專案將不會成功建立。</span><span class="sxs-lookup"><span data-stu-id="1e55a-121">In Windows Vista and later, the project will not build successfully unless you run Visual Studio with a full administrator access token.</span></span> <span data-ttu-id="1e55a-122">以滑鼠右鍵按一下 Visual Studio 名稱或圖示，然後按一下 [以 **系統管理員身分執行**]。</span><span class="sxs-lookup"><span data-stu-id="1e55a-122">Right-click the Visual Studio name or icon, and click **Run as administrator**.</span></span>

 

<span data-ttu-id="1e55a-123">嘗試建立專案之前，請務必設定您的開發環境，以指向您安裝 Windows SDK 的名稱包括和 Lib 資料夾。</span><span class="sxs-lookup"><span data-stu-id="1e55a-123">Before attempting to build the project, be sure to configure your development environment to point to the folders named Include and Lib where you installed the Windows SDK.</span></span> <span data-ttu-id="1e55a-124">您的編譯器和連結器將需要存取這些資料夾中的某些檔案。</span><span class="sxs-lookup"><span data-stu-id="1e55a-124">Your compiler and linker will need access to some of the files in these folders.</span></span>

<span data-ttu-id="1e55a-125">如果您執行的是 Windows Vista SDK 隨附的 Visual Studio 註冊公用程式，您的開發環境可能已經設定成指向 Windows SDK Include 和 Lib 資料夾。</span><span class="sxs-lookup"><span data-stu-id="1e55a-125">If you ran the Visual Studio Registration utility that comes with the Windows Vista SDK, your development environment has probably already been configured to point to the Windows SDK Include and Lib folders.</span></span> <span data-ttu-id="1e55a-126">否則，您必須手動設定開發環境。</span><span class="sxs-lookup"><span data-stu-id="1e55a-126">Otherwise, you must manually configure your development environment.</span></span>

<span data-ttu-id="1e55a-127">若要手動設定 Visual Studio，請使用下列步驟。</span><span class="sxs-lookup"><span data-stu-id="1e55a-127">To manually configure Visual Studio, use the following steps.</span></span>

1.  <span data-ttu-id="1e55a-128">在 **[工具]** 功能表上，按一下 **[選項]** 。</span><span class="sxs-lookup"><span data-stu-id="1e55a-128">On the **Tools** menu, click **Options**.</span></span>
2.  <span data-ttu-id="1e55a-129">按一下 [ **專案和方案**]，然後按一下 [ **VC + + 目錄**]。</span><span class="sxs-lookup"><span data-stu-id="1e55a-129">Click **Projects and Solutions**, and then click **VC++ Directories**.</span></span>
3.  <span data-ttu-id="1e55a-130">在 [ **顯示目錄**] 下，按一下 [ **包含** 檔案] 或 [文檔 **庫** 檔案]。</span><span class="sxs-lookup"><span data-stu-id="1e55a-130">Under **Show directories for**, click **Include files** or **Library files**.</span></span>
4.  <span data-ttu-id="1e55a-131">新增所需檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="1e55a-131">Add the directories for the required files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="1e55a-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="1e55a-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1e55a-133">建立 Type 2 線上商店的外掛程式</span><span class="sxs-lookup"><span data-stu-id="1e55a-133">Building the Plug-in for a Type 2 Online Store</span></span>](building-the-plug-in-for-a-type-2-online-store.md)
</dt> </dl>

 

 




