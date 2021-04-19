---
title: EventDefinitionType 複雜類型
description: 定義您的提供者可以撰寫的事件。
ms.assetid: 09ea89c9-6618-4874-ac72-5ee19cde4040
keywords:
- EventDefinitionType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- EventDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b7719abea1e97cae88edd47d176e5c578d73f0b7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106991781"
---
# <a name="eventdefinitiontype-complex-type"></a><span data-ttu-id="dd322-104">EventDefinitionType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="dd322-104">EventDefinitionType Complex Type</span></span>

<span data-ttu-id="dd322-105">定義您的提供者可以撰寫的事件。</span><span class="sxs-lookup"><span data-stu-id="dd322-105">Defines an event that your provider can write.</span></span>

``` syntax
<xs:complexType name="EventDefinitionType">
    <xs:simpleContent>
        <xs:extension
            base="string"
        >
            <xs:attribute name="value"
                type="UInt32Type"
                use="required"
             />
            <xs:attribute name="level"
                type="QName"
                use="optional"
             />
            <xs:attribute name="template"
                type="token"
                use="optional"
             />
            <xs:attribute name="channel"
                type="token"
                use="optional"
             />
            <xs:attribute name="keywords"
                type="QNameList"
                use="optional"
             />
            <xs:attribute name="task"
                type="QName"
                use="optional"
             />
            <xs:attribute name="opcode"
                type="QName"
                use="optional"
             />
            <xs:attribute name="symbol"
                type="CSymbolType"
                use="optional"
             />
            <xs:attribute name="version"
                type="unsignedByte"
                use="optional"
             />
            <xs:attribute name="message"
                type="strTableRef"
                use="optional"
             />
            <xs:attribute name="notLogged"
                type="boolean"
                use="optional"
                default="false"
             />
        </xs:extension>
    </xs:simpleContent>
</xs:complexType>
```

## <a name="attributes"></a><span data-ttu-id="dd322-106">屬性</span><span class="sxs-lookup"><span data-stu-id="dd322-106">Attributes</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd322-107">名稱</span><span class="sxs-lookup"><span data-stu-id="dd322-107">Name</span></span></th>
<th><span data-ttu-id="dd322-108">類型</span><span class="sxs-lookup"><span data-stu-id="dd322-108">Type</span></span></th>
<th><span data-ttu-id="dd322-109">Description</span><span class="sxs-lookup"><span data-stu-id="dd322-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="dd322-110">通道</span><span class="sxs-lookup"><span data-stu-id="dd322-110">channel</span></span></td>
<td><span data-ttu-id="dd322-111">token</span><span class="sxs-lookup"><span data-stu-id="dd322-111">token</span></span></td>
<td><span data-ttu-id="dd322-112">識別寫入事件之通道的識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd322-112">An identifier that identifies the channel to where the event is written.</span></span> <span data-ttu-id="dd322-113">指定您所定義或匯入之其中一個通道的通道識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd322-113">Specify a channel identifier of one of the channels that you defined or imported.</span></span> <span data-ttu-id="dd322-114">如果通道未指定通道識別碼，請使用通道的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd322-114">If the channel does not specify a channel identifier, use the channel's name.</span></span> <span data-ttu-id="dd322-115">如需定義或匯入通道的詳細資訊，請參閱 <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> 複雜類型。</span><span class="sxs-lookup"><span data-stu-id="dd322-115">For details on defining or importing a channel, see the <a href="eventmanifestschema-channellisttype-complextype.md"><strong>ChannelListType</strong></a> complex type.</span></span><br/> <span data-ttu-id="dd322-116">如果您未指定通道，則不會將事件寫入通道。</span><span class="sxs-lookup"><span data-stu-id="dd322-116">If you do not specify a channel, the event is not written to a channel.</span></span> <span data-ttu-id="dd322-117">一般而言，不指定通道的唯一原因是您只是要將事件寫入至 ETW 會話。</span><span class="sxs-lookup"><span data-stu-id="dd322-117">Typically, the only reason not to specify a channel is if you are writing events only to an ETW session.</span></span> <span data-ttu-id="dd322-118">如需詳細資訊，請參閱建立 ETW 會話的詳細資訊，請參閱 <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">控制事件追蹤會話</a>。</span><span class="sxs-lookup"><span data-stu-id="dd322-118">For details, see creating an ETW session, see <a href="/windows/desktop/ETW/controlling-event-tracing-sessions">Controlling Event Tracing Sessions</a>.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd322-119">關鍵字</span><span class="sxs-lookup"><span data-stu-id="dd322-119">keywords</span></span></td>
<td><span data-ttu-id="dd322-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd322-120"><a href="eventmanifestschema-qnamelist-simpletype.md"><strong>QNameList</strong></a></span></span></td>
<td><span data-ttu-id="dd322-121">關鍵字名稱的空格分隔清單，用來識別這個事件所屬的事件類別。</span><span class="sxs-lookup"><span data-stu-id="dd322-121">A space-separated list of keyword names that identify the category of events to which this event belongs.</span></span> <span data-ttu-id="dd322-122">從您定義的關鍵字清單中指定關鍵字名稱。</span><span class="sxs-lookup"><span data-stu-id="dd322-122">Specify a keyword name from the list of keywords that you define.</span></span> <span data-ttu-id="dd322-123">如需定義關鍵字的詳細資訊，請參閱 <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> 複雜類型。</span><span class="sxs-lookup"><span data-stu-id="dd322-123">For details on defining keywords, see the <a href="eventmanifestschema-keywordtype-complextype.md"><strong>KeywordType</strong></a> complex type.</span></span><br/> <span data-ttu-id="dd322-124">如果您未指定關鍵字，則事件描述項會針對關鍵字包含零。</span><span class="sxs-lookup"><span data-stu-id="dd322-124">If you do not specify keywords, the event descriptor will contain a zero for keywords.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd322-125">等級</span><span class="sxs-lookup"><span data-stu-id="dd322-125">level</span></span></td>
<td><span data-ttu-id="dd322-126"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="dd322-126"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="dd322-127">寫入事件時要使用的詳細層級。</span><span class="sxs-lookup"><span data-stu-id="dd322-127">The level of verbosity to use when writing the event.</span></span> <span data-ttu-id="dd322-128">指定您在資訊清單中定義的層級名稱，或是包含在 Windows SDK 的 \Include\Winmeta.xml 檔中定義的其中一個層級的名稱。</span><span class="sxs-lookup"><span data-stu-id="dd322-128">Specify the name of a level that you defined in the manifest or one of the levels defined in the \Include\Winmeta.xml file that is included in the Windows SDK.</span></span> <span data-ttu-id="dd322-129">如需定義層級的詳細資訊，請參閱 <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> 複雜類型。</span><span class="sxs-lookup"><span data-stu-id="dd322-129">For details on defining a level, see the <a href="eventmanifestschema-leveltype-complextype.md"><strong>LevelType</strong></a> complex type.</span></span><br/> <span data-ttu-id="dd322-130">如果您未指定層級，事件描述項的層級就會包含零。</span><span class="sxs-lookup"><span data-stu-id="dd322-130">If you do not specify a level, the event descriptor will contain a zero for level.</span></span><br/> <span data-ttu-id="dd322-131">如果寫入事件的通道類型為 Admin，您必須指定層級。層級必須是 Winmeata.xml 中所定義的下列其中一個層級：</span><span class="sxs-lookup"><span data-stu-id="dd322-131">You must specify a level if the channel type to which the event is written is Admin; the level must be one of the following levels defined in Winmeata.xml:</span></span>
<ul>
<li><span data-ttu-id="dd322-132">win:Critical</span><span class="sxs-lookup"><span data-stu-id="dd322-132">win:Critical</span></span></li>
<li><span data-ttu-id="dd322-133">win:Error</span><span class="sxs-lookup"><span data-stu-id="dd322-133">win:Error</span></span></li>
<li><span data-ttu-id="dd322-134">win:Warning</span><span class="sxs-lookup"><span data-stu-id="dd322-134">win:Warning</span></span></li>
<li><span data-ttu-id="dd322-135">win:Informational</span><span class="sxs-lookup"><span data-stu-id="dd322-135">win:Informational</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd322-136">message</span><span class="sxs-lookup"><span data-stu-id="dd322-136">message</span></span></td>
<td><span data-ttu-id="dd322-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd322-137"><a href="eventmanifestschema-strtableref-simpletype.md"><strong>strTableRef</strong></a></span></span></td>
<td><span data-ttu-id="dd322-138">事件的當地語系化訊息。</span><span class="sxs-lookup"><span data-stu-id="dd322-138">The localized message for the event.</span></span> <span data-ttu-id="dd322-139">訊息字串會參考資訊清單之 <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> 區段中的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="dd322-139">The message string references a localized string in the <a href="eventmanifestschema-stringtable-resources-element.md"><strong>stringTable</strong></a> section of the manifest.</span></span><br/> <span data-ttu-id="dd322-140">如果寫入事件的通道類型是 Admin，則必須指定訊息。</span><span class="sxs-lookup"><span data-stu-id="dd322-140">You must specify a message if the channel type to which the event is written is Admin.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd322-141">notLogged</span><span class="sxs-lookup"><span data-stu-id="dd322-141">notLogged</span></span></td>
<td><span data-ttu-id="dd322-142">boolean</span><span class="sxs-lookup"><span data-stu-id="dd322-142">boolean</span></span></td>
<td><span data-ttu-id="dd322-143">決定提供者是否要記錄此事件。</span><span class="sxs-lookup"><span data-stu-id="dd322-143">Determines whether the provider logs this event.</span></span> <span data-ttu-id="dd322-144">如果提供者記錄此事件，請指定 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="dd322-144">Specify true if the provider logs this event; otherwise, false.</span></span> <span data-ttu-id="dd322-145">使用這個屬性來表示提供者不再記錄此事件，而不是從資訊清單中移除事件。</span><span class="sxs-lookup"><span data-stu-id="dd322-145">Use this attribute to indicate that the provider is no longer logging this event instead of removing the event from the manifest.</span></span> <span data-ttu-id="dd322-146">在資訊清單中保留事件，可讓取用者將包含事件的舊版 etl 檔案解碼。</span><span class="sxs-lookup"><span data-stu-id="dd322-146">Retaining the event in the manifest will let consumers decode older etl files that include the event.</span></span><br/> <span data-ttu-id="dd322-147"><strong>Windows Server 2008 和 Windows Vista：</strong> 在 Windows SDK 的 Windows 7 版本之前隨附的訊息編譯器版本不支援這個屬性。</span><span class="sxs-lookup"><span data-stu-id="dd322-147"><strong>Windows Server 2008 and Windows Vista:</strong> This attribute is not supported in versions of the message compiler that shipped prior to the Windows 7 version of the Windows SDK.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd322-148">opcode</span><span class="sxs-lookup"><span data-stu-id="dd322-148">opcode</span></span></td>
<td><span data-ttu-id="dd322-149"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="dd322-149"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="dd322-150">在工作中識別作業的 opcode 名稱。</span><span class="sxs-lookup"><span data-stu-id="dd322-150">The name of an opcode that identifies an operation within the task.</span></span> <span data-ttu-id="dd322-151">指定您在資訊清單中定義的 opcode 名稱，或 Winmeta.xml 中定義的其中一個操作碼。</span><span class="sxs-lookup"><span data-stu-id="dd322-151">Specify the name of an opcode that you defined in the manifest or one of the opcodes defined in Winmeta.xml.</span></span> <span data-ttu-id="dd322-152">如需定義 opcode 的詳細資訊，請參閱 <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> 複雜類型。</span><span class="sxs-lookup"><span data-stu-id="dd322-152">For details on defining an opcode, see the <a href="eventmanifestschema-opcodetype-complextype.md"><strong>OpcodeType</strong></a> complex type.</span></span><br/> <span data-ttu-id="dd322-153">如果您參考的工作包含工作特定 (本機) 作業碼，則可以指定其中一個工作特定的作業碼，或在提供者層級定義的作業碼， (全域操作碼) 。</span><span class="sxs-lookup"><span data-stu-id="dd322-153">If the task that you reference contains task-specific (local) opcodes, you can specify one of its task-specific opcodes or an opcode defined at the provider level (a global opcode).</span></span> <span data-ttu-id="dd322-154">如果您指定全域操作碼，全域 opcode 的值不能與工作的其中一個本機作業碼相同。</span><span class="sxs-lookup"><span data-stu-id="dd322-154">If you specify a global opcode, the value of the global opcode cannot be the same as one of the local opcodes for the task.</span></span><br/> <span data-ttu-id="dd322-155">如果您參考本機作業碼，則工作屬性必須參考本機作業碼所屬的工作。</span><span class="sxs-lookup"><span data-stu-id="dd322-155">If you reference a local opcode, the task attribute must reference the task to which the local opcode belongs.</span></span><br/> <span data-ttu-id="dd322-156">如果您未指定作業碼，則事件描述項會針對 opcode 包含零。</span><span class="sxs-lookup"><span data-stu-id="dd322-156">If you do not specify an opcode, the event descriptor will contain a zero for opcode.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd322-157">符號</span><span class="sxs-lookup"><span data-stu-id="dd322-157">symbol</span></span></td>
<td><span data-ttu-id="dd322-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd322-158"><a href="eventmanifestschema-csymboltype-simpletype.md"><strong>CSymbolType</strong></a></span></span></td>
<td><span data-ttu-id="dd322-159">用來在應用程式中參考這個事件之事件描述項的符號。</span><span class="sxs-lookup"><span data-stu-id="dd322-159">The symbol to use to reference the event descriptor for this event in your application.</span></span> <span data-ttu-id="dd322-160"><a href="message-compiler--mc-exe-.md"><strong>訊息編譯器 (MC.exe) </strong></a>會使用符號，在編譯器產生的標頭檔中建立事件描述項的常數。</span><span class="sxs-lookup"><span data-stu-id="dd322-160">The <a href="message-compiler--mc-exe-.md"><strong>Message Compiler (MC.exe)</strong></a> uses the symbol to create a constant for the event descriptor in the header file that the compiler generates.</span></span> <span data-ttu-id="dd322-161">如果您未指定符號，編譯器會為您產生一個符號。</span><span class="sxs-lookup"><span data-stu-id="dd322-161">If you do not specify a symbol, the compiler generates one for you.</span></span> <span data-ttu-id="dd322-162">當您呼叫 <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> 函式來寫入事件時，會使用描述項。</span><span class="sxs-lookup"><span data-stu-id="dd322-162">You use the descriptor when you call the <a href="/windows/desktop/api/evntprov/nf-evntprov-eventwrite"><strong>EventWrite</strong></a> function to write the event.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd322-163">工作 (task)</span><span class="sxs-lookup"><span data-stu-id="dd322-163">task</span></span></td>
<td><span data-ttu-id="dd322-164"><strong>QName</strong></span><span class="sxs-lookup"><span data-stu-id="dd322-164"><strong>QName</strong></span></span></td>
<td><span data-ttu-id="dd322-165">識別產生此事件之元件或子元件的工作名稱。</span><span class="sxs-lookup"><span data-stu-id="dd322-165">The name of a task that identifies the component or subcomponent that generates this event.</span></span> <span data-ttu-id="dd322-166">指定您在資訊清單中定義的工作名稱。</span><span class="sxs-lookup"><span data-stu-id="dd322-166">Specify the name of a task that you defined in the manifest.</span></span> <span data-ttu-id="dd322-167">如需定義工作的詳細資訊，請參閱 <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> 複雜類型。</span><span class="sxs-lookup"><span data-stu-id="dd322-167">For details on defining a task, see the <a href="eventmanifestschema-tasktype-complextype.md"><strong>TaskType</strong></a> complex type.</span></span><br/> <span data-ttu-id="dd322-168">如果您未指定工作，則事件描述項會包含工作的零。</span><span class="sxs-lookup"><span data-stu-id="dd322-168">If you do not specify a task, the event descriptor will contain a zero for task.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd322-169">template</span><span class="sxs-lookup"><span data-stu-id="dd322-169">template</span></span></td>
<td><span data-ttu-id="dd322-170">token</span><span class="sxs-lookup"><span data-stu-id="dd322-170">token</span></span></td>
<td><span data-ttu-id="dd322-171">範本的範本識別碼，定義此事件包含的資料項目。</span><span class="sxs-lookup"><span data-stu-id="dd322-171">The template identifier of the template that defines the data items that this event includes.</span></span> <span data-ttu-id="dd322-172">指定您在資訊清單中定義的範本識別碼。</span><span class="sxs-lookup"><span data-stu-id="dd322-172">Specify the identifier of a template that you defined in the manifest.</span></span> <span data-ttu-id="dd322-173">如需定義範本的詳細資訊，請參閱 <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> 複雜類型。</span><span class="sxs-lookup"><span data-stu-id="dd322-173">For details on defining a template, see the <a href="eventmanifestschema-templateitemtype-complextype.md"><strong>TemplateItemType</strong></a> complex type.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="dd322-174">value</span><span class="sxs-lookup"><span data-stu-id="dd322-174">value</span></span></td>
<td><span data-ttu-id="dd322-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span><span class="sxs-lookup"><span data-stu-id="dd322-175"><a href="eventmanifestschema-hexint32type-simpletype.md"><strong>UInt32Type</strong></a></span></span></td>
<td><span data-ttu-id="dd322-176">事件識別項。</span><span class="sxs-lookup"><span data-stu-id="dd322-176">The event identifier.</span></span> <span data-ttu-id="dd322-177">識別碼在您定義的事件清單中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="dd322-177">The identifier must be unique within the list of events that you define.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="dd322-178">version</span><span class="sxs-lookup"><span data-stu-id="dd322-178">version</span></span></td>
<td><span data-ttu-id="dd322-179">unsignedByte</span><span class="sxs-lookup"><span data-stu-id="dd322-179">unsignedByte</span></span></td>
<td><span data-ttu-id="dd322-180">事件定義的單位元組版本號碼。</span><span class="sxs-lookup"><span data-stu-id="dd322-180">A one-byte version number of the event definition.</span></span><br/></td>
</tr>
</tbody>
</table>



## <a name="remarks"></a><span data-ttu-id="dd322-181">備註</span><span class="sxs-lookup"><span data-stu-id="dd322-181">Remarks</span></span>

<span data-ttu-id="dd322-182">如果您使用 [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) 來格式化事件 (的訊息字串，或使用事件檢視器來查看訊息字串) ，訊息字串可以包含插入字串和 Win32 **FormatMessage** 函數所支援的任何格式字串。</span><span class="sxs-lookup"><span data-stu-id="dd322-182">If you use [**EvtFormatMessage**](/windows/desktop/api/WinEvt/nf-winevt-evtformatmessage) to format the message string for the event (or use the Event Viewer to view the message string), the message string can contain insertion strings and any of the format strings that the Win32 **FormatMessage** function supports.</span></span> <span data-ttu-id="dd322-183">插入字串的限制為%*n* 或%*n*！ s！</span><span class="sxs-lookup"><span data-stu-id="dd322-183">The insertion strings are limited to %*n* or %*n*!s!</span></span> <span data-ttu-id="dd322-184"> (例如，%1) ，其中 *n* 是在事件範本中定義之資料項目的參考（以一為基礎）。</span><span class="sxs-lookup"><span data-stu-id="dd322-184">(for example, %1) where *n* is the one-based reference the data items defined in the event's template.</span></span> <span data-ttu-id="dd322-185">訊息字串也可以包含格式為%%*n* (的參數插入字串，例如% %4) 。</span><span class="sxs-lookup"><span data-stu-id="dd322-185">The message string can also contain parameter insertion strings in the form %%*n* (for example, %%4).</span></span> <span data-ttu-id="dd322-186">訊息可以包含的插入字串數目上限為100。</span><span class="sxs-lookup"><span data-stu-id="dd322-186">The maximum number of insertion strings that the message can contain is 100.</span></span>

## <a name="requirements"></a><span data-ttu-id="dd322-187">規格需求</span><span class="sxs-lookup"><span data-stu-id="dd322-187">Requirements</span></span>



| <span data-ttu-id="dd322-188">需求</span><span class="sxs-lookup"><span data-stu-id="dd322-188">Requirement</span></span> | <span data-ttu-id="dd322-189">值</span><span class="sxs-lookup"><span data-stu-id="dd322-189">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="dd322-190">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dd322-190">Minimum supported client</span></span><br/> | <span data-ttu-id="dd322-191">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd322-191">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="dd322-192">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dd322-192">Minimum supported server</span></span><br/> | <span data-ttu-id="dd322-193">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dd322-193">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

