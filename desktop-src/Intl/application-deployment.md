---
description: 本節說明部署 MUI 應用程式以達到最佳應用程式載入邏輯和資源載入器使用的考慮。
ms.assetid: 6c10b355-9bdd-4dba-8446-91034d4fe9b8
title: 應用程式部署
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2023e5fc2dbde51a6ef996126e7557c9ffce8d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990505"
---
# <a name="application-deployment"></a><span data-ttu-id="246d5-103">應用程式部署</span><span class="sxs-lookup"><span data-stu-id="246d5-103">Application Deployment</span></span>

<span data-ttu-id="246d5-104">本節說明部署 MUI 應用程式以達到最佳應用程式載入邏輯和資源載入器使用的考慮。</span><span class="sxs-lookup"><span data-stu-id="246d5-104">This section describes considerations for deploying your MUI application for optimal use by the application loading logic and the resource loader.</span></span>

## <a name="packaging"></a><span data-ttu-id="246d5-105">包裝</span><span class="sxs-lookup"><span data-stu-id="246d5-105">Packaging</span></span>

<span data-ttu-id="246d5-106">應用程式的封裝取決於所提供的語言支援類型，因為 Windows 會根據使用者喜好設定來安裝語言套件。</span><span class="sxs-lookup"><span data-stu-id="246d5-106">Packaging for the application depends on the type of language support provided, as Windows installs language packs based on user preferences.</span></span> <span data-ttu-id="246d5-107">例如，如果您已決定支援系統語言設定，您可能會想要在單一套件中提供所有語言支援，不論所需的使用者為何。</span><span class="sxs-lookup"><span data-stu-id="246d5-107">For example, if you have decided on supporting system language settings, you might want to provide all language support in a single package, regardless of the intended user.</span></span>

<span data-ttu-id="246d5-108">如果應用程式和資源很大，您應該針對每個支援的語言使用一個套件。</span><span class="sxs-lookup"><span data-stu-id="246d5-108">If the application and resources are large, you should use one package per supported language.</span></span> <span data-ttu-id="246d5-109">比方說，如果您的應用程式呈現使用者可選取的語言，而且使用者需要動態新增和移除語言資源，您可能會使用此封裝類型。</span><span class="sxs-lookup"><span data-stu-id="246d5-109">For instance, you might use this packaging type if your application is presenting user-selectable languages and the user needs dynamic addition and removal of language resources.</span></span>

## <a name="file-placement-on-windows-vista-and-later"></a><span data-ttu-id="246d5-110">Windows Vista 和更新版本上的檔案放置</span><span class="sxs-lookup"><span data-stu-id="246d5-110">File Placement on Windows Vista and Later</span></span>

<span data-ttu-id="246d5-111">本節說明以 Windows Vista 和更新版本為目標的 MUI 應用程式檔案放置。</span><span class="sxs-lookup"><span data-stu-id="246d5-111">This section describes file placement for a MUI application targeted only at Windows Vista and later.</span></span>

### <a name="place-the-ln-file"></a><span data-ttu-id="246d5-112">放置 LN 檔案</span><span class="sxs-lookup"><span data-stu-id="246d5-112">Place the LN File</span></span>

<span data-ttu-id="246d5-113">MUI 應用程式的一般 LN 檔是 .exe 檔案或 .dll 檔案，例如 BakerDelta.dll。</span><span class="sxs-lookup"><span data-stu-id="246d5-113">A typical LN file for a MUI application is an .exe file or a .dll file, for example, BakerDelta.dll.</span></span> <span data-ttu-id="246d5-114">您應該將這個檔案放在您的應用程式安裝所在的根資料夾中，例如 X： \\ \\ <somepath> \\BakerDelta.dll。</span><span class="sxs-lookup"><span data-stu-id="246d5-114">You should place this file in the root folder where your application is installed, for example, X:\\\\<somepath>\\BakerDelta.dll.</span></span>

### <a name="place-language-specific-resource-files"></a><span data-ttu-id="246d5-115">放置 Language-Specific 資源檔</span><span class="sxs-lookup"><span data-stu-id="246d5-115">Place Language-Specific Resource Files</span></span>

<span data-ttu-id="246d5-116">特定語言的資源檔必須具有可預測的名稱，方法是將 "mui" 附加到 LN 檔案的完整名稱，例如 BakerDelta.dll mui。</span><span class="sxs-lookup"><span data-stu-id="246d5-116">Your language-specific resource files must have predictable names formed by appending ".mui" to the full name of the LN file, for example, BakerDelta.dll.mui.</span></span> <span data-ttu-id="246d5-117">這些檔案必須放在以適當 [語言名稱](language-names.md)命名的子資料夾中。</span><span class="sxs-lookup"><span data-stu-id="246d5-117">These files must be placed in subfolders named after the appropriate [language names](language-names.md).</span></span> <span data-ttu-id="246d5-118">下列範例會顯示 BakerDelta.dll LN 檔案的資源位置，以及英文的語言專屬資源檔 (英國) 、英文 (美國) 、中性英文、西班牙文 (西班牙) 、西班牙文 (墨西哥) 和中性西班牙文：</span><span class="sxs-lookup"><span data-stu-id="246d5-118">The following example shows placement of resources for the BakerDelta.dll LN file, with language-specific resource files for English (United Kingdom), English (United States), neutral English, Spanish (Spain), Spanish (Mexico), and neutral Spanish:</span></span>

-   <span data-ttu-id="246d5-119">X： \\ \\ <somepath> \\BakerDelta.dll</span><span class="sxs-lookup"><span data-stu-id="246d5-119">X:\\\\<somepath>\\BakerDelta.dll</span></span>
-   <span data-ttu-id="246d5-120">X： \\ \\ <somepath> \\ en-us \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-120">X:\\\\<somepath>\\en-GB\\BakerDelta.dll.mui</span></span>
-   <span data-ttu-id="246d5-121">X： \\ \\ <somepath> \\ en-us \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-121">X:\\\\<somepath>\\en-US\\BakerDelta.dll.mui</span></span>
-   <span data-ttu-id="246d5-122">X： \\ \\ <somepath> \\ en \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-122">X:\\\\<somepath>\\en\\BakerDelta.dll.mui</span></span>
-   <span data-ttu-id="246d5-123">X： \\ \\ <somepath> \\ es \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-123">X:\\\\<somepath>\\es-ES\\BakerDelta.dll.mui</span></span>
-   <span data-ttu-id="246d5-124">X： \\ \\ <somepath> \\ es-MX \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-124">X:\\\\<somepath>\\es-MX\\BakerDelta.dll.mui</span></span>
-   <span data-ttu-id="246d5-125">X： \\ \\ <somepath> \\ es \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-125">X:\\\\<somepath>\\es\\BakerDelta.dll.mui</span></span>

<span data-ttu-id="246d5-126">資源檔必須放在安裝 MUI 應用程式或語言套件期間的正確位置。</span><span class="sxs-lookup"><span data-stu-id="246d5-126">The resource files must be placed in their correct locations during installation of the MUI application or a language package.</span></span> <span data-ttu-id="246d5-127">請務必將每個檔案放在正確的資料夾中，否則資源載入器無法正常運作。</span><span class="sxs-lookup"><span data-stu-id="246d5-127">It is important to place each file in the correct folder, as the resource loader cannot operate properly otherwise.</span></span> <span data-ttu-id="246d5-128">使用上述範例，資源載入器會檢查 X： \\ <somepath> \\ en-us \\BakerDelta.dll 的英文 (美國) 資源。</span><span class="sxs-lookup"><span data-stu-id="246d5-128">Using the example above, the resource loader examines X:\\<somepath>\\en-US\\BakerDelta.dll.mui for English (United States) resources.</span></span> <span data-ttu-id="246d5-129">如果載入器會查看該檔案，而且只會遇到西班牙文語言的資源，則會失敗。</span><span class="sxs-lookup"><span data-stu-id="246d5-129">If the loader looks in that file and encounters only Spanish-language resources, it fails.</span></span>

## <a name="file-placement-on-a-pre-windows-vista-operating-system"></a><span data-ttu-id="246d5-130">Windows Vista 前版作業系統上的檔案放置</span><span class="sxs-lookup"><span data-stu-id="246d5-130">File Placement on a Pre-Windows Vista Operating System</span></span>

<span data-ttu-id="246d5-131">在 Windows Vista 之前的作業系統上執行的應用程式可以使用 Windows Vista 慣例，將語言特定的資源檔放在以語言名稱為基礎的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="246d5-131">An application to run on a pre-Windows Vista operating system can use the Windows Vista convention of placing language-specific resource files in folders based on language names.</span></span> <span data-ttu-id="246d5-132">或者，應用程式可以符合從 [語言識別項](language-identifiers.md)形成路徑的較舊慣例。</span><span class="sxs-lookup"><span data-stu-id="246d5-132">Alternatively, the application can conform to an older convention that forms paths from [language identifiers](language-identifiers.md).</span></span> <span data-ttu-id="246d5-133">針對僅支援單一語言的應用程式，您可以將特定語言的資源檔放在具有二進位檔案的根目錄中。</span><span class="sxs-lookup"><span data-stu-id="246d5-133">For applications that only support a single language, you can just place the language-specific resource file in the root directory with the binary file.</span></span>

<span data-ttu-id="246d5-134">例如，假設有一個名為 BakerDelta.dll 的 LN 檔案，其中包含英文 (英國) 的語言特定資源檔、英文 (美國) 、中性英文、西班牙文 (西班牙) 、西班牙文 (墨西哥) 和中性西班牙文。</span><span class="sxs-lookup"><span data-stu-id="246d5-134">For example, consider an LN file called BakerDelta.dll, with language-specific resource files for English (United Kingdom), English (United States), neutral English, Spanish (Spain), Spanish (Mexico), and neutral Spanish.</span></span> <span data-ttu-id="246d5-135">在 Windows Vista 前版作業系統上安裝可能會將這些檔案放在下面，如下所示：</span><span class="sxs-lookup"><span data-stu-id="246d5-135">An installation on a pre-Windows Vista operating system might place these files as follows:</span></span>

-   <span data-ttu-id="246d5-136">X： \\ \\ <somepath> \\BakerDelta.dll</span><span class="sxs-lookup"><span data-stu-id="246d5-136">X:\\\\<somepath>\\BakerDelta.dll</span></span>
-   <span data-ttu-id="246d5-137">X： \\ \\ <somepath> \\BakerDelta.dll mui (選用的 mui 檔案，其中包含作業系統語言的資源，作為最終的回溯) </span><span class="sxs-lookup"><span data-stu-id="246d5-137">X:\\\\<somepath>\\BakerDelta.dll.mui (optional .mui file containing resources in the language of the operating system as the ultimate fallback)</span></span>
-   <span data-ttu-id="246d5-138">X： \\ \\ <somepath> \\ mui \\ 0809 \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-138">X:\\\\<somepath>\\MUI\\0809\\BakerDelta.dll.mui</span></span>
-   <span data-ttu-id="246d5-139">X： \\ \\ <somepath> \\ mui \\ 0409 \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-139">X:\\\\<somepath>\\MUI\\0409\\BakerDelta.dll.mui</span></span>
-   <span data-ttu-id="246d5-140">X： \\ \\ <somepath> \\ mui \\ 0209 \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-140">X:\\\\<somepath>\\MUI\\0209\\BakerDelta.dll.mui</span></span>
-   <span data-ttu-id="246d5-141">X： \\ \\ <somepath> \\ mui \\ 040a \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-141">X:\\\\<somepath>\\MUI\\040a\\BakerDelta.dll.mui</span></span>
-   <span data-ttu-id="246d5-142">X： \\ \\ <somepath> \\ mui \\ 080a \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-142">X:\\\\<somepath>\\MUI\\080a\\BakerDelta.dll.mui</span></span>
-   <span data-ttu-id="246d5-143">X： \\ \\ <somepath> \\ mui \\ 0209 \\BakerDelta.dll mui</span><span class="sxs-lookup"><span data-stu-id="246d5-143">X:\\\\<somepath>\\MUI\\0209\\BakerDelta.dll.mui</span></span>

<span data-ttu-id="246d5-144">除了這些檔案之外，應用程式也可以設定絕佳的回溯語言專屬資源檔，與應用程式本身位於相同的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="246d5-144">In addition to these files, the application can set up an ultimate fallback language-specific resource file, to reside in the same folder as the application itself.</span></span> <span data-ttu-id="246d5-145">在上述範例中，這個檔案是 X： \\ <somepath> \\BakerDelta.dll 的 mui。</span><span class="sxs-lookup"><span data-stu-id="246d5-145">For the above example, this file is X:\\<somepath>\\BakerDelta.dll.mui.</span></span>

## <a name="installation"></a><span data-ttu-id="246d5-146">安裝</span><span class="sxs-lookup"><span data-stu-id="246d5-146">Installation</span></span>

<span data-ttu-id="246d5-147">複製和設定應用程式檔的安裝邏輯依賴支援的語言，以及語言資源檔在正確安裝位置的位置。</span><span class="sxs-lookup"><span data-stu-id="246d5-147">Installation logic for copying and setting up application files relies on the supported languages and the location of language resource files in the correct install locations.</span></span> <span data-ttu-id="246d5-148">安裝程式必須安裝並設定應用程式，讓使用者可以輕鬆地新增和移除語言。</span><span class="sxs-lookup"><span data-stu-id="246d5-148">An installer must install and set up the application so that the user can easily add and remove languages.</span></span>

<span data-ttu-id="246d5-149">如果您的應用程式只安裝目標作業系統的語言，安裝程式必須偵測作業系統使用者介面，以判斷要安裝的應用程式資源。</span><span class="sxs-lookup"><span data-stu-id="246d5-149">If your application simply installs the language of the target operating system, the installer must detect the operating system user interface to determine the application resources to install.</span></span> <span data-ttu-id="246d5-150">為了支援最佳的使用者體驗，安裝程式也應該偵測使用者介面語言，為安裝本身提供當地語系化的使用者介面。</span><span class="sxs-lookup"><span data-stu-id="246d5-150">To support the best user experience, the installer should also detect the user interface language to present a localized user interface for the installation itself.</span></span>

<span data-ttu-id="246d5-151">建議使用 Windows Installer (MSI) 來建立您的安裝軟體。</span><span class="sxs-lookup"><span data-stu-id="246d5-151">It is recommended to use Windows Installer (MSI) to create your installation software.</span></span> <span data-ttu-id="246d5-152">相關聯的資源應該包含在基礎語言資源檔中，如 [建立基礎語言資源檔](creating-the-base-language-resource-file.md)中所述。</span><span class="sxs-lookup"><span data-stu-id="246d5-152">Associated resources should be included in the base language resource file, as described in [Creating the Base Language Resource File](creating-the-base-language-resource-file.md).</span></span> <span data-ttu-id="246d5-153">如需使用 MSI 來準備應用程式安裝程式的指示，請參閱 [Windows Installer](../msi/windows-installer-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="246d5-153">For instructions on using MSI to prepare the application installer, see [Windows Installer](../msi/windows-installer-portal.md).</span></span>

## <a name="uninstall-program"></a><span data-ttu-id="246d5-154">卸載程式</span><span class="sxs-lookup"><span data-stu-id="246d5-154">Uninstall Program</span></span>

<span data-ttu-id="246d5-155">您也可能想要使用您的 MUI 應用程式來提供卸載程式。</span><span class="sxs-lookup"><span data-stu-id="246d5-155">You might also want to furnish an uninstall program with your MUI application.</span></span> <span data-ttu-id="246d5-156">也建議您建立此程式的 MSI。</span><span class="sxs-lookup"><span data-stu-id="246d5-156">MSI is also recommended for creation of this program.</span></span> <span data-ttu-id="246d5-157">如需使用 MSI 準備卸載軟體的指示，請參閱 [Windows Installer](../msi/windows-installer-portal.md)。</span><span class="sxs-lookup"><span data-stu-id="246d5-157">For instructions on using MSI to prepare the uninstall software, see [Windows Installer](../msi/windows-installer-portal.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="246d5-158">相關主題</span><span class="sxs-lookup"><span data-stu-id="246d5-158">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="246d5-159">使用多語系消費者介面</span><span class="sxs-lookup"><span data-stu-id="246d5-159">Using Multilingual User Interface</span></span>](using-multilingual-user-interface.md)
</dt> </dl>

 

 
