---
description: 若要將啟用筆墨的應用程式散發到未執行 Windows Vista 或 Windows XP Tablet PC Edition 2005 (也就是執行 Windows XP、Windows Server 2003 或 Windows 2000) 的電腦，您必須在安裝程式中包含必要的合併模組。
ms.assetid: 97515703-0bf4-4230-ae35-181b48b70c40
title: 建立可轉散發安裝程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1ad9b9ec8b10032d4a2bb44cca52e5c2f4178b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510757"
---
# <a name="creating-a-redistributable-setup"></a><span data-ttu-id="d5ef6-103">建立可轉散發安裝程式</span><span class="sxs-lookup"><span data-stu-id="d5ef6-103">Creating a Redistributable Setup</span></span>

<span data-ttu-id="d5ef6-104">若要將啟用筆墨的應用程式散發到未執行 Windows Vista 或 Windows XP Tablet PC Edition 2005 (也就是執行 Windows XP、Windows Server 2003 或 Windows 2000) 的電腦，您必須在安裝程式中包含必要的合併模組。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-104">To distribute an ink-enabled application to computers that are not running either Windows Vista or Windows XP Tablet PC Edition 2005 (that is, computers running Windows XP, Windows Server 2003, or Windows 2000), you must include the necessary merge modules in your setup.</span></span>

<span data-ttu-id="d5ef6-105">Mstpcrt .msm merge 模組包含 Windows Installer 安裝共用檔案所需的所有檔案、資源、登錄專案和安裝程式邏輯，而其他平臺需要這些檔案才能執行針對 Tablet PC 開發的非受控應用程式。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-105">The Mstpcrt.msm merge module includes all of the files, resources, registry entries, and setup logic necessary for Windows Installer to install the shared files that other platforms require to run unmanaged applications developed for the Tablet PC.</span></span> <span data-ttu-id="d5ef6-106">Windows Installer ( .msi) 檔會使用 Mstpcrt。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-106">Mstpcrt.msm is consumed by Windows Installer (.msi) files.</span></span> <span data-ttu-id="d5ef6-107">若為使用 [**InkDivider**](inkdivider-class.md) 物件的應用程式，您也必須轉散發 InkDiv .msm。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-107">For applications that use the [**InkDivider**](inkdivider-class.md) object, you must also redistribute InkDiv.msm.</span></span> <span data-ttu-id="d5ef6-108">針對使用 managed 元件的應用程式，您也必須包含這些受管理元件的合併模組檔案。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-108">For applications that use managed components, you must also include the merge module files for those managed components.</span></span>

<span data-ttu-id="d5ef6-109">下表說明 Windows XP Tablet PC Edition 軟體發展工具組 (SDK) 隨附的合併模組檔案。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-109">The following table describes the merge module files that ship with the Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>



| <span data-ttu-id="d5ef6-110">可轉散發合併模組</span><span class="sxs-lookup"><span data-stu-id="d5ef6-110">Redistributable Merge Module</span></span> | <span data-ttu-id="d5ef6-111">Description</span><span class="sxs-lookup"><span data-stu-id="d5ef6-111">Description</span></span>                                                                                                                    | <span data-ttu-id="d5ef6-112">檔案</span><span class="sxs-lookup"><span data-stu-id="d5ef6-112">Files</span></span>                                                       |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="d5ef6-113">InkDiv .msm</span><span class="sxs-lookup"><span data-stu-id="d5ef6-113">InkDiv.msm</span></span><br/>        | <span data-ttu-id="d5ef6-114">安裝 [**InkDivider**](inkdivider-class.md) 物件的非受控版本。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-114">Installs the unmanaged version of the [**InkDivider**](inkdivider-class.md) object.</span></span><br/>                                | <span data-ttu-id="d5ef6-115">InkDiv.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-115">InkDiv.dll</span></span><br/>                                       |
| <span data-ttu-id="d5ef6-116">Mstpcrt .msm</span><span class="sxs-lookup"><span data-stu-id="d5ef6-116">Mstpcrt.msm</span></span><br/>       | <span data-ttu-id="d5ef6-117">安裝 Tablet PC Platform 版本1.0 的非受控元件。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-117">Installs the unmanaged components of the Tablet PC Platform version 1.0.</span></span><br/>                                            | <span data-ttu-id="d5ef6-118">Gdiplus.dll、InkEd.dll、Tpcps.dll、Wisptis.exe</span><span class="sxs-lookup"><span data-stu-id="d5ef6-118">Gdiplus.dll, InkEd.dll, Tpcps.dll, Wisptis.exe</span></span><br/>   |
| <span data-ttu-id="d5ef6-119">Msvcp60 .msm</span><span class="sxs-lookup"><span data-stu-id="d5ef6-119">Msvcp60.msm</span></span><br/>       | <span data-ttu-id="d5ef6-120">安裝 Microsoft Visual C++ runtime 的元件。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-120">Installs components of the Microsoft Visual C++ runtime.</span></span><br/>                                                            | <span data-ttu-id="d5ef6-121">Msvcp60.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-121">Msvcp60.dll</span></span><br/>                                      |
| <span data-ttu-id="d5ef6-122">Msvcrt.lib .msm</span><span class="sxs-lookup"><span data-stu-id="d5ef6-122">Msvcrt.msm</span></span><br/>        | <span data-ttu-id="d5ef6-123">安裝 Microsoft Visual C runtime 的元件。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-123">Installs components of the Microsoft Visual C runtime.</span></span><br/>                                                              | <span data-ttu-id="d5ef6-124">Msvcrt.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-124">Msvcrt.dll</span></span><br/>                                       |
| <span data-ttu-id="d5ef6-125">Tpcman17 .msm</span><span class="sxs-lookup"><span data-stu-id="d5ef6-125">Tpcman17.msm</span></span><br/>      | <span data-ttu-id="d5ef6-126">安裝 Tablet PC 平臺執行時間的 managed 元件。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-126">Installs the managed components of the Tablet PC Platform runtime.</span></span> <span data-ttu-id="d5ef6-127">需要安裝 mstpcrt .msm 檔。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-127">Requires that the mstpcrt.msm file is installed.</span></span><br/> | <span data-ttu-id="d5ef6-128">Microsoft.Ink.dll，Microsoft.Ink.resources.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-128">Microsoft.Ink.dll, Microsoft.Ink.resources.dll</span></span><br/>   |
| <span data-ttu-id="d5ef6-129">iaCOM .msm</span><span class="sxs-lookup"><span data-stu-id="d5ef6-129">iaCOM.msm</span></span><br/>         | <span data-ttu-id="d5ef6-130">安裝 InkAnalysis API 的自動化元件。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-130">Installs the Automation components of the InkAnalysis API.</span></span><br/>                                                          | <span data-ttu-id="d5ef6-131">IACom.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-131">IACom.dll</span></span><br/>                                        |
| <span data-ttu-id="d5ef6-132">iacore .msm</span><span class="sxs-lookup"><span data-stu-id="d5ef6-132">iacore.msm</span></span><br/>        | <span data-ttu-id="d5ef6-133">安裝 InkAnalysis API 的基本類別元件。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-133">Installs the base class components of the InkAnalysis API.</span></span><br/>                                                          | <span data-ttu-id="d5ef6-134">IACore.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-134">IACore.dll</span></span><br/> <span data-ttu-id="d5ef6-135">IALoader.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-135">IALoader.dll</span></span><br/>               |
| <span data-ttu-id="d5ef6-136">IAWinFrm .msm</span><span class="sxs-lookup"><span data-stu-id="d5ef6-136">IAWinFrm.msm</span></span><br/>      | <span data-ttu-id="d5ef6-137">安裝 InkAnalysis API 的 managed 程式庫元件。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-137">Installs the managed library components of the InkAnalysis API.</span></span><br/>                                                     | <span data-ttu-id="d5ef6-138">Microsoft.Ink.Analysis.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-138">Microsoft.Ink.Analysis.dll</span></span><br/>                       |
| <span data-ttu-id="d5ef6-139">IAWinFX .msm</span><span class="sxs-lookup"><span data-stu-id="d5ef6-139">IAWinFX.msm</span></span><br/>       | <span data-ttu-id="d5ef6-140">安裝 InkAnalysis API 的 Windows Presentation Foundation 元件。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-140">Installs the Windows Presentation Foundation components of the InkAnalysis API.</span></span><br/>                                     | <span data-ttu-id="d5ef6-141">IAWinFX.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-141">IAWinFX.dll</span></span><br/>                                      |
| <span data-ttu-id="d5ef6-142">日誌 .msm</span><span class="sxs-lookup"><span data-stu-id="d5ef6-142">journal.msm</span></span><br/>       | <span data-ttu-id="d5ef6-143">安裝「日誌讀取器」元件。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-143">Installs the Journal Reader components.</span></span><br/>                                                                             | <span data-ttu-id="d5ef6-144">Journal.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-144">Journal.dll</span></span><br/> <span data-ttu-id="d5ef6-145">Microsoft.ink.journal.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-145">Microsoft.ink.journal.dll</span></span><br/> |
| <span data-ttu-id="d5ef6-146">rtscom .msm</span><span class="sxs-lookup"><span data-stu-id="d5ef6-146">rtscom.msm</span></span><br/>        | <span data-ttu-id="d5ef6-147">安裝 StylusInput 命名空間的自動化元件。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-147">Installs the Automation components of the StylusInput namespace.</span></span><br/>                                                    | <span data-ttu-id="d5ef6-148">Rtscom.dll</span><span class="sxs-lookup"><span data-stu-id="d5ef6-148">Rtscom.dll</span></span><br/>                                       |



 

> [!Note]  
> <span data-ttu-id="d5ef6-149">若要使用受管理元件合併模組中包含的 Microsoft .NET Framework 功能，您必須已在目的電腦上安裝此架構的 Service Pack 2。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-149">To use the functionality of the Microsoft .NET Framework that is included in merge modules for managed components, you must have installed Service Pack 2 of the Framework on the target computer.</span></span>

 

## <a name="reduced-feature-set"></a><span data-ttu-id="d5ef6-150">縮減功能集</span><span class="sxs-lookup"><span data-stu-id="d5ef6-150">Reduced Feature Set</span></span>

<span data-ttu-id="d5ef6-151">啟用筆墨的應用程式會將滑鼠事件視為畫筆移動，以模擬使用 tablet 畫筆。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-151">Ink-enabled applications treat mouse events as pen movements to simulate working with a tablet pen.</span></span> <span data-ttu-id="d5ef6-152">使用者可以新增筆跡、清除筆跡和儲存筆跡檔。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-152">Users can add ink, erase ink, and save ink documents.</span></span> <span data-ttu-id="d5ef6-153">但是，不是執行 Windows XP Tablet PC Edition 的使用者無法使用辨識和手勢。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-153">However, recognition and gestures are not available for users other than those running Windows XP Tablet PC Edition.</span></span>

<span data-ttu-id="d5ef6-154">Mstpcrt 不包含 Windows 筆記本或 Tablet PC 輸入面板。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-154">Mstpcrt.msm does not include Windows Journal or Tablet PC Input Panel.</span></span>

<span data-ttu-id="d5ef6-155">[**PenInputPanel**](peninputpanel-class.md)物件無法在 Windows XP Tablet PC Edition 以外的任何作業系統上運作。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-155">The [**PenInputPanel**](peninputpanel-class.md) object does not function on any operating systems besides Windows XP Tablet PC Edition.</span></span>

## <a name="deployment"></a><span data-ttu-id="d5ef6-156">部署</span><span class="sxs-lookup"><span data-stu-id="d5ef6-156">Deployment</span></span>

> [!Note]  
> <span data-ttu-id="d5ef6-157">如果您的應用程式使用 managed 程式碼，您也必須部署架構。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-157">If your application uses managed code, you must also deploy the Framework.</span></span> <span data-ttu-id="d5ef6-158">安裝 Tablet PC 受管理的元件之前，必須先安裝此架構。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-158">The Framework must be installed before your Tablet PC managed assemblies are installed.</span></span>

 

<span data-ttu-id="d5ef6-159">若要將 Mstpcrt 包含在 Microsoft Visual Studio .NET 安裝專案中：</span><span class="sxs-lookup"><span data-stu-id="d5ef6-159">To include Mstpcrt.msm in a Microsoft Visual Studio .NET Setup project:</span></span>

1.  <span data-ttu-id="d5ef6-160">在 [方案總管中，選取您的安裝專案。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-160">In the Solution Explorer, select your Setup project.</span></span>
2.  <span data-ttu-id="d5ef6-161">在 [專案] 功能表上，按一下 [ **加入**]，然後按一下 [ **合併模組**]。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-161">On the Project menu, click **Add**, and then click **Merge Module**.</span></span>
    > [!Note]  
    > <span data-ttu-id="d5ef6-162">您也可以用滑鼠右鍵按一下 [方案總管中的安裝程式專案名稱，按一下 [**加入**]，然後選取 [**合併模組**]，以連線到 [**加入模組**] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-162">You can also reach the **Add Modules** dialog box by right-clicking the installer project name in the Solution Explorer, clicking **Add**, and then selecting **Merge Module**.</span></span>

     

3.  <span data-ttu-id="d5ef6-163">在 [ **新增模組** ] 對話方塊中，流覽至並選取 [ **Mstpcrt**]。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-163">In the **Add Modules** dialog box, navigate to and select **Mstpcrt.msm**.</span></span>
4.  <span data-ttu-id="d5ef6-164">按一下 [開啟]。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-164">Click **Open**.</span></span>

<span data-ttu-id="d5ef6-165">Mstpcrt 會加入至您的安裝專案，並顯示在方案總管視窗中。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-165">Mstpcrt.msm is added to your Setup project and appears in the Solution Explorer window.</span></span>

<span data-ttu-id="d5ef6-166">Windows Installer 將合併模組中包含的檔案新增至 Program Files 資料夾。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-166">Windows Installer adds the files contained in the merge module to the Program Files folder.</span></span> <span data-ttu-id="d5ef6-167">若要使用這些檔案，終端使用者必須使用可存取 [Program Files] 資料夾的帳戶登入。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-167">To use these files, end users must be logged on with an account that has access to the Program Files folder.</span></span>

> [!Note]  
> <span data-ttu-id="d5ef6-168">您必須將 [SelfRegModules 動作](../msi/selfregmodules-action.md) 和 [SelfUnregModules 動作](../msi/selfunregmodules-action.md) 動作新增至安裝順序。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-168">You must add [SelfRegModules Action](../msi/selfregmodules-action.md) and [SelfUnregModules Action](../msi/selfunregmodules-action.md) actions to the installation sequence.</span></span> <span data-ttu-id="d5ef6-169">[MsiPublishAssemblies 動作](../msi/msipublishassemblies-action.md)和[MsiUnpublishAssemblies 動作](/windows/desktop/Msi/msiunpublishassemblies-action)動作會從這些動作的安裝順序中收到其順序。</span><span class="sxs-lookup"><span data-stu-id="d5ef6-169">The [MsiPublishAssemblies Action](../msi/msipublishassemblies-action.md) and [MsiUnpublishAssemblies Action](/windows/desktop/Msi/msiunpublishassemblies-action) actions receive their order in the installation sequence from these actions.</span></span>

 

 

