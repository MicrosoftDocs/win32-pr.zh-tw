---
title: App 封裝工具 (MakeAppx.exe)
description: 應用程式封裝工具 (MakeAppx.exe) 會從磁片上的檔案建立應用程式套件，或將檔案從應用程式封裝解壓縮至磁片。
ms.assetid: 9B7BF420-8E19-4BFD-B378-D09E61F68A39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41595550f3bee7b1149959886ed649e9212224b2
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092645"
---
# <a name="app-packager-makeappxexe"></a><span data-ttu-id="71769-103">App 封裝工具 (MakeAppx.exe)</span><span class="sxs-lookup"><span data-stu-id="71769-103">App packager (MakeAppx.exe)</span></span>

> [!Note]  
> <span data-ttu-id="71769-104">如需使用此工具的 UWP 指引，請參閱使用 [MakeAppx.exe 工具建立應用程式套件](/windows/msix/package/create-app-package-with-makeappx-tool)。</span><span class="sxs-lookup"><span data-stu-id="71769-104">For UWP guidance on using this tool, see [Create an app package with the MakeAppx.exe tool](/windows/msix/package/create-app-package-with-makeappx-tool).</span></span>

 

<span data-ttu-id="71769-105">應用程式封裝工具 (MakeAppx.exe) 會從磁片上的檔案建立應用程式套件，或將檔案從應用程式封裝解壓縮至磁片。</span><span class="sxs-lookup"><span data-stu-id="71769-105">App packager (MakeAppx.exe) creates an app package from files on disk or extracts the files from an app package to disk.</span></span> <span data-ttu-id="71769-106">從 Windows 8.1 開始，應用程式封裝程式也會從磁片上的應用程式套件建立應用程式套件套件組合，或將應用程式套件套件組合中的應用程式套件解壓縮至磁片。</span><span class="sxs-lookup"><span data-stu-id="71769-106">Starting with Windows 8.1, App packager also creates an app package bundle from app packages on disk or extracts the app packages from an app package bundle to disk.</span></span> <span data-ttu-id="71769-107">它包含在 Microsoft Visual Studio 和 Windows 軟體開發套件 (SDK) ，適用于 Windows 8 Windows 軟體開發套件或 () SDK Windows 8.1。</span><span class="sxs-lookup"><span data-stu-id="71769-107">It is included in Microsoft Visual Studio and the Windows Software Development Kit (SDK) for Windows 8 or Windows Software Development Kit (SDK) for Windows 8.1.</span></span> <span data-ttu-id="71769-108">造訪 [下載以供開發人員]( https://msdn.microsoft.com/windows/apps/br229516.aspx) 取得。</span><span class="sxs-lookup"><span data-stu-id="71769-108">Visit [Downloads for developers]( https://msdn.microsoft.com/windows/apps/br229516.aspx) to get them.</span></span>

<span data-ttu-id="71769-109">MakeAppx.exe 工具通常會在下列位置找到：</span><span class="sxs-lookup"><span data-stu-id="71769-109">The MakeAppx.exe tool is typically found at these locations:</span></span>

-   <span data-ttu-id="71769-110">在 x86： C： \\ Program files (x86) \\ windows 套件 \\ 8.0 \\ Bin \\ x86 \\makeappx.exe 或 C： \\ Program files (x86) \\ windows 套件 \\ 8.1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="71769-110">On x86: C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
-   <span data-ttu-id="71769-111">在 x64 上的兩個位置：</span><span class="sxs-lookup"><span data-stu-id="71769-111">On x64 in two locations:</span></span>
    -   <span data-ttu-id="71769-112">C： \\ Program files (x86) \\ windows 套件 \\ 8.0 \\ Bin \\ x86 \\makeappx.exe 或 C： \\ program files (x86) \\ Windows 套件 \\ 8.1 \\ bin \\ x86 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="71769-112">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x86\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x86\\makeappx.exe</span></span>
    -   <span data-ttu-id="71769-113">C： \\ Program files (x86) \\ windows 套件 \\ 8.0 \\ Bin \\ x64 \\makeappx.exe 或 C： \\ program files (x86) \\ Windows 套件 \\ 8.1 \\ bin \\ x64 \\makeappx.exe</span><span class="sxs-lookup"><span data-stu-id="71769-113">C:\\Program Files (x86)\\Windows Kits\\8.0\\bin\\x64\\makeappx.exe or C:\\Program Files (x86)\\Windows Kits\\8.1\\bin\\x64\\makeappx.exe</span></span>

<span data-ttu-id="71769-114">沒有 ARM 版本的工具。</span><span class="sxs-lookup"><span data-stu-id="71769-114">There is no ARM version of the tool.</span></span>

-   [<span data-ttu-id="71769-115">使用目錄結構建立封裝</span><span class="sxs-lookup"><span data-stu-id="71769-115">To create a package using a directory structure</span></span>](#to-create-a-package-using-a-directory-structure)
-   [<span data-ttu-id="71769-116">使用對應檔建立封裝</span><span class="sxs-lookup"><span data-stu-id="71769-116">To create a package using a mapping file</span></span>](#to-create-a-package-using-a-mapping-file)
-   [<span data-ttu-id="71769-117">若要使用 SignTool 簽署封裝</span><span class="sxs-lookup"><span data-stu-id="71769-117">To sign the package using SignTool</span></span>](#to-sign-the-package-using-signtool)
-   [<span data-ttu-id="71769-118">從封裝解壓縮檔案</span><span class="sxs-lookup"><span data-stu-id="71769-118">To extract files from a package</span></span>](#to-extract-files-from-a-package)
-   [<span data-ttu-id="71769-119">使用目錄結構建立封裝套件組合</span><span class="sxs-lookup"><span data-stu-id="71769-119">To create a package bundle using a directory structure</span></span>](#to-create-a-package-bundle-using-a-directory-structure)
-   [<span data-ttu-id="71769-120">使用對應檔建立封裝套件組合</span><span class="sxs-lookup"><span data-stu-id="71769-120">To create a package bundle using a mapping file</span></span>](#to-create-a-package-bundle-using-a-mapping-file)
-   [<span data-ttu-id="71769-121">從套件組合解壓縮套件</span><span class="sxs-lookup"><span data-stu-id="71769-121">To extract packages from a bundle</span></span>](#to-extract-packages-from-a-bundle)
-   [<span data-ttu-id="71769-122">使用金鑰檔加密封裝</span><span class="sxs-lookup"><span data-stu-id="71769-122">To encrypt a package with a key file</span></span>](#to-encrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="71769-123">使用全域測試金鑰加密封裝</span><span class="sxs-lookup"><span data-stu-id="71769-123">To encrypt a package with a global test key</span></span>](#to-encrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="71769-124">使用金鑰檔解密封裝</span><span class="sxs-lookup"><span data-stu-id="71769-124">To decrypt a package with a key file</span></span>](#to-decrypt-a-package-with-a-key-file)
-   [<span data-ttu-id="71769-125">使用全域測試金鑰解密封裝</span><span class="sxs-lookup"><span data-stu-id="71769-125">To decrypt a package with a global test key</span></span>](#to-decrypt-a-package-with-a-global-test-key)
-   [<span data-ttu-id="71769-126">使用量</span><span class="sxs-lookup"><span data-stu-id="71769-126">Usage</span></span>](#usage)

## <a name="using-app-packager"></a><span data-ttu-id="71769-127">使用應用程式封裝工具</span><span class="sxs-lookup"><span data-stu-id="71769-127">Using App packager</span></span>

> [!Note]  
> <span data-ttu-id="71769-128">整個工具都支援相對路徑。</span><span class="sxs-lookup"><span data-stu-id="71769-128">Relative paths are supported throughout the tool.</span></span>

 

### <a name="to-create-a-package-using-a-directory-structure"></a><span data-ttu-id="71769-129">使用目錄結構建立封裝</span><span class="sxs-lookup"><span data-stu-id="71769-129">To create a package using a directory structure</span></span>

<span data-ttu-id="71769-130">將 AppxManifest.xml 放在包含應用程式的所有承載檔的目錄根目錄中。</span><span class="sxs-lookup"><span data-stu-id="71769-130">Place the AppxManifest.xml in the root of a directory containing all of the payload files for your app.</span></span> <span data-ttu-id="71769-131">系統會為應用程式套件建立相同的目錄結構，並在部署期間解壓縮封裝時可供使用。</span><span class="sxs-lookup"><span data-stu-id="71769-131">An identical directory structure is created for the app package, and will be available when the package is extracted at deployment time.</span></span>

1.  <span data-ttu-id="71769-132">將所有檔案都放在單一目錄結構中，視需要建立子目錄。</span><span class="sxs-lookup"><span data-stu-id="71769-132">Place all files in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="71769-133">建立有效的套件資訊清單，AppxManifest.xml，並將它放在根目錄中。</span><span class="sxs-lookup"><span data-stu-id="71769-133">Create a valid package manifest, AppxManifest.xml, and place it in the root directory.</span></span>

3.  <span data-ttu-id="71769-134">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="71769-134">Run this command:</span></span>

    <span data-ttu-id="71769-135">**MakeAppx pack/d** *input \_ directorypath* **/p** _filepath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="71769-135">**MakeAppx pack /d** *input\_directorypath* **/p** _filepath_**.appx**</span></span>

### <a name="to-create-a-package-using-a-mapping-file"></a><span data-ttu-id="71769-136">使用對應檔建立封裝</span><span class="sxs-lookup"><span data-stu-id="71769-136">To create a package using a mapping file</span></span>

1.  <span data-ttu-id="71769-137">建立有效的套件資訊清單，AppxManifest.xml。</span><span class="sxs-lookup"><span data-stu-id="71769-137">Create a valid package manifest, AppxManifest.xml.</span></span>

2.  <span data-ttu-id="71769-138">建立對應檔。</span><span class="sxs-lookup"><span data-stu-id="71769-138">Create a mapping file.</span></span> <span data-ttu-id="71769-139">第一行包含 **\[ \] 字串檔案**，接下來的幾行則會指定來源 (磁片) 和目的地 (封裝在加上引號的字串中) 路徑。</span><span class="sxs-lookup"><span data-stu-id="71769-139">The first line contains the string **\[Files\]**, and the lines that follow specify the source (disk) and destination (package) paths in quoted strings.</span></span>

    ``` syntax
    [Files]
    "C:\MyApp\StartPage.htm"     "default.html"
    "C:\MyApp\readme.txt"        "doc\readme.txt"
    "\\MyServer\path\icon.png"   "icon.png"
    "MyCustomManifest.xml"       "AppxManifest.xml"
    ```

3.  <span data-ttu-id="71769-140">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="71769-140">Run this command:</span></span>

    <span data-ttu-id="71769-141">**MakeAppx pack/f** *對應 \_ filepath* **/p** _filepath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="71769-141">**MakeAppx pack /f** *mapping\_filepath* **/p** _filepath_**.appx**</span></span>

### <a name="to-sign-the-package-using-signtool"></a><span data-ttu-id="71769-142">若要使用 SignTool 簽署封裝</span><span class="sxs-lookup"><span data-stu-id="71769-142">To sign the package using SignTool</span></span>

1.  <span data-ttu-id="71769-143">建立憑證。</span><span class="sxs-lookup"><span data-stu-id="71769-143">Create the certificate.</span></span> <span data-ttu-id="71769-144">資訊清單中列出的發行者必須符合簽署憑證的發行者主體資訊。</span><span class="sxs-lookup"><span data-stu-id="71769-144">The publisher listed in the manifest must match the publisher subject information of the signing certificate.</span></span> <span data-ttu-id="71769-145">如需建立簽署憑證的詳細資訊，請參閱 [如何建立應用程式套件簽署憑證](how-to-create-a-package-signing-certificate.md)。</span><span class="sxs-lookup"><span data-stu-id="71769-145">For more info about creating a signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span>

2.  <span data-ttu-id="71769-146">執行 SignTool.exe 以簽署套件：</span><span class="sxs-lookup"><span data-stu-id="71769-146">Run SignTool.exe to sign the package:</span></span>

    <span data-ttu-id="71769-147">**SignTool sign/a/v/Fd** *hashAlgorithm* **/f** *certFileName* _filepath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="71769-147">**SignTool sign /a /v /fd** *hashAlgorithm* **/f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="71769-148">*HashAlgorithm* 必須符合在封裝應用程式時用來建立 blockmap 的雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="71769-148">The *hashAlgorithm* must match the hash algorithm used to create the blockmap when the app was packaged.</span></span> <span data-ttu-id="71769-149">使用 MakeAppx 封裝公用程式時，預設 Appx blockmap 雜湊演算法是 **SHA256**。</span><span class="sxs-lookup"><span data-stu-id="71769-149">With the MakeAppx packaging utility, the default Appx blockmap hash algorithm is **SHA256**.</span></span> <span data-ttu-id="71769-150">執行 SignTool.exe 指定 **SHA256** 作為檔案摘要 (/fd) 演算法：</span><span class="sxs-lookup"><span data-stu-id="71769-150">Run SignTool.exe specifying **SHA256** as the file digest (/fd) algorithm:</span></span>

    <span data-ttu-id="71769-151">**SignTool sign/a/v/FD SHA256/F** *certFileName* _filepath_**. appx**</span><span class="sxs-lookup"><span data-stu-id="71769-151">**SignTool sign /a /v /fd SHA256 /f** *certFileName* _filepath_**.appx**</span></span>

    <span data-ttu-id="71769-152">如需如何簽署套件的詳細資訊，請參閱 [如何使用 SignTool 簽署應用程式套件](how-to-sign-a-package-using-signtool.md)。</span><span class="sxs-lookup"><span data-stu-id="71769-152">For more info about how to sign packages, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span>

### <a name="to-extract-files-from-a-package"></a><span data-ttu-id="71769-153">從封裝解壓縮檔案</span><span class="sxs-lookup"><span data-stu-id="71769-153">To extract files from a package</span></span>

1.  <span data-ttu-id="71769-154">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="71769-154">Run this command:</span></span>

    <span data-ttu-id="71769-155">**MakeAppx 解壓縮/p** __ **. .appx/d** *輸出 \_ 目錄*</span><span class="sxs-lookup"><span data-stu-id="71769-155">**MakeAppx unpack /p** _file_**.appx /d** *output\_directory*</span></span>

2.  <span data-ttu-id="71769-156">解除封裝的套件與安裝的套件具有相同的結構。</span><span class="sxs-lookup"><span data-stu-id="71769-156">The unpacked package has the same structure as the installed package.</span></span>

### <a name="to-create-a-package-bundle-using-a-directory-structure"></a><span data-ttu-id="71769-157">使用目錄結構建立封裝套件組合</span><span class="sxs-lookup"><span data-stu-id="71769-157">To create a package bundle using a directory structure</span></span>

<span data-ttu-id="71769-158">我們會使用套件 **組合命令，** 在</span><span class="sxs-lookup"><span data-stu-id="71769-158">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="71769-159">藉由從 (加入所有封裝， <content directory> 包括) 的子資料夾。</span><span class="sxs-lookup"><span data-stu-id="71769-159">by adding all packages from <content directory> (including subfolders).</span></span> <span data-ttu-id="71769-160">如果 <content directory> 包含套件組合資訊清單，AppxBundleManifest.xml，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="71769-160">If <content directory> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="71769-161">將所有套件都放在單一目錄結構中，視需要建立子目錄。</span><span class="sxs-lookup"><span data-stu-id="71769-161">Place all packages in a single directory structure, creating subdirectories as desired.</span></span>

2.  <span data-ttu-id="71769-162">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="71769-162">Run this command:</span></span>

    <span data-ttu-id="71769-163">**MakeAppx 組合/d** *輸入 \_ directorypath* **/p** _filepath_**. .appxbundle**</span><span class="sxs-lookup"><span data-stu-id="71769-163">**MakeAppx bundle /d** *input\_directorypath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-create-a-package-bundle-using-a-mapping-file"></a><span data-ttu-id="71769-164">使用對應檔建立封裝套件組合</span><span class="sxs-lookup"><span data-stu-id="71769-164">To create a package bundle using a mapping file</span></span>

<span data-ttu-id="71769-165">我們會使用套件 **組合命令，** 在</span><span class="sxs-lookup"><span data-stu-id="71769-165">We use the **bundle** command to create an app bundle at</span></span> <output bundle name> <span data-ttu-id="71769-166">藉由在中從套件清單加入所有套件 <mapping file> 。</span><span class="sxs-lookup"><span data-stu-id="71769-166">by adding all packages from a list of packages within <mapping file>.</span></span> <span data-ttu-id="71769-167">如果 <mapping file> 包含套件組合資訊清單，AppxBundleManifest.xml，則會予以忽略。</span><span class="sxs-lookup"><span data-stu-id="71769-167">If <mapping file> contains a bundle manifest, AppxBundleManifest.xml, it is ignored.</span></span>

1.  <span data-ttu-id="71769-168">建立 <mapping file>。</span><span class="sxs-lookup"><span data-stu-id="71769-168">Create a <mapping file>.</span></span> <span data-ttu-id="71769-169">第一行包含 **\[ \] 字串檔案**，接下來的幾行指定要加入套件組合的封裝。</span><span class="sxs-lookup"><span data-stu-id="71769-169">The first line contains the string **\[Files\]**, and the lines that follow specify the packages to add to the bundle.</span></span> <span data-ttu-id="71769-170">每個套件都是由引號中的一組路徑所描述，並以空格或定位字元分隔。</span><span class="sxs-lookup"><span data-stu-id="71769-170">Each package is described by a pair of paths in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="71769-171">成對的路徑代表磁片) 上的套件來源 (以及套件組合) 中的目的地 (。</span><span class="sxs-lookup"><span data-stu-id="71769-171">The pair of paths represents the package's source (on disk) and destination (in bundle).</span></span> <span data-ttu-id="71769-172">所有目的地封裝名稱的副檔名都必須是 .appx。</span><span class="sxs-lookup"><span data-stu-id="71769-172">All destination package names must have the .appx extension.</span></span>

    ``` syntax
        [Files]
        "C:\MyApp\MyApp_x86.appx"                 "MyApp_x86.appx"
        "C:\Program Files (x86)\ResPack.appx"    "resources\resPack.appx"
        "\\MyServer\path\ResPack.appx"           "Respack.appx"
        "my app files\respack.appx"              "my app files\respack.appx"
    ```

2.  <span data-ttu-id="71769-173">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="71769-173">Run this command:</span></span>

    <span data-ttu-id="71769-174">**MakeAppx 組合/f** *對應 \_ filepath* **/p** _filepath_ \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="71769-174">**MakeAppx bundle /f** *mapping\_filepath* **/p** _filepath_**.appxbundle**</span></span>

### <a name="to-extract-packages-from-a-bundle"></a><span data-ttu-id="71769-175">從套件組合解壓縮套件</span><span class="sxs-lookup"><span data-stu-id="71769-175">To extract packages from a bundle</span></span>

1.  <span data-ttu-id="71769-176">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="71769-176">Run this command:</span></span>

    <span data-ttu-id="71769-177">**MakeAppx 解除配套/p** _組合 \_ 名稱_**.appxbundle/d** *輸出 \_ 目錄*</span><span class="sxs-lookup"><span data-stu-id="71769-177">**MakeAppx unbundle /p** _bundle\_name_**.appxbundle /d** *output\_directory*</span></span>

2.  <span data-ttu-id="71769-178">解除封裝的組合具有與已安裝套件配套相同的結構。</span><span class="sxs-lookup"><span data-stu-id="71769-178">The unpacked bundle has the same structure as the installed package bundle.</span></span>

### <a name="to-encrypt-a-package-with-a-key-file"></a><span data-ttu-id="71769-179">使用金鑰檔加密封裝</span><span class="sxs-lookup"><span data-stu-id="71769-179">To encrypt a package with a key file</span></span>

1.  <span data-ttu-id="71769-180">建立金鑰檔。</span><span class="sxs-lookup"><span data-stu-id="71769-180">Create a key file.</span></span> <span data-ttu-id="71769-181">金鑰檔必須以包含字串「機碼」的行開頭， \[ \] 後面接著描述用來加密封裝之金鑰的行。</span><span class="sxs-lookup"><span data-stu-id="71769-181">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="71769-182">每個索引鍵都是由引號中的一組字串所描述，並以空格或定位字元分隔。</span><span class="sxs-lookup"><span data-stu-id="71769-182">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="71769-183">第一個字串代表金鑰識別碼，而第二個字串表示以十六進位形式表示的加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="71769-183">The first string represents the key ID and the second string represents the encryption key in hexadecimal form.</span></span>

    ``` syntax
        [Keys]
        "0"                 "1AC4CDCFF1924D2885A0607269787BA6BF09B7FFEBF74ED4B9D86E423CF9186B"
    ```

2.  <span data-ttu-id="71769-184">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="71769-184">Run this command:</span></span>

    <span data-ttu-id="71769-185">**MakeAppx.exe 加密/p** _封裝 \_ 名稱_**.appx/ep** _加密的 \_ 封裝 \_ 名稱_**. eappx/kf** _keyfile \_ 名稱_**.txt**</span><span class="sxs-lookup"><span data-stu-id="71769-185">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="71769-186">輸入封裝會使用提供的金鑰檔加密為指定的加密封裝。</span><span class="sxs-lookup"><span data-stu-id="71769-186">The input package will be encrypted into the specified encrypted package using the provided key file.</span></span>

### <a name="to-encrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="71769-187">使用全域測試金鑰加密封裝</span><span class="sxs-lookup"><span data-stu-id="71769-187">To encrypt a package with a global test key</span></span>

1.  <span data-ttu-id="71769-188">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="71769-188">Run this command:</span></span>

    <span data-ttu-id="71769-189">**MakeAppx.exe 加密/p** _封裝 \_ 名稱_**.appx/ep** _加密的 \_ 封裝 \_ 名稱_**. eappx/kt**</span><span class="sxs-lookup"><span data-stu-id="71769-189">**MakeAppx.exe encrypt /p** _package\_name_**.appx /ep** _encrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="71769-190">輸入封裝將會使用全域測試金鑰加密為指定的加密封裝。</span><span class="sxs-lookup"><span data-stu-id="71769-190">The input package will be encrypted into the specified encrypted package using the global test key.</span></span>

### <a name="to-decrypt-a-package-with-a-key-file"></a><span data-ttu-id="71769-191">使用金鑰檔解密封裝</span><span class="sxs-lookup"><span data-stu-id="71769-191">To decrypt a package with a key file</span></span>

1.  <span data-ttu-id="71769-192">建立金鑰檔。</span><span class="sxs-lookup"><span data-stu-id="71769-192">Create a key file.</span></span> <span data-ttu-id="71769-193">金鑰檔必須以包含字串「機碼」的行開頭， \[ \] 後面接著描述用來加密封裝之金鑰的行。</span><span class="sxs-lookup"><span data-stu-id="71769-193">Key files must begin with a line containing the string "\[Keys\]" followed by lines describing the keys to encrypt the package with.</span></span> <span data-ttu-id="71769-194">每個索引鍵都是由引號中的一組字串所描述，並以空格或定位字元分隔。</span><span class="sxs-lookup"><span data-stu-id="71769-194">Each key is described by a pair of strings in quotation marks, separated by spaces or tabs.</span></span> <span data-ttu-id="71769-195">第一個字串代表 base64 編碼的32位元組金鑰識別碼，而第二個字串代表 base64 編碼的32位元組加密金鑰。</span><span class="sxs-lookup"><span data-stu-id="71769-195">The first string represents the base64 encoded 32-byte key ID and the second string represents the base64 encoded 32-byte encryption key.</span></span>

    ``` syntax
        [Keys]
        "OWVwSzliRGY1VWt1ODk4N1Q4R2Vqc04zMzIzNnlUREU="                 "MjNFTlFhZGRGZEY2YnVxMTBocjd6THdOdk9pZkpvelc="
    ```

2.  <span data-ttu-id="71769-196">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="71769-196">Run this command:</span></span>

    <span data-ttu-id="71769-197">**MakeAppx.exe 解密/p** _封裝 \_ 名稱_**. appx/ep** _未加密的 \_ 封裝 \_ 名稱_**。 eappx/kf** _keyfile \_ 名稱_**.txt**</span><span class="sxs-lookup"><span data-stu-id="71769-197">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kf** _keyfile\_name_**.txt**</span></span>

3.  <span data-ttu-id="71769-198">輸入封裝會使用提供的金鑰檔解密為指定的未加密封裝。</span><span class="sxs-lookup"><span data-stu-id="71769-198">The input package will be decrypted into the specified unencrypted package using the provided key file.</span></span>

### <a name="to-decrypt-a-package-with-a-global-test-key"></a><span data-ttu-id="71769-199">使用全域測試金鑰解密封裝</span><span class="sxs-lookup"><span data-stu-id="71769-199">To decrypt a package with a global test key</span></span>

1.  <span data-ttu-id="71769-200">請執行這個命令：</span><span class="sxs-lookup"><span data-stu-id="71769-200">Run this command:</span></span>

    <span data-ttu-id="71769-201">**MakeAppx.exe 解密/p** _封裝 \_ 名稱_**. appx/ep** _未加密的 \_ 封裝 \_ 名稱_**。 eappx/kt**</span><span class="sxs-lookup"><span data-stu-id="71769-201">**MakeAppx.exe decrypt /p** _package\_name_**.appx /ep** _unencrypted\_package\_name_**.eappx /kt**</span></span>

2.  <span data-ttu-id="71769-202">輸入封裝將會使用全域測試金鑰解密至指定的未加密封裝中。</span><span class="sxs-lookup"><span data-stu-id="71769-202">The input package will be decrypted into the specified unencrypted package using the global test key.</span></span>

## <a name="usage"></a><span data-ttu-id="71769-203">使用方式</span><span class="sxs-lookup"><span data-stu-id="71769-203">Usage</span></span>

<span data-ttu-id="71769-204">命令列引數 **/p** 一律是必要的，其中包含 **/d**、 **/f** 或 **/ep**。</span><span class="sxs-lookup"><span data-stu-id="71769-204">The command line argument **/p** is always required, with either **/d**, **/f**, or **/ep**.</span></span> <span data-ttu-id="71769-205">請注意， **/d**、 **/f** 和 **/ep** 互斥。</span><span class="sxs-lookup"><span data-stu-id="71769-205">Note that **/d**, **/f**, and **/ep** are mutually exclusive.</span></span>

<span data-ttu-id="71769-206">**MakeAppx pack \[ 選項 \]** **/p** *\<output package name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="71769-206">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="71769-207">**MakeAppx pack \[ 選項 \]** **/p** *\<output package name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="71769-207">**MakeAppx pack \[options\]** **/p** *\<output package name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="71769-208">**MakeAppx 解壓縮 \[ 選項 \]** **/p** *\<input package name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="71769-208">**MakeAppx unpack \[options\]** **/p** *\<input package name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="71769-209">**MakeAppx 套件 \[ 組合 \] 選項** **/p** *\<output bundle name\>* \**/d\*\*\*\<content directory\>*</span><span class="sxs-lookup"><span data-stu-id="71769-209">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/d** *\<content directory\>*</span></span>

<span data-ttu-id="71769-210">**MakeAppx 套件 \[ 組合 \] 選項** **/p** *\<output bundle name\>* \**/f\*\*\*\<mapping file\>*</span><span class="sxs-lookup"><span data-stu-id="71769-210">**MakeAppx bundle \[options\]** **/p** *\<output bundle name\>* **/f** *\<mapping file\>*</span></span>

<span data-ttu-id="71769-211">**MakeAppx 解除配套 \[ options \]** **/p** *\<input bundle name\>* \**/d\*\*\*\<output directory\>*</span><span class="sxs-lookup"><span data-stu-id="71769-211">**MakeAppx unbundle \[options\]** **/p** *\<input bundle name\>* **/d** *\<output directory\>*</span></span>

<span data-ttu-id="71769-212">**MakeAppx encrypt \[ 選項 \]** **/p** *\<input package name\>* \**/ep\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="71769-212">**MakeAppx encrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

<span data-ttu-id="71769-213">**MakeAppx 解密 \[ 選項 \]** **/p** *\<input package name\>* \**/ep\*\*\*\<output package name\>*</span><span class="sxs-lookup"><span data-stu-id="71769-213">**MakeAppx decrypt \[options\]** **/p** *\<input package name\>* **/ep** *\<output package name\>*</span></span>

## <a name="command-line-syntax"></a><span data-ttu-id="71769-214">命令列語法</span><span class="sxs-lookup"><span data-stu-id="71769-214">Command-line Syntax</span></span>

<span data-ttu-id="71769-215">以下是 MakeAppx 的命令列常見使用語法。</span><span class="sxs-lookup"><span data-stu-id="71769-215">Here is the command-line common usage syntax for MakeAppx.</span></span>

<span data-ttu-id="71769-216">**MakeAppx \[ pack \| 解壓縮套件組合 \| \| 解除配套 \| 加密 encrypt \| \]** \[ **/h** **/kf** **/kt** **/l** **/o** **/no** **/nv** **/v** **/pfn** **/？**\]</span><span class="sxs-lookup"><span data-stu-id="71769-216">**MakeAppx \[pack\|unpack\|bundle\|unbundle\|encrypt\|decrypt\]** \[**/h** **/kf** **/kt** **/l** **/o** **/no** **/nv** **/v** **/pfn** **/?**\]</span></span>

<span data-ttu-id="71769-217">**MakeAppx** 會封裝或解壓縮套件中的檔案、配套或 unbundles 套件組合中的套件，或加密或解密指定輸入目錄或對應檔中的應用程式套件或套件組合。</span><span class="sxs-lookup"><span data-stu-id="71769-217">**MakeAppx** packs or unpacks the files in a package, bundles or unbundles the packages in a bundle, or encrypts or decrypts the app package or bundle in the specified input directory or mapping file.</span></span> <span data-ttu-id="71769-218">以下是適用于 **MakeAppx pack**、 **MakeAppx 解壓縮**、 **MakeAppx** 配套、 **MakeAppx 解除配套**、 **MakeAppx 加密** 或 **MakeAppx 解密** 的參數清單。</span><span class="sxs-lookup"><span data-stu-id="71769-218">Here is the list of parameters that apply to **MakeAppx pack**, **MakeAppx unpack**, **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, or **MakeAppx decrypt**.</span></span>

<dl> <dt>

<span data-ttu-id="71769-219"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="71769-219"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="71769-220">此選項用於當地語系化的封裝。</span><span class="sxs-lookup"><span data-stu-id="71769-220">This option is used for localized packages.</span></span> <span data-ttu-id="71769-221">預設驗證是針對當地語系化的套件進行。</span><span class="sxs-lookup"><span data-stu-id="71769-221">The default validation trips on localized packages.</span></span> <span data-ttu-id="71769-222">此選項只會停用該特定驗證，而不需要停用所有驗證。</span><span class="sxs-lookup"><span data-stu-id="71769-222">This option disables only that specific validation, without requiring that all validation be disabled.</span></span>

</dd> <dt>

<span data-ttu-id="71769-223"><span id="_o"></span><span id="_O"></span>**/o**</span><span class="sxs-lookup"><span data-stu-id="71769-223"><span id="_o"></span><span id="_O"></span>**/o**</span></span>
</dt> <dd>

<span data-ttu-id="71769-224">如果輸出檔案存在，請予以覆寫。</span><span class="sxs-lookup"><span data-stu-id="71769-224">Overwrite the output file if it exists.</span></span> <span data-ttu-id="71769-225">如果您未指定此選項或 **/no** 選項，則會詢問使用者是否要覆寫檔案。</span><span class="sxs-lookup"><span data-stu-id="71769-225">If you don't specify this option or the **/no** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="71769-226">您無法將此選項與 **/no** 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="71769-226">You can't use this option with **/no**.</span></span>

</dd> <dt>

<span data-ttu-id="71769-227"><span id="_no"></span><span id="_NO"></span>**/no**</span><span class="sxs-lookup"><span data-stu-id="71769-227"><span id="_no"></span><span id="_NO"></span>**/no**</span></span>
</dt> <dd>

<span data-ttu-id="71769-228">如果有，可以避免覆寫輸出檔案。</span><span class="sxs-lookup"><span data-stu-id="71769-228">Prevents an overwrite of the output file if it exists.</span></span> <span data-ttu-id="71769-229">如果您未指定此選項或 **/o** 選項，系統會詢問使用者是否要覆寫檔案。</span><span class="sxs-lookup"><span data-stu-id="71769-229">If you don't specify this option or the **/o** option, the user is asked whether they want to overwrite the file.</span></span>

<span data-ttu-id="71769-230">您無法搭配使用此選項與 **/o**。</span><span class="sxs-lookup"><span data-stu-id="71769-230">You can't use this option with **/o**.</span></span>

</dd> <dt>

<span data-ttu-id="71769-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span><span class="sxs-lookup"><span data-stu-id="71769-231"><span id="_nv"></span><span id="_NV"></span>**/nv**</span></span>
</dt> <dd>

<span data-ttu-id="71769-232">略過語意驗證。</span><span class="sxs-lookup"><span data-stu-id="71769-232">Skip semantic validation.</span></span> <span data-ttu-id="71769-233">如果您沒有指定此選項，工具會對套件執行完整驗證。</span><span class="sxs-lookup"><span data-stu-id="71769-233">If you don't specify this option, the tool performs a full validation of the package.</span></span>

</dd> <dt>

<span data-ttu-id="71769-234"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="71769-234"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="71769-235">啟用主控台的詳細資訊記錄輸出。</span><span class="sxs-lookup"><span data-stu-id="71769-235">Enable verbose logging output to the console.</span></span>

</dd> <dt>

<span data-ttu-id="71769-236"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="71769-236"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="71769-237">顯示解說文字。</span><span class="sxs-lookup"><span data-stu-id="71769-237">Display help text.</span></span>

</dd> </dl>

<span data-ttu-id="71769-238">**MakeAppx pack** 、 **MakeAppx 解壓縮** 、 **MakeAppx** 配套、 **MakeAppx 解除配套**、 **MakeAppx 加密** 和 **MakeAppx 解密** 都是互斥的命令。</span><span class="sxs-lookup"><span data-stu-id="71769-238">**MakeAppx pack** , **MakeAppx unpack** , **MakeAppx bundle**, **MakeAppx unbundle**, **MakeAppx encrypt**, and **MakeAppx decrypt** are mutually exclusive commands.</span></span> <span data-ttu-id="71769-239">以下是特別適用于每個命令的命令列參數：</span><span class="sxs-lookup"><span data-stu-id="71769-239">Here are the command-line parameters that apply specifically to each command:</span></span>

<span data-ttu-id="71769-240">**MakeAppx 套件** \[**h**\]</span><span class="sxs-lookup"><span data-stu-id="71769-240">**MakeAppx pack** \[**h**\]</span></span>

<span data-ttu-id="71769-241">建立套件。</span><span class="sxs-lookup"><span data-stu-id="71769-241">Creates a package.</span></span>

<dl> <dt>

<span data-ttu-id="71769-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** *演算法*</span><span class="sxs-lookup"><span data-stu-id="71769-242"><span id="_h_algorithm"></span><span id="_H_ALGORITHM"></span>**/h** *algorithm*</span></span>
</dt> <dd>

<span data-ttu-id="71769-243">指定建立區塊對應時要使用的雜湊演算法。</span><span class="sxs-lookup"><span data-stu-id="71769-243">Specifies the hash algorithm to use when creating the block map.</span></span> <span data-ttu-id="71769-244">以下是有效的 *演算法* 值：</span><span class="sxs-lookup"><span data-stu-id="71769-244">Here are valid values for *algorithm*:</span></span>

<dl> <dd><span data-ttu-id="71769-245">SHA256 (預設)</span><span class="sxs-lookup"><span data-stu-id="71769-245">SHA256 (default)</span></span></dd> <dd><span data-ttu-id="71769-246">SHA384</span><span class="sxs-lookup"><span data-stu-id="71769-246">SHA384</span></span></dd> <dd><span data-ttu-id="71769-247">SHA512</span><span class="sxs-lookup"><span data-stu-id="71769-247">SHA512</span></span></dd> </dl>

<span data-ttu-id="71769-248">您無法使用此選項搭配 **解壓縮** 命令。</span><span class="sxs-lookup"><span data-stu-id="71769-248">You can't use this option with the **unpack** command.</span></span>

</dd> </dl>

<span data-ttu-id="71769-249">**MakeAppx 解壓縮** \[**pfn**\]</span><span class="sxs-lookup"><span data-stu-id="71769-249">**MakeAppx unpack** \[**pfn**\]</span></span>

<span data-ttu-id="71769-250">將指定套件中的所有檔案解壓縮到指定的輸出目錄。</span><span class="sxs-lookup"><span data-stu-id="71769-250">Extracts all files in the specified package to the specified output directory.</span></span> <span data-ttu-id="71769-251">輸出的目錄結構與封裝相同。</span><span class="sxs-lookup"><span data-stu-id="71769-251">The output has the same directory structure as the package.</span></span>

<dl> <dt>

<span data-ttu-id="71769-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="71769-252"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="71769-253">使用封裝的完整名稱指定名稱為的目錄。</span><span class="sxs-lookup"><span data-stu-id="71769-253">Specifies a directory named with the package full name.</span></span> <span data-ttu-id="71769-254">此目錄會建立在所提供的輸出位置下。</span><span class="sxs-lookup"><span data-stu-id="71769-254">This directory is created under the provided output location.</span></span> <span data-ttu-id="71769-255">您無法使用此選項搭配 **pack** 命令。</span><span class="sxs-lookup"><span data-stu-id="71769-255">You can't use this option with the **pack** command.</span></span>

</dd> </dl>

<span data-ttu-id="71769-256">**MakeAppx 解除配套** \[**pfn**\]</span><span class="sxs-lookup"><span data-stu-id="71769-256">**MakeAppx unbundle** \[**pfn**\]</span></span>

<span data-ttu-id="71769-257">將所有套件解壓縮至指定的輸出路徑底下的子目錄，並以配套的完整名稱命名。</span><span class="sxs-lookup"><span data-stu-id="71769-257">Unpacks all packages to a subdirectory under the specified output path, named after the bundle full name.</span></span> <span data-ttu-id="71769-258">輸出具有與已安裝套件配套相同的目錄結構。</span><span class="sxs-lookup"><span data-stu-id="71769-258">The output has the same directory structure as the installed package bundle.</span></span>

<dl> <dt>

<span data-ttu-id="71769-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span><span class="sxs-lookup"><span data-stu-id="71769-259"><span id="_pfn"></span><span id="_PFN"></span>**/pfn**</span></span>
</dt> <dd>

<span data-ttu-id="71769-260">使用封裝套件組合的完整名稱指定名為的目錄。</span><span class="sxs-lookup"><span data-stu-id="71769-260">Specifies a directory named with the package bundle full name.</span></span> <span data-ttu-id="71769-261">此目錄會建立在所提供的輸出位置下。</span><span class="sxs-lookup"><span data-stu-id="71769-261">This directory is created under the provided output location.</span></span> <span data-ttu-id="71769-262">您無法使用此選項搭配套件 **組合命令。**</span><span class="sxs-lookup"><span data-stu-id="71769-262">You can't use this option with the **bundle** command.</span></span>

</dd> </dl>

<span data-ttu-id="71769-263">**MakeAppx 加密** \[**kf**、 **kt**\]</span><span class="sxs-lookup"><span data-stu-id="71769-263">**MakeAppx encrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="71769-264">從指定之輸出封裝的指定輸入應用程式封裝建立加密應用程式封裝。</span><span class="sxs-lookup"><span data-stu-id="71769-264">Creates an encrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="71769-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/kf\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="71769-265"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="71769-266">使用指定金鑰檔中的金鑰來加密封裝或套件組合。</span><span class="sxs-lookup"><span data-stu-id="71769-266">Encrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="71769-267">您無法將此選項與 **kt** 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="71769-267">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="71769-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="71769-268"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="71769-269">使用全域測試金鑰來加密封裝或套件組合。</span><span class="sxs-lookup"><span data-stu-id="71769-269">Encrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="71769-270">您無法將此選項與 **kf** 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="71769-270">You can't use this option with **kf**.</span></span>

</dd> </dl>

<span data-ttu-id="71769-271">**MakeAppx 解密** \[**kf**、 **kt**\]</span><span class="sxs-lookup"><span data-stu-id="71769-271">**MakeAppx decrypt** \[**kf**, **kt**\]</span></span>

<span data-ttu-id="71769-272">從指定之輸出封裝的指定輸入應用程式封裝，建立未加密的應用程式套件。</span><span class="sxs-lookup"><span data-stu-id="71769-272">Creates an unencrypted app package from the specified input app package at the specified output package.</span></span>

<dl> <dt>

<span data-ttu-id="71769-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>\**/kf\*\*\*<key file>*</span><span class="sxs-lookup"><span data-stu-id="71769-273"><span id="_kf__key_file_"></span><span id="_KF__KEY_FILE_"></span>**/kf** *<key file>*</span></span>
</dt> <dd>

<span data-ttu-id="71769-274">使用指定金鑰檔中的金鑰來解密封裝或套件組合。</span><span class="sxs-lookup"><span data-stu-id="71769-274">Decrypts the package or bundle using the key from the specified key file.</span></span> <span data-ttu-id="71769-275">您無法將此選項與 **kt** 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="71769-275">You can't use this option with **kt**.</span></span>

</dd> <dt>

<span data-ttu-id="71769-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span><span class="sxs-lookup"><span data-stu-id="71769-276"><span id="_kt"></span><span id="_KT"></span>**/kt**</span></span>
</dt> <dd>

<span data-ttu-id="71769-277">使用全域測試金鑰來解密封裝或組合。</span><span class="sxs-lookup"><span data-stu-id="71769-277">Decrypts the package or bundle using the global test key.</span></span> <span data-ttu-id="71769-278">您無法將此選項與 **kf** 搭配使用。</span><span class="sxs-lookup"><span data-stu-id="71769-278">You can't use this option with **kf**.</span></span>

</dd> </dl>

## <a name="semantic-validation-performed-by-makeappx"></a><span data-ttu-id="71769-279">MakeAppx 執行的語意驗證</span><span class="sxs-lookup"><span data-stu-id="71769-279">Semantic validation performed by MakeAppx</span></span>

<span data-ttu-id="71769-280">MakeAppx 會執行有限的語意驗證，其設計目的是要攔截最常見的部署錯誤，並協助確保應用程式封裝有效。</span><span class="sxs-lookup"><span data-stu-id="71769-280">MakeAppx performs limited semantic validation that is designed to catch the most common deployment errors and help ensure that the app package is valid.</span></span>

<span data-ttu-id="71769-281">此驗證可確保︰</span><span class="sxs-lookup"><span data-stu-id="71769-281">This validation ensures that:</span></span>

-   <span data-ttu-id="71769-282">在套件資訊清單中參考的所有檔案都包含在應用程式套件中。</span><span class="sxs-lookup"><span data-stu-id="71769-282">All files referenced in the package manifest are included in the app package.</span></span>
-   <span data-ttu-id="71769-283">應用程式不會有兩個相同的金鑰。</span><span class="sxs-lookup"><span data-stu-id="71769-283">An application does not have two identical keys.</span></span>
-   <span data-ttu-id="71769-284">應用程式不會從這份清單註冊禁止的通訊協定： SMB、檔案、MS-WWA-WEB、WWA。</span><span class="sxs-lookup"><span data-stu-id="71769-284">An application does not register for a forbidden protocol from this list: SMB , FILE, MS-WWA-WEB, MS-WWA.</span></span>

<span data-ttu-id="71769-285">此語意驗證未完成，而且 MakeAppx 所建立的套件不保證可供安裝。</span><span class="sxs-lookup"><span data-stu-id="71769-285">This semantic validation is not complete, and packages built by MakeAppx are not guaranteed to be installable.</span></span>

 

 