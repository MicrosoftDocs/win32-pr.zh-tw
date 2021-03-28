---
description: 建立啟用自動啟用的應用程式是一個簡單的程式。 本主題使用 CD-ROM 作為範例 (它是執行這項技術的第一個媒體) 但現今有許多不同的媒體類型可以使用它。
title: 建立 AutoRun-Enabled 應用程式
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0d01f4a2-64c4-4b31-9fc9-361da6825ab8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 24a944b011c926d1638e5d0bcb0d35fc348e5783
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112352"
---
# <a name="creating-an-autorun-enabled-application"></a><span data-ttu-id="0e67b-104">建立 AutoRun-Enabled 應用程式</span><span class="sxs-lookup"><span data-stu-id="0e67b-104">Creating an AutoRun-Enabled Application</span></span>

<span data-ttu-id="0e67b-105">建立啟用自動啟用的應用程式是一個簡單的程式。</span><span class="sxs-lookup"><span data-stu-id="0e67b-105">Creating an AutoRun-enabled application is a straightforward procedure.</span></span> <span data-ttu-id="0e67b-106">本主題使用 CD-ROM 作為範例 (它是執行這項技術的第一個媒體) 但現今有許多不同的媒體類型可以使用它。</span><span class="sxs-lookup"><span data-stu-id="0e67b-106">This topic uses CD-ROM as an example (it was the first medium to implement this technology) but today there are many different media types that can use it.</span></span>

<span data-ttu-id="0e67b-107">若要在您的應用程式中啟用自動執行，您只需要包含兩個基本的檔案：</span><span class="sxs-lookup"><span data-stu-id="0e67b-107">To enable AutoRun in your application, you simply include two essential files:</span></span>

-   <span data-ttu-id="0e67b-108">自動運行的 .inf 檔案</span><span class="sxs-lookup"><span data-stu-id="0e67b-108">An Autorun.inf file</span></span>
-   <span data-ttu-id="0e67b-109">啟動應用程式</span><span class="sxs-lookup"><span data-stu-id="0e67b-109">A startup application</span></span>

<span data-ttu-id="0e67b-110">當使用者將光碟插入與自動執行相容的電腦上的 CD-ROM 光碟機時，系統會立即檢查光碟是否有個人電腦檔案系統。</span><span class="sxs-lookup"><span data-stu-id="0e67b-110">When a user inserts a disc into a CD-ROM drive on a AutoRun-compatible computer, the system immediately checks to see if the disc has a personal computer file system.</span></span> <span data-ttu-id="0e67b-111">如果有的話，系統會搜尋名為「 [自動執行 .inf](#creating-an-autoruninf-file)」的檔案。</span><span class="sxs-lookup"><span data-stu-id="0e67b-111">If it does, the system searches for a file named [Autorun.inf](#creating-an-autoruninf-file).</span></span> <span data-ttu-id="0e67b-112">此檔案會指定要執行的安裝應用程式，以及各種選擇性的設定。</span><span class="sxs-lookup"><span data-stu-id="0e67b-112">This file specifies a setup application that will be run, along with a variety of optional settings.</span></span> <span data-ttu-id="0e67b-113">啟動應用程式通常會安裝、卸載、設定，而且可能會執行應用程式。</span><span class="sxs-lookup"><span data-stu-id="0e67b-113">The startup application typically installs, uninstalls, configures, and perhaps runs the application.</span></span>

-   [<span data-ttu-id="0e67b-114">建立自動播放 .inf 檔案</span><span class="sxs-lookup"><span data-stu-id="0e67b-114">Creating an Autorun.inf File</span></span>](#creating-an-autoruninf-file)
-   <span data-ttu-id="0e67b-115">[\[DeviceInstall \] 區段](#the-deviceinstall-section)</span><span class="sxs-lookup"><span data-stu-id="0e67b-115">[The \[DeviceInstall\] Section](#the-deviceinstall-section)</span></span>
-   [<span data-ttu-id="0e67b-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e67b-116">Related topics</span></span>](#related-topics)

## <a name="creating-an-autoruninf-file"></a><span data-ttu-id="0e67b-117">建立自動播放 .inf 檔案</span><span class="sxs-lookup"><span data-stu-id="0e67b-117">Creating an Autorun.inf File</span></span>

<span data-ttu-id="0e67b-118">[自動安裝] 是位於 cd-rom 根目錄的文字檔，其中包含您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="0e67b-118">Autorun.inf is a text file located in the root directory of the CD-ROM that contains your application.</span></span> <span data-ttu-id="0e67b-119">其主要功能是為系統提供應用程式啟動程式的名稱和位置，在插入光碟時將會執行此程式。</span><span class="sxs-lookup"><span data-stu-id="0e67b-119">Its primary function is to provide the system with the name and location of the application's startup program that will be run when the disc is inserted.</span></span>

> [!Note]  
> <span data-ttu-id="0e67b-120">\_從 [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea)傳回磁片磁碟機的磁片磁碟機，在 Windows XP 下不支援自動運行 .inf 檔案。</span><span class="sxs-lookup"><span data-stu-id="0e67b-120">Autorun.inf files are not supported under Windows XP for drives that return DRIVE\_REMOVABLE from [**GetDriveType**](/windows/win32/api/fileapi/nf-fileapi-getdrivetypea).</span></span>

 

<span data-ttu-id="0e67b-121">自動執行 .inf 檔案也可以包含選用的資訊，包括：</span><span class="sxs-lookup"><span data-stu-id="0e67b-121">The Autorun.inf file can also contain optional information including:</span></span>

-   <span data-ttu-id="0e67b-122">包含圖示的檔案名，該圖示代表您應用程式的 CD-ROM 光碟機。</span><span class="sxs-lookup"><span data-stu-id="0e67b-122">The name of a file that contains an icon that will represent your application's CD-ROM drive.</span></span> <span data-ttu-id="0e67b-123">Windows 檔案總管取代標準磁片磁碟機圖示時，會顯示此圖示。</span><span class="sxs-lookup"><span data-stu-id="0e67b-123">This icon will be displayed by Windows Explorer in place of the standard drive icon.</span></span>
-   <span data-ttu-id="0e67b-124">當使用者以滑鼠右鍵按一下 CD-ROM 圖示時，所顯示之快捷方式功能表的其他命令。</span><span class="sxs-lookup"><span data-stu-id="0e67b-124">Additional commands for the shortcut menu that is displayed when the user right-clicks the CD-ROM icon.</span></span> <span data-ttu-id="0e67b-125">您也可以指定當使用者按兩下圖示時，所執行的預設命令。</span><span class="sxs-lookup"><span data-stu-id="0e67b-125">You can also specify the default command that is run when the user double-clicks the icon.</span></span>

<span data-ttu-id="0e67b-126">自動運行的 .inf 檔案類似于 .ini 檔案。</span><span class="sxs-lookup"><span data-stu-id="0e67b-126">Autorun.inf files are similar to .ini files.</span></span> <span data-ttu-id="0e67b-127">它們是由一或多個區段所組成，每個區段都是以方括弧括住的名稱。</span><span class="sxs-lookup"><span data-stu-id="0e67b-127">They consist of one or more sections, each headed by a name enclosed in square brackets.</span></span> <span data-ttu-id="0e67b-128">每個區段都包含一系列的命令，這些命令會在插入光碟時由 Shell 執行。</span><span class="sxs-lookup"><span data-stu-id="0e67b-128">Each section contains a series of commands that will be run by the Shell when the disc is inserted.</span></span> <span data-ttu-id="0e67b-129">目前有兩個區段是針對自動播放的 .inf 檔案所定義。</span><span class="sxs-lookup"><span data-stu-id="0e67b-129">There are two sections that are currently defined for Autorun.inf files.</span></span>

-   <span data-ttu-id="0e67b-130">[ **\[ 自動 \] 運行**] 區段包含預設的自動運行命令。</span><span class="sxs-lookup"><span data-stu-id="0e67b-130">The **\[autorun\]** section contains the default AutoRun commands.</span></span> <span data-ttu-id="0e67b-131">所有自動運行的 .inf 檔案都必須有 [ **\[ 自動運行 \]** ] 區段。</span><span class="sxs-lookup"><span data-stu-id="0e67b-131">All Autorun.inf files must have an **\[autorun\]** section.</span></span>
-   <span data-ttu-id="0e67b-132">選擇性的 [自動執行] **\[ Alpha \]** 區段可包含在 RISC 型電腦上執行的系統中。</span><span class="sxs-lookup"><span data-stu-id="0e67b-132">An optional **\[autorun.alpha\]** section can be included for systems running on RISC-based computers.</span></span> <span data-ttu-id="0e67b-133">將光碟插入至 RISC 型系統的 CD-ROM 光碟機時，Shell 會執行本節中的命令，而不是 [ **\[ 自動 \]** 執行] 區段中的命令。</span><span class="sxs-lookup"><span data-stu-id="0e67b-133">When a disc is inserted in a CD-ROM drive on a RISC-based system, the Shell will run the commands in this section instead of those in the **\[autorun\]** section.</span></span>

> [!Note]  
> <span data-ttu-id="0e67b-134">Shell 會先檢查特定的架構區段。</span><span class="sxs-lookup"><span data-stu-id="0e67b-134">The Shell checks for an architecture-specific section first.</span></span> <span data-ttu-id="0e67b-135">如果找不到，則會使用 [ **\[ 自動 \]** 執行] 區段中的資訊。</span><span class="sxs-lookup"><span data-stu-id="0e67b-135">If it does not find one, it uses the information in the **\[autorun\]** section.</span></span> <span data-ttu-id="0e67b-136">當 Shell 找到某個區段之後，它會忽略所有其他區段，因此每個區段都必須是獨立的。</span><span class="sxs-lookup"><span data-stu-id="0e67b-136">After the Shell finds a section, it ignores all others, so each section must be self-contained.</span></span>

 

<span data-ttu-id="0e67b-137">每一節都包含一系列的命令，用來決定自動執行時間的運作方式。</span><span class="sxs-lookup"><span data-stu-id="0e67b-137">Each section contains a series of commands that determine how the Autorun operation takes place.</span></span> <span data-ttu-id="0e67b-138">有五個可用的命令。</span><span class="sxs-lookup"><span data-stu-id="0e67b-138">There are five commands available.</span></span>



| <span data-ttu-id="0e67b-139">命令</span><span class="sxs-lookup"><span data-stu-id="0e67b-139">Command</span></span>                         | <span data-ttu-id="0e67b-140">描述</span><span class="sxs-lookup"><span data-stu-id="0e67b-140">Description</span></span>                                                                            |
|---------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="0e67b-141">defaulticon</span><span class="sxs-lookup"><span data-stu-id="0e67b-141">defaulticon</span></span>](autorun-cmds.md) | <span data-ttu-id="0e67b-142">指定應用程式的預設圖示。</span><span class="sxs-lookup"><span data-stu-id="0e67b-142">Specifies the default icon for the application.</span></span>                                        |
| [<span data-ttu-id="0e67b-143">圖示</span><span class="sxs-lookup"><span data-stu-id="0e67b-143">icon</span></span>](autorun-cmds.md)        | <span data-ttu-id="0e67b-144">指定 CD-ROM 光碟機的應用程式特定圖示的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="0e67b-144">Specifies the path and file name of an application-specific icon for the CD-ROM drive.</span></span> |
| [<span data-ttu-id="0e67b-145">open</span><span class="sxs-lookup"><span data-stu-id="0e67b-145">open</span></span>](autorun-cmds.md)        | <span data-ttu-id="0e67b-146">指定啟動應用程式的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="0e67b-146">Specifies the path and file name of the startup application.</span></span>                           |
| [<span data-ttu-id="0e67b-147">useautorun</span><span class="sxs-lookup"><span data-stu-id="0e67b-147">useautorun</span></span>](autorun-cmds.md)  | <span data-ttu-id="0e67b-148">指定如果支援，則應使用自動播放 V2 功能。</span><span class="sxs-lookup"><span data-stu-id="0e67b-148">Specifies that Autoplay V2 features should be used if supported.</span></span>                       |
| [<span data-ttu-id="0e67b-149">殼</span><span class="sxs-lookup"><span data-stu-id="0e67b-149">shell</span></span>](autorun-cmds.md)       | <span data-ttu-id="0e67b-150">在 CD-ROM 的快捷方式功能表中定義預設命令。</span><span class="sxs-lookup"><span data-stu-id="0e67b-150">Defines the default command in the CD-ROM's shortcut menu.</span></span>                             |
| [<span data-ttu-id="0e67b-151">shell \_ 動詞</span><span class="sxs-lookup"><span data-stu-id="0e67b-151">shell\_verb</span></span>](autorun-cmds.md) | <span data-ttu-id="0e67b-152">將命令新增至 CD-ROM 的快捷方式功能表。</span><span class="sxs-lookup"><span data-stu-id="0e67b-152">Adds commands to the CD-ROM's shortcut menu.</span></span>                                           |



 

<span data-ttu-id="0e67b-153">以下是簡單的自動執行 .inf 檔案範例。</span><span class="sxs-lookup"><span data-stu-id="0e67b-153">The following is an example of a simple Autorun.inf file.</span></span> <span data-ttu-id="0e67b-154">它會將 Filename.exe 指定為啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="0e67b-154">It specifies Filename.exe as the startup application.</span></span> <span data-ttu-id="0e67b-155">Filename.exe 中的第二個圖示將表示 CD-ROM 光碟機，而不是標準磁片磁碟機圖示。</span><span class="sxs-lookup"><span data-stu-id="0e67b-155">The second icon in Filename.exe will represent the CD-ROM drive instead of the standard drive icon.</span></span>


```
[autorun] 
open=Filename.exe 
icon=Filename.exe,1
```



<span data-ttu-id="0e67b-156">這個自動執行 .inf 範例會根據電腦的類型，執行不同的啟動應用程式。</span><span class="sxs-lookup"><span data-stu-id="0e67b-156">This Autorun.inf sample runs different startup applications depending on the type of computer.</span></span>


```
[autorun] 
open=Filename_x86.exe 
icon=IconFile.ico 

[autorun.alpha] 
open=Filename_RISC.exe 
icon=IconFile.ico
```



## <a name="the-deviceinstall-section"></a><span data-ttu-id="0e67b-157">\[DeviceInstall \] 區段</span><span class="sxs-lookup"><span data-stu-id="0e67b-157">The \[DeviceInstall\] Section</span></span>

<span data-ttu-id="0e67b-158">您可以使用任何卸載式媒體上的 **\[ DeviceInstall \]** 區段。</span><span class="sxs-lookup"><span data-stu-id="0e67b-158">You can use the **\[DeviceInstall\]** section on any removable media.</span></span> <span data-ttu-id="0e67b-159">只有在 Windows XP 下才支援此功能。</span><span class="sxs-lookup"><span data-stu-id="0e67b-159">It is supported only under Windows XP.</span></span> <span data-ttu-id="0e67b-160">您可以使用 **DriverPath** 來指定 Windows XP 搜尋驅動程式檔案的目錄路徑，以避免長時間搜尋整個內容。</span><span class="sxs-lookup"><span data-stu-id="0e67b-160">You use **DriverPath** to specify a directory path where Windows XP searches for driver files, which prevents a lengthy search through the entire contents.</span></span>

<span data-ttu-id="0e67b-161">您可以使用 **\[ DeviceInstall \]** 區段和驅動程式安裝，來指定 Windows XP 應該在媒體上搜尋驅動程式檔案的目錄。</span><span class="sxs-lookup"><span data-stu-id="0e67b-161">You use the **\[DeviceInstall\]** section with a driver installation to specify directories where Windows XP should search the media for driver files.</span></span> <span data-ttu-id="0e67b-162">在 Windows XP 中，預設不會再搜尋整個媒體，因此需要 **\[ DeviceInstall \]** 指定搜尋位置。</span><span class="sxs-lookup"><span data-stu-id="0e67b-162">Under Windows XP, entire media are no longer searched by default, therefore requiring **\[DeviceInstall\]** to specify search locations.</span></span> <span data-ttu-id="0e67b-163">以下是 Windows XP 在執行 .inf 檔案中完全不需要 **\[ DeviceInstall \]** 區段就能完全搜尋的卸載式媒體。</span><span class="sxs-lookup"><span data-stu-id="0e67b-163">The following are the only removable media that Windows XP fully searches without a **\[DeviceInstall\]** section in an Autorun.inf file.</span></span>

-   <span data-ttu-id="0e67b-164">磁片磁碟機 A 或 B 中找到的磁片。</span><span class="sxs-lookup"><span data-stu-id="0e67b-164">Floppy disks found in drives A or B.</span></span>
-   <span data-ttu-id="0e67b-165">CD/DVD 媒體的大小不會超過 1 gb (GB) 。</span><span class="sxs-lookup"><span data-stu-id="0e67b-165">CD/DVD media less that 1 gigabyte (GB) in size.</span></span>

<span data-ttu-id="0e67b-166">所有其他媒體都必須包含 **\[ DeviceInstall \]** 區段，才能讓 Windows XP 偵測儲存在該媒體上的任何驅動程式。</span><span class="sxs-lookup"><span data-stu-id="0e67b-166">All other media must include a **\[DeviceInstall\]** section for Windows XP to detect any drivers stored on that media.</span></span>

> [!Note]  
> <span data-ttu-id="0e67b-167">如同 [ **\[ 自動運行 \]** ] 區段， **\[ DeviceInstall \]** 區段可以是架構專屬的。</span><span class="sxs-lookup"><span data-stu-id="0e67b-167">As with the **\[AutoRun\]** section, the **\[DeviceInstall\]** section can be architecture-specific.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="0e67b-168">相關主題</span><span class="sxs-lookup"><span data-stu-id="0e67b-168">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e67b-169">如何執行自動啟動應用程式</span><span class="sxs-lookup"><span data-stu-id="0e67b-169">How to Implement Autorun Startup Applications</span></span>](how-to-implement-autorun-startup-applications.md)
</dt> <dt>

[<span data-ttu-id="0e67b-170">撰寫裝置安裝應用程式</span><span class="sxs-lookup"><span data-stu-id="0e67b-170">Writing a Device Installation Application</span></span>](/windows-hardware/drivers/install/writing-a-device-installation-application)
</dt> </dl>

 

 
