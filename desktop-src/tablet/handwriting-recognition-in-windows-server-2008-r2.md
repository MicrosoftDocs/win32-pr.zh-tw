---
description: Windows Server 2008 R2 將伺服器端手寫辨識的支援新增至 Windows。 本主題說明如何在 Windows Server 2008 R2 中辨識手寫。
ms.assetid: ec22391d-a6e8-49b0-8650-943a661cbcd3
title: Windows Server 2008 R2 中的手寫辨識
ms.topic: article
ms.date: 06/02/2020
ms.openlocfilehash: e014a69919c6bdc87b149f761eece14bcc3d69a4
ms.sourcegitcommit: 3d718d8f69d3f86eaecf94c5705d761c5a9ef4a1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104024291"
---
# <a name="handwriting-recognition-in-windows-server-2008-r2"></a><span data-ttu-id="bf4ae-104">Windows Server 2008 R2 中的手寫辨識</span><span class="sxs-lookup"><span data-stu-id="bf4ae-104">Handwriting Recognition in Windows Server 2008 R2</span></span>

<span data-ttu-id="bf4ae-105">Windows Server 2008 R2 支援伺服器端的手寫辨識。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-105">Windows Server 2008 R2 supports server-side handwriting recognition.</span></span> <span data-ttu-id="bf4ae-106">伺服器端辨識可讓伺服器辨識網頁上手寫筆輸入的內容。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-106">Server-side recognition lets a server recognize content from pen input on Web pages.</span></span> <span data-ttu-id="bf4ae-107">當網路上的使用者將會指定使用自訂字典來解讀的字詞時，這特別有用。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-107">This is particularly useful when users on a network will be specifying terms that are interpreted using a custom dictionary.</span></span> <span data-ttu-id="bf4ae-108">例如，如果您的醫療應用程式會查詢伺服器資料庫中的患者名稱，這些名稱可能會新增至從手寫 Silverlight 表單執行搜尋時，會交叉參考的另一個資料庫。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-108">For example, if you had a medical application that queried a server database for patient names, those names could be added to another database that would be cross-referenced when performing searches from a handwritten Silverlight form.</span></span>

## <a name="set-up-your-server-for-server-side-recognition"></a><span data-ttu-id="bf4ae-109">設定您的伺服器進行 Server-Side 辨識</span><span class="sxs-lookup"><span data-stu-id="bf4ae-109">Set up your Server for Server-Side Recognition</span></span>

<span data-ttu-id="bf4ae-110">您應遵循下列步驟來設定伺服器端識別。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-110">The following steps should be followed to set up server-side recognition.</span></span>

- <span data-ttu-id="bf4ae-111">安裝筆跡和手寫服務</span><span class="sxs-lookup"><span data-stu-id="bf4ae-111">Install Ink and Handwriting Services</span></span>
- <span data-ttu-id="bf4ae-112"> (IIS) 和應用程式伺服器安裝 Web 服務器的支援</span><span class="sxs-lookup"><span data-stu-id="bf4ae-112">Install Support for Web Server (IIS) and Application Server</span></span>
- <span data-ttu-id="bf4ae-113">啟用桌面體驗角色</span><span class="sxs-lookup"><span data-stu-id="bf4ae-113">Enable the Desktop Experience Role</span></span>
- <span data-ttu-id="bf4ae-114">啟動 Tablet PC 輸入服務</span><span class="sxs-lookup"><span data-stu-id="bf4ae-114">Start the Tablet PC Input Service</span></span>

### <a name="install-ink-and-handwriting-services"></a><span data-ttu-id="bf4ae-115">安裝筆跡和手寫服務</span><span class="sxs-lookup"><span data-stu-id="bf4ae-115">Install Ink and Handwriting Services</span></span>

<span data-ttu-id="bf4ae-116">若要安裝筆跡和手寫服務，請按一下快速啟動紙匣中的 [伺服器管理員] 圖示，以開啟 [伺服器管理員]。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-116">To install Ink and Handwriting services, open the server manager by clicking the server manager icon from the Quick Launch tray.</span></span> <span data-ttu-id="bf4ae-117">在 [ **功能** ] 功能表中，按一下 [ **新增功能**]。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-117">From the **Features** menu, click **Add Features**.</span></span> <span data-ttu-id="bf4ae-118">請確定選取 [ **筆跡和手寫服務** ] 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-118">Make sure that you select the **Ink and Handwriting Services** check box.</span></span> <span data-ttu-id="bf4ae-119">下圖顯示已選取 **筆跡和手寫服務** 的 [**選取功能**] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-119">The following image shows the **Select Features** dialog box with **Ink and Handwriting Services** selected.</span></span>

<span data-ttu-id="bf4ae-120">![選取 [筆跡和手寫服務] 核取方塊的 [選取功能] 對話方塊](images/setup-server-1-ink-and-handwriting.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-120">![Select features dialog box with ink and handwriting services check box selected](images/setup-server-1-ink-and-handwriting.png)</span></span><br/>
<span data-ttu-id="bf4ae-121">*選取 [筆跡和手寫服務] 核取方塊的 [選取功能] 對話方塊*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-121">*Select features dialog box with ink and handwriting services check box selected*</span></span>

### <a name="installation-support-for-web-server-iis-and-application-server"></a><span data-ttu-id="bf4ae-122">Web 服務器 (IIS) 和應用程式伺服器的安裝支援</span><span class="sxs-lookup"><span data-stu-id="bf4ae-122">Installation Support for Web Server (IIS) and Application Server</span></span>

<span data-ttu-id="bf4ae-123">開啟 [伺服器管理員]，如同您在第一個步驟中所做的一樣。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-123">Open the server manager as you did for the first step.</span></span> <span data-ttu-id="bf4ae-124">接下來，您必須將 Web 服務器 (IIS) 和應用程式伺服器角色。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-124">Next, you will need to add the Web Server (IIS) and Application Server roles.</span></span> <span data-ttu-id="bf4ae-125">在 [ **角色** ] 功能表中，按一下 [ **新增角色**]。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-125">From the **Roles** menu, click **Add Roles**.</span></span> <span data-ttu-id="bf4ae-126">[新增角色] wizard 隨即出現。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-126">The Add Roles wizard appears.</span></span> <span data-ttu-id="bf4ae-127">按一下 [下一步] 。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-127">Click **Next**.</span></span> <span data-ttu-id="bf4ae-128">確定已選取 [ **應用程式伺服器** ] 和 [ **WEB 伺服器 (IIS)** 。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-128">Make sure **Application Server** and **Web Server (IIS)** are selected.</span></span> <span data-ttu-id="bf4ae-129">下圖顯示 [ **選取伺服器角色** ] 對話方塊，其中已選取 **網頁伺服器 (IIS)** 和 **應用程式伺服器** 角色。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-129">The following image shows the **Select Server Roles** dialog box with the **Web Server (IIS)** and **Application Server** roles selected.</span></span>

<span data-ttu-id="bf4ae-130">![選取 [伺服器角色] 對話方塊，其中已選取 web 伺服器 (iis) 和應用程式伺服器角色](images/setup-server-2-select-server-roles.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-130">![Select server roles dialog box with web server (iis) and application server roles selected](images/setup-server-2-select-server-roles.png)</span></span><br/>
<span data-ttu-id="bf4ae-131">*選取 [伺服器角色] 對話方塊，其中已選取 web 伺服器 (iis) 和應用程式伺服器角色*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-131">*Select server roles dialog box with web server (iis) and application server roles selected*</span></span>

<span data-ttu-id="bf4ae-132">當您選取 [ **應用程式伺服器**] 時，系統會要求您安裝 ASP.NET framework。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-132">When you select **Application Server**, you will be asked to install the ASP.NET framework.</span></span> <span data-ttu-id="bf4ae-133">按一下 [ **新增所需的功能** ] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-133">Click the **Add the Required Features** button.</span></span> <span data-ttu-id="bf4ae-134">按一下 **[下一步**] 之後，您會看到 [總覽] 對話方塊;按 **[下一步]**。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-134">After you click **Next**, you will be presented with an overview dialog box; click **Next**.</span></span> <span data-ttu-id="bf4ae-135">[ **選取角色服務** ] 對話方塊現在應該可以使用。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-135">The **Select Role Services** dialog box should now be available.</span></span> <span data-ttu-id="bf4ae-136">確定已選取 [ **網頁伺服器 (IIS)** 。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-136">Make sure that **Web Server (IIS)** is selected.</span></span> <span data-ttu-id="bf4ae-137">下圖顯示 [ **選取角色服務** ] 對話方塊，其中已啟用 Web 服務器 (IIS) 。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-137">The following image shows the **Select Role Services** dialog box with Web Server (IIS) enabled.</span></span>

<span data-ttu-id="bf4ae-138">![啟用 web 伺服器 (iis) 的 [選取角色服務] 對話方塊](images/setup-server-3-select-role-services.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-138">![Select role services dialog box with web server (iis) enabled](images/setup-server-3-select-role-services.png)</span></span><br/>
<span data-ttu-id="bf4ae-139">*啟用 web 伺服器 (iis) 的 [選取角色服務] 對話方塊*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-139">*Select role services dialog box with web server (iis) enabled*</span></span>

<span data-ttu-id="bf4ae-140">按一下 [下一步] 。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-140">Click **Next**.</span></span> <span data-ttu-id="bf4ae-141">[總覽] 對話方塊隨即出現;再次按 **[下一步]** 。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-141">An overview dialog box appears; click **Next** again.</span></span> <span data-ttu-id="bf4ae-142">您現在會看到一個頁面，提供您選項給 Web 服務器 (IIS) 的角色。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-142">You will now be presented with a page offering you options for roles for Web Server (IIS).</span></span> <span data-ttu-id="bf4ae-143">按一下 [下一步] 。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-143">Click **Next**.</span></span> <span data-ttu-id="bf4ae-144">在下一個頁面上，[ **安裝** ] 按鈕將會變成作用中狀態。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-144">On the next page, the **Install** button will become active.</span></span> <span data-ttu-id="bf4ae-145">按一下 [ **安裝** ]，您將會安裝 Web 服務器 (IIS) 和應用程式伺服器的支援。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-145">Click **Install** and you will install support for Web Server (IIS) and Application Server.</span></span>

### <a name="enable-the-desktop-experience-role"></a><span data-ttu-id="bf4ae-146">啟用桌面體驗角色</span><span class="sxs-lookup"><span data-stu-id="bf4ae-146">Enable the Desktop Experience Role</span></span>

<span data-ttu-id="bf4ae-147">若要啟用 [桌面體驗]，請按一下 [ **開始**]，按一下 [系統 **管理工具**]，然後按一下 [ **伺服器管理員**]。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-147">To enable the desktop experience, click **Start**, click **Administrative Tools**, and then click **Server Manager**.</span></span> <span data-ttu-id="bf4ae-148">選取 [ **新增服務** ]，然後選取 [ **桌面體驗** ] 服務。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-148">Select **Add Services** and then select the **Desktop Experience** service.</span></span> <span data-ttu-id="bf4ae-149">下圖顯示已安裝桌面體驗專案的 [ **選取功能** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-149">The following image shows the **Select Features** dialog box with the Desktop Experience item installed.</span></span>

<span data-ttu-id="bf4ae-150">![選取 [桌面體驗服務] 的 [選取功能] 對話方塊](images/setup-server-4-desktop-experience.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-150">![Select features dialog box with desktop experience service selected](images/setup-server-4-desktop-experience.png)</span></span><br/>
<span data-ttu-id="bf4ae-151">*選取 [桌面體驗服務] 的 [選取功能] 對話方塊*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-151">*Select features dialog box with desktop experience service selected*</span></span>

<span data-ttu-id="bf4ae-152">按 **[下一步]** 安裝桌面體驗。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-152">Click **Next** to install the Desktop Experience.</span></span>

### <a name="start-the-tablet-service"></a><span data-ttu-id="bf4ae-153">啟動平板電腦服務</span><span class="sxs-lookup"><span data-stu-id="bf4ae-153">Start the Tablet Service</span></span>

<span data-ttu-id="bf4ae-154">安裝桌面體驗服務之後，Tablet PC 輸入服務將會出現在 [ **服務** ] 功能表中。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-154">After you have installed the Desktop Experience service, the Tablet PC Input service will appear in the **Services** menu.</span></span> <span data-ttu-id="bf4ae-155">若要存取 [ **服務** ] 功能表，請按一下 [ **開始**]，按一下 [系統 **管理工具**]，然後按一下 [ **服務**]。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-155">To access the **Services** menu, click **Start**, click **Administrative Tools**, and then click **Services**.</span></span> <span data-ttu-id="bf4ae-156">若要啟動服務，請在 [ **TABLET PC 輸入服務** ] 上按一下滑鼠右鍵，然後按一下 [ **啟動**]。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-156">To start the service, right-click **Tablet PC Input Service** and then click **Start**.</span></span> <span data-ttu-id="bf4ae-157">下圖顯示 Tablet PC 輸入服務啟動的 [ **服務** ] 功能表。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-157">The following image shows the **Services** menu with the Tablet PC Input Service started.</span></span>

<span data-ttu-id="bf4ae-158">![已啟動 tablet pc 輸入服務的 [服務] 功能表](images/setup-server-5-tablet-pc-input-service.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-158">![Services menu with the tablet pc input service started](images/setup-server-5-tablet-pc-input-service.png)</span></span><br/>
<span data-ttu-id="bf4ae-159">*已啟動 tablet pc 輸入服務的 [服務] 功能表*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-159">*Services menu with the tablet pc input service started*</span></span>

## <a name="performing-server-side-recognition-using-silverlight"></a><span data-ttu-id="bf4ae-160">使用 Silverlight 執行 Server-Side 辨識</span><span class="sxs-lookup"><span data-stu-id="bf4ae-160">Performing Server-Side Recognition Using Silverlight</span></span>

<span data-ttu-id="bf4ae-161">本節說明如何建立使用 Silverlight 來捕捉手寫輸入的 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-161">This section shows how to create a Web application that uses Silverlight to capture handwriting input.</span></span> <span data-ttu-id="bf4ae-162">使用下列步驟，在 Visual Studio 2008 中編寫辨識器的程式。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-162">Use the following steps to program the recognizer in Visual Studio 2008.</span></span>

- <span data-ttu-id="bf4ae-163">安裝和更新 Visual Studio 2008 以新增 Silverlight 的支援。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-163">Install and update Visual Studio 2008 to add support for Silverlight.</span></span>
- <span data-ttu-id="bf4ae-164">在 Visual Studio 2008 中建立新的 Silverlight 專案。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-164">Create a new Silverlight project in Visual Studio 2008.</span></span>
- <span data-ttu-id="bf4ae-165">將必要的服務參考新增至您的專案。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-165">Add the necessary service references to your project.</span></span>
- <span data-ttu-id="bf4ae-166">建立手寫辨識的 Silverlight WCF 服務。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-166">Create a Silverlight WCF Service for ink recognition.</span></span>
- <span data-ttu-id="bf4ae-167">將服務參考加入至您的用戶端專案。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-167">Add the service reference to your client project.</span></span>
- <span data-ttu-id="bf4ae-168">將 InkCollector 類別新增至 InkRecognition 專案。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-168">Add the InkCollector class to the InkRecognition project.</span></span>
- <span data-ttu-id="bf4ae-169">從用戶端設定移除安全傳輸指示詞</span><span class="sxs-lookup"><span data-stu-id="bf4ae-169">Remove secure transport directives from the client configuration</span></span>

### <a name="install-and-update-visual-studio-2008-to-add-support-for-silverlight"></a><span data-ttu-id="bf4ae-170">安裝和更新 Visual Studio 2008 以新增 Silverlight 支援</span><span class="sxs-lookup"><span data-stu-id="bf4ae-170">Install and Update Visual Studio 2008 to Add Support for Silverlight</span></span>

<span data-ttu-id="bf4ae-171">開始之前，您必須在 Windows Server 2008 R2 伺服器上執行下列步驟。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-171">Before you begin, you must perform the following steps on your Windows Server 2008 R2 server.</span></span>

- <span data-ttu-id="bf4ae-172">安裝 Visual Studio 2008。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-172">Install Visual Studio 2008.</span></span>
- <span data-ttu-id="bf4ae-173">安裝 [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986)。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-173">Install [Microsoft Visual Studio 2008 Service Pack 1](https://www.microsoft.com/download/details.aspx?id=10986).</span></span>
- <span data-ttu-id="bf4ae-174">安裝 [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/)。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-174">Install [Microsoft Silverlight 5 SDK](https://www.microsoft.com/silverlight/).</span></span>

<span data-ttu-id="bf4ae-175">安裝這些應用程式和更新之後，您就可以開始建立您的伺服器端識別 Web 應用程式。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-175">After you have installed these applications and updates, you are ready to create your server-side recognition Web application.</span></span>

### <a name="create-a-new-silverlight-web-project-in-visual-studio-2008"></a><span data-ttu-id="bf4ae-176">在 Visual Studio 2008 中建立新的 Silverlight Web 專案</span><span class="sxs-lookup"><span data-stu-id="bf4ae-176">Create a new Silverlight Web Project in Visual Studio 2008</span></span>

<span data-ttu-id="bf4ae-177">從 [檔案] 功能表，按一下 [新增專案]。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-177">From the **File** menu, click **New Project**.</span></span> <span data-ttu-id="bf4ae-178">從 Visual C 專案清單中選取 [Silverlight 應用程式] 範本 \# 。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-178">Select the Silverlight Application template from the Visual C\# project list.</span></span> <span data-ttu-id="bf4ae-179">命名您的專案 InkRecognition，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-179">Name your project InkRecognition and click **OK**.</span></span> <span data-ttu-id="bf4ae-180">下圖顯示 \# 已選取的 C Silverlight 專案並命名為 InkRecognition。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-180">The following image shows the C\# Silverlight project selected and named InkRecognition.</span></span>

<span data-ttu-id="bf4ae-181">![已 \# 選取 c silverlight 專案，名稱為 inkrecognition](images/project-1-new-project.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-181">![c\# silverlight project selected, with the name inkrecognition](images/project-1-new-project.png)</span></span><br/>
<span data-ttu-id="bf4ae-182">*已 \# 選取 c silverlight 專案，名稱為 inkrecognition*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-182">*c\# silverlight project selected, with the name inkrecognition*</span></span>

<span data-ttu-id="bf4ae-183">按一下 **[確定**] 之後，會出現一個對話方塊，提示您將 Silverlight 應用程式新增至您的專案。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-183">After you click **OK**, a dialog box prompts you to add a Silverlight application to your project.</span></span> <span data-ttu-id="bf4ae-184">選取 **[將新的 ASP.NET Web 專案加入至方案來裝載 Silverlight** ]，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-184">Select **Add a new ASP.NET Web project to the solution to host Silverlight** and click **OK**.</span></span> <span data-ttu-id="bf4ae-185">下圖顯示如何設定範例專案，然後再按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-185">The following image shows how to set up the example project before you click **OK**.</span></span>

<span data-ttu-id="bf4ae-186">![提示將 silverlight 應用程式新增至專案的對話方塊](images/project-2-add-a-new-aspnetproject.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-186">![Dialog box with prompt for adding a silverlight application to a project](images/project-2-add-a-new-aspnetproject.png)</span></span><br/>
<span data-ttu-id="bf4ae-187">*提示將 silverlight 應用程式新增至專案的對話方塊*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-187">*Dialog box with prompt for adding a silverlight application to a project*</span></span>

### <a name="add-the-necessary-service-references-to-your-project"></a><span data-ttu-id="bf4ae-188">將必要的服務參考新增至您的專案</span><span class="sxs-lookup"><span data-stu-id="bf4ae-188">Add the Necessary Service References to your Project</span></span>

<span data-ttu-id="bf4ae-189">現在您已將一般 Silverlight 用戶端專案 (InkRecognition) 與 Web 專案搭配使用， () InkRecognition 在您的方案中設定。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-189">Now you have your generic Silverlight client project (InkRecognition) with a Web project (InkRecognition.Web) set up in your solution.</span></span> <span data-ttu-id="bf4ae-190">專案將會開啟，並開啟頁面。 xaml 和 default.aspx。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-190">The project will open with Page.xaml and Default.aspx open.</span></span> <span data-ttu-id="bf4ae-191">關閉這些視窗，並以滑鼠右鍵按一下 InkRecognition 專案中的 [參考] 資料夾，然後選取 [ **加入參考**]，將 System.string 和 system.servicemodel 參考新增至 InkRecognition 專案。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-191">Close these windows and add the System.Runtime.Serialization and System.ServiceModel references to the InkRecognition project by right-clicking on the references folder in the InkRecognition project and selecting **Add Reference**.</span></span> <span data-ttu-id="bf4ae-192">下圖顯示已選取必要參考的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-192">The following image shows the dialog box with the requisite references selected.</span></span>

<span data-ttu-id="bf4ae-193">![[加入參考] 對話方塊，其中已選取 [system.object] 和 [system.servicemodel]](images/project-3a-add-references-to-inkreco.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-193">![Add references dialog box with system.runtime.serialization and system.servicemodel selected](images/project-3a-add-references-to-inkreco.png)</span></span><br/>
<span data-ttu-id="bf4ae-194">*[加入參考] 對話方塊，其中已選取 [system.object] 和 [system.servicemodel]*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-194">*Add references dialog box with system.runtime.serialization and system.servicemodel selected*</span></span>

<span data-ttu-id="bf4ae-195">接下來，您必須將 System.servicemodel 和 InkRecognition 的參考加入至 Web 專案。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-195">Next, you need to add the System.ServiceModel and Microsoft.Ink references to the InkRecognition.Web project.</span></span> <span data-ttu-id="bf4ae-196">根據預設，Microsoft Ink 參考不會出現在 .NET 參考中，因此請在您的 Windows 資料夾中搜尋 Microsoft.Ink.dll。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-196">The Microsoft.Ink reference will not appear in the .NET references by default, so search your Windows folder for Microsoft.Ink.dll.</span></span> <span data-ttu-id="bf4ae-197">在您找到 DLL 之後，請將元件新增至專案參考：選取 [ **流覽** ] 索引標籤，變更至包含 Microsoft.Ink.dll 的資料夾，選取 [Microsoft.Ink.dll]，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-197">After you have located the DLL, add the assembly to the project references: select the **Browse** tab, change to the folder containing Microsoft.Ink.dll, select Microsoft.Ink.dll, and then click **OK**.</span></span> <span data-ttu-id="bf4ae-198">下圖顯示 Windows 檔案總管中的專案方案，並加入所有參考元件。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-198">The following image shows the project's solution in Windows Explorer with all of the reference assemblies added.</span></span>

<span data-ttu-id="bf4ae-199">![已新增所有參考元件的 windows explorer 中的 inkrecognition 專案](images/project-3b-with-reference-assemblies.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-199">![inkrecognition project in windows explorer with all reference assemblies added](images/project-3b-with-reference-assemblies.png)</span></span><br/>
<span data-ttu-id="bf4ae-200">*已新增所有參考元件的 windows explorer 中的 inkrecognition 專案*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-200">*inkrecognition project in windows explorer with all reference assemblies added*</span></span>

### <a name="create-a-silverlight-wcf-service-for-ink-recognition"></a><span data-ttu-id="bf4ae-201">建立手寫辨識的 Silverlight WCF 服務</span><span class="sxs-lookup"><span data-stu-id="bf4ae-201">Create a Silverlight WCF Service for Ink Recognition</span></span>

<span data-ttu-id="bf4ae-202">接下來，您會將筆跡辨識的 WCF 服務新增至專案。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-202">Next, you will add a WCF service for ink recognition to the project.</span></span> <span data-ttu-id="bf4ae-203">以滑鼠右鍵按一下 [InkRecognition] 專案，按一下 [ **加入**]，然後按一下 [ **新增專案**]。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-203">Right-click your InkRecognition.Web project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="bf4ae-204">選取 [WCF Silverlight 服務] 範本，將名稱變更為 InkRecogitionService，然後按一下 [ **新增**]。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-204">Select the WCF Silverlight Service template, change the name to InkRecogitionService, and then click **Add**.</span></span> <span data-ttu-id="bf4ae-205">下圖顯示 [ **加入新專案** ] 對話方塊，其中已選取並命名 Silverlight WCF 服務。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-205">The following image shows the **Add New Item** dialog box with the Silverlight WCF service selected and named.</span></span>

<span data-ttu-id="bf4ae-206">![[新增專案] 對話方塊，其中已選取並命名 silverlight wcf 服務](images/project-4-add-wcf-service.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-206">![Add new item dialog box with silverlight wcf service selected and named](images/project-4-add-wcf-service.png)</span></span><br/>
<span data-ttu-id="bf4ae-207&quot;>*[新增專案] 對話方塊，其中已選取並命名 silverlight wcf 服務*</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;bf4ae-207&quot;>*Add new item dialog box with silverlight wcf service selected and named*</span></span>

<span data-ttu-id=&quot;bf4ae-208&quot;>新增 WCF Silverlight 服務之後，將會開啟服務程式代碼後 InkRecognitionService。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;bf4ae-208&quot;>After you add the WCF Silverlight service, the service code behind, InkRecognitionService.cs, will open.</span></span> <span data-ttu-id=&quot;bf4ae-209&quot;>以下列程式碼取代服務程式代碼。</span><span class=&quot;sxs-lookup&quot;><span data-stu-id=&quot;bf4ae-209&quot;>Replace the service code with the following code.</span></span>

```CSharp
using System;
using System.Linq;
using System.Runtime.Serialization;
using System.ServiceModel;
using System.ServiceModel.Activation;
using System.Collections.Generic;
using System.Text;
using Microsoft.Ink;

namespace InkRecognition.Web
{
    [ServiceContract(Namespace = &quot;")]
    [AspNetCompatibilityRequirements(RequirementsMode = AspNetCompatibilityRequirementsMode.Allowed)]
    public class InkRecognitionService
    {
        [OperationContract]
        public string[] Recognize(int[][] packets)
        {
            // Deserialize ink.
            Ink ink = new Ink();
            Tablet tablet = new Tablets().DefaultTablet;
            TabletPropertyDescriptionCollection desc = new TabletPropertyDescriptionCollection();
            desc.Add(new TabletPropertyDescription(PacketProperty.X, tablet.GetPropertyMetrics(PacketProperty.X)));
            desc.Add(new TabletPropertyDescription(PacketProperty.Y, tablet.GetPropertyMetrics(PacketProperty.Y)));
            int numOfStrokes = packets.GetUpperBound(0) + 1;
            for (int i = 0; i < numOfStrokes; i++)
            {
                ink.CreateStroke(packets[i], desc);
            }

            // Recognize ink.
            RecognitionStatus recoStatus;
            RecognizerContext recoContext = new RecognizerContext();
            recoContext.RecognitionFlags = RecognitionModes.LineMode | RecognitionModes.TopInkBreaksOnly;
            recoContext.Strokes = ink.Strokes;
            RecognitionResult recoResult = recoContext.Recognize(out recoStatus);
            RecognitionAlternates alternates = recoResult.GetAlternatesFromSelection();
            string[] results = new string[alternates.Count];
            for (int i = 0; i < alternates.Count; i++)
            {
                results[i] = alternates[i].ToString();
            }

            // Send results to client.
            return results;
        }
    }
}
```

### <a name="add-the-service-reference-to-your-client-project"></a><span data-ttu-id="bf4ae-210">將服務參考加入至您的用戶端專案</span><span class="sxs-lookup"><span data-stu-id="bf4ae-210">Add the Service Reference to your Client Project</span></span>

<span data-ttu-id="bf4ae-211">現在您已擁有適用于 InkRecognition 的 Silverlight WCF 服務，您將會從用戶端應用程式取用服務。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-211">Now that you have your Silverlight WCF service for InkRecognition, you will consume the service from your client application.</span></span> <span data-ttu-id="bf4ae-212">以滑鼠右鍵按一下 [InkRecognition] 專案，然後選取 [ **加入服務參考**]。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-212">Right-click the InkRecognition project and select **Add Service Reference**.</span></span> <span data-ttu-id="bf4ae-213">從顯示的 [ **加入服務參考** ] 對話方塊中，選取 [ **探索** ] 以從目前的方案探索服務。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-213">From the **Add Service Reference** dialog box that appears, select **Discover** to discover services from the current solution.</span></span> <span data-ttu-id="bf4ae-214">InkRecognitionService 將會出現在 [服務] 窗格中。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-214">InkRecognitionService will appear in the Services pane.</span></span> <span data-ttu-id="bf4ae-215">按兩下 [服務] 窗格中的 [InkRecognitionService]，將命名空間變更為 InkRecognitionServiceReference，然後按一下 **[確定]**。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-215">Double-click InkRecognitionService from the Services pane, change the namespace to InkRecognitionServiceReference, and then click **OK**.</span></span> <span data-ttu-id="bf4ae-216">下圖顯示已選取 InkRecognitionService 並變更命名空間的 [ **加入服務參考** ] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-216">The following image shows the **Add Service Reference** dialog box with InkRecognitionService selected and the namespace changed.</span></span>

<span data-ttu-id="bf4ae-217">![已選取 inkrecognitionservice 並變更命名空間的 [加入服務參考] 對話方塊](images/project-5-discover-service-reference.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-217">![Add service reference dialog box with inkrecognitionservice selected and namespace changed](images/project-5-discover-service-reference.png)</span></span><br/>
<span data-ttu-id="bf4ae-218">*已選取 inkrecognitionservice 並變更命名空間的 [加入服務參考] 對話方塊*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-218">*Add service reference dialog box with inkrecognitionservice selected and namespace changed*</span></span>

### <a name="add-the-inkcollector-class-to-the-inkrecognition-project"></a><span data-ttu-id="bf4ae-219">將 InkCollector 類別新增至 InkRecognition 專案</span><span class="sxs-lookup"><span data-stu-id="bf4ae-219">Add the InkCollector Class to the InkRecognition Project</span></span>

<span data-ttu-id="bf4ae-220">以滑鼠右鍵按一下 [InkRecognition] 專案，按一下 [ **加入**]，然後按一下 [ **新增專案**]。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-220">Right-click the InkRecognition project, click **Add**, and then click **New Item**.</span></span> <span data-ttu-id="bf4ae-221">從 **Visual C \#** 功能表選取 **C \# 類別**。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-221">From the **Visual C\#** menu, select **C\# class**.</span></span> <span data-ttu-id="bf4ae-222">將類別命名為 InkCollector。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-222">Name the class InkCollector.</span></span> <span data-ttu-id="bf4ae-223">下圖顯示 \# 已選取 C 類別並命名的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-223">The following image shows the dialog box with the C\# class selected and named.</span></span>

<span data-ttu-id="bf4ae-224">![[加入新專案] 對話方塊 \# ，其中已選取 c 類別並命名為](images/project-6-add-ink-collector.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-224">![Add new item dialog box with c\# class selected and named](images/project-6-add-ink-collector.png)</span></span><br/>
<span data-ttu-id="bf4ae-225">*[加入新專案] 對話方塊 \# ，其中已選取 c 類別並命名為*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-225">*Add new item dialog box with c\# class selected and named*</span></span>

<span data-ttu-id="bf4ae-226">加入 InkCollector 類別之後，將會開啟類別定義。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-226">After you add the InkCollector class, the class definition will open.</span></span> <span data-ttu-id="bf4ae-227">將筆墨收集器中的程式碼取代為下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-227">Replace the code in the Ink Collector with the following code.</span></span>

```CSharp
using System;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Documents;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;

namespace InkRecognition
{
    public class InkCollector : IDisposable
    {
        public InkCollector(InkPresenter presenter)
        {
            _presenter = presenter;
            _presenter.Cursor = Cursors.Stylus;
            _presenter.MouseLeftButtonDown += new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove += new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp += new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
        }

        void _presenter_MouseLeftButtonDown(object sender, MouseButtonEventArgs e)
        {
            _presenter.CaptureMouse();
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
                _stroke = new Stroke(e.StylusDevice.GetStylusPoints(_presenter));
                _stroke.DrawingAttributes = _drawingAttributes;
                _presenter.Strokes.Add(_stroke);
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
                _erasePoints = e.StylusDevice.GetStylusPoints(_presenter);
            }
        }

        void _presenter_MouseMove(object sender, MouseEventArgs e)
        {
            if (!e.StylusDevice.Inverted)
            {
                _presenter.Cursor = Cursors.Stylus;
            }
            else
            {
                _presenter.Cursor = Cursors.Eraser;
            }
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            else if (_erasePoints != null)
            {
                _erasePoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
                StrokeCollection hitStrokes = _presenter.Strokes.HitTest(_erasePoints);
                if (hitStrokes.Count > 0)
                {
                    foreach (Stroke hitStroke in hitStrokes)
                    {
                        _presenter.Strokes.Remove(hitStroke);
                    }
                }
            }
        }

        void _presenter_MouseLeftButtonUp(object sender, MouseButtonEventArgs e)
        {
            _presenter.ReleaseMouseCapture();
            if (_stroke != null)
            {
                _stroke.StylusPoints.Add(e.StylusDevice.GetStylusPoints(_presenter));
            }
            _stroke = null;
            _erasePoints = null;
        }

        public DrawingAttributes DefaultDrawingAttributes
        {
            get { return _drawingAttributes; }
            set { _drawingAttributes = value; }
        }

        public void Dispose()
        {
            _presenter.MouseLeftButtonDown -= new MouseButtonEventHandler(_presenter_MouseLeftButtonDown);
            _presenter.MouseMove -= new MouseEventHandler(_presenter_MouseMove);
            _presenter.MouseLeftButtonUp -= new MouseButtonEventHandler(_presenter_MouseLeftButtonUp);
            _presenter = null;
        }

        private InkPresenter _presenter = null;
        private Stroke _stroke = null;
        private StylusPointCollection _erasePoints = null;
        private DrawingAttributes _drawingAttributes = new DrawingAttributes();
    }
}
```

### <a name="update-the-xaml-for-the-default-page-and-add-a-code-behind-for-handwriting-recognition"></a><span data-ttu-id="bf4ae-228">更新預設頁面的 XAML，並加入手寫辨識的程式碼後置於</span><span class="sxs-lookup"><span data-stu-id="bf4ae-228">Update the XAML for the Default Page and Add a Code Behind for Handwriting Recognition</span></span>

<span data-ttu-id="bf4ae-229">現在您已有一個可收集筆跡的類別，您必須使用下列 XAML 更新頁面中的 XAML。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-229">Now that you have a class that collects ink, you will need to update the XAML in page.xaml with the following XAML.</span></span> <span data-ttu-id="bf4ae-230">下列程式碼會將黃色漸層新增至輸入區域、InkCanvas 控制項，以及將觸發辨識的按鈕。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-230">The following code adds a yellow gradient to the input area, an InkCanvas control, and a button that will trigger recognition.</span></span>

```XML
<UserControl x:Class="InkRecognition.Page"
    xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation" 
    xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">
    <Grid x:Name="LayoutRoot" Background="White">
        <Grid.RowDefinitions>
            <RowDefinition Height="Auto"/>
            <RowDefinition Height="Auto"/>
        </Grid.RowDefinitions>
        <Border Margin="5" Grid.Row="0" BorderThickness="4" BorderBrush="Black" CornerRadius="5" Height="200">
            <Grid>
                <InkPresenter x:Name="inkCanvas">
                    <InkPresenter.Background>
                        <LinearGradientBrush StartPoint="0.5,0" EndPoint="0.5,1">
                            <GradientStop Offset="0" Color="Yellow"/>
                            <GradientStop Offset="1" Color="LightYellow"/>
                        </LinearGradientBrush>
                    </InkPresenter.Background>
                </InkPresenter>
                <Button Grid.Row="0" HorizontalAlignment="Right" VerticalAlignment="Bottom" Margin="10" Content="Recognize" Click="RecoButton_Click"/>
            </Grid>
        </Border>
        <Grid Grid.Row="1">
            <Grid.ColumnDefinitions>
                <ColumnDefinition Width="Auto"/>
                <ColumnDefinition Width="*"/>
            </Grid.ColumnDefinitions>
            <TextBlock Grid.Column="0" FontSize="28" Text="Result: "/>
            <ComboBox x:Name="results" Grid.Column="1" FontSize="28"/>
        </Grid>
    </Grid>
</UserControl>
```

<span data-ttu-id="bf4ae-231">以下列程式碼取代 [程式碼後頁] 頁面，將會加入 [ **辨識** ] 按鈕的事件處理常式。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-231">Replace the code behind page, Page.xaml.cs, with the following code that will add an event handler for the **Recognize** button.</span></span>

```CSharp
using System;
using System.Collections.Generic;
using System.Collections.ObjectModel;
using System.Linq;
using System.Net;
using System.Windows;
using System.Windows.Controls;
using System.Windows.Ink;
using System.Windows.Input;
using System.Windows.Media;
using System.Windows.Media.Animation;
using System.Windows.Shapes;
using InkRecognition.InkRecognitionServiceReference;

namespace InkRecognition
{
    public partial class Page : UserControl
    {
        public Page()
        {
            InitializeComponent();
            inkCol = new InkCollector(inkCanvas);
            recoClient = new InkRecognitionServiceClient();
            recoClient.RecognizeCompleted += new EventHandler<RecognizeCompletedEventArgs>(recoClient_RecognizeCompleted);
        }

        private void RecoButton_Click(object sender, RoutedEventArgs e)
        {
            // Serialize the ink into an array on ints.
            ObservableCollection<ObservableCollection<int>> packets = new ObservableCollection<ObservableCollection<int>>();
            double pixelToHimetricMultiplier = 2540d / 96d;

            foreach (Stroke stroke in inkCanvas.Strokes)
            {
                packets.Add(new ObservableCollection<int>());
                int index = inkCanvas.Strokes.IndexOf(stroke);
                for (int i = 0; i < stroke.StylusPoints.Count; i += 2)
                {
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].X * pixelToHimetricMultiplier));
                    packets[index].Add(Convert.ToInt32(stroke.StylusPoints[i].Y * pixelToHimetricMultiplier));
                }
            }

            // Call the Web service.
            recoClient.RecognizeAsync(packets);
        }

        void recoClient_RecognizeCompleted(object sender, RecognizeCompletedEventArgs e)
        {
            // We have received results from the server, now display them.
            results.ItemsSource = e.Result;
            UpdateLayout();
            results.SelectedIndex = 0;
            inkCanvas.Strokes.Clear();
        }

        private InkRecognitionServiceClient recoClient = null;
        private InkCollector inkCol = null;
    }
}
```

### <a name="remove-secure-transport-directives-from-the-client-configuration"></a><span data-ttu-id="bf4ae-232">從用戶端設定移除安全傳輸指示詞</span><span class="sxs-lookup"><span data-stu-id="bf4ae-232">Remove Secure Transport Directives from the Client Configuration</span></span>

<span data-ttu-id="bf4ae-233">在您可以取用 WCF 服務之前，您必須從服務設定移除所有安全傳輸選項，因為 Silverlight 2.0 WCF 服務目前不支援安全傳輸。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-233">Before you can consume the WCF service, you must remove all secure transport options from the service configuration because secure transports are not currently supported in Silverlight 2.0 WCF services.</span></span> <span data-ttu-id="bf4ae-234">從 InkRecognition 專案中，更新 ServiceReferences. ClientConfig 中的安全性設定。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-234">From the InkRecognition project, update the security settings in ServiceReferences.ClientConfig.</span></span> <span data-ttu-id="bf4ae-235">變更安全性 XML 來源</span><span class="sxs-lookup"><span data-stu-id="bf4ae-235">Change the security XML from</span></span>

```XML
          <security mode="None">
            <transport>
              <extendedProtectionPolicy policyEnforcement="WhenSupported" />
            </transport>
          </security>
```

<span data-ttu-id="bf4ae-236">to</span><span class="sxs-lookup"><span data-stu-id="bf4ae-236">to</span></span>

```XML
       <security mode="None"/>
```

<span data-ttu-id="bf4ae-237">現在，您的應用程式應該會執行。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-237">Now, your application should run.</span></span> <span data-ttu-id="bf4ae-238">下圖顯示應用程式在 awebpagewith 中輸入的一些手寫內容。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-238">The following image shows how the application looks within awebpagewith some handwriting entered into the recognition box.</span></span>

<span data-ttu-id="bf4ae-239">![Awebpagewith 中的應用程式在辨識方塊中輸入的一些手寫](images/demo-1.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-239">![Application within awebpagewith some handwriting entered into recognition box](images/demo-1.png)</span></span><br/>
<span data-ttu-id="bf4ae-240">*Awebpagewith 中的應用程式在辨識方塊中輸入的一些手寫*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-240">*Application within awebpagewith some handwriting entered into recognition box*</span></span>

<span data-ttu-id="bf4ae-241">下圖顯示 [ **結果** ] 下拉式清單中的已辨識文字。</span><span class="sxs-lookup"><span data-stu-id="bf4ae-241">The following image shows the recognized text in the **Result** drop-down list.</span></span>

<span data-ttu-id="bf4ae-242">![Awebpagewith 中的應用程式已辨識結果下拉式清單中的文字](images/demo-2.png)</span><span class="sxs-lookup"><span data-stu-id="bf4ae-242">![Application within awebpagewith recognized text in result drop-down list](images/demo-2.png)</span></span><br/>
<span data-ttu-id="bf4ae-243">*Awebpagewith 中的應用程式已辨識結果下拉式清單中的文字*</span><span class="sxs-lookup"><span data-stu-id="bf4ae-243">*Application within awebpagewith recognized text in result drop-down list*</span></span>

 

 



