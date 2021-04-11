---
description: 本教學課程示範如何取得單一語言應用程式，並讓它成為世界級的應用程式。 此應用程式是以 Microsoft Visual Studio 內建的完整方案形式。
ms.assetid: 6d71aa90-8444-4f30-a2f8-f1a2aab015b0
title: 將多語系消費者介面支援新增至應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 192d9053513a7fe915990c80deb32ffdb9114910
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851828"
---
# <a name="adding-multilingual-user-interface-support-to-an-application"></a><span data-ttu-id="ce37f-104">將多語系消費者介面支援新增至應用程式</span><span class="sxs-lookup"><span data-stu-id="ce37f-104">Adding Multilingual User Interface Support to an Application</span></span>

<span data-ttu-id="ce37f-105">本教學課程示範如何取得單一語言應用程式，並讓它成為世界級的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-105">This tutorial demonstrates how to take a monolingual application and make it world-ready.</span></span> <span data-ttu-id="ce37f-106">此應用程式是以 Microsoft Visual Studio 內建的完整方案形式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-106">This application is in the form of a complete solution that is built within Microsoft Visual Studio.</span></span>

-   [<span data-ttu-id="ce37f-107">概觀</span><span class="sxs-lookup"><span data-stu-id="ce37f-107">Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="ce37f-108">Hello MUI 背後的構想</span><span class="sxs-lookup"><span data-stu-id="ce37f-108">The Idea Behind Hello MUI</span></span>](#the-idea-behind-hello-mui)
-   [<span data-ttu-id="ce37f-109">設定 Hello MUI 方案</span><span class="sxs-lookup"><span data-stu-id="ce37f-109">Setting up the Hello MUI Solution</span></span>](#setting-up-the-hello-mui-solution)
    -   [<span data-ttu-id="ce37f-110">平臺需求</span><span class="sxs-lookup"><span data-stu-id="ce37f-110">Platform Requirements</span></span>](#platform-requirements)
    -   [<span data-ttu-id="ce37f-111">先決條件</span><span class="sxs-lookup"><span data-stu-id="ce37f-111">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="ce37f-112">步驟0：建立硬式編碼的 Hello MUI</span><span class="sxs-lookup"><span data-stu-id="ce37f-112">Step 0: Creating the Hard-coded Hello MUI</span></span>](#step-0-creating-the-hard-coded-hello-mui)
-   [<span data-ttu-id="ce37f-113">步驟1：執行基本資源模組</span><span class="sxs-lookup"><span data-stu-id="ce37f-113">Step 1: Implementing the Basic Resource Module</span></span>](#step-1-implementing-the-basic-resource-module)
-   [<span data-ttu-id="ce37f-114">步驟2：建立基本資源模組</span><span class="sxs-lookup"><span data-stu-id="ce37f-114">Step 2: Building the Basic Resource Module</span></span>](#step-2-building-the-basic-resource-module)
    -   [<span data-ttu-id="ce37f-115">分割各種語言資源模組：總覽</span><span class="sxs-lookup"><span data-stu-id="ce37f-115">Splitting the Various Language Resource Modules: An Overview</span></span>](#splitting-the-various-language-resource-modules-an-overview)
    -   [<span data-ttu-id="ce37f-116">分割不同的語言資源模組：建立檔案</span><span class="sxs-lookup"><span data-stu-id="ce37f-116">Splitting the Various Language Resource Modules: Creating the Files</span></span>](#splitting-the-various-language-resource-modules-creating-the-files)
-   [<span data-ttu-id="ce37f-117">步驟3：建立 Resource-Savvy "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="ce37f-117">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>](#step-3-creating-a-resource-savvy-hello-mui)
-   [<span data-ttu-id="ce37f-118">步驟4：全球化「Hello MUI」</span><span class="sxs-lookup"><span data-stu-id="ce37f-118">Step 4: Globalizing "Hello MUI"</span></span>](#step-4-globalizing-hello-mui)
-   [<span data-ttu-id="ce37f-119">步驟5：自訂 "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="ce37f-119">Step 5: Customizing "Hello MUI"</span></span>](#step-5-customizing-hello-mui)
-   [<span data-ttu-id="ce37f-120">MUI 的其他考慮</span><span class="sxs-lookup"><span data-stu-id="ce37f-120">Additional Considerations for MUI</span></span>](#additional-considerations-for-mui)
    -   [<span data-ttu-id="ce37f-121">主控台應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="ce37f-121">Support for Console Applications</span></span>](#support-for-console-applications)
    -   [<span data-ttu-id="ce37f-122">判斷在執行時間支援的語言</span><span class="sxs-lookup"><span data-stu-id="ce37f-122">Determination of Languages to Support at Run-Time</span></span>](#determination-of-languages-to-support-at-run-time)
    -   [<span data-ttu-id="ce37f-123">Windows Vista 之前版本中的複雜字集支援</span><span class="sxs-lookup"><span data-stu-id="ce37f-123">Complex Script Support in Versions Prior to Windows Vista</span></span>](#complex-script-support-in-versions-prior-to-windows-vista)
-   [<span data-ttu-id="ce37f-124">總結</span><span class="sxs-lookup"><span data-stu-id="ce37f-124">Summary</span></span>](#summary)

## <a name="overview"></a><span data-ttu-id="ce37f-125">概觀</span><span class="sxs-lookup"><span data-stu-id="ce37f-125">Overview</span></span>

<span data-ttu-id="ce37f-126">從 Windows Vista 開始，Windows 作業系統本身的建立是多語系平臺，可讓您建立使用 Windows MUI 資源模型的多語系應用程式，並提供額外的支援。</span><span class="sxs-lookup"><span data-stu-id="ce37f-126">Beginning with Windows Vista, the Windows operating system itself was built from the ground up to be a multilingual platform, with additional support that enables you to create multilingual applications that use the Windows MUI resource model.</span></span>

<span data-ttu-id="ce37f-127">本教學課程說明這項新的多語系應用程式支援，包括下列層面：</span><span class="sxs-lookup"><span data-stu-id="ce37f-127">This tutorial illustrates this new support for multilingual applications by covering the following aspects:</span></span>

-   <span data-ttu-id="ce37f-128">使用改良的 MUI 平臺支援，輕鬆地啟用多語系應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-128">Uses the improved MUI platform support to easily enable multilingual applications.</span></span>
-   <span data-ttu-id="ce37f-129">擴充多語系應用程式，在 Windows Vista 之前的 Windows 版本上執行。</span><span class="sxs-lookup"><span data-stu-id="ce37f-129">Extends multilingual applications to run on versions of Windows prior to Windows Vista.</span></span>
-   <span data-ttu-id="ce37f-130">請考慮開發專用的多語系應用程式（例如主控台應用程式）所需的其他考慮。</span><span class="sxs-lookup"><span data-stu-id="ce37f-130">Touches on the additional considerations involved in developing specialized multilingual applications such as console applications.</span></span>

<span data-ttu-id="ce37f-131">這些連結可協助您快速複習國際化與 MUI 的概念：</span><span class="sxs-lookup"><span data-stu-id="ce37f-131">These links help provide a quick refresher on the concepts on internationalization and MUI:</span></span>

-   <span data-ttu-id="ce37f-132">[國際化簡介](understanding-internationalization.md)。</span><span class="sxs-lookup"><span data-stu-id="ce37f-132">[Quick overview of internationalization](understanding-internationalization.md).</span></span>
-   <span data-ttu-id="ce37f-133">[MUI 概念](understanding-mui.md)。</span><span class="sxs-lookup"><span data-stu-id="ce37f-133">[MUI Concepts](understanding-mui.md).</span></span>
-   <span data-ttu-id="ce37f-134">[使用 MUI 開發 Win32 應用程式](using-multilingual-user-interface.md)。</span><span class="sxs-lookup"><span data-stu-id="ce37f-134">[Using MUI to develop Win32 applications](using-multilingual-user-interface.md).</span></span>

### <a name="the-idea-behind-hello-mui"></a><span data-ttu-id="ce37f-135">Hello MUI 背後的構想</span><span class="sxs-lookup"><span data-stu-id="ce37f-135">The Idea Behind Hello MUI</span></span>

<span data-ttu-id="ce37f-136">您可能已經熟悉傳統的 Hello World 應用程式，其中說明基本的程式設計概念。</span><span class="sxs-lookup"><span data-stu-id="ce37f-136">You are probably familiar with the classic Hello World application, which illustrates basic programming concepts.</span></span> <span data-ttu-id="ce37f-137">本教學課程採用類似的方法來說明如何使用 MUI 資源模型來更新單一語言應用程式，以建立名為 Hello MUI 的多國語言版本。</span><span class="sxs-lookup"><span data-stu-id="ce37f-137">This tutorial takes a similar approach to illustrate how to use the MUI resource model to update a monolingual application to create a multilingual version called Hello MUI.</span></span>

> [!Note]  
> <span data-ttu-id="ce37f-138">本教學課程中的工作會在詳細步驟中說明，因為這些活動必須執行的有效位數，以及對這些工作沒有經驗的開發人員說明詳細資料的需要。</span><span class="sxs-lookup"><span data-stu-id="ce37f-138">The tasks in this tutorial are described in detailed steps because of the precision with which these activities must be performed, and the need to explain the details to developers who have little experience with these tasks.</span></span>

 

## <a name="setting-up-the-hello-mui-solution"></a><span data-ttu-id="ce37f-139">設定 Hello MUI 方案</span><span class="sxs-lookup"><span data-stu-id="ce37f-139">Setting up the Hello MUI Solution</span></span>

<span data-ttu-id="ce37f-140">這些步驟概述如何準備建立 Hello MUI 方案。</span><span class="sxs-lookup"><span data-stu-id="ce37f-140">These steps outline how to prepare to create the Hello MUI solution.</span></span>

### <a name="platform-requirements"></a><span data-ttu-id="ce37f-141">平台需求</span><span class="sxs-lookup"><span data-stu-id="ce37f-141">Platform Requirements</span></span>

<span data-ttu-id="ce37f-142">您必須使用適用于 Windows 7 的 Windows 軟體開發套件 (SDK) 和 Visual Studio 2008，在本教學課程中編譯器代碼範例。</span><span class="sxs-lookup"><span data-stu-id="ce37f-142">You must compile the code samples in this tutorial using the Windows Software Development Kit (SDK) for Windows 7 and Visual Studio 2008.</span></span> <span data-ttu-id="ce37f-143">Windows 7 SDK 會安裝在 Windows XP、Windows Vista 和 Windows 7 上，而範例解決方案可以建立在這些作業系統版本上。</span><span class="sxs-lookup"><span data-stu-id="ce37f-143">The Windows 7 SDK will install on Windows XP, Windows Vista and Windows 7, and the sample solution can be built on any of these operating system versions.</span></span>

<span data-ttu-id="ce37f-144">本教學課程中的所有程式碼範例都是設計來在 x86 和 x64 版本的 Windows XP、Windows Vista 和 Windows 7 上執行。</span><span class="sxs-lookup"><span data-stu-id="ce37f-144">All code samples in this tutorial are designed to be executed on x86 and x64 versions of Windows XP, Windows Vista and Windows 7.</span></span> <span data-ttu-id="ce37f-145">在適當的情況下，將不會在 Windows XP 上運作的特定部分會被呼叫。</span><span class="sxs-lookup"><span data-stu-id="ce37f-145">Specific parts that will not work on Windows XP are called out where appropriate.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ce37f-146">必要條件</span><span class="sxs-lookup"><span data-stu-id="ce37f-146">Prerequisites</span></span>

1.  <span data-ttu-id="ce37f-147">安裝 Visual Studio 2008。</span><span class="sxs-lookup"><span data-stu-id="ce37f-147">Install Visual Studio 2008.</span></span>

    <span data-ttu-id="ce37f-148">如需詳細資訊，請參閱 [Visual Studio 開發人員中心](https://msdn.microsoft.com/vstudio/default.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ce37f-148">For more information, see the [Visual Studio Developer Center](https://msdn.microsoft.com/vstudio/default.aspx).</span></span>

2.  <span data-ttu-id="ce37f-149">安裝適用于 Windows 7 的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="ce37f-149">Install the Windows SDK for Windows 7.</span></span>

    <span data-ttu-id="ce37f-150">您可以從 [Windows 開發人員中心](https://msdn.microsoft.com/windowsserver/bb980924.aspx)的 [Windows SDK] 頁面進行安裝。</span><span class="sxs-lookup"><span data-stu-id="ce37f-150">You can install it from the Windows SDK page of the [Windows Developer Center](https://msdn.microsoft.com/windowsserver/bb980924.aspx).</span></span> <span data-ttu-id="ce37f-151">SDK 包含從 Windows XP 到最新版本的作業系統版本開發應用程式的公用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-151">The SDK includes utilities to develop applications for OS versions starting from Windows XP through the most recent.</span></span>

    > [!Note]  
    > <span data-ttu-id="ce37f-152">如果您未將套件安裝到預設位置，或者您不是在系統磁片磁碟機（通常是 C 磁片磁碟機）上安裝，請記下安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="ce37f-152">If you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>

     

3.  <span data-ttu-id="ce37f-153">設定 Visual Studio 命令列參數。</span><span class="sxs-lookup"><span data-stu-id="ce37f-153">Configure the Visual Studio command line parameters.</span></span>

    1.  <span data-ttu-id="ce37f-154">開啟 Visual Studio 的命令視窗。</span><span class="sxs-lookup"><span data-stu-id="ce37f-154">Open a Visual Studio command window.</span></span>
    2.  <span data-ttu-id="ce37f-155">輸入 **集路徑**。</span><span class="sxs-lookup"><span data-stu-id="ce37f-155">Type **set path**.</span></span>
    3.  <span data-ttu-id="ce37f-156">確認 path 變數包含 Windows 7 SDK 的 bin 資料夾路徑： .。。Microsoft Sdk \\ Windows \\ 7.0 版 \\</span><span class="sxs-lookup"><span data-stu-id="ce37f-156">Confirm that the path variable includes the path of the bin folder of the Windows 7 SDK: ...Microsoft SDKs\\Windows\\v7.0\\bin</span></span>

4.  <span data-ttu-id="ce37f-157">安裝 Microsoft NLS 下層 Api 附加元件套件。</span><span class="sxs-lookup"><span data-stu-id="ce37f-157">Install the Microsoft NLS downlevel APIs add-on package.</span></span>
    > [!Note]  
    > <span data-ttu-id="ce37f-158">在本教學課程的內容中，只有當您要自訂應用程式，才能在 windows Vista 之前的 Windows 版本上執行時，才需要此套件。</span><span class="sxs-lookup"><span data-stu-id="ce37f-158">In the context of this tutorial, this package is necessary only if you will be customizing the application to run on Windows versions prior to Windows Vista.</span></span> <span data-ttu-id="ce37f-159">請參閱 [步驟5：自訂 HELLO MUI](#step-5-customizing-hello-mui)。</span><span class="sxs-lookup"><span data-stu-id="ce37f-159">See [Step 5: Customizing Hello MUI](#step-5-customizing-hello-mui).</span></span>

     

    1.  <span data-ttu-id="ce37f-160">從其 [下載網站](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en)下載並安裝套件。</span><span class="sxs-lookup"><span data-stu-id="ce37f-160">Download and install the package from its [download site](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en).</span></span>
    2.  <span data-ttu-id="ce37f-161">如同 Windows SDK，如果您未將套件安裝到預設位置，或者您不是安裝在系統磁片磁碟機（通常是 C 磁片磁碟機），請記下安裝路徑。</span><span class="sxs-lookup"><span data-stu-id="ce37f-161">As with the Windows SDK, if you are not installing the package to the default location, or if you are not installing on the system drive, which is usually the C drive, make note of the install path.</span></span>
    3.  <span data-ttu-id="ce37f-162">如果您的開發平臺是 Windows XP 或 Windows Server 2003，請確認已正確安裝及註冊 Nlsdl.dll。</span><span class="sxs-lookup"><span data-stu-id="ce37f-162">If your development platform is Windows XP or Windows Server 2003, confirm that Nlsdl.dll is installed and registered correctly.</span></span>

        1.  <span data-ttu-id="ce37f-163">流覽至安裝路徑位置下的「可轉散發套件」資料夾。</span><span class="sxs-lookup"><span data-stu-id="ce37f-163">Browse to the "redist" folder under the install path location.</span></span>
        2.  <span data-ttu-id="ce37f-164">執行適當的可轉散發套件 \* Nlsdl。exe，例如 nlsdl.x86.exe。</span><span class="sxs-lookup"><span data-stu-id="ce37f-164">Run the appropriate redistributable Nlsdl.\*.exe, such as nlsdl.x86.exe.</span></span> <span data-ttu-id="ce37f-165">此步驟會安裝並註冊 Nlsdl.dll。</span><span class="sxs-lookup"><span data-stu-id="ce37f-165">This step installs and registers Nlsdl.dll.</span></span>

    > [!Note]  
    > <span data-ttu-id="ce37f-166">如果您開發的應用程式使用 MUI，而且必須在 windows Vista 之前的 Windows 版本上執行，則 Nlsdl.dll 必須存在於目的地 Windows 平臺上。</span><span class="sxs-lookup"><span data-stu-id="ce37f-166">If you develop an application that uses MUI and that must run on Windows versions prior to Windows Vista, Nlsdl.dll must be present on the destination Windows platform.</span></span> <span data-ttu-id="ce37f-167">在大部分的情況下，這表示應用程式必須執行可轉散發 Nlsdl 安裝程式 (，而不只是複製 Nlsdl.dll 本身) 。</span><span class="sxs-lookup"><span data-stu-id="ce37f-167">In most cases, this means that the application needs to carry and install the redistributable Nlsdl installer (and not merely copy Nlsdl.dll itself).</span></span>

     

## <a name="step-0-creating-the-hard-coded-hello-mui"></a><span data-ttu-id="ce37f-168">步驟0：建立硬式編碼的 Hello MUI</span><span class="sxs-lookup"><span data-stu-id="ce37f-168">Step 0: Creating the Hard-coded Hello MUI</span></span>

<span data-ttu-id="ce37f-169">本教學課程的開頭是 Hello MUI 應用程式的單一語言版本。</span><span class="sxs-lookup"><span data-stu-id="ce37f-169">This tutorial begins with the monolingual version of the Hello MUI application.</span></span> <span data-ttu-id="ce37f-170">應用程式會假設使用 c + + 程式設計語言、寬字元字串和 [**>messageboxw**](/windows/win32/api/winuser/nf-winuser-messagebox) 函式進行輸出。</span><span class="sxs-lookup"><span data-stu-id="ce37f-170">The application assumes the use of the C++ programming language, wide character strings, and the [**MessageBoxW**](/windows/win32/api/winuser/nf-winuser-messagebox) function for output.</span></span>

<span data-ttu-id="ce37f-171">首先，建立初始 GuiStep \_ 0 應用程式以及 HelloMUI 方案，其中包含本教學課程中的所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-171">Begin by creating the initial GuiStep\_0 application, as well as the HelloMUI solution, which contain all of the applications in this tutorial.</span></span>

1.  <span data-ttu-id="ce37f-172">在 Visual Studio 2008 中，建立新專案。</span><span class="sxs-lookup"><span data-stu-id="ce37f-172">In Visual Studio 2008, create a new project.</span></span> <span data-ttu-id="ce37f-173">使用下列設定和值：</span><span class="sxs-lookup"><span data-stu-id="ce37f-173">Use the following settings and values:</span></span>

    1.  <span data-ttu-id="ce37f-174">專案類型：在 Visual C++ 選取 [Win32]，然後在 [Visual Studio 安裝的範本] 底下選取 [Win32 專案]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-174">Project type: Under Visual C++ select Win32, and then under Visual Studio installed templates select Win32 Project.</span></span>
    2.  <span data-ttu-id="ce37f-175">名稱： GuiStep \_ 0。</span><span class="sxs-lookup"><span data-stu-id="ce37f-175">Name: GuiStep\_0.</span></span>
    3.  <span data-ttu-id="ce37f-176">位置： *ProjectRootDirectory* (稍後的步驟會參考此目錄) 。</span><span class="sxs-lookup"><span data-stu-id="ce37f-176">Location: *ProjectRootDirectory* (Later steps reference this directory).</span></span>
    4.  <span data-ttu-id="ce37f-177">解決方案名稱： HelloMUI。</span><span class="sxs-lookup"><span data-stu-id="ce37f-177">Solution Name: HelloMUI.</span></span>
    5.  <span data-ttu-id="ce37f-178">選取 [為方案建立目錄]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-178">Select Create directory for solution.</span></span>
    6.  <span data-ttu-id="ce37f-179">在 Win32 應用程式精靈中，選取預設的應用程式類型： Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-179">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="ce37f-180">設定專案執行緒模型：</span><span class="sxs-lookup"><span data-stu-id="ce37f-180">Configure the project threading model:</span></span>

    1.  <span data-ttu-id="ce37f-181">在方案總管中，以滑鼠右鍵按一下專案 GuiStep \_ 0，然後選取 [屬性]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-181">In the Solution Explorer, right-click the project GuiStep\_0, and then select Properties.</span></span>
    2.  <span data-ttu-id="ce37f-182">在 [專案屬性頁] 對話方塊中：</span><span class="sxs-lookup"><span data-stu-id="ce37f-182">In the project Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="ce37f-183">在左上方的下拉式清單中，將 [設定] 設定為 [所有設定]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-183">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="ce37f-184">在 [設定屬性] 下展開 [C/c + +]，選取 [程式碼產生]，並設定執行時間程式庫：多執行緒的 Debug () /MTd</span><span class="sxs-lookup"><span data-stu-id="ce37f-184">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="ce37f-185">\_以下列程式碼取代 GuiStep 0 .cpp 的內容：</span><span class="sxs-lookup"><span data-stu-id="ce37f-185">Replace the contents of GuiStep\_0.cpp with the following code:</span></span>
    ```C++
    // GuiStep_0.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_0.h"

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        MessageBoxW(NULL,L"Hello MUI",L"HelloMUI!",MB_OK | MB_ICONINFORMATION);
        return 0;
    }
    ```

    

4.  <span data-ttu-id="ce37f-186">建置並執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-186">Build and run the application.</span></span>

<span data-ttu-id="ce37f-187">上述直接原始程式碼可讓您以簡單的方式設計選項來進行硬式編碼或內嵌，讓使用者看到的所有輸出（在此案例中為文字 "Hello MUI"）。</span><span class="sxs-lookup"><span data-stu-id="ce37f-187">The straightforward source code above makes the simplistic design choice of hard-coding, or embedding, all the output the user will see—in this case the text "Hello MUI".</span></span> <span data-ttu-id="ce37f-188">這項選擇會限制無法辨識英文文字 "Hello" 之使用者的應用程式公用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-188">This choice limits the utility of the application for users who don't recognize the English word "Hello."</span></span> <span data-ttu-id="ce37f-189">因為 MUI 是以技術為基礎的英文縮寫，所以在本教學課程中會假設它是所有語言的字串「MUI」。</span><span class="sxs-lookup"><span data-stu-id="ce37f-189">Because MUI is a technology-based English acronym, it is assumed for this tutorial that the string remains "MUI" for all languages.</span></span>

## <a name="step-1-implementing-the-basic-resource-module"></a><span data-ttu-id="ce37f-190">步驟1：執行基本資源模組</span><span class="sxs-lookup"><span data-stu-id="ce37f-190">Step 1: Implementing the Basic Resource Module</span></span>

<span data-ttu-id="ce37f-191">Microsoft Win32 有很長的功能，可讓應用程式開發人員將其 UI 資源資料與應用程式原始程式碼分開。</span><span class="sxs-lookup"><span data-stu-id="ce37f-191">Microsoft Win32 has long exposed the capability for application developers to separate their UI resource data from application source code.</span></span> <span data-ttu-id="ce37f-192">這種分隔會以 Win32 資源模型的形式呈現，在此模式中，會將字串、點陣圖、圖示、訊息和其他通常顯示給使用者的專案封裝到可執行檔的相異區段中，並與可執行程式碼分開。</span><span class="sxs-lookup"><span data-stu-id="ce37f-192">This separation comes in the form of the Win32 resource model, in which strings, bitmaps, icons, messages and other items normally displayed to a user are packaged into a distinct section of the executable, separated from executable code.</span></span>

<span data-ttu-id="ce37f-193">為了說明可執行程式碼與資源資料封裝之間的分隔，在此步驟中，教學課程會將先前硬式編碼的 "Hello" 字串放 ("en-us" 資源) 至 HelloModule \_ en us 專案中 DLL 模組的資源區段 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ce37f-193">To illustrate this separation between executable code and resource data packaging, in this step the tutorial places the previously hard-coded "Hello" string (the "en-US" resource) into the resource section of a DLL module in the HelloModule\_en\_us project.</span></span>

<span data-ttu-id="ce37f-194">此 Win32 DLL 也可以包含程式庫類型可執行檔功能 (因為任何其他 DLL 可能) 。</span><span class="sxs-lookup"><span data-stu-id="ce37f-194">This Win32 DLL could also contain library type executable functionality (as any other DLL might).</span></span> <span data-ttu-id="ce37f-195">但為了協助您專注于 Win32 資源相關層面，我們會將執行時間 DLL 程式碼 stub 在 dllmain 中。</span><span class="sxs-lookup"><span data-stu-id="ce37f-195">But to help focus on the Win32 resource-related aspects, we leave the run-time DLL code stubbed out in dllmain.cpp.</span></span> <span data-ttu-id="ce37f-196">本教學課程的後續章節會使用此處建立的 HelloModule 資源資料，也會顯示適當的執行時間程式碼。</span><span class="sxs-lookup"><span data-stu-id="ce37f-196">Subsequent sections of this tutorial make use of the HelloModule resource data being built here and also present appropriate runtime code.</span></span>

<span data-ttu-id="ce37f-197">若要建立 Win32 資源模組，請從建立具有 stub out dllmain 的 DLL 開始：</span><span class="sxs-lookup"><span data-stu-id="ce37f-197">To construct a Win32 resource module, start by creating a DLL with a stubbed out dllmain:</span></span>

1.  <span data-ttu-id="ce37f-198">將新專案新增至 HelloMUI 方案：</span><span class="sxs-lookup"><span data-stu-id="ce37f-198">Add a new project to the HelloMUI solution:</span></span>

    1.  <span data-ttu-id="ce37f-199">在 [檔案] 功能表中，選取 [加入]，然後選取 [新增專案]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-199">From the File menu, select Add, and then New Project.</span></span>
    2.  <span data-ttu-id="ce37f-200">專案類型： Win32 專案。</span><span class="sxs-lookup"><span data-stu-id="ce37f-200">Project type: Win32 Project.</span></span>
    3.  <span data-ttu-id="ce37f-201">名稱： HelloModule \_ en \_ us。</span><span class="sxs-lookup"><span data-stu-id="ce37f-201">Name: HelloModule\_en\_us.</span></span>
    4.  <span data-ttu-id="ce37f-202">位置： *ProjectRootDirectory* \\ HelloMUI。</span><span class="sxs-lookup"><span data-stu-id="ce37f-202">Location: *ProjectRootDirectory*\\HelloMUI.</span></span>
    5.  <span data-ttu-id="ce37f-203">在 [Win32 應用程式] 中，選取 [應用程式類型： DLL]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-203">In the Win32 Application Wizard, select Application type: DLL.</span></span>

2.  <span data-ttu-id="ce37f-204">設定此專案的執行緒模型：</span><span class="sxs-lookup"><span data-stu-id="ce37f-204">Configure this project's threading model:</span></span>

    1.  <span data-ttu-id="ce37f-205">在 [方案總管中，以滑鼠右鍵按一下 HelloModule 的專案， \_ \_ 然後選取 [屬性]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-205">In the Solution Explorer, right-click the project HelloModule\_en\_us and select Properties.</span></span>
    2.  <span data-ttu-id="ce37f-206">在專案的 [屬性頁] 對話方塊中：</span><span class="sxs-lookup"><span data-stu-id="ce37f-206">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="ce37f-207">在左上方的下拉式清單中，將 [設定] 設定為 [所有設定]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-207">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="ce37f-208">在 [設定屬性] 下展開 [C/c + +]，選取 [程式碼產生]，並設定執行時間程式庫：多執行緒的 Debug () /MTd</span><span class="sxs-lookup"><span data-stu-id="ce37f-208">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="ce37f-209">檢查 dllmain .cpp。</span><span class="sxs-lookup"><span data-stu-id="ce37f-209">Examine dllmain.cpp.</span></span> <span data-ttu-id="ce37f-210"> (您可能會想要將未參考的 \_ 參數宏新增至產生的程式碼（如我們在此所示），讓它能夠在警告層級4進行編譯。 ) </span><span class="sxs-lookup"><span data-stu-id="ce37f-210">(You may want to add the UNREFERENCED\_PARAMETER macros to the generated code, as we have here, to enable it to compile at warning level 4.)</span></span>
    ```C++
    // dllmain.cpp : Defines the entry point for the DLL application.
    #include "stdafx.h"

    BOOL APIENTRY DllMain( HMODULE hModule,
                           DWORD  ul_reason_for_call,
                           LPVOID lpReserved
                         )
    {
        UNREFERENCED_PARAMETER(hModule);
        UNREFERENCED_PARAMETER(lpReserved);

        switch (ul_reason_for_call)
        {
        case DLL_PROCESS_ATTACH:
        case DLL_THREAD_ATTACH:
        case DLL_THREAD_DETACH:
        case DLL_PROCESS_DETACH:
            break;
        }
        return TRUE;
    }
    ```

    

4.  <span data-ttu-id="ce37f-211">將 HelloModule 的資源定義檔新增至專案：</span><span class="sxs-lookup"><span data-stu-id="ce37f-211">Add a resource-definition file HelloModule.rc to the project:</span></span>

    1.  <span data-ttu-id="ce37f-212">在 [專案] \_ HelloModule \_ 中，以滑鼠右鍵按一下 [資源檔] 資料夾，然後選取 [加入]，再選取 [新增專案]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-212">Under the project HelloModule\_en\_us, right-click the Resource Files folder, and select Add, and then select New Item.</span></span>
    2.  <span data-ttu-id="ce37f-213">在 [加入新專案] 對話方塊中，選擇下列專案：</span><span class="sxs-lookup"><span data-stu-id="ce37f-213">In the Add New Item dialog box, choose the following:</span></span>

        1.  <span data-ttu-id="ce37f-214">類別：在 Visual C++ 選取資源] 底下，然後在 [Visual Studio 安裝的範本] 下，選取 [資源檔] ( .rc) 。</span><span class="sxs-lookup"><span data-stu-id="ce37f-214">Categories: Under Visual C++ select Resource, and then under "Visual Studio installed templates" select Resource File (.rc).</span></span>
        2.  <span data-ttu-id="ce37f-215">名稱： HelloModule。</span><span class="sxs-lookup"><span data-stu-id="ce37f-215">Name: HelloModule.</span></span>
        3.  <span data-ttu-id="ce37f-216">位置：接受預設值。</span><span class="sxs-lookup"><span data-stu-id="ce37f-216">Location: accept the default.</span></span>
        4.  <span data-ttu-id="ce37f-217">按一下 [新增]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-217">Click Add.</span></span>

    3.  <span data-ttu-id="ce37f-218">指定要將新的 HelloModule .rc 檔儲存為 Unicode：</span><span class="sxs-lookup"><span data-stu-id="ce37f-218">Specify that the new HelloModule.rc file is to be saved as Unicode:</span></span>

        1.  <span data-ttu-id="ce37f-219">在方案總管中，以滑鼠右鍵按一下 HelloModule，然後選取 [視圖程式碼]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-219">In the Solution Explorer, right-click HelloModule.rc, and select View Code.</span></span>
        2.  <span data-ttu-id="ce37f-220">如果您看到一則訊息，告訴您檔案已開啟，並詢問您是否要關閉它，請按一下 [是]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-220">If you see a message that tells you that the file is already open, and asks whether you want to close it, click Yes.</span></span>
        3.  <span data-ttu-id="ce37f-221">當檔案顯示為文字時，請選取功能表選取檔案，然後選取 [Advanced Save Options]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-221">With the file displayed as text, make the menu selection File and then Advanced Save Options.</span></span>
        4.  <span data-ttu-id="ce37f-222">在 [編碼] 下，指定 [Unicode-字碼頁 1200]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-222">Under Encoding, specify Unicode - Codepage 1200.</span></span>
        5.  <span data-ttu-id="ce37f-223">按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-223">Click OK.</span></span>
        6.  <span data-ttu-id="ce37f-224">儲存並關閉 HelloModule .rc。</span><span class="sxs-lookup"><span data-stu-id="ce37f-224">Save and close HelloModule.rc.</span></span>

    4.  <span data-ttu-id="ce37f-225">新增包含 "Hello" 字串的字串資料表：</span><span class="sxs-lookup"><span data-stu-id="ce37f-225">Add a string table containing the "Hello" string:</span></span>

        1.  <span data-ttu-id="ce37f-226">在資源檢視中，以滑鼠右鍵按一下 HelloModule，然後選取 [新增資源]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-226">In the Resource View, right-click HelloModule.rc and select Add Resource.</span></span>
        2.  <span data-ttu-id="ce37f-227">選取 [字串資料表]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-227">Select String Table.</span></span>
        3.  <span data-ttu-id="ce37f-228">按一下 \[新增\]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-228">Click New.</span></span>
        4.  <span data-ttu-id="ce37f-229">將字串新增至字串資料表：</span><span class="sxs-lookup"><span data-stu-id="ce37f-229">Add a string to the String Table:</span></span>

            1.  <span data-ttu-id="ce37f-230">識別碼： HELLO \_ MUI \_ STR \_ 0。</span><span class="sxs-lookup"><span data-stu-id="ce37f-230">ID: HELLO\_MUI\_STR\_0.</span></span>
            2.  <span data-ttu-id="ce37f-231">值：0。</span><span class="sxs-lookup"><span data-stu-id="ce37f-231">Value: 0.</span></span>
            3.  <span data-ttu-id="ce37f-232">標題： Hello。</span><span class="sxs-lookup"><span data-stu-id="ce37f-232">Caption: Hello.</span></span>

        <span data-ttu-id="ce37f-233">如果您立即以文字形式來查看 HelloModule，您會看到各種資源專屬的原始程式碼。</span><span class="sxs-lookup"><span data-stu-id="ce37f-233">If you view HelloModule.rc as text now, you will see various pieces of resource-specific source code.</span></span> <span data-ttu-id="ce37f-234">其中一個最重要的是描述 "Hello" 字串的區段：</span><span class="sxs-lookup"><span data-stu-id="ce37f-234">The one of greatest interest is the section that describes the "Hello" string:</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "Hello"
        END
        ```

        

        <span data-ttu-id="ce37f-235">這個 "Hello" 字串是需要當地語系化的資源 (也就是，轉譯) 為應用程式希望支援的所有語言。</span><span class="sxs-lookup"><span data-stu-id="ce37f-235">This "Hello" string is the resource that needs to be localized (that is, translated) into every language that the application hopes to support.</span></span> <span data-ttu-id="ce37f-236">例如， \_ \_ 您將在下一個步驟中建立的 project (中的 HelloModule ta) 將會包含其專屬的 HelloModule .rc 版本（適用于 "TA-in"）：</span><span class="sxs-lookup"><span data-stu-id="ce37f-236">For example, the HelloModule\_ta\_in project (which you will create in the next step) will contain its own localized version of HelloModule.rc for "ta-IN":</span></span>

        ```C++
        /////////////////////////////////////////////////////////////////////////////
        //
        // String Table
        //

        STRINGTABLE 
        BEGIN
            HELLO_MUI_STR_0         "வணக்கம்"
        END
        ```

        

    5.  <span data-ttu-id="ce37f-237">建立 HelloModule \_ en \_ us 專案，以確定沒有任何錯誤。</span><span class="sxs-lookup"><span data-stu-id="ce37f-237">Build the HelloModule\_en\_us project to be sure there are no errors.</span></span>

5.  <span data-ttu-id="ce37f-238">在 HelloMUI 方案中建立六個以上的專案 (或您想要的多個專案，) 為其他語言建立額外六個資源 Dll。</span><span class="sxs-lookup"><span data-stu-id="ce37f-238">Create six more projects in the HelloMUI solution (or as many of them as you wish) to create six more resource DLLs for additional languages.</span></span> <span data-ttu-id="ce37f-239">使用下表中的值：</span><span class="sxs-lookup"><span data-stu-id="ce37f-239">Use the values in this table:</span></span>

    | <span data-ttu-id="ce37f-240">專案名稱</span><span class="sxs-lookup"><span data-stu-id="ce37f-240">Project name</span></span>        | <span data-ttu-id="ce37f-241">.Rc 檔的名稱</span><span class="sxs-lookup"><span data-stu-id="ce37f-241">Name of .rc file</span></span> | <span data-ttu-id="ce37f-242">字串識別碼</span><span class="sxs-lookup"><span data-stu-id="ce37f-242">String ID</span></span>          | <span data-ttu-id="ce37f-243">字串值</span><span class="sxs-lookup"><span data-stu-id="ce37f-243">String value</span></span> | <span data-ttu-id="ce37f-244">字串標題</span><span class="sxs-lookup"><span data-stu-id="ce37f-244">String caption</span></span> |
    |---------------------|------------------|--------------------|--------------|----------------|
    | <span data-ttu-id="ce37f-245">HelloModule \_ de \_</span><span class="sxs-lookup"><span data-stu-id="ce37f-245">HelloModule\_de\_de</span></span> | <span data-ttu-id="ce37f-246">HelloModule</span><span class="sxs-lookup"><span data-stu-id="ce37f-246">HelloModule</span></span>      | <span data-ttu-id="ce37f-247">HELLO \_ MUI \_ STR \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce37f-247">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="ce37f-248">0</span><span class="sxs-lookup"><span data-stu-id="ce37f-248">0</span></span>            | <span data-ttu-id="ce37f-249">喂</span><span class="sxs-lookup"><span data-stu-id="ce37f-249">Hallo</span></span>          |
    | <span data-ttu-id="ce37f-250">HelloModule \_ es \_ es</span><span class="sxs-lookup"><span data-stu-id="ce37f-250">HelloModule\_es\_es</span></span> | <span data-ttu-id="ce37f-251">HelloModule</span><span class="sxs-lookup"><span data-stu-id="ce37f-251">HelloModule</span></span>      | <span data-ttu-id="ce37f-252">HELLO \_ MUI \_ STR \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce37f-252">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="ce37f-253">0</span><span class="sxs-lookup"><span data-stu-id="ce37f-253">0</span></span>            | <span data-ttu-id="ce37f-254">你好</span><span class="sxs-lookup"><span data-stu-id="ce37f-254">Hola</span></span>           |
    | <span data-ttu-id="ce37f-255">HelloModule \_ fr \_ fr</span><span class="sxs-lookup"><span data-stu-id="ce37f-255">HelloModule\_fr\_fr</span></span> | <span data-ttu-id="ce37f-256">HelloModule</span><span class="sxs-lookup"><span data-stu-id="ce37f-256">HelloModule</span></span>      | <span data-ttu-id="ce37f-257">HELLO \_ MUI \_ STR \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce37f-257">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="ce37f-258">0</span><span class="sxs-lookup"><span data-stu-id="ce37f-258">0</span></span>            | <span data-ttu-id="ce37f-259">你好</span><span class="sxs-lookup"><span data-stu-id="ce37f-259">Bonjour</span></span>        |
    | <span data-ttu-id="ce37f-260">HelloModule \_ 嗨 \_</span><span class="sxs-lookup"><span data-stu-id="ce37f-260">HelloModule\_hi\_in</span></span> | <span data-ttu-id="ce37f-261">HelloModule</span><span class="sxs-lookup"><span data-stu-id="ce37f-261">HelloModule</span></span>      | <span data-ttu-id="ce37f-262">HELLO \_ MUI \_ STR \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce37f-262">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="ce37f-263">0</span><span class="sxs-lookup"><span data-stu-id="ce37f-263">0</span></span>            | <span data-ttu-id="ce37f-264">नमस्</span><span class="sxs-lookup"><span data-stu-id="ce37f-264">नमस्</span></span>           |
    | <span data-ttu-id="ce37f-265">HelloModule \_ ru \_ ru</span><span class="sxs-lookup"><span data-stu-id="ce37f-265">HelloModule\_ru\_ru</span></span> | <span data-ttu-id="ce37f-266">HelloModule</span><span class="sxs-lookup"><span data-stu-id="ce37f-266">HelloModule</span></span>      | <span data-ttu-id="ce37f-267">HELLO \_ MUI \_ STR \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce37f-267">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="ce37f-268">0</span><span class="sxs-lookup"><span data-stu-id="ce37f-268">0</span></span>            | <span data-ttu-id="ce37f-269">Здравствуйте</span><span class="sxs-lookup"><span data-stu-id="ce37f-269">Здравствуйте</span></span>   |
    | <span data-ttu-id="ce37f-270">HelloModule \_ ta \_</span><span class="sxs-lookup"><span data-stu-id="ce37f-270">HelloModule\_ta\_in</span></span> | <span data-ttu-id="ce37f-271">HelloModule</span><span class="sxs-lookup"><span data-stu-id="ce37f-271">HelloModule</span></span>      | <span data-ttu-id="ce37f-272">HELLO \_ MUI \_ STR \_ 0</span><span class="sxs-lookup"><span data-stu-id="ce37f-272">HELLO\_MUI\_STR\_0</span></span> | <span data-ttu-id="ce37f-273">0</span><span class="sxs-lookup"><span data-stu-id="ce37f-273">0</span></span>            | <span data-ttu-id="ce37f-274">வணக்கம்</span><span class="sxs-lookup"><span data-stu-id="ce37f-274">வணக்கம்</span></span>        |

    

     

<span data-ttu-id="ce37f-275">如需 .rc 檔結構和語法的詳細資訊，請參閱 [關於資源檔](../menurc/about-resource-files.md)。</span><span class="sxs-lookup"><span data-stu-id="ce37f-275">For more about .rc file structure and syntax, see [About Resource Files](../menurc/about-resource-files.md).</span></span>

## <a name="step-2-building-the-basic-resource-module"></a><span data-ttu-id="ce37f-276">步驟2：建立基本資源模組</span><span class="sxs-lookup"><span data-stu-id="ce37f-276">Step 2: Building the Basic Resource Module</span></span>

<span data-ttu-id="ce37f-277">使用先前的資源模型，建立七個 HelloModule 專案中的任一個，會產生七個不同的 Dll。</span><span class="sxs-lookup"><span data-stu-id="ce37f-277">Using previous resource models, building any one of the seven HelloModule projects would result in seven separate DLLs.</span></span> <span data-ttu-id="ce37f-278">每個 DLL 都會包含一個資源區段，並將單一字串當地語系化成適當的語言。</span><span class="sxs-lookup"><span data-stu-id="ce37f-278">Each DLL would contain a resource section with a single string localized into the appropriate language.</span></span> <span data-ttu-id="ce37f-279">雖然適用于歷史的 Win32 資源模型，但這項設計不會利用 MUI。</span><span class="sxs-lookup"><span data-stu-id="ce37f-279">Although appropriate for the historic Win32 resource model, this design does not take advantage of MUI.</span></span>

<span data-ttu-id="ce37f-280">在 Windows Vista SDK 和更新版本中，MUI 提供將可執行檔分割為原始程式碼和可當地語系化內容模組的功能。</span><span class="sxs-lookup"><span data-stu-id="ce37f-280">In the Windows Vista SDK and later, MUI provides the ability to split executables into source code and localizable content modules.</span></span> <span data-ttu-id="ce37f-281">使用步驟5稍後所涵蓋的其他自訂，可以讓應用程式在 Windows Vista 之前的版本上執行多語言支援。</span><span class="sxs-lookup"><span data-stu-id="ce37f-281">With the additional customization that is covered later in Step 5, applications can be enabled for multi-lingual support to run on versions prior to Windows Vista.</span></span>

<span data-ttu-id="ce37f-282">從 Windows Vista 開始，可從可執行程式碼分割資源的主要機制如下：</span><span class="sxs-lookup"><span data-stu-id="ce37f-282">The primary mechanisms available to split resources from executable code, starting with Windows Vista, are:</span></span>

-   <span data-ttu-id="ce37f-283">使用 rc.exe (RC 編譯器) 的特定參數，或</span><span class="sxs-lookup"><span data-stu-id="ce37f-283">Using rc.exe (the RC Compiler) with specific switches, or</span></span>
-   <span data-ttu-id="ce37f-284">使用名為 muirct.exe 的建立後樣式分割工具。</span><span class="sxs-lookup"><span data-stu-id="ce37f-284">Using a post-build style splitting tool named muirct.exe.</span></span>

<span data-ttu-id="ce37f-285">如需詳細資訊，請參閱 [資源公用程式](resource-utilities.md) 。</span><span class="sxs-lookup"><span data-stu-id="ce37f-285">See [Resource Utilities](resource-utilities.md) for more information.</span></span>

<span data-ttu-id="ce37f-286">為了簡單起見，本教學課程會使用 muirct.exe 來分割 "Hello MUI" 可執行檔。</span><span class="sxs-lookup"><span data-stu-id="ce37f-286">For the sake of simplicity, this tutorial uses muirct.exe to split the "Hello MUI" executable.</span></span>

### <a name="splitting-the-various-language-resource-modules-an-overview"></a><span data-ttu-id="ce37f-287">分割各種語言資源模組：總覽</span><span class="sxs-lookup"><span data-stu-id="ce37f-287">Splitting the Various Language Resource Modules: An Overview</span></span>

<span data-ttu-id="ce37f-288">多部分進程牽涉到將 Dll 分割成一個可執行檔 HelloModule.dll，再加上此教學課程中支援的七種語言的 HelloModule.dll。</span><span class="sxs-lookup"><span data-stu-id="ce37f-288">A multi-part process is involved in splitting the DLLs into one executable HelloModule.dll, plus a HelloModule.dll.mui for each of the seven supported languages within this tutorial.</span></span> <span data-ttu-id="ce37f-289">本總覽說明所需的步驟;下一節會顯示執行這些步驟的命令檔。</span><span class="sxs-lookup"><span data-stu-id="ce37f-289">This overview describes the required steps; the next section presents a command file that performs those steps.</span></span>

<span data-ttu-id="ce37f-290">首先，使用下列命令來分割僅限英文的 HelloModule.dll 模組：</span><span class="sxs-lookup"><span data-stu-id="ce37f-290">First, split the English-only HelloModule.dll module by using the command:</span></span>


```C++
mkdir .\en-US
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
```



<span data-ttu-id="ce37f-291">上述命令列使用設定檔 DoReverseMuiLoc. rcconfig。</span><span class="sxs-lookup"><span data-stu-id="ce37f-291">The command line above uses the configuration file DoReverseMuiLoc.rcconfig.</span></span> <span data-ttu-id="ce37f-292">muirct.exe 通常會使用這種類型的設定檔來分割非語言相關 (LN) DLL 和與語言相關的 mui 檔案之間的資源。</span><span class="sxs-lookup"><span data-stu-id="ce37f-292">This type of configuration file is typically used by muirct.exe to split resources between the language-neutral (LN) DLL and the language-dependent .mui files.</span></span> <span data-ttu-id="ce37f-293">在此情況下，下一節中所列的 DoReverseMuiLoc. rcconfig (xml 檔案) 表示許多資源類型，但全都落在 "localizedResources" 或 mui 檔案類別中，而且沒有語言中立類別中的資源。</span><span class="sxs-lookup"><span data-stu-id="ce37f-293">In this case, the DoReverseMuiLoc.rcconfig xml file (listed in the next section) indicates many resource types, but they all fall into the "localizedResources" or .mui file category, and there are no resources in the language-neutral category.</span></span> <span data-ttu-id="ce37f-294">如需如何準備資源設定檔的詳細資訊，請參閱 [準備資源設定檔](preparing-a-resource-configuration-file.md)。</span><span class="sxs-lookup"><span data-stu-id="ce37f-294">For more information about how to prepare a resource configuration file, see [Preparing a Resource Configuration File](preparing-a-resource-configuration-file.md).</span></span>

<span data-ttu-id="ce37f-295">除了建立包含英文字串 "Hello" 的 HelloModule.dll mui 檔案，muirct.exe 也會在分割期間將 MUI 資源內嵌到 HelloModule.dll 模組。</span><span class="sxs-lookup"><span data-stu-id="ce37f-295">In addition to creating a HelloModule.dll.mui file which contains the English string "Hello", muirct.exe also embeds a MUI resource into the HelloModule.dll module during the splitting.</span></span> <span data-ttu-id="ce37f-296">為了在執行時間適當地從特定語言的 HelloModule.dll mui 模組載入適當的資源，每個 mui 檔案都必須修正其總和檢查碼，以符合基準語言中性之 LN 模組中的總和檢查碼。</span><span class="sxs-lookup"><span data-stu-id="ce37f-296">In order to properly load at run-time the appropriate resources from the language-specific HelloModule.dll.mui modules, each .mui file must have its checksums fixed-up to match the checksums in the baseline language-neutral LN module.</span></span> <span data-ttu-id="ce37f-297">這是透過下列命令來完成：</span><span class="sxs-lookup"><span data-stu-id="ce37f-297">This is done by a command such as:</span></span>


```C++
muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui
```



<span data-ttu-id="ce37f-298">同樣地，也會叫用 muirct.exe，為每個其他語言建立 HelloModule.dll 的 mui 檔。</span><span class="sxs-lookup"><span data-stu-id="ce37f-298">Similarly, muirct.exe is invoked to create a HelloModule.dll.mui file for each of the other languages.</span></span> <span data-ttu-id="ce37f-299">不過，在這些情況下，會捨棄非語言相關 DLL，因為只需要第一個建立的 DLL。</span><span class="sxs-lookup"><span data-stu-id="ce37f-299">However, in those cases the language-neutral DLL is discarded, as only the first one created will be needed.</span></span> <span data-ttu-id="ce37f-300">處理西班牙文和法文資源的命令看起來像這樣：</span><span class="sxs-lookup"><span data-stu-id="ce37f-300">The commands that process the Spanish and French resources look like this:</span></span>


```C++
mkdir .\es-ES
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

mkdir .\fr-FR
muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui
```



<span data-ttu-id="ce37f-301">上述 muirct.exe 命令列中最重要的一件事，就是使用-x 旗標來指定目標語言識別項。</span><span class="sxs-lookup"><span data-stu-id="ce37f-301">One of the most important things to notice in the muirct.exe command lines above is that the -x flag is used to specify a target language ID.</span></span> <span data-ttu-id="ce37f-302">針對每個語言特定的 HelloModule.dll 模組，提供給 muirct.exe 的值不同。</span><span class="sxs-lookup"><span data-stu-id="ce37f-302">The value provided to muirct.exe is different for each language-specific HelloModule.dll module.</span></span> <span data-ttu-id="ce37f-303">這個語言值是 central，可供 muirct.exe 在分割期間適當地標記 mui 檔。</span><span class="sxs-lookup"><span data-stu-id="ce37f-303">This language value is central and is used by muirct.exe to appropriately mark the .mui file during splitting.</span></span> <span data-ttu-id="ce37f-304">不正確的值會在執行時間為該特定的 mui 檔案產生資源載入失敗。</span><span class="sxs-lookup"><span data-stu-id="ce37f-304">An incorrect value produces resource loading failures for that particular .mui file at run-time.</span></span> <span data-ttu-id="ce37f-305">如需將語言名稱對應至 LCID 的詳細資訊，請參閱 [語言識別項常數和字串](language-identifier-constants-and-strings.md) 。</span><span class="sxs-lookup"><span data-stu-id="ce37f-305">See [Language Identifier Constants and Strings](language-identifier-constants-and-strings.md) for more details on mapping language name to LCID.</span></span>

<span data-ttu-id="ce37f-306">每個分割的 mui 檔案最後都會放置在與語言中立的 HelloModule.dll 所在的目錄之下，與其語言名稱相對應的目錄。</span><span class="sxs-lookup"><span data-stu-id="ce37f-306">Each split .mui file ends up being placed into a directory corresponding to its language name, immediately underneath the directory in which the language-neutral HelloModule.dll will reside.</span></span> <span data-ttu-id="ce37f-307">如需有關 mui 檔案放置的詳細資訊，請參閱 [應用程式部署](application-deployment.md)。</span><span class="sxs-lookup"><span data-stu-id="ce37f-307">For more about .mui file placement, see [Application Deployment](application-deployment.md).</span></span>

### <a name="splitting-the-various-language-resource-modules-creating-the-files"></a><span data-ttu-id="ce37f-308">分割不同的語言資源模組：建立檔案</span><span class="sxs-lookup"><span data-stu-id="ce37f-308">Splitting the Various Language Resource Modules: Creating the Files</span></span>

<span data-ttu-id="ce37f-309">在本教學課程中，您會建立一個命令檔，其中包含用來分割各種 Dll 的命令，而且您會以手動方式叫用它。</span><span class="sxs-lookup"><span data-stu-id="ce37f-309">For this tutorial you create a command file containing the commands to split the various DLLs, and you invoke it manually.</span></span> <span data-ttu-id="ce37f-310">請注意，在實際的開發工作中，您可以在 HelloMUI 方案中將這些命令納入預先建立或後置事件，以降低組建錯誤的可能性，但這已超出本教學課程的範圍。</span><span class="sxs-lookup"><span data-stu-id="ce37f-310">Note that in actual development work, you could reduce the potential for build errors by including these commands as pre-build or post-build events in the HelloMUI solution, but that is beyond the scope of this tutorial.</span></span>

<span data-ttu-id="ce37f-311">建立偵錯工具組建的檔案：</span><span class="sxs-lookup"><span data-stu-id="ce37f-311">Create the files for the debug build:</span></span>

1.  <span data-ttu-id="ce37f-312">建立包含下列命令的命令檔 DoReverseMuiLoc：</span><span class="sxs-lookup"><span data-stu-id="ce37f-312">Create a command file DoReverseMuiLoc.cmd containing the following commands:</span></span>
    ```C++
    mkdir .\en-US
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0409 -g 0x0407 .\HelloModule_en_us.dll .\HelloModule.dll .\en-US\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e en-US\HelloModule.dll.mui

    mkdir .\de-DE
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0407 -g 0x0407 .\HelloModule_de_de.dll .\HelloModule_discard.dll .\de-DE\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e de-DE\HelloModule.dll.mui

    mkdir .\es-ES
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0C0A -g 0x0407 .\HelloModule_es_es.dll .\HelloModule_discard.dll .\es-ES\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e es-ES\HelloModule.dll.mui

    mkdir .\fr-FR
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x040C -g 0x0407 .\HelloModule_fr_fr.dll .\HelloModule_discard.dll .\fr-FR\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e fr-FR\HelloModule.dll.mui

    mkdir .\hi-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0439 -g 0x0407 .\HelloModule_hi_in.dll .\HelloModule_discard.dll .\hi-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e hi-IN\HelloModule.dll.mui

    mkdir .\ru-RU
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0419 -g 0x0407 .\HelloModule_ru_ru.dll .\HelloModule_discard.dll .\ru-RU\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ru-RU\HelloModule.dll.mui

    mkdir .\ta-IN
    muirct.exe -q DoReverseMuiLoc.rcconfig -v 2 -x 0x0449 -g 0x0407 .\HelloModule_ta_in.dll .\HelloModule_discard.dll .\ta-IN\HelloModule.dll.mui
    muirct.exe -c HelloModule.dll -e ta-IN\HelloModule.dll.mui
    pause
    ```

    

2.  <span data-ttu-id="ce37f-313">建立包含下列幾行的 xml 檔案 DoReverseMuiLoc rcconfig：</span><span class="sxs-lookup"><span data-stu-id="ce37f-313">Create an xml file DoReverseMuiLoc.rcconfig containing the following lines:</span></span>
    ```C++
    <?xml version="1.0" encoding="utf-8"?>
        <localization>
            <resources>
                <win32Resources fileType="Application">
                    <neutralResources>
                    </neutralResources>
                    <localizedResources>
                        <resourceType typeNameId="#1"/>
                        <resourceType typeNameId="#10"/>
                        <resourceType typeNameId="#1024"/>
                        <resourceType typeNameId="#11"/>
                        <resourceType typeNameId="#12"/>
                        <resourceType typeNameId="#13"/>
                        <resourceType typeNameId="#14"/>
                        <resourceType typeNameId="#15"/>
                        <resourceType typeNameId="#16"/>
                        <resourceType typeNameId="#17"/>
                        <resourceType typeNameId="#18"/>
                        <resourceType typeNameId="#19"/>
                        <resourceType typeNameId="#2"/>
                        <resourceType typeNameId="#20"/>
                        <resourceType typeNameId="#2110"/>
                        <resourceType typeNameId="#23"/>
                        <resourceType typeNameId="#240"/>
                        <resourceType typeNameId="#3"/>
                        <resourceType typeNameId="#4"/>
                        <resourceType typeNameId="#5"/>
                        <resourceType typeNameId="#6"/>
                        <resourceType typeNameId="#7"/>
                        <resourceType typeNameId="#8"/>
                        <resourceType typeNameId="#9"/>
                        <resourceType typeNameId="HTML"/>
                        <resourceType typeNameId="MOFDATA"/>
                    </localizedResources>
                </win32Resources>
            </resources>
        </localization>
    ```

    

3.  <span data-ttu-id="ce37f-314">將 DoReverseMuiLoc 和 DoReverseMuiLoc 複製到 *ProjectRootDirectory* \\ HelloMUI \\ Debug。</span><span class="sxs-lookup"><span data-stu-id="ce37f-314">Copy DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig to *ProjectRootDirectory*\\HelloMUI\\Debug.</span></span>
4.  <span data-ttu-id="ce37f-315">開啟 Visual Studio 2008 命令提示字元，然後流覽至 Debug 目錄。</span><span class="sxs-lookup"><span data-stu-id="ce37f-315">Open the Visual Studio 2008 command prompt and navigate to the Debug directory.</span></span>
5.  <span data-ttu-id="ce37f-316">執行 DoReverseMuiLoc .cmd。</span><span class="sxs-lookup"><span data-stu-id="ce37f-316">Run DoReverseMuiLoc.cmd.</span></span>

<span data-ttu-id="ce37f-317">當您建立發行組建時，會將相同的 DoReverseMuiLoc 和 DoReverseMuiLoc. rcconfig 檔案複製到發行目錄，然後在該處執行命令檔。</span><span class="sxs-lookup"><span data-stu-id="ce37f-317">When you create a release build, you copy the same DoReverseMuiLoc.cmd and DoReverseMuiLoc.rcconfig files to the Release directory and run the command file there.</span></span>

## <a name="step-3-creating-a-resource-savvy-hello-mui"></a><span data-ttu-id="ce37f-318">步驟3：建立 Resource-Savvy "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="ce37f-318">Step 3: Creating a Resource-Savvy "Hello MUI"</span></span>

<span data-ttu-id="ce37f-319">根據上述的初始硬式編碼 GuiStep \_0.exe 範例，您可以選擇納入 Win32 資源模型，將應用程式的範圍延伸至多個語言使用者。</span><span class="sxs-lookup"><span data-stu-id="ce37f-319">Building on the initial hard-coded GuiStep\_0.exe example from above, you could extend the reach of the application to multiple language users by choosing to incorporate the Win32 resource model.</span></span> <span data-ttu-id="ce37f-320">此步驟中所提供的新執行時間程式碼包括模組載入 ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) 和字串抓取 ([**loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa)) 邏輯。</span><span class="sxs-lookup"><span data-stu-id="ce37f-320">The new run-time code presented in this step includes the module loading ([**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)) and string retrieval ([**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa)) logic.</span></span>

1.  <span data-ttu-id="ce37f-321">將新專案加入至 HelloMUI 方案 (使用功能表選取檔案、加入，以及使用下列設定和值的新專案) ：</span><span class="sxs-lookup"><span data-stu-id="ce37f-321">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="ce37f-322">專案類型： Win32 專案。</span><span class="sxs-lookup"><span data-stu-id="ce37f-322">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="ce37f-323">名稱： GuiStep \_ 1。</span><span class="sxs-lookup"><span data-stu-id="ce37f-323">Name: GuiStep\_1.</span></span>
    3.  <span data-ttu-id="ce37f-324">位置：接受預設值。</span><span class="sxs-lookup"><span data-stu-id="ce37f-324">Location: accept the default.</span></span>
    4.  <span data-ttu-id="ce37f-325">在 Win32 應用程式精靈中，選取預設的應用程式類型： Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-325">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="ce37f-326">將這個專案設定為從 Visual Studio 中執行，並設定其執行緒模型：</span><span class="sxs-lookup"><span data-stu-id="ce37f-326">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="ce37f-327">在方案總管中，以滑鼠右鍵按一下專案 GuiStep \_ 1，然後選取 [設定為啟始專案]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-327">In the Solution Explorer, right-click the project GuiStep\_1 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="ce37f-328">再以滑鼠右鍵按一下它，然後選取 [屬性]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-328">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="ce37f-329">在專案的 [屬性頁] 對話方塊中：</span><span class="sxs-lookup"><span data-stu-id="ce37f-329">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="ce37f-330">在左上方的下拉式清單中，將 [設定] 設定為 [所有設定]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-330">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="ce37f-331">在 [設定屬性] 下展開 [C/c + +]，選取 [程式碼產生]，並設定執行時間程式庫：多執行緒的 Debug () /MTd</span><span class="sxs-lookup"><span data-stu-id="ce37f-331">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="ce37f-332">將 GuiStep 1 .cpp 的內容取代為 \_ 下列程式碼：</span><span class="sxs-lookup"><span data-stu-id="ce37f-332">Replace the contents of GuiStep\_1.cpp with the following code:</span></span>
    ```C++
    // GuiStep_1.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_1.h"
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Basic application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 2. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 3. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 4. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }
    ```

    

4.  <span data-ttu-id="ce37f-333">建置並執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-333">Build and run the application.</span></span> <span data-ttu-id="ce37f-334">輸出將會以目前設定為電腦顯示語言的語言來顯示 (前提是這是我們建立) 的七種語言之一。</span><span class="sxs-lookup"><span data-stu-id="ce37f-334">The output will be displayed in the language currently set as the display language of the computer (provided it is one of the seven languages we have built).</span></span>

## <a name="step-4-globalizing-hello-mui"></a><span data-ttu-id="ce37f-335">步驟4：全球化「Hello MUI」</span><span class="sxs-lookup"><span data-stu-id="ce37f-335">Step 4: Globalizing "Hello MUI"</span></span>

<span data-ttu-id="ce37f-336">雖然先前的範例能夠以不同的語言顯示其輸出，但在許多方面都很短。</span><span class="sxs-lookup"><span data-stu-id="ce37f-336">Although the previous example is able to display its output in different languages, it falls short in a number of areas.</span></span> <span data-ttu-id="ce37f-337">最明顯的是，應用程式只在與 Windows 作業系統本身相較之下，只有一小部分的語言才能使用。</span><span class="sxs-lookup"><span data-stu-id="ce37f-337">Perhaps the most noticeable is that the application is only available in a small subset of languages when compared to the Windows operating system itself.</span></span> <span data-ttu-id="ce37f-338">例如，如果上一個 \_ 步驟中的 GuiStep 1 應用程式是安裝在日文版的 Windows 上，則可能會發生資源位置失敗。</span><span class="sxs-lookup"><span data-stu-id="ce37f-338">If, for example, the GuiStep\_1 application from the previous step were installed on a Japanese build of Windows, resource location failures would be likely.</span></span>

<span data-ttu-id="ce37f-339">若要解決這種情況，您有兩個主要選項：</span><span class="sxs-lookup"><span data-stu-id="ce37f-339">To address this situation, you have two primary options:</span></span>

-   <span data-ttu-id="ce37f-340">確定已包含預先決定的終極回溯語言中的資源。</span><span class="sxs-lookup"><span data-stu-id="ce37f-340">Ensure that resources in a predetermined ultimate fallback language are included.</span></span>
-   <span data-ttu-id="ce37f-341">提供一種方式，讓終端使用者從應用程式特別支援的語言子集設定其語言喜好設定。</span><span class="sxs-lookup"><span data-stu-id="ce37f-341">Provide a way for the end user to configure their language preferences from among the subset of languages specifically supported by the application.</span></span>

<span data-ttu-id="ce37f-342">在這些選項中，強烈建議使用提供終極回溯語言的方法，並藉由將-g 旗標傳遞給 muirct.exe （如上所示），在本教學課程中執行此動作。</span><span class="sxs-lookup"><span data-stu-id="ce37f-342">Of these options, the one providing an ultimate fallback language is highly advisable and is implemented in this tutorial by passing the -g flag to muirct.exe, as seen above.</span></span> <span data-ttu-id="ce37f-343">此旗標會指示 muirct.exe 將特定語言 (de/0x0407) 與語言中立的 dll 模組相關聯的最終回溯語言 (HelloModule.dll) 。</span><span class="sxs-lookup"><span data-stu-id="ce37f-343">This flag tells muirct.exe to make a specific language (de-DE / 0x0407) the ultimate fallback language associated with the language-neutral dll module (HelloModule.dll).</span></span> <span data-ttu-id="ce37f-344">在執行時間，此參數是用來產生要對使用者顯示之文字的最後手段。</span><span class="sxs-lookup"><span data-stu-id="ce37f-344">At run-time this parameter is used as a last resort to generate text to display to the user.</span></span> <span data-ttu-id="ce37f-345">如果找不到終極的回溯語言，而且語言中立的二進位檔中沒有適當的資源，載入資源將會失敗。</span><span class="sxs-lookup"><span data-stu-id="ce37f-345">In the event that an ultimate fallback language is not found and no appropriate resource is available in the language-neutral binary, loading of the resource fails.</span></span> <span data-ttu-id="ce37f-346">因此，您應該仔細判斷應用程式可能會遇到的案例，並據以規劃最終的回溯語言。</span><span class="sxs-lookup"><span data-stu-id="ce37f-346">Therefore you should carefully determine the scenarios that your application might encounter and plan the ultimate fallback language accordingly.</span></span>

<span data-ttu-id="ce37f-347">另一個可讓您根據此使用者定義階層進行可設定的語言喜好設定和載入資源的選項，可以大幅提升客戶滿意度。</span><span class="sxs-lookup"><span data-stu-id="ce37f-347">The other option of allowing for configurable language preferences and loading resources based on this user-defined hierarchy can greatly increase customer satisfaction.</span></span> <span data-ttu-id="ce37f-348">可惜的是，它也會使應用程式內所需的功能變得更複雜。</span><span class="sxs-lookup"><span data-stu-id="ce37f-348">Unfortunately, it also complicates the functionality needed within the application.</span></span>

<span data-ttu-id="ce37f-349">本教學課程的這個步驟使用簡化的文字檔機制來啟用自訂使用者語言設定。</span><span class="sxs-lookup"><span data-stu-id="ce37f-349">This step of the tutorial uses a simplified text file mechanism to enable custom user language configuration.</span></span> <span data-ttu-id="ce37f-350">應用程式會在執行時間剖析文字檔，並且使用剖析和驗證的語言清單來建立自訂的回溯清單。</span><span class="sxs-lookup"><span data-stu-id="ce37f-350">The text file is parsed at run-time by the application, and the parsed and validated language list is used in establishing a custom fallback list.</span></span> <span data-ttu-id="ce37f-351">建立自訂的回溯清單之後，Windows Api 會根據此清單中所述的語言優先順序來載入資源。</span><span class="sxs-lookup"><span data-stu-id="ce37f-351">After the custom fallback list is established, the Windows APIs will load resources according to the language precedence set forth in this list.</span></span> <span data-ttu-id="ce37f-352">程式碼的其餘部分類似于上一個步驟中找到的程式碼。</span><span class="sxs-lookup"><span data-stu-id="ce37f-352">The remainder of the code is similar to that found in the preceding step.</span></span>

1.  <span data-ttu-id="ce37f-353">將新專案加入至 HelloMUI 方案 (使用功能表選取檔案、加入，以及使用下列設定和值的新專案) ：</span><span class="sxs-lookup"><span data-stu-id="ce37f-353">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="ce37f-354">專案類型： Win32 專案。</span><span class="sxs-lookup"><span data-stu-id="ce37f-354">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="ce37f-355">名稱： GuiStep \_ 2。</span><span class="sxs-lookup"><span data-stu-id="ce37f-355">Name: GuiStep\_2.</span></span>
    3.  <span data-ttu-id="ce37f-356">位置：接受預設值。</span><span class="sxs-lookup"><span data-stu-id="ce37f-356">Location: accept the default.</span></span>
    4.  <span data-ttu-id="ce37f-357">在 Win32 應用程式精靈中，選取預設的應用程式類型： Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-357">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="ce37f-358">將這個專案設定為從 Visual Studio 中執行，並設定其執行緒模型：</span><span class="sxs-lookup"><span data-stu-id="ce37f-358">Set this project to run from within Visual Studio, and configure its threading model:</span></span>

    1.  <span data-ttu-id="ce37f-359">在方案總管中，以滑鼠右鍵按一下專案 GuiStep \_ 2，然後選取 [設定為啟始專案]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-359">In the Solution Explorer, right-click the project GuiStep\_2 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="ce37f-360">再以滑鼠右鍵按一下它，然後選取 [屬性]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-360">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="ce37f-361">在專案的 [屬性頁] 對話方塊中：</span><span class="sxs-lookup"><span data-stu-id="ce37f-361">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="ce37f-362">在左上方的下拉式清單中，將 [設定] 設定為 [所有設定]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-362">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="ce37f-363">在 [設定屬性] 下展開 [C/c + +]，選取 [程式碼產生]，並設定執行時間程式庫：多執行緒的 Debug () /MTd</span><span class="sxs-lookup"><span data-stu-id="ce37f-363">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>

3.  <span data-ttu-id="ce37f-364">以下列程式碼取代 GuiStep 2 的內容 \_ ：</span><span class="sxs-lookup"><span data-stu-id="ce37f-364">Replace the contents of GuiStep\_2.cpp with the following code:</span></span>
    ```C++
    // GuiStep_2.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_2.h"
    #include <strsafe.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now sets the appropriate fallback list
        DWORD langCount = 0;
        // next commented out line of code could be used on Windows 7 and later
        // using SetProcessPreferredUILanguages is recomended for new applications (esp. multi-threaded applications)
    //    if(!SetProcessPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        // the following line of code is supported on Windows Vista and later
        if(!SetThreadPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&langCount) || langCount == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to set the user defined languages, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // NOTES on step #1:
        // an application developer that makes the assumption the fallback list provided by the
        // system / OS is entirely sufficient may or may not be making a good assumption based 
        // mostly on:
        // A. your choice of languages installed with your application
        // B. the languages on the OS at application install time
        // C. the OS users propensity to install/uninstall language packs
        // D. the OS users propensity to change laguage settings

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module - use LoadLibraryEx
        // LoadLibraryEx is the preferred alternative for resource modules as used below because it
        // provides increased security and performance over that of LoadLibrary
        HMODULE resContainer = LoadLibraryExW(HELLO_MODULE_CONTRIVED_FILE_PATH,NULL,LOAD_LIBRARY_AS_IMAGE_RESOURCE | LOAD_LIBRARY_AS_DATAFILE);
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeLibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) && 
                    IsValidLocaleName(next))
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="ce37f-365">建立包含下列這一行的 Unicode 文字檔 langs.txt：</span><span class="sxs-lookup"><span data-stu-id="ce37f-365">Create a Unicode text file langs.txt containing the following line:</span></span>

    ``` syntax
    hi-IN ta-IN ru-RU fr-FR es-ES en-US
    ```

    > [!Note]  
    > <span data-ttu-id="ce37f-366">務必將檔案儲存為 Unicode。</span><span class="sxs-lookup"><span data-stu-id="ce37f-366">Be sure to save the file as Unicode.</span></span>

     

    <span data-ttu-id="ce37f-367">將 langs.txt 複製到程式執行所在的目錄：</span><span class="sxs-lookup"><span data-stu-id="ce37f-367">Copy langs.txt to the directory from which the program will run:</span></span>

    -   <span data-ttu-id="ce37f-368">如果從 Visual Studio 內執行，請將它複製到 *ProjectRootDirectory* \\ HelloMUI \\ GuiStep \_ 2。</span><span class="sxs-lookup"><span data-stu-id="ce37f-368">If running from within Visual Studio, copy it to *ProjectRootDirectory*\\HelloMUI\\GuiStep\_2.</span></span>
    -   <span data-ttu-id="ce37f-369">如果從 Windows 檔案總管執行，請將它複製到 GuiStep2.exe 的相同目錄中 \_ 。</span><span class="sxs-lookup"><span data-stu-id="ce37f-369">If running from Windows Explorer, copy it to the same directory as GuiStep\_2.exe.</span></span>

5.  <span data-ttu-id="ce37f-370">建置並執行專案。</span><span class="sxs-lookup"><span data-stu-id="ce37f-370">Build and run the project.</span></span> <span data-ttu-id="ce37f-371">嘗試編輯 langs.txt，讓不同的語言出現在清單前端。</span><span class="sxs-lookup"><span data-stu-id="ce37f-371">Try editing langs.txt so that different languages appear at the front of the list.</span></span>

## <a name="step-5-customizing-hello-mui"></a><span data-ttu-id="ce37f-372">步驟5：自訂 "Hello MUI"</span><span class="sxs-lookup"><span data-stu-id="ce37f-372">Step 5: Customizing "Hello MUI"</span></span>

<span data-ttu-id="ce37f-373">在本教學課程中，到目前為止提到的一些執行時間功能，僅適用于 Windows Vista 和更新版本。</span><span class="sxs-lookup"><span data-stu-id="ce37f-373">A number of the run-time features mentioned so far within this tutorial are available only on Windows Vista and later.</span></span> <span data-ttu-id="ce37f-374">您可以讓應用程式在舊版 Windows 作業系統版本（例如 Windows XP）上運作，以重複使用投資于當地語系化和分割資源的工作。</span><span class="sxs-lookup"><span data-stu-id="ce37f-374">You may wish to re-use the effort invested in localizing and splitting resources by making the application work on downlevel Windows operating system versions, such as Windows XP.</span></span> <span data-ttu-id="ce37f-375">此程式牽涉到調整上述兩個主要區域中的範例：</span><span class="sxs-lookup"><span data-stu-id="ce37f-375">This process involves adjusting the previous example in two key areas:</span></span>

-   <span data-ttu-id="ce37f-376">Windows Vista 之前的資源載入函式 (例如 [**loadstring 時**](/windows/win32/api/winuser/nf-winuser-loadstringa)、 [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona)、 [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa)、 [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage)和其他) 為非 MUI 感知的功能。</span><span class="sxs-lookup"><span data-stu-id="ce37f-376">The pre-Windows Vista resource loading functions (such as [**LoadString**](/windows/win32/api/winuser/nf-winuser-loadstringa), [**LoadIcon**](/windows/win32/api/winuser/nf-winuser-loadicona), [**LoadBitmap**](/windows/win32/api/winuser/nf-winuser-loadbitmapa), [**FormatMessage**](/windows/win32/api/winbase/nf-winbase-formatmessage), and others) are non-MUI aware.</span></span> <span data-ttu-id="ce37f-377">分割資源 (LN 和 mui 檔中隨附的應用程式) 必須使用下列兩個函式的其中一個來載入資源模組：</span><span class="sxs-lookup"><span data-stu-id="ce37f-377">Applications that ship with split resources (LN and .mui files) must load resource modules using one of these two functions:</span></span>

    -   <span data-ttu-id="ce37f-378">如果應用程式只在 Windows Vista 和更新版本上執行，則應該使用 [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa)載入資源模組。</span><span class="sxs-lookup"><span data-stu-id="ce37f-378">If the application is to be run only on Windows Vista and later, it should load resource modules with [**LoadLibraryEx**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibraryexa).</span></span>
    -   <span data-ttu-id="ce37f-379">如果應用程式是在 Windows Vista 之前的版本，以及 Windows Vista 或更新版本上執行，則必須使用 [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya)，這是 WINDOWS 7 SDK 中提供的特定舊版功能。</span><span class="sxs-lookup"><span data-stu-id="ce37f-379">If the application is to be run on versions prior to Windows Vista, as well as Windows Vista or later, it must use [**LoadMUILibrary**](/windows/desktop/api/Muiload/nf-muiload-loadmuilibrarya), which is a specific downlevel function provided in the Windows 7 SDK.</span></span>

-   <span data-ttu-id="ce37f-380">在 windows vista 之前版本的 Windows 作業系統中，提供的語言管理和語言回溯順序支援與 Windows Vista 和更新版本中的功能有很大的差異。</span><span class="sxs-lookup"><span data-stu-id="ce37f-380">The language management and language fallback order support offered in pre-Windows Vista versions of the Windows operating system differs significantly from that in Windows Vista and later.</span></span> <span data-ttu-id="ce37f-381">基於這個理由，允許使用者設定之語言回復的應用程式必須調整其語言管理作法：</span><span class="sxs-lookup"><span data-stu-id="ce37f-381">For this reason, applications that allow user-configured language fallback must adjust their language management practices:</span></span>

    -   <span data-ttu-id="ce37f-382">如果應用程式只在 Windows Vista 和更新版本上執行，使用 [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) 設定語言清單就已足夠。</span><span class="sxs-lookup"><span data-stu-id="ce37f-382">If the application is to be run only on Windows Vista and later, setting the language list using [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) is sufficient.</span></span>
    -   <span data-ttu-id="ce37f-383">如果應用程式要在所有 Windows 版本上執行，則必須將程式碼結構化，以在舊版平臺上執行，以逐一查看使用者設定的語言清單，並探查所需的資源模組。</span><span class="sxs-lookup"><span data-stu-id="ce37f-383">If the application is to be run on all Windows versions, code must be constructed that will run on downlevel platforms to iterate through the user configured language list and probe for the desired resource module.</span></span> <span data-ttu-id="ce37f-384">這可以在此步驟稍後提供的第1c 節和第2節中看到。</span><span class="sxs-lookup"><span data-stu-id="ce37f-384">This can be seen in sections 1c and 2 of the code provided later in this step.</span></span>

<span data-ttu-id="ce37f-385">建立可在任何版本的 Windows 上使用當地語系化資源模組的專案：</span><span class="sxs-lookup"><span data-stu-id="ce37f-385">Create a project that can use the localized resource modules on any version of Windows:</span></span>

1.  <span data-ttu-id="ce37f-386">將新專案加入至 HelloMUI 方案 (使用功能表選取檔案、加入，以及使用下列設定和值的新專案) ：</span><span class="sxs-lookup"><span data-stu-id="ce37f-386">Add a new project to the HelloMUI solution (using the menu selection File, Add, and New Project) with the following settings and values:</span></span>

    1.  <span data-ttu-id="ce37f-387">專案類型： Win32 專案。</span><span class="sxs-lookup"><span data-stu-id="ce37f-387">Project type: Win32 Project.</span></span>
    2.  <span data-ttu-id="ce37f-388">名稱： GuiStep \_ 3。</span><span class="sxs-lookup"><span data-stu-id="ce37f-388">Name: GuiStep\_3.</span></span>
    3.  <span data-ttu-id="ce37f-389">位置：接受預設值。</span><span class="sxs-lookup"><span data-stu-id="ce37f-389">Location: accept the default.</span></span>
    4.  <span data-ttu-id="ce37f-390">在 Win32 應用程式精靈中，選取預設的應用程式類型： Windows 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-390">In the Win32 Application Wizard, select the default Application type: Windows application.</span></span>

2.  <span data-ttu-id="ce37f-391">將這個專案設定為從 Visual Studio 中執行，並設定其執行緒模型。</span><span class="sxs-lookup"><span data-stu-id="ce37f-391">Set this project to run from within Visual Studio, and configure its threading model.</span></span> <span data-ttu-id="ce37f-392">此外，請將它設定為新增必要的標頭和程式庫。</span><span class="sxs-lookup"><span data-stu-id="ce37f-392">Also, configure it to add the necessary headers and libraries.</span></span>

    > [!Note]  
    > <span data-ttu-id="ce37f-393">本教學課程中使用的路徑假設 Windows 7 SDK 和 Microsoft NLS 下層 Api 封裝已安裝在其預設目錄中。</span><span class="sxs-lookup"><span data-stu-id="ce37f-393">The paths used in this tutorial assume that the Windows 7 SDK and the Microsoft NLS downlevel APIs package were installed to their default directories.</span></span> <span data-ttu-id="ce37f-394">如果不是這種情況，請適當地修改路徑。</span><span class="sxs-lookup"><span data-stu-id="ce37f-394">If that is not the case, modify the paths appropriately.</span></span>

     

    1.  <span data-ttu-id="ce37f-395">在方案總管中，以滑鼠右鍵按一下專案 GuiStep \_ 3，然後選取 [設定為啟始專案]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-395">In the Solution Explorer, right-click the project GuiStep\_3 and select Set as StartUp Project.</span></span>
    2.  <span data-ttu-id="ce37f-396">再以滑鼠右鍵按一下它，然後選取 [屬性]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-396">Right-click it again and select Properties.</span></span>
    3.  <span data-ttu-id="ce37f-397">在專案的 [屬性頁] 對話方塊中：</span><span class="sxs-lookup"><span data-stu-id="ce37f-397">In the project's Property Pages dialog box:</span></span>

        1.  <span data-ttu-id="ce37f-398">在左上方的下拉式清單中，將 [設定] 設定為 [所有設定]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-398">In the top left drop-down, set Configuration to All Configurations.</span></span>
        2.  <span data-ttu-id="ce37f-399">在 [設定屬性] 下展開 [C/c + +]，選取 [程式碼產生]，並設定執行時間程式庫：多執行緒的 Debug () /MTd</span><span class="sxs-lookup"><span data-stu-id="ce37f-399">Under Configuration Properties expand C/C++, select Code Generation, and set Runtime Library: Multi-threaded Debug (/MTd).</span></span>
        3.  <span data-ttu-id="ce37f-400">選取 [一般]，並新增至其他 Include 目錄：</span><span class="sxs-lookup"><span data-stu-id="ce37f-400">Select General and add to Additional Include Directories:</span></span>

            -   <span data-ttu-id="ce37f-401">"C： \\ MICROSOFT NLS 下層 api \\ 包含"。</span><span class="sxs-lookup"><span data-stu-id="ce37f-401">"C:\\Microsoft NLS Downlevel APIs\\Include".</span></span>

        4.  <span data-ttu-id="ce37f-402">選取 Language 並將 wchar \_ t 視為內建類型： No (/zc： wchar \_ t-) 。</span><span class="sxs-lookup"><span data-stu-id="ce37f-402">Select Language and set Treat wchar\_t as Built-in Type: No (/Zc:wchar\_t-).</span></span>
        5.  <span data-ttu-id="ce37f-403">選取 Advanced 和 set 呼叫慣例： \_ stdcall (/Gz) 。</span><span class="sxs-lookup"><span data-stu-id="ce37f-403">Select Advanced and set Calling Convention: \_stdcall (/Gz).</span></span>
        6.  <span data-ttu-id="ce37f-404">在 [設定屬性] 下展開 [連結器]，選取 [輸入]，然後新增至其他相依性</span><span class="sxs-lookup"><span data-stu-id="ce37f-404">Under Configuration Properties expand Linker, select Input, and add to Additional Dependencies:</span></span>

            -   <span data-ttu-id="ce37f-405">"C： \\ Program Files \\ Microsoft sdk \\ Windows \\ v 7.0 \\ lib \\ MUILoad .lib"。</span><span class="sxs-lookup"><span data-stu-id="ce37f-405">"C:\\Program Files\\Microsoft SDKs\\Windows\\v7.0\\Lib\\MUILoad.lib".</span></span>
            -   <span data-ttu-id="ce37f-406">"C： \\ MICROSOFT NLS 下層 api \\ Lib \\ x86 \\ Nlsdl .lib"。</span><span class="sxs-lookup"><span data-stu-id="ce37f-406">"C:\\Microsoft NLS Downlevel APIs\\Lib\\x86\\Nlsdl.lib".</span></span>

3.  <span data-ttu-id="ce37f-407">以下列程式碼取代 GuiStep 3 的內容 \_ ：</span><span class="sxs-lookup"><span data-stu-id="ce37f-407">Replace the contents of GuiStep\_3.cpp with the following code:</span></span>
    ```C++
    // GuiStep_3.cpp : Defines the entry point for the application.
    //

    #include "stdafx.h"
    #include "GuiStep_3.h"
    #include <strsafe.h>
    #include <Nlsdl.h>
    #include <MUILoad.h>
    #include "..\HelloModule_en_us\resource.h"

    #define SUFFICIENTLY_LARGE_STRING_BUFFER (MAX_PATH*2)
    #define USER_CONFIGURATION_STRING_BUFFER (((LOCALE_NAME_MAX_LENGTH+1)*5)+1)
    #define SUFFICIENTLY_LARGE_ERROR_BUFFER (1024*2)
    #define HELLO_MODULE_CONTRIVED_FILE_PATH  (L"HelloModule.dll")

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize);
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize);

    int WINAPI WinMain(HINSTANCE hInstance, HINSTANCE hPrevInstance, LPSTR lpCmdLine, int nCmdShow)
    {
        UNREFERENCED_PARAMETER(hInstance);
        UNREFERENCED_PARAMETER(hPrevInstance);
        UNREFERENCED_PARAMETER(lpCmdLine);
        UNREFERENCED_PARAMETER(nCmdShow);

        // The following code presents a hypothetical, yet common use pattern of MUI technology
        WCHAR displayBuffer[SUFFICIENTLY_LARGE_ERROR_BUFFER];

        // 1. Application starts by applying any user defined language preferences
        // (language setting is potentially optional for an application that wishes to strictly use OS system language fallback)
        // 1a. Application looks in pre-defined location for user preferences (registry, file, web, etc.)
        WCHAR userLanguagesString[USER_CONFIGURATION_STRING_BUFFER*2];
        if(!GetMyUserDefinedLanguages(userLanguagesString,USER_CONFIGURATION_STRING_BUFFER*2))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to find the user defined language configuration, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1b. Application converts the user defined 'readable' languages to the proper multi-string 'less readable' language name format
        WCHAR userLanguagesMultiString[USER_CONFIGURATION_STRING_BUFFER];
        if(!ConvertMyLangStrToMultiLangStr(userLanguagesString,userLanguagesMultiString,USER_CONFIGURATION_STRING_BUFFER))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to convert the user defined language configuration to multi-string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }
        // 1c. Application now attempts to set the fallback list - this is much different for a down-level 
        // shipping application when compared to a Windows Vista or Windows 7 only shipping application    
        BOOL setSuccess = FALSE;
        DWORD setLangCount = 0;
        HMODULE hDLL = GetModuleHandleW(L"kernel32.dll");
        if( hDLL )
        {
            typedef BOOL (* SET_PREFERRED_UI_LANGUAGES_PROTOTYPE ) ( DWORD, PCWSTR, PULONG );
            SET_PREFERRED_UI_LANGUAGES_PROTOTYPE fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE)NULL;
            fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetProcessPreferredUILanguages");
            if( fp_SetPreferredUILanguages )
            {
                // call SetProcessPreferredUILanguages if it is available in Kernel32.dll's export table - Windows 7 and later
                setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
            else
            {
                fp_SetPreferredUILanguages = (SET_PREFERRED_UI_LANGUAGES_PROTOTYPE) GetProcAddress(hDLL,"SetThreadPreferredUILanguages");
                // call SetThreadPreferredUILanguages if it is available in Kernel32.dll's export table - Windows Vista and later
                if(fp_SetPreferredUILanguages)
                    setSuccess = fp_SetPreferredUILanguages(MUI_LANGUAGE_NAME,userLanguagesMultiString,&setLangCount);
            }
        }

        // 2. Application obtains access to the proper resource container 
        // for standard Win32 resource loading this is normally a PE module
        // LoadMUILibrary is the preferred alternative for loading of resource modules
        // when the application is potentially run on OS versions prior to Windows Vista
        // LoadMUILibrary is available via Windows SDK releases in Windows Vista and later
        // When available, it is advised to get the most up-to-date Windows SDK (e.g., Windows 7)
        HMODULE resContainer = NULL;
        if(setSuccess) // Windows Vista and later OS scenario
        {
            resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        else // this block should only be hit on Windows XP and earlier OS platforms as setSuccess will be TRUE on Windows Vista and later
        {
            // need to provide your own fallback mechanism such as the implementation below
            // in essence the application will iterate through the user configured language list
            WCHAR * next = userLanguagesMultiString;
            while(!resContainer && *next != L'\0')
            {
                // convert the language name to an appropriate LCID
                // DownlevelLocaleNameToLCID is available via standalone download package 
                // and is contained in Nlsdl.h / Nlsdl.lib
                LCID nextLcid = DownlevelLocaleNameToLCID(next,DOWNLEVEL_LOCALE_NAME);
                // then have LoadMUILibrary attempt to probe for the right .mui module
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,(LANGID)nextLcid);
                // increment to the next language name in our list
                size_t nextStrLen = 0;
                if(SUCCEEDED(StringCchLengthW(next,LOCALE_NAME_MAX_LENGTH,&nextStrLen)))
                    next += (nextStrLen + 1);
                else
                    break; // string is invalid - need to exit
            }
            // if the user configured list did not locate a module then try the languages associated with the system
            if(!resContainer)
                resContainer = LoadMUILibraryW(HELLO_MODULE_CONTRIVED_FILE_PATH,MUI_LANGUAGE_NAME,0);
        }
        if(!resContainer)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource container module, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        // 3. Application parses the resource container to find the appropriate item
        WCHAR szHello[SUFFICIENTLY_LARGE_STRING_BUFFER];
        if(LoadStringW(resContainer,HELLO_MUI_STR_0,szHello,SUFFICIENTLY_LARGE_STRING_BUFFER) == 0)
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to load the resource string, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            FreeLibrary(resContainer);
            return 1; // exit
        }

        // 4. Application presents the discovered resource to the user via UI
        swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"%s MUI",szHello);
        MessageBoxW(NULL,displayBuffer,L"HelloMUI",MB_OK | MB_ICONINFORMATION);

        // 5. Application cleans up memory associated with the resource container after this item is no longer needed.
        if(!FreeMUILibrary(resContainer))
        {
            swprintf_s(displayBuffer,SUFFICIENTLY_LARGE_ERROR_BUFFER,L"FAILURE: Unable to unload the resource container, last error = %d.",GetLastError());
            MessageBoxW(NULL,displayBuffer,L"HelloMUI ERROR!",MB_OK | MB_ICONERROR);
            return 1; // exit
        }

        return 0;
    }

    BOOL GetMyUserDefinedLanguages(WCHAR * langStr, DWORD langStrSize)
    {
        BOOL rtnVal = FALSE;
        // very simple implementation - assumes that first 'langStrSize' characters of the 
        // L".\\langs.txt" file comprises a string of one or more languages
        HANDLE langConfigFileHandle = CreateFileW(L".\\langs.txt", GENERIC_READ, 0, 
            NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
        if(langConfigFileHandle != INVALID_HANDLE_VALUE)
        {
            // clear out the input variables
            DWORD bytesActuallyRead = 0;
            if(ReadFile(langConfigFileHandle,langStr,langStrSize*sizeof(WCHAR),&bytesActuallyRead,NULL) && bytesActuallyRead > 0)
            {
                rtnVal = TRUE;
                DWORD nullIndex = (bytesActuallyRead/sizeof(WCHAR) < langStrSize) ? bytesActuallyRead/sizeof(WCHAR) : langStrSize;
                langStr[nullIndex] = L'\0';
            }
            CloseHandle(langConfigFileHandle);
        }
        return rtnVal;
    }
    BOOL ConvertMyLangStrToMultiLangStr(WCHAR * langStr, WCHAR * langMultiStr, DWORD langMultiStrSize)
    {
        BOOL rtnVal = FALSE;
        size_t strLen = 0;
        rtnVal = SUCCEEDED(StringCchLengthW(langStr,USER_CONFIGURATION_STRING_BUFFER*2,&strLen));
        if(rtnVal && strLen > 0 && langMultiStr && langMultiStrSize > 0)
        {
            WCHAR * langMultiStrPtr = langMultiStr;
            WCHAR * last = langStr + (langStr[0] == 0xFEFF ? 1 : 0);
            WCHAR * context = last;
            WCHAR * next = wcstok_s(last,L",; :",&context);
            while(next && rtnVal)
            {
                // make sure you validate the user input
                if(SUCCEEDED(StringCchLengthW(last,LOCALE_NAME_MAX_LENGTH,&strLen)) 
                    && DownlevelLocaleNameToLCID(next,0) != 0)
                {
                    langMultiStrPtr[0] = L'\0';
                    rtnVal &= SUCCEEDED(StringCchCatW(langMultiStrPtr,(langMultiStrSize - (langMultiStrPtr - langMultiStr)),next));
                    langMultiStrPtr += strLen + 1;
                }
                next = wcstok_s(NULL,L",; :",&context);
                if(next)
                    last = next;
            }
            if(rtnVal && (langMultiStrSize - (langMultiStrPtr - langMultiStr))) // make sure there is a double null term for the multi-string 
            {
                langMultiStrPtr[0] = L'\0';
            }
            else // fail and guard anyone whom might use the multi-string
            {
                langMultiStr[0] = L'\0';
                langMultiStr[1] = L'\0';
            }
        }
        return rtnVal;
    }
    ```

    

4.  <span data-ttu-id="ce37f-408">將 langs.txt 建立或複製到適當的目錄，如先前 [步驟4：全球化 "HELLO MUI"](#step-4-globalizing-hello-mui)所述。</span><span class="sxs-lookup"><span data-stu-id="ce37f-408">Create or copy langs.txt to the appropriate directory, as previously described in [Step 4: Globalizing "Hello MUI"](#step-4-globalizing-hello-mui).</span></span>
5.  <span data-ttu-id="ce37f-409">建置並執行專案。</span><span class="sxs-lookup"><span data-stu-id="ce37f-409">Build and run the project.</span></span>

> [!Note]  
> <span data-ttu-id="ce37f-410">如果應用程式應該在 windows Vista 之前的 Windows 版本上執行，請務必閱讀 [MICROSOFT NLS 下層 api](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) 套件隨附的檔，以瞭解如何轉散發 Nlsdl.dll。</span><span class="sxs-lookup"><span data-stu-id="ce37f-410">If the application should run on Windows versions prior to Windows Vista, be sure to read the documents that came with the [Microsoft NLS downlevel APIs](https://www.microsoft.com/downloads/details.aspx?FamilyID=eb72cda0-834e-4c35-9419-ff14bc349c9d&amp;DisplayLang=en) package on how to redistribute Nlsdl.dll.</span></span>

 

## <a name="additional-considerations-for-mui"></a><span data-ttu-id="ce37f-411">MUI 的其他考慮</span><span class="sxs-lookup"><span data-stu-id="ce37f-411">Additional Considerations for MUI</span></span>

### <a name="support-for-console-applications"></a><span data-ttu-id="ce37f-412">主控台應用程式的支援</span><span class="sxs-lookup"><span data-stu-id="ce37f-412">Support for Console Applications</span></span>

<span data-ttu-id="ce37f-413">本教學課程中所涵蓋的技巧也可以用於主控台應用程式。</span><span class="sxs-lookup"><span data-stu-id="ce37f-413">The techniques covered in this tutorial can also be used in console applications.</span></span> <span data-ttu-id="ce37f-414">但是，與大部分的標準 GUI 控制項不同的是，Windows 命令視窗無法顯示所有語言的字元。</span><span class="sxs-lookup"><span data-stu-id="ce37f-414">However, unlike most standard GUI controls, the Windows command window cannot display characters for all languages.</span></span> <span data-ttu-id="ce37f-415">基於這個理由，多語系主控台應用程式需要特別注意。</span><span class="sxs-lookup"><span data-stu-id="ce37f-415">For this reason, multilingual console applications require special attention.</span></span>

<span data-ttu-id="ce37f-416">使用特定篩選旗標呼叫 Api [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) 或 [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) ，會導致資源載入函式移除在命令視窗中通常不會顯示的特定語言的語言資源探查。</span><span class="sxs-lookup"><span data-stu-id="ce37f-416">Calling the APIs [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) or [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages) with specific filtering flags causes the resource loading functions to remove language resource probes for specific languages that are not normally displayed within a command window.</span></span> <span data-ttu-id="ce37f-417">設定這些旗標之後，語言設定演算法只允許在 [命令] 視窗中正確顯示的語言為 [回復清單]。</span><span class="sxs-lookup"><span data-stu-id="ce37f-417">When these flags are set, the language-setting algorithms allow only those languages that will display properly in the command window to be on the fallback list.</span></span>

<span data-ttu-id="ce37f-418">如需有關使用這些 Api 建立多語系主控台應用程式的詳細資訊，請參閱 [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) 和 [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages)的備註章節。</span><span class="sxs-lookup"><span data-stu-id="ce37f-418">For more information on using these APIs to build a multilingual console application, see the remarks sections of [**SetThreadUILanguage**](/windows/desktop/api/Winnls/nf-winnls-setthreaduilanguage) and [**SetThreadPreferredUILanguages**](/windows/desktop/api/Winnls/nf-winnls-setthreadpreferreduilanguages).</span></span>

### <a name="determination-of-languages-to-support-at-run-time"></a><span data-ttu-id="ce37f-419">在 Run-Time 上判斷支援的語言</span><span class="sxs-lookup"><span data-stu-id="ce37f-419">Determination of Languages to Support at Run-Time</span></span>

<span data-ttu-id="ce37f-420">您可以採用下列其中一個設計建議，判斷您的應用程式在執行時間應該支援的語言：</span><span class="sxs-lookup"><span data-stu-id="ce37f-420">You can adopt one of the following design suggestions to determine which languages your application should support at run-time:</span></span>

-   <span data-ttu-id="ce37f-421">**在安裝期間，讓終端使用者從支援的語言清單中選取慣用語言**</span><span class="sxs-lookup"><span data-stu-id="ce37f-421">**During installation, enable the end user to select the preferred language from a list of supported languages**</span></span>

-   <span data-ttu-id="ce37f-422">**從設定檔讀取語言清單**</span><span class="sxs-lookup"><span data-stu-id="ce37f-422">**Read a language list from a configuration file**</span></span>

    <span data-ttu-id="ce37f-423">本教學課程中的部分專案包含用來剖析 langs.txt 設定檔的函式，其中包含語言清單。</span><span class="sxs-lookup"><span data-stu-id="ce37f-423">Some of the projects in this tutorial contain a function used to parse a langs.txt configuration file, which contains a language list.</span></span>

    <span data-ttu-id="ce37f-424">因為此函式會接受外部輸入，所以請驗證提供作為輸入的語言。</span><span class="sxs-lookup"><span data-stu-id="ce37f-424">Because this function takes external input, validate the languages that are provided as input.</span></span> <span data-ttu-id="ce37f-425">如需執行該驗證的詳細資訊，請參閱 [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) 或 [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="ce37f-425">See the [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) or [**DownLevelLocaleNameToLCID**](downlevellocalenametolcid.md) functions for more details on performing that validation.</span></span>

-   <span data-ttu-id="ce37f-426">**查詢作業系統以判斷已安裝的語言**</span><span class="sxs-lookup"><span data-stu-id="ce37f-426">**Query the operating system to determine which languages are installed**</span></span>

    <span data-ttu-id="ce37f-427">這種方法可協助應用程式使用與作業系統相同的語言。</span><span class="sxs-lookup"><span data-stu-id="ce37f-427">This approach helps the application use the same language as the operating system.</span></span> <span data-ttu-id="ce37f-428">雖然這不需要使用者提示，但如果您選擇此選項，請留意作業系統語言可以隨時新增或移除，而且可以在使用者安裝應用程式之後變更。</span><span class="sxs-lookup"><span data-stu-id="ce37f-428">Although this does not require user prompting, if you choose this option, be aware that operating system languages can be added or removed at any time and can change after the user installs the application.</span></span> <span data-ttu-id="ce37f-429">此外，請注意，在某些情況下，作業系統會以有限的語言支援進行安裝，而如果支援作業系統不支援的語言，則應用程式會提供更多的價值。</span><span class="sxs-lookup"><span data-stu-id="ce37f-429">Also, be aware that in some cases, the operating system is installed with limited language support, and the application offers more value if it supports languages that the operating system does not support.</span></span>

    <span data-ttu-id="ce37f-430">如需如何判斷作業系統中目前已安裝之語言的詳細資訊，請參閱 [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) 函數。</span><span class="sxs-lookup"><span data-stu-id="ce37f-430">For more information on how to determine the currently installed languages in the operating system, see the [**EnumUILanguages**](/windows/desktop/api/Winnls/nf-winnls-enumuilanguagesa) function.</span></span>

### <a name="complex-script-support-in-versions-prior-to-windows-vista"></a><span data-ttu-id="ce37f-431">Windows Vista 之前版本中的複雜字集支援</span><span class="sxs-lookup"><span data-stu-id="ce37f-431">Complex Script Support in Versions Prior to Windows Vista</span></span>

<span data-ttu-id="ce37f-432">當支援特定複雜字集的應用程式在 Windows Vista 之前的 Windows 版本上執行時，該腳本中的文字可能無法在 GUI 元件中正確顯示。</span><span class="sxs-lookup"><span data-stu-id="ce37f-432">When an application that supports certain complex scripts runs on a version of Windows prior to Windows Vista, text in that script may not display properly in GUI components.</span></span> <span data-ttu-id="ce37f-433">例如，在本教學課程中的舊版專案中，如果處理複雜字集和缺少相關字型的問題，則不會在訊息方塊中顯示 hi 和 ta 腳本。</span><span class="sxs-lookup"><span data-stu-id="ce37f-433">For example, in the downlevel project within this tutorial, hi-IN and ta-IN scripts may not display in the message box due to issues with processing complex scripts and the lack of related fonts.</span></span> <span data-ttu-id="ce37f-434">一般來說，這個本質的問題會以 GUI 元件的方塊呈現。</span><span class="sxs-lookup"><span data-stu-id="ce37f-434">Normally, problems of this nature present themselves as square boxes in the GUI component.</span></span>

<span data-ttu-id="ce37f-435">如需如何啟用複雜字集處理的詳細資訊，請參閱 [Windows 中的腳本和字型支援](https://msdn.microsoft.com/goglobal/bb688099.aspx)。</span><span class="sxs-lookup"><span data-stu-id="ce37f-435">More information about how to enable complex script processing can be found at [Script and Font Support in Windows](https://msdn.microsoft.com/goglobal/bb688099.aspx).</span></span>

## <a name="summary"></a><span data-ttu-id="ce37f-436">總結</span><span class="sxs-lookup"><span data-stu-id="ce37f-436">Summary</span></span>

<span data-ttu-id="ce37f-437">本教學課程全球化單一語言應用程式，並示範下列最佳做法。</span><span class="sxs-lookup"><span data-stu-id="ce37f-437">This tutorial globalized a monolingual application and demonstrated the following best practices.</span></span>

-   <span data-ttu-id="ce37f-438">設計應用程式以利用 Win32 資源模型。</span><span class="sxs-lookup"><span data-stu-id="ce37f-438">Design the application to take advantage of the Win32 resource model.</span></span>
-   <span data-ttu-id="ce37f-439">使用 MUI 將資源分割成 ( mui 檔) 的附屬二進位檔。</span><span class="sxs-lookup"><span data-stu-id="ce37f-439">Utilize MUI splitting of resources into satellite binaries (.mui files).</span></span>
-   <span data-ttu-id="ce37f-440">請確定當地語系化程式會更新 mui 檔案中的資源，以適用于目的語言。</span><span class="sxs-lookup"><span data-stu-id="ce37f-440">Ensure that the localization process updates the resources in the .mui files to be appropriate for the target language.</span></span>
-   <span data-ttu-id="ce37f-441">確定封裝和部署應用程式、相關聯的 mui 檔案和設定內容都已正確完成，以允許資源載入 Api 尋找當地語系化的內容。</span><span class="sxs-lookup"><span data-stu-id="ce37f-441">Ensure that packaging and deployment of the application, associated .mui files, and configuration content is done correctly to allow the resource loading APIs to find the localized content.</span></span>
-   <span data-ttu-id="ce37f-442">為終端使用者提供調整應用程式語言設定的機制。</span><span class="sxs-lookup"><span data-stu-id="ce37f-442">Provide the end user a mechanism to adjust the language configuration of the application.</span></span>
-   <span data-ttu-id="ce37f-443">調整執行時間程式碼以利用語言設定，讓應用程式更能回應使用者的需求。</span><span class="sxs-lookup"><span data-stu-id="ce37f-443">Adjust the run-time code to take advantage of language configuration, to make the application more responsive to end user needs.</span></span>

 

 
