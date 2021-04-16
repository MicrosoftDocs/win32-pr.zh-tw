---
title: 使用 Windows 應用程式認證套件
description: 為了讓您的傳統型應用程式在提交認證並在 Windows 市集中列出之前，獲得認證、驗證及測試電腦上的最佳機會。
ms.assetid: 8B460B84-0997-4987-9B66-90F9C6D88D83
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 89b3c6e4de3286dd6418c4c8e186bcadaddf00b7
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104383090"
---
# <a name="using-the-windows-app-certification-kit"></a><span data-ttu-id="1bd43-103">使用 Windows 應用程式認證套件</span><span class="sxs-lookup"><span data-stu-id="1bd43-103">Using the Windows App Certification Kit</span></span>

<span data-ttu-id="1bd43-104">為了讓您的傳統型應用程式在提交認證並在 Windows 市集中列出之前，獲得認證、驗證及測試電腦上的最佳機會。</span><span class="sxs-lookup"><span data-stu-id="1bd43-104">To give your desktop app the best chance of getting certified, validate and test it on your computer before you submit it for certification and listing in the Windows Store.</span></span> <span data-ttu-id="1bd43-105">若要認證您的應用程式，您必須安裝並執行 [Windows 應用程式認證套件](/previous-versions//mt637081(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="1bd43-105">To certify your app, you need to install and run the [Windows App Certification Kit](/previous-versions//mt637081(v=vs.85)).</span></span> <span data-ttu-id="1bd43-106">如需套件內特定測試的詳細資訊，請參閱 [Windows 應用程式認證套件測試](windows-app-certification-kit-tests.md)。</span><span class="sxs-lookup"><span data-stu-id="1bd43-106">For details on specific tests within the kit, refer to [Windows App Certification Kit tests](windows-app-certification-kit-tests.md).</span></span>

<span data-ttu-id="1bd43-107">如需深入瞭解認證程式，以及此工具的使用方式，請參閱 [認證您的桌面應用程式](windows-certification-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="1bd43-107">For a high level look at the certification process, and where the use of this tool fits in, see [Certify your desktop app](windows-certification-portal.md).</span></span>

<span data-ttu-id="1bd43-108">目前版本的 Windows ACK 提供14種語言 (捷克文、英文、法文、德文、義大利文、日文、韓文、波蘭文、葡萄牙文 (巴西) 、俄文、簡體中文、西班牙文、繁體中文和土耳其文) 。</span><span class="sxs-lookup"><span data-stu-id="1bd43-108">The current release of Windows ACK is available in 14 languages (Czech, English, French, German, Italian, Japanese, Korean, Polish, Portuguese (Brazil), Russian, Simplified Chinese, Spanish, Traditional Chinese, and Turkish).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="1bd43-109">必要條件</span><span class="sxs-lookup"><span data-stu-id="1bd43-109">Prerequisites</span></span>

<span data-ttu-id="1bd43-110">在安裝 Windows ACK 之前，您必須先安裝並執行作業系統。</span><span class="sxs-lookup"><span data-stu-id="1bd43-110">Before you install the Windows ACK, you need to install and run the operating system.</span></span>

1. <span data-ttu-id="1bd43-111">安裝並執行您要開發應用程式的作業系統。</span><span class="sxs-lookup"><span data-stu-id="1bd43-111">Install and run the operating system you're developing apps for.</span></span>

-   <span data-ttu-id="1bd43-112">如果您要開發適用于 Windows 7 的應用程式，您可以安裝和執行 Windows 7、Windows 8 或 Windows 8.1。</span><span class="sxs-lookup"><span data-stu-id="1bd43-112">If you're developing apps for Windows 7, you can install and run Windows 7, Windows 8, or Windows 8.1.</span></span>
-   <span data-ttu-id="1bd43-113">如果您要開發 Windows 8 傳統型應用程式或 Windows 8 桌面裝置應用程式，您可以安裝並執行 Windows 8 或 Windows 8.1。</span><span class="sxs-lookup"><span data-stu-id="1bd43-113">If you're developing a Windows 8 desktop app or Windows 8 desktop device app, you can install and run Windows 8 or Windows 8.1.</span></span>
-   <span data-ttu-id="1bd43-114">如果您要開發 Windows 8.1 desktop 應用程式或 Windows 8 桌面裝置應用程式，請安裝 Windows 8.1。</span><span class="sxs-lookup"><span data-stu-id="1bd43-114">If you're developing a Windows 8.1 desktop app or Windows 8 desktop device app, install Windows 8.1.</span></span>

2. <span data-ttu-id="1bd43-115">安裝 [Windows 應用程式認證套件 3.3](/previous-versions//mt637081(v=vs.85))，其包含在適用于 Windows 8.1 的 WINDOWS 軟體開發套件 (SDK) 中。</span><span class="sxs-lookup"><span data-stu-id="1bd43-115">Install the [Windows App Certification Kit 3.3](/previous-versions//mt637081(v=vs.85)), which is included in the Windows Software Development Kit (SDK) for Windows 8.1.</span></span>

<span data-ttu-id="1bd43-116">**注意：** 當您在電腦上安裝 Windows 應用程式認證套件3.3 或更高版本時，會取代任何先前安裝的套件版本。</span><span class="sxs-lookup"><span data-stu-id="1bd43-116">**Note:** When you install Windows App Certification Kit 3.3 or higher on your PC, you replace any previously installed version of the kit.</span></span>

## <a name="instructions-to-run-windows-app-certification-kit-33"></a><span data-ttu-id="1bd43-117">執行 Windows 應用程式認證套件3.3 的指示</span><span class="sxs-lookup"><span data-stu-id="1bd43-117">Instructions to run Windows App Certification Kit 3.3</span></span>

<span data-ttu-id="1bd43-118">**以互動方式使用 Windows 應用程式認證套件3.3 來驗證您的桌面應用程式**</span><span class="sxs-lookup"><span data-stu-id="1bd43-118">**Validate your desktop app by using the Windows App Certification Kit 3.3 interactively**</span></span>

1.  <span data-ttu-id="1bd43-119">從 [開始] 功能表搜尋 Windows 應用程式憑證套件。</span><span class="sxs-lookup"><span data-stu-id="1bd43-119">From the Start menu, search for Windows App Cert Kit.</span></span>
2.  <span data-ttu-id="1bd43-120">在 [Windows 應用程式認證套件中，按一下您要執行的測試驗證類別目錄。</span><span class="sxs-lookup"><span data-stu-id="1bd43-120">From the Windows App Certification Kit, click the test validation category you want to run.</span></span> <span data-ttu-id="1bd43-121">如果您要驗證傳統型應用程式，請選取 [ **驗證桌面應用程式**]。</span><span class="sxs-lookup"><span data-stu-id="1bd43-121">If you’re validating a desktop app, select **Validate Desktop app**.</span></span>
3.  <span data-ttu-id="1bd43-122">在下一個畫面中，流覽至您要驗證的桌面應用程式的安裝檔案。</span><span class="sxs-lookup"><span data-stu-id="1bd43-122">In the next screen, browse to the setup file of the desktop app you want to validate.</span></span>
    -   <span data-ttu-id="1bd43-123">**注意：** 如有必要，您可以使用 [命令列步驟](#commandlinesteps) 來包含選項或安裝參數。</span><span class="sxs-lookup"><span data-stu-id="1bd43-123">**Note:** You can use the [command line steps](#commandlinesteps) to include options or an installation switch, if necessary.</span></span>
4.  <span data-ttu-id="1bd43-124">指出應用程式的使用類型，然後按 **[下一步]**。</span><span class="sxs-lookup"><span data-stu-id="1bd43-124">Indicate the app usage type, and then click **Next**.</span></span> <span data-ttu-id="1bd43-125">Windows 應用程式認證套件開始使用安裝程式檔案來安裝傳統型應用程式，以便驗證安裝。</span><span class="sxs-lookup"><span data-stu-id="1bd43-125">The Windows App Certification Kit starts installing the desktop app using the setup files so it can validate the installation.</span></span>
5.  <span data-ttu-id="1bd43-126">如果系統要求您重新開機系統以完成安裝程式，請選擇 [ **否**]。</span><span class="sxs-lookup"><span data-stu-id="1bd43-126">If you're asked to reboot the system to complete setup, choose **No**.</span></span> <span data-ttu-id="1bd43-127">如果您的應用程式需要安裝數個元件或外部相依性，請仔細選取應用程式的名稱。</span><span class="sxs-lookup"><span data-stu-id="1bd43-127">If your app needs to install several components or external dependencies, carefully select the name for your app.</span></span> <span data-ttu-id="1bd43-128">如果您在 Windows 市集中列出應用程式，則您在此處選擇的名稱就是您的應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="1bd43-128">The name you choose here is the name your app is given if it gets listed in the Windows Store.</span></span> <span data-ttu-id="1bd43-129">驗證完成時，請以您在步驟6中為應用程式提供的名稱來儲存報表。</span><span class="sxs-lookup"><span data-stu-id="1bd43-129">When validation is complete, save the report with the name you gave your app in Step 6.</span></span> <span data-ttu-id="1bd43-130">Windows 應用程式認證套件會建立 XML 報表檔案並加以儲存。</span><span class="sxs-lookup"><span data-stu-id="1bd43-130">The Windows App Certification Kit creates an XML report file and saves it.</span></span>
6.  <span data-ttu-id="1bd43-131">流覽至您儲存報表的資料夾，然後開啟該資料夾以查看測試的結果。</span><span class="sxs-lookup"><span data-stu-id="1bd43-131">Navigate to the folder where you saved the report and open it to view the results of the test.</span></span> <span data-ttu-id="1bd43-132">如果您的測試失敗，且您有資格獲得棄權，您需要提交的資訊會列在此處。</span><span class="sxs-lookup"><span data-stu-id="1bd43-132">If your test failed and you’re eligible for a waiver, the info you need to submit is listed here.</span></span> <span data-ttu-id="1bd43-133">您必須針對每個可能的棄權要求提交詳細的描述。</span><span class="sxs-lookup"><span data-stu-id="1bd43-133">You must submit a detailed description for each possible waiver request.</span></span>

<span data-ttu-id="1bd43-134">**從命令列使用 Windows 應用程式認證套件3.3 來驗證您的 Windows 桌面應用程式**</span><span class="sxs-lookup"><span data-stu-id="1bd43-134">**Validate your Windows desktop app by using the Windows App Certification Kit 3.3 from a command line**</span></span>

1.  <span data-ttu-id="1bd43-135">流覽至您儲存報表的資料夾，然後開啟該資料夾以查看測試的結果。</span><span class="sxs-lookup"><span data-stu-id="1bd43-135">Navigate to the folder where you saved the report and open it to view the results of the test.</span></span> <span data-ttu-id="1bd43-136">此處會列出可能具有棄權要求的失敗測試。</span><span class="sxs-lookup"><span data-stu-id="1bd43-136">Failed tests with a possible waiver request are listed here.</span></span> <span data-ttu-id="1bd43-137">您必須針對每個可能的棄權要求提交詳細的描述。</span><span class="sxs-lookup"><span data-stu-id="1bd43-137">You must submit a detailed description for each possible waiver request.</span></span>
2.  <span data-ttu-id="1bd43-138">從包含 Windows 應用程式認證套件的資料夾中，依下列順序輸入下列命令：</span><span class="sxs-lookup"><span data-stu-id="1bd43-138">From the folder that contains the Windows App Certification Kit, enter these commands in this order:</span></span>

    -   <span id="commandLineSteps"></span><span id="commandlinesteps"></span><span id="COMMANDLINESTEPS"></span>`appcert.exe reset`
    -   `appcert test -apptype desktop -setuppath d:\cdrom\setup.exe  -appusage peruser -reportoutputpath [report file name]`

    <span data-ttu-id="1bd43-139">其中： `[report file name]` 是套件將建立以包含測試報表之 XML 檔案的完整檔案名。</span><span class="sxs-lookup"><span data-stu-id="1bd43-139">where: `[report file name]`is the fully qualified file name of the XML file that the kit will create to contain the test report.</span></span>

3.  <span data-ttu-id="1bd43-140">測試完成之後，請開啟名為 [報表檔案名] 的報表檔案 \[ \] ，並查看測試結果。</span><span class="sxs-lookup"><span data-stu-id="1bd43-140">After the test completes, open the report file named \[report file name\] and view the test results.</span></span>

    <span data-ttu-id="1bd43-141">**注意：** 如需 Windows 應用程式認證套件命令列的詳細資訊，請輸入命令 appcert.exe/？</span><span class="sxs-lookup"><span data-stu-id="1bd43-141">**Note:** For more information about the Windows App Certification Kit command line, enter the command appcert.exe /?</span></span>

    <span data-ttu-id="1bd43-142">Windows 應用程式認證套件必須在作用中使用者會話的內容中執行，但是您無法在非互動式會話中啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="1bd43-142">The Windows App Certification Kit must be run in the context of an active user session but you can't launch apps in a non-interactive session.</span></span> <span data-ttu-id="1bd43-143">套件處理權杖以使用或不使用系統管理許可權來執行測試的方式，也取決於此使用者會話內容。</span><span class="sxs-lookup"><span data-stu-id="1bd43-143">The way the kit handles tokens for running tests with or without administrative privileges depends on this user session context as well.</span></span> <span data-ttu-id="1bd43-144">您可以從服務執行套件，但是服務必須能夠在使用中的使用者會話中產生套件進程。</span><span class="sxs-lookup"><span data-stu-id="1bd43-144">The kit can be run from a service, but the service must be able to spawn the kit process in an active user session.</span></span>

<span data-ttu-id="1bd43-145">**使用 Windows 應用程式認證套件來驗證您的 Windows 7 應用程式**</span><span class="sxs-lookup"><span data-stu-id="1bd43-145">**Use the Windows App Certification Kit to validate your Windows 7 apps**</span></span>

-   <span data-ttu-id="1bd43-146">Windows 應用程式認證套件取代了 Windows 軟體標誌套件。</span><span class="sxs-lookup"><span data-stu-id="1bd43-146">The Windows App Certification Kit replaced the Windows Software Logo Kit.</span></span> <span data-ttu-id="1bd43-147">如果您想要應用程式的 Windows 7 標誌，請使用驗證測試和報告的 Windows 應用程式認證套件。</span><span class="sxs-lookup"><span data-stu-id="1bd43-147">If you want the Windows 7 logo for your app, use the Windows App Certification Kit for your validation testing and report.</span></span> <span data-ttu-id="1bd43-148">套件可以偵測正在執行的作業系統，並自動啟動 Windows 7 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1bd43-148">The kit can detect which operating system it's running on and automatically launches for Windows 7 apps.</span></span> <span data-ttu-id="1bd43-149">遵循相同的程式來驗證 Windows 7 應用程式。</span><span class="sxs-lookup"><span data-stu-id="1bd43-149">Follow the same process for validating Windows 7 apps.</span></span>

<span data-ttu-id="1bd43-150">**提交認證**</span><span class="sxs-lookup"><span data-stu-id="1bd43-150">**Submit for certification**</span></span>

-   <span data-ttu-id="1bd43-151">驗證您的應用程式之後，您就可以 [透過入口網站提交](https://www.microsoft.com/?ref=go)程式來提交認證。</span><span class="sxs-lookup"><span data-stu-id="1bd43-151">After your app is validated, you're ready to submit it for certification [through the portal submission process](https://www.microsoft.com/?ref=go).</span></span>

## <a name="reference-documents"></a><span data-ttu-id="1bd43-152">參考檔</span><span class="sxs-lookup"><span data-stu-id="1bd43-152">Reference Documents</span></span>

-   [<span data-ttu-id="1bd43-153">Windows 桌面應用程式的認證需求</span><span class="sxs-lookup"><span data-stu-id="1bd43-153">Certification requirements for Windows desktop apps</span></span>](/windows/desktop/win_cert/certification-requirements-for-windows-desktop-apps)
-   [<span data-ttu-id="1bd43-154">應用程式認證技術白皮書</span><span class="sxs-lookup"><span data-stu-id="1bd43-154">App certification white paper</span></span>](https://www.microsoft.com/download/details.aspx?id=27414)
-   <span data-ttu-id="1bd43-155">[適用于桌面應用程式的 Windows Store 上線](/previous-versions//dn322034(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1bd43-155">[Windows Store onboarding for desktop apps](/previous-versions//dn322034(v=vs.85))</span></span>
-   [<span data-ttu-id="1bd43-156">Windows 7 桌面應用程式認證需求</span><span class="sxs-lookup"><span data-stu-id="1bd43-156">Windows 7 desktop app certification requirements</span></span>](https://techcommunity.microsoft.com/t5/windows-hardware-certification/bg-p/WindowsHardwareCertification)

## <a name="windows-app-certification-kit-tests"></a><span data-ttu-id="1bd43-157">Windows 應用程式認證套件測試</span><span class="sxs-lookup"><span data-stu-id="1bd43-157">Windows App Certification Kit tests</span></span>

<span data-ttu-id="1bd43-158">我們已變更套件，讓 [WINDOWS ACK 測試](windows-app-certification-kit-tests.md) 更容易使用。</span><span class="sxs-lookup"><span data-stu-id="1bd43-158">We’ve changed the kit to make the [Windows ACK tests](windows-app-certification-kit-tests.md) easier to use.</span></span> <span data-ttu-id="1bd43-159">套件現在具有：</span><span class="sxs-lookup"><span data-stu-id="1bd43-159">The kit now has:</span></span>

-   <span data-ttu-id="1bd43-160">全新的簡化使用者介面</span><span class="sxs-lookup"><span data-stu-id="1bd43-160">A new simplified user interface</span></span>
-   <span data-ttu-id="1bd43-161">已改善多使用者測試，因此您不再需要設定第二個使用者帳戶</span><span class="sxs-lookup"><span data-stu-id="1bd43-161">Improved multi-user test, which no longer requires that you set up a second user account</span></span>

 

 