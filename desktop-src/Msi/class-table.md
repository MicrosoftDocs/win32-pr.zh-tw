---
description: 類別資料表包含必須在產品公告中產生的 COM 伺服器相關資訊。 每個資料列可能會產生一組登錄機碼和值。 此資料表包含相關聯的 ProgId 資訊。
ms.assetid: 0fa00a3f-2a5d-411d-9fc6-9486a600f018
title: 類別資料表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29e7584fcb0440b8754179d8e274158cc64e3b74
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106985642"
---
# <a name="class-table"></a><span data-ttu-id="59ae8-105">類別資料表</span><span class="sxs-lookup"><span data-stu-id="59ae8-105">Class Table</span></span>

<span data-ttu-id="59ae8-106">類別資料表包含必須在產品公告中產生的 COM 伺服器相關資訊。</span><span class="sxs-lookup"><span data-stu-id="59ae8-106">The Class table contains COM server-related information that must be generated as a part of the product advertisement.</span></span> <span data-ttu-id="59ae8-107">每個資料列可能會產生一組登錄機碼和值。</span><span class="sxs-lookup"><span data-stu-id="59ae8-107">Each row may generate a set of registry keys and values.</span></span> <span data-ttu-id="59ae8-108">此資料表包含相關聯的 ProgId 資訊。</span><span class="sxs-lookup"><span data-stu-id="59ae8-108">The associated ProgId information is included in this table.</span></span>

<span data-ttu-id="59ae8-109">類別資料表具有下列資料行。</span><span class="sxs-lookup"><span data-stu-id="59ae8-109">The Class table has the following columns.</span></span>



| <span data-ttu-id="59ae8-110">Column</span><span class="sxs-lookup"><span data-stu-id="59ae8-110">Column</span></span>           | <span data-ttu-id="59ae8-111">類型</span><span class="sxs-lookup"><span data-stu-id="59ae8-111">Type</span></span>                         | <span data-ttu-id="59ae8-112">答案</span><span class="sxs-lookup"><span data-stu-id="59ae8-112">Key</span></span> | <span data-ttu-id="59ae8-113">Nullable</span><span class="sxs-lookup"><span data-stu-id="59ae8-113">Nullable</span></span> |
|------------------|------------------------------|-----|----------|
| <span data-ttu-id="59ae8-114">CLSID</span><span class="sxs-lookup"><span data-stu-id="59ae8-114">CLSID</span></span>            | [<span data-ttu-id="59ae8-115">GUID</span><span class="sxs-lookup"><span data-stu-id="59ae8-115">GUID</span></span>](guid.md)             | <span data-ttu-id="59ae8-116">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-116">Y</span></span>   | <span data-ttu-id="59ae8-117">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-117">N</span></span>        |
| <span data-ttu-id="59ae8-118">Context</span><span class="sxs-lookup"><span data-stu-id="59ae8-118">Context</span></span>          | [<span data-ttu-id="59ae8-119">識別碼</span><span class="sxs-lookup"><span data-stu-id="59ae8-119">Identifier</span></span>](identifier.md) | <span data-ttu-id="59ae8-120">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-120">Y</span></span>   | <span data-ttu-id="59ae8-121">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-121">N</span></span>        |
| <span data-ttu-id="59ae8-122">元件\_</span><span class="sxs-lookup"><span data-stu-id="59ae8-122">Component\_</span></span>      | [<span data-ttu-id="59ae8-123">識別碼</span><span class="sxs-lookup"><span data-stu-id="59ae8-123">Identifier</span></span>](identifier.md) | <span data-ttu-id="59ae8-124">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-124">Y</span></span>   | <span data-ttu-id="59ae8-125">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-125">N</span></span>        |
| <span data-ttu-id="59ae8-126">ProgId \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="59ae8-126">ProgId\_Default</span></span>  | [<span data-ttu-id="59ae8-127">Text</span><span class="sxs-lookup"><span data-stu-id="59ae8-127">Text</span></span>](text.md)             | <span data-ttu-id="59ae8-128">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-128">N</span></span>   | <span data-ttu-id="59ae8-129">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-129">Y</span></span>        |
| <span data-ttu-id="59ae8-130">Description</span><span class="sxs-lookup"><span data-stu-id="59ae8-130">Description</span></span>      | [<span data-ttu-id="59ae8-131">Text</span><span class="sxs-lookup"><span data-stu-id="59ae8-131">Text</span></span>](text.md)             | <span data-ttu-id="59ae8-132">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-132">N</span></span>   | <span data-ttu-id="59ae8-133">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-133">Y</span></span>        |
| <span data-ttu-id="59ae8-134">AppId\_</span><span class="sxs-lookup"><span data-stu-id="59ae8-134">AppId\_</span></span>          | [<span data-ttu-id="59ae8-135">GUID</span><span class="sxs-lookup"><span data-stu-id="59ae8-135">GUID</span></span>](guid.md)             | <span data-ttu-id="59ae8-136">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-136">N</span></span>   | <span data-ttu-id="59ae8-137">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-137">Y</span></span>        |
| <span data-ttu-id="59ae8-138">FileTypeMask</span><span class="sxs-lookup"><span data-stu-id="59ae8-138">FileTypeMask</span></span>     | [<span data-ttu-id="59ae8-139">Text</span><span class="sxs-lookup"><span data-stu-id="59ae8-139">Text</span></span>](text.md)             | <span data-ttu-id="59ae8-140">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-140">N</span></span>   | <span data-ttu-id="59ae8-141">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-141">Y</span></span>        |
| <span data-ttu-id="59ae8-142">圖示\_</span><span class="sxs-lookup"><span data-stu-id="59ae8-142">Icon\_</span></span>           | [<span data-ttu-id="59ae8-143">識別碼</span><span class="sxs-lookup"><span data-stu-id="59ae8-143">Identifier</span></span>](identifier.md) | <span data-ttu-id="59ae8-144">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-144">N</span></span>   | <span data-ttu-id="59ae8-145">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-145">Y</span></span>        |
| <span data-ttu-id="59ae8-146">>iconindex</span><span class="sxs-lookup"><span data-stu-id="59ae8-146">IconIndex</span></span>        | [<span data-ttu-id="59ae8-147">整數</span><span class="sxs-lookup"><span data-stu-id="59ae8-147">Integer</span></span>](integer.md)       | <span data-ttu-id="59ae8-148">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-148">N</span></span>   | <span data-ttu-id="59ae8-149">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-149">Y</span></span>        |
| <span data-ttu-id="59ae8-150">DefInprocHandler</span><span class="sxs-lookup"><span data-stu-id="59ae8-150">DefInprocHandler</span></span> | [<span data-ttu-id="59ae8-151">檔案名稱</span><span class="sxs-lookup"><span data-stu-id="59ae8-151">Filename</span></span>](filename.md)     | <span data-ttu-id="59ae8-152">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-152">N</span></span>   | <span data-ttu-id="59ae8-153">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-153">Y</span></span>        |
| <span data-ttu-id="59ae8-154">引數</span><span class="sxs-lookup"><span data-stu-id="59ae8-154">Argument</span></span>         | [<span data-ttu-id="59ae8-155">格式 化</span><span class="sxs-lookup"><span data-stu-id="59ae8-155">Formatted</span></span>](formatted.md)   | <span data-ttu-id="59ae8-156">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-156">N</span></span>   | <span data-ttu-id="59ae8-157">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-157">Y</span></span>        |
| <span data-ttu-id="59ae8-158">功能\_</span><span class="sxs-lookup"><span data-stu-id="59ae8-158">Feature\_</span></span>        | [<span data-ttu-id="59ae8-159">識別碼</span><span class="sxs-lookup"><span data-stu-id="59ae8-159">Identifier</span></span>](identifier.md) | <span data-ttu-id="59ae8-160">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-160">N</span></span>   | <span data-ttu-id="59ae8-161">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-161">N</span></span>        |
| <span data-ttu-id="59ae8-162">屬性</span><span class="sxs-lookup"><span data-stu-id="59ae8-162">Attributes</span></span>       | [<span data-ttu-id="59ae8-163">整數</span><span class="sxs-lookup"><span data-stu-id="59ae8-163">Integer</span></span>](integer.md)       | <span data-ttu-id="59ae8-164">N</span><span class="sxs-lookup"><span data-stu-id="59ae8-164">N</span></span>   | <span data-ttu-id="59ae8-165">Y</span><span class="sxs-lookup"><span data-stu-id="59ae8-165">Y</span></span>        |



 

## <a name="column-information"></a><span data-ttu-id="59ae8-166">資料行資訊</span><span class="sxs-lookup"><span data-stu-id="59ae8-166">Column Information</span></span>

<dl> <dt>

<span data-ttu-id="59ae8-167"><span id="CLSID"></span><span id="clsid"></span>Clsid</span><span class="sxs-lookup"><span data-stu-id="59ae8-167"><span id="CLSID"></span><span id="clsid"></span>CLSID</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-168">COM 伺服器 (識別碼) 的類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="59ae8-168">The Class identifier (ID) of a COM server.</span></span>

</dd> <dt>

<span data-ttu-id="59ae8-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>上下文</span><span class="sxs-lookup"><span data-stu-id="59ae8-169"><span id="Context"></span><span id="context"></span><span id="CONTEXT"></span>Context</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-170">此伺服器的伺服器內容。</span><span class="sxs-lookup"><span data-stu-id="59ae8-170">The server context for this server.</span></span> <span data-ttu-id="59ae8-171">為 CLSID 索引鍵輸入下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="59ae8-171">Enter one of the following values for the CLSID Key.</span></span>



| <span data-ttu-id="59ae8-172">CLSID 金鑰</span><span class="sxs-lookup"><span data-stu-id="59ae8-172">CLSID KEY</span></span>                             | <span data-ttu-id="59ae8-173">Description</span><span class="sxs-lookup"><span data-stu-id="59ae8-173">Description</span></span>                                                               |
|---------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="59ae8-174">LocalServer</span><span class="sxs-lookup"><span data-stu-id="59ae8-174">LocalServer</span></span>](../com/localserver.md)       | <span data-ttu-id="59ae8-175">指定16位本機伺服器應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="59ae8-175">Specifies the full path to a 16-bit local server application.</span></span>             |
| [<span data-ttu-id="59ae8-176">LocalServer32</span><span class="sxs-lookup"><span data-stu-id="59ae8-176">LocalServer32</span></span>](../com/localserver32.md)   | <span data-ttu-id="59ae8-177">指定32位本機伺服器應用程式的完整路徑。</span><span class="sxs-lookup"><span data-stu-id="59ae8-177">Specifies the full path to a 32-bit local server application.</span></span>             |
| [<span data-ttu-id="59ae8-178">InprocServer</span><span class="sxs-lookup"><span data-stu-id="59ae8-178">InprocServer</span></span>](../com/inprocserver.md)     | <span data-ttu-id="59ae8-179">指定同進程伺服器 DLL 的路徑。</span><span class="sxs-lookup"><span data-stu-id="59ae8-179">Specifies the path to an in-process server DLL.</span></span>                           |
| [<span data-ttu-id="59ae8-180">InprocServer32</span><span class="sxs-lookup"><span data-stu-id="59ae8-180">InprocServer32</span></span>](../com/inprocserver32.md) | <span data-ttu-id="59ae8-181">指定32位同進程伺服器和執行緒模型的路徑。</span><span class="sxs-lookup"><span data-stu-id="59ae8-181">Specifies the path to a 32-bit in-process server and the threading model.</span></span> |



 

</dd> <dt>

<span data-ttu-id="59ae8-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>元件\_</span><span class="sxs-lookup"><span data-stu-id="59ae8-182"><span id="Component_"></span><span id="component_"></span><span id="COMPONENT_"></span>Component\_</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-183">在 [元件資料表](component-table.md) 中，指定金鑰檔提供 COM 伺服器的元件的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="59ae8-183">External key into the [Component table](component-table.md) specifying the component whose key file provides the COM server.</span></span>

</dd> <dt>

<span data-ttu-id="59ae8-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId \_ 預設值</span><span class="sxs-lookup"><span data-stu-id="59ae8-184"><span id="ProgId_Default"></span><span id="progid_default"></span><span id="PROGID_DEFAULT"></span>ProgId\_Default</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-185">與此類別識別碼相關聯的預設程式識別碼。</span><span class="sxs-lookup"><span data-stu-id="59ae8-185">The default Program ID associated with this Class ID.</span></span> <span data-ttu-id="59ae8-186">此資料行是 [ProgID 資料表](progid-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="59ae8-186">This column is a foreign key into the [ProgID table](progid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="59ae8-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>描述</span><span class="sxs-lookup"><span data-stu-id="59ae8-187"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>Description</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-188">與類別識別碼和程式識別碼相關聯的當地語系化描述。</span><span class="sxs-lookup"><span data-stu-id="59ae8-188">Localized description associated with the Class ID and Program ID.</span></span>

</dd> <dt>

<span data-ttu-id="59ae8-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span><span class="sxs-lookup"><span data-stu-id="59ae8-189"><span id="AppId_"></span><span id="appid_"></span><span id="APPID_"></span>AppId\_</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-190">應用程式識別碼包含相關聯之應用程式的 DCOM 資訊 (字串 [GUID](guid.md)) 。</span><span class="sxs-lookup"><span data-stu-id="59ae8-190">Application ID containing DCOM information for the associated application (string [GUID](guid.md)).</span></span> <span data-ttu-id="59ae8-191">此資料行是 [AppId 資料表](appid-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="59ae8-191">This column is a foreign key into the [AppId table](appid-table.md).</span></span>

</dd> <dt>

<span data-ttu-id="59ae8-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span><span class="sxs-lookup"><span data-stu-id="59ae8-192"><span id="FileTypeMask"></span><span id="filetypemask"></span><span id="FILETYPEMASK"></span>FileTypeMask</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-193">包含此 CLSID) 機碼 (的 HKCR 資訊。</span><span class="sxs-lookup"><span data-stu-id="59ae8-193">Contains information for the HKCR (this CLSID) key.</span></span>

<span data-ttu-id="59ae8-194">如果有多個模式，則必須以分號分隔，而且會產生數位子機碼：0、1、2 .。。如需此功能的詳細資訊，請參閱 [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile)。</span><span class="sxs-lookup"><span data-stu-id="59ae8-194">If multiple patterns exist, they must be delimited by a semicolon, and numeric subkeys are generated: 0, 1, 2... For more information about this functionality, see [**GetClassFile**](/windows/win32/api/objbase/nf-objbase-getclassfile).</span></span>

</dd> <dt>

<span data-ttu-id="59ae8-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>圖示\_</span><span class="sxs-lookup"><span data-stu-id="59ae8-195"><span id="Icon_"></span><span id="icon_"></span><span id="ICON_"></span>Icon\_</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-196">提供與此 CLSID 相關聯之圖示的檔案。</span><span class="sxs-lookup"><span data-stu-id="59ae8-196">The file providing the icon associated with this CLSID.</span></span> <span data-ttu-id="59ae8-197">安裝程式會將此資料行中的專案寫入與 ProgId 相關聯的 DefaultIcon 索引鍵下。</span><span class="sxs-lookup"><span data-stu-id="59ae8-197">The installer writes the entry in this column under the DefaultIcon key associated with the ProgId.</span></span> <span data-ttu-id="59ae8-198">如果它不是 null，則資料行是 [圖示資料表](icon-table.md)中的外鍵。</span><span class="sxs-lookup"><span data-stu-id="59ae8-198">If it is not null, the column is a foreign key into the [Icon table](icon-table.md).</span></span> <span data-ttu-id="59ae8-199">如果是 null，COM 伺服器會提供圖示資源。</span><span class="sxs-lookup"><span data-stu-id="59ae8-199">If it is null, the COM server provides the icon resource.</span></span> <span data-ttu-id="59ae8-200">宣告的檔案關聯和快捷方式需要此資料行中的非 null 值，才能正確顯示。</span><span class="sxs-lookup"><span data-stu-id="59ae8-200">Advertised file associations and shortcuts require a non-null value in this column to display properly.</span></span>

</dd> <dt>

<span data-ttu-id="59ae8-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>>iconindex</span><span class="sxs-lookup"><span data-stu-id="59ae8-201"><span id="IconIndex"></span><span id="iconindex"></span><span id="ICONINDEX"></span>IconIndex</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-202">圖示檔中的圖示索引。</span><span class="sxs-lookup"><span data-stu-id="59ae8-202">Icon index into the icon file.</span></span> <span data-ttu-id="59ae8-203">這個可以是 null。</span><span class="sxs-lookup"><span data-stu-id="59ae8-203">This can be null.</span></span>

<span data-ttu-id="59ae8-204">僅限非負數位。</span><span class="sxs-lookup"><span data-stu-id="59ae8-204">Non-negative numbers only.</span></span>

</dd> <dt>

<span data-ttu-id="59ae8-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span><span class="sxs-lookup"><span data-stu-id="59ae8-205"><span id="DefInprocHandler"></span><span id="definprochandler"></span><span id="DEFINPROCHANDLER"></span>DefInprocHandler</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-206">這個欄位會針對內容欄位中指定的伺服器內容，指定預設的同進程處理常式。</span><span class="sxs-lookup"><span data-stu-id="59ae8-206">This field specifies the default in-process handler for the server context specified in the Context field.</span></span>

<span data-ttu-id="59ae8-207">如果內容欄位中出現 InprocServer 或 InprocServer CLSID 索引鍵，則這個欄位必須是 Null。</span><span class="sxs-lookup"><span data-stu-id="59ae8-207">This field must be Null if an InprocServer or InprocServer CLSID key appears in the Context field.</span></span>

<span data-ttu-id="59ae8-208">如果 LocalServer 或 LocalServer32 CLSID 索引鍵出現在內容欄位中，則 [DefInprocHandler] 欄位中的值會識別預設的同進程處理常式。</span><span class="sxs-lookup"><span data-stu-id="59ae8-208">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the value in the DefInprocHandler field identifies the default in-process handler.</span></span>



| <span data-ttu-id="59ae8-209">值</span><span class="sxs-lookup"><span data-stu-id="59ae8-209">Value</span></span>                | <span data-ttu-id="59ae8-210">描述</span><span class="sxs-lookup"><span data-stu-id="59ae8-210">Description</span></span>                                                                                                                                                                                                                                                                       |
|----------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="59ae8-211">非數值</span><span class="sxs-lookup"><span data-stu-id="59ae8-211">non-numeric value</span></span>    | <span data-ttu-id="59ae8-212">安裝程式會將 DefInprocHandler 欄位中的非數值視為系統檔案，做為 InprocHandler32 索引鍵所指定的32位同進程處理常式。</span><span class="sxs-lookup"><span data-stu-id="59ae8-212">The installer treats a non-numeric value in the DefInprocHandler field as a system file serving as the 32-bit in-process handler specified by the InprocHandler32 key.</span></span>                                                                                                            |
| <span data-ttu-id="59ae8-213">Null</span><span class="sxs-lookup"><span data-stu-id="59ae8-213">Null</span></span>                 | <span data-ttu-id="59ae8-214">LocalServer 或 LocalServer32 CLSID 索引鍵的 DefInprocHandler 和引數欄位都可以是 Null。</span><span class="sxs-lookup"><span data-stu-id="59ae8-214">The DefInprocHandler and Argument fields can both be Null for a LocalServer or LocalServer32 CLSID key.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="59ae8-215">1 = 預設 (系統) </span><span class="sxs-lookup"><span data-stu-id="59ae8-215">1 = default (system)</span></span> | <span data-ttu-id="59ae8-216">預設值是 InprocHandler 所指定的16位同進程處理常式。</span><span class="sxs-lookup"><span data-stu-id="59ae8-216">The default is the 16-bit in-process handler specified by InprocHandler.</span></span> <span data-ttu-id="59ae8-217">在這種情況下，InprocHandler 的值就是登錄中預設儲存同進程處理常式值的名稱。</span><span class="sxs-lookup"><span data-stu-id="59ae8-217">In this case, the value of InprocHandler is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="59ae8-218">例如，HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID。</span><span class="sxs-lookup"><span data-stu-id="59ae8-218">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span>     |
| <span data-ttu-id="59ae8-219">2 = 預設 (系統) </span><span class="sxs-lookup"><span data-stu-id="59ae8-219">2 = default (system)</span></span> | <span data-ttu-id="59ae8-220">預設值是 InprocHandler32 所指定的32位同進程處理常式。</span><span class="sxs-lookup"><span data-stu-id="59ae8-220">The default is the 32-bit in-process handler specified by InprocHandler32.</span></span> <span data-ttu-id="59ae8-221">在這種情況下，InprocHandler32 的值就是登錄中預設儲存同進程處理常式值的名稱。</span><span class="sxs-lookup"><span data-stu-id="59ae8-221">In this case, the value of InprocHandler32 is the name in the registry under which the value of the default in-process handler is stored.</span></span> <span data-ttu-id="59ae8-222">例如，HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ 類別 \\ CLSID。</span><span class="sxs-lookup"><span data-stu-id="59ae8-222">For example, HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Classes\\CLSID.</span></span> |
| <span data-ttu-id="59ae8-223">3 = 預設 (系統) </span><span class="sxs-lookup"><span data-stu-id="59ae8-223">3 = default (system)</span></span> | <span data-ttu-id="59ae8-224">預設值為16位或32位的同進程處理常式。</span><span class="sxs-lookup"><span data-stu-id="59ae8-224">The default is a 16-bit or 32-bit in-process handler.</span></span>                                                                                                                                                                                                                             |



 

</dd> <dt>

<span data-ttu-id="59ae8-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>參數</span><span class="sxs-lookup"><span data-stu-id="59ae8-225"><span id="Argument"></span><span id="argument"></span><span id="ARGUMENT"></span>Argument</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-226">如果 LocalServer 或 LocalServer32 CLSID 索引鍵出現在內容欄位中，則此欄位中的文字會註冊為伺服器的引數，並由 COM 用來叫用伺服器。</span><span class="sxs-lookup"><span data-stu-id="59ae8-226">If a LocalServer or LocalServer32 CLSID key appears in the Context field, the text in this field is registered as the argument against the server and is used by COM to invoke the server.</span></span> <span data-ttu-id="59ae8-227">如果內容欄位中出現 LocalServer 或 LocalServer32，DefInprocHandler 和 Argument 欄位都可以是 Null。</span><span class="sxs-lookup"><span data-stu-id="59ae8-227">The DefInprocHandler and Argument fields can both be Null if LocalServer or LocalServer32 appears in the Context field.</span></span>

<span data-ttu-id="59ae8-228">請注意，[引數] 欄位中的屬性解析有限。</span><span class="sxs-lookup"><span data-stu-id="59ae8-228">Note that the resolution of properties in the Argument field is limited.</span></span> <span data-ttu-id="59ae8-229">\[ \] 當安裝擁有類別的元件時，如果屬性已經有預期的值，則只能解析此欄位中格式化為屬性的屬性。</span><span class="sxs-lookup"><span data-stu-id="59ae8-229">A property formatted as \[Property\] in this field can only be resolved if the property already has the intended value when the component owning the class is installed.</span></span> <span data-ttu-id="59ae8-230">例如，若要將引數 " \[ \#MyDoc.doc\] " 解析為正確的值，則相同的進程必須安裝 MyDoc.doc 和擁有該類別的元件。</span><span class="sxs-lookup"><span data-stu-id="59ae8-230">For example, for the argument "\[\#MyDoc.doc\]" to resolve to the correct value, the same process must be installing the file MyDoc.doc and the component that owns the class.</span></span>

</dd> <dt>

<span data-ttu-id="59ae8-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>特徵\_</span><span class="sxs-lookup"><span data-stu-id="59ae8-231"><span id="Feature_"></span><span id="feature_"></span><span id="FEATURE_"></span>Feature\_</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-232">[功能資料表](feature-table.md)中的外部索引鍵，指定提供 COM 伺服器的功能。</span><span class="sxs-lookup"><span data-stu-id="59ae8-232">External key into the [Feature table](feature-table.md) specifying the feature that provides the COM server.</span></span>

<span data-ttu-id="59ae8-233">功能資料表的第一個資料行的外部索引鍵。</span><span class="sxs-lookup"><span data-stu-id="59ae8-233">External key to column one of the Feature table.</span></span>

</dd> <dt>

<span data-ttu-id="59ae8-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>屬性</span><span class="sxs-lookup"><span data-stu-id="59ae8-234"><span id="Attributes"></span><span id="attributes"></span><span id="ATTRIBUTES"></span>Attributes</span></span>
</dt> <dd>

<span data-ttu-id="59ae8-235">如果在此資料行中設定了 **msidbClassAttributesRelativePath** ，則完整檔案名可以用於 COM 伺服器。</span><span class="sxs-lookup"><span data-stu-id="59ae8-235">If **msidbClassAttributesRelativePath** is set in this column, the bare file name can be used for COM servers.</span></span> <span data-ttu-id="59ae8-236">安裝程式只會註冊檔案名，而不是完整的路徑。</span><span class="sxs-lookup"><span data-stu-id="59ae8-236">The installer registers the file name only instead of the complete path.</span></span> <span data-ttu-id="59ae8-237">這可讓目前目錄中的伺服器優先採用，並允許相同元件的多個複本。</span><span class="sxs-lookup"><span data-stu-id="59ae8-237">This enables the server in the current directory to take precedence and allows multiple copies of the same component.</span></span>



| <span data-ttu-id="59ae8-238">屬性</span><span class="sxs-lookup"><span data-stu-id="59ae8-238">Attribute</span></span>                            | <span data-ttu-id="59ae8-239">Decimal</span><span class="sxs-lookup"><span data-stu-id="59ae8-239">Decimal</span></span> | <span data-ttu-id="59ae8-240">十六進位</span><span class="sxs-lookup"><span data-stu-id="59ae8-240">Hexadecimal</span></span> |
|--------------------------------------|---------|-------------|
| <span data-ttu-id="59ae8-241">**msidbClassAttributesRelativePath**</span><span class="sxs-lookup"><span data-stu-id="59ae8-241">**msidbClassAttributesRelativePath**</span></span> | <span data-ttu-id="59ae8-242">1</span><span class="sxs-lookup"><span data-stu-id="59ae8-242">1</span></span>       | <span data-ttu-id="59ae8-243">0x001</span><span class="sxs-lookup"><span data-stu-id="59ae8-243">0x001</span></span>       |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="59ae8-244">備註</span><span class="sxs-lookup"><span data-stu-id="59ae8-244">Remarks</span></span>

<span data-ttu-id="59ae8-245">當執行 [RegisterClassInfo 動作](registerclassinfo-action.md) 或 [UnregisterClassInfo 動作](unregisterclassinfo-action.md) 時，就會參考此資料表。</span><span class="sxs-lookup"><span data-stu-id="59ae8-245">This table is referred to when the [RegisterClassInfo action](registerclassinfo-action.md) or the [UnregisterClassInfo action](unregisterclassinfo-action.md) are executed.</span></span>

## <a name="validation"></a><span data-ttu-id="59ae8-246">驗證</span><span class="sxs-lookup"><span data-stu-id="59ae8-246">Validation</span></span>

<dl>

[<span data-ttu-id="59ae8-247">ICE03</span><span class="sxs-lookup"><span data-stu-id="59ae8-247">ICE03</span></span>](ice03.md)  
[<span data-ttu-id="59ae8-248">ICE06</span><span class="sxs-lookup"><span data-stu-id="59ae8-248">ICE06</span></span>](ice06.md)  
[<span data-ttu-id="59ae8-249">ICE19</span><span class="sxs-lookup"><span data-stu-id="59ae8-249">ICE19</span></span>](ice19.md)  
[<span data-ttu-id="59ae8-250">ICE32</span><span class="sxs-lookup"><span data-stu-id="59ae8-250">ICE32</span></span>](ice32.md)  
[<span data-ttu-id="59ae8-251">ICE36</span><span class="sxs-lookup"><span data-stu-id="59ae8-251">ICE36</span></span>](ice36.md)  
[<span data-ttu-id="59ae8-252">ICE41</span><span class="sxs-lookup"><span data-stu-id="59ae8-252">ICE41</span></span>](ice41.md)  
[<span data-ttu-id="59ae8-253">ICE42</span><span class="sxs-lookup"><span data-stu-id="59ae8-253">ICE42</span></span>](ice42.md)  
[<span data-ttu-id="59ae8-254">ICE46</span><span class="sxs-lookup"><span data-stu-id="59ae8-254">ICE46</span></span>](ice46.md)  
[<span data-ttu-id="59ae8-255">ICE66</span><span class="sxs-lookup"><span data-stu-id="59ae8-255">ICE66</span></span>](ice66.md)  
[<span data-ttu-id="59ae8-256">ICE69</span><span class="sxs-lookup"><span data-stu-id="59ae8-256">ICE69</span></span>](ice69.md)  
</dl>

 

 
