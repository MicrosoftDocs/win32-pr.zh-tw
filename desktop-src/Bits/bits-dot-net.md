---
title: 使用參考 Dll 從 .NET 使用 BITS
description: 下列範例示範如何從 .NET 程式呼叫 BITS COM 介面
ms.assetid: 1058970C-CE81-47D6-950E-3B6289E956B6
ms.topic: article
ms.date: 11/13/2018
ms.openlocfilehash: c359bafe4f1937d49a6ec21896af32606a2ae894
ms.sourcegitcommit: 00e0a8e56d28c4c720b97f0cf424c29f547460d7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "103679255"
---
# <a name="calling-into-bits-from-net-and-c-using-reference-dlls"></a><span data-ttu-id="4999e-103">使用參考 Dll 從 .NET 和 c # 呼叫 BITS</span><span class="sxs-lookup"><span data-stu-id="4999e-103">Calling into BITS from .NET and C# using Reference DLLs</span></span>

<span data-ttu-id="4999e-104">從 .NET 程式呼叫 BITS COM 類別的其中一種方式，就是使用[MIDL](/windows/desktop/Midl/using-the-midl-compiler-2)和[tlbimp.exe](/dotnet/framework/tools/tlbimp-exe-type-library-importer)工具，從 Windows SDK 中的位[IDL](/windows/desktop/Midl/midl-start-page) (介面定義語言) 檔案建立參考 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-104">One way to call into the BITS COM classes from a .NET program is to create a reference DLL file starting with the BITS [IDL](/windows/desktop/Midl/midl-start-page) (Interface Definition Language) files in the Windows SDK, using the [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) and [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) tools.</span></span> <span data-ttu-id="4999e-105">參考 DLL 是 BITS COM 類別的一組類別包裝函式;然後，您可以直接從 .NET 使用包裝函式類別。</span><span class="sxs-lookup"><span data-stu-id="4999e-105">The reference DLL is a set of class wrappers for the BITS COM classes; you can then use the wrapper classes directly from .NET.</span></span>

<span data-ttu-id="4999e-106">使用自動建立之參考 Dll 的替代方法是使用來自 [GitHub](https://github.com/) 和 [NuGet](https://www.nuget.org/)的協力廠商 .net 位包裝函式。</span><span class="sxs-lookup"><span data-stu-id="4999e-106">An alternative to using automatically-created reference DLLs is to use a 3rd party .NET BITS wrapper from [GitHub](https://github.com/) and [NuGet](https://www.nuget.org/).</span></span> <span data-ttu-id="4999e-107">這些包裝函式通常有更自然的 .NET 程式設計樣式，但它們可能會落後 BITS 介面中的變更和更新。</span><span class="sxs-lookup"><span data-stu-id="4999e-107">These wrappers often have a more natural .NET programming style but they might lag behind the changes and updates in the BITS interfaces.</span></span>

## <a name="creating-the-reference-dlls"></a><span data-ttu-id="4999e-108">建立參考 Dll</span><span class="sxs-lookup"><span data-stu-id="4999e-108">Creating the reference DLLs</span></span>
### <a name="bits-idl-files"></a><span data-ttu-id="4999e-109">BITS IDL 檔案</span><span class="sxs-lookup"><span data-stu-id="4999e-109">BITS IDL files</span></span>

<span data-ttu-id="4999e-110">您將從一組 BITS IDL 檔案開始。</span><span class="sxs-lookup"><span data-stu-id="4999e-110">You will start with the set of BITS IDL files.</span></span> <span data-ttu-id="4999e-111">這些是完整定義 BITS COM 介面的檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-111">These are files that fully define the BITS COM interface.</span></span> <span data-ttu-id="4999e-112">這些檔案位於 **Windows 套件** 目錄中，並命名為 bits *版本*.idl (例如，bits10_2 .idl) 除了版本1.0 檔案，也就是僅限 bits .idl。</span><span class="sxs-lookup"><span data-stu-id="4999e-112">The files are located in the **Windows Kits** directory and are named bits *version*.idl (for example, bits10_2.idl) except for the version 1.0 file which is just Bits.idl.</span></span> <span data-ttu-id="4999e-113">建立新版本的 BITS 時，也會建立新的 BITS IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-113">As new versions of BITS are created, new BITS IDL files are also created.</span></span>

<span data-ttu-id="4999e-114">您也可能想要修改一份 SDK 位 IDL 檔案，以使用未自動轉換成 .NET 對等專案的 BITS 功能。</span><span class="sxs-lookup"><span data-stu-id="4999e-114">You may also want to modify a copy of the SDK BITS IDL files to use BITS features that aren't automatically converted into .NET equivalents.</span></span> <span data-ttu-id="4999e-115">稍後會討論可能的 IDL 檔案變更。</span><span class="sxs-lookup"><span data-stu-id="4999e-115">Possible IDL file changes are discussed later on.</span></span>

<span data-ttu-id="4999e-116">BITS IDL 檔案包含其他數個以傳址方式提供的 IDL 檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-116">The BITS IDL files include several other IDL files by reference.</span></span> <span data-ttu-id="4999e-117">它們也會進行嵌套，因此，如果您使用一個版本，則會包含所有較低的版本。</span><span class="sxs-lookup"><span data-stu-id="4999e-117">They also nest, so that if you use one version, it includes all the lower versions.</span></span>

<span data-ttu-id="4999e-118">針對您想要在程式中作為目標的每個位版本，您將需要該版本的一個參考 DLL。</span><span class="sxs-lookup"><span data-stu-id="4999e-118">For each version of BITS that you want to target in your program you will need one reference DLL for that version.</span></span> <span data-ttu-id="4999e-119">例如，如果您想要撰寫可在 BITS 1.5 和更新版本上運作的程式，但在 BITS 10.2 存在時有其他功能，您需要轉換 bits1_5 .idl 和 bits10_2 .idl 檔。</span><span class="sxs-lookup"><span data-stu-id="4999e-119">For example, if you want to write a program that works on BITS 1.5 and up but has additional features when BITS 10.2 is present, you need to convert both the bits1_5.idl and bits10_2.idl files.</span></span>


### <a name="midl-and-tlbimp-utilities"></a><span data-ttu-id="4999e-120">MIDL 和 TLBIMP 公用程式</span><span class="sxs-lookup"><span data-stu-id="4999e-120">MIDL and TLBIMP utilities</span></span>

<span data-ttu-id="4999e-121">[MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft 介面定義語言) 公用程式會將描述 BITS COM 介面的 IDL 檔案，轉換成 TLB (型別程式庫) 檔。</span><span class="sxs-lookup"><span data-stu-id="4999e-121">The [MIDL](/windows/desktop/Midl/using-the-midl-compiler-2) (Microsoft Interface Definition Language) utility converts the IDL files that describe the BITS COM interface into a TLB (Type Library) file.</span></span> <span data-ttu-id="4999e-122">MIDL 工具相依于 CL 公用程式 (C 預處理器) ，以正確地讀取 IDL 語言檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-122">The MIDL tool depends on the CL utility (C preprocessor) to correctly read the IDL language file.</span></span> <span data-ttu-id="4999e-123">CL 公用程式是 Visual Studio 的一部分，當您在 Visual Studio 安裝中包含 C/c + + 功能時，會安裝此公用程式。</span><span class="sxs-lookup"><span data-stu-id="4999e-123">The CL utility is part of Visual Studio and is installed when you include C/C++ features in the Visual Studio installation.</span></span>

<span data-ttu-id="4999e-124">MIDL 公用程式通常會建立一組 C 和 H (C 語言程式碼和 C 語言標頭) 檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-124">The MIDL utility will normally create a set of C and H (C language code and C language header) files.</span></span> <span data-ttu-id="4999e-125">您可以藉由將輸出傳送至 NUL：裝置來隱藏這些額外的檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-125">You can suppress these extra files by sending the output to the NUL: device.</span></span> <span data-ttu-id="4999e-126">例如，設定/dlldata NUL： switch 將會隱藏 dlldata.c .c 檔案的建立。</span><span class="sxs-lookup"><span data-stu-id="4999e-126">For example, setting the /dlldata NUL: switch will suppress creating a dlldata.c file.</span></span> <span data-ttu-id="4999e-127">下列範例命令會顯示哪些參數應設定為 NUL：。</span><span class="sxs-lookup"><span data-stu-id="4999e-127">The sample commands below shows which switches should be set to NUL:.</span></span>

<span data-ttu-id="4999e-128">[Tlbimp.exe](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (型別程式庫匯入工具) 公用程式會讀取 TLB 檔案，並建立對應的參考 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-128">The [TLBIMP](/dotnet/framework/tools/tlbimp-exe-type-library-importer) (Type Library Importer) utility reads in a TLB file and creates the corresponding reference DLL file.</span></span> 


### <a name="example-commands-for-midl-and-tlbimp"></a><span data-ttu-id="4999e-129">MIDL 和 TLBIMP 的命令範例</span><span class="sxs-lookup"><span data-stu-id="4999e-129">Example commands for MIDL and TLBIMP</span></span>

<span data-ttu-id="4999e-130">這是用來產生一組參考檔案的完整命令集範例。</span><span class="sxs-lookup"><span data-stu-id="4999e-130">This is an example of the complete set of commands to generate a set of reference files.</span></span> <span data-ttu-id="4999e-131">您可能需要根據您的 Visual Studio 和 Windows SDK 安裝來修改命令，並根據您目標的 BITS 功能和作業系統版本。</span><span class="sxs-lookup"><span data-stu-id="4999e-131">You may need to modify the commands based on your Visual Studio and Windows SDK installation and based on the BITS features and OS versions you are targeting.</span></span> 

<span data-ttu-id="4999e-132">此範例會建立一個目錄來放置參考 DLL 檔案，並建立環境變數 BITSTEMP 來指向該目錄。</span><span class="sxs-lookup"><span data-stu-id="4999e-132">The example creates a directory to place the reference DLL files and creates an environment variable BITSTEMP to point to that directory.</span></span> 

<span data-ttu-id="4999e-133">然後，範例命令會執行 Visual Studio 安裝程式所建立的 vsdevcmd.bat 檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-133">The example commands then run the vsdevcmd.bat file that's created by the Visual Studio installer.</span></span> <span data-ttu-id="4999e-134">這個 .BAT 檔案會設定您的路徑和一些環境變數，以便執行 MIDL 和 TLBIMP.EXE 命令。</span><span class="sxs-lookup"><span data-stu-id="4999e-134">This BAT file will set up your paths and some environment variables so that the MIDL and TLBIMP commands will run.</span></span> <span data-ttu-id="4999e-135">它也會設定 WindowsSdkDir 和 WindowsSDKLibVersion 變數，以指向最新的 Windows SDK 目錄。</span><span class="sxs-lookup"><span data-stu-id="4999e-135">It also sets up the WindowsSdkDir and WindowsSDKLibVersion variables to point to the most recent Windows SDK directories.</span></span>

```console
REM Create a working directory
REM You can select a different directory based on your needs.
SET BITSTEMP=C:\BITSTEMPDIR
MKDIR "%BITSTEMP%"

REM Run the VsDevCmd.bat file to locate the Windows
REM SDK directory and the tools directories
REM This will be different for different versions of
REM Visual Studio

CALL "C:\Program Files (x86)\Microsoft Visual Studio\2017\Enterprise\Common7\Tools\vsdevcmd.bat"

REM Run the MIDL command on the desired BITS IDL file
REM This will generate a TLB file for the TLBIMP command
REM The IDL file will be different depending on which
REM set of BITS interfaces you need to use.
REM Run the MIDL command once per reference file
REM that you will need to explicitly use.
PUSHD .
CD /D "%WindowsSdkDir%Include\%WindowsSDKLibVersion%um"

MIDL  /I ..\shared /out "%BITSTEMP%" bits1_5.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits4_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits5_0.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_1.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:
MIDL  /I ..\shared /out "%BITSTEMP%" bits10_2.idl /dlldata NUL: /header NUL: /iid NUL: /proxy NUL:

REM Run the TLBIMP command on the resulting TLB file(s)
REM Try to keep a parallel set of names.
TLBIMP "%BITSTEMP%"\bits1_5.tlb /out: "%BITSTEMP%"\BITSReference1_5.dll
TLBIMP "%BITSTEMP%"\bits4_0.tlb /out: "%BITSTEMP%"\BITSReference4_0.dll
TLBIMP "%BITSTEMP%"\bits5_0.tlb /out: "%BITSTEMP%"\BITSReference5_0.dll
TLBIMP "%BITSTEMP%"\bits10_1.tlb /out: "%BITSTEMP%"\BITSReference10_1.dll
TLBIMP "%BITSTEMP%"\bits10_2.tlb /out: "%BITSTEMP%"\BITSReference10_2.dll
DEL "%BITSTEMP%"\bits*.tlb
POPD

```
<span data-ttu-id="4999e-136">執行這些命令之後，您會在 BITSTEMP 目錄中有一組參照 Dll。</span><span class="sxs-lookup"><span data-stu-id="4999e-136">Once these commands are run you will have a set of reference DLLs in the BITSTEMP directory.</span></span>

### <a name="adding-the-reference-dlls-to-your-project"></a><span data-ttu-id="4999e-137">將參考 Dll 新增至專案</span><span class="sxs-lookup"><span data-stu-id="4999e-137">Adding the reference DLLs to your project</span></span>

<span data-ttu-id="4999e-138">若要在 c # 專案中使用參考 DLL，請在 Visual Studio 中開啟您的 c # 專案。</span><span class="sxs-lookup"><span data-stu-id="4999e-138">To use a reference DLL in a C# project, open your C# project in Visual Studio.</span></span> <span data-ttu-id="4999e-139">在 [方案總管中，以滑鼠右鍵按一下 [參考]，然後按一下 [加入參考]。</span><span class="sxs-lookup"><span data-stu-id="4999e-139">In the Solution Explorer, right-click the References and click Add Reference.</span></span> <span data-ttu-id="4999e-140">然後按一下 [流覽] 按鈕，然後按一下 [新增] 按鈕。</span><span class="sxs-lookup"><span data-stu-id="4999e-140">Then click the Browse button and then the Add button.</span></span> <span data-ttu-id="4999e-141">流覽至含有參考 Dll 的目錄，選取它們，然後按一下 [新增]。</span><span class="sxs-lookup"><span data-stu-id="4999e-141">Navigate to the directory with the reference DLLs, select them, and click Add.</span></span> <span data-ttu-id="4999e-142">在 [參考管理員] 視窗中，將會檢查參照 Dll。</span><span class="sxs-lookup"><span data-stu-id="4999e-142">In the Reference Manager window the reference DLLs will be checked.</span></span> <span data-ttu-id="4999e-143">然後按一下 [確定]。</span><span class="sxs-lookup"><span data-stu-id="4999e-143">Then click OK.</span></span>

<span data-ttu-id="4999e-144">BITS 參考 Dll 現在已加入至您的專案。</span><span class="sxs-lookup"><span data-stu-id="4999e-144">The BITS reference DLLs are now added to your project.</span></span>

<span data-ttu-id="4999e-145">參考 DLL 檔案中的資訊將內嵌至您的最終程式。</span><span class="sxs-lookup"><span data-stu-id="4999e-145">The information in the reference DLL files will be embedded into your final program.</span></span> <span data-ttu-id="4999e-146">您不需要與您的程式一起寄送參照 DLL 檔案。您只需要寄送。Exe。</span><span class="sxs-lookup"><span data-stu-id="4999e-146">You do not have to ship the reference DLL files with your program; you just need to ship the .EXE.</span></span> 

<span data-ttu-id="4999e-147">您可以變更參考 Dll 是否內嵌至最終 EXE。</span><span class="sxs-lookup"><span data-stu-id="4999e-147">You can change whether the reference DLLs are embedded into the final EXE.</span></span> <span data-ttu-id="4999e-148">您可以使用 [ [內嵌 Interop 類型](/dotnet/framework/interop/how-to-add-references-to-type-libraries) ] 屬性來設定是否將內嵌參考 dll。</span><span class="sxs-lookup"><span data-stu-id="4999e-148">Use the [Embed Interop Types](/dotnet/framework/interop/how-to-add-references-to-type-libraries) property to set whether or not the reference DLLs will be embedded.</span></span> <span data-ttu-id="4999e-149">這可以根據每個參考來完成。</span><span class="sxs-lookup"><span data-stu-id="4999e-149">This can be done on a per-reference basis.</span></span> <span data-ttu-id="4999e-150">預設值為 True，以內嵌 Dll。</span><span class="sxs-lookup"><span data-stu-id="4999e-150">The default is True to embed the DLLs.</span></span>

## <a name="modifying-idl-files-for-more-complete-net-code"></a><span data-ttu-id="4999e-151">修改 IDL 檔案以取得更完整的 .NET 程式碼</span><span class="sxs-lookup"><span data-stu-id="4999e-151">Modifying IDL files for more complete .NET code</span></span>

<span data-ttu-id="4999e-152"> (Microsoft 介面定義語言) 檔案的 BITS IDL 可原封不動地使用，以建立 BackgroundCopyManager DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-152">The BITS IDL (Microsoft Interface Definition Language) files can be used unchanged to make the BackgroundCopyManager DLL file.</span></span> <span data-ttu-id="4999e-153">但是，所產生的 .NET 參考 DLL 將會遺漏某些產生無法翻譯聯集，而且某些結構和列舉會有難以使用的名稱。</span><span class="sxs-lookup"><span data-stu-id="4999e-153">However, the resulting .NET reference DLL will be missing some untranslatable unions and has hard-to-use names for some structures and enums.</span></span> <span data-ttu-id="4999e-154">本節將說明一些您可以進行的變更，讓 .NET DLL 更完整且更容易使用。</span><span class="sxs-lookup"><span data-stu-id="4999e-154">This section will describe some of the changes that you can make to make the .NET DLL more complete and easier to use.</span></span>

### <a name="simpler-enum-names"></a><span data-ttu-id="4999e-155">更簡單的列舉名稱</span><span class="sxs-lookup"><span data-stu-id="4999e-155">Simpler ENUM names</span></span>

<span data-ttu-id="4999e-156">BITS IDL 檔案通常會定義如下的列舉值：</span><span class="sxs-lookup"><span data-stu-id="4999e-156">The BITS IDL files typically define enum values like this:</span></span>
```
    typedef enum
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```
<span data-ttu-id="4999e-157">BG_AUTH_TARGET 是 typedef 的名稱;實際的列舉未命名。</span><span class="sxs-lookup"><span data-stu-id="4999e-157">The BG_AUTH_TARGET is the name of the typedef; the actual enum is not named.</span></span> <span data-ttu-id="4999e-158">這通常不會造成 C 程式碼發生問題，但無法順利轉譯以搭配 .NET 程式使用。</span><span class="sxs-lookup"><span data-stu-id="4999e-158">This doesn’t typically cause problems with C code but doesn’t translate well for use with a .NET program.</span></span> <span data-ttu-id="4999e-159">系統會自動建立新的名稱，但它可能看起來像 _MIDL___MIDL_itf_bits4_0_0005_0001_0001 而不是人類看得懂的值。</span><span class="sxs-lookup"><span data-stu-id="4999e-159">A new name will be automatically created, but it might look something like _MIDL___MIDL_itf_bits4_0_0005_0001_0001 instead of a human-readable value.</span></span> <span data-ttu-id="4999e-160">您可以藉由更新 MIDL 檔案以包含列舉名稱來修正此問題。</span><span class="sxs-lookup"><span data-stu-id="4999e-160">You can fix this problem by updating the MIDL files to include an enum name.</span></span>

```
    typedef enum BG_AUTH_TARGET
    {
            BG_AUTH_TARGET_SERVER = 1,
            BG_AUTH_TARGET_PROXY
    } BG_AUTH_TARGET;
```

<span data-ttu-id="4999e-161">允許列舉名稱與 typedef 名稱相同。</span><span class="sxs-lookup"><span data-stu-id="4999e-161">The enum name is allowed to be the same as the typedef name.</span></span> <span data-ttu-id="4999e-162">某些程式設計人員有一個命名慣例，其中 (例如，藉由在列舉名稱之前加上底線，將底線放在) ，但這只會混淆 .NET 翻譯。</span><span class="sxs-lookup"><span data-stu-id="4999e-162">Some programmers have a naming convention where they are kept different (for example, by putting an underscore before the enum name), but this will only confuse the .NET translations.</span></span> 

### <a name="string-types-in-unions"></a><span data-ttu-id="4999e-163">等位中的字串類型</span><span class="sxs-lookup"><span data-stu-id="4999e-163">String types in unions</span></span>

<span data-ttu-id="4999e-164">BITS IDL 檔案會使用 LPWSTR (long 指標來傳遞字串) 慣例的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="4999e-164">The BITS IDL files pass strings using the LPWSTR (long pointer to wide-character string) convention.</span></span> <span data-ttu-id="4999e-165">雖然這在傳遞函式參數時很有用 (例如 GetDisplayName ( [out] LPWSTR \* pVal) 方法) ，但是當字串是等位的一部分時，就無法運作。</span><span class="sxs-lookup"><span data-stu-id="4999e-165">Although this works when passing function parameters (like the Job.GetDisplayName([out] LPWSTR \*pVal) method), it doesn’t work when the strings are part of unions.</span></span> <span data-ttu-id="4999e-166">例如，bits5_0 .idl 檔包含 BITS_FILE_PROPERTY_VALUE 聯集：</span><span class="sxs-lookup"><span data-stu-id="4999e-166">For example, the bits5_0.idl file includes the BITS_FILE_PROPERTY_VALUE union:</span></span>

```
typedef [switch_type(BITS_FILE_PROPERTY_ID)] union
{
    [case( BITS_FILE_PROPERTY_ID_HTTP_RESPONSE_HEADERS )]
        LPWSTR String;
}
BITS_FILE_PROPERTY_VALUE;
```

<span data-ttu-id="4999e-167">LPWSTR 欄位將不會包含在 .NET 版本的聯集內。</span><span class="sxs-lookup"><span data-stu-id="4999e-167">The LPWSTR field won’t be included in the .NET version of the union.</span></span> <span data-ttu-id="4999e-168">若要修正此問題，請將 LPWSTR 變更為 WCHAR \*。</span><span class="sxs-lookup"><span data-stu-id="4999e-168">To fix this, change the LPWSTR to a WCHAR\*.</span></span> <span data-ttu-id="4999e-169">產生的欄位 (呼叫的字串) 將會以 IntPtr 的形式傳遞。</span><span class="sxs-lookup"><span data-stu-id="4999e-169">The resulting field (called String) will be passed as a IntPtr.</span></span> <span data-ttu-id="4999e-170">使用 System.runtime.interopservices.outattribute. PtrToStringAuto (值將此轉換成字串。字串) ;方法。</span><span class="sxs-lookup"><span data-stu-id="4999e-170">Convert this into a string using the  System.Runtime.InteropServices.Marshal.PtrToStringAuto(value.String); method.</span></span>

### <a name="unions-in-structures"></a><span data-ttu-id="4999e-171">結構中的等位</span><span class="sxs-lookup"><span data-stu-id="4999e-171">Unions in structures</span></span>

<span data-ttu-id="4999e-172">有時內嵌在結構中的聯集不會包含在結構中。</span><span class="sxs-lookup"><span data-stu-id="4999e-172">Sometimes unions that are embedded in structures won't be included in the structure at all.</span></span> <span data-ttu-id="4999e-173">例如，在 Bits1_5 .idl 中，BG_AUTH_CREDENTIALS 的定義如下：</span><span class="sxs-lookup"><span data-stu-id="4999e-173">For example, in the Bits1_5.idl the BG_AUTH_CREDENTIALS is defined as follows:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        [switch_is(Scheme)] BG_AUTH_CREDENTIALS_UNION Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

<span data-ttu-id="4999e-174">BG_AUTH_CREDENTIALS_UNION 定義為聯集，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4999e-174">The BG_AUTH_CREDENTIALS_UNION is defined to be a union as follows:</span></span>
```
    typedef [switch_type(BG_AUTH_SCHEME)] union
    {
            [case( BG_AUTH_SCHEME_BASIC, BG_AUTH_SCHEME_DIGEST, BG_AUTH_SCHEME_NTLM,
            BG_AUTH_SCHEME_NEGOTIATE, BG_AUTH_SCHEME_PASSPORT )] BG_BASIC_CREDENTIALS Basic;
            [default] ;
    } BG_AUTH_CREDENTIALS_UNION;
```
<span data-ttu-id="4999e-175">BG_AUTH_CREDENTIALS 中的 [認證] 欄位將不會包含在 .NET 類別定義中。</span><span class="sxs-lookup"><span data-stu-id="4999e-175">The Credentials field in the BG_AUTH_CREDENTIALS will not be included in the .NET class definition.</span></span>

<span data-ttu-id="4999e-176">請注意，不論 BG_AUTH_SCHEME，union 都會定義為一律是 BG_BASIC_CREDENTIALS。</span><span class="sxs-lookup"><span data-stu-id="4999e-176">Note that the union is defined to always be a BG_BASIC_CREDENTIALS regardless of the BG_AUTH_SCHEME.</span></span> <span data-ttu-id="4999e-177">因為等位不會當做聯集使用，所以我們可以直接傳遞 BG_BASIC_CREDENTIALS，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4999e-177">Because the union isn’t used as a union, we can just pass a BG_BASIC_CREDENTIALS like this:</span></span>
```
    typedef struct
    {
        BG_AUTH_TARGET Target;
        BG_AUTH_SCHEME Scheme;
        BG_BASIC_CREDENTIALS Credentials;
    }
    BG_AUTH_CREDENTIALS;
```

## <a name="using-bits-from-c"></a><span data-ttu-id="4999e-178">使用 C 的位#</span><span class="sxs-lookup"><span data-stu-id="4999e-178">Using BITS from C#</span></span>

### <a name="recommended-using-statement"></a><span data-ttu-id="4999e-179">建議使用語句</span><span class="sxs-lookup"><span data-stu-id="4999e-179">Recommended using statement</span></span>

<span data-ttu-id="4999e-180">在 c # 中設定某些 using 語句，會減少您需要輸入以使用不同位版本的字元數。</span><span class="sxs-lookup"><span data-stu-id="4999e-180">Setting up some using statements in C# will reduce the number of characters you need to type to use the different BITS versions.</span></span> <span data-ttu-id="4999e-181">名稱 "BITSReference" 來自參考 DLL 的名稱。</span><span class="sxs-lookup"><span data-stu-id="4999e-181">The name "BITSReference" comes from the name of the reference DLL.</span></span>

```csharp
// Set up the BITS namespaces
using BITS = BITSReference1_5;
using BITS4 = BITSReference4_0;
using BITS5 = BITSReference5_0;
using BITS10_2 = BITSReference10_2;
```

### <a name="quick-sample-download-a-file"></a><span data-ttu-id="4999e-182">快速範例：下載檔案</span><span class="sxs-lookup"><span data-stu-id="4999e-182">Quick Sample: download a file</span></span>

<span data-ttu-id="4999e-183">以下提供簡單但完整的 c # 程式碼程式碼片段，以從 URL 下載檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-183">A short but complete snippet of C# code to download a file from a URL is given below.</span></span> 

```csharp
    var mgr = new BITS.BackgroundCopyManager1_5();
    BITS.GUID jobGuid;
    BITS.IBackgroundCopyJob job;
    mgr.CreateJob("Quick download", BITS.BG_JOB_TYPE.BG_JOB_TYPE_DOWNLOAD, out jobGuid, out job);
    job.AddFile("https://aka.ms/WinServ16/StndPDF", @"C:\Server2016.pdf");
    job.Resume();
    bool jobIsFinal = false;
    while (!jobIsFinal)
    {
        BITS.BG_JOB_STATE state;
        job.GetState(out state);
        switch (state)
        {
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ERROR:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_TRANSFERRED:
                job.Complete();
                break;

            case BITS.BG_JOB_STATE.BG_JOB_STATE_CANCELLED:
            case BITS.BG_JOB_STATE.BG_JOB_STATE_ACKNOWLEDGED:
                jobIsFinal = true;
                break;
            default:
                Task.Delay(500); // delay a little bit
                break;
        }
    }
    // Job is complete
```

<span data-ttu-id="4999e-184">在此範例程式碼中，會建立名為 mgr 的 BITS 管理員。</span><span class="sxs-lookup"><span data-stu-id="4999e-184">In this sample code, a BITS manager named mgr is created.</span></span> <span data-ttu-id="4999e-185">它會直接對應至 [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) 介面。</span><span class="sxs-lookup"><span data-stu-id="4999e-185">It directly corresponds to the [IBackgroundCopyManager](/windows/desktop/api/bits/nn-bits-ibackgroundcopymanager) interface.</span></span> 

<span data-ttu-id="4999e-186">從管理員建立新的作業。</span><span class="sxs-lookup"><span data-stu-id="4999e-186">From the manager a new job is created.</span></span> <span data-ttu-id="4999e-187">作業是 >batchclient.joboperations.createjob 方法上的 out 參數。</span><span class="sxs-lookup"><span data-stu-id="4999e-187">The job is an out parameter on the CreateJob method.</span></span> <span data-ttu-id="4999e-188">傳入的也是不需要是唯一) 的作業 (名稱，以及下載類型，也就是下載作業。</span><span class="sxs-lookup"><span data-stu-id="4999e-188">Also passed in is the job name (which doesn't have to be unique) and the download type, which is a download job.</span></span> <span data-ttu-id="4999e-189">工作識別碼的位 GUID 也會填入。</span><span class="sxs-lookup"><span data-stu-id="4999e-189">A BITS GUID for the job identifier is also filled in.</span></span>

<span data-ttu-id="4999e-190">一旦建立作業之後，您就可以使用 AddFile 方法，將新的下載檔案新增至作業。</span><span class="sxs-lookup"><span data-stu-id="4999e-190">Once the job is created you add a new download file to the job with the AddFile method.</span></span> <span data-ttu-id="4999e-191">您必須傳入兩個字串，一個用於遠端檔案 (URL 或檔案共用) ，另一個用於本機檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-191">You need to pass in two strings, one for the remote file (the URL or file share) and one for the local file.</span></span> 

<span data-ttu-id="4999e-192">新增檔案之後，請在作業上呼叫 Resume 來啟動它。</span><span class="sxs-lookup"><span data-stu-id="4999e-192">After adding the file, call Resume on the job to start it.</span></span> <span data-ttu-id="4999e-193">然後，程式碼會等到工作處於最終狀態 (錯誤或傳輸) ，然後才會完成。</span><span class="sxs-lookup"><span data-stu-id="4999e-193">Then the code waits until the job is in a final state (ERROR or TRANSFERRED) and is then completed.</span></span>

### <a name="bits-versions-casting-and-queryinterface"></a><span data-ttu-id="4999e-194">BITS 版本、轉換和 QueryInterface</span><span class="sxs-lookup"><span data-stu-id="4999e-194">BITS Versions, Casting and QueryInterface</span></span>

<span data-ttu-id="4999e-195">您會發現，您通常必須在程式中使用舊版的 BITS 物件和較新的版本。</span><span class="sxs-lookup"><span data-stu-id="4999e-195">You'll find that you often have to use both an early version of a BITS object and a more recent version in your program.</span></span>  

<span data-ttu-id="4999e-196">例如，當您建立工作物件時，即使您要使用較新的管理員物件，且有較新的 IBackgroundCopyJob 物件可用，還是會收到 IBackgroundCopyJob (部分的 BITS 1.0 版) 。</span><span class="sxs-lookup"><span data-stu-id="4999e-196">For example, when you make a job object, you will get an IBackgroundCopyJob (part of BITS version 1.0) even when you're making it using a more recent manager object and a more recent IBackgroundCopyJob object is available.</span></span> <span data-ttu-id="4999e-197">因為 >batchclient.joboperations.createjob 方法不接受最新版本的介面，所以您無法直接建立較新版本。</span><span class="sxs-lookup"><span data-stu-id="4999e-197">Because the CreateJob method doesn't accept an interface for the more recent version, you can't directly make the more recent version.</span></span>

<span data-ttu-id="4999e-198">使用 .NET cast 從較舊的型別物件轉換成較新的型別物件。</span><span class="sxs-lookup"><span data-stu-id="4999e-198">Use a .NET cast to convert from an older type object to a newer type object.</span></span> <span data-ttu-id="4999e-199">轉換會自動依適當情況呼叫 COM QueryInterface。</span><span class="sxs-lookup"><span data-stu-id="4999e-199">The cast will automatically call a COM QueryInterface as appropriate.</span></span> 

<span data-ttu-id="4999e-200">在此範例中，有一個名為 "job" 的位 IBackgroundCopyJob 物件，而我們想要將它轉換成名為 "job5" 的 IBackgroundCopyJob5 物件，以便我們可以呼叫 BITS 5.0 GetProperty 方法。</span><span class="sxs-lookup"><span data-stu-id="4999e-200">In this example, there's a BITS IBackgroundCopyJob object named "job", and we want to convert it to an IBackgroundCopyJob5 object named "job5" so that we can call the BITS 5.0 GetProperty method.</span></span> <span data-ttu-id="4999e-201">我們只是轉換成 IBackgroundCopyJob5 型別，如下所示：</span><span class="sxs-lookup"><span data-stu-id="4999e-201">We just cast to the IBackgroundCopyJob5 type like this:</span></span>

```csharp
var job5 = (BITS5.IBackgroundCopyJob5)job;
```

<span data-ttu-id="4999e-202">Job5 變數將使用正確的 QueryInterface，由 .NET 初始化。</span><span class="sxs-lookup"><span data-stu-id="4999e-202">The job5 variable will be initialized by .NET by using the correct QueryInterface.</span></span> 

<span data-ttu-id="4999e-203">如果您的程式碼可能在不支援特定版本 BITS 的系統上執行，您可以嘗試轉換並攔截 InvalidCastException。</span><span class="sxs-lookup"><span data-stu-id="4999e-203">If your code might run on a system that doesn't support a particular version of BITS, you can try the cast and catch the System.InvalidCastException.</span></span> 

```csharp
BITS5.IBackgroundCopyJob5 job5 = null;
try
{
    job5 = (BITS5.IBackgroundCopyJob5)Job;
}
catch (System.InvalidCastException)
{
    ; // Must be running an earlier version of BITS
}
```

<span data-ttu-id="4999e-204">常見的問題是當您嘗試轉換成錯誤的物件類型時。</span><span class="sxs-lookup"><span data-stu-id="4999e-204">A common problem is when you try to cast into the wrong kind of object.</span></span> <span data-ttu-id="4999e-205">.NET 系統不知道 BITS 介面之間的真正關聯性。</span><span class="sxs-lookup"><span data-stu-id="4999e-205">The .NET system doesn't know about the real relationship between the BITS interfaces.</span></span> <span data-ttu-id="4999e-206">如果您要求的是錯誤類型的介面，.NET 將會嘗試為您進行處理，並會因為 InvalidCastException 和 HResult 0x80004002 (E_NOINTERFACE) 而失敗。</span><span class="sxs-lookup"><span data-stu-id="4999e-206">If you ask for the wrong kind of interface, .NET will try to make it for you and will fail with an InvalidCastException and HResult 0x80004002 (E_NOINTERFACE).</span></span>

### <a name="working-with-bits-versions-10_1-and-10_2"></a><span data-ttu-id="4999e-207">使用 BITS 版本10_1 和10_2</span><span class="sxs-lookup"><span data-stu-id="4999e-207">Working with BITS Versions 10_1 and 10_2</span></span>

<span data-ttu-id="4999e-208">在某些版本的 Windows 10 上，您無法使用10.1 或10.2 介面直接建立 BITS IBackgroundCopyManager 物件。</span><span class="sxs-lookup"><span data-stu-id="4999e-208">On some versions of Windows 10 you can't directly create a BITS IBackgroundCopyManager object using the 10.1 or 10.2 interfaces.</span></span> <span data-ttu-id="4999e-209">相反地，您必須使用多個版本的 BackgroundCopyManager DLL 參考檔案。</span><span class="sxs-lookup"><span data-stu-id="4999e-209">Instead, you'll have to use multiple versions of the BackgroundCopyManager DLL reference files.</span></span> <span data-ttu-id="4999e-210">例如，您可以使用1.5 版本建立 IBackgroundCopyManager 物件，然後使用10.1 或10.2 版本來轉換產生的作業或檔案物件。</span><span class="sxs-lookup"><span data-stu-id="4999e-210">For example, you can use the 1.5 version to make an IBackgroundCopyManager object, and then cast the resulting job or file objects using the 10.1 or 10.2 versions.</span></span>

