---
description: 元件資料表會列出元件，並具有下列資料行。
ms.assetid: 069d64e9-106a-42b7-8dea-a44fc0c6e0cd
title: 元件資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b721996767fa98209f0e13530f8f1bb1ba8cca07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191700"
---
# <a name="component-table"></a><span data-ttu-id="69fc9-103">元件資料表</span><span class="sxs-lookup"><span data-stu-id="69fc9-103">Component Table</span></span>

<span data-ttu-id="69fc9-104">元件資料表會列出元件，並具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="69fc9-104">The Component table lists components and it has the following columns.</span></span>



| <span data-ttu-id="69fc9-105">Column</span><span class="sxs-lookup"><span data-stu-id="69fc9-105">Column</span></span>      | <span data-ttu-id="69fc9-106">類型</span><span class="sxs-lookup"><span data-stu-id="69fc9-106">Type</span></span>                         | <span data-ttu-id="69fc9-107">答案</span><span class="sxs-lookup"><span data-stu-id="69fc9-107">Key</span></span> | <span data-ttu-id="69fc9-108">Nullable</span><span class="sxs-lookup"><span data-stu-id="69fc9-108">Nullable</span></span> |
|-------------|------------------------------|-----|----------|
| <span data-ttu-id="69fc9-109">元件</span><span class="sxs-lookup"><span data-stu-id="69fc9-109">Component</span></span>   | [<span data-ttu-id="69fc9-110">識別碼</span><span class="sxs-lookup"><span data-stu-id="69fc9-110">Identifier</span></span>](identifier.md) | <span data-ttu-id="69fc9-111">Y</span><span class="sxs-lookup"><span data-stu-id="69fc9-111">Y</span></span>   | <span data-ttu-id="69fc9-112">N</span><span class="sxs-lookup"><span data-stu-id="69fc9-112">N</span></span>        |
| <span data-ttu-id="69fc9-113">ComponentId</span><span class="sxs-lookup"><span data-stu-id="69fc9-113">ComponentId</span></span> | [<span data-ttu-id="69fc9-114">GUID</span><span class="sxs-lookup"><span data-stu-id="69fc9-114">GUID</span></span>](guid.md)             | <span data-ttu-id="69fc9-115">N</span><span class="sxs-lookup"><span data-stu-id="69fc9-115">N</span></span>   | <span data-ttu-id="69fc9-116">Y</span><span class="sxs-lookup"><span data-stu-id="69fc9-116">Y</span></span>        |
| <span data-ttu-id="69fc9-117">目錄\_</span><span class="sxs-lookup"><span data-stu-id="69fc9-117">Directory\_</span></span> | [<span data-ttu-id="69fc9-118">識別碼</span><span class="sxs-lookup"><span data-stu-id="69fc9-118">Identifier</span></span>](identifier.md) | <span data-ttu-id="69fc9-119">N</span><span class="sxs-lookup"><span data-stu-id="69fc9-119">N</span></span>   | <span data-ttu-id="69fc9-120">N</span><span class="sxs-lookup"><span data-stu-id="69fc9-120">N</span></span>        |
| <span data-ttu-id="69fc9-121">屬性</span><span class="sxs-lookup"><span data-stu-id="69fc9-121">Attributes</span></span>  | [<span data-ttu-id="69fc9-122">整數</span><span class="sxs-lookup"><span data-stu-id="69fc9-122">Integer</span></span>](integer.md)       | <span data-ttu-id="69fc9-123">N</span><span class="sxs-lookup"><span data-stu-id="69fc9-123">N</span></span>   | <span data-ttu-id="69fc9-124">N</span><span class="sxs-lookup"><span data-stu-id="69fc9-124">N</span></span>        |
| <span data-ttu-id="69fc9-125">條件</span><span class="sxs-lookup"><span data-stu-id="69fc9-125">Condition</span></span>   | [<span data-ttu-id="69fc9-126">Condition</span><span class="sxs-lookup"><span data-stu-id="69fc9-126">Condition</span></span>](condition.md)   | <span data-ttu-id="69fc9-127">N</span><span class="sxs-lookup"><span data-stu-id="69fc9-127">N</span></span>   | <span data-ttu-id="69fc9-128">Y</span><span class="sxs-lookup"><span data-stu-id="69fc9-128">Y</span></span>        |
| <span data-ttu-id="69fc9-129">KeyPath</span><span class="sxs-lookup"><span data-stu-id="69fc9-129">KeyPath</span></span>     | [<span data-ttu-id="69fc9-130">識別碼</span><span class="sxs-lookup"><span data-stu-id="69fc9-130">Identifier</span></span>](identifier.md) | <span data-ttu-id="69fc9-131">N</span><span class="sxs-lookup"><span data-stu-id="69fc9-131">N</span></span>   | <span data-ttu-id="69fc9-132">Y</span><span class="sxs-lookup"><span data-stu-id="69fc9-132">Y</span></span>        |



 

## <a name="columns"></a><span data-ttu-id="69fc9-133">資料行</span><span class="sxs-lookup"><span data-stu-id="69fc9-133">Columns</span></span>

<dl> <dt>

<span data-ttu-id="69fc9-134"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>元件</span><span class="sxs-lookup"><span data-stu-id="69fc9-134"><span id="Component"></span><span id="component"></span><span id="COMPONENT"></span>Component</span></span>
</dt> <dd>

<span data-ttu-id="69fc9-135">識別元件記錄。</span><span class="sxs-lookup"><span data-stu-id="69fc9-135">Identifies the component record.</span></span>

<span data-ttu-id="69fc9-136">主表索引鍵。</span><span class="sxs-lookup"><span data-stu-id="69fc9-136">Primary table key.</span></span>

</dd> <dt>

<span data-ttu-id="69fc9-137"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span><span class="sxs-lookup"><span data-stu-id="69fc9-137"><span id="ComponentId"></span><span id="componentid"></span><span id="COMPONENTID"></span>ComponentId</span></span>
</dt> <dd>

<span data-ttu-id="69fc9-138">此元件、版本和語言特有的字串 GUID。</span><span class="sxs-lookup"><span data-stu-id="69fc9-138">A string GUID unique to this component, version, and language.</span></span>

<span data-ttu-id="69fc9-139">請注意，這些 Guid 的字母必須為大寫。</span><span class="sxs-lookup"><span data-stu-id="69fc9-139">Note that the letters of these GUIDs must be uppercase.</span></span> <span data-ttu-id="69fc9-140">GUIDGEN 之類的公用程式可以產生包含小寫字母的 Guid。</span><span class="sxs-lookup"><span data-stu-id="69fc9-140">Utilities such as GUIDGEN can generate GUIDs containing lowercase letters.</span></span> <span data-ttu-id="69fc9-141">小寫字母必須變更為大寫才能讓這些有效的元件程式碼 Guid。</span><span class="sxs-lookup"><span data-stu-id="69fc9-141">The lowercase letters must be changed to uppercase to make these valid component code GUIDs.</span></span>

<span data-ttu-id="69fc9-142">如果這個資料行是 null，安裝程式就不會註冊元件，而且安裝程式無法移除或修復元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-142">If this column is null the installer does not register the component and the component cannot be removed or repaired by the installer.</span></span> <span data-ttu-id="69fc9-143">如果只有在安裝期間才需要元件，例如可清除暫存檔或移除舊產品的自訂動作，則可能會刻意完成這項操作。</span><span class="sxs-lookup"><span data-stu-id="69fc9-143">This might be intentionally done if the component is only needed during the installation, such as a custom action that cleans up temporary files or removes an old product.</span></span> <span data-ttu-id="69fc9-144">將資料檔案複製到不需要註冊的使用者電腦時，也可能很有用。</span><span class="sxs-lookup"><span data-stu-id="69fc9-144">It may also be useful when copying data files to a user's computer that do not need to be registered.</span></span>

</dd> <dt>

<span data-ttu-id="69fc9-145"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>目錄\_</span><span class="sxs-lookup"><span data-stu-id="69fc9-145"><span id="Directory_"></span><span id="directory_"></span><span id="DIRECTORY_"></span>Directory\_</span></span>
</dt> <dd>

<span data-ttu-id="69fc9-146">[目錄資料表](directory-table.md)中專案的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="69fc9-146">External key of an entry in the [Directory table](directory-table.md).</span></span> <span data-ttu-id="69fc9-147">這是屬性名稱，其值包含實際的路徑，可以透過 [AppSearch 動作](appsearch-action.md) 或從目錄資料表取得的預設設定來設定。</span><span class="sxs-lookup"><span data-stu-id="69fc9-147">This is a property name whose value contains the actual path, which can be set either by the [AppSearch action](appsearch-action.md) or with the default setting obtained from the Directory table.</span></span>

<span data-ttu-id="69fc9-148">開發人員必須避免撰寫將檔案放入其中一個使用者設定檔資料夾的元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-148">Developers must avoid authoring components that place files into one of the User Profile folders.</span></span> <span data-ttu-id="69fc9-149">在多使用者的情況下，所有使用者都無法使用這些檔案，而且可能會導致安裝程式將元件永久視為需要修復。</span><span class="sxs-lookup"><span data-stu-id="69fc9-149">These files would not be available to all users in multi-user situations and could cause the installer to permanently view the component as requiring repair.</span></span>

<span data-ttu-id="69fc9-150">目錄資料表中第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="69fc9-150">External key to column one of the Directory table.</span></span>

</dd> <dt>

<span data-ttu-id="69fc9-151"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="69fc9-151"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="69fc9-152">此資料行包含一個位旗標，可指定遠端執行的選項。</span><span class="sxs-lookup"><span data-stu-id="69fc9-152">This column contains a bit flag that specifies options for remote execution.</span></span> <span data-ttu-id="69fc9-153">將指定的位新增至資料行中的總計值，以包含選項。</span><span class="sxs-lookup"><span data-stu-id="69fc9-153">Add the indicated bit to the total value in the column to include an option.</span></span>

> [!Note]  
> <span data-ttu-id="69fc9-154">如果是從 web 位置下載的 .msi 檔案，則不應將屬性旗標設定為允許從來源執行元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-154">In the case of an .msi file that is being downloaded from a web location, the attribute flags should not be set to allow a component to be run-from-source.</span></span> <span data-ttu-id="69fc9-155">這是 Windows Installer 的限制，而且可能會傳回 INSTALLSTATE BADCONFIG 的功能狀態 \_ 。</span><span class="sxs-lookup"><span data-stu-id="69fc9-155">This is a limitation of the Windows Installer and can return a feature state of INSTALLSTATE\_BADCONFIG.</span></span>

 



<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69fc9-156">位旗標</span><span class="sxs-lookup"><span data-stu-id="69fc9-156">Bit flag</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><dl> <span data-ttu-id="69fc9-157"><dt><strong>msidbComponentAttributesLocalOnly</strong></dt> <dt>0</dt> <dt>0x0000</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-157"><dt><strong>msidbComponentAttributesLocalOnly</strong></dt> <dt>0</dt> <dt>0x0000</dt> </span></span></dl> <span data-ttu-id="69fc9-158">元件無法從來源執行。</span><span class="sxs-lookup"><span data-stu-id="69fc9-158">Component cannot be run from source.</span></span> <span data-ttu-id="69fc9-159">針對屬於某項功能的所有元件設定此位，以防止此功能從網路或從來源執行。</span><span class="sxs-lookup"><span data-stu-id="69fc9-159">Set this bit for all components belonging to a feature to prevent the feature from being run-from-network or run-from-source.</span></span> <span data-ttu-id="69fc9-160">請注意，如果功能沒有元件，則此功能一律會顯示從來源執行，並從我的電腦執行為有效的選項。</span><span class="sxs-lookup"><span data-stu-id="69fc9-160">Note that if a feature has no components, the feature always shows run-from-source and run-from-my-computer as valid options.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="69fc9-161"><dt><strong>msidbComponentAttributesSourceOnly</strong></dt> <dt>1</dt> <dt>0x0001</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-161"><dt><strong>msidbComponentAttributesSourceOnly</strong></dt> <dt>1</dt> <dt>0x0001</dt> </span></span></dl> <span data-ttu-id="69fc9-162">元件只能從來源執行。</span><span class="sxs-lookup"><span data-stu-id="69fc9-162">Component can only be run from source.</span></span> <span data-ttu-id="69fc9-163">針對屬於某項功能的所有元件設定此位，以防止從我的電腦執行此功能。</span><span class="sxs-lookup"><span data-stu-id="69fc9-163">Set this bit for all components belonging to a feature to prevent the feature from being run-from-my-computer.</span></span> <span data-ttu-id="69fc9-164">請注意，如果功能沒有元件，則此功能一律會顯示從來源執行，並從我的電腦執行為有效的選項。</span><span class="sxs-lookup"><span data-stu-id="69fc9-164">Note that if a feature has no components, the feature always shows run-from-source and run-from-my-computer as valid options.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="69fc9-165"><dt><strong>msidbComponentAttributesOptional</strong></dt> <dt>2</dt> <dt>0x0002</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-165"><dt><strong>msidbComponentAttributesOptional</strong></dt> <dt>2</dt> <dt>0x0002</dt> </span></span></dl> <span data-ttu-id="69fc9-166">元件可以在本機或從來源執行。</span><span class="sxs-lookup"><span data-stu-id="69fc9-166">Component can run locally or from source.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="69fc9-167"><dt><strong>msidbComponentAttributesRegistryKeyPath</strong></dt> <dt>4</dt> <dt>0x0004</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-167"><dt><strong>msidbComponentAttributesRegistryKeyPath</strong></dt> <dt>4</dt> <dt>0x0004</dt> </span></span></dl> <span data-ttu-id="69fc9-168">如果設定此位，則 KeyPath 資料行中的值會當做登錄 <a href="registry-table.md">表</a>中的索引鍵使用。</span><span class="sxs-lookup"><span data-stu-id="69fc9-168">If this bit is set, the value in the KeyPath column is used as a key into the <a href="registry-table.md">Registry table</a>.</span></span> <span data-ttu-id="69fc9-169">如果登錄資料表中對應記錄的值欄位為 null，則該記錄中的名稱欄位不能包含 &quot; + &quot; 、 &quot; - &quot; 或 &quot; \* &quot; 。</span><span class="sxs-lookup"><span data-stu-id="69fc9-169">If the Value field of the corresponding record in the Registry table is null, the Name field in that record must not contain &quot;+&quot;, &quot;-&quot;, or &quot;\*&quot;.</span></span> <span data-ttu-id="69fc9-170">如需詳細資訊，請參閱登錄 <a href="registry-table.md">表</a>中的名稱欄位描述。</span><span class="sxs-lookup"><span data-stu-id="69fc9-170">For more information, see the description of the Name field in <a href="registry-table.md">Registry table</a>.</span></span><br/> <span data-ttu-id="69fc9-171">建議將此位設定為寫入 HKCU hive 的登錄專案。</span><span class="sxs-lookup"><span data-stu-id="69fc9-171">Setting this bit is recommended for registry entries written to the HKCU hive.</span></span> <span data-ttu-id="69fc9-172">這可確保當相同電腦上有多個使用者時，安裝程式會寫入必要的 HKCU 登錄專案。</span><span class="sxs-lookup"><span data-stu-id="69fc9-172">This ensures the installer writes the necessary HKCU registry entries when there are multiple users on the same machine.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="69fc9-173"><dt><strong>msidbComponentAttributesSharedDllRefCount</strong></dt> <dt>8</dt> <dt>0x0008</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-173"><dt><strong>msidbComponentAttributesSharedDllRefCount</strong></dt> <dt>8</dt> <dt>0x0008</dt> </span></span></dl> <span data-ttu-id="69fc9-174">如果設定此位，安裝程式會在元件金鑰檔的共用 DLL 登錄中遞增參考計數。</span><span class="sxs-lookup"><span data-stu-id="69fc9-174">If this bit is set, the installer increments the reference count in the shared DLL registry of the component's key file.</span></span> <span data-ttu-id="69fc9-175">如果未設定此位，則只有在參考計數已經存在時，安裝程式才會遞增參考計數。</span><span class="sxs-lookup"><span data-stu-id="69fc9-175">If this bit is not set, the installer increments the reference count only if the reference count already exists.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="69fc9-176"><dt><strong>msidbComponentAttributesPermanent</strong></dt> <dt>16</dt> <dt>0x0010</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-176"><dt><strong>msidbComponentAttributesPermanent</strong></dt> <dt>16</dt> <dt>0x0010</dt> </span></span></dl> <span data-ttu-id="69fc9-177">如果設定此位，安裝程式就不會在卸載期間移除元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-177">If this bit is set, the installer does not remove the component during an uninstall.</span></span> <span data-ttu-id="69fc9-178">安裝程式會在 Windows Installer 登錄設定中為元件註冊額外的系統用戶端。</span><span class="sxs-lookup"><span data-stu-id="69fc9-178">The installer registers an extra system client for the component in the Windows Installer registry settings.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="69fc9-179"><dt><strong>msidbComponentAttributesODBCDataSource</strong></dt> <dt>32</dt> <dt>0x0020</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-179"><dt><strong>msidbComponentAttributesODBCDataSource</strong></dt> <dt>32</dt> <dt>0x0020</dt> </span></span></dl> <span data-ttu-id="69fc9-180">如果設定此位，KeyPath 資料行中的值就是 <a href="odbcdatasource-table.md">ODBCDataSource 資料表</a>中的索引鍵。</span><span class="sxs-lookup"><span data-stu-id="69fc9-180">If this bit is set, the value in the KeyPath column is a key into the <a href="odbcdatasource-table.md">ODBCDataSource table</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="69fc9-181"><dt><strong>msidbComponentAttributesTransitive</strong></dt> <dt>64</dt> <dt>0x0040</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-181"><dt><strong>msidbComponentAttributesTransitive</strong></dt> <dt>64</dt> <dt>0x0040</dt> </span></span></dl> <span data-ttu-id="69fc9-182">如果設定此位，則安裝程式會在重新安裝時重新評估 [條件] 資料行中的語句值。</span><span class="sxs-lookup"><span data-stu-id="69fc9-182">If this bit is set, the installer reevaluates the value of the statement in the Condition column upon a reinstall.</span></span> <span data-ttu-id="69fc9-183">如果值先前是 False，且已變更為 True，則安裝程式會安裝元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-183">If the value was previously False and has changed to True, the installer installs the component.</span></span> <span data-ttu-id="69fc9-184">如果值先前是 True 且已變更為 False，即使元件有其他產品做為用戶端，安裝程式也會移除該元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-184">If the value was previously True and has changed to False, the installer removes the component even if the component has other products as clients.</span></span><br/> <span data-ttu-id="69fc9-185">此位應該只針對可轉移的元件進行設定。</span><span class="sxs-lookup"><span data-stu-id="69fc9-185">This bit should only be set for transitive components.</span></span> <span data-ttu-id="69fc9-186">請參閱 <a href="using-transitive-components.md">使用可轉移的元件</a>。</span><span class="sxs-lookup"><span data-stu-id="69fc9-186">See <a href="using-transitive-components.md">Using Transitive Components</a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="69fc9-187"><dt><strong>msidbComponentAttributesNeverOverwrite</strong></dt> <dt>128</dt> <dt>0x0080</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-187"><dt><strong>msidbComponentAttributesNeverOverwrite</strong></dt> <dt>128</dt> <dt>0x0080</dt> </span></span></dl> <span data-ttu-id="69fc9-188">如果設定此位，則如果元件的金鑰路徑檔案或機碼路徑登錄專案已經存在，安裝程式就不會安裝或重新安裝元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-188">If this bit is set, the installer does not install or reinstall the component if a key path file or a key path registry entry for the component already exists.</span></span> <span data-ttu-id="69fc9-189">應用程式會將本身註冊為元件的用戶端。</span><span class="sxs-lookup"><span data-stu-id="69fc9-189">The application does register itself as a client of the component.</span></span><br/> <span data-ttu-id="69fc9-190">只有登錄資料表所註冊的元件才能使用此旗標。</span><span class="sxs-lookup"><span data-stu-id="69fc9-190">Use this flag only for components that are being registered by the Registry table.</span></span> <span data-ttu-id="69fc9-191">請勿將此旗標用於 <a href="appid-table.md">AppId</a>、 <a href="class-table.md">類別</a>、 <a href="extension-table.md">延伸</a>模組、 <a href="progid-table.md">ProgId</a>、 <a href="mime-table.md">MIME</a>和 <a href="verb-table.md">動詞資料表</a>所註冊的元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-191">Do not use this flag for components registered by the <a href="appid-table.md">AppId</a>, <a href="class-table.md">Class</a>, <a href="extension-table.md">Extension</a>, <a href="progid-table.md">ProgId</a>, <a href="mime-table.md">MIME</a>, and <a href="verb-table.md">Verb tables</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="69fc9-192"><dt><strong>msidbComponentAttributes64bit</strong></dt> <dt>256</dt> <dt>0x0100</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-192"><dt><strong>msidbComponentAttributes64bit</strong></dt> <dt>256</dt> <dt>0x0100</dt> </span></span></dl> <span data-ttu-id="69fc9-193">設定此位以將此標示為64位元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-193">Set this bit to mark this as a 64-bit component.</span></span> <span data-ttu-id="69fc9-194">這個屬性可協助安裝包含32位和64位元件的封裝。</span><span class="sxs-lookup"><span data-stu-id="69fc9-194">This attribute facilitates the installation of packages that include both 32-bit and 64-bit components.</span></span> <span data-ttu-id="69fc9-195">如果未設定此位，則會將元件註冊為32位元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-195">If this bit is not set, the component is registered as a 32-bit component.</span></span><br/> <span data-ttu-id="69fc9-196">如果這是取代32位元件的64位元件，請在 [元件] 資料行中設定此位並指派新的 GUID。</span><span class="sxs-lookup"><span data-stu-id="69fc9-196">If this is a 64-bit component replacing a 32-bit component, set this bit and assign a new GUID in the ComponentId column.</span></span><br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="69fc9-197"><dt><strong>msidbComponentAttributesDisableRegistryReflection</strong></dt> <dt>512</dt> <dt>0x0200</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-197"><dt><strong>msidbComponentAttributesDisableRegistryReflection</strong></dt> <dt>512</dt> <dt>0x0200</dt> </span></span></dl> <span data-ttu-id="69fc9-198">設定此位可針對受此元件影響的所有現有和新登錄機碼停用登錄 <a href="/windows/desktop/WinProg64/registry-reflection">反映</a> 。</span><span class="sxs-lookup"><span data-stu-id="69fc9-198">Set this bit to disable <a href="/windows/desktop/WinProg64/registry-reflection">Registry Reflection</a> on all existing and new registry keys affected by this component.</span></span> <span data-ttu-id="69fc9-199">如果設定此位，Windows Installer 會在元件所存取的每個索引鍵上呼叫 <a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey"><strong>RegDisableReflectionKey</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="69fc9-199">If this bit is set, the Windows Installer calls the <a href="/windows/desktop/api/winreg/nf-winreg-regdisablereflectionkey"><strong>RegDisableReflectionKey</strong></a> on each key being accessed by the component.</span></span> <span data-ttu-id="69fc9-200">這位 Windows Installer 版本4.0 提供。</span><span class="sxs-lookup"><span data-stu-id="69fc9-200">This bit is available with Windows Installer version 4.0.</span></span> <span data-ttu-id="69fc9-201">32位系統會忽略此位。</span><span class="sxs-lookup"><span data-stu-id="69fc9-201">This bit is ignored on 32-bit systems.</span></span> <span data-ttu-id="69fc9-202">64位版本的 Windows XP 會忽略此位。</span><span class="sxs-lookup"><span data-stu-id="69fc9-202">This bit is ignored on the 64-bit versions of Windows XP.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="69fc9-203">在64位 Windows 模擬器上執行的32位 Windows 應用程式 (WOW64) 參考的登錄與64位應用程式不同。</span><span class="sxs-lookup"><span data-stu-id="69fc9-203">32-bit Windows applications running on the 64-bit Windows emulator (WOW64) refer to a different view of the registry than 64-bit applications.</span></span> <span data-ttu-id="69fc9-204">登錄反映會複製這兩個登錄視圖之間的一些登錄值。</span><span class="sxs-lookup"><span data-stu-id="69fc9-204">Registry reflection copies some registry values between these two registry views.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><dl> <span data-ttu-id="69fc9-205"><dt><strong>msidbComponentAttributesUninstallOnSupersedence</strong></dt> <dt>1024</dt> <dt>0x0400</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-205"><dt><strong>msidbComponentAttributesUninstallOnSupersedence</strong></dt> <dt>1024</dt> <dt>0x0400</dt> </span></span></dl> <span data-ttu-id="69fc9-206">為修補程式套件中的元件設定此位，以避免在電腦上留下孤立的元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-206">Set this bit for a component in a patch package to prevent leaving orphan components on the computer.</span></span> <span data-ttu-id="69fc9-207">如果已安裝後續修補程式，並在其<a href="msipatchsequence-table.md">MsiPatchSequence</a>資料表中標示<strong>msidbPatchSequenceSupersedeEarlier</strong>值來取代第一個修補程式，Windows Installer 4.5 和更新版本可以取消註冊並卸載以<strong>msidbComponentAttributesUninstallOnSupersedence</strong>值標示的元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-207">If a subsequent patch is installed, marked with the <strong>msidbPatchSequenceSupersedeEarlier</strong> value in its <a href="msipatchsequence-table.md">MsiPatchSequence</a> table to supersede the first patch, Windows Installer 4.5 and later can unregister and uninstall components marked with the <strong>msidbComponentAttributesUninstallOnSupersedence</strong> value.</span></span> <span data-ttu-id="69fc9-208">如果元件未標示此位，則取代修補程式的安裝可能會離開電腦上未使用的元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-208">If the component is not marked with this bit, installation of a superseding patch can leave behind an unused component on the computer.</span></span><br/> <span data-ttu-id="69fc9-209">設定 <strong>MSIUNINSTALLSUPERSEDEDCOMPONENTS</strong> 屬性的效果與設定所有元件的這個位相同。</span><span class="sxs-lookup"><span data-stu-id="69fc9-209">Setting the <strong>MSIUNINSTALLSUPERSEDEDCOMPONENTS</strong> property has the same effect as setting this bit for all components.</span></span><br/> <span data-ttu-id="69fc9-210"><strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4.0 及更早版本</a>：</strong> 不支援 <strong>msidbComponentAttributesUninstallOnSupersedence</strong> 值，且會忽略。</span><span class="sxs-lookup"><span data-stu-id="69fc9-210"><strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4.0 and earlier</a>:</strong> The <strong>msidbComponentAttributesUninstallOnSupersedence</strong> value is not supported and is ignored.</span></span><br/> <br/></td>
</tr>
<tr class="odd">
<td><dl> <span data-ttu-id="69fc9-211"><dt><strong>msidbComponentAttributesShared</strong></dt> <dt>2048</dt> <dt>0x0800</dt> </span><span class="sxs-lookup"><span data-stu-id="69fc9-211"><dt><strong>msidbComponentAttributesShared</strong></dt> <dt>2048</dt> <dt>0x0800</dt> </span></span></dl> <span data-ttu-id="69fc9-212">如果元件在至少一個安裝于系統上的封裝中以此屬性值標示，則安裝程式會將元件視為所有封裝中標示的元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-212">If a component is marked with this attribute value in at least one package installed on the system, the installer treats the component as marked in all packages.</span></span> <span data-ttu-id="69fc9-213">如果已卸載共用標示元件的套件，Windows Installer 4.5 可繼續在系統上共用元件的最高版本，即使是由正在卸載的封裝所安裝的最高版本。</span><span class="sxs-lookup"><span data-stu-id="69fc9-213">If a package that shares the marked component is uninstalled, Windows Installer 4.5 can continue to share the highest version of the component on the system, even if that highest version was installed by the package that is being uninstalled.</span></span> <br/> <span data-ttu-id="69fc9-214">如果 DisableSharedComponent 原則設定為1，則沒有任何套件會取得此位啟用的共用元件功能。</span><span class="sxs-lookup"><span data-stu-id="69fc9-214">If the DisableSharedComponent policy is set to 1, no package gets the shared component functionality enabled by this bit.</span></span><br/> <span data-ttu-id="69fc9-215"><strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4.0 及更早版本</a>：</strong> 不支援 <strong>msidbComponentAttributesShared</strong> 值，且會忽略。</span><span class="sxs-lookup"><span data-stu-id="69fc9-215"><strong><a href="not-supported-in-windows-installer-4-0.md">Windows Installer 4.0 and earlier</a>:</strong> The <strong>msidbComponentAttributesShared</strong> value is not supported and is ignored.</span></span><br/> <br/></td>
</tr>
</tbody>
</table>



 

</dd> <dt>

<span data-ttu-id="69fc9-216"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>條件</span><span class="sxs-lookup"><span data-stu-id="69fc9-216"><span id="Condition"></span><span id="condition"></span><span id="CONDITION"></span>Condition</span></span>
</dt> <dd>

<span data-ttu-id="69fc9-217">此資料行包含可控制是否已安裝元件的條件陳述式。</span><span class="sxs-lookup"><span data-stu-id="69fc9-217">This column contains a conditional statement that can control whether a component is installed.</span></span> <span data-ttu-id="69fc9-218">如果條件為 null 或評估為 true，則會啟用元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-218">If the condition is null or evaluates to true, then the component is enabled.</span></span> <span data-ttu-id="69fc9-219">如果條件評估為 False，則元件已停用且未安裝。</span><span class="sxs-lookup"><span data-stu-id="69fc9-219">If the condition evaluates to False, then the component is disabled and is not installed.</span></span>

<span data-ttu-id="69fc9-220">[條件] 欄位只會在 [CostFinalize 動作](costfinalize-action.md)期間啟用或停用元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-220">The Condition field enables or disables a component only during the [CostFinalize action](costfinalize-action.md).</span></span> <span data-ttu-id="69fc9-221">若要在 CostFinalize 之後啟用或停用元件，您必須使用自訂動作或 [Dataadapter.doaction ControlEvent](doaction-controlevent.md) 來呼叫 [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea)。</span><span class="sxs-lookup"><span data-stu-id="69fc9-221">To enable or disable a component after CostFinalize, you must use a custom action or the [DoAction ControlEvent](doaction-controlevent.md) to call [**MsiSetComponentState**](/windows/desktop/api/Msiquery/nf-msiquery-msisetcomponentstatea).</span></span>

<span data-ttu-id="69fc9-222">請注意，除非為元件設定 [屬性] 資料行中的可轉移位，否則即使在 [條件] 資料行中的條件陳述式之後，會在產品的後續維護安裝中評估為 False，仍然會在安裝後啟用此元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-222">Note that unless the Transitive bit in the Attributes column is set for a component, the component remains enabled once installed even if the conditional statement in the Condition column later evaluates to False on a subsequent maintenance installation of the product.</span></span>

<span data-ttu-id="69fc9-223">元件資料表中的 [條件] 資料行接受條件運算式，其中包含已安裝的功能和元件狀態的參考。</span><span class="sxs-lookup"><span data-stu-id="69fc9-223">The Condition column in the Component table accepts conditional expressions containing references to the installed states of features and components.</span></span> <span data-ttu-id="69fc9-224">如需條件陳述式語法的詳細資訊，請參閱 [條件陳述式語法](conditional-statement-syntax.md)。</span><span class="sxs-lookup"><span data-stu-id="69fc9-224">For information on the syntax of conditional statements, see [Conditional Statement Syntax](conditional-statement-syntax.md).</span></span>

</dd> <dt>

<span data-ttu-id="69fc9-225"><span id="KeyPath"></span><span id="keypath"></span><span id="KEYPATH"></span>KeyPath</span><span class="sxs-lookup"><span data-stu-id="69fc9-225"><span id="KeyPath"></span><span id="keypath"></span><span id="KEYPATH"></span>KeyPath</span></span>
</dt> <dd>

<span data-ttu-id="69fc9-226">這個值指向安裝程式用來偵測元件的檔案或資料夾。</span><span class="sxs-lookup"><span data-stu-id="69fc9-226">This value points to a file or folder belonging to the component that the installer uses to detect the component.</span></span> <span data-ttu-id="69fc9-227">兩個元件不能共用相同的索引鍵路徑值。</span><span class="sxs-lookup"><span data-stu-id="69fc9-227">Two components cannot share the same key path value.</span></span> <span data-ttu-id="69fc9-228">此資料行中的值也是 [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) 函數所傳回的路徑。</span><span class="sxs-lookup"><span data-stu-id="69fc9-228">The value in this column is also the path returned by the [**MsiGetComponentPath**](/windows/desktop/api/Msi/nf-msi-msigetcomponentpatha) function.</span></span>

<span data-ttu-id="69fc9-229">如果值不是 null，則根據屬性值，KeyPath 就會是登錄、 [ODBCDataSource](odbcdatasource-table.md)或檔案[資料表](file-table.md)[中的主鍵](registry-table.md)。</span><span class="sxs-lookup"><span data-stu-id="69fc9-229">If the value is not null, then KeyPath is either a primary key into the [Registry](registry-table.md), [ODBCDataSource](odbcdatasource-table.md), or [File tables](file-table.md) depending upon the Attribute value.</span></span> <span data-ttu-id="69fc9-230">如果 KeyPath 為 null，則會使用目錄資料行的資料夾 \_ 做為金鑰路徑。</span><span class="sxs-lookup"><span data-stu-id="69fc9-230">If KeyPath is null, then the folder of the Directory\_ column is used as the key path.</span></span>

<span data-ttu-id="69fc9-231">因為安裝程式所建立的資料夾是空的，所以您必須在 [CreateFolder 資料表](createfolder-table.md) 中撰寫一個專案，才能安裝包含空資料夾的元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-231">Because folders created by the installer are deleted when they become empty, you must author an entry into the [CreateFolder table](createfolder-table.md) to install a component that consists of an empty folder.</span></span>

<span data-ttu-id="69fc9-232">請注意，如果 Windows Installer 元件包含受 [Windows 資源保護](/windows/desktop/Wfp/windows-resource-protection-portal) (WRP) 的檔案或登錄機碼，或受 Windows 檔案保護 (WFP) 保護的檔案，則必須使用此資源做為元件的 KeyPath。</span><span class="sxs-lookup"><span data-stu-id="69fc9-232">Note that if a Windows Installer component contains a file or registry key that is protected by [Windows Resource Protection](/windows/desktop/Wfp/windows-resource-protection-portal) (WRP) or a file that is protected by Windows File Protection (WFP), this resource must be used as the KeyPath for the component.</span></span> <span data-ttu-id="69fc9-233">在此情況下，Windows Installer 不會安裝、更新或移除元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-233">In this case, Windows Installer does not install, update, or remove the component.</span></span> <span data-ttu-id="69fc9-234">您不應該在安裝套件中包含任何受保護的資源。</span><span class="sxs-lookup"><span data-stu-id="69fc9-234">You should not include any protected resources in an installation package.</span></span> <span data-ttu-id="69fc9-235">相反地，您應該針對 Windows 資源保護使用 [支援的資源取代機制](/windows/desktop/Wfp/supported-file-replacement-mechanisms) 。</span><span class="sxs-lookup"><span data-stu-id="69fc9-235">Instead, you should use the [supported resource replacement mechanisms](/windows/desktop/Wfp/supported-file-replacement-mechanisms) for Windows Resource Protection.</span></span> <span data-ttu-id="69fc9-236">如需詳細資訊，請參閱 [使用 Windows Installer 和 Windows 資源保護](windows-resource-protection-on-windows-vista.md)。</span><span class="sxs-lookup"><span data-stu-id="69fc9-236">For more information, see [Using Windows Installer and Windows Resource Protection](windows-resource-protection-on-windows-vista.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69fc9-237">備註</span><span class="sxs-lookup"><span data-stu-id="69fc9-237">Remarks</span></span>

<span data-ttu-id="69fc9-238">如需元件和功能之間關聯性的討論，請參閱 [功能表](feature-table.md)。</span><span class="sxs-lookup"><span data-stu-id="69fc9-238">For a discussion of the relationship between components and features, see [Feature Table](feature-table.md).</span></span>

<span data-ttu-id="69fc9-239">安裝程式會持續追蹤共用 Dll，而不受登錄中的共用 DLL 參考計數影響。</span><span class="sxs-lookup"><span data-stu-id="69fc9-239">The installer keeps track of shared DLLs independently of the shared DLL reference count in the registry.</span></span> <span data-ttu-id="69fc9-240">如果有共用 DLL 的參考計數存在於登錄中，安裝程式會在安裝檔案時，一律遞增計數，並在卸載時將其遞減。</span><span class="sxs-lookup"><span data-stu-id="69fc9-240">If a reference count for a shared DLL exists in the registry, the installer always increments the count when it is installing the file and decrements it when it is uninstalling.</span></span> <span data-ttu-id="69fc9-241">如果未設定 **msidbComponentAttributesSharedDllRefCount**，而且參考計數尚未存在，安裝程式將不會建立該參考計數。</span><span class="sxs-lookup"><span data-stu-id="69fc9-241">If **msidbComponentAttributesSharedDllRefCount**, is not set, and the reference count does not already exist, the installer will not create one.</span></span> <span data-ttu-id="69fc9-242">請注意，所有安裝到系統資料夾的檔案，登錄中的 Shareddll 參考計數都會遞增。</span><span class="sxs-lookup"><span data-stu-id="69fc9-242">Note that the SharedDLLs reference count in the registry is incremented for any files installed to the System folder.</span></span>

<span data-ttu-id="69fc9-243">如果未設定 **msidbComponentAttributesSharedDllRefCount** ，則其他應用程式即使仍然需要，也可以移除該元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-243">If **msidbComponentAttributesSharedDllRefCount** is not set, then another application can remove the component even if it is still needed.</span></span> <span data-ttu-id="69fc9-244">若要瞭解如何發生這種情況，請考慮下列案例：</span><span class="sxs-lookup"><span data-stu-id="69fc9-244">To see how this could happen consider the following scenario:</span></span>

-   <span data-ttu-id="69fc9-245">使用安裝程式的應用程式會安裝共用元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-245">An application that uses the installer installs a shared component.</span></span>
-   <span data-ttu-id="69fc9-246">未設定 **msidbComponentAttributesSharedDllRefCount** 位，而且沒有參考計數。</span><span class="sxs-lookup"><span data-stu-id="69fc9-246">The **msidbComponentAttributesSharedDllRefCount** bit is not set and there is no reference count.</span></span> <span data-ttu-id="69fc9-247">因此，安裝程式不會開始參考計數。</span><span class="sxs-lookup"><span data-stu-id="69fc9-247">Thus the installer does not begin a reference count.</span></span>
-   <span data-ttu-id="69fc9-248">會安裝共用此元件且不使用安裝程式的繼承應用程式。</span><span class="sxs-lookup"><span data-stu-id="69fc9-248">A legacy application that shares this component and does not use the installer is installed.</span></span>
-   <span data-ttu-id="69fc9-249">繼承應用程式會建立並遞增共用元件的參考計數。</span><span class="sxs-lookup"><span data-stu-id="69fc9-249">The legacy application creates and increments a reference count for the shared component.</span></span>
-   <span data-ttu-id="69fc9-250">卸載繼承應用程式。</span><span class="sxs-lookup"><span data-stu-id="69fc9-250">The legacy application is uninstalled.</span></span>
-   <span data-ttu-id="69fc9-251">共用元件的參考計數會減少為零，而且會移除該元件。</span><span class="sxs-lookup"><span data-stu-id="69fc9-251">The reference count for the shared component is decremented to zero and the component is removed.</span></span>
-   <span data-ttu-id="69fc9-252">使用安裝程式的應用程式不再具有元件的存取權。</span><span class="sxs-lookup"><span data-stu-id="69fc9-252">The application using the installer no longer has access to the component.</span></span>

<span data-ttu-id="69fc9-253">若要避免此行為，請設定 **msidbComponentAttributesSharedDllRefCount**。</span><span class="sxs-lookup"><span data-stu-id="69fc9-253">To avoid this behavior, set **msidbComponentAttributesSharedDllRefCount**.</span></span>

<span data-ttu-id="69fc9-254">請注意，系統服務元件不應指定為從來源執行，而不需要特別針對這類用途所設計。</span><span class="sxs-lookup"><span data-stu-id="69fc9-254">Note that system services components should not be specified as run-from-source without being specifically designed for such use.</span></span> <span data-ttu-id="69fc9-255">如需詳細資訊，請參閱 [ServiceInstall 資料表](serviceinstall-table.md) 。</span><span class="sxs-lookup"><span data-stu-id="69fc9-255">See the [ServiceInstall table](serviceinstall-table.md) for more details.</span></span>

<span data-ttu-id="69fc9-256">請注意，對於包含進入系統資料夾的動態連結程式庫的元件，一律不應設定啟用從來源執行安裝的屬性。</span><span class="sxs-lookup"><span data-stu-id="69fc9-256">Note that attributes enabling run-from-source installation should never be set for components containing dynamic-link libraries that are going into the system folder.</span></span> <span data-ttu-id="69fc9-257">原因是，如果元件的安裝狀態變成設定為從來源執行（藉由遵循某項功能或在 UI 中設定），則在 DLL 上對 **LoadLibrary** 的後續呼叫會失敗。</span><span class="sxs-lookup"><span data-stu-id="69fc9-257">The reason is that if the installation state of the component becomes set to run-from-source by following a feature or by being set in the UI, subsequent calls to **LoadLibrary** on the DLL would fail.</span></span>

<span data-ttu-id="69fc9-258">另請參閱 [控制特徵選取狀態](controlling-feature-selection-states.md)。</span><span class="sxs-lookup"><span data-stu-id="69fc9-258">See also, [Controlling Feature Selection States](controlling-feature-selection-states.md).</span></span>

## <a name="validation"></a><span data-ttu-id="69fc9-259">驗證</span><span class="sxs-lookup"><span data-stu-id="69fc9-259">Validation</span></span>

<dl>

[<span data-ttu-id="69fc9-260">ICE02</span><span class="sxs-lookup"><span data-stu-id="69fc9-260">ICE02</span></span>](ice02.md)  
[<span data-ttu-id="69fc9-261">ICE03</span><span class="sxs-lookup"><span data-stu-id="69fc9-261">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="69fc9-262">ICE06</span><span class="sxs-lookup"><span data-stu-id="69fc9-262">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="69fc9-263">ICE07</span><span class="sxs-lookup"><span data-stu-id="69fc9-263">ICE07</span></span>](ice07.md)  
[<span data-ttu-id="69fc9-264">ICE08</span><span class="sxs-lookup"><span data-stu-id="69fc9-264">ICE08</span></span>](ice08.md)  
[<span data-ttu-id="69fc9-265">ICE09</span><span class="sxs-lookup"><span data-stu-id="69fc9-265">ICE09</span></span>](ice09.md)  
[<span data-ttu-id="69fc9-266">ICE18</span><span class="sxs-lookup"><span data-stu-id="69fc9-266">ICE18</span></span>](ice18.md)  
[<span data-ttu-id="69fc9-267">ICE19</span><span class="sxs-lookup"><span data-stu-id="69fc9-267">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="69fc9-268">ICE21</span><span class="sxs-lookup"><span data-stu-id="69fc9-268">ICE21</span></span>](ice21.md)  
[<span data-ttu-id="69fc9-269">ICE30</span><span class="sxs-lookup"><span data-stu-id="69fc9-269">ICE30</span></span>](ice30.md)  
[<span data-ttu-id="69fc9-270">ICE32</span><span class="sxs-lookup"><span data-stu-id="69fc9-270">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="69fc9-271">ICE35</span><span class="sxs-lookup"><span data-stu-id="69fc9-271">ICE35</span></span>](ice35.md)  
[<span data-ttu-id="69fc9-272">ICE38</span><span class="sxs-lookup"><span data-stu-id="69fc9-272">ICE38</span></span>](ice38.md)  
[<span data-ttu-id="69fc9-273">ICE41</span><span class="sxs-lookup"><span data-stu-id="69fc9-273">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="69fc9-274">ICE42</span><span class="sxs-lookup"><span data-stu-id="69fc9-274">ICE42</span></span>](ice42.md)  
[<span data-ttu-id="69fc9-275">ICE43</span><span class="sxs-lookup"><span data-stu-id="69fc9-275">ICE43</span></span>](ice43.md)  
[<span data-ttu-id="69fc9-276">ICE46</span><span class="sxs-lookup"><span data-stu-id="69fc9-276">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="69fc9-277">ICE50</span><span class="sxs-lookup"><span data-stu-id="69fc9-277">ICE50</span></span>](ice50.md)  
[<span data-ttu-id="69fc9-278">ICE54</span><span class="sxs-lookup"><span data-stu-id="69fc9-278">ICE54</span></span>](ice54.md)  
[<span data-ttu-id="69fc9-279">ICE57</span><span class="sxs-lookup"><span data-stu-id="69fc9-279">ICE57</span></span>](ice57.md)  
[<span data-ttu-id="69fc9-280">ICE59</span><span class="sxs-lookup"><span data-stu-id="69fc9-280">ICE59</span></span>](ice59.md)  
[<span data-ttu-id="69fc9-281">ICE62</span><span class="sxs-lookup"><span data-stu-id="69fc9-281">ICE62</span></span>](ice62.md)  
[<span data-ttu-id="69fc9-282">ICE67</span><span class="sxs-lookup"><span data-stu-id="69fc9-282">ICE67</span></span>](ice67.md)  
[<span data-ttu-id="69fc9-283">ICE76</span><span class="sxs-lookup"><span data-stu-id="69fc9-283">ICE76</span></span>](ice76.md)  
[<span data-ttu-id="69fc9-284">ICE79</span><span class="sxs-lookup"><span data-stu-id="69fc9-284">ICE79</span></span>](ice79.md)  
[<span data-ttu-id="69fc9-285">ICE80</span><span class="sxs-lookup"><span data-stu-id="69fc9-285">ICE80</span></span>](ice80.md)  
[<span data-ttu-id="69fc9-286">ICE83</span><span class="sxs-lookup"><span data-stu-id="69fc9-286">ICE83</span></span>](ice83.md)  
[<span data-ttu-id="69fc9-287">ICE86</span><span class="sxs-lookup"><span data-stu-id="69fc9-287">ICE86</span></span>](ice86.md)  
[<span data-ttu-id="69fc9-288">ICE88</span><span class="sxs-lookup"><span data-stu-id="69fc9-288">ICE88</span></span>](ice88.md)  
[<span data-ttu-id="69fc9-289">ICE91</span><span class="sxs-lookup"><span data-stu-id="69fc9-289">ICE91</span></span>](ice91.md)  
[<span data-ttu-id="69fc9-290">ICE92</span><span class="sxs-lookup"><span data-stu-id="69fc9-290">ICE92</span></span>](ice92.md)  
[<span data-ttu-id="69fc9-291">ICE97</span><span class="sxs-lookup"><span data-stu-id="69fc9-291">ICE97</span></span>](ice97.md)  
</dl>

