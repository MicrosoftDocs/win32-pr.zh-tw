---
description: 如果在執行安裝之後，您必須確認已安裝特定功能、元件或檔案，請在安裝期間開啟詳細資訊記錄選項。 請參閱 Windows Installer 記錄和命令列選項。
ms.assetid: c4547e5d-ea71-494f-9d92-c7fef23bcc0f
title: 檢查功能、元件、檔案的安裝
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7cab15b4f0590ee5613865d4b7c21439eec6dbc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979769"
---
# <a name="checking-the-installation-of-features-components-files"></a><span data-ttu-id="f3a1e-104">檢查功能、元件、檔案的安裝</span><span class="sxs-lookup"><span data-stu-id="f3a1e-104">Checking the Installation of Features, Components, Files</span></span>

<span data-ttu-id="f3a1e-105">如果在執行安裝之後，您必須確認已安裝特定功能、元件或檔案，請在安裝期間開啟詳細資訊記錄選項。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-105">If after running an installation, you need to verify that a particular feature, component, or file has been installed, turn on the verbose logging option during the installation.</span></span> <span data-ttu-id="f3a1e-106">請參閱 [Windows Installer 記錄](windows-installer-logging.md) 和 [命令列選項](command-line-options.md)。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-106">See [Windows Installer Logging](windows-installer-logging.md) and [Command Line Options](command-line-options.md).</span></span>

<span data-ttu-id="f3a1e-107">詳細資訊記錄檔包含安裝套件可能安裝的每個功能和元件的專案。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-107">The verbose log includes an entry for each feature and component the installation package may install.</span></span> <span data-ttu-id="f3a1e-108">記錄檔會指出該功能或元件在安裝之前的狀態、安裝所要求的狀態，以及安裝程式離開功能或元件的狀態。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-108">The log tells what the state of that feature or component was prior to the installation, what state was requested by the installation, and in what state the installer left the feature or component.</span></span> <span data-ttu-id="f3a1e-109">記錄檔中的功能和元件專案會顯示為下列範例。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-109">Feature and component entries in the log appear as the following examples.</span></span>

``` syntax
MSI (s) (40:A4): Feature: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
MSI (s) (40:A4): Component: QuickTest; Installed: Absent;   Request:
 Local;   Action: Local
```

<span data-ttu-id="f3a1e-110">此詳細資訊記錄檔指出：</span><span class="sxs-lookup"><span data-stu-id="f3a1e-110">This verbose log indicates that:</span></span>

-   <span data-ttu-id="f3a1e-111">執行封裝之前，QuickTest 功能和元件的安裝狀態不存在</span><span class="sxs-lookup"><span data-stu-id="f3a1e-111">the installation state of the QuickTest feature and component was absent before running the package</span></span>
-   <span data-ttu-id="f3a1e-112">套件要求本機安裝這些</span><span class="sxs-lookup"><span data-stu-id="f3a1e-112">the package requested a local installation of these</span></span>
-   <span data-ttu-id="f3a1e-113">在執行封裝之後，功能和元件都會保持在本機安裝的狀態。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-113">the feature and component were both left in the locally installed state after running the package.</span></span>

<span data-ttu-id="f3a1e-114">記錄檔中的「已安裝」標籤是指功能或元件目前的安裝狀態，「要求」指的是功能或元件的要求安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-114">The label "Installed" in the log refers to the current install state of the feature or component, "Request" refers to the requested install state of the feature or component.</span></span> <span data-ttu-id="f3a1e-115">「動作」是指功能或元件的實際動作狀態。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-115">"Action" refers to the actual action state of the feature or component.</span></span>

<span data-ttu-id="f3a1e-116">下表列出可能出現在記錄檔中的元件或功能狀態。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-116">The following table lists the possible component or feature states that can appear in the log.</span></span>



| <span data-ttu-id="f3a1e-117">記錄項目</span><span class="sxs-lookup"><span data-stu-id="f3a1e-117">Log Entry</span></span>              | <span data-ttu-id="f3a1e-118">Description</span><span class="sxs-lookup"><span data-stu-id="f3a1e-118">Description</span></span>                                                                                                     |
|------------------------|-----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3a1e-119">要求： Null</span><span class="sxs-lookup"><span data-stu-id="f3a1e-119">Request: Null</span></span>          | <span data-ttu-id="f3a1e-120">沒有要求。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-120">No request.</span></span>                                                                                                     |
| <span data-ttu-id="f3a1e-121">Action： Null</span><span class="sxs-lookup"><span data-stu-id="f3a1e-121">Action: Null</span></span>           | <span data-ttu-id="f3a1e-122">未採取任何動作。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-122">No action taken.</span></span>                                                                                                |
| <span data-ttu-id="f3a1e-123">已安裝：不存在</span><span class="sxs-lookup"><span data-stu-id="f3a1e-123">Installed: Absent</span></span>      | <span data-ttu-id="f3a1e-124">目前未安裝元件或功能。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-124">Component or feature is not currently installed.</span></span>                                                                |
| <span data-ttu-id="f3a1e-125">要求：不存在</span><span class="sxs-lookup"><span data-stu-id="f3a1e-125">Request: Absent</span></span>        | <span data-ttu-id="f3a1e-126">安裝要求元件或功能已卸載。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-126">Installation requests component or feature be uninstalled.</span></span>                                                      |
| <span data-ttu-id="f3a1e-127">動作：不存在</span><span class="sxs-lookup"><span data-stu-id="f3a1e-127">Action: Absent</span></span>         | <span data-ttu-id="f3a1e-128">安裝程式會實際卸載元件或功能。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-128">Installer actually uninstalls component or feature.</span></span>                                                             |
| <span data-ttu-id="f3a1e-129">已安裝：本機</span><span class="sxs-lookup"><span data-stu-id="f3a1e-129">Installed: Local</span></span>       | <span data-ttu-id="f3a1e-130">目前已安裝元件或功能以執行本機。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-130">Component or feature is currently installed to run local.</span></span>                                                       |
| <span data-ttu-id="f3a1e-131">要求：本機</span><span class="sxs-lookup"><span data-stu-id="f3a1e-131">Request: Local</span></span>         | <span data-ttu-id="f3a1e-132">安裝要求元件或功能可在本機執行。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-132">Installation requests component or feature be installed to run local.</span></span>                                           |
| <span data-ttu-id="f3a1e-133">動作：本機</span><span class="sxs-lookup"><span data-stu-id="f3a1e-133">Action: Local</span></span>          | <span data-ttu-id="f3a1e-134">安裝程式會實際安裝元件或功能以執行本機。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-134">Installer actually installs component or feature to run local.</span></span>                                                  |
| <span data-ttu-id="f3a1e-135">已安裝：來源</span><span class="sxs-lookup"><span data-stu-id="f3a1e-135">Installed: Source</span></span>      | <span data-ttu-id="f3a1e-136">元件或功能目前已安裝成從來源執行。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-136">Component or feature is currently installed to run from source.</span></span>                                                 |
| <span data-ttu-id="f3a1e-137">要求：來源</span><span class="sxs-lookup"><span data-stu-id="f3a1e-137">Requested: Source</span></span>      | <span data-ttu-id="f3a1e-138">安裝會要求安裝元件或功能以從來源執行。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-138">Installation requests that component or feature be installed to run from source.</span></span>                                |
| <span data-ttu-id="f3a1e-139">動作：來源</span><span class="sxs-lookup"><span data-stu-id="f3a1e-139">Action: Source</span></span>         | <span data-ttu-id="f3a1e-140">安裝程式實際上會安裝從來源執行的元件或功能。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-140">Installer actually installs the component or feature to run from source.</span></span>                                        |
| <span data-ttu-id="f3a1e-141">已安裝：公告</span><span class="sxs-lookup"><span data-stu-id="f3a1e-141">Installed: Advertise</span></span>   | <span data-ttu-id="f3a1e-142">功能目前已公告。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-142">Feature is currently advertised.</span></span> <span data-ttu-id="f3a1e-143">元件永遠不會公佈。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-143">Components are never advertised.</span></span>                                               |
| <span data-ttu-id="f3a1e-144">要求：公告</span><span class="sxs-lookup"><span data-stu-id="f3a1e-144">Request: Advertise</span></span>     | <span data-ttu-id="f3a1e-145">安裝要求功能是以公告功能的形式安裝。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-145">Installation requests feature be installed as an advertised feature.</span></span>                                            |
| <span data-ttu-id="f3a1e-146">動作：公告</span><span class="sxs-lookup"><span data-stu-id="f3a1e-146">Action: Advertise</span></span>      | <span data-ttu-id="f3a1e-147">安裝程式會實際將此功能安裝為已公告的功能。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-147">Installer actually installs the feature as an advertised feature.</span></span>                                               |
| <span data-ttu-id="f3a1e-148">要求：重新安裝</span><span class="sxs-lookup"><span data-stu-id="f3a1e-148">Request: Reinstall</span></span>     | <span data-ttu-id="f3a1e-149">安裝要求功能已重新安裝。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-149">Installation requests feature be reinstalled.</span></span> <span data-ttu-id="f3a1e-150">元件不會使用重新安裝狀態。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-150">Components do not use reinstall state.</span></span>                            |
| <span data-ttu-id="f3a1e-151">動作：重新安裝</span><span class="sxs-lookup"><span data-stu-id="f3a1e-151">Action: Reinstall</span></span>      | <span data-ttu-id="f3a1e-152">安裝程式會實際重新安裝功能。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-152">Installer actually reinstalls feature.</span></span>                                                                          |
| <span data-ttu-id="f3a1e-153">已安裝：目前</span><span class="sxs-lookup"><span data-stu-id="f3a1e-153">Installed: Current</span></span>     | <span data-ttu-id="f3a1e-154">功能目前是以預設撰寫的安裝狀態安裝。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-154">Feature is currently installed in the default authored install state.</span></span>                                           |
| <span data-ttu-id="f3a1e-155">要求：目前</span><span class="sxs-lookup"><span data-stu-id="f3a1e-155">Request: Current</span></span>       | <span data-ttu-id="f3a1e-156">安裝要求功能是以預設撰寫的安裝狀態安裝。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-156">Installation requests feature be installed in the default authored install state.</span></span>                               |
| <span data-ttu-id="f3a1e-157">動作：目前</span><span class="sxs-lookup"><span data-stu-id="f3a1e-157">Action: Current</span></span>        | <span data-ttu-id="f3a1e-158">安裝程式會實際以預設撰寫的安裝狀態安裝該功能。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-158">Installer actually installs the feature in the default authored install state.</span></span>                                  |
| <span data-ttu-id="f3a1e-159">Action： FileAbsent</span><span class="sxs-lookup"><span data-stu-id="f3a1e-159">Action: FileAbsent</span></span>     | <span data-ttu-id="f3a1e-160">安裝程式會實際卸載元件的檔案，並保留已安裝元件的所有其他資源。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-160">Installer actually uninstalls component's files and leaves all other resources of the component installed.</span></span>      |
| <span data-ttu-id="f3a1e-161">Action： HKCRAbsent</span><span class="sxs-lookup"><span data-stu-id="f3a1e-161">Action: HKCRAbsent</span></span>     | <span data-ttu-id="f3a1e-162">安裝程式會實際移除元件的 HKCR 資訊。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-162">Installer actually removes component's HKCR information.</span></span> <span data-ttu-id="f3a1e-163">檔案和非 HKCR 資訊仍然存在。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-163">File and non-HKCR information remain.</span></span>                  |
| <span data-ttu-id="f3a1e-164">Action： HKCRFileAbsent</span><span class="sxs-lookup"><span data-stu-id="f3a1e-164">Action: HKCRFileAbsent</span></span> | <span data-ttu-id="f3a1e-165">安裝程式會實際移除元件的 HKCR 資訊和檔案。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-165">Installer actually removes component's HKCR information and files.</span></span> <span data-ttu-id="f3a1e-166">元件的其他所有資源都會保留下來。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-166">All other resources of the component remain.</span></span> |



 

<span data-ttu-id="f3a1e-167">詳細資訊記錄檔中有套件可能安裝的每個檔案的專案。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-167">The verbose log has an entry for each file that may be installed by the package.</span></span> <span data-ttu-id="f3a1e-168">記錄檔會告知檔案已完成的作業，並提供一些說明。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-168">The log tells what was done to the file and provides some explanation.</span></span> <span data-ttu-id="f3a1e-169">記錄檔中的檔案專案會如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-169">File entries in the log appear as in the following example.</span></span>

``` syntax
MSI (s) (40:A4): File: C:\Test\TESTDB.EXE;  Won't Overwrite;  Existing
 file is of an equal version
```

<span data-ttu-id="f3a1e-170">此記錄檔表示安裝程式不會覆寫現有的 Testdb.exe 檔案，因為現有的檔案與所安裝的版本相同。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-170">This log indicates that the installer will not overwrite the existing Testdb.exe file because the existing file is the same as the version being installed.</span></span>

> [!Note]  
> <span data-ttu-id="f3a1e-171">如果您需要撰寫安裝套件，以在安裝期間在使用者電腦上搜尋現有的檔案或目錄，請使用 [搜尋現有的應用程式、檔案、登錄專案或 .ini 檔案專案](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md)中所述的方法。</span><span class="sxs-lookup"><span data-stu-id="f3a1e-171">If you need to author an installation package that searches for an existing file or directory on the user's computer during an installation, use the method described in [Searching for Existing Applications, Files, Registry Entries or .ini File Entries](searching-for-existing-applications-files-registry-entries-or--ini-file-entries.md).</span></span>

 

 

 



