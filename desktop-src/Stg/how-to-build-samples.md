---
title: 如何建立範例
description: 若要建立 COM 範例，必須設定電腦環境以建立 Microsoft Win32 c + + 應用程式。
ms.assetid: c62b8b4d-a9d2-4587-8bb6-7b2c30d1c00d
keywords:
- 如何建立範例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593d3465d3ebcc32a6768dd8b2dffe1f0a653d07
ms.sourcegitcommit: c2a1c4314550ea9bd202d28adfcc7bfe6180932f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2020
ms.locfileid: "106967881"
---
# <a name="how-to-build-samples"></a><span data-ttu-id="42d1d-104">如何建立範例</span><span class="sxs-lookup"><span data-stu-id="42d1d-104">How to Build Samples</span></span>

<span data-ttu-id="42d1d-105">若要建立 COM 範例，必須設定電腦環境以建立 Microsoft Win32 c + + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="42d1d-105">To build a COM sample, the computer environment must be set up to build Microsoft Win32 C++ applications.</span></span>

## <a name="preparing-a-computer-to-create-com-samples"></a><span data-ttu-id="42d1d-106">準備電腦以建立 COM 範例</span><span class="sxs-lookup"><span data-stu-id="42d1d-106">Preparing a Computer to Create COM Samples</span></span>

<span data-ttu-id="42d1d-107">電腦環境必須設定正確安裝的32位 c + + 編譯器、連結器和資源編譯器，與 Microsoft Visual C++ 4.x 或更新版本，以及正確安裝的 Windows SDK 相容。</span><span class="sxs-lookup"><span data-stu-id="42d1d-107">The computer environment must be set up with a properly installed 32-bit C++ compiler, linker, and resource compiler that are compatible with Microsoft Visual C++ 4.x or later, and a properly installed Windows SDK.</span></span> <span data-ttu-id="42d1d-108">最好是最後安裝 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="42d1d-108">It is best to install the Windows SDK last.</span></span> <span data-ttu-id="42d1d-109">Windows SDK 針對範例中編碼的 COM 功能，提供需要的 .h 包含和 .lib 程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="42d1d-109">The Windows SDK provides .h include and .lib library files required for the COM functionality coded in the samples.</span></span>

<span data-ttu-id="42d1d-110">若要成功執行 Remclien、Freserve 和 Freclien 範例，需要可在 Windows 作業系統中使用的系統裝置： Windows Server 2003、Windows XP、Windows 2000 或 Windows NT 4.0。</span><span class="sxs-lookup"><span data-stu-id="42d1d-110">To successfully run the Remclien, Freserve, and Freclien samples requires system facilities that are available in the Windows operating systems: Windows Server 2003, Windows XP, Windows 2000, or Windows NT 4.0.</span></span> <span data-ttu-id="42d1d-111">Remclien、Freserve 和 Freclien 範例將會建立，但不會在 Windows Me、Windows 98 或 Windows 95 作業系統上執行，除非分散式 COM (DCOM) 和無限制執行緒 COM 是作業系統的一部分。</span><span class="sxs-lookup"><span data-stu-id="42d1d-111">The Remclien, Freserve, and Freclien samples will build but will not run on the Windows Me, Windows 98, or Windows 95 operating systems unless Distributed COM (DCOM) and free threaded COM are part of the operating system.</span></span> <span data-ttu-id="42d1d-112">這項支援適用于 DCOM95.EXE add on 中的 Windows Me、Windows 98 和 Windows 95 作業系統。</span><span class="sxs-lookup"><span data-stu-id="42d1d-112">This support is available for the Windows Me, Windows 98, and Windows 95 operating systems in the DCOM95 add on.</span></span> <span data-ttu-id="42d1d-113">您可以 [從 Microsoft 下載](https://www.microsoft.com/download/details.aspx?id=31661)dcom95.exe 來取得。</span><span class="sxs-lookup"><span data-stu-id="42d1d-113">DCOM95 can currently be obtained by [download from Microsoft](https://www.microsoft.com/download/details.aspx?id=31661).</span></span>

<span data-ttu-id="42d1d-114">每個範例目錄都有必要的原始程式檔，可建立並執行範例。</span><span class="sxs-lookup"><span data-stu-id="42d1d-114">Each sample directory has the necessary source files to build and run the sample.</span></span> <span data-ttu-id="42d1d-115">父範例目錄具有 Makeall.bat 檔案，您可以從命令提示字元執行此檔案，以將所有的程式碼範例都設為下列分支中的所有程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="42d1d-115">The parent sample directory has a Makeall.bat file, which you can run from the command prompt to make all the code samples in the branch below.</span></span> <span data-ttu-id="42d1d-116">如需詳細資訊，請參閱 Makeall.bat 檔案。</span><span class="sxs-lookup"><span data-stu-id="42d1d-116">For more information, see the Makeall.bat file.</span></span> <span data-ttu-id="42d1d-117">如果您的環境已設定為建立 Win32 c + + 應用程式，您可以直接從它所在的目錄執行 Makeall.bat，以建立下一個分支中的所有程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="42d1d-117">If your environment is set up to build Win32 C++ applications, you can simply run Makeall.bat from the directory where it resides to build all the code samples in the branch below.</span></span> <span data-ttu-id="42d1d-118">Makeall 可確保組建的正確順序，以滿足所有的程式碼範例相依性。</span><span class="sxs-lookup"><span data-stu-id="42d1d-118">Makeall ensures the correct order to the build so that all the code sample dependencies are satisfied.</span></span>

<span data-ttu-id="42d1d-119">主要目錄也有 makefile，可使用類似 Makeall.bat 所支援的選項來建立所有教學課程程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="42d1d-119">The main directory also has a makefile that builds all the tutorial code samples using options similar to those supported by Makeall.bat.</span></span> <span data-ttu-id="42d1d-120">如需詳細資訊，請參閱這個 makefile。</span><span class="sxs-lookup"><span data-stu-id="42d1d-120">For more information, see this makefile.</span></span> <span data-ttu-id="42d1d-121">這個 makefile 假設整個程式碼範例分支會安裝為 Windows SDK 的一部分。</span><span class="sxs-lookup"><span data-stu-id="42d1d-121">This makefile assumes that the entire code samples branch is installed as part of the Windows SDK.</span></span> <span data-ttu-id="42d1d-122">此位置目前的路徑類似 *d： \\ MSSDK \\ 範例 \\ COM \\ TUTSAMP*，其中 d：代表安裝磁片磁碟機。</span><span class="sxs-lookup"><span data-stu-id="42d1d-122">Currently this location has a path similar to *D:\\MSSDK\\SAMPLES\\COM\\TUTSAMP*, where D: represents the installation drive.</span></span> <span data-ttu-id="42d1d-123">如果您已將教學課程程式碼範例分支解壓縮 (例如，COM 目錄 COM 及其子目錄) 至 Windows SDK (以外的其他位置，或您從 Microsoft 網站) 取得範例集合作為個別下載，則請使用 Makeall.bat 來編譯分支中的所有範例。</span><span class="sxs-lookup"><span data-stu-id="42d1d-123">If you have extracted the tutorial code sample branch (for example, the COM directory COM and its subdirectories) to another location outside the Windows SDK (or if you obtained the sample set as a separate download from the Microsoft website), then use Makeall.bat to compile all the samples in the branch.</span></span> <span data-ttu-id="42d1d-124">一般情況下，建議使用 Makeall.bat。</span><span class="sxs-lookup"><span data-stu-id="42d1d-124">In general, Makeall.bat is recommended.</span></span> <span data-ttu-id="42d1d-125">也會提供 Logmall.bat 檔案。</span><span class="sxs-lookup"><span data-stu-id="42d1d-125">A Logmall.bat file is also provided.</span></span> <span data-ttu-id="42d1d-126">它會與 Makeall 批次檔相同，不同之處在于它會將所有編譯輸出記錄至主要教學課程目錄中的檔案 Errorlog.txt。</span><span class="sxs-lookup"><span data-stu-id="42d1d-126">It does the same as Makeall batch file except that it logs all compilation output to file Errorlog.txt in the main tutorial directory.</span></span>

<span data-ttu-id="42d1d-127">主要目錄中也提供兩個批次檔 Regall.bat 和 Unregall.bat，可在教學課程程式碼範例系列中註冊及取消註冊所有的 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="42d1d-127">Two batch files, Regall.bat and Unregall.bat, are also provided in the main directory to register and unregister all COM servers in the tutorial code sample series.</span></span> <span data-ttu-id="42d1d-128">若要註冊所有伺服器，請從主要目錄執行 Regall.bat 檔案。</span><span class="sxs-lookup"><span data-stu-id="42d1d-128">To register all servers, run Regall.bat file from the main directory.</span></span> <span data-ttu-id="42d1d-129">若要取消註冊所有伺服器，請以相同的方式執行 Unregall.bat。</span><span class="sxs-lookup"><span data-stu-id="42d1d-129">To unregister all servers, run Unregall.bat in the same manner.</span></span> <span data-ttu-id="42d1d-130">這些批次檔需要註冊、封送、DLLSERVE、LICSERVE、LOCSERVE、APTSERVE、FRESERVE 的先前組建，以及節省程式碼範例。</span><span class="sxs-lookup"><span data-stu-id="42d1d-130">These batch files require a prior build of the REGISTER, MARSHAL, DLLSERVE, LICSERVE, LOCSERVE, APTSERVE, FRESERVE, and CONSERVE code samples.</span></span> <span data-ttu-id="42d1d-131">如果您執行一般的程式碼範例組建，伺服器 makefile 將會自動註冊伺服器。</span><span class="sxs-lookup"><span data-stu-id="42d1d-131">If you perform a normal build of the code samples, the server makefiles will automatically register the servers.</span></span> <span data-ttu-id="42d1d-132">在此情況下，不需要執行 Regall 批次檔。</span><span class="sxs-lookup"><span data-stu-id="42d1d-132">In this case, it is not necessary to run the Regall batch file.</span></span>

<span data-ttu-id="42d1d-133">執行 Cleanall.bat 批次檔，以執行所有 COM 教學課程範例的完整 Cleanall。</span><span class="sxs-lookup"><span data-stu-id="42d1d-133">Run the Cleanall.bat batch file to perform an exhaustive Cleanall of all the COM Tutorial Samples.</span></span>

> [!WARNING]
> <span data-ttu-id="42d1d-134">此批次檔會刪除範例中 Visual C++ 所建立的所有 Visual Studio 專案檔和其他暫存工作檔案。</span><span class="sxs-lookup"><span data-stu-id="42d1d-134">This batch file deletes all Visual Studio project files and other temporary work files created by Visual C++ in the samples.</span></span> <span data-ttu-id="42d1d-135">教學課程程式碼範例中內建的所有 COM 伺服器都會從登錄中取消註冊。</span><span class="sxs-lookup"><span data-stu-id="42d1d-135">All of the COM servers built in the tutorial code samples are unregistered from the registry.</span></span> <span data-ttu-id="42d1d-136">所有可執行檔 exe 和 .dll 檔案都會刪除。</span><span class="sxs-lookup"><span data-stu-id="42d1d-136">All executable exe and .dll files are deleted.</span></span> <span data-ttu-id="42d1d-137">所有的 debug 符號檔都會刪除。</span><span class="sxs-lookup"><span data-stu-id="42d1d-137">All debug symbol files are deleted.</span></span> <span data-ttu-id="42d1d-138">也會刪除各種組建環境中產生的檔案。</span><span class="sxs-lookup"><span data-stu-id="42d1d-138">Files generated in a variety of build environments are also deleted.</span></span>

 

<span data-ttu-id="42d1d-139">執行 ' Makeall Clean ' 以執行更快且更適度的程式碼範例清除。</span><span class="sxs-lookup"><span data-stu-id="42d1d-139">Run 'Makeall Clean' to perform a faster, but more modest, cleanup of all the code samples.</span></span> <span data-ttu-id="42d1d-140">這項清除作業不會嘗試像 Cleanall.bat 所執行的完整。</span><span class="sxs-lookup"><span data-stu-id="42d1d-140">This cleaning operation does not attempt to be as comprehensive as that performed by Cleanall.bat.</span></span> <span data-ttu-id="42d1d-141">.Obj 檔案會遭到刪除，但會保留輸出二進位檔。</span><span class="sxs-lookup"><span data-stu-id="42d1d-141">The .obj files are deleted, but the output binaries are retained.</span></span> <span data-ttu-id="42d1d-142">COM 伺服器不會從登錄中取消註冊。</span><span class="sxs-lookup"><span data-stu-id="42d1d-142">The COM servers are not unregistered from the registry.</span></span>

<span data-ttu-id="42d1d-143">此範例系列是 Windows SDK 的不可或缺部分產生，因此教學課程的敘述會假設已正確安裝 Windows SDK 的環境。</span><span class="sxs-lookup"><span data-stu-id="42d1d-143">This sample series originated as an integral part of the Windows SDK, therefore the tutorial narrative assumes an environment with the Windows SDK properly installed.</span></span>

<span data-ttu-id="42d1d-144">不過，版本4.0 和更新版本的 Microsoft Visual C++ 也可以提供編譯所需的 .h 和 .lib 程式庫檔案。</span><span class="sxs-lookup"><span data-stu-id="42d1d-144">However, releases of Microsoft Visual C++ version 4.0 and later may also provide the .h include and .lib library files required for compilation.</span></span> <span data-ttu-id="42d1d-145">在這種情況下，可能不需要安裝 Windows SDK 來編譯範例。</span><span class="sxs-lookup"><span data-stu-id="42d1d-145">In such cases, installation of the Windows SDK may not be required to compile the samples.</span></span>

<span data-ttu-id="42d1d-146">如需詳細資訊及完整的範例組建詳細資料，請參閱：</span><span class="sxs-lookup"><span data-stu-id="42d1d-146">For more information and complete sample build details, see:</span></span>

[<span data-ttu-id="42d1d-147">環境設定</span><span class="sxs-lookup"><span data-stu-id="42d1d-147">Environment Setup</span></span>](environment-setup.md)

[<span data-ttu-id="42d1d-148">生成</span><span class="sxs-lookup"><span data-stu-id="42d1d-148">Makefiles</span></span>](makefiles.md)

[<span data-ttu-id="42d1d-149">使用 Visual Studio</span><span class="sxs-lookup"><span data-stu-id="42d1d-149">Using Visual Studio</span></span>](using-visual-studio.md)

[<span data-ttu-id="42d1d-150">解壓縮程式代碼範例</span><span class="sxs-lookup"><span data-stu-id="42d1d-150">Extracting the Code Samples</span></span>](extracting-the-code-samples.md)

[<span data-ttu-id="42d1d-151">編碼樣式慣例</span><span class="sxs-lookup"><span data-stu-id="42d1d-151">Coding Style Conventions</span></span>](coding-style-conventions.md)

 

 




