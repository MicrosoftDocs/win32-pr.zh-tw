---
title: 使用 Visual Studio
description: 為了方便起見，Microsoft Visual Studio 6.0 會提供每個範例的專案檔。
ms.assetid: 8da6affd-a881-4dc4-a2e6-d35f655c69fe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5b32359a29d14a6cd5a4d08d015a6598ade376d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671063"
---
# <a name="using-visual-studio"></a><span data-ttu-id="8f64f-103">使用 Visual Studio</span><span class="sxs-lookup"><span data-stu-id="8f64f-103">Using Visual Studio</span></span>

<span data-ttu-id="8f64f-104">為了方便起見，Microsoft Visual Studio 6.0 會提供每個範例的專案檔。</span><span class="sxs-lookup"><span data-stu-id="8f64f-104">For convenience, Microsoft Visual Studio 6.0 provides a project file for each sample.</span></span> <span data-ttu-id="8f64f-105">此檔案具有 DSP 延伸模組。</span><span class="sxs-lookup"><span data-stu-id="8f64f-105">This file has the DSP extension.</span></span> <span data-ttu-id="8f64f-106">主要目錄中也提供 Allsamp dsw 工作區檔案，讓您可以從 Visual Studio 內一次編譯所有範例。</span><span class="sxs-lookup"><span data-stu-id="8f64f-106">An Allsamp.dsw workspace file is also provided in the main directory so that you can compile all the samples at once from within Visual Studio.</span></span>

> [!Note]  
> <span data-ttu-id="8f64f-107">下列指示是針對 Microsoft Visual Studio 6.0 所撰寫。</span><span class="sxs-lookup"><span data-stu-id="8f64f-107">The following instructions are written for Microsoft Visual Studio 6.0.</span></span> <span data-ttu-id="8f64f-108">在舊版和更新版本的 Visual Studio 中，這些命令可能會有所不同。</span><span class="sxs-lookup"><span data-stu-id="8f64f-108">The commands may differ in earlier and later versions of Visual Studio.</span></span>

 

<span data-ttu-id="8f64f-109">若要為範例載入適當的專案，您可以在範例目錄的命令提示字元中執行 Visual Studio，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="8f64f-109">To load the appropriate project for a sample, you can run Visual Studio at the command prompt in the sample's directory as shown in the following example.</span></span> <span data-ttu-id="8f64f-110">您必須以的範例專案名稱取代 **<project name>** 。</span><span class="sxs-lookup"><span data-stu-id="8f64f-110">You must substitute the sample project name for **<project name>**.</span></span>

<span data-ttu-id="8f64f-111">**msdev <project name> dsp**</span><span class="sxs-lookup"><span data-stu-id="8f64f-111">**msdev <project name>.dsp**</span></span>

<span data-ttu-id="8f64f-112">您也可以直接按兩下 Windows 檔案總管中的 dsp 檔案，將範例的工作區載入 Visual Studio。</span><span class="sxs-lookup"><span data-stu-id="8f64f-112">You can also simply double-click the .dsp file in the Windows Explorer to load a sample's workspace into Visual Studio.</span></span> <span data-ttu-id="8f64f-113">在 Visual Studio 中，您接著可以流覽範例來源的 c + + 類別，並一般執行其他編輯-編譯-debug 作業。</span><span class="sxs-lookup"><span data-stu-id="8f64f-113">From within Visual Studio you can then browse the C++ classes of the sample source and generally perform the other edit-compile-debug operations.</span></span>

<span data-ttu-id="8f64f-114">作為平臺軟體發展工具組的一部分 (SDK) ，在 Visual Studio 中編譯這些範例需要 Visual Studio 中正確設定目錄路徑。</span><span class="sxs-lookup"><span data-stu-id="8f64f-114">As part of the Platform Software Development Kit (SDK), the compilation of these samples from within Visual Studio requires the proper setting of directory paths in Visual Studio.</span></span> <span data-ttu-id="8f64f-115">若要設定目錄路徑，請執行下列步驟：</span><span class="sxs-lookup"><span data-stu-id="8f64f-115">To set the directory paths, perform the following steps:</span></span>

-   <span data-ttu-id="8f64f-116">執行 Microsoft Visual Studio (Visual C++) 。</span><span class="sxs-lookup"><span data-stu-id="8f64f-116">Run Microsoft Visual Studio (Visual C++).</span></span>
-   <span data-ttu-id="8f64f-117">選擇 [**工具**] 功能表上的 [**選項**]。</span><span class="sxs-lookup"><span data-stu-id="8f64f-117">Choose **Options...** on the **Tools** menu.</span></span>
-   <span data-ttu-id="8f64f-118">選擇 [**選項**] 對話方塊中的 [**目錄**] 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="8f64f-118">Choose the **Directories** tab in the **Options** dialog.</span></span>
-   <span data-ttu-id="8f64f-119">在 [ **顯示目錄** ] 下拉式清單中，選取 [ **可執行檔** ]，並輸入已安裝平臺 SDK 的 BIN 目錄路徑 (例如 C： \\ Program files \\ Microsoft SDK \\ BIN) 。</span><span class="sxs-lookup"><span data-stu-id="8f64f-119">In the **Show Directories For** drop-down list, select **Executable files** and enter the BIN directory path for your installed Platform SDK (for example, C:\\Program Files\\Microsoft SDK\\Bin).</span></span> <span data-ttu-id="8f64f-120">按一下向上箭號按鈕，將這個新輸入的路徑移到 [ **目錄** ] 清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="8f64f-120">Click the up arrow button to move this newly entered path so that it is the first entry in the **Directories** list.</span></span>
-   <span data-ttu-id="8f64f-121">在 [ **顯示目錄** ] 下拉式清單中，選取 [ **包含** 檔案]，然後輸入已安裝之平臺 SDK 的包含目錄路徑 (例如，C： \\ Program files \\ Microsoft SDK \\ 包含) 。</span><span class="sxs-lookup"><span data-stu-id="8f64f-121">In the **Show Directories For** drop-down list select **Include files** and enter the INCLUDE directory path for your installed Platform SDK(for example, C:\\Program Files\\Microsoft SDK\\include).</span></span> <span data-ttu-id="8f64f-122">按一下向上箭號按鈕，將這個新輸入的路徑移到 [ **目錄** ] 清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="8f64f-122">Click the up arrow button to move this newly entered path so that it is the first entry in the **Directories** list.</span></span>
-   <span data-ttu-id="8f64f-123">在 [ **顯示目錄** ] 下拉式清單中，選取 [連結 **庫** 檔案]，然後輸入已安裝平臺 SDK 的 LIB 目錄路徑 (例如，C： \\ Program files \\ Microsoft SDK \\ LIB) 。</span><span class="sxs-lookup"><span data-stu-id="8f64f-123">In the **Show Directories For** drop-down list select **Library files** and enter the LIB directory path for your installed Platform SDK(for example, C:\\Program Files\\Microsoft SDK\\Lib).</span></span> <span data-ttu-id="8f64f-124">按一下向上箭號按鈕，將這個新輸入的路徑移到 [ **目錄** ] 清單中的第一個專案。</span><span class="sxs-lookup"><span data-stu-id="8f64f-124">Click the up arrow buttons to move this newly entered path so that it is the first entry in the **Directories** list.</span></span>
-   <span data-ttu-id="8f64f-125">按一下 [ **選項** ] 對話方塊中的 [確定] 按鈕，以完成設定。</span><span class="sxs-lookup"><span data-stu-id="8f64f-125">Click the OK button in the **Options** dialog to complete the settings.</span></span>

<span data-ttu-id="8f64f-126">從該處，您可以使用編輯器、偵錯工具和專案功能來編輯、編譯、連結和偵錯工具。</span><span class="sxs-lookup"><span data-stu-id="8f64f-126">From there you can use the editor, debugger, and project facilities to edit, compile, link, and debug.</span></span>

<span data-ttu-id="8f64f-127">如果有程式碼範例的現有原始程式檔，其他 visual Ide 也可以輕鬆地產生其中一個原生專案 makefile。</span><span class="sxs-lookup"><span data-stu-id="8f64f-127">Other visual IDEs can also easily generate one of their native project makefiles, given the existing source files of a code sample.</span></span> <span data-ttu-id="8f64f-128">如果您使用這類的 IDE，產生這類原生專案 makefile 可能很值得，因為它提供了流覽程式 c + + 類別的方法。</span><span class="sxs-lookup"><span data-stu-id="8f64f-128">If you are using such an IDE, generating such a native project makefile can be very worthwhile because it offers a way to browse the C++ classes of the program.</span></span> <span data-ttu-id="8f64f-129">如需使用外部 makefile 或使用一組現有原始程式檔建立原生專案 makefile 的詳細資訊，請參閱您的 IDE 檔。</span><span class="sxs-lookup"><span data-stu-id="8f64f-129">For more information about using external makefiles or creating a native project makefile using a set of existing source files, see your IDE documentation.</span></span>

<span data-ttu-id="8f64f-130">除了相依于同輩 APPUTIL、INC. 和 LIB 目錄中的通用程式碼，許多程式碼範例都是獨立的。</span><span class="sxs-lookup"><span data-stu-id="8f64f-130">Aside from the dependence on the common code in the sibling APPUTIL, INC, and LIB directories, many code samples are self-contained.</span></span> <span data-ttu-id="8f64f-131">建立任何其他程式碼範例之前的組建 APPUTIL。</span><span class="sxs-lookup"><span data-stu-id="8f64f-131">Build APPUTIL before you build any other code samples.</span></span> <span data-ttu-id="8f64f-132">序列中稍後的一些範例可能會使用先前範例的已編譯結果。</span><span class="sxs-lookup"><span data-stu-id="8f64f-132">Some samples later in the sequence may work with the compiled results of earlier samples.</span></span> <span data-ttu-id="8f64f-133">下列程式碼範例相互相關性如下所示：</span><span class="sxs-lookup"><span data-stu-id="8f64f-133">These code sample interdependencies are as follows:</span></span>

-   <span data-ttu-id="8f64f-134">任何：任何程式碼範例的組建都需要先前的 APPUTIL 組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-134">Any: Build of any code sample needs prior build of APPUTIL.</span></span>
-   <span data-ttu-id="8f64f-135">DLLUSER：組建或執行需要先前的 DLLSKEL 組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-135">DLLUSER: Build or run needs prior build of DLLSKEL.</span></span>
-   <span data-ttu-id="8f64f-136">COMUSER：組建或執行需要先前的 COMOBJ 組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-136">COMUSER: Build or run needs prior build of COMOBJ.</span></span>
-   <span data-ttu-id="8f64f-137">DLLSERVE：組建需要註冊之前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-137">DLLSERVE: Build needs prior build of REGISTER.</span></span>
-   <span data-ttu-id="8f64f-138">DLLCLIEN： Run 需要 DLLSERVE 先前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-138">DLLCLIEN: Run needs prior build of DLLSERVE.</span></span>
-   <span data-ttu-id="8f64f-139">LICSERVE：組建需要註冊之前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-139">LICSERVE: Build needs prior build of REGISTER.</span></span>
-   <span data-ttu-id="8f64f-140">LICCLIEN： Run 必須有 LICSERVE 和 DLLSERVE 之前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-140">LICCLIEN: Run needs prior build of LICSERVE and DLLSERVE.</span></span>
-   <span data-ttu-id="8f64f-141">封送處理：組建需要預先註冊的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-141">MARSHAL: Build needs prior build of REGISTER.</span></span>
-   <span data-ttu-id="8f64f-142">LOCSERVE：組建或執行需要先前的註冊和封送處理組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-142">LOCSERVE: Build or run needs prior build of REGISTER and MARSHAL.</span></span>
-   <span data-ttu-id="8f64f-143">LOCCLIEN： Run 需要 LOCSERVE 先前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-143">LOCCLIEN: Run needs prior build of LOCSERVE.</span></span>
-   <span data-ttu-id="8f64f-144">APTSERVE：組建或執行需要先前的註冊和封送處理組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-144">APTSERVE: Build or run needs prior build of REGISTER and MARSHAL.</span></span>
-   <span data-ttu-id="8f64f-145">APTCLIEN： Run 需要 APTSERVE 先前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-145">APTCLIEN: Run needs prior build of APTSERVE.</span></span>
-   <span data-ttu-id="8f64f-146">REMCLIEN：組建或執行需要在本機 (用戶端) 電腦上註冊和封送處理之前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-146">REMCLIEN: Build or run needs prior build of REGISTER and MARSHAL on local (client) computer.</span></span> <span data-ttu-id="8f64f-147">在遠端 (server) 的電腦上執行註冊、封送和 APTSERVE 之前的版本需要執行。</span><span class="sxs-lookup"><span data-stu-id="8f64f-147">Run needs prior build of REGISTER, MARSHAL, and APTSERVE on remote (server) computer.</span></span>
-   <span data-ttu-id="8f64f-148">FRESERVE：組建需要註冊之前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-148">FRESERVE: Build needs prior build of REGISTER.</span></span>
-   <span data-ttu-id="8f64f-149">FRECLIEN： Run 需要 FRESERVE 先前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-149">FRECLIEN: Run needs prior build of FRESERVE.</span></span>
-   <span data-ttu-id="8f64f-150">節省：組建需要預先註冊的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-150">CONSERVE: Build needs prior build of REGISTER.</span></span>
-   <span data-ttu-id="8f64f-151">CONCLIEN：執行之前需要節省的版本。</span><span class="sxs-lookup"><span data-stu-id="8f64f-151">CONCLIEN: Run needs prior build of CONSERVE.</span></span>
-   <span data-ttu-id="8f64f-152">STOSERVE：組建需要註冊之前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-152">STOSERVE: Build needs prior build of REGISTER.</span></span>
-   <span data-ttu-id="8f64f-153">STOCLIEN： Run 需要 STOSERVE 先前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-153">STOCLIEN: Run needs prior build of STOSERVE.</span></span>
-   <span data-ttu-id="8f64f-154">保留：組建需要註冊之前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-154">PERSERVE: Build needs prior build of REGISTER.</span></span>
-   <span data-ttu-id="8f64f-155">PERTEXT：組建需要註冊之前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-155">PERTEXT: Build needs prior build of REGISTER.</span></span>
-   <span data-ttu-id="8f64f-156">PERDRAW：組建需要註冊之前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-156">PERDRAW: Build needs prior build of REGISTER.</span></span>
-   <span data-ttu-id="8f64f-157">PERCLIEN： Run 必須有保留、PERTEXT 和 PERDRAW 之前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-157">PERCLIEN: Run needs prior build of PERSERVE, PERTEXT, and PERDRAW.</span></span>
-   <span data-ttu-id="8f64f-158">DCDMARSH：組建需要註冊之前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-158">DCDMARSH: Build needs prior build of REGISTER.</span></span>
-   <span data-ttu-id="8f64f-159">DCDSERVE：組建或執行需要先前的 REGISTER 和 DCDMARSH 組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-159">DCDSERVE: Build or run needs prior build of REGISTER and DCDMARSH.</span></span>
-   <span data-ttu-id="8f64f-160">DCOMDRAW：組建或執行需要在本機 (用戶端) 電腦上進行登錄和 DCDMARSH 先前的組建。</span><span class="sxs-lookup"><span data-stu-id="8f64f-160">DCOMDRAW: Build or run needs prior build of REGISTER and DCDMARSH on local (client) computer.</span></span> <span data-ttu-id="8f64f-161">執行需要在遠端 (server) 電腦上註冊、DCDMARSH 和 DCOMDRAW 之前的版本。</span><span class="sxs-lookup"><span data-stu-id="8f64f-161">Run needs prior build of REGISTER, DCDMARSH, and DCOMDRAW on remote (server) computer.</span></span>

 

 




