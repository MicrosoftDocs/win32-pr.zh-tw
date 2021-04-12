---
description: 受控物件格式 (MOF) 編譯器會剖析包含 MOF 語句的檔案，並將檔案中定義的類別和類別實例新增至 WMI 存放庫。
ms.assetid: 9858da09-fb91-43a4-9817-83b10e2ee08f
ms.tgt_platform: multiple
title: mofcomp.exe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: da63525e4bb8a32f3628b68295e5cc8ade0b08de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848394"
---
# <a name="mofcomp"></a><span data-ttu-id="3c0a3-103">mofcomp.exe</span><span class="sxs-lookup"><span data-stu-id="3c0a3-103">mofcomp</span></span>

<span data-ttu-id="3c0a3-104">[*受控物件格式 (mof)*](gloss-m.md)編譯器會剖析包含 MOF 語句的檔案，並將檔案中定義的類別和類別實例新增至 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-104">The [*Managed Object Format (MOF)*](gloss-m.md) compiler parses a file containing MOF statements and adds the classes and class instances defined in the file to the WMI repository.</span></span> <span data-ttu-id="3c0a3-105">MOF 檔案通常會在安裝時自動編譯，但您也可以使用此工具來編譯 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-105">MOF files are usually automatically compiled during the installation of the systems with which they are provided, but you can also compile MOF files by using this tool.</span></span>

<span data-ttu-id="3c0a3-106">如需尋找和使用 mofcomp.exe 的詳細資訊，請參閱 [使用 WMI 管理工具](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-106">For more information about locating and using mofcomp.exe, see [Using WMI Management Tools](/previous-versions/system-center/configuration-manager-2003/cc180468(v=technet.10)).</span></span> <span data-ttu-id="3c0a3-107">如需從 WMI 儲存機制移除類別和實例的詳細資訊，請參閱 [**pragma deleteclass**](pragma-deleteclass.md) 預處理器命令。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-107">For information about removing classes and instances from the WMI repository, see the [**pragma deleteclass**](pragma-deleteclass.md) preprocessor command.</span></span>

<span data-ttu-id="3c0a3-108">下列程式碼範例顯示如何在檔案上執行 MOF 編譯器。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-108">The following code example shows how to run the MOF compiler on a file.</span></span>

``` syntax
mofcomp
  [-autorecover]
  [-check]
  [-N:<namespacepath>]
  [-class:createonly | -class:forceupdate | 
   -class:safeupdate | -class:updateonly ] 
  [-instance:updateonly | -instance:createonly]
  [-B:<filename>]
  [-WMI]
  [-P:<Password>]
  [-U:<UserName>]
  [-A:<Authority>]
  [-MOF:<path>] 
  [-MFL:<path>] 
  [-AMENDMENT:<Locale>]
  [-ER:<ResourceName>]
  [-L:<ResourceLocale>] 
  <MOFfile>
```

## <a name="switches"></a><span data-ttu-id="3c0a3-109">交換器</span><span class="sxs-lookup"><span data-stu-id="3c0a3-109">Switches</span></span>

<dl> <dt>

<span data-ttu-id="3c0a3-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-自動回復**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-110"><span id="-autorecover"></span><span id="-AUTORECOVER"></span>**-autorecover**</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-111">將命名的 MOF 檔案新增至儲存機制復原期間所編譯的檔案清單。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-111">Adds the named MOF file to the list of files compiled during repository recovery.</span></span> <span data-ttu-id="3c0a3-112">自動回復 MOF 檔案的清單儲存在登錄機碼中：</span><span class="sxs-lookup"><span data-stu-id="3c0a3-112">The list of autorecover MOF files is stored in the registry key:</span></span>

<span data-ttu-id="3c0a3-113">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **WBEM** \\ **CIMOM \\**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-113">**HKEY\_LOCAL\_MACHINE**\\**SOFTWARE**\\**Microsoft**\\**WBEM**\\**CIMOM\\**</span></span>

<span data-ttu-id="3c0a3-114">此登錄專案中列出的 MOF 檔案必須位於本機電腦上，因為使用 [ **自動** 復原] 命令的 mof 檔案無法復原位於遠端電腦上的 mof 檔案。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-114">The MOF files listed in this registry entry must reside on the local computer because MOF files that use the **autorecover** command cannot recover MOF files located on a remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="3c0a3-115">若要確保在 WMI 失敗並重新啟動時，managed 物件的所有 WMI 類別定義都會還原至 [*wmi 儲存*](gloss-w.md)機制，請使用 [*受控物件格式*](gloss-m.md) (MOF) 檔中的 [**\# pragma 自動**](pragma-autorecover.md)復原預處理器指令。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-115">To ensure that all your WMI class definitions for managed objects are restored to the [*WMI repository*](gloss-w.md) if WMI has a failure and restarts, use the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor instruction in your [*Managed Object Format*](gloss-m.md) (MOF) file.</span></span>

 

</dd> <dt>

<span data-ttu-id="3c0a3-116"><span id="-check"></span><span id="-CHECK"></span>**-檢查**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-116"><span id="-check"></span><span id="-CHECK"></span>**-check**</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-117">要求編譯器只執行語法檢查並列印適當的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-117">Requests that the compiler perform a syntax check only and print appropriate error messages.</span></span> <span data-ttu-id="3c0a3-118">此參數不能使用其他參數。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-118">No other switch can be used with this switch.</span></span> <span data-ttu-id="3c0a3-119">使用此參數時，不會建立 Windows Management Instrumentation (WMI) 的連線，也不會對 WMI 存放庫進行任何修改。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-119">When this switch is used, no connection to Windows Management Instrumentation (WMI) is established and no modifications to the WMI repository are made.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N： <** _namespacepath_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3c0a3-120"><span id="-N__namespacepath_"></span><span id="-n__namespacepath_"></span><span id="-N__NAMESPACEPATH_"></span>**-N:<**_namespacepath_*_>_*</span></span>
</dt> <dd><span data-ttu-id="3c0a3-121">要求編譯器將 MOF 檔案載入至指定為 *namespacepath* 的命名空間。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-121">Requests that the compiler load the MOF file into the namespace specified as *namespacepath*.</span></span> <span data-ttu-id="3c0a3-122">除非使用此參數，否則已編譯的 MOF 會載入預設的 Mofcomp.exe 命名空間（根 \\ 預設值）。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-122">The compiled MOF is loaded into the default Mofcomp namespace, root\\default, unless this switch is used.</span></span> <span data-ttu-id="3c0a3-123">您也可以將預處理器命令 **\# pragma 命名空間 (**「_命名空間路徑_」*_)_* 在 MOF 檔案中，以達到相同的效果。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-123">You can also insert the preprocessor command **\#pragma namespace ("**_namespace path_*_")_* in the MOF file to achieve the same effect.</span></span> <span data-ttu-id="3c0a3-124">如果同時使用 **-N：** switch 和 \# <a href="pragma-namespace.md">pragma namespace</a>命令，則會優先使用 \# **pragma namespace** **自動** 回復。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-124">If both the **-N:** switch and the \#<a href="pragma-namespace.md">pragma namespace</a> command are used, \#**pragma namespace** **autorecover** takes priority.</span></span> <span data-ttu-id="3c0a3-125">在此情況下，將 MOF 編譯成另一個命名空間的唯一方法，是編輯 MOF 檔案並變更 \# **pragma namespace** 命令。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-125">In this case, the only way to compile the MOF into another namespace is to edit the MOF file and change the \#**pragma namespace** command.</span></span> <span data-ttu-id="3c0a3-126">您可以使用 \\ \\ machinename \\ 根 \\ 預設值來指定遠端電腦。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-126">A remote computer can be specified using \\\\machinename\\root\\default.</span></span></dd> <dt>

<span data-ttu-id="3c0a3-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-class：以**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-127"><span id="-class_createonly"></span><span id="-CLASS_CREATEONLY"></span>**-class:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-128">要求編譯器不會對現有的類別進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-128">Requests that the compiler not make any changes to existing classes.</span></span> <span data-ttu-id="3c0a3-129">使用這個參數時，如果 MOF 檔案中指定的類別已存在，編譯作業就會終止。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-129">When this switch is used, the compile operation terminates if a class specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-class： forceupdate**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-130"><span id="-class_forceupdate"></span><span id="-CLASS_FORCEUPDATE"></span>**-class:forceupdate**</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-131">存在衝突的子類別時，強制更新類別。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-131">Forces updates of classes when conflicting child classes exist.</span></span> <span data-ttu-id="3c0a3-132">例如，假設類別限定詞是在子類別中定義，而且基類嘗試加入相同的辨識符號。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-132">For example, suppose a class qualifier is defined in a child class and the base class tries to add the same qualifier.</span></span> <span data-ttu-id="3c0a3-133">在 **類別中： forceupdate** 模式，MOF 編譯器會藉由刪除子類別中的衝突辨識符號來解決這項衝突。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-133">In **-class:forceupdate** mode, the MOF compiler resolves this conflict by deleting the conflicting qualifier in the child class.</span></span> <span data-ttu-id="3c0a3-134">如果子類別具有實例，強制更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-134">If the child class has instances, the forced update fails.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-class： safeupdate**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-135"><span id="-class_safeupdate"></span><span id="-CLASS_SAFEUPDATE"></span>**-class:safeupdate**</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-136">即使有子類別，也允許更新類別，只要變更不會造成與子類別的衝突。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-136">Allows updates of classes even if there are child classes, as long as the change does not cause conflicts with child classes.</span></span> <span data-ttu-id="3c0a3-137">例如，這個旗標可讓您將新的屬性加入至先前未在子類別中提及的基類。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-137">For example, this flag allows adding a new property to the base class that was not previously mentioned in child classes.</span></span> <span data-ttu-id="3c0a3-138">如果子類別具有實例，則更新會失敗。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-138">If the child classes have instances, the update fails.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-class： updateonly**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-139"><span id="-class_updateonly"></span><span id="-CLASS_UPDATEONLY"></span>**-class:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-140">要求編譯器不會建立任何新的類別。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-140">Requests that the compiler not create any new classes.</span></span> <span data-ttu-id="3c0a3-141">使用這個參數時，如果 MOF 檔案中指定的類別不存在，編譯作業就會終止。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-141">When this switch is used, the compile operation terminates if a class specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance： updateonly**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-142"><span id="-instance_updateonly"></span><span id="-INSTANCE_UPDATEONLY"></span>**-instance:updateonly**</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-143">要求編譯器不會建立任何新的實例。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-143">Requests that the compiler not create any new instances.</span></span> <span data-ttu-id="3c0a3-144">使用這個參數時，如果 MOF 檔案中指定的實例不存在，編譯作業就會終止。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-144">When this switch is used, the compile operation terminates if an instance specified in the MOF file does not exist.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance：以**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-145"><span id="-instance_createonly"></span><span id="-INSTANCE_CREATEONLY"></span>**-instance:createonly**</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-146">要求編譯器不會對現有的實例進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-146">Requests that the compiler not make any changes to existing instances.</span></span> <span data-ttu-id="3c0a3-147">使用這個參數時，如果 MOF 檔案中指定的實例已經存在，編譯作業就會終止。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-147">When this switch is used, the compile operation terminates if an instance specified in the MOF file already exists.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B： <** _filename_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3c0a3-148"><span id="-B__filename_"></span><span id="-b__filename_"></span><span id="-B__FILENAME_"></span>**-B:<**_filename_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-149">要求編譯器建立具有名稱 *檔案名* 的二進位版本 MOF 檔案，而不需要對 WMI 儲存機制進行任何修改。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-149">Requests that the compiler create a binary version of the MOF file with the name *filename* without making any modifications to the WMI repository.</span></span>

<span data-ttu-id="3c0a3-150">如果您使用 **-B： <** _filename_ *_>_* 選項來建立二進位 MOF 檔案，則只有預設的限定詞類別會儲存在 WMI 存放庫中。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-150">If you use the **-B:<**_filename_*_>_* option to create a binary MOF file, only default qualifier flavors are stored in the WMI repository.</span></span>

<span data-ttu-id="3c0a3-151">二元 MOF 格式是將 WDM 驅動程式與 MOF 結合為資源的中繼格式。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-151">Binary MOF format is the intermediate format for combining a WDM-driver with the MOF as a resource.</span></span> <span data-ttu-id="3c0a3-152">二元 MOF 代表類別和實例，就像是文字 MOF 檔案一樣，並且會在儲存于磁片之前壓縮。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-152">The binary MOF represents classes and instances just as a text MOF file does and is compressed before it is stored on disk.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-153"><span id="-WMI"></span><span id="-wmi"></span>**-WMI**</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-154">要求編譯器執行 WMI 語法檢查。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-154">Requests that the compiler perform a WMI syntax check.</span></span> <span data-ttu-id="3c0a3-155">必須搭配此參數使用 **-B：** switch。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-155">The **-B:** switch must be used with this switch.</span></span> <span data-ttu-id="3c0a3-156">**-WMI** 參數僅用來建立可供 WDM 設備磁碟機使用的二進位 MOF 檔案。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-156">The **-WMI** switch is only used for building binary MOF files for use by WDM device drivers.</span></span> <span data-ttu-id="3c0a3-157">此參數會叫用個別的二進位 MOF 檔案檢查程式，並在建立二元 MOF 檔案之後執行。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-157">This switch invokes a separate binary MOF file checker, which runs after the binary MOF file is created.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P： <**_密碼_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3c0a3-158"><span id="-P__Password_"></span><span id="-p__password_"></span><span id="-P__PASSWORD_"></span>**-P:<**_Password_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-159">指定 *密碼* 做為登入時電腦使用者輸入的密碼。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-159">Specifies *Password* as the password for the computer user to enter when logging on.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U： <** 使用者 _名稱_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3c0a3-160"><span id="-U__UserName_"></span><span id="-u__username_"></span><span id="-U__USERNAME_"></span>**-U:<**_UserName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-161">指定 *使用者* 名稱做為登入使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-161">Specifies *UserName* as the name of the user logging on.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A： <**_授權_ 單位 *_>_*</span><span class="sxs-lookup"><span data-stu-id="3c0a3-162"><span id="-A__Authority_"></span><span id="-a__authority_"></span><span id="-A__AUTHORITY_"></span>**-A:<**_Authority_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-163">將 *授權* 單位指定為登入 WMI 時所要使用 (功能變數名稱) 的授權單位。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-163">Specifies *Authority* as the authority (domain name) to use when logging on to WMI.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF： <**_路徑_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3c0a3-164"><span id="-MOF__path_"></span><span id="-mof__path_"></span><span id="-MOF__PATH_"></span>**-MOF:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-165">非語言相關輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-165">Name of the language neutral output.</span></span> <span data-ttu-id="3c0a3-166">搭配 **-修訂** 參數使用，以指定將產生的語言中性 MOF 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-166">Used with the **-AMENDMENT** switch to specify the name of the language-neutral MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL： <**_路徑_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3c0a3-167"><span id="-MFL__path_"></span><span id="-mfl__path_"></span><span id="-MFL__PATH_"></span>**-MFL:<**_path_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-168">特定語言輸出的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-168">Name of the language specific output.</span></span> <span data-ttu-id="3c0a3-169">與 **-修訂** 參數搭配使用，以指定將產生的語言特定 MOF 檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-169">Used with the **-AMENDMENT** switch to specify the name of the language-specific MOF file that will be generated.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-修訂： <**_地區_ 設定 *_>_*</span><span class="sxs-lookup"><span data-stu-id="3c0a3-170"><span id="-AMENDMENT__Locale_"></span><span id="-amendment__locale_"></span><span id="-AMENDMENT__LOCALE_"></span>**-AMENDMENT:<**_Locale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-171">將 MOF 檔案分割成非語言相關和特定版本。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-171">Splits the MOF file into language-neutral and -specific versions.</span></span> <span data-ttu-id="3c0a3-172">MOF 編譯器會建立 MOF 檔案的語言中性形式，其中已移除所有修改過的限定詞。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-172">The MOF compiler creates a language-neutral form of the MOF file that has all amended qualifiers removed.</span></span> <span data-ttu-id="3c0a3-173">您也可以使用 MFL 副檔名來建立 MOF 檔案的當地語系化版本。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-173">A localized version of the MOF file is also created with an MFL file name extension.</span></span> <span data-ttu-id="3c0a3-174">*Locale* 參數會指定子命名空間的名稱，其中包含當地語系化的類別定義。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-174">The *Locale* parameter specifies the name of the child namespace that contains the localized class definitions.</span></span> <span data-ttu-id="3c0a3-175">*地區* 設定參數的格式為 MS \_ xxx，其中 XXX 是 Windows LCID 的十六進位值。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-175">The format of the *Locale* parameter is MS\_xxx where xxx is the hexadecimal value of the Windows LCID.</span></span> <span data-ttu-id="3c0a3-176">例如，美式英文的地區設定為 MS \_ 409。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-176">For example, the locale for American English is MS\_409.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <的** _coNtext.resourcename_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3c0a3-177"><span id="-ER__ResourceName_"></span><span id="-er__resourcename_"></span><span id="-ER__RESOURCENAME_"></span>**-ER <**_ResourceName_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-178">從命名資源中解壓縮二進位 MOF。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-178">Extracts binary MOF from a named resource.</span></span> <span data-ttu-id="3c0a3-179">此參數會從 WMI 存放庫中的類別取得二進位 MOF，而-B 參數會從 MOF 檔案建立二進位 MOF 格式。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-179">This switch gets the binary MOF from the class in the WMI repository while the -B switch creates the binary MOF format from a MOF file.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L： <** _ResourceLocale_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3c0a3-180"><span id="-L__ResourceLocale_"></span><span id="-l__resourcelocale_"></span><span id="-L__RESOURCELOCALE_"></span>**-L:<**_ResourceLocale_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-181">選擇性。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-181">Optional.</span></span> <span data-ttu-id="3c0a3-182">搭配-ER 參數使用時，從二進位 MOF 中解壓縮當地語系化的 MOF 描述。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-182">Extracts the localized MOF descriptions from the binary MOF when used with -ER switch.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3c0a3-183"><span id="_MOFfile_"></span><span id="_moffile_"></span><span id="_MOFFILE_"></span>**<**_MOFfile_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-184">要剖析的檔案名。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-184">Name of the file to parse.</span></span>

</dd> </dl>

## <a name="return-values"></a><span data-ttu-id="3c0a3-185">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c0a3-185">Return Values</span></span>

<span data-ttu-id="3c0a3-186">MOF 編譯器做為第一次作業時，會對 MOF 檔案執行語法檢查。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-186">As its first operation, the MOF compiler performs a syntax check on the MOF file.</span></span> <span data-ttu-id="3c0a3-187">如果編譯器發現任何錯誤，則會列印錯誤訊息，且進程會終止。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-187">If the compiler finds any errors, it prints an error message and the process terminates.</span></span>

<span data-ttu-id="3c0a3-188">MOF 編譯器可能會傳回下列值：</span><span class="sxs-lookup"><span data-stu-id="3c0a3-188">The MOF compiler can return the following values:</span></span>

<dl> <dt>

<span data-ttu-id="3c0a3-189"><span id="0"></span>0</span><span class="sxs-lookup"><span data-stu-id="3c0a3-189"><span id="0"></span>0</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-190">MOF 編譯操作成功。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-190">MOF compile operation was successful.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-191"><span id="1"></span>1</span><span class="sxs-lookup"><span data-stu-id="3c0a3-191"><span id="1"></span>1</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-192">MOF 編譯器無法與 WMI 伺服器連接。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-192">The MOF compiler could not connect with the WMI server.</span></span> <span data-ttu-id="3c0a3-193">這可能是因為有語意錯誤，例如與現有 WMI 存放庫不相容，或實際的錯誤，例如 WMI 伺服器無法啟動。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-193">This is either because of a semantic error such as an incompatibility with the existing WMI repository or an actual error such as the failure of the WMI server to start.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-194"><span id="2"></span>2</span><span class="sxs-lookup"><span data-stu-id="3c0a3-194"><span id="2"></span>2</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-195">一或多個命令列參數無效。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-195">One or more command-line switches were not valid.</span></span>

</dd> <dt>

<span data-ttu-id="3c0a3-196"><span id="3"></span>3</span><span class="sxs-lookup"><span data-stu-id="3c0a3-196"><span id="3"></span>3</span></span>
</dt> <dd>

<span data-ttu-id="3c0a3-197">發生 MOF 語法錯誤。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-197">A MOF syntax error occurred.</span></span>

</dd> </dl>

<span data-ttu-id="3c0a3-198">如果 MOF 檔案已正確剖析，但嘗試執行命令列參數所禁止的作業，則編譯器會傳回 WMI 產生的錯誤碼，而不是上述清單中所列的任何傳回碼。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-198">If the MOF file is parsed correctly, but an attempt is made to perform an operation that is forbidden by a command-line switch, the compiler returns an error code generated by WMI instead of any of the return codes listed in the list preceding.</span></span> <span data-ttu-id="3c0a3-199">例如，當指定 **-instance： updateonly** 參數，且 MOF 檔案嘗試建立實例時，會傳回 WMI 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-199">For example, a WMI error code is returned when the **-instance:updateonly** switch is specified and the MOF file attempts to create an instance.</span></span>

<span data-ttu-id="3c0a3-200">如果 [**\# pragma 自動**](pragma-autorecover.md)回復預處理器語句不在檔案中，則會傳回下列警告：</span><span class="sxs-lookup"><span data-stu-id="3c0a3-200">If the [**\#pragma autorecover**](pragma-autorecover.md) preprocessor statement is not in the file, then the following warning is returned:</span></span>

``` syntax
WARNING: FileYourMof.Mof does not contain #PRAGMA AUTORECOVER.
If the WMI repository is rebuilt in the future, the contents of this 
MOF file   will not be included in the new WMI repository.
To include this MOF file when the WMI Repository is automatically 
reconstructed, place the #PRAGMA AUTORECOVER statement on the first 
line of the MOF file.
```

## <a name="remarks"></a><span data-ttu-id="3c0a3-201">備註</span><span class="sxs-lookup"><span data-stu-id="3c0a3-201">Remarks</span></span>

<span data-ttu-id="3c0a3-202">MOF 編譯器可在% Windir% \\ System32 \\ wbem 目錄中取得。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-202">The MOF Compiler is available in the %Windir%\\System32\\wbem directory.</span></span> <span data-ttu-id="3c0a3-203">您必須將 MOF 檔案指定為 MOF 編譯器的參數。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-203">You must specify the MOF file as the parameter of the MOF Compiler.</span></span> <span data-ttu-id="3c0a3-204">如果您想要自動重新編譯 MOF 檔案（如果必須自動復原 CIM 存放庫），您也可以指定自動重設開關。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-204">You can also specify an Autorecover switch if you want the MOF file to be automatically recompiled if the CIM Repository ever has to be automatically recovered.</span></span> <span data-ttu-id="3c0a3-205">如需詳細資訊，請輸入 **mofcomp.exe/？**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-205">For more information, type **Mofcomp /?**</span></span> <span data-ttu-id="3c0a3-206">。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-206">at the command prompt.</span></span>

<span data-ttu-id="3c0a3-207">使用 Unicode 字元集的 MOF 檔案，會將簽章包含為檔案的前兩個位元組。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-207">A MOF file that uses the Unicode character set contains a signature as the first two bytes of the file.</span></span> <span data-ttu-id="3c0a3-208">此簽章可以是 U + FFFE 或 U + FEFF，視檔案的位元組順序而定。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-208">This signature is either U+FFFE or U+FEFF, depending on the byte ordering of the file.</span></span>

<span data-ttu-id="3c0a3-209">當剖析程式中未發生任何錯誤時，MOF 編譯器會連接到本機電腦上執行的 WMI 伺服器，除非已指定 **-check** 參數。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-209">When no errors occur in the parsing process, the MOF compiler connects to the WMI server running on the local computer unless the **-check** switch is specified.</span></span> <span data-ttu-id="3c0a3-210">MOF 檔案中定義的類別和實例會新增至 WMI 存放庫。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-210">Classes and instances defined in the MOF file are added to the WMI repository.</span></span>

<span data-ttu-id="3c0a3-211">當更新 WMI 儲存機制發生錯誤時，編譯器不會在編譯器開始處理之前，嘗試將存放庫傳回其狀態。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-211">When an error occurs in updating the WMI repository, the compiler makes no attempt to return the repository to its state before the compiler began processing.</span></span>

<span data-ttu-id="3c0a3-212">**Windows 8：** 在安裝提供者時，mofcomp.exe \[ 會將金鑰 \] 和 \[ 靜態限定詞視為 \] true （如果存在的話），而不論其實際值為何。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-212">**Windows 8:** When installing a provider, mofcomp treats the \[Key\] and \[Static\] qualifiers as true if they are present, regardless of their actual values.</span></span> <span data-ttu-id="3c0a3-213">如果有其他限定詞存在但未明確設定為 true，則會將它們視為 false。</span><span class="sxs-lookup"><span data-stu-id="3c0a3-213">Other qualifiers are treated as false if they are present but not explicitly set to true.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c0a3-214">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c0a3-214">Requirements</span></span>



| <span data-ttu-id="3c0a3-215">需求</span><span class="sxs-lookup"><span data-stu-id="3c0a3-215">Requirement</span></span> | <span data-ttu-id="3c0a3-216">值</span><span class="sxs-lookup"><span data-stu-id="3c0a3-216">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3c0a3-217">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c0a3-217">Minimum supported client</span></span><br/> | <span data-ttu-id="3c0a3-218">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3c0a3-218">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3c0a3-219">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c0a3-219">Minimum supported server</span></span><br/> | <span data-ttu-id="3c0a3-220">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3c0a3-220">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3c0a3-221">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c0a3-221">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c0a3-222">**pragma 命名空間**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-222">**pragma namespace**</span></span>](pragma-namespace.md)
</dt> <dt>

[<span data-ttu-id="3c0a3-223">編譯 MOF 檔案</span><span class="sxs-lookup"><span data-stu-id="3c0a3-223">Compiling MOF Files</span></span>](compiling-mof-files.md)
</dt> <dt>

[<span data-ttu-id="3c0a3-224">編譯當地語系化的 MOF 檔案</span><span class="sxs-lookup"><span data-stu-id="3c0a3-224">Compiling Localized MOF Files</span></span>](compiling-localized-mof-files.md)
</dt> <dt>

[<span data-ttu-id="3c0a3-225">註冊提供者</span><span class="sxs-lookup"><span data-stu-id="3c0a3-225">Registering a Provider</span></span>](registering-a-provider.md)
</dt> <dt>

[<span data-ttu-id="3c0a3-226">**IMOFCompiler::CompileFile**</span><span class="sxs-lookup"><span data-stu-id="3c0a3-226">**IMOFCompiler::CompileFile**</span></span>](/windows/desktop/api/Wbemcli/nf-wbemcli-imofcompiler-compilefile)
</dt> </dl>

 

