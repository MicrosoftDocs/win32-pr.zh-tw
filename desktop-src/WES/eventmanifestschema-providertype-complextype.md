---
title: ProviderType 複雜類型
description: 定義提供者及其用來定義其事件的中繼資料。 |ProviderType 複雜類型
ms.assetid: 70199cf5-a6d0-4780-9ff1-ed083a5b49ac
keywords:
- ProviderType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- ProviderType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c258b3ff48cdd2f00f632fdce770b58182a531c7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104322324"
---
# <a name="providertype-complex-type"></a><span data-ttu-id="a9750-105">ProviderType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="a9750-105">ProviderType Complex Type</span></span>

<span data-ttu-id="a9750-106">定義提供者及其用來定義其事件的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="a9750-106">Defines a provider and the metadata that it uses to define its events.</span></span>

``` syntax
<xs:complexType name="ProviderType">
    <xs:choice
        minOccurs="0"
        maxOccurs="unbounded"
    >
        <xs:element name="channels"
            type="ChannelListType"
         />
        <xs:element name="levels"
            type="LevelListType"
         />
        <xs:element name="tasks"
            type="TaskListType"
         />
        <xs:element name="opcodes"
            type="OpcodeListType"
         />
        <xs:element name="keywords"
            type="KeywordListType"
         />
        <xs:element name="maps"
            type="MapType"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
         />
        <xs:element name="templates"
            type="TemplateListType"
         />
        <xs:element name="events"
            type="DefinitionType"
         />
        <xs:element name="filters"
            type="FilterListType"
         />
        <xs:any
            processContents="lax"
            namespace="##other"
         />
    </xs:choice>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:attribute name="guid"
        type="GUIDType"
        use="required"
     />
    <xs:attribute name="resourceFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="messageFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="parameterFileName"
        type="filePath"
        use="optional"
     />
    <xs:attribute name="helpLink"
        type="anyURI"
        use="optional"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="required"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:attribute name="source"
        use="optional"
        default="Xml"
    >
        <xs:simpleType>
            <xs:restriction
                base="xs:string"
            >
                <xs:enumeration
                    value="Xml"
                 />
                <xs:enumeration
                    value="Wbem"
                 />
            </xs:restriction>
        </xs:simpleType>
    </xs:attribute>
    <xs:attribute name="warnOnApplicationCompatibilityError"
        type="xs:boolean"
        use="optional"
        default="false"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a9750-107">子元素</span><span class="sxs-lookup"><span data-stu-id="a9750-107">Child elements</span></span>



| <span data-ttu-id="a9750-108">元素</span><span class="sxs-lookup"><span data-stu-id="a9750-108">Element</span></span>                                                                       | <span data-ttu-id="a9750-109">類型</span><span class="sxs-lookup"><span data-stu-id="a9750-109">Type</span></span>                                                                         | <span data-ttu-id="a9750-110">Description</span><span class="sxs-lookup"><span data-stu-id="a9750-110">Description</span></span>                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a9750-111">**管道**</span><span class="sxs-lookup"><span data-stu-id="a9750-111">**channels**</span></span>](eventmanifestschema-channels-providertype-element.md)         | [<span data-ttu-id="a9750-112">**ChannelListType**</span><span class="sxs-lookup"><span data-stu-id="a9750-112">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md)   | <span data-ttu-id="a9750-113">定義提供者可以記錄事件的通道清單。</span><span class="sxs-lookup"><span data-stu-id="a9750-113">Defines a list of channels to which providers can log events.</span></span><br/>                                                                                                                                                                                      |
| [<span data-ttu-id="a9750-114">**事件**</span><span class="sxs-lookup"><span data-stu-id="a9750-114">**events**</span></span>](eventmanifestschema-events-providertype-element.md)             | [<span data-ttu-id="a9750-115">**DefinitionType**</span><span class="sxs-lookup"><span data-stu-id="a9750-115">**DefinitionType**</span></span>](eventmanifestschema-definitiontype-complextype.md)     | <span data-ttu-id="a9750-116">定義提供者可以記錄之事件的事件定義清單。</span><span class="sxs-lookup"><span data-stu-id="a9750-116">Defines a list of event definitions of the events that the provider can log.</span></span><br/>                                                                                                                                                                       |
| <span data-ttu-id="a9750-117">**過濾 器**</span><span class="sxs-lookup"><span data-stu-id="a9750-117">**filters**</span></span>                                                                   | [<span data-ttu-id="a9750-118">**FilterListType**</span><span class="sxs-lookup"><span data-stu-id="a9750-118">**FilterListType**</span></span>](eventmanifestschema-filterlisttype-complextype.md)     | <span data-ttu-id="a9750-119">定義提供者所支援的篩選器清單。</span><span class="sxs-lookup"><span data-stu-id="a9750-119">Defines a list of filters that your provider supports.</span></span> <span data-ttu-id="a9750-120">您可以使用篩選準則（如同您對層級和關鍵字）來判斷是否要撰寫事件。</span><span class="sxs-lookup"><span data-stu-id="a9750-120">You can use the filters, as you would level and keywords, to determine if you want to write an event.</span></span> <br/> <span data-ttu-id="a9750-121">**Windows Server 2008 和 Windows Vista：** 在 Windows 7 之前不受支援。</span><span class="sxs-lookup"><span data-stu-id="a9750-121">**Windows Server 2008 and Windows Vista:** Not supported until Windows 7.</span></span><br/> |
| [<span data-ttu-id="a9750-122">**關鍵 字**</span><span class="sxs-lookup"><span data-stu-id="a9750-122">**keywords**</span></span>](eventmanifestschema-keywords-providertype-element.md)         | [<span data-ttu-id="a9750-123">**KeywordListType**</span><span class="sxs-lookup"><span data-stu-id="a9750-123">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md)   | <span data-ttu-id="a9750-124">定義分類事件的關鍵字清單。</span><span class="sxs-lookup"><span data-stu-id="a9750-124">Defines a list of keywords that categorize events.</span></span><br/>                                                                                                                                                                                                 |
| [<span data-ttu-id="a9750-125">**水準**</span><span class="sxs-lookup"><span data-stu-id="a9750-125">**levels**</span></span>](eventmanifestschema-levels-providertype-element.md)             | [<span data-ttu-id="a9750-126">**LevelListType**</span><span class="sxs-lookup"><span data-stu-id="a9750-126">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)       | <span data-ttu-id="a9750-127">定義指定事件嚴重性的層級清單。</span><span class="sxs-lookup"><span data-stu-id="a9750-127">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="a9750-128">**地圖**</span><span class="sxs-lookup"><span data-stu-id="a9750-128">**maps**</span></span>](eventmanifestschema-maps-providertype-element.md)                 | [<span data-ttu-id="a9750-129">**MapType**</span><span class="sxs-lookup"><span data-stu-id="a9750-129">**MapType**</span></span>](eventmanifestschema-maptype-complextype.md)                   | <span data-ttu-id="a9750-130">定義名稱/值組的清單，您可以在資訊清單的範本區段中參考。</span><span class="sxs-lookup"><span data-stu-id="a9750-130">Defines a list of name/value pairs that you can reference in the template section of the manifest.</span></span><br/>                                                                                                                                                 |
| [<span data-ttu-id="a9750-131">**namedQueries**</span><span class="sxs-lookup"><span data-stu-id="a9750-131">**namedQueries**</span></span>](eventmanifestschema-namedqueries-providertype-element.md) | [<span data-ttu-id="a9750-132">**NamedQueryType**</span><span class="sxs-lookup"><span data-stu-id="a9750-132">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)     | <span data-ttu-id="a9750-133">未使用。</span><span class="sxs-lookup"><span data-stu-id="a9750-133">Not used.</span></span> <span data-ttu-id="a9750-134">定義已命名查詢的清單，這些查詢會查詢事件訊息字串中的值，並執行指定的動作（如果找到的話）。</span><span class="sxs-lookup"><span data-stu-id="a9750-134">Defines a list of named queries that query the event message string for a value and perform a specified action if found.</span></span><br/>                                                                                                                 |
| [<span data-ttu-id="a9750-135">**碼**</span><span class="sxs-lookup"><span data-stu-id="a9750-135">**opcodes**</span></span>](eventmanifestschema-opcodes-providertype-element.md)           | [<span data-ttu-id="a9750-136">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="a9750-136">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)     | <span data-ttu-id="a9750-137">定義可用於將工作中的事件群組在一起的作業碼清單。</span><span class="sxs-lookup"><span data-stu-id="a9750-137">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                                                                                                                          |
| [<span data-ttu-id="a9750-138">**任務**</span><span class="sxs-lookup"><span data-stu-id="a9750-138">**tasks**</span></span>](eventmanifestschema-tasks-providertype-element.md)               | [<span data-ttu-id="a9750-139">**TaskListType**</span><span class="sxs-lookup"><span data-stu-id="a9750-139">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)         | <span data-ttu-id="a9750-140">定義提供者可用來群組事件的工作清單。</span><span class="sxs-lookup"><span data-stu-id="a9750-140">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="a9750-141">一般而言，您會使用工作將提供者的功能或元件的事件分組。</span><span class="sxs-lookup"><span data-stu-id="a9750-141">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/>                                                                                              |
| [<span data-ttu-id="a9750-142">**範本**</span><span class="sxs-lookup"><span data-stu-id="a9750-142">**templates**</span></span>](eventmanifestschema-templates-providertype-element.md)       | [<span data-ttu-id="a9750-143">**TemplateListType**</span><span class="sxs-lookup"><span data-stu-id="a9750-143">**TemplateListType**</span></span>](eventmanifestschema-templatelisttype-complextype.md) | <span data-ttu-id="a9750-144">定義範本清單，以指定要包含在事件中的資料。</span><span class="sxs-lookup"><span data-stu-id="a9750-144">Defines a list of templates that specify the data to include with the events.</span></span><br/>                                                                                                                                                                      |



## <a name="attributes"></a><span data-ttu-id="a9750-145">屬性</span><span class="sxs-lookup"><span data-stu-id="a9750-145">Attributes</span></span>



| <span data-ttu-id="a9750-146">名稱</span><span class="sxs-lookup"><span data-stu-id="a9750-146">Name</span></span>                                | <span data-ttu-id="a9750-147">類型</span><span class="sxs-lookup"><span data-stu-id="a9750-147">Type</span></span>                                                              | <span data-ttu-id="a9750-148">Description</span><span class="sxs-lookup"><span data-stu-id="a9750-148">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|-------------------------------------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a9750-149">guid</span><span class="sxs-lookup"><span data-stu-id="a9750-149">guid</span></span>                                | [<span data-ttu-id="a9750-150">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="a9750-150">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="a9750-151">可唯一識別提供者的 GUID。</span><span class="sxs-lookup"><span data-stu-id="a9750-151">A GUID that uniquely identifies the provider.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
| <span data-ttu-id="a9750-152">helpLink</span><span class="sxs-lookup"><span data-stu-id="a9750-152">helpLink</span></span>                            | <span data-ttu-id="a9750-153">anyURI</span><span class="sxs-lookup"><span data-stu-id="a9750-153">anyURI</span></span>                                                            | <span data-ttu-id="a9750-154">提供提供者所引發事件相關資訊的內容 URL 或 MS 說明連結。</span><span class="sxs-lookup"><span data-stu-id="a9750-154">The URL or MS help link to content that provides information about the events that the provider raises.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a9750-155">message</span><span class="sxs-lookup"><span data-stu-id="a9750-155">message</span></span>                             | [<span data-ttu-id="a9750-156">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="a9750-156">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="a9750-157">提供者的當地語系化顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a9750-157">The localized display name for the provider.</span></span> <span data-ttu-id="a9750-158">訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="a9750-158">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a9750-159">messageFileName</span><span class="sxs-lookup"><span data-stu-id="a9750-159">messageFileName</span></span>                     | [<span data-ttu-id="a9750-160">**filePath**</span><span class="sxs-lookup"><span data-stu-id="a9750-160">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="a9750-161">檔案的完整路徑，該檔案包含提供者的當地語系化訊息資源。</span><span class="sxs-lookup"><span data-stu-id="a9750-161">The full path to the file that contains the provider's localized message resources.</span></span> <span data-ttu-id="a9750-162">檔案可以是可執行檔或 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="a9750-162">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a9750-163">NAME</span><span class="sxs-lookup"><span data-stu-id="a9750-163">name</span></span>                                | <span data-ttu-id="a9750-164">anyURI</span><span class="sxs-lookup"><span data-stu-id="a9750-164">anyURI</span></span>                                                            | <span data-ttu-id="a9750-165">提供者的名稱。</span><span class="sxs-lookup"><span data-stu-id="a9750-165">The name of the provider.</span></span> <span data-ttu-id="a9750-166">名稱的格式應為 *Company* - *Product* - *Component*。</span><span class="sxs-lookup"><span data-stu-id="a9750-166">The name should be of the form, *Company*-*Product*-*Component*.</span></span><br/> <span data-ttu-id="a9750-167">名稱不能超過255個字元，且不能包含下列字元： ' > '、' < '、' & '、' "'、' \| '、' \\ '、'： '、' '、'？ '、' \* '，或代碼小於31的字元。</span><span class="sxs-lookup"><span data-stu-id="a9750-167">The name cannot be longer than 255 characters, and cannot contain the characters: '>', '<', '&', '"', '\|', '\\', ':', '', '?', '\*', or characters with codes less than 31.</span></span> <span data-ttu-id="a9750-168">此外，名稱必須遵循檔案和登錄機碼名稱的一般條件約束。</span><span class="sxs-lookup"><span data-stu-id="a9750-168">In addition, the name must follow the general constraints on file and registry key names.</span></span> <span data-ttu-id="a9750-169">您可以在 [命名](/windows/desktop/FileIO/naming-a-file)檔案和登錄專案 [大小限制](/windows/desktop/SysInfo/registry-element-size-limits)中找到這些條件約束。</span><span class="sxs-lookup"><span data-stu-id="a9750-169">These constraints can be found at [Naming a File](/windows/desktop/FileIO/naming-a-file), and [Registry Element Size Limits](/windows/desktop/SysInfo/registry-element-size-limits).</span></span><br/> |
| <span data-ttu-id="a9750-170">parameterFileName</span><span class="sxs-lookup"><span data-stu-id="a9750-170">parameterFileName</span></span>                   | [<span data-ttu-id="a9750-171">**filePath**</span><span class="sxs-lookup"><span data-stu-id="a9750-171">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="a9750-172">檔案的完整路徑，該檔案包含提供者的參數字串資源。</span><span class="sxs-lookup"><span data-stu-id="a9750-172">The full path to the file that contain the provider's parameter string resources.</span></span> <span data-ttu-id="a9750-173">檔案可以是可執行檔或 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="a9750-173">The file can be an executable file or DLL file.</span></span> <span data-ttu-id="a9750-174">您可以指定一個以上的參數檔案，並以分號分隔。</span><span class="sxs-lookup"><span data-stu-id="a9750-174">You can specify more than one parameter file separated by a semicolon.</span></span> <span data-ttu-id="a9750-175">當事件的訊息字串包含參數字串時，會搜尋該檔案。</span><span class="sxs-lookup"><span data-stu-id="a9750-175">The file is searched when an event's message string contains a parameter string.</span></span> <span data-ttu-id="a9750-176">參數可讓您提供可當地語系化的插入字串。</span><span class="sxs-lookup"><span data-stu-id="a9750-176">Parameters let you provide localizable insert strings.</span></span> <span data-ttu-id="a9750-177">如需詳細資訊，請參閱「備註」。</span><span class="sxs-lookup"><span data-stu-id="a9750-177">See Remarks for more information.</span></span><br/>                                                                                                                                                |
| <span data-ttu-id="a9750-178">resourceFileName</span><span class="sxs-lookup"><span data-stu-id="a9750-178">resourceFileName</span></span>                    | [<span data-ttu-id="a9750-179">**filePath**</span><span class="sxs-lookup"><span data-stu-id="a9750-179">**filePath**</span></span>](eventmanifestschema-filepath-simpletype.md)       | <span data-ttu-id="a9750-180">檔案的完整路徑，該檔案包含提供者的中繼資料資源。</span><span class="sxs-lookup"><span data-stu-id="a9750-180">The full path to the file that contains the provider's metadata resources.</span></span> <span data-ttu-id="a9750-181">檔案可以是可執行檔或 DLL 檔案。</span><span class="sxs-lookup"><span data-stu-id="a9750-181">The file can be an executable file or DLL file.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span data-ttu-id="a9750-182">source</span><span class="sxs-lookup"><span data-stu-id="a9750-182">source</span></span>                              |                                                                   | <span data-ttu-id="a9750-183">僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="a9750-183">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span data-ttu-id="a9750-184">符號</span><span class="sxs-lookup"><span data-stu-id="a9750-184">symbol</span></span>                              | [<span data-ttu-id="a9750-185">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="a9750-185">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="a9750-186">用來參考應用程式中提供者 GUID 的符號。</span><span class="sxs-lookup"><span data-stu-id="a9750-186">The symbol to use to reference the provider's GUID in your application.</span></span> <span data-ttu-id="a9750-187">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中，為提供者的 GUID 建立常數。</span><span class="sxs-lookup"><span data-stu-id="a9750-187">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the provider's GUID in the header file that the compiler generates.</span></span><br/>                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="a9750-188">warnOnApplicationCompatibilityError</span><span class="sxs-lookup"><span data-stu-id="a9750-188">warnOnApplicationCompatibilityError</span></span> | <span data-ttu-id="a9750-189">**xs:boolean**</span><span class="sxs-lookup"><span data-stu-id="a9750-189">**xs:boolean**</span></span>                                                    | <span data-ttu-id="a9750-190">僅供內部使用。</span><span class="sxs-lookup"><span data-stu-id="a9750-190">For internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |



## <a name="remarks"></a><span data-ttu-id="a9750-191">備註</span><span class="sxs-lookup"><span data-stu-id="a9750-191">Remarks</span></span>

<span data-ttu-id="a9750-192">Windows 事件檢視器 (Eventvwr.exe) 會使用當地語系化的訊息字串（如果有的話）：否則，它會使用 name 屬性中的字串。</span><span class="sxs-lookup"><span data-stu-id="a9750-192">The Windows Event Viewer (Eventvwr.exe) will use the localized message string if available; otherwise, it uses the string from the name attribute.</span></span>

<span data-ttu-id="a9750-193">ResourceFileName、messageFileName 和 parameterFileName 的路徑可以包含環境變數。</span><span class="sxs-lookup"><span data-stu-id="a9750-193">The paths for resourceFileName, messageFileName, and parameterFileName can contain environment variables.</span></span> <span data-ttu-id="a9750-194">如果您定義要在路徑中使用的新環境變數，則必須重新開機電腦，事件記錄檔服務才能挑選新的變數;否則，服務將無法找到您的提供者資源。</span><span class="sxs-lookup"><span data-stu-id="a9750-194">If you define a new environment variable to use in the path, you must restart the computer so that the event log service can pick up the new variable; otherwise, the service will not be able to find your provider's resources.</span></span>

<span data-ttu-id="a9750-195">事件的訊息字串可以包含插入字串和參數字串。</span><span class="sxs-lookup"><span data-stu-id="a9750-195">An event's message string can contain insertion strings and parameter strings.</span></span> <span data-ttu-id="a9750-196">插入字串的格式為%*n*，其中 *n* 是以一為起始的索引，可從事件的資料範本識別您想要插入至訊息的資料項目。</span><span class="sxs-lookup"><span data-stu-id="a9750-196">An insertion string is of the form %*n*, where *n* is a one-based index that identifies a data item from the event's data template that you want to insert into the message.</span></span> <span data-ttu-id="a9750-197">參數字串 (查看 **parameterFileName** 屬性) 的格式為%%*n*，其中 n 是訊息資料表中訊息的識別碼。</span><span class="sxs-lookup"><span data-stu-id="a9750-197">A parameter string (see the **parameterFileName** attribute) is of the form %%*n*, where n is the identifier of a message in the message table.</span></span> <span data-ttu-id="a9750-198">如果事件的訊息字串包含 "%1% %11 = %2% %12" 和 %1 和 %2 的資料項目值分別為8和2，而且% %11 和% %12 的參數字串分別為 "夸脫" 和 "加侖"，則格式化的字串會是 "8 夸脫 = 2 加侖"。</span><span class="sxs-lookup"><span data-stu-id="a9750-198">If the event's message string contained "%1 %%11 = %2 %%12" and the data item values for %1 and %2 were 8 and 2, respectively, and the parameter strings for %%11 and %%12 were "quarts" and "gallons", respectively, the formatted string would be "8 quarts = 2 gallons".</span></span>

## <a name="requirements"></a><span data-ttu-id="a9750-199">規格需求</span><span class="sxs-lookup"><span data-stu-id="a9750-199">Requirements</span></span>



| <span data-ttu-id="a9750-200">需求</span><span class="sxs-lookup"><span data-stu-id="a9750-200">Requirement</span></span> | <span data-ttu-id="a9750-201">值</span><span class="sxs-lookup"><span data-stu-id="a9750-201">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a9750-202">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a9750-202">Minimum supported client</span></span><br/> | <span data-ttu-id="a9750-203">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9750-203">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a9750-204">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a9750-204">Minimum supported server</span></span><br/> | <span data-ttu-id="a9750-205">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a9750-205">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

