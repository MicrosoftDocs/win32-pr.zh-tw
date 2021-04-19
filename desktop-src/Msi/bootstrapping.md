---
description: 目前每次嘗試使用 Windows Installer 的安裝都會先檢查安裝程式是否出現在使用者的電腦上，如果不存在，是否已準備好安裝 Windows Installer 的使用者和電腦。
ms.assetid: a5174284-2a8c-4510-accf-641fda5be98d
title: 引導
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff743acbcd2dfc81b0e912e5be84c363f34614ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982379"
---
# <a name="bootstrapping"></a><span data-ttu-id="f7527-103">引導</span><span class="sxs-lookup"><span data-stu-id="f7527-103">Bootstrapping</span></span>

<span data-ttu-id="f7527-104">目前每次嘗試使用 Windows Installer 的安裝都會先檢查安裝程式是否出現在使用者的電腦上，如果不存在，是否已準備好安裝 Windows Installer 的使用者和電腦。</span><span class="sxs-lookup"><span data-stu-id="f7527-104">Currently every installation that attempts to use the Windows Installer begins by checking whether the installer is present on the user's computer, and if it is not present, whether the user and computer are ready to install Windows Installer.</span></span> <span data-ttu-id="f7527-105">Windows Installer SDK 提供安裝應用程式 [Instmsi.exe](instmsi-exe.md) ，其中包含安裝 Windows Installer 的所有邏輯和功能。</span><span class="sxs-lookup"><span data-stu-id="f7527-105">A setup application [Instmsi.exe](instmsi-exe.md) is available with the Windows Installer SDK that contains all logic and functionality to install Windows Installer.</span></span> <span data-ttu-id="f7527-106">不過，啟動載入應用程式必須管理此安裝。</span><span class="sxs-lookup"><span data-stu-id="f7527-106">However, a bootstrapping application must manage this installation.</span></span>

<span data-ttu-id="f7527-107">啟動載入應用程式必須先檢查目前是否已安裝 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="f7527-107">The bootstrapping application must first check to see whether Windows Installer is currently installed.</span></span> <span data-ttu-id="f7527-108">應用程式可以使用 [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc)取得目前安裝的 Windows Installer 版本。</span><span class="sxs-lookup"><span data-stu-id="f7527-108">Applications can get the version of Windows Installer currently installed by using [**DllGetVersion**](/windows/win32/api/shlwapi/nc-shlwapi-dllgetversionproc).</span></span> <span data-ttu-id="f7527-109">如果目前未安裝 Windows Installer，啟動載入器應用程式必須查詢作業系統，以判斷所需的 Instmsi.exe 版本。</span><span class="sxs-lookup"><span data-stu-id="f7527-109">If Windows Installer is not currently installed, the bootstrapping application must query the operating system to determine which version of the Instmsi.exe is required.</span></span> <span data-ttu-id="f7527-110">開始安裝 Windows Installer 之後，啟動載入應用程式必須處理來自 Instmsi.exe 應用程式的傳回碼，並處理 Windows Installer 安裝期間所產生的任何重新開機。</span><span class="sxs-lookup"><span data-stu-id="f7527-110">Once the installation of Windows Installer has initiated, the bootstrapping application must handle return codes from the Instmsi.exe application and handle any reboot that is incurred during the Windows Installer installation.</span></span> <span data-ttu-id="f7527-111">如需詳細資訊，請參閱 [判斷 Windows Installer 版本](determining-the-windows-installer-version.md)</span><span class="sxs-lookup"><span data-stu-id="f7527-111">For more information, see [Determining the Windows Installer Version](determining-the-windows-installer-version.md)</span></span>

<span data-ttu-id="f7527-112">下列範例會示範安裝 Microsoft Office 2000 的安裝應用程式如何檢查使用者的系統，並設定 Windows Installer 安裝。</span><span class="sxs-lookup"><span data-stu-id="f7527-112">The following example demonstrates how the setup application which installs Microsoft Office 2000 checks the user's system and configures the Windows Installer installation.</span></span> <span data-ttu-id="f7527-113">此範例是專為安裝 Office 2000 所撰寫，且僅供一般參考使用。</span><span class="sxs-lookup"><span data-stu-id="f7527-113">This example is specifically written to install Office 2000 and should be used as a general reference only.</span></span>

<span data-ttu-id="f7527-114">當使用者將 Office 2000 CD-ROM 插入電腦時，Setup.exe 會根據使用者的需求，嘗試啟動維護模式、安裝應用程式，或完全不執行任何動作。</span><span class="sxs-lookup"><span data-stu-id="f7527-114">When a user inserts an Office 2000 CD-ROM into their computer, Setup.exe attempts to launch the maintenance mode, the setup application, or does nothing at all, according to the user's needs.</span></span> <span data-ttu-id="f7527-115">下一節描述 Office 2000 安裝應用程式（名為 Setup.exe）如何限定使用者和其電腦、如何建立命令列，並使用 Msiexec.exe 應用程式安裝 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="f7527-115">The following section describes how the Office 2000 setup application, named Setup.exe, qualifies the user and their computer, constructs a command line and installs Windows Installer using the Msiexec.exe application.</span></span>

## <a name="how-setupexe-bootstraps-the-windows-installer-when-installing-office-2000"></a><span data-ttu-id="f7527-116">Setup.exe 如何在安裝 Office 2000 時啟動 Windows Installer</span><span class="sxs-lookup"><span data-stu-id="f7527-116">How Setup.exe Bootstraps the Windows Installer when Installing Office 2000</span></span>

1.  <span data-ttu-id="f7527-117">使用者將 Office 2000 CD-ROM 插入他們的電腦。</span><span class="sxs-lookup"><span data-stu-id="f7527-117">The user inserts an Office 2000 CD-ROM into their computer.</span></span> <span data-ttu-id="f7527-118">Windows 作業系統會使用/autorun 參數和自動播放 .inf 檔案起始 Setup.exe。</span><span class="sxs-lookup"><span data-stu-id="f7527-118">The Windows operating system initiates Setup.exe using the /autorun switch and the Autorun.inf file.</span></span> <span data-ttu-id="f7527-119">您可以在 Office 2000 CD-ROM 的根目錄找到自動執行 .inf 檔案，其中包含下列各節：</span><span class="sxs-lookup"><span data-stu-id="f7527-119">The Autorun.inf file is found at the root of the Office 2000 CD-ROM and contains the following sections:</span></span>

    <span data-ttu-id="f7527-120">\[自動執行\]</span><span class="sxs-lookup"><span data-stu-id="f7527-120">\[Autorun\]</span></span>

     

    <span data-ttu-id="f7527-121">\[Office 功能\]</span><span class="sxs-lookup"><span data-stu-id="f7527-121">\[Office Features\]</span></span>

     

    <span data-ttu-id="f7527-122">\[產品資訊\]</span><span class="sxs-lookup"><span data-stu-id="f7527-122">\[Product Information\]</span></span>

     

    <span data-ttu-id="f7527-123">\[ServicePack \] 。</span><span class="sxs-lookup"><span data-stu-id="f7527-123">\[ServicePack\].</span></span>

    <span data-ttu-id="f7527-124">[ \[ 自動 \] 執行] 區段包含執行 Setup.exe 應用程式的命令列、執行用來顯示光碟的圖示，以及包含將 [安裝] 選項和 [設定] 選項新增至 cd-rom 內容功能表的資訊。</span><span class="sxs-lookup"><span data-stu-id="f7527-124">The \[Autorun\] section contains a command line that executes the Setup.exe application, executes the icon used to display the disc, and contains information to add an "Install" option and a "Configure" option to the context menu for the CD-ROM.</span></span>

    <span data-ttu-id="f7527-125">[ \[ Office 功能] \] 區段包含功能和功能名稱組的清單。</span><span class="sxs-lookup"><span data-stu-id="f7527-125">The \[Office Features\] section contains a list of features and feature name pairs.</span></span>

    <span data-ttu-id="f7527-126">[ \[ 產品資訊] \] 區段會指定應用程式的名稱和版本。</span><span class="sxs-lookup"><span data-stu-id="f7527-126">The \[Product Information\] section specifies the name and version of the application.</span></span>

    <span data-ttu-id="f7527-127">[ \[ ServicePack] \] 區段可讓網路系統管理員設定所需的最低 service pack 層級。</span><span class="sxs-lookup"><span data-stu-id="f7527-127">The \[ServicePack\] section allows a network administrator to set the minimum required service pack level.</span></span> <span data-ttu-id="f7527-128">網路系統管理員可以使用此區段來撰寫當本機作業系統沒有必要的 service pack 時，所顯示的警示訊息文字。</span><span class="sxs-lookup"><span data-stu-id="f7527-128">The network administrator can use this section to author the text of an alert message displayed if the local operating system does not have the required service pack.</span></span>

    <span data-ttu-id="f7527-129">以下是範例自動執行 .inf。</span><span class="sxs-lookup"><span data-stu-id="f7527-129">The following is a sample Autorun.inf.</span></span>

    ``` syntax
    [autorun] 
    OPEN=setup.EXE /AUTORUN /KEY:Software\Microsoft\Office\9.0\Common\General\InstallProductID
    ICON=setup.EXE,1
    shell\configure=&Configure
    shell\configure\command=setup.EXE
    shell\install=&Install
    shell\install\command=setup.EXE
    [OfficeFeatures]
    Feature1=ACCESSFiles
    Feature2=OfficeFiles
    Feature3=WORDFiles
    Feature4=EXCELFiles
    Feature5=PPTFiles
    [ProductInformation]
    DisplayName=Microsoft Office 9
    Version=9.0
    ProductCode={product guid}
    [ServicePack]
    MessageText="The operating system does not have a required service pack. Please download and install this from www.microsoft.com."
    SPLevel=3
    ```

2.  <span data-ttu-id="f7527-130">Setup.exe 的應用程式會檢查 \_ MsiPromptForCD mutex。</span><span class="sxs-lookup"><span data-stu-id="f7527-130">The Setup.exe application checks for the \_MsiPromptForCD mutex.</span></span> <span data-ttu-id="f7527-131">Windows Installer 會在提示使用者插入 CD-ROM 時建立此 mutex。</span><span class="sxs-lookup"><span data-stu-id="f7527-131">Windows Installer creates this mutex when it prompts the user to insert the CD-ROM.</span></span> <span data-ttu-id="f7527-132">Mutex 是否存在指出 Windows Installer 正在執行已要求 Office 2000 CD-ROM 的安裝。</span><span class="sxs-lookup"><span data-stu-id="f7527-132">The presence of the mutex indicates that Windows Installer is running an installation that has requested the Office 2000 CD-ROM.</span></span> <span data-ttu-id="f7527-133">在此情況下，Setup.exe 的應用程式會立即結束，並允許 Office 2000 安裝繼續進行。</span><span class="sxs-lookup"><span data-stu-id="f7527-133">In this case, the Setup.exe application exits immediately and allows the Office 2000 installation to continue.</span></span> <span data-ttu-id="f7527-134">如果沒有 mutex，Setup.exe 的應用程式會繼續進行評估登錄機碼以判斷是否已安裝 Office 2000 的步驟3。</span><span class="sxs-lookup"><span data-stu-id="f7527-134">If the mutex is absent, the Setup.exe application continues at step 3 where a registry key is evaluated to determine if Office 2000 is installed.</span></span>
3.  <span data-ttu-id="f7527-135">Setup.exe 的應用程式會檢查 Office9 登錄機碼是否存在：</span><span class="sxs-lookup"><span data-stu-id="f7527-135">The Setup.exe application checks the presence of the Office9 registry key:</span></span>

    <span data-ttu-id="f7527-136">**HKCU/Software/Microsoft/Office/9.0/Common/General/InstallProductID**</span><span class="sxs-lookup"><span data-stu-id="f7527-136">**HKCU/Software/Microsoft/Office/9.0/Common/General/InstallProductID**</span></span>

    <span data-ttu-id="f7527-137">如果這個登錄機碼不存在，Setup.exe 的應用程式會在檢查作業系統的步驟6繼續進行，以判斷它是否符合安裝 Office 2000 的資格。</span><span class="sxs-lookup"><span data-stu-id="f7527-137">If this registry key does not exist, the Setup.exe application continues at step 6 where the operating system is checked to determine if it qualifies for the installation of Office 2000.</span></span>

4.  <span data-ttu-id="f7527-138">如果 Office 2000 登錄機碼存在，Setup.exe 的應用程式會藉由呼叫 [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea)來檢查目前的安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="f7527-138">If the Office 2000 registry key exists, the Setup.exe application checks the current installation state by calling [**MsiQueryProductState**](/windows/desktop/api/Msi/nf-msi-msiqueryproductstatea).</span></span> <span data-ttu-id="f7527-139">InstallState 預設值的傳回狀態 \_ 表示已安裝 office 2000，而 Setup.exe 應用程式會繼續執行步驟5，並在其中檢查 office 2000 以從來源執行。</span><span class="sxs-lookup"><span data-stu-id="f7527-139">A return state of InstallState\_Default indicates that Office 2000 is already installed and the Setup.exe application continues at step 5 where the Office 2000 is checked for run from source.</span></span>

    <span data-ttu-id="f7527-140">如果未安裝 Office 2000，Setup.exe 應用程式會在檢查作業系統的步驟6繼續進行，以判斷它是否符合安裝 Office 2000 的資格。</span><span class="sxs-lookup"><span data-stu-id="f7527-140">If Office 2000 is not installed, the Setup.exe application continues at step 6 where the operating system is checked to determine if it qualifies for the installation of Office 2000.</span></span>

5.  <span data-ttu-id="f7527-141">Setup.exe 的應用程式會針對每個 **\[ \] OfficeFeatures** 區段中的每一項功能呼叫 [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) ，以進行每個自動播放 .inf 檔案的功能。</span><span class="sxs-lookup"><span data-stu-id="f7527-141">The Setup.exe application calls [**MsiQueryFeatureState**](/windows/desktop/api/Msi/nf-msi-msiqueryfeaturestatea) for each of the features in the **\[OfficeFeatures\]** section of the Autorun.inf file.</span></span> <span data-ttu-id="f7527-142">如果其中任何一項功能傳回 INSTALLSTATE \_ 來源，這表示該功能正在從來源執行，而且 Setup.exe 應用程式會立即結束。</span><span class="sxs-lookup"><span data-stu-id="f7527-142">If any of these features returns INSTALLSTATE\_SOURCE, this indicates that the feature is being run from source and the Setup.exe application exits immediately.</span></span>

    <span data-ttu-id="f7527-143">如果沒有任何功能傳回 INSTALLSTATE \_ 來源，Setup.exe 應用程式會啟動安裝程式應用程式、Msiexec.exe，並在結束之前提供 Windows Installer 維護模式。</span><span class="sxs-lookup"><span data-stu-id="f7527-143">If none of the features returns INSTALLSTATE\_SOURCE, the Setup.exe application launches the installer application, Msiexec.exe, and presents the Windows Installer maintenance mode before exiting.</span></span>

6.  <span data-ttu-id="f7527-144">Setup.exe 的應用程式會判斷作業系統是否符合安裝 Office 2000 的資格。</span><span class="sxs-lookup"><span data-stu-id="f7527-144">The Setup.exe application determines whether the operating system qualifies for an installation of Office 2000.</span></span> <span data-ttu-id="f7527-145">需要 Windows XP 才能安裝 Office 2000。</span><span class="sxs-lookup"><span data-stu-id="f7527-145">Windows XP is required to install Office 2000.</span></span> <span data-ttu-id="f7527-146">如果作業系統需要 service pack 更新才能符合 Office 2000 的資格，Setup.exe 應用程式會顯示在 [自動播放] 檔案中指定的文字。</span><span class="sxs-lookup"><span data-stu-id="f7527-146">If the operating system requires a service pack update to qualify for Office 2000, the Setup.exe application displays the text specified in the Autorun.inf file.</span></span> <span data-ttu-id="f7527-147">如果作業系統不符合 Office 2000 或 Office 2000 升級的資格，Setup.exe 的應用程式會顯示一則訊息，讓使用者無法繼續。</span><span class="sxs-lookup"><span data-stu-id="f7527-147">If the operating system does not qualify for Office 2000 or an upgrade of Office 2000, the Setup.exe application displays a message that prevents the user from continuing.</span></span>

    <span data-ttu-id="f7527-148">如果作業系統符合 Office 2000 的資格，Setup.exe 的應用程式會繼續進行步驟7，判斷是否已在使用者的電腦上安裝 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="f7527-148">If the operating system qualifies for Office 2000, the Setup.exe application continues at step 7, which determines whether Windows Installer is installed on the user's computer.</span></span>

7.  <span data-ttu-id="f7527-149">如果使用者的電腦上有 Windows Installer，Setup.exe 應用程式就會啟動 Msiexec.exe 應用程式，並將 Office 2000 .msi 檔案傳遞給它。</span><span class="sxs-lookup"><span data-stu-id="f7527-149">If Windows Installer exists on the user's machine, the Setup.exe application launches the Msiexec.exe application and passes the Office 2000 .msi file to it.</span></span>

    <span data-ttu-id="f7527-150">如果本機電腦上未安裝 Windows Installer，Setup.exe 應用程式會繼續執行步驟8，判斷作業系統是否符合安裝 Windows Installer 的資格。</span><span class="sxs-lookup"><span data-stu-id="f7527-150">If Windows Installer is not installed on the local machine, the Setup.exe application continues at step 8, which determines whether the operating system qualifies to have Windows Installer installed.</span></span>

8.  <span data-ttu-id="f7527-151">如果本機電腦有資格安裝 Windows Installer，Setup.exe 應用程式會針對該平臺執行 Instmsi.exe 安裝程式應用程式的正確版本。</span><span class="sxs-lookup"><span data-stu-id="f7527-151">If the local computer is eligible to have Windows Installer installed, the Setup.exe application runs the correct version of the Instmsi.exe installer application for the platform.</span></span> <span data-ttu-id="f7527-152">Setup.exe 可以傳遞 "/q" 命令列參數來隱藏使用者介面，並防止使用者變更任何安裝設定選項。</span><span class="sxs-lookup"><span data-stu-id="f7527-152">Setup.exe may pass the "/q" command line switch to suppress the user interface and prevent the user from changing any installation configuration options.</span></span>
9.  <span data-ttu-id="f7527-153">Setup.exe 的應用程式會載入新安裝的 Msi.dll 檔案，並執行 [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) 函式的呼叫，以安裝使用者的應用程式。</span><span class="sxs-lookup"><span data-stu-id="f7527-153">The Setup.exe application loads the newly installed Msi.dll file and performs a call to the [**MsiInstallProduct**](/windows/desktop/api/Msi/nf-msi-msiinstallproducta) function to install the user's application.</span></span>

## <a name="setupexe-command-line-parameters"></a><span data-ttu-id="f7527-154">Setup.exe 命令列參數</span><span class="sxs-lookup"><span data-stu-id="f7527-154">Setup.exe Command Line Parameters</span></span>

<span data-ttu-id="f7527-155">Setup.exe 的應用程式可讓系統管理員和使用者將命令列選項傳遞至 Msiexec.exe 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f7527-155">The Setup.exe application enables administrators and users to pass command line options to the Msiexec.exe application.</span></span> <span data-ttu-id="f7527-156">如需詳細資訊，請參閱 [命令列選項](command-line-options.md)。</span><span class="sxs-lookup"><span data-stu-id="f7527-156">For more information, see [Command Line Options](command-line-options.md).</span></span> <span data-ttu-id="f7527-157">下表列出可搭配 Setup.exe 使用的命令選項。</span><span class="sxs-lookup"><span data-stu-id="f7527-157">The following table lists the command options that can be used with Setup.exe.</span></span>



| <span data-ttu-id="f7527-158">選項</span><span class="sxs-lookup"><span data-stu-id="f7527-158">Option</span></span>                       | <span data-ttu-id="f7527-159">使用方式</span><span class="sxs-lookup"><span data-stu-id="f7527-159">Usage</span></span>                                                                                                                                        | <span data-ttu-id="f7527-160">意義</span><span class="sxs-lookup"><span data-stu-id="f7527-160">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
|------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f7527-161">/autorun</span><span class="sxs-lookup"><span data-stu-id="f7527-161">/autorun</span></span>                     | <span data-ttu-id="f7527-162">setup.exe/autorun</span><span class="sxs-lookup"><span data-stu-id="f7527-162">setup.exe /autorun</span></span>                                                                                                                           | <span data-ttu-id="f7527-163">執行上面所述的執行 .inf。</span><span class="sxs-lookup"><span data-stu-id="f7527-163">Runs the Autorun.inf described above.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="f7527-164">/a</span><span class="sxs-lookup"><span data-stu-id="f7527-164">/a</span></span>                           | <span data-ttu-id="f7527-165">setup.exe /a</span><span class="sxs-lookup"><span data-stu-id="f7527-165">setup.exe /a</span></span>                                                                                                                                 | <span data-ttu-id="f7527-166">起始系統管理安裝。</span><span class="sxs-lookup"><span data-stu-id="f7527-166">Initiates an administrative installation.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f7527-167">/j</span><span class="sxs-lookup"><span data-stu-id="f7527-167">/j</span></span>                           | <span data-ttu-id="f7527-168">\[u \| m \] *套件* 或</span><span class="sxs-lookup"><span data-stu-id="f7527-168">\[u\|m\]*Package* or</span></span> <br/> <span data-ttu-id="f7527-169">\[u \| m \] *封裝*/t *轉換清單*</span><span class="sxs-lookup"><span data-stu-id="f7527-169">\[u\|m\]*Package* /t *Transform List*</span></span><br/> <span data-ttu-id="f7527-170">或</span><span class="sxs-lookup"><span data-stu-id="f7527-170">or</span></span> <br/> <span data-ttu-id="f7527-171">\[u \| m \] *套件*/g *LanguageID*</span><span class="sxs-lookup"><span data-stu-id="f7527-171">\[u\|m\]*Package* /g *LanguageID*</span></span><br/> | <span data-ttu-id="f7527-172">通告產品。</span><span class="sxs-lookup"><span data-stu-id="f7527-172">Advertises a product.</span></span> <span data-ttu-id="f7527-173">此選項會忽略在命令列上輸入的任何屬性值。</span><span class="sxs-lookup"><span data-stu-id="f7527-173">This option ignores any property values entered on the command line.</span></span> <span data-ttu-id="f7527-174">u 向目前的使用者通告。</span><span class="sxs-lookup"><span data-stu-id="f7527-174">u   Advertise to the current user.</span></span><br/> <span data-ttu-id="f7527-175">m 通告給電腦的所有使用者。</span><span class="sxs-lookup"><span data-stu-id="f7527-175">m   Advertise to all users of machine.</span></span><br/> <span data-ttu-id="f7527-176">g 語言識別項</span><span class="sxs-lookup"><span data-stu-id="f7527-176">g   Language identifier</span></span><br/> <span data-ttu-id="f7527-177">t 會將轉換套用至已公告的封裝。</span><span class="sxs-lookup"><span data-stu-id="f7527-177">t   Applies transform to advertised package.</span></span><br/>                                                                                                                                                                                                                        |
| <span data-ttu-id="f7527-178">/I</span><span class="sxs-lookup"><span data-stu-id="f7527-178">/I</span></span>                           | <span data-ttu-id="f7527-179">setup.exe/I Office9.msi/t ProgramMgmt .mst</span><span class="sxs-lookup"><span data-stu-id="f7527-179">setup.exe /I Office9.msi /t ProgramMgmt.mst</span></span>                                                                                                  | <span data-ttu-id="f7527-180">指定要安裝 Setup.exe 的 .msi 檔案。</span><span class="sxs-lookup"><span data-stu-id="f7527-180">Specifies the .msi file that Setup.exe is to install.</span></span> <span data-ttu-id="f7527-181">如果未包含/I 選項，Setup.exe 會使用 Office9.msi 檔。</span><span class="sxs-lookup"><span data-stu-id="f7527-181">If the /I option is not included, Setup.exe uses the Office9.msi file.</span></span>                                                                                                                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f7527-182">/o<*屬性* = *值*></span><span class="sxs-lookup"><span data-stu-id="f7527-182">/o<*property*=*value*></span></span> | <span data-ttu-id="f7527-183">setup.exe/o CDKEY = 111111-1111</span><span class="sxs-lookup"><span data-stu-id="f7527-183">setup.exe /o CDKEY=111111-1111</span></span>                                                                                                               | <span data-ttu-id="f7527-184">設定 .msi 檔案中的屬性。</span><span class="sxs-lookup"><span data-stu-id="f7527-184">Sets properties in the .msi file.</span></span> <span data-ttu-id="f7527-185">Setup.exe 將其傳遞至 msiexec （如撰寫）。</span><span class="sxs-lookup"><span data-stu-id="f7527-185">Setup.exe passes these it to msiexec as written.</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="f7527-186">/q</span><span class="sxs-lookup"><span data-stu-id="f7527-186">/q</span></span>                           | <span data-ttu-id="f7527-187">setup.exe/q</span><span class="sxs-lookup"><span data-stu-id="f7527-187">setup.exe /q</span></span>                                                                                                                                 | <span data-ttu-id="f7527-188">設定安裝的 UI 層級。</span><span class="sxs-lookup"><span data-stu-id="f7527-188">Set the UI level the installation.</span></span> <span data-ttu-id="f7527-189">/q 沒有適用于 msiexec 的 UI (/qn。 ) /qb 基本 UI</span><span class="sxs-lookup"><span data-stu-id="f7527-189">/q   no UI (/qn   for msiexec.) /qb   basic UI</span></span><br/> <span data-ttu-id="f7527-190">/qr 縮減的 UI。</span><span class="sxs-lookup"><span data-stu-id="f7527-190">/qr   reduced UI.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="f7527-191">一樣\#</span><span class="sxs-lookup"><span data-stu-id="f7527-191">/m\#</span></span>                         | <span data-ttu-id="f7527-192">setup.exe/m4</span><span class="sxs-lookup"><span data-stu-id="f7527-192">setup.exe /m4</span></span>                                                                                                                                | <span data-ttu-id="f7527-193">根據選取的協定支援多個授權。</span><span class="sxs-lookup"><span data-stu-id="f7527-193">Supports multiple licenses in accordance with Select agreements.</span></span> <span data-ttu-id="f7527-194">授權驗證自訂動作會使用這個屬性來寫入 LV 憑證。</span><span class="sxs-lookup"><span data-stu-id="f7527-194">This property is used in by the License Verification custom action to write the LV certificate.</span></span> <span data-ttu-id="f7527-195">/M 選項後面必須接著允許的解除鎖定數目。</span><span class="sxs-lookup"><span data-stu-id="f7527-195">The /m option must be followed by the number of unlocks allowed.</span></span> <span data-ttu-id="f7527-196">/M 選項指定的值應該設定為 Office9.msi 檔中的 "M" 屬性。</span><span class="sxs-lookup"><span data-stu-id="f7527-196">The value specified by the /m option should be set as the "M" property in the Office9.msi file.</span></span> <span data-ttu-id="f7527-197">如果未指定任何值，但使用/m 選項與安裝程式，則應該設定0的值。</span><span class="sxs-lookup"><span data-stu-id="f7527-197">If no value is specified, but the /m option is used with setup, the value of 0 should be set.</span></span> <span data-ttu-id="f7527-198">需要有/m 選項，才能支援使用 CD 或網路的選取客戶。</span><span class="sxs-lookup"><span data-stu-id="f7527-198">The /m option is required to support Select customers using a CD or network.</span></span> |
| <span data-ttu-id="f7527-199">/settings</span><span class="sxs-lookup"><span data-stu-id="f7527-199">/settings</span></span>                    | <span data-ttu-id="f7527-200">setup.exe/settings mysettings.ini</span><span class="sxs-lookup"><span data-stu-id="f7527-200">setup.exe /settings mysettings.ini</span></span>                                                                                                           | <span data-ttu-id="f7527-201">可讓系統管理員指定 .ini 檔案，其中包含要在 Office 2000 安裝期間傳遞的所有自訂設定。</span><span class="sxs-lookup"><span data-stu-id="f7527-201">Enables administrators to specify an .ini file containing all of the customized settings to be passed during Office 2000 setup.</span></span> <span data-ttu-id="f7527-202">請參閱以下 .ini 檔案的描述。</span><span class="sxs-lookup"><span data-stu-id="f7527-202">See the description of the .ini file below.</span></span>                                                                                                                                                                                                                                                                                                                                  |



 

## <a name="using-an-ini-file"></a><span data-ttu-id="f7527-203">使用 .ini 檔案</span><span class="sxs-lookup"><span data-stu-id="f7527-203">Using an .ini File</span></span>

<span data-ttu-id="f7527-204">建立初始化檔可能比建立長命令列更容易。</span><span class="sxs-lookup"><span data-stu-id="f7527-204">Creating an initialization file may be easier than creating a long command line.</span></span> <span data-ttu-id="f7527-205">使用/settings 選項，Setup.exe 應用程式會讀取指定的 .ini 檔，並建立命令列以傳遞至 Msiexec.exe 應用程式。</span><span class="sxs-lookup"><span data-stu-id="f7527-205">Using the /settings option, the Setup.exe application reads the specified .ini file and constructs a command line to pass to the Msiexec.exe application.</span></span> <span data-ttu-id="f7527-206">.Ini 檔只支援命令列支援的屬性。</span><span class="sxs-lookup"><span data-stu-id="f7527-206">Only properties supported on the command line are supported in the .ini file.</span></span> <span data-ttu-id="f7527-207">如果在 .ini 檔和命令列中都找到屬性或值，則命令列設定會覆寫 .ini 檔案設定。</span><span class="sxs-lookup"><span data-stu-id="f7527-207">If a property or value is found in both the .ini file and on the command line, the command line settings override the .ini file settings.</span></span>

<span data-ttu-id="f7527-208">.Ini 檔案的格式為：</span><span class="sxs-lookup"><span data-stu-id="f7527-208">The format of the .ini file is:</span></span>

<span data-ttu-id="f7527-209">\[微星\]</span><span class="sxs-lookup"><span data-stu-id="f7527-209">\[msi\]</span></span>

 

<span data-ttu-id="f7527-210">\[Mst\]</span><span class="sxs-lookup"><span data-stu-id="f7527-210">\[mst\]</span></span>

 

<span data-ttu-id="f7527-211">\[options\]</span><span class="sxs-lookup"><span data-stu-id="f7527-211">\[options\]</span></span>

 

<span data-ttu-id="f7527-212">\[顯示\]</span><span class="sxs-lookup"><span data-stu-id="f7527-212">\[Display\]</span></span>

<span data-ttu-id="f7527-213">.Ini 檔案的 \[ msi \] 區段會指定安裝安裝套件的路徑。</span><span class="sxs-lookup"><span data-stu-id="f7527-213">The \[msi\] section of the .ini file specifies the path to the installation package for the installation.</span></span> <span data-ttu-id="f7527-214">這會對應至命令列上的/I 選項。</span><span class="sxs-lookup"><span data-stu-id="f7527-214">This corresponds to the /I option on the command line.</span></span>

<span data-ttu-id="f7527-215">.Ini 檔案的 \[ mst \] 區段會指定此安裝所使用的轉換路徑。</span><span class="sxs-lookup"><span data-stu-id="f7527-215">The \[mst\] section of the .ini file specifies the path to transforms used with this installation.</span></span> <span data-ttu-id="f7527-216">這會對應至命令列上的/j 選項。</span><span class="sxs-lookup"><span data-stu-id="f7527-216">This corresponds to the /j option on the command line.</span></span> <span data-ttu-id="f7527-217">使用 MST1 MST (N) ，在不同的行上指出多個轉換。</span><span class="sxs-lookup"><span data-stu-id="f7527-217">Multiple transforms are each indicated on a different line, using MST1   MST(N).</span></span> <span data-ttu-id="f7527-218">當剖析為命令列時，.ini 檔案中的清單會從左至右轉換。</span><span class="sxs-lookup"><span data-stu-id="f7527-218">When parsed into the command line, the list in the .ini file is turned from left to right.</span></span> <span data-ttu-id="f7527-219">請注意，與 MST (N) 標題相關聯的數位只存在於維護唯一識別碼，而且沒有任何程式設計意義。</span><span class="sxs-lookup"><span data-stu-id="f7527-219">Note that the number associated with the MST(N) title is present only to maintain unique identifiers and has no programmatic meaning.</span></span>

<span data-ttu-id="f7527-220">\[選項 \] 區段可讓網路系統管理員設定及覆寫 .msi 或 .mst 檔案中的屬性。</span><span class="sxs-lookup"><span data-stu-id="f7527-220">The \[options\] section allows network administrators to set and override properties in the .msi or .mst files.</span></span> <span data-ttu-id="f7527-221">在 .ini 檔案中設定的選項會使用/o 選項新增至命令列。</span><span class="sxs-lookup"><span data-stu-id="f7527-221">Options set in the .ini file are added to the command line using the /o option.</span></span> <span data-ttu-id="f7527-222">選項區段中的每個選項都必須有屬性名稱和值。</span><span class="sxs-lookup"><span data-stu-id="f7527-222">Each option in the option section must have a property name and a value.</span></span>

<span data-ttu-id="f7527-223">[ \[ 顯示] \] 區段是用來設定安裝期間使用的使用者介面層級。</span><span class="sxs-lookup"><span data-stu-id="f7527-223">The \[Display\] section is used to set the user interface level used during setup.</span></span> <span data-ttu-id="f7527-224">這會對應至命令列上的/q 選項。</span><span class="sxs-lookup"><span data-stu-id="f7527-224">This corresponds to the /q option on the command line.</span></span> <span data-ttu-id="f7527-225">有效值為 [無]、[基本]、[已縮減] 和 [完整]。</span><span class="sxs-lookup"><span data-stu-id="f7527-225">Valid values are   none, basic, reduced, and full.</span></span>

<span data-ttu-id="f7527-226">範例 .ini 檔案</span><span class="sxs-lookup"><span data-stu-id="f7527-226">Sample .ini file</span></span>

<span data-ttu-id="f7527-227">\[MSI\]</span><span class="sxs-lookup"><span data-stu-id="f7527-227">\[MSI\]</span></span>

 

<span data-ttu-id="f7527-228">MSI = \\ \\ sourceshare \\ Office2000 \\Office2000.msi</span><span class="sxs-lookup"><span data-stu-id="f7527-228">MSI=\\\\sourceshare\\Office2000\\Office2000.msi</span></span>

 

<span data-ttu-id="f7527-229">\[Mst\]</span><span class="sxs-lookup"><span data-stu-id="f7527-229">\[MST\]</span></span>

 

<span data-ttu-id="f7527-230">MST1 = \\ \\ sourceshare \\ Office2000 \\ trns1 .mst</span><span class="sxs-lookup"><span data-stu-id="f7527-230">MST1=\\\\sourceshare\\Office2000\\trns1.mst</span></span>

 

<span data-ttu-id="f7527-231">MST2 = \\ \\ sourceshare \\ Office2000 \\ trns2 .mst</span><span class="sxs-lookup"><span data-stu-id="f7527-231">MST2=\\\\sourceshare\\Office2000\\trns2.mst</span></span>

 

<span data-ttu-id="f7527-232">\[選項\]</span><span class="sxs-lookup"><span data-stu-id="f7527-232">\[Options\]</span></span>

 

<span data-ttu-id="f7527-233">PUBLICPROPERTY = 您的值</span><span class="sxs-lookup"><span data-stu-id="f7527-233">PUBLICPROPERTY=your value</span></span>

<span data-ttu-id="f7527-234">\[顯示\]</span><span class="sxs-lookup"><span data-stu-id="f7527-234">\[Display\]</span></span>

 

<span data-ttu-id="f7527-235">顯示 = 無</span><span class="sxs-lookup"><span data-stu-id="f7527-235">Display=None</span></span>

 

