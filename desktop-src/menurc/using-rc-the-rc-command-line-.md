---
title: 使用 RC (RC 命令列)
description: 若要啟動 RC，請使用下列命令。
ms.assetid: da087e15-ecb5-4d03-b534-be872cf7d8b6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c34e24fdf7b9b648a9baf9c6db8981f05d5434ef
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103933166"
---
# <a name="using-rc-the-rc-command-line"></a><span data-ttu-id="aaa7d-103">使用 RC (RC 命令列)</span><span class="sxs-lookup"><span data-stu-id="aaa7d-103">Using RC (The RC Command Line)</span></span>

<span data-ttu-id="aaa7d-104">若要啟動 RC，請使用下列命令。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-104">To start RC, use the following command.</span></span>

<span data-ttu-id="aaa7d-105">**RC** \[*選項* \]*腳本-file*</span><span class="sxs-lookup"><span data-stu-id="aaa7d-105">**RC** \[*options*\] *script-file*</span></span>

<span data-ttu-id="aaa7d-106">*腳本* 檔案參數會指定資源定義檔的名稱，其中包含要編譯之資源的名稱、類型、檔案名和描述。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-106">The *script-file* parameter specifies the name of the resource-definition file that contains the names, types, filenames, and descriptions of the resources to be compiled.</span></span>

<span data-ttu-id="aaa7d-107">RC 可以針對同時具有非語言相關和語言專屬資源的應用程式，產生個別的資源檔。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-107">RC can generate separate resource files for applications that have both language-neutral and language-specific resources.</span></span> <span data-ttu-id="aaa7d-108">開發人員可以使用 [資源設定檔](/windows/desktop/Intl/preparing-resources) 案或設定命令列選項，來選取哪些資源類型和專案是非當地語系化的 [語言 (LN) ](/windows/desktop/Intl/mui-resource-management) 檔案的不可當地語系化資源，以及哪些是特定語言的 MUI 檔案的可當地語系化資源。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-108">Developers can use a [resource configuration file](/windows/desktop/Intl/preparing-resources) or set command-line options to select which resource types and items are non-localizable resources of the [language-neutral (LN) file](/windows/desktop/Intl/mui-resource-management) and which are localizable resources of language-specific MUI files.</span></span> <span data-ttu-id="aaa7d-109">如需詳細資訊，請參閱 [多語系消費者介面](/windows/desktop/Intl/multilingual-user-interface)。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-109">For more information, see the [Multilingual User Interface](/windows/desktop/Intl/multilingual-user-interface).</span></span>

<span data-ttu-id="aaa7d-110">*Options* 參數可以是下列一或多個命令列選項。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-110">The *options* parameter can be one or more of the following command-line options.</span></span>

## <a name="options"></a><span data-ttu-id="aaa7d-111">選項</span><span class="sxs-lookup"><span data-stu-id="aaa7d-111">Options</span></span>

<dl> <dt>

<span data-ttu-id="aaa7d-112"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="aaa7d-112"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-113">顯示命令列選項的清單。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-113">Displays a list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-114"><span id="_c"></span><span id="_C"></span>**/c**</span><span class="sxs-lookup"><span data-stu-id="aaa7d-114"><span id="_c"></span><span id="_C"></span>**/c**</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-115">定義 NLS 轉換所使用的字碼頁。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-115">Defines a code page used by NLS conversion.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-116"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="aaa7d-116"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-117">定義預處理器的符號，您可以使用 [**\# ifdef**](-ifdef.md)指示詞進行測試。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-117">Defines a symbol for the preprocessor that you can test with the [**\#ifdef**](-ifdef.md) directive.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*</span><span class="sxs-lookup"><span data-stu-id="aaa7d-118"><span id="_fm_mresname"></span><span id="_FM_MRESNAME"></span>**/fm** *mresname*</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-119">RC 會建立一個語言中立的。RES 檔案和與語言相依 (MUI) 。使用 *指令檔的* RES 檔案。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-119">RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file using *script-file*.</span></span> <span data-ttu-id="aaa7d-120">此選項必須與 **/fo** *resname* 選項一起使用。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-120">This option must be used together with the **/fo** *resname* option.</span></span> <span data-ttu-id="aaa7d-121">RC 會以非語言相關的名稱來命名。RES file *resname* 和 language 相依 (MUI) 的名稱。RES file *mresname .res*。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-121">RC names the language-neutral .RES file *resname.res* and names the language-dependent (MUI) .RES file *mresname.res*.</span></span>

<span data-ttu-id="aaa7d-122">**Windows Server 2003 和 WINDOWS XP/2000：** 此選項無法使用，也不會在更新的系統上使用 [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) 函數。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-122">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*</span><span class="sxs-lookup"><span data-stu-id="aaa7d-123"><span id="_fo_resname"></span><span id="_FO_RESNAME"></span>**/fo** *resname*</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-124">RC 會建立。使用腳本檔案名稱為 *resname* *的* RES 檔案。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-124">RC creates a .RES file named *resname* using *script-file*.</span></span>

<span data-ttu-id="aaa7d-125">如果同時設定了 **/fm** *MRESNAME* 選項，RC 就會建立一個非語言相關。RES 檔案和與語言相依 (MUI) 。RES 檔。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-125">If the **/fm** *mresname* option is also set, RC creates one language-neutral .RES file and one language-dependent (MUI) .RES file.</span></span>

<span data-ttu-id="aaa7d-126">**Windows Server 2003 和 WINDOWS XP/2000：** 此選項無法使用，也不會在更新的系統上使用 [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) 函數。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-126">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-127"><span id="_g1"></span><span id="_G1"></span>**/g1**</span><span class="sxs-lookup"><span data-stu-id="aaa7d-127"><span id="_g1"></span><span id="_G1"></span>**/g1**</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-128">如果設定了/g1，則當 MUI 檔案中唯一包含的可當地語系化資源是版本資源時，RC 會產生 MUI 檔案。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-128">If /g1, is set, RC generates a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span> <span data-ttu-id="aaa7d-129">如果未設定/g1，則如果 MUI 檔中唯一包含的可當地語系化資源是版本資源，RC 將不會產生 MUI 檔案。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-129">If /g1 is not set, RC will not generate a MUI file if the only localizable resource being included in the MUI file is a version resource.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-130"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="aaa7d-130"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-131">顯示命令列選項的清單。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-131">Displays the list of command-line options.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-132"><span id="_I"></span><span id="_i"></span>**/I**</span><span class="sxs-lookup"><span data-stu-id="aaa7d-132"><span id="_I"></span><span id="_i"></span>**/I**</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-133">搜尋指定的目錄，然後搜尋 INCLUDE 環境變數所指定的目錄。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-133">Searches the specified directory before searching the directories specified by the INCLUDE environment variable.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*</span><span class="sxs-lookup"><span data-stu-id="aaa7d-134"><span id="_j__loctype"></span><span id="_J__LOCTYPE"></span>**/j** *loctype*</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-135">可當地語系化的資源類型 RC 會放入與語言相依的 (MUI) 。RES 檔。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-135">Localizable resource types RC places into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="aaa7d-136">如果 **/q** 選項也已設定，則會忽略此選項，且 RC 設定檔中的資訊會優先。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-136">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="aaa7d-137">**Windows Server 2003 和 WINDOWS XP/2000：** 此選項無法使用，也不會在更新的系統上使用 [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) 函數。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-137">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** 的 *改寫*</span><span class="sxs-lookup"><span data-stu-id="aaa7d-138"><span id="_k_overtype"></span><span id="_K_OVERTYPE"></span>**/k** *overtype*</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-139">RC 同時放入非語言相關的重迭資源類型。RES 和與語言相依的 (MUI) 。RES 檔。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-139">Overlapping resource types that RC places into both the language-neutral .RES and the language-dependent (MUI).RES files.</span></span> <span data-ttu-id="aaa7d-140">**/K** 選項所指定的資源類型必須是 **/j** 選項所指定的子集。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-140">The resource types that are specified by the **/k** option must be a subset of those that are specified by the **/j** option.</span></span> <span data-ttu-id="aaa7d-141">例如，？J2?J3 接?K3 指定 RC 會在語言中性和語言相依 (MUI) 檔中放置資源類型3。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-141">For example, ?J2 ?J3 ?K3 specifies that RC places resource type 3 in both the language-neutral and language-dependent (MUI) files.</span></span> <span data-ttu-id="aaa7d-142">如果 **/q** 選項也已設定，則會忽略此選項，且 RC 設定檔中的資訊會優先。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-142">If the **/q** option is also set, this option is ignored, and the information in the RC Configuration file takes precedence.</span></span>

<span data-ttu-id="aaa7d-143">**Windows Server 2003 和 WINDOWS XP/2000：** 此選項無法使用，也不會在更新的系統上使用 [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) 函數。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-143">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*</span><span class="sxs-lookup"><span data-stu-id="aaa7d-144"><span id="_l_langid"></span><span id="_L_LANGID"></span>**/l** *langid*</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-145">指定編譯的預設語言。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-145">Specifies the default language for compilation.</span></span> <span data-ttu-id="aaa7d-146">例如，-l409 相當於在資源腳本檔案的頂端包含下列語句： `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span><span class="sxs-lookup"><span data-stu-id="aaa7d-146">For example, -l409 is equivalent to including the following statement at the top of the resource script file: `LANGUAGE LANG_ENGLISH,SUBLANG_ENGLISH_US`</span></span>

<span data-ttu-id="aaa7d-147">如需詳細資訊，請參閱 [語言識別項](/windows/desktop/Intl/language-identifiers)。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-147">For more information, see [Language Identifiers](/windows/desktop/Intl/language-identifiers).</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-148"><span id="_n"></span><span id="_N"></span>**n**</span><span class="sxs-lookup"><span data-stu-id="aaa7d-148"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-149">Null 會終止字串資料表中的所有字串。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-149">Null terminates all strings in the string table.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/Q** *Mui. RCConfig*</span><span class="sxs-lookup"><span data-stu-id="aaa7d-150"><span id="_q_Mui.RCConfig"></span><span id="_q_mui.rcconfig"></span><span id="_Q_MUI.RCCONFIG"></span>**/q** *Mui.RCConfig*</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-151">遵循 RC 設定檔案格式的 RC 設定檔案。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-151">An RC configuration file that follows the RC Configuration File format.</span></span> <span data-ttu-id="aaa7d-152">RC 設定檔案格式可讓元件自行描述資源的資訊，例如資源版本控制、MUI 檔案路徑、資源類型和專案。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-152">The RC Configuration File format enables components to self-describe resource information such as resource versioning, MUI file path, resource types and items.</span></span> <span data-ttu-id="aaa7d-153">此檔案會指定哪些資源要進入非語言相關。RES 檔案，以及哪些資源會進入與語言相依的 (MUI) 。RES 檔。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-153">This file specifies which resources go into the language-neutral .RES file and which resources go into the language-dependent (MUI) .RES file.</span></span> <span data-ttu-id="aaa7d-154">此選項以及 RC 設定檔中提供的資訊，會覆寫命令列選項 **/j** 和 **/k**。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-154">This option, and the information provided in the RC Configuration file, override the command line options **/j** and **/k**.</span></span>

<span data-ttu-id="aaa7d-155">**Windows Server 2003 和 WINDOWS XP/2000：** 此選項無法使用，也不會在更新的系統上使用 [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) 和 [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) 函數。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-155">**Windows Server 2003 and Windows XP/2000:** This option is not available without also using the [**LoadMUILibrary**](/windows/desktop/api/muiload/nf-muiload-loadmuilibrarya) and [**FreeMUILibrary**](/windows/desktop/api/muiload/nf-muiload-freemuilibrary) functions on an updated system.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-156"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="aaa7d-156"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-157">忽略。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-157">Ignored.</span></span> <span data-ttu-id="aaa7d-158">為了與現有的 makefile 相容而提供。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-158">Provided for compatibility with existing makefiles.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-159"><span id="_u"></span><span id="_U"></span>**u**</span><span class="sxs-lookup"><span data-stu-id="aaa7d-159"><span id="_u"></span><span id="_U"></span>**/u**</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-160">取消預處理器的符號。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-160">Undefines a symbol for the preprocessor.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-161"><span id="_v"></span><span id="_V"></span>**/v**</span><span class="sxs-lookup"><span data-stu-id="aaa7d-161"><span id="_v"></span><span id="_V"></span>**/v**</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-162">顯示報告編譯器進度的訊息。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-162">Displays messages that report on the progress of the compiler.</span></span>

</dd> <dt>

<span data-ttu-id="aaa7d-163"><span id="_x"></span><span id="_X"></span>**/x**</span><span class="sxs-lookup"><span data-stu-id="aaa7d-163"><span id="_x"></span><span id="_X"></span>**/x**</span></span>
</dt> <dd>

<span data-ttu-id="aaa7d-164">在搜尋標頭檔或資源檔時，防止 RC 檢查 INCLUDE 環境變數。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-164">Prevents RC from checking the INCLUDE environment variable when searching for header files or resource files.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aaa7d-165">備註</span><span class="sxs-lookup"><span data-stu-id="aaa7d-165">Remarks</span></span>

<span data-ttu-id="aaa7d-166">選項不區分大小寫，且 ( ) 的連字號可以用來取代 (/) 的斜線符號。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-166">Options are not case sensitive, and a hyphen (-) can be used in place of a slash mark (/).</span></span> <span data-ttu-id="aaa7d-167">如果不需要任何額外的參數，您可以結合單字母選項。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-167">You can combine single-letter options if they do not require any additional parameters.</span></span>

<span data-ttu-id="aaa7d-168">RC 不會在下列情況下產生 MUI 檔案。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-168">RC will not generate a MUI file in the following cases.</span></span>

-   <span data-ttu-id="aaa7d-169">.Rc 檔中沒有可當地語系化的資源存在。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-169">No localizable resources exist in the .rc file.</span></span>
-   <span data-ttu-id="aaa7d-170">.Rc 檔中唯一指定的資源語言識別項是中性 (0x0) 。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-170">The only resource language id specified in the .rc file is neutral (0x0).</span></span>
-   <span data-ttu-id="aaa7d-171">.Rc 檔中的資源會以一種以上的語言指定。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-171">The .rc file has resources that are specified in more than one language.</span></span> <span data-ttu-id="aaa7d-172">例外狀況是，如果 .rc 檔包含兩種語言，而其中一種語言為中性 (0x0) ，RC 會產生 MUI 檔案。</span><span class="sxs-lookup"><span data-stu-id="aaa7d-172">The exception is if the .rc file contains two languages, and one language is neutral (0x0), RC generates a MUI file.</span></span>

<span data-ttu-id="aaa7d-173">如需詳細資訊，請參閱下列主題：</span><span class="sxs-lookup"><span data-stu-id="aaa7d-173">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="aaa7d-174">定義預處理器的名稱</span><span class="sxs-lookup"><span data-stu-id="aaa7d-174">Defining Names for the Preprocessor</span></span>](defining-names-for-the-preprocessor.md)
-   [<span data-ttu-id="aaa7d-175">重新命名已編譯的資源檔</span><span class="sxs-lookup"><span data-stu-id="aaa7d-175">Renaming the Compiled Resource File</span></span>](renaming-the-compiled-resource-file.md)
-   [<span data-ttu-id="aaa7d-176">搜尋檔案</span><span class="sxs-lookup"><span data-stu-id="aaa7d-176">Searching for Files</span></span>](searching-for-files.md)
-   [<span data-ttu-id="aaa7d-177">顯示進度訊息</span><span class="sxs-lookup"><span data-stu-id="aaa7d-177">Displaying Progress Messages</span></span>](displaying-progress-messages.md)
-   [<span data-ttu-id="aaa7d-178">RC 診斷訊息</span><span class="sxs-lookup"><span data-stu-id="aaa7d-178">RC Diagnostic Messages</span></span>](rc-diagnostic-messages.md)

## <a name="related-topics"></a><span data-ttu-id="aaa7d-179">相關主題</span><span class="sxs-lookup"><span data-stu-id="aaa7d-179">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aaa7d-180">多語系使用者介面</span><span class="sxs-lookup"><span data-stu-id="aaa7d-180">Multilingual User Interface</span></span>](/windows/desktop/Intl/multilingual-user-interface)
</dt> </dl>

 

 