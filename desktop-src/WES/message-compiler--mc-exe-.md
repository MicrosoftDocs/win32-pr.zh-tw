---
title: '訊息編譯器 (MC.exe) '
description: 用來編譯檢測資訊清單和訊息文字檔。
ms.assetid: f9de35f1-6d31-4f4b-b2c4-8474d6fce9e0
keywords:
- 訊息編譯器 (MC.exe) EventLog
topic_type:
- apiref
api_name:
- Message Compiler (MC.exe)
api_type:
- NA
ms.topic: reference
ms.date: 06/03/2020
ms.openlocfilehash: 5eb852dcbb13800705db0a0f19d912de899f9b0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510721"
---
# <a name="message-compiler-mcexe"></a><span data-ttu-id="60556-104">訊息編譯器 (MC.exe) </span><span class="sxs-lookup"><span data-stu-id="60556-104">Message Compiler (MC.exe)</span></span>

<span data-ttu-id="60556-105">用來編譯檢測資訊清單和訊息文字檔。</span><span class="sxs-lookup"><span data-stu-id="60556-105">Used to compile instrumentation manifests and message text files.</span></span> <span data-ttu-id="60556-106">編譯器會產生您的應用程式所連結的訊息資源檔。</span><span class="sxs-lookup"><span data-stu-id="60556-106">The compiler generates the message resource files to which your application links.</span></span>

``` syntax
MC [-?aAbcdnouUv] [-m <length>] [-h <path>] [-e <extension>] [-r <path>]
   [-x <path>] [-w <file>] [-W <file>] [-z <basename> ] [-cp <encoding>]
   [-km | -um | -generateProjections | -cs <namespace>]
   [-mof] [-p <prefix>] [-P <prefix>]
   [<filename.man>] [<filename.mc>]
```

-   [<span data-ttu-id="60556-107">訊息文字檔與資訊清單檔案通用的引數</span><span class="sxs-lookup"><span data-stu-id="60556-107">Arguments common to both message text files and manifest files</span></span>](#arguments-common-to-both-message-text-files-and-manifest-files)
-   [<span data-ttu-id="60556-108">資訊清單檔特定的引數</span><span class="sxs-lookup"><span data-stu-id="60556-108">Arguments specific to manifest files</span></span>](#arguments-specific-to-manifest-files)
-   [<span data-ttu-id="60556-109">產生提供者用來記錄事件之程式碼的特定引數</span><span class="sxs-lookup"><span data-stu-id="60556-109">Arguments specific to generating code that your provider would use to log events</span></span>](#arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events)
-   [<span data-ttu-id="60556-110">訊息文字檔特定的引數</span><span class="sxs-lookup"><span data-stu-id="60556-110">Arguments specific to message text files</span></span>](#arguments-specific-to-message-text-files)

## <a name="arguments-common-to-both-message-text-files-and-manifest-files"></a><span data-ttu-id="60556-111">訊息文字檔與資訊清單檔案通用的引數</span><span class="sxs-lookup"><span data-stu-id="60556-111">Arguments common to both message text files and manifest files</span></span>

<dl> <dt>

<span data-ttu-id="60556-112"><span id="-_"></span>**-?**</span><span class="sxs-lookup"><span data-stu-id="60556-112"><span id="-_"></span>**-?**</span></span>
</dt> <dd>

<span data-ttu-id="60556-113">顯示訊息編譯器的使用量資訊。</span><span class="sxs-lookup"><span data-stu-id="60556-113">Displays the usage information for the Message Compiler.</span></span>

</dd> <dt>

<span data-ttu-id="60556-114"><span id="-c"></span><span id="-C"></span>**-c**</span><span class="sxs-lookup"><span data-stu-id="60556-114"><span id="-c"></span><span id="-C"></span>**-c**</span></span>
</dt> <dd>

<span data-ttu-id="60556-115">使用這個引數，讓編譯器將客戶位設定為在所有訊息識別碼中 (位 28) 。</span><span class="sxs-lookup"><span data-stu-id="60556-115">Use this argument to have the compiler set the customer bit (bit 28) in all message IDs.</span></span> <span data-ttu-id="60556-116">如需客戶位的詳細資訊，請參閱 winerror.h。</span><span class="sxs-lookup"><span data-stu-id="60556-116">For information on the customer bit, see winerror.h.</span></span>

</dd> <dt>

<span data-ttu-id="60556-117"><span id="-cp"></span><span id="-CP"></span>**-cp** *編碼*</span><span class="sxs-lookup"><span data-stu-id="60556-117"><span id="-cp"></span><span id="-CP"></span>**-cp** *encoding*</span></span>
</dt> <dd>

<span data-ttu-id="60556-118">您可以使用這個引數來指定用於所有產生之文字檔的字元編碼。</span><span class="sxs-lookup"><span data-stu-id="60556-118">Use this argument to specify the character encoding used for all generated text files.</span></span> <span data-ttu-id="60556-119">有效的名稱包括「ansi」 (預設) 、「utf-8」和「utf-16」。</span><span class="sxs-lookup"><span data-stu-id="60556-119">Valid names include "ansi" (default), "utf-8", and "utf-16".</span></span> <span data-ttu-id="60556-120">Unicode 編碼會加入位元組順序標記。</span><span class="sxs-lookup"><span data-stu-id="60556-120">The Unicode encodings will add a byte order mark.</span></span>

</dd> <dt>

<span data-ttu-id="60556-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e** *擴充* 功能</span><span class="sxs-lookup"><span data-stu-id="60556-121"><span id="-e_extension"></span><span id="-E_EXTENSION"></span>**-e** *extension*</span></span>
</dt> <dd>

<span data-ttu-id="60556-122">使用這個引數來指定要用於標頭檔的延伸模組。</span><span class="sxs-lookup"><span data-stu-id="60556-122">Use this argument to specify the extension to use for the header file.</span></span> <span data-ttu-id="60556-123">您最多可以指定三個字元的副檔名，而不包含句點。</span><span class="sxs-lookup"><span data-stu-id="60556-123">You can specify up to a three characters extension, not including the period.</span></span> <span data-ttu-id="60556-124">預設值為 .h。</span><span class="sxs-lookup"><span data-stu-id="60556-124">The default is .h.</span></span>

</dd> <dt>

<span data-ttu-id="60556-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *路徑*</span><span class="sxs-lookup"><span data-stu-id="60556-125"><span id="-h_path"></span><span id="-H_PATH"></span>**-h** *path*</span></span>
</dt> <dd>

<span data-ttu-id="60556-126">您可以使用這個引數來指定要編譯器放置所產生標頭檔的資料夾。</span><span class="sxs-lookup"><span data-stu-id="60556-126">Use this argument to specify the folder into which you want the compiler to place the generated header file.</span></span> <span data-ttu-id="60556-127">預設值是目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="60556-127">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="60556-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *長度*</span><span class="sxs-lookup"><span data-stu-id="60556-128"><span id="-m_length"></span><span id="-M_LENGTH"></span>**-m** *length*</span></span>
</dt> <dd>

<span data-ttu-id="60556-129">使用這個引數可讓編譯器在任何訊息超過 *長度* 字元時產生警告。</span><span class="sxs-lookup"><span data-stu-id="60556-129">Use this argument to have the compiler generate a warning if the any message exceeds *length* characters.</span></span>

</dd> <dt>

<span data-ttu-id="60556-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *路徑*</span><span class="sxs-lookup"><span data-stu-id="60556-130"><span id="-r_path"></span><span id="-R_PATH"></span>**-r** *path*</span></span>
</dt> <dd>

<span data-ttu-id="60556-131">您可以使用這個引數來指定要編譯器將產生的資源編譯器腳本放 ( .rc 檔) 和產生的 bin 檔案 (二進位資源的資料夾，) 資源編譯器腳本所包含的檔案。</span><span class="sxs-lookup"><span data-stu-id="60556-131">Use this argument to specify the folder into which you want the compiler to place the generated resource compiler script (.rc file) and the generated .bin files (binary resources) that the resource compiler script includes.</span></span> <span data-ttu-id="60556-132">預設值是目前的目錄。</span><span class="sxs-lookup"><span data-stu-id="60556-132">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="60556-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *名稱*</span><span class="sxs-lookup"><span data-stu-id="60556-133"><span id="-z_name"></span><span id="-Z_NAME"></span>**-z** *name*</span></span>
</dt> <dd>

<span data-ttu-id="60556-134">使用這個引數來覆寫編譯器針對其產生的檔案所使用的預設基底名稱。</span><span class="sxs-lookup"><span data-stu-id="60556-134">Use this argument to override the default base name that the compiler uses for the files that it generates.</span></span> <span data-ttu-id="60556-135">預設值是使用 *檔案名* 輸入檔的基底名稱。</span><span class="sxs-lookup"><span data-stu-id="60556-135">The default is to use the base name of the *filename* input file.</span></span>

</dd> <dt>

<span data-ttu-id="60556-136"><span id="filename"></span><span id="FILENAME"></span>*檔案名*</span><span class="sxs-lookup"><span data-stu-id="60556-136"><span id="filename"></span><span id="FILENAME"></span>*filename*</span></span>
</dt> <dd>

<span data-ttu-id="60556-137">檢測資訊清單檔案或訊息文字檔。</span><span class="sxs-lookup"><span data-stu-id="60556-137">The instrumentation manifest file or message text file.</span></span> <span data-ttu-id="60556-138">檔案必須存在於目前的目錄中。</span><span class="sxs-lookup"><span data-stu-id="60556-138">The file must exist in the current directory.</span></span> <span data-ttu-id="60556-139">您可以指定資訊清單檔、訊息文字檔或兩者。</span><span class="sxs-lookup"><span data-stu-id="60556-139">You can specify a manifest file, message text file, or both.</span></span> <span data-ttu-id="60556-140">檔案名必須包含副檔名。</span><span class="sxs-lookup"><span data-stu-id="60556-140">The file name must include the extension.</span></span> <span data-ttu-id="60556-141">慣例是在資訊清單檔中使用 man 副檔名，並為郵件文字檔使用 mc 副檔名。</span><span class="sxs-lookup"><span data-stu-id="60556-141">The convention is to use a .man extension for manifest files and a .mc extension for message text files.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-manifest-files"></a><span data-ttu-id="60556-142">資訊清單檔特定的引數</span><span class="sxs-lookup"><span data-stu-id="60556-142">Arguments specific to manifest files</span></span>

<dl> <dt>

<span data-ttu-id="60556-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *路徑*</span><span class="sxs-lookup"><span data-stu-id="60556-143"><span id="-s_path"></span><span id="-S_PATH"></span>**-s** *path*</span></span>
</dt> <dd>

<span data-ttu-id="60556-144">使用這個引數來建立您的檢測基準。</span><span class="sxs-lookup"><span data-stu-id="60556-144">Use this argument to create a baseline of your instrumentation.</span></span> <span data-ttu-id="60556-145">指定包含您的基準資訊清單檔案之資料夾的路徑。</span><span class="sxs-lookup"><span data-stu-id="60556-145">Specify the path to the folder that contains your baseline manifest files.</span></span> <span data-ttu-id="60556-146">在後續的版本中，您會使用 **-t** 引數，根據相容性問題的基準來檢查新的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="60556-146">For subsequent releases, you would then use the **-t** argument to check the new manifest against the baseline for compatibility issues.</span></span>

<span data-ttu-id="60556-147">**在 MC 版本1.12.7051 之前：** 無法使用</span><span class="sxs-lookup"><span data-stu-id="60556-147">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="60556-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *路徑*</span><span class="sxs-lookup"><span data-stu-id="60556-148"><span id="-t_path"></span><span id="-T_PATH"></span>**-t** *path*</span></span>
</dt> <dd>

<span data-ttu-id="60556-149">當您建立新版本的資訊清單，而且想要檢查它是否符合您使用 **-s** 引數所建立的基準時，請使用這個引數。</span><span class="sxs-lookup"><span data-stu-id="60556-149">Use this argument when you create a new version of your manifest and want to check it for application compatibility against the baseline that you created using the **-s** argument.</span></span> <span data-ttu-id="60556-150">路徑必須指向包含的資料夾。基準作業所建立的 BIN 檔案 (看到 **-s** 參數) 。</span><span class="sxs-lookup"><span data-stu-id="60556-150">The path must point to the folder that contains the .BIN files that the baseline operation created (see the **-s** switch).</span></span>

<span data-ttu-id="60556-151">**在 MC 版本1.12.7051 之前：** 無法使用</span><span class="sxs-lookup"><span data-stu-id="60556-151">**Prior to MC version 1.12.7051:** Not available</span></span>

</dd> <dt>

<span data-ttu-id="60556-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *路徑*</span><span class="sxs-lookup"><span data-stu-id="60556-152"><span id="-w_path"></span><span id="-W_PATH"></span>**-w** *path*</span></span>
</dt> <dd>

<span data-ttu-id="60556-153">編譯器會忽略此引數，並自動驗證資訊清單。</span><span class="sxs-lookup"><span data-stu-id="60556-153">The compiler ignores this argument and automatically validates the manifest.</span></span>

<span data-ttu-id="60556-154">**在 MC 版本1.12.7051 之前：** 您可以使用這個引數來指定包含 Eventman .xsd 架構檔案的資料夾，而編譯器會使用此檔案來驗證您的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="60556-154">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Eventman.xsd schema file, which the compiler uses to validate your manifest.</span></span> <span data-ttu-id="60556-155">Windows SDK 在 Include 資料夾中包含 Eventman .xsd 架構檔案。 \\</span><span class="sxs-lookup"><span data-stu-id="60556-155">The Windows SDK includes the Eventman.xsd schema file in the \\Include folder.</span></span> <span data-ttu-id="60556-156">如果您未指定這個引數，則編譯器不會驗證您的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="60556-156">If you do not specify this argument, the compiler does not validate your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="60556-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *路徑*</span><span class="sxs-lookup"><span data-stu-id="60556-157"><span id="-W_path"></span><span id="-w_path"></span><span id="-W_PATH"></span>**-W** *path*</span></span>
</dt> <dd>

<span data-ttu-id="60556-158">編譯器會忽略此引數。</span><span class="sxs-lookup"><span data-stu-id="60556-158">The compiler ignores this argument.</span></span>

<span data-ttu-id="60556-159">**在 MC 版本1.12.7051 之前：** 使用這個引數來指定包含 Winmeta.xml 檔的資料夾。</span><span class="sxs-lookup"><span data-stu-id="60556-159">**Prior to MC version 1.12.7051:** Use this argument to specify the folder that contains the Winmeta.xml file.</span></span> <span data-ttu-id="60556-160">Winmeta.xml 檔案包含已辨識的輸入和輸出類型，以及預先定義的通道、層級和 opcode。</span><span class="sxs-lookup"><span data-stu-id="60556-160">The Winmeta.xml file contains the recognized input and output types as well as the predefined channels, levels, and opcodes.</span></span> <span data-ttu-id="60556-161">Windows SDK 包含包含資料夾中的 Winmeta.xml 檔案 \\ 。</span><span class="sxs-lookup"><span data-stu-id="60556-161">The Windows SDK includes the Winmeta.xml file in the \\Include folder.</span></span>

</dd> </dl>

### <a name="arguments-specific-to-generating-code-that-your-provider-would-use-to-log-events"></a><span data-ttu-id="60556-162">產生提供者用來記錄事件之程式碼的特定引數</span><span class="sxs-lookup"><span data-stu-id="60556-162">Arguments specific to generating code that your provider would use to log events</span></span>

<span data-ttu-id="60556-163">您可以使用下列編譯器引數來產生核心模式或使用者模式程式碼，您可以用來記錄事件。</span><span class="sxs-lookup"><span data-stu-id="60556-163">You can use the following compiler arguments to generate kernel-mode or user-mode code that you can use to log events.</span></span> <span data-ttu-id="60556-164">您也可以要求編譯器產生程式碼，以支援在 Windows Vista 之前的電腦上寫入事件。</span><span class="sxs-lookup"><span data-stu-id="60556-164">You can also request that the compiler generate code to support writing events on computers prior to Windows Vista.</span></span> <span data-ttu-id="60556-165">如果您的應用程式是以 c # 撰寫，則編譯器可以產生可供您用來記錄事件的 c # 類別。</span><span class="sxs-lookup"><span data-stu-id="60556-165">If your application is written C#, the compiler can generate a C# class that you can use to log events.</span></span> <span data-ttu-id="60556-166">從 Windows 7 版的 Window SDK 隨附的 MC 版本1.12.7051 開始，可以使用這些引數。</span><span class="sxs-lookup"><span data-stu-id="60556-166">These arguments are available beginning with MC version 1.12.7051 that ships with the Windows 7 version of the Window SDK.</span></span>

<dl> <dt>

<span data-ttu-id="60556-167"><span id="-co"></span><span id="-CO"></span>**-co**</span><span class="sxs-lookup"><span data-stu-id="60556-167"><span id="-co"></span><span id="-CO"></span>**-co**</span></span>
</dt> <dd>

<span data-ttu-id="60556-168">您可以使用這個引數，讓記錄服務針對您所記錄的每個事件呼叫您的使用者定義函數， (在) 事件記錄之後呼叫該函式。</span><span class="sxs-lookup"><span data-stu-id="60556-168">Use this argument to have the logging service call your user-defined function for each event that you log (the function is called after the event has been logged).</span></span> <span data-ttu-id="60556-169">您的使用者定義函數必須有下列簽章。</span><span class="sxs-lookup"><span data-stu-id="60556-169">Your user-defined function must have the following signature.</span></span>


```C++
VOID
pFnUserFunction(
    __in REGHANDLE RegHandle,
    __in PCEVENT_DESCRIPTOR Descriptor,
    __in ULONG EventDataCount,
    __in_ecount(EventDataCount) PEVENT_DATA_DESCRIPTOR EventData
    );
```



<span data-ttu-id="60556-170">您也必須在程式碼中包含下列指示詞。</span><span class="sxs-lookup"><span data-stu-id="60556-170">You must also include the following directive in your code.</span></span>

`#define MCGEN_CALLOUT pFnUserFunction`

<span data-ttu-id="60556-171">您應盡可能縮短您的執行，以避免記錄問題;在函數傳回之前，服務將不會再記錄您的事件。</span><span class="sxs-lookup"><span data-stu-id="60556-171">You should keep your implementation as short as possible to prevent logging issues; the service will not log anymore of your events until the function returns.</span></span>

<span data-ttu-id="60556-172">您可以使用這個引數搭配 **-公里** 或 **-um** 引數。</span><span class="sxs-lookup"><span data-stu-id="60556-172">You can use this argument with the **-km** or **-um** argument.</span></span>

</dd> <dt>

<span data-ttu-id="60556-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs** *命名空間*</span><span class="sxs-lookup"><span data-stu-id="60556-173"><span id="-cs_namespace"></span><span id="-CS_NAMESPACE"></span>**-cs** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="60556-174">您可以使用這個引數，讓編譯器根據 .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) 類別產生 c # 類別。</span><span class="sxs-lookup"><span data-stu-id="60556-174">Use this argument to have the compiler generate a C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="60556-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-css** *命名空間*</span><span class="sxs-lookup"><span data-stu-id="60556-175"><span id="-css_namespace"></span><span id="-CSS_NAMESPACE"></span>**-css** *namespace*</span></span>
</dt> <dd>

<span data-ttu-id="60556-176">您可以使用這個引數，讓編譯器根據 .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) 類別產生靜態 c # 類別。</span><span class="sxs-lookup"><span data-stu-id="60556-176">Use this argument to have the compiler generate a static C# class based on the .NET 3.5 [EventProvider](/dotnet/api/system.diagnostics.eventing.eventprovider?view=netframework-3.5&preserve-view=true) class.</span></span>

</dd> <dt>

<span data-ttu-id="60556-177"><span id="-km"></span><span id="-KM"></span>**-公里**</span><span class="sxs-lookup"><span data-stu-id="60556-177"><span id="-km"></span><span id="-KM"></span>**-km**</span></span>
</dt> <dd>

<span data-ttu-id="60556-178">您可以使用這個引數，讓編譯器產生核心模式程式碼，用來記錄資訊清單中所定義的事件。</span><span class="sxs-lookup"><span data-stu-id="60556-178">Use this argument to have the compiler generate the kernel-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> <dt>

<span data-ttu-id="60556-179"><span id="-mof"></span><span id="-MOF"></span>**-mof**</span><span class="sxs-lookup"><span data-stu-id="60556-179"><span id="-mof"></span><span id="-MOF"></span>**-mof**</span></span>
</dt> <dd>

<span data-ttu-id="60556-180">廢棄。</span><span class="sxs-lookup"><span data-stu-id="60556-180">DEPRECATED.</span></span> <span data-ttu-id="60556-181">使用這個引數，讓編譯器產生程式碼，讓您可以在 Windows Vista 之前，用來記錄電腦上的事件。</span><span class="sxs-lookup"><span data-stu-id="60556-181">Use this argument to have the compiler generate code that you can use to log events on computers prior to Windows Vista.</span></span> <span data-ttu-id="60556-182">此選項也會建立一個 MOF 檔案，其中包含資訊清單中所定義之每個事件的 MOF 類別。</span><span class="sxs-lookup"><span data-stu-id="60556-182">This option also creates a MOF file that contains the MOF classes for each event defined in the manifest.</span></span> <span data-ttu-id="60556-183">若要註冊 MOF 檔案中的類別，讓取用者可以解碼事件，請使用 MOF 編譯器 (Mofcomp.exe) 。</span><span class="sxs-lookup"><span data-stu-id="60556-183">To register the classes in the MOF file so that consumers can decode the events, use the MOF compiler (Mofcomp.exe).</span></span> <span data-ttu-id="60556-184">如需使用 MOF 編譯器的詳細資訊，請參閱 [受控物件格式](/windows/desktop/WmiSdk/managed-object-format--mof-)。</span><span class="sxs-lookup"><span data-stu-id="60556-184">For details on using the MOF compiler, see [Managed Object Format](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

<span data-ttu-id="60556-185">若要使用此參數，您必須遵守下列限制：</span><span class="sxs-lookup"><span data-stu-id="60556-185">To use this switch, you must adhere to the following restrictions:</span></span>

-   <span data-ttu-id="60556-186">每個事件定義都必須包含工作和 opcode 屬性</span><span class="sxs-lookup"><span data-stu-id="60556-186">Every event definition must include the task and opcode attributes</span></span>
-   <span data-ttu-id="60556-187">每項工作都必須包含 eventGuid 屬性</span><span class="sxs-lookup"><span data-stu-id="60556-187">Every task must include the eventGuid attribute</span></span>
-   <span data-ttu-id="60556-188">事件所參考的範本資料不能包含：</span><span class="sxs-lookup"><span data-stu-id="60556-188">The template data that the event references cannot contain:</span></span>
    -   <span data-ttu-id="60556-189">指定 win： Binary 或 win： SYSTEMTIME 輸入類型的資料項目</span><span class="sxs-lookup"><span data-stu-id="60556-189">Data items that specify the win:Binary or win:SYSTEMTIME input types</span></span>
    -   <span data-ttu-id="60556-190">結構</span><span class="sxs-lookup"><span data-stu-id="60556-190">Structures</span></span>
    -   <span data-ttu-id="60556-191">變數大小的陣列;不過，您可以指定固定長度的陣列</span><span class="sxs-lookup"><span data-stu-id="60556-191">Variable sized arrays; however, you can specify fixed length arrays</span></span>
    -   <span data-ttu-id="60556-192">字串資料類型無法指定長度屬性</span><span class="sxs-lookup"><span data-stu-id="60556-192">String data types cannot specify the length attribute</span></span>

<span data-ttu-id="60556-193">您必須使用此引數搭配 **-um**、 **-cs**、 **-css** 或 **-公里** 引數</span><span class="sxs-lookup"><span data-stu-id="60556-193">You must use this argument with the **-um**, **-cs**, **-css**, or **-km** argument</span></span>

</dd> <dt>

<span data-ttu-id="60556-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *前置* 詞</span><span class="sxs-lookup"><span data-stu-id="60556-194"><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-p** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="60556-195">使用這個引數來覆寫編譯器用來記錄宏名稱和方法名稱的預設前置詞。</span><span class="sxs-lookup"><span data-stu-id="60556-195">Use this argument to override the default prefix that the compiler uses for the logging macro names and method names.</span></span> <span data-ttu-id="60556-196">預設前置詞是 "EventWrite"。</span><span class="sxs-lookup"><span data-stu-id="60556-196">The default prefix is "EventWrite".</span></span> <span data-ttu-id="60556-197">此字串區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="60556-197">The string is case-sensitive.</span></span>

<span data-ttu-id="60556-198">您可以使用這個引數搭配 **-um**、 **-cs**、 **-css** 或 **-公里** 引數。</span><span class="sxs-lookup"><span data-stu-id="60556-198">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="60556-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *前置* 詞</span><span class="sxs-lookup"><span data-stu-id="60556-199"><span id="-P_prefix"></span><span id="-p_prefix"></span><span id="-P_PREFIX"></span>**-P** *prefix*</span></span>
</dt> <dd>

<span data-ttu-id="60556-200">使用這個引數，從您為事件指定的符號名稱開頭移除字元。</span><span class="sxs-lookup"><span data-stu-id="60556-200">Use this argument to remove characters from the beginning of the symbolic name that you specified for the event.</span></span> <span data-ttu-id="60556-201">此比較不區分大小寫。</span><span class="sxs-lookup"><span data-stu-id="60556-201">The comparison is case-insensitive.</span></span> <span data-ttu-id="60556-202">編譯器會使用符號名稱來構成記錄宏名稱和方法名稱。</span><span class="sxs-lookup"><span data-stu-id="60556-202">The compiler uses the symbolic name to form the logging macro names and method names.</span></span>

<span data-ttu-id="60556-203">記錄宏的預設名稱是 EventWrite *SymbolName*，其中 *SymbolName* 是您為事件指定的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="60556-203">The default name for a logging macro is EventWrite *SymbolName*, where *SymbolName* is the symbolic name that you specified for the event.</span></span> <span data-ttu-id="60556-204">例如，如果您將事件的 symbol 屬性設為 PrinterConnection，則宏名稱會是 EventWritePrinterConnection。</span><span class="sxs-lookup"><span data-stu-id="60556-204">For example, if you set the symbol attribute of the event to PrinterConnection, the macro name would be EventWritePrinterConnection.</span></span> <span data-ttu-id="60556-205">若要從名稱移除印表機，請使用 **-P** **印表機**，這會導致 EventWriteConnection。</span><span class="sxs-lookup"><span data-stu-id="60556-205">To remove Printer from the name, use **-P** **Printer**, which results in EventWriteConnection.</span></span>

<span data-ttu-id="60556-206">您可以使用這個引數搭配 **-um**、 **-cs**、 **-css** 或 **-公里** 引數。</span><span class="sxs-lookup"><span data-stu-id="60556-206">You can use this argument with the **-um**, **-cs**, **-css**, or **-km** argument.</span></span>

</dd> <dt>

<span data-ttu-id="60556-207"><span id="-um"></span><span id="-UM"></span>**-um**</span><span class="sxs-lookup"><span data-stu-id="60556-207"><span id="-um"></span><span id="-UM"></span>**-um**</span></span>
</dt> <dd>

<span data-ttu-id="60556-208">您可以使用這個引數，讓編譯器產生使用者模式程式碼，用來記錄您在資訊清單中定義的事件。</span><span class="sxs-lookup"><span data-stu-id="60556-208">Use this argument to have the compiler generate the user-mode code that you would use to log the events defined in your manifest.</span></span>

</dd> </dl>

<span data-ttu-id="60556-209">若要讓編譯器產生記錄程式碼，您必須指定 **-um**、 **-cs**、 **-css** 或 **-公里** 引數;這些引數都是互斥的。</span><span class="sxs-lookup"><span data-stu-id="60556-209">To have the compiler generate logging code, you must specify the **-um**, **-cs**, **-css**, or **-km** argument; these arguments are mutually exclusive.</span></span>

<span data-ttu-id="60556-210">若要指定編譯器所產生之 .h、.cs 和 mof 檔案的放置位置，請使用 **-h** 引數。</span><span class="sxs-lookup"><span data-stu-id="60556-210">To specify where to place the .h, .cs, and .mof files that the compiler generates, use the **-h** argument.</span></span> <span data-ttu-id="60556-211">如果您未指定 **-h** 引數，則會將檔案放在目前的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="60556-211">If you do not specify the **-h** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="60556-212">若要指定要將 .rc 檔和二進位檔案放 (的位置，其中包含編譯器所產生) 的中繼資料資源，請使用 **-r** 引數。</span><span class="sxs-lookup"><span data-stu-id="60556-212">To specify where to place the .rc file and binary files (that contain the metadata resources) that the compiler generates, use the **-r** argument.</span></span> <span data-ttu-id="60556-213">如果您未指定 **-r** 引數，則會將檔案放在目前的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="60556-213">If you do not specify the **-r** argument, the files are placed in the current folder.</span></span>

<span data-ttu-id="60556-214">編譯器會使用輸入檔的基底名稱做為它所產生之檔案的基底名稱。</span><span class="sxs-lookup"><span data-stu-id="60556-214">The compiler uses the base name of the input file as the base name of the files that it generates.</span></span> <span data-ttu-id="60556-215">若要指定基底名稱，請使用 **-z** 引數。</span><span class="sxs-lookup"><span data-stu-id="60556-215">To specify a base name, use the **-z** argument.</span></span>

### <a name="arguments-specific-to-message-text-files"></a><span data-ttu-id="60556-216">訊息文字檔特定的引數</span><span class="sxs-lookup"><span data-stu-id="60556-216">Arguments specific to message text files</span></span>

<dl> <dt>

<span data-ttu-id="60556-217"><span id="-a"></span><span id="-A"></span>**-a**</span><span class="sxs-lookup"><span data-stu-id="60556-217"><span id="-a"></span><span id="-A"></span>**-a**</span></span>
</dt> <dd>

<span data-ttu-id="60556-218">使用這個引數來指定 *檔案名* 輸入檔案包含系統預設 Windows ANSI 字碼頁中的內容 (CP_ACP) 。</span><span class="sxs-lookup"><span data-stu-id="60556-218">Use this argument to specify that the *filename* input file contains content in the system-default Windows ANSI code page (CP_ACP).</span></span> <span data-ttu-id="60556-219">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="60556-219">This is the default.</span></span> <span data-ttu-id="60556-220">使用 **-u** 代表 Unicode。</span><span class="sxs-lookup"><span data-stu-id="60556-220">Use **-u** for Unicode.</span></span> <span data-ttu-id="60556-221">如果輸入檔包含 BOM，則會忽略此引數。</span><span class="sxs-lookup"><span data-stu-id="60556-221">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="60556-222"><span id="-A"></span><span id="-a"></span>**-A**</span><span class="sxs-lookup"><span data-stu-id="60556-222"><span id="-A"></span><span id="-a"></span>**-A**</span></span>
</dt> <dd>

<span data-ttu-id="60556-223">廢棄。</span><span class="sxs-lookup"><span data-stu-id="60556-223">DEPRECATED.</span></span> <span data-ttu-id="60556-224">使用這個引數來指定輸出 bin 檔案中的訊息應該是 ANSI。</span><span class="sxs-lookup"><span data-stu-id="60556-224">Use this argument to specify that the messages in the output .bin file should be ANSI.</span></span>

</dd> <dt>

<span data-ttu-id="60556-225"><span id="-b"></span><span id="-B"></span>**-b**</span><span class="sxs-lookup"><span data-stu-id="60556-225"><span id="-b"></span><span id="-B"></span>**-b**</span></span>
</dt> <dd>

<span data-ttu-id="60556-226">您可以使用這個引數，讓編譯器使用 *檔案名* 輸入檔的基底名稱作為 bin 檔案名。</span><span class="sxs-lookup"><span data-stu-id="60556-226">Use this argument to have the compiler use the base name of the *filename* input file for the .bin file names.</span></span> <span data-ttu-id="60556-227">預設值是使用 "MSG"。</span><span class="sxs-lookup"><span data-stu-id="60556-227">The default is to use "MSG".</span></span>

</dd> <dt>

<span data-ttu-id="60556-228"><span id="-d"></span><span id="-D"></span>**-d.ddd...e**</span><span class="sxs-lookup"><span data-stu-id="60556-228"><span id="-d"></span><span id="-D"></span>**-d**</span></span>
</dt> <dd>

<span data-ttu-id="60556-229">使用這個引數可針對標頭檔中的嚴重性和設備常數使用十進位值，而不是使用十六進位值。</span><span class="sxs-lookup"><span data-stu-id="60556-229">Use this argument to use decimal values for the Severity and Facility constants in the header file instead of hexadecimal values.</span></span>

</dd> <dt>

<span data-ttu-id="60556-230"><span id="-n"></span><span id="-N"></span>**-n**</span><span class="sxs-lookup"><span data-stu-id="60556-230"><span id="-n"></span><span id="-N"></span>**-n**</span></span>
</dt> <dd>

<span data-ttu-id="60556-231">使用這個引數來指定訊息在訊息本文之後立即終止。</span><span class="sxs-lookup"><span data-stu-id="60556-231">Use this argument to specify that messages terminate immediately after the message body.</span></span> <span data-ttu-id="60556-232">預設值是使用 CR/LF 來終止訊息主體。</span><span class="sxs-lookup"><span data-stu-id="60556-232">The default is to terminate the message body with a CR/LF.</span></span>

</dd> <dt>

<span data-ttu-id="60556-233"><span id="-o"></span><span id="-O"></span>**-o**</span><span class="sxs-lookup"><span data-stu-id="60556-233"><span id="-o"></span><span id="-O"></span>**-o**</span></span>
</dt> <dd>

<span data-ttu-id="60556-234">您可以使用這個引數，讓編譯器使用 **HRESULT** 定義來產生 OLE2 標頭檔，而不是狀態碼。</span><span class="sxs-lookup"><span data-stu-id="60556-234">Use this argument to have the compiler generate an OLE2 header file using **HRESULT** definitions instead of status codes.</span></span> <span data-ttu-id="60556-235">預設會使用狀態碼。</span><span class="sxs-lookup"><span data-stu-id="60556-235">Using status codes is the default.</span></span>

</dd> <dt>

<span data-ttu-id="60556-236"><span id="-u"></span><span id="-U"></span>**-u**</span><span class="sxs-lookup"><span data-stu-id="60556-236"><span id="-u"></span><span id="-U"></span>**-u**</span></span>
</dt> <dd>

<span data-ttu-id="60556-237">使用這個引數來指定 *檔案名* 輸入檔案包含 utf-16le 內容。</span><span class="sxs-lookup"><span data-stu-id="60556-237">Use this argument to specify that the *filename* input file contains UTF-16LE content.</span></span> <span data-ttu-id="60556-238">預設值為 ANSI 內容。</span><span class="sxs-lookup"><span data-stu-id="60556-238">The default is ANSI content.</span></span> <span data-ttu-id="60556-239">如果輸入檔包含 BOM，則會忽略此引數。</span><span class="sxs-lookup"><span data-stu-id="60556-239">If the input file contains a BOM this argument will be ignored.</span></span>

</dd> <dt>

<span data-ttu-id="60556-240"><span id="-U"></span><span id="-u"></span>**-U**</span><span class="sxs-lookup"><span data-stu-id="60556-240"><span id="-U"></span><span id="-u"></span>**-U**</span></span>
</dt> <dd>

<span data-ttu-id="60556-241">使用這個引數來指定輸出 bin 檔案中的訊息應該是 Unicode。</span><span class="sxs-lookup"><span data-stu-id="60556-241">Use this argument to specify that the messages in the output .bin file should be Unicode.</span></span> <span data-ttu-id="60556-242">此為預設值。</span><span class="sxs-lookup"><span data-stu-id="60556-242">This is the default.</span></span>

</dd> <dt>

<span data-ttu-id="60556-243"><span id="-v"></span><span id="-V"></span>**-v**</span><span class="sxs-lookup"><span data-stu-id="60556-243"><span id="-v"></span><span id="-V"></span>**-v**</span></span>
</dt> <dd>

<span data-ttu-id="60556-244">使用這個引數以產生詳細資訊輸出。</span><span class="sxs-lookup"><span data-stu-id="60556-244">Use this argument to generate verbose output.</span></span>

</dd> <dt>

<span data-ttu-id="60556-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *路徑*</span><span class="sxs-lookup"><span data-stu-id="60556-245"><span id="-x_path"></span><span id="-X_PATH"></span>**-x** *path*</span></span>
</dt> <dd>

<span data-ttu-id="60556-246">您可以使用這個引數來指定您要編譯器放置 dbg C include 檔的資料夾。</span><span class="sxs-lookup"><span data-stu-id="60556-246">Use this argument to specify the folder into which you want the compiler to place the .dbg C include file.</span></span> <span data-ttu-id="60556-247">此 dbg 檔案會將訊息識別碼對應至其符號名稱。</span><span class="sxs-lookup"><span data-stu-id="60556-247">The .dbg file maps message IDs to their symbolic names.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="60556-248">備註</span><span class="sxs-lookup"><span data-stu-id="60556-248">Remarks</span></span>

<span data-ttu-id="60556-249">**-A** 和 **-mof** 引數已淘汰，未來將會移除。</span><span class="sxs-lookup"><span data-stu-id="60556-249">The **-A** and **-mof** arguments are deprecated and will be removed in the future.</span></span>

<span data-ttu-id="60556-250">編譯器會將資訊清單接受為輸入 ( 的) 檔案或郵件內文 ( mc) 檔案，並產生下列檔案：</span><span class="sxs-lookup"><span data-stu-id="60556-250">The compiler accepts as input a manifest (.man) file or a message text (.mc) file and generates the following files:</span></span>

-   <span data-ttu-id="60556-251">*filename*。h</span><span class="sxs-lookup"><span data-stu-id="60556-251">*filename*.h</span></span>

    <span data-ttu-id="60556-252">C/c + + 標頭檔，其中包含您在應用程式中參考的事件描述元、提供者 GUID 和符號名稱。</span><span class="sxs-lookup"><span data-stu-id="60556-252">A C/C++ header file that contains the event descriptors, provider GUID, and symbol names that you reference in your application.</span></span>

-   <span data-ttu-id="60556-253">*檔案名* 臨時 bin</span><span class="sxs-lookup"><span data-stu-id="60556-253">*filename* TEMP.bin</span></span>

    <span data-ttu-id="60556-254">包含提供者和事件中繼資料的二進位資源檔。</span><span class="sxs-lookup"><span data-stu-id="60556-254">A binary resource file that contains the provider and event metadata.</span></span> <span data-ttu-id="60556-255">這是範本資源，以檔案基底名稱的暫存尾碼表示。</span><span class="sxs-lookup"><span data-stu-id="60556-255">This is the template resource, which is signified by the TEMP suffix of the base name of the file.</span></span>

-   <span data-ttu-id="60556-256">Msg00001 bin</span><span class="sxs-lookup"><span data-stu-id="60556-256">Msg00001.bin</span></span>

    <span data-ttu-id="60556-257">您所指定之每種語言的二進位資源檔 (例如，如果您的資訊清單包含 en-us 和 fr-fr 中的訊息字串，則編譯器會產生 Msg00001 bin 和 Msg00002) 。</span><span class="sxs-lookup"><span data-stu-id="60556-257">A binary resource file for each language that you specify (for example, if your manifest contains message strings in en-US and fr-FR, the compiler would generate Msg00001.bin and Msg00002.bin).</span></span>

-   <span data-ttu-id="60556-258">*檔案名*.rc</span><span class="sxs-lookup"><span data-stu-id="60556-258">*filename*.rc</span></span>

    <span data-ttu-id="60556-259">資源編譯器腳本，其中包含要包含每個 bin 檔案做為資源的語句。</span><span class="sxs-lookup"><span data-stu-id="60556-259">A resource compiler script that contains the statements to include each .bin file as a resource.</span></span>

<span data-ttu-id="60556-260">若為採用路徑的引數，路徑可以是絕對路徑、相對路徑或 UNC 路徑，而且可以包含環境變數。</span><span class="sxs-lookup"><span data-stu-id="60556-260">For arguments that take a path, the path can be an absolute, relative, or UNC path and it can contain environment variables.</span></span>

<span data-ttu-id="60556-261">**在 MC 版本1.12.7051 之前：** 編譯器不允許相對路徑或環境變數。</span><span class="sxs-lookup"><span data-stu-id="60556-261">**Prior to MC version 1.12.7051:** The compiler does not allow relative paths or environment variables.</span></span>

<span data-ttu-id="60556-262">Windows SDK 包含 Bin 資料夾中的編譯器 (mc.exe) \\ 。</span><span class="sxs-lookup"><span data-stu-id="60556-262">The Windows SDK includes the compiler (mc.exe) in the \\Bin folder.</span></span>

## <a name="examples"></a><span data-ttu-id="60556-263">範例</span><span class="sxs-lookup"><span data-stu-id="60556-263">Examples</span></span>

<span data-ttu-id="60556-264">下列範例會使用編譯器預設值來編譯資訊清單。</span><span class="sxs-lookup"><span data-stu-id="60556-264">The following example compiles a manifest using the compiler defaults.</span></span>

``` syntax
mc spooler.man
```

<span data-ttu-id="60556-265">下列範例會編譯資訊清單，並將標頭和資源檔放在指定的資料夾中。</span><span class="sxs-lookup"><span data-stu-id="60556-265">The following example compiles the manifest and places the header and resource files in the specified folders.</span></span>

``` syntax
mc -h <pathgoeshere> -r <pathgoeshere> spooler.man
```

## <a name="requirements"></a><span data-ttu-id="60556-266">規格需求</span><span class="sxs-lookup"><span data-stu-id="60556-266">Requirements</span></span>

| <span data-ttu-id="60556-267">需求</span><span class="sxs-lookup"><span data-stu-id="60556-267">Requirement</span></span> | <span data-ttu-id="60556-268">值</span><span class="sxs-lookup"><span data-stu-id="60556-268">Value</span></span> |
|--------------------------|-------------------------------------------------|
| <span data-ttu-id="60556-269">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="60556-269">Minimum supported client</span></span> | <span data-ttu-id="60556-270">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60556-270">Windows 2000 Professional \[desktop apps only\]</span></span> |
| <span data-ttu-id="60556-271">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="60556-271">Minimum supported server</span></span> | <span data-ttu-id="60556-272">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="60556-272">Windows 2000 Server \[desktop apps only\]</span></span>       |
