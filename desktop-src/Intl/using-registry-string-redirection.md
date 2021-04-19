---
description: 登錄中硬式編碼字串的儲存是 Windows Vista 之前的當地語系化模型的一部分。
ms.assetid: 70185942-7d32-4151-a4e1-f71cf45e87af
title: 使用登錄字串重新導向
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 287f6e1420aae0ff41c386e19852bebbd1a322c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980084"
---
# <a name="using-registry-string-redirection"></a><span data-ttu-id="c08c7-103">使用登錄字串重新導向</span><span class="sxs-lookup"><span data-stu-id="c08c7-103">Using Registry String Redirection</span></span>

<span data-ttu-id="c08c7-104">登錄中硬式編碼字串的儲存是 Windows Vista 之前的當地語系化模型的一部分。</span><span class="sxs-lookup"><span data-stu-id="c08c7-104">Storage of hard-coded strings in the registry is part of a pre-Windows Vista localization model.</span></span> <span data-ttu-id="c08c7-105">MUI 不支援此功能。</span><span class="sxs-lookup"><span data-stu-id="c08c7-105">It is not supported by MUI.</span></span> <span data-ttu-id="c08c7-106">在目前的模型中，作業系統的使用者介面會在語言中立的基底之上，以特定語言的資源檔執行。</span><span class="sxs-lookup"><span data-stu-id="c08c7-106">In the current model, the user interface for the operating system runs in language-specific resource files on top of a language-neutral base.</span></span> <span data-ttu-id="c08c7-107">作業系統的元件會以非語言相關的方式使用登錄。</span><span class="sxs-lookup"><span data-stu-id="c08c7-107">The components of the operating system use the registry in a language-neutral manner.</span></span>

<span data-ttu-id="c08c7-108">MUI 只會使用基底語言資源檔中的 Win32 PE 資源所定義的重新導向登錄字串。</span><span class="sxs-lookup"><span data-stu-id="c08c7-108">MUI uses only redirected registry strings defined by Win32 PE resources in the base language resource file.</span></span> <span data-ttu-id="c08c7-109">重新導向是個別定義，例如在 .inf 檔案中。</span><span class="sxs-lookup"><span data-stu-id="c08c7-109">Redirection is defined separately, for example, in an .inf file.</span></span> <span data-ttu-id="c08c7-110">這種類型的儲存體可讓資源載入器在資源模組載入期間自動選取正確的語言資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-110">This type of storage allows the resource loader to select the correct language resources automatically during resource module loading.</span></span>

> [!Note]  
> <span data-ttu-id="c08c7-111">本主題僅適用于 Win32 PE 資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-111">This topic pertains only to Win32 PE resources.</span></span> <span data-ttu-id="c08c7-112">如果使用非 Win32 PE 資源，您必須提供自訂的登錄字串重新導向（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="c08c7-112">If using non-Win32 PE resources, you must provide customized registry string redirection, if required.</span></span>

 

## <a name="create-a-language-neutral-resource"></a><span data-ttu-id="c08c7-113">建立 Language-Neutral 資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-113">Create a Language-Neutral Resource</span></span>

<span data-ttu-id="c08c7-114">在 Windows Vista 和更新版本上執行的 MUI 應用程式會使用中性語言的字串資源，以允許存取儲存在字串資源資料表中的特定語言字串。</span><span class="sxs-lookup"><span data-stu-id="c08c7-114">A MUI application running on Windows Vista and later uses a language-neutral string resource to allow access to language-specific strings stored in a string resource table.</span></span> <span data-ttu-id="c08c7-115">從登錄中讀取這些值的應用程式程式碼會在 [尋找重新導向字串](locating-redirected-strings.md)的 [載入 Language-Neutral 登錄值] 區段中描述。</span><span class="sxs-lookup"><span data-stu-id="c08c7-115">Application code that reads these values from the registry is described in the Load a Language-Neutral Registry Value section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="c08c7-116">語言中立登錄值的資料格式為 " `@<PE-path>,-<stringID>[;<comment>]` "，其中：</span><span class="sxs-lookup"><span data-stu-id="c08c7-116">The data for a language-neutral registry value has the format "`@<PE-path>,-<stringID>[;<comment>]`", where:</span></span>

-   <span data-ttu-id="c08c7-117">*PE 路徑* 指定可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="c08c7-117">*PE-path* specifies the path of the executable.</span></span> <span data-ttu-id="c08c7-118">您可以使用環境變數（例如% ProgramFiles%）來指定路徑，以支援部署。</span><span class="sxs-lookup"><span data-stu-id="c08c7-118">You can specify the path using an environment variable, such as %ProgramFiles%, to support deployment.</span></span> <span data-ttu-id="c08c7-119">進行字串參考的替代方法是省略檔案路徑資訊。</span><span class="sxs-lookup"><span data-stu-id="c08c7-119">An alternative for making your string reference is to leave out the file path information.</span></span> <span data-ttu-id="c08c7-120">在此情況下，您的應用程式必須有一些方法（例如，另一個登錄值），才能傳達自己的安裝目錄。</span><span class="sxs-lookup"><span data-stu-id="c08c7-120">In this case, your application must have some means, for example, another registry value, to communicate its own install directory.</span></span>
-   <span data-ttu-id="c08c7-121">*stringid 指定* 會指定相關字串資源的數值資源識別碼，其執行方式就像任何其他可當地語系化的字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-121">*stringID* specifies the numeric resource identifier of the relevant string resource, which is implemented just like any other localizable string resource.</span></span>
-   <span data-ttu-id="c08c7-122">*批註* 會指定選擇性的資訊來進行偵錯工具或登錄值的可讀性。</span><span class="sxs-lookup"><span data-stu-id="c08c7-122">*comment* specifies optional information for debugging or readability of the registry value.</span></span> <span data-ttu-id="c08c7-123">登錄 API 函數會在載入字串時忽略批註。</span><span class="sxs-lookup"><span data-stu-id="c08c7-123">The registry API functions ignore the comment when loading the string.</span></span>

> [!Note]  
> <span data-ttu-id="c08c7-124">登錄值的資料不會明確參考特定語言的資源檔。</span><span class="sxs-lookup"><span data-stu-id="c08c7-124">The data for the registry value makes no explicit reference to the language-specific resource file.</span></span> <span data-ttu-id="c08c7-125">根據目前的使用者介面語言喜好設定，在執行時間決定正確的檔案。</span><span class="sxs-lookup"><span data-stu-id="c08c7-125">The correct file is determined at runtime, based on the current user interface language preferences.</span></span>

 

<span data-ttu-id="c08c7-126">輸入的登錄值不會有 "，" 和 "-" 之間的空格。</span><span class="sxs-lookup"><span data-stu-id="c08c7-126">A registry value is entered without a space between the "," and "-".</span></span> <span data-ttu-id="c08c7-127">正確的登錄值為：</span><span class="sxs-lookup"><span data-stu-id="c08c7-127">A correct registry value is:</span></span>

`shell32.dll,-22912`

<span data-ttu-id="c08c7-128">不正確的登錄值為：</span><span class="sxs-lookup"><span data-stu-id="c08c7-128">An incorrect registry value is:</span></span>

`shell32.dll, -22912`

<span data-ttu-id="c08c7-129">Windows Vista 的其中一個範例是具有下列資料的登錄值：</span><span class="sxs-lookup"><span data-stu-id="c08c7-129">An example from Windows Vista is the registry value with the following data:</span></span>

`@%SystemRoot%\system32\input.dll,-5020`

## <a name="create-resources-for-shortcut-strings"></a><span data-ttu-id="c08c7-130">建立快捷方式字串的資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-130">Create Resources for Shortcut Strings</span></span>

<span data-ttu-id="c08c7-131">當 MUI 應用程式在 shell 使用者介面中顯示其名稱時，會顯示應用程式圖示的提示字元字串。</span><span class="sxs-lookup"><span data-stu-id="c08c7-131">When the MUI application displays its name in the shell user interface, an InfoTip string is displayed for the application icon.</span></span> <span data-ttu-id="c08c7-132">針對每個支援的語言，您應該建立應用程式顯示名稱和相關聯的提示字元字串的字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-132">You should create string resources for your application display name and associated InfoTip string for each supported language.</span></span> <span data-ttu-id="c08c7-133">當資源就緒時，您的應用程式可以使用在 [尋找重新導向字串](locating-redirected-strings.md)的登錄區段中，使用 Shell API 中所述的字串來載入快速鍵字串。</span><span class="sxs-lookup"><span data-stu-id="c08c7-133">When the resources are ready, your application can use the strings as described in the Use Shell API to Load Shortcut Strings from the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

### <a name="prepare-resources-for-a-shortcut-created-with-windows-installer"></a><span data-ttu-id="c08c7-134">準備使用 Windows Installer 建立之快捷方式的資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-134">Prepare Resources for a Shortcut Created with Windows Installer</span></span>

<span data-ttu-id="c08c7-135">如果您使用 Windows Installer (MSI) 建立快捷方式，則字串資源會包含快捷方式顯示名稱和描述。</span><span class="sxs-lookup"><span data-stu-id="c08c7-135">If you use Windows Installer (MSI) to create a shortcut, string resources include shortcut display name and description.</span></span> <span data-ttu-id="c08c7-136">在 [MSI 快速鍵資料表](../msi/shortcut-table.md)中，資源 DLL 會在適當的資料行中參考，而快速鍵顯示名稱和描述的資源識別碼則會用於對應的資源識別碼資料行。</span><span class="sxs-lookup"><span data-stu-id="c08c7-136">In the [MSI shortcut table](../msi/shortcut-table.md), the resource DLL is referenced in the appropriate columns and the resource identifiers for your shortcut display name and description are used in the corresponding resource identifier columns.</span></span>

<span data-ttu-id="c08c7-137">為了讓應用程式快捷方式可與 MUI 資源技術正常搭配運作，請在準備快速鍵字串時記住下列幾點：</span><span class="sxs-lookup"><span data-stu-id="c08c7-137">So that the application shortcut works properly with MUI resource technology, keep the following points in mind when preparing the shortcut strings:</span></span>

-   <span data-ttu-id="c08c7-138">請使用環境變數或相對路徑來註冊 DLL。</span><span class="sxs-lookup"><span data-stu-id="c08c7-138">Use either environment variables or a relative path to register the DLL.</span></span> <span data-ttu-id="c08c7-139">您可以指定 @% systemroot% \\ system32shell32.dll，只要登錄 \\ 字串類型為 REG \_ EXPAND SZ 即可 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c08c7-139">You can specify @%systemroot%\\system32\\shell32.dll as long as the registry string type is REG\_EXPAND\_SZ.</span></span> <span data-ttu-id="c08c7-140">Shell32.dll 中「文字檔」的字串資源識別碼為12345。</span><span class="sxs-lookup"><span data-stu-id="c08c7-140">The string resource identifier for "Text Document" in Shell32.dll is 12345.</span></span>
-   <span data-ttu-id="c08c7-141">請勿在 "，" 和 "-" 符號前後使用空格。</span><span class="sxs-lookup"><span data-stu-id="c08c7-141">Do not use spaces around the "," and "-" symbols.</span></span> <span data-ttu-id="c08c7-142">正確的範例是 "shell32.dll，-22912"。</span><span class="sxs-lookup"><span data-stu-id="c08c7-142">A correct example is "shell32.dll,-22912".</span></span>
-   <span data-ttu-id="c08c7-143">請勿使用簡短的檔案名。</span><span class="sxs-lookup"><span data-stu-id="c08c7-143">Do not use a short file name.</span></span> <span data-ttu-id="c08c7-144">此類型的名稱不適用於資源載入器。</span><span class="sxs-lookup"><span data-stu-id="c08c7-144">This type of name does not work with the resource loader.</span></span>

### <a name="prepare-resources-for-a-shortcut-using-inf-format"></a><span data-ttu-id="c08c7-145">使用 INF 格式準備快速鍵的資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-145">Prepare Resources for a Shortcut Using INF Format</span></span>

<span data-ttu-id="c08c7-146">如果您使用 INF 檔案格式來建立快捷方式字串，資源檔應該進行下列登錄設定。</span><span class="sxs-lookup"><span data-stu-id="c08c7-146">If you use the INF file format to create shortcut strings, the resource file should make the following registry settings.</span></span> <span data-ttu-id="c08c7-147">這些指示假設您使用的是安裝程式 API 的 ProfileItems 語法。</span><span class="sxs-lookup"><span data-stu-id="c08c7-147">These instructions assume the use of the ProfileItems syntax of Setup API.</span></span>

1.  <span data-ttu-id="c08c7-148">使用路徑和資源識別碼，將 [提示] 值變更為指向 [字串重新導向參考]。</span><span class="sxs-lookup"><span data-stu-id="c08c7-148">Change the InfoTip value to point to the string redirection reference, using the path and resource identifier.</span></span>
2.  <span data-ttu-id="c08c7-149">在 ProfileItems 安裝區段底下新增值 DisplayResource。</span><span class="sxs-lookup"><span data-stu-id="c08c7-149">Add the new value DisplayResource under the ProfileItems installation sections.</span></span>

<span data-ttu-id="c08c7-150">下列範例顯示如何將計算機應用程式新增至 [ **開始** ] 功能表：</span><span class="sxs-lookup"><span data-stu-id="c08c7-150">The following is an example showing the addition of the Calculator application to the **Start** menu:</span></span>


```C++
[CalcInstallItems]
"Name" = %Calc_DESC%
"CmdLine" = 11, calc.exe
"SubDir" = %Access_GROUP%
"WorkingDir" = 11

"InfoTip" = "@%systemroot%\system32\shell32.dll,-22531"

"DisplayResource" = "%systemroot%\system32\shell32.dll",22019
```



<span data-ttu-id="c08c7-151">使用 INF 將專案（例如存取群組資料夾）新增至 [ **開始** ] 功能表時，請使用如下所示的語法。</span><span class="sxs-lookup"><span data-stu-id="c08c7-151">Use the syntax shown below when using INF to add items, for example, an Access Group folder, to the **Start** menu.</span></span> <span data-ttu-id="c08c7-152">此語法假設 \[ \] 從安裝程式使用 StartMenuItems 支援，類似于 Syssetup 中使用的語法。</span><span class="sxs-lookup"><span data-stu-id="c08c7-152">This syntax assumes the use of \[StartMenuItems\] support from Setup, similar to the syntax used in Syssetup.inf.</span></span>


```C++
[StartMenuItems]
<description> = <binary>,<commandline>,<iconfile>,<iconnum>,<infotip>,<resDLL,resID>
```



<span data-ttu-id="c08c7-153">將 *[值]* 提示字元設定為字串參考 " `@<path>,-resID` "。</span><span class="sxs-lookup"><span data-stu-id="c08c7-153">Set the value *infotip* to the string reference "`@<path>,-resID`".</span></span>

<span data-ttu-id="c08c7-154">顯示名稱取決於 *resDLL* 和 *resID* 值。</span><span class="sxs-lookup"><span data-stu-id="c08c7-154">The display name is determined by the *resDLL* and *resID* values.</span></span> <span data-ttu-id="c08c7-155">*ResID* 值會指定與非語言相關檔案相關聯之字串資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c08c7-155">The *resID* value specifies the resource identifier for a string resource associated with the language-neutral file.</span></span> <span data-ttu-id="c08c7-156">*ResDLL* 值指定非語言相關檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="c08c7-156">The *resDLL* value specifies the path to the language-neutral file.</span></span>

## <a name="create-resources-for-friendly-document-type-names"></a><span data-ttu-id="c08c7-157">建立易記檔案類型名稱的資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-157">Create Resources for Friendly Document Type Names</span></span>

<span data-ttu-id="c08c7-158">您必須將應用程式的易記名稱和提示字元字串作為字串資源來執行。</span><span class="sxs-lookup"><span data-stu-id="c08c7-158">You must implement friendly name and InfoTip strings for your application as string resources.</span></span> <span data-ttu-id="c08c7-159">若要允許易記的檔案類型名稱回應使用者介面語言，應用程式必須在檔案類型的程式識別碼機碼下，使用 FriendlyTypeName 值來註冊名稱。</span><span class="sxs-lookup"><span data-stu-id="c08c7-159">To allow friendly document type names to react to the user interface language, the application must register the names using the FriendlyTypeName value under the program identifier key for the file type.</span></span> <span data-ttu-id="c08c7-160">應該保留程式識別碼金鑰的預設值，以維持回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="c08c7-160">The default value for the program identifier key should be retained to keep backward compatibility.</span></span> <span data-ttu-id="c08c7-161">如需從應用程式存取名稱的詳細資訊，請參閱 [尋找重新導向字串](locating-redirected-strings.md)之登錄區段中的查詢易記檔案類型名稱。</span><span class="sxs-lookup"><span data-stu-id="c08c7-161">For information about accessing the names from your application, see the Query Friendly Document Type Names in the Registry section of [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

<span data-ttu-id="c08c7-162">特定工作牽涉到下列步驟：</span><span class="sxs-lookup"><span data-stu-id="c08c7-162">The specific work involves the following steps:</span></span>

1.  <span data-ttu-id="c08c7-163">將易記名稱和提示字串實作為特定語言的字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-163">Implement the friendly name and InfoTip strings as language-specific string resources.</span></span>
2.  <span data-ttu-id="c08c7-164">在 [檔案類型] 登錄機碼底下新增 FriendlyTypeName 值。</span><span class="sxs-lookup"><span data-stu-id="c08c7-164">Add the FriendlyTypeName value under the document type registry key.</span></span> <span data-ttu-id="c08c7-165">值的資料會在模式 "" 之後 `@<path>,-<resID>` ，其中 *path* 表示可執行檔，而 *resID* 是與該可執行檔相關聯之可當地語系化字串資源的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c08c7-165">The data for the value follows the pattern "`@<path>,-<resID>`", where *path* indicates the executable and *resID* is the resource identifier of a localizable string resource associated with that executable.</span></span>
3.  <span data-ttu-id="c08c7-166">根據 "" 格式指定提示登錄值 `@<path>,-<resID>` 。</span><span class="sxs-lookup"><span data-stu-id="c08c7-166">Specify the InfoTip registry value according to the format "`@<path>,-<resID>`".</span></span>

<span data-ttu-id="c08c7-167">下列範例顯示 .txt 檔案的登錄設定：</span><span class="sxs-lookup"><span data-stu-id="c08c7-167">The following example shows the registry settings for a .txt file:</span></span>


```C++
HKCR\.txt
@="txtfile"
"Content Type"="text/plain"

HKCR\txtfile
@="Text Document"

"FriendlyTypeName" = "@%systemroot%\system32\shell32.dll,-12345"

"InfoTip" = "@%systemroot%\system32\shell32.dll,-12346"
```



## <a name="provide-resources-for-shell-verb-action-strings"></a><span data-ttu-id="c08c7-168">提供 Shell 動詞動作字串的資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-168">Provide Resources for Shell Verb Action Strings</span></span>

<span data-ttu-id="c08c7-169">特定動詞的動作字串（例如「開啟」和「編輯」）會顯示在使用者以滑鼠右鍵按一下 Windows 檔案總管中的檔案時顯示的快顯功能表中。</span><span class="sxs-lookup"><span data-stu-id="c08c7-169">Action strings for certain verbs, for example, "open" and "edit", are shown in the pop-up menu displayed when the user right-clicks a file in Windows Explorer.</span></span> <span data-ttu-id="c08c7-170">您的應用程式不需要指定常用 shell 動詞命令的字串，因為 shell 針對這些動詞電腦有其具有 MUI 功能的預設值。</span><span class="sxs-lookup"><span data-stu-id="c08c7-170">Your application does not have to specify strings for common shell verbs, as the shell has its own MUI-enabled defaults for these verbs.</span></span> <span data-ttu-id="c08c7-171">不過，您應該為代表不尋常動詞的字串提供可當地語系化的字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-171">However, you should provide localizable string resources for strings representing uncommon verbs.</span></span>

<span data-ttu-id="c08c7-172">在 Windows XP 之前的作業系統上，會使用下列語法來轉譯登錄中 shell 動詞命令的字串，其中 *verb* 會指定實際的動詞名稱：</span><span class="sxs-lookup"><span data-stu-id="c08c7-172">On pre-Windows XP operating systems, strings for shell verbs in the registry are rendered using the following syntax, where *verb* specifies the actual verb name:</span></span>


```C++
HKCR\<progid>\shell\<verb>
@ = <friendly-name>
```



<span data-ttu-id="c08c7-173">以下為範例：</span><span class="sxs-lookup"><span data-stu-id="c08c7-173">Here's an example:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
```



<span data-ttu-id="c08c7-174">在 Windows XP 和更新版本上，您可以使用間接取值層級，讓動作字串相依于使用者介面語言。</span><span class="sxs-lookup"><span data-stu-id="c08c7-174">On Windows XP and later, you can use a level of indirection to make an action string depend on user interface language.</span></span> <span data-ttu-id="c08c7-175">這些作業系統支援 MUIVerb 值來定義與 MUI 相容的字串。</span><span class="sxs-lookup"><span data-stu-id="c08c7-175">These operating systems support a MUIVerb value for definition of a MUI-compatible string.</span></span> <span data-ttu-id="c08c7-176">以下是非常見動詞命令的登錄專案範例：</span><span class="sxs-lookup"><span data-stu-id="c08c7-176">Here's an example of a registry entry for an uncommon verb:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "Disconnect"
"MUIVerb" = "@%systemroot%\system32\sample.exe,-9875"
```



<span data-ttu-id="c08c7-177">您的 MUI 應用程式也應該能夠將舊的預設值註冊為可當地語系化的字串，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c08c7-177">Your MUI application should also be able to register the old default value as a localizable string, as shown below:</span></span>


```C++
HKCR\Sample.app\shell\Disc
@ = "@%systemroot%\system32\sample.exe,-9875"
```



> [!Note]  
> <span data-ttu-id="c08c7-178">不建議您註冊舊的預設值，因為它需要在 Windows XP 和更新版本上使用不同于舊版作業系統上的安裝程式進行不同的設定。</span><span class="sxs-lookup"><span data-stu-id="c08c7-178">Registration of the old default value is not recommended because it requires a different setup on Windows XP and later from the setup used on earlier operating systems.</span></span>

 

## <a name="create-resources-for-verb-protocol-and-auxusertype-strings"></a><span data-ttu-id="c08c7-179">建立動詞、通訊協定和 AuxUserType 字串的資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-179">Create Resources for Verb, Protocol, and AuxUserType Strings</span></span>

<span data-ttu-id="c08c7-180">您應該為動詞、Protocol 和 AuxUserType 字串建立可當地語系化的字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-180">You should create localizable string resources for Verb, Protocol, and AuxUserType strings.</span></span> <span data-ttu-id="c08c7-181">使用下列登錄設定：</span><span class="sxs-lookup"><span data-stu-id="c08c7-181">Use the following registry settings:</span></span>


```C++
HKCR\CLSID\{<Your_CLSID>}\Verb\<number> @="<Your Verb>, <menu_flag>, <verb_flag>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...

HKCR\CLSID\{<Your_CLSID>}\AuxUserType\<number>
@="<Your Short Name>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID1"
...

HKCR\<Your_Name>\protocol\StdFileEditing\verb\<number>
@="<Your Verb>"
"LocalizedString"="@<resDLLpath\resDLL.DLL>,-resStrID"
...
```



<span data-ttu-id="c08c7-182">針對 >localizedstring 指定的值只會包含或取代您的 *動詞* 值（而不是兩個旗標值）。</span><span class="sxs-lookup"><span data-stu-id="c08c7-182">The value specified for LocalizedString only contains or replaces the value for *Your Verb*, not the two flag values.</span></span>

<span data-ttu-id="c08c7-183">以下是可協助您確保正確登錄設定的摘要：</span><span class="sxs-lookup"><span data-stu-id="c08c7-183">Here is a summary to help you ensure correct registry settings:</span></span>

-   <span data-ttu-id="c08c7-184">如果 CLSID 有 HKCR \\ clsid \\ {clsid} 的 [插入] 索引 \\ 鍵，請使用 HKCR \\ CLSID \\ {clsid} >LOCALIZEDSTRING \\ 來定義預設的 clsid 值。</span><span class="sxs-lookup"><span data-stu-id="c08c7-184">If CLSID has a HKCR\\CLSID\\{clsid}\\Insertable key, define the default CLSID value using HKCR\\CLSID\\{clsid}\\LocalizedString.</span></span>
-   <span data-ttu-id="c08c7-185">如果 CLSID 在 HKCR clsid {clsid} 動詞下有一或多個子機碼 \\ \\ \\ ，請使用 HKCR \\ CLSID \\ {clsid} \\ 動詞 \\ xxx \\ >localizedstring 來定義每個個別的動詞字串。</span><span class="sxs-lookup"><span data-stu-id="c08c7-185">If CLSID has one or more subkeys under HKCR\\CLSID\\{clsid}\\Verb, define each individual Verb string using HKCR\\CLSID\\{clsid}\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="c08c7-186">如果 CLSID 在 HKCR {progid} protocol Stdfileediting 動詞下有一或多個子機碼 \\ \\ \\ \\ ，請使用 HKCR \\ {progid} \\ protocol \\ Stdfileediting \\ Verb \\ xxx >localizedstring \\ 來定義每個個別的動詞字串。</span><span class="sxs-lookup"><span data-stu-id="c08c7-186">If CLSID has one or more subkeys under HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb, define each individual Verb string using HKCR\\{progid}\\Protocol\\Stdfileediting\\Verb\\xxx\\LocalizedString.</span></span>
-   <span data-ttu-id="c08c7-187">如果 CLSID 在 HKCR clsid {clsid} AuxUserType 下有一或多個列出的 AuxUserType 子機碼 \\ \\ \\ ，請使用 HKCR \\ CLSID \\ {clsid} \\ AuxUserType \\ xxx \\ >localizedstring 來定義每個 AuxUserType 專案。</span><span class="sxs-lookup"><span data-stu-id="c08c7-187">If CLSID has one or more listed AuxUserType subkeys under HKCR\\CLSID\\{clsid}\\AuxUserType, define each AuxUserType entry using HKCR\\CLSID\\{clsid}\\AuxUserType\\xxx\\LocalizedString.</span></span>

## <a name="create-a-resource-for-the-uninstall-program"></a><span data-ttu-id="c08c7-188">建立卸載程式的資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-188">Create a Resource for the Uninstall Program</span></span>

<span data-ttu-id="c08c7-189">若要註冊應用程式的卸載程式，您可以在登錄機碼 HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ Windows \\ CurrentVersion \\ 卸載的應用程式的唯一識別碼子機碼中建立登錄值。</span><span class="sxs-lookup"><span data-stu-id="c08c7-189">To register the uninstall program for the application, you can create registry values in the unique identifier subkey for the application under the registry key HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows\\CurrentVersion\\Uninstall.</span></span> <span data-ttu-id="c08c7-190">要設定的值包括： DisplayName、DisplayVersion、Publisher、ProductID、RegOwner、RegCompany、UrlInfoAbout、HelpTelephone、HelpLink、InstallLocation、InstallSource、InstallDate、Contact、comment、DisplayIcon、Readme、UrlUpdateInfo。</span><span class="sxs-lookup"><span data-stu-id="c08c7-190">Values to set include: DisplayName, DisplayVersion, Publisher, ProductID, RegOwner, RegCompany, UrlInfoAbout, HelpTelephone, HelpLink, InstallLocation, InstallSource, InstallDate, Contact, Comments, DisplayIcon, Readme, UrlUpdateInfo.</span></span>

> [!Note]  
> <span data-ttu-id="c08c7-191">若要啟用每個值的 MUI 技術，您可以在值名稱中附加「 \_ 當地語系化」。</span><span class="sxs-lookup"><span data-stu-id="c08c7-191">To enable MUI technology for each value, you can append "\_Localized" to the value name.</span></span>

 

<span data-ttu-id="c08c7-192">需要作業系統元件才能針對 \_ 以 MUI 為特定的方式當地語系化的 DisplayName 提供值。</span><span class="sxs-lookup"><span data-stu-id="c08c7-192">Operating system components are required to provide a value for DisplayName\_Localized in a MUI-specific way.</span></span> <span data-ttu-id="c08c7-193">假設識別碼是1245，您應該將顯示名稱放在 DLL 中，例如 Res.dll，作為字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-193">You should place the display name in a DLL, such as Res.dll, as a string resource, assuming the identifier to be 1245.</span></span> <span data-ttu-id="c08c7-194">然後，應用程式可以將顯示名稱註冊為 \_ 使用 "@ \\res.DLL，-1245" 值當地語系化的 DisplayName。</span><span class="sxs-lookup"><span data-stu-id="c08c7-194">Then the application can register the display name as DisplayName\_Localized with value "@\\res.DLL,-1245".</span></span> <span data-ttu-id="c08c7-195">所有其他的登錄設定都應該保持不變，包括 DisplayName 的原始值。</span><span class="sxs-lookup"><span data-stu-id="c08c7-195">All the other registry settings should be retained as they are, including the original value for DisplayName.</span></span>

## <a name="create-resources-for-sound-events"></a><span data-ttu-id="c08c7-196">建立音效事件的資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-196">Create Resources for Sound Events</span></span>

<span data-ttu-id="c08c7-197">Windows 會將某些事件與音效檔產生關聯，例如新的郵件通知事件或重大電池警示事件。</span><span class="sxs-lookup"><span data-stu-id="c08c7-197">Windows associates certain events with sound files, for example, a New Mail Notification event or a Critical Battery Alarm event.</span></span> <span data-ttu-id="c08c7-198">事件名稱必須由使用者介面顯示，且必須支援全球化。</span><span class="sxs-lookup"><span data-stu-id="c08c7-198">The event names must be displayed by the user interface and must support globalization.</span></span> <span data-ttu-id="c08c7-199">因此，您應該針對每個事件描述的描述，執行可當地語系化的字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-199">Therefore, you should implement a localizable string resource for the description of each event description.</span></span> <span data-ttu-id="c08c7-200">針對每個事件名稱新增一個新的登錄值，以及硬式編碼的預設值。</span><span class="sxs-lookup"><span data-stu-id="c08c7-200">Add a new registry value for each event name, in addition to the hard-coded default value.</span></span>

<span data-ttu-id="c08c7-201">執行下列動作來啟用音效事件：</span><span class="sxs-lookup"><span data-stu-id="c08c7-201">Do the following to enable a sound event:</span></span>

1.  <span data-ttu-id="c08c7-202">將描述實作為可當地語系化的字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-202">Implement the description as a localizable string resource.</span></span>
2.  <span data-ttu-id="c08c7-203">除了硬式編碼的預設值外，還會為顯示名稱加入新的登錄值。</span><span class="sxs-lookup"><span data-stu-id="c08c7-203">Add a new registry value for the display name, in addition to the hard-coded default value.</span></span> <span data-ttu-id="c08c7-204">相關聯的登錄配置如下所示：</span><span class="sxs-lookup"><span data-stu-id="c08c7-204">The associated registry layout is shown below:</span></span>


```C++
HKCR\AppEvents\EventLabels
<event_name>
    (Default) REG_SZ "<description>"
    DispFileName REG_EXPAND_SZ "@<path>,-<resID>"
```



<span data-ttu-id="c08c7-205">如果 shell 找不到或無法取出 DispFileName 的值，則會使用預設描述。</span><span class="sxs-lookup"><span data-stu-id="c08c7-205">If the shell cannot find or retrieve the value of DispFileName, it uses the default description.</span></span>

## <a name="create-resources-for-keyboard-layout-strings"></a><span data-ttu-id="c08c7-206">建立鍵盤配置字串的資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-206">Create Resources for Keyboard Layout Strings</span></span>

<span data-ttu-id="c08c7-207">如果您的應用程式會執行鍵盤配置，則需要可當地語系化的字串資源作為螢幕顯示配置的名稱，例如，在鍵盤配置的清單中。</span><span class="sxs-lookup"><span data-stu-id="c08c7-207">If your application implements a keyboard layout, it requires a localizable string resource for the name of the layout for screen display, for example, in lists of keyboard layouts.</span></span> <span data-ttu-id="c08c7-208">每個鍵盤配置都有一個登錄機碼，位於 HKEY \_ LOCAL \_ MACHINE \\ System \\ CurrentControlSet \\ Control \\ 鍵盤版面配置。</span><span class="sxs-lookup"><span data-stu-id="c08c7-208">Each keyboard layout has a registry key under HKEY\_LOCAL\_MACHINE\\System\\CurrentControlSet\\Control\\Keyboard Layouts.</span></span>

<span data-ttu-id="c08c7-209">該索引鍵的值包括版面配置文字、可供回溯相容的人們看得懂的名稱，以及版面配置顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c08c7-209">Among the values for that key are Layout Text, a human-readable name for backward compatibility, and Layout Display Name.</span></span> <span data-ttu-id="c08c7-210">針對版面配置顯示名稱提供的資料應該是 "" 格式的字串參考 `@<path>,-resID` ，參考與鍵盤配置相關聯的可當地語系化字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-210">The data supplied for Layout Display Name should be a string reference of the form "`@<path>,-resID`", referring to a localizable string resource associated with the keyboard layout.</span></span>

<span data-ttu-id="c08c7-211">以下是西班牙文 (西班牙) 鍵盤配置的登錄設定範例：</span><span class="sxs-lookup"><span data-stu-id="c08c7-211">Here is an example of a registry setting for the Spanish (Spain) keyboard layout:</span></span>

`Layout Display Name=@%SystemRoot%\system32\input.dll,-5020`

## <a name="represent-ole-insert-object-common-dialog-strings"></a><span data-ttu-id="c08c7-212">代表 OLE 插入物件的通用對話方塊字串</span><span class="sxs-lookup"><span data-stu-id="c08c7-212">Represent OLE Insert Object Common Dialog Strings</span></span>

<span data-ttu-id="c08c7-213">您可以將 OLE 可插入物件的顯示名稱，作為與執行該物件之程式碼相關聯的可當地語系化字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-213">You can implement the display name of an OLE insertable object as a localizable string resource associated with the code implementing that object.</span></span> <span data-ttu-id="c08c7-214">[ [OLE 插入物件] 對話方塊](/cpp/mfc/reference/coleinsertdialog-class) 會從登錄機碼 HKCR \\ CLSID {} 取得顯示名稱 \\ *<GUID>* ，其中 *GUID* 會識別可插入的 OLE 物件的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="c08c7-214">The [OLE Insert Object dialog box](/cpp/mfc/reference/coleinsertdialog-class) gets a display name from the registry key HKCR\\CLSID\\{*<GUID>*}, where *GUID* identifies the class identifier of an insertable OLE object.</span></span> <span data-ttu-id="c08c7-215">Windows Vista 和更新版本會以可當地語系化的方式來執行這種類型的物件，並使用符合 MUI 規範的顯示名稱，以允許自訂使用者介面語言。</span><span class="sxs-lookup"><span data-stu-id="c08c7-215">Windows Vista and later implement this type of object in a localizable way, using a MUI-compliant display name that allows customization to the user interface language.</span></span> <span data-ttu-id="c08c7-216">相反地，Windows Vista 之前的作業系統會使用對應的登錄機碼的預設值來執行此類型物件的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c08c7-216">In contrast, pre-Windows Vista operating systems implement the display name for this type of object using the default value of the corresponding registry key.</span></span> <span data-ttu-id="c08c7-217">此名稱通常是英文 (美國) 名稱或系統預設 UI 語言中的名稱。</span><span class="sxs-lookup"><span data-stu-id="c08c7-217">Typically this name is either an English (United States) name or a name in the system default UI language.</span></span>

> [!Note]  
> <span data-ttu-id="c08c7-218">並非所有對應到登錄機碼子機碼的物件都是可插入的。</span><span class="sxs-lookup"><span data-stu-id="c08c7-218">Not all objects that correspond to subkeys of the registry key are insertable.</span></span>

 

<span data-ttu-id="c08c7-219">HKCR \\ CLSID \\ {} 金鑰的預設值 *<GUID>* 應該保留人們可讀取的名稱，以提供回溯相容性。</span><span class="sxs-lookup"><span data-stu-id="c08c7-219">The default value of the HKCR\\CLSID\\{*<GUID>*} key should retain a human-readable name for backward compatibility.</span></span> <span data-ttu-id="c08c7-220">不過，它也應該以 "" 格式來定義 >localizedstring 值， `@<path>,-ResID` 其中路徑會識別執行物件的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="c08c7-220">However, it should also define the LocalizedString value, in the format "`@<path>,-ResID`", where path identifies the executable file implementing the object.</span></span> <span data-ttu-id="c08c7-221">ResID 值會為顯示名稱指定可當地語系化字串的資源識別碼。</span><span class="sxs-lookup"><span data-stu-id="c08c7-221">The ResID value specifies the resource identifier of the localizable string for the display name.</span></span>

<span data-ttu-id="c08c7-222">例如，可插入媒體剪輯物件的註冊腳本包含下列幾行：</span><span class="sxs-lookup"><span data-stu-id="c08c7-222">For example, the registration script for the insertable Media Clip object includes the following lines:</span></span>


```C++
HKCR,"CLSID\%CLSID_Media_Clip%",,,"%default description%"
HKCR,"CLSID\%CLSID_Media_Clip%","LocalizedString",,"@%systemroot%\system32\mplay32.exe,-9217"
```



<span data-ttu-id="c08c7-223">第一行提供回溯相容性，方法是將簡單的文字字串放在登錄中作為預設的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="c08c7-223">The first line provides backward compatibility by placing a simple text string in the registry as a default display name.</span></span> <span data-ttu-id="c08c7-224">第二行提供 MUI 相容顯示名稱的存取權。</span><span class="sxs-lookup"><span data-stu-id="c08c7-224">The second line provides access to the MUI-compliant display name.</span></span> <span data-ttu-id="c08c7-225">指出儲存在 Mplay32.exe 中的字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="c08c7-225">It indicates the string identifier stored in Mplay32.exe.</span></span> <span data-ttu-id="c08c7-226">Mplay32.exe 中識別碼為9217的字串可以與任意數目語言的字串資源值產生關聯。</span><span class="sxs-lookup"><span data-stu-id="c08c7-226">The string with identifier 9217 in Mplay32.exe can be associated with string resource values for any number of languages.</span></span> <span data-ttu-id="c08c7-227">其英文 (美國) 名稱是「媒體剪輯」。</span><span class="sxs-lookup"><span data-stu-id="c08c7-227">Its English (United States) name is "Media Clip".</span></span>

## <a name="create-string-resources-for-microsoft-management-console-snap-ins"></a><span data-ttu-id="c08c7-228">建立 Microsoft Management Console Snap-Ins 的字串資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-228">Create String Resources for Microsoft Management Console Snap-Ins</span></span>

<span data-ttu-id="c08c7-229">您應該為您的 MUI 應用程式所使用的每個 Microsoft Management Console (MMC) 嵌入式管理單元建立可當地語系化的字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-229">You should create a localizable string resource for each Microsoft Management Console (MMC) snap-in used by your MUI application.</span></span> <span data-ttu-id="c08c7-230">因為嵌入式管理單元是主控台的一部分，所以它具有使用者介面，且必須經過全球化才能以多種語言運作。</span><span class="sxs-lookup"><span data-stu-id="c08c7-230">Because a snap-in is part of a console, it has a user interface and must be globalized to operate in more than one language.</span></span>

<span data-ttu-id="c08c7-231">大部分的情況下，MMC 嵌入式管理單元會引發與 MUI 應用程式本身相同的全球化和當地語系化問題。</span><span class="sxs-lookup"><span data-stu-id="c08c7-231">For the most part, MMC snap-ins raise the same globalization and localization issues as the MUI application itself.</span></span> <span data-ttu-id="c08c7-232">MMC 嵌入式管理單元必須反映其在登錄中的名稱以供顯示。</span><span class="sxs-lookup"><span data-stu-id="c08c7-232">An MMC snap-in must reflect its name in the registry for display.</span></span> <span data-ttu-id="c08c7-233">登錄專案應該包含可當地語系化字串資源的間接參考，以及回溯相容性的常值字串。</span><span class="sxs-lookup"><span data-stu-id="c08c7-233">The registry entry should include both an indirect reference to a localizable string resource and a literal string for backward compatibility.</span></span>

<span data-ttu-id="c08c7-234">每個 MMC 嵌入式管理單元都有一個登錄機碼，位於 HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MMC \\ 嵌入式管理單元。</span><span class="sxs-lookup"><span data-stu-id="c08c7-234">Each MMC snap-in has a registry key under HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\MMC\\SnapIns.</span></span> <span data-ttu-id="c08c7-235">該索引鍵的值會 NameString，指定可讀的名稱以提供回溯相容性，而 NameStringIndirect 則指定可當地語系化字串資源的間接參考。</span><span class="sxs-lookup"><span data-stu-id="c08c7-235">Among the values for that key are NameString, specifying a human-readable name for backward compatibility, and NameStringIndirect, specifying an indirect reference to a localizable string resource.</span></span> <span data-ttu-id="c08c7-236">針對 NameStringIndirect，您應該提供 "" 格式的字串參考 `@<path>,-resID` ，代表可當地語系化的字串資源。</span><span class="sxs-lookup"><span data-stu-id="c08c7-236">For NameStringIndirect, you should provide a string reference of the form "`@<path>,-resID`", representing a localizable string resource.</span></span>

<span data-ttu-id="c08c7-237">例如，您可能會為 Mymmc.dll 進行下列設定，其中12345是對應字串資源的識別碼，其中包含嵌入式管理單元的可當地語系化名稱：</span><span class="sxs-lookup"><span data-stu-id="c08c7-237">For example, you might make the following setting for Mymmc.dll, where 12345 is the identifier of the corresponding string resource containing the localizable name of the snap-in:</span></span>


```C++
NameStringIndirect=@%systemroot%@c:\windir\system32\mymmc.dll,-12345
```



<span data-ttu-id="c08c7-238">某些嵌入式管理單元會註冊 MMC 不會從登錄讀取的其他登錄字串值。</span><span class="sxs-lookup"><span data-stu-id="c08c7-238">Some snap-ins register other registry string values that MMC does not read from the registry.</span></span> <span data-ttu-id="c08c7-239">如需有關使用這些值的詳細資訊，請參閱註冊 Microsoft Management Console Snap-In 在 [尋找重新導向的字串](locating-redirected-strings.md)時無法從登錄讀取的字串。</span><span class="sxs-lookup"><span data-stu-id="c08c7-239">For more information about using these values, see Register Microsoft Management Console Snap-In Strings Not Read from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span>

## <a name="create-string-resources-for-a-windows-service"></a><span data-ttu-id="c08c7-240">建立 Windows 服務的字串資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-240">Create String Resources for a Windows Service</span></span>

<span data-ttu-id="c08c7-241">雖然 Windows 服務通常只有少量或沒有使用者介面，但它必須顯示符合 MUI 規範的名稱，而且通常會提供符合 MUI 規範的語言特定描述。</span><span class="sxs-lookup"><span data-stu-id="c08c7-241">Although a Windows service typically has little or no user interface, it must display a MUI-compliant name and usually provides a MUI-compliant language-specific description.</span></span> <span data-ttu-id="c08c7-242">描述 Windows 服務的登錄機碼只支援服務名稱的 DisplayName 值和服務描述的描述值。</span><span class="sxs-lookup"><span data-stu-id="c08c7-242">The registry key that describes a Windows service supports only the DisplayName value for the service name and the Description value for the service description.</span></span>

<span data-ttu-id="c08c7-243">Windows 服務的設定是從應用程式進行，如在 [尋找重新導向的字串](locating-redirected-strings.md)中從登錄設定 windows 服務的顯示名稱和描述所述。</span><span class="sxs-lookup"><span data-stu-id="c08c7-243">Settings for the Windows service are made from the application, as described in Set the Display Name and Description for a Windows Service from the Registry in [Locating Redirected Strings](locating-redirected-strings.md).</span></span> <span data-ttu-id="c08c7-244">如果您的應用程式未設定服務使用者介面的登錄值，則登錄中的值仍會設定為 [英文]，即使使用者介面是另一種語言。</span><span class="sxs-lookup"><span data-stu-id="c08c7-244">If your application does not set the registry values for the service user interface, values in the registry remain set to English, even if the user interface is in another language.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c08c7-245">相關主題</span><span class="sxs-lookup"><span data-stu-id="c08c7-245">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c08c7-246">準備資源</span><span class="sxs-lookup"><span data-stu-id="c08c7-246">Preparing Resources</span></span>](preparing-resources.md)
</dt> <dt>

[<span data-ttu-id="c08c7-247">尋找重新導向的字串</span><span class="sxs-lookup"><span data-stu-id="c08c7-247">Locating Redirected Strings</span></span>](locating-redirected-strings.md)
</dt> </dl>

 

 
