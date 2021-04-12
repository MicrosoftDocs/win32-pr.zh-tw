---
title: MetadataType 複雜類型
description: 定義您可以在資訊清單的 metadata 區段中定義的元資料類型。
ms.assetid: 602bafe7-940e-4313-9da5-54c6aa7f60a2
keywords:
- MetadataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- MetadataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 69b140a2b65d47d563fd88f49d6818efc13613f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025453"
---
# <a name="metadatatype-complex-type"></a><span data-ttu-id="e7dce-104">MetadataType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="e7dce-104">MetadataType Complex Type</span></span>

<span data-ttu-id="e7dce-105">定義您可以在資訊清單的 metadata 區段中定義的元資料類型。</span><span class="sxs-lookup"><span data-stu-id="e7dce-105">Defines the metadata types that you can define in the metadata section of the manifest.</span></span>

``` syntax
<xs:complexType name="MetadataType">
    <xs:sequence>
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
            minOccurs="0"
         />
        <xs:element name="keywords"
            type="KeywordListType"
            minOccurs="0"
         />
        <xs:element name="types"
            type="TypeListType"
            minOccurs="0"
         />
        <xs:element name="namedQueries"
            type="NamedQueryType"
            minOccurs="0"
         />
        <xs:element name="messageTable"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:sequence>
                    <xs:element name="message"
                        minOccurs="0"
                        maxOccurs="unbounded"
                    >
                        <xs:complexType>
                            <xs:attribute name="value"
                                type="UInt32Type"
                                use="required"
                             />
                            <xs:attribute name="mid"
                                type="xs:string"
                                use="optional"
                             />
                            <xs:attribute name="message"
                                type="strTableRef"
                                use="required"
                             />
                            <xs:attribute name="symbol"
                                type="CSymbolType"
                                use="optional"
                             />
                        </xs:complexType>
                    </xs:element>
                </xs:sequence>
            </xs:complexType>
        </xs:element>
        <xs:any
            processContents="lax"
            minOccurs="0"
            maxOccurs="unbounded"
            namespace="##other"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="anyURI"
        use="required"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="e7dce-106">子元素</span><span class="sxs-lookup"><span data-stu-id="e7dce-106">Child elements</span></span>



| <span data-ttu-id="e7dce-107">元素</span><span class="sxs-lookup"><span data-stu-id="e7dce-107">Element</span></span>                                                                       | <span data-ttu-id="e7dce-108">類型</span><span class="sxs-lookup"><span data-stu-id="e7dce-108">Type</span></span>                                                                       | <span data-ttu-id="e7dce-109">Description</span><span class="sxs-lookup"><span data-stu-id="e7dce-109">Description</span></span>                                                                                                                                                      |
|-------------------------------------------------------------------------------|----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e7dce-110">**管道**</span><span class="sxs-lookup"><span data-stu-id="e7dce-110">**channels**</span></span>](eventmanifestschema-channels-metadatatype-element.md)         | [<span data-ttu-id="e7dce-111">**ChannelListType**</span><span class="sxs-lookup"><span data-stu-id="e7dce-111">**ChannelListType**</span></span>](eventmanifestschema-channellisttype-complextype.md) | <span data-ttu-id="e7dce-112">定義提供者可以記錄事件的通道清單。</span><span class="sxs-lookup"><span data-stu-id="e7dce-112">Defines a list of channels to which providers can log events.</span></span> <span data-ttu-id="e7dce-113">然後，提供者可以在其資訊清單中匯入一或多個通道。</span><span class="sxs-lookup"><span data-stu-id="e7dce-113">A provider can then import one or more of the channels in their manifest.</span></span><br/>               |
| [<span data-ttu-id="e7dce-114">**關鍵 字**</span><span class="sxs-lookup"><span data-stu-id="e7dce-114">**keywords**</span></span>](eventmanifestschema-keywords-metadatatype-element.md)         | [<span data-ttu-id="e7dce-115">**KeywordListType**</span><span class="sxs-lookup"><span data-stu-id="e7dce-115">**KeywordListType**</span></span>](eventmanifestschema-keywordlisttype-complextype.md) | <span data-ttu-id="e7dce-116">定義關鍵字清單，以決定提供者寫入的事件類別。</span><span class="sxs-lookup"><span data-stu-id="e7dce-116">Defines a list of keywords that determine the category of events that the provider writes.</span></span><br/>                                                            |
| [<span data-ttu-id="e7dce-117">**水準**</span><span class="sxs-lookup"><span data-stu-id="e7dce-117">**levels**</span></span>](eventmanifestschema-levels-metadatatype-element.md)             | [<span data-ttu-id="e7dce-118">**LevelListType**</span><span class="sxs-lookup"><span data-stu-id="e7dce-118">**LevelListType**</span></span>](eventmanifestschema-levellisttype-complextype.md)     | <span data-ttu-id="e7dce-119">定義指定事件嚴重性的層級清單。</span><span class="sxs-lookup"><span data-stu-id="e7dce-119">Defines a list of levels that specify the severity of an event.</span></span><br/>                                                                                       |
| <span data-ttu-id="e7dce-120">**message**</span><span class="sxs-lookup"><span data-stu-id="e7dce-120">**message**</span></span>                                                                   |                                                                            | <span data-ttu-id="e7dce-121">定義訊息字串。</span><span class="sxs-lookup"><span data-stu-id="e7dce-121">Defines a message string.</span></span><br/>                                                                                                                             |
| <span data-ttu-id="e7dce-122">**messageTable**</span><span class="sxs-lookup"><span data-stu-id="e7dce-122">**messageTable**</span></span>                                                              |                                                                            | <span data-ttu-id="e7dce-123">定義訊息字串的清單。</span><span class="sxs-lookup"><span data-stu-id="e7dce-123">Defines a list of message strings.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="e7dce-124">**namedQueries**</span><span class="sxs-lookup"><span data-stu-id="e7dce-124">**namedQueries**</span></span>](eventmanifestschema-namedqueries-metadatatype-element.md) | [<span data-ttu-id="e7dce-125">**NamedQueryType**</span><span class="sxs-lookup"><span data-stu-id="e7dce-125">**NamedQueryType**</span></span>](eventmanifestschema-namedquerytype-complextype.md)   | <span data-ttu-id="e7dce-126">定義已命名查詢的清單，這些查詢會使用正則運算式來執行事件訊息字串的尋找和取代動作。</span><span class="sxs-lookup"><span data-stu-id="e7dce-126">Defines a list of named queries that use regular expressions to perform find and replace actions on an event's message string.</span></span><br/>                        |
| [<span data-ttu-id="e7dce-127">**碼**</span><span class="sxs-lookup"><span data-stu-id="e7dce-127">**opcodes**</span></span>](eventmanifestschema-opcodes-metadatatype-element.md)           | [<span data-ttu-id="e7dce-128">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="e7dce-128">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md)   | <span data-ttu-id="e7dce-129">定義可用於將工作中的事件群組在一起的作業碼清單。</span><span class="sxs-lookup"><span data-stu-id="e7dce-129">Defines a list of opcodes that you can use to group events within a task.</span></span><br/>                                                                             |
| <span data-ttu-id="e7dce-130">**任務**</span><span class="sxs-lookup"><span data-stu-id="e7dce-130">**tasks**</span></span>                                                                     | [<span data-ttu-id="e7dce-131">**TaskListType**</span><span class="sxs-lookup"><span data-stu-id="e7dce-131">**TaskListType**</span></span>](eventmanifestschema-tasklisttype-complextype.md)       | <span data-ttu-id="e7dce-132">定義提供者可用來群組事件的工作清單。</span><span class="sxs-lookup"><span data-stu-id="e7dce-132">Defines a list of tasks that a provider can use to group events.</span></span> <span data-ttu-id="e7dce-133">一般而言，您會使用工作將提供者的功能或元件的事件分組。</span><span class="sxs-lookup"><span data-stu-id="e7dce-133">Typically, you use tasks to group events for a feature or component of the provider.</span></span><br/> |
| [<span data-ttu-id="e7dce-134">**類型**</span><span class="sxs-lookup"><span data-stu-id="e7dce-134">**types**</span></span>](eventmanifestschema-types-metadatatype-element.md)               | [<span data-ttu-id="e7dce-135">**TypeListType**</span><span class="sxs-lookup"><span data-stu-id="e7dce-135">**TypeListType**</span></span>](eventmanifestschema-typelisttype-complextype.md)       | <span data-ttu-id="e7dce-136">定義 XML 類型的清單。</span><span class="sxs-lookup"><span data-stu-id="e7dce-136">Defines a list of XML types.</span></span><br/>                                                                                                                          |



## <a name="attributes"></a><span data-ttu-id="e7dce-137">屬性</span><span class="sxs-lookup"><span data-stu-id="e7dce-137">Attributes</span></span>



| <span data-ttu-id="e7dce-138">名稱</span><span class="sxs-lookup"><span data-stu-id="e7dce-138">Name</span></span>    | <span data-ttu-id="e7dce-139">類型</span><span class="sxs-lookup"><span data-stu-id="e7dce-139">Type</span></span>                                                              | <span data-ttu-id="e7dce-140">Description</span><span class="sxs-lookup"><span data-stu-id="e7dce-140">Description</span></span>                                                                                        |
|---------|-------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e7dce-141">message</span><span class="sxs-lookup"><span data-stu-id="e7dce-141">message</span></span> | [<span data-ttu-id="e7dce-142">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="e7dce-142">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="e7dce-143">字串資料表中當地語系化字串的參考。</span><span class="sxs-lookup"><span data-stu-id="e7dce-143">A reference to the localized string in the string table.</span></span><br/>                                |
| <span data-ttu-id="e7dce-144">mid</span><span class="sxs-lookup"><span data-stu-id="e7dce-144">mid</span></span>     | <span data-ttu-id="e7dce-145">xs:string</span><span class="sxs-lookup"><span data-stu-id="e7dce-145">xs:string</span></span>                                                         | <span data-ttu-id="e7dce-146">未使用。</span><span class="sxs-lookup"><span data-stu-id="e7dce-146">Not used.</span></span><br/>                                                                               |
| <span data-ttu-id="e7dce-147">NAME</span><span class="sxs-lookup"><span data-stu-id="e7dce-147">name</span></span>    | <span data-ttu-id="e7dce-148">anyURI</span><span class="sxs-lookup"><span data-stu-id="e7dce-148">anyURI</span></span>                                                            | <span data-ttu-id="e7dce-149">中繼檔案的 URI。</span><span class="sxs-lookup"><span data-stu-id="e7dce-149">The URI of the meta file.</span></span> <br/>                                                              |
| <span data-ttu-id="e7dce-150">符號</span><span class="sxs-lookup"><span data-stu-id="e7dce-150">symbol</span></span>  | [<span data-ttu-id="e7dce-151">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="e7dce-151">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="e7dce-152">您希望訊息編譯器為此訊息字串建立的符號名稱。</span><span class="sxs-lookup"><span data-stu-id="e7dce-152">The symbolic name that you want the message compiler to create for this message string.</span></span><br/> |
| <span data-ttu-id="e7dce-153">value</span><span class="sxs-lookup"><span data-stu-id="e7dce-153">value</span></span>   | [<span data-ttu-id="e7dce-154">**UInt32Type**</span><span class="sxs-lookup"><span data-stu-id="e7dce-154">**UInt32Type**</span></span>](eventmanifestschema-hexint32type-simpletype.md) | <span data-ttu-id="e7dce-155">要用來做為此訊息之訊息識別碼的數位。</span><span class="sxs-lookup"><span data-stu-id="e7dce-155">The number to use as the message identifier for this message.</span></span><br/>                           |



## <a name="remarks"></a><span data-ttu-id="e7dce-156">備註</span><span class="sxs-lookup"><span data-stu-id="e7dce-156">Remarks</span></span>

<span data-ttu-id="e7dce-157">雖然您可以建立包含中繼資料區段的資訊清單，但服務將不會使用它。服務唯一可辨識的中繼資料是 Winmeta.xml 檔案中找到的中繼資料。</span><span class="sxs-lookup"><span data-stu-id="e7dce-157">Although you can create a manifest that contains a metadata section, the service will not use it; the only metadata that the service recognizes is the metadata found in the Winmeta.xml file.</span></span>

## <a name="requirements"></a><span data-ttu-id="e7dce-158">規格需求</span><span class="sxs-lookup"><span data-stu-id="e7dce-158">Requirements</span></span>



| <span data-ttu-id="e7dce-159">需求</span><span class="sxs-lookup"><span data-stu-id="e7dce-159">Requirement</span></span> | <span data-ttu-id="e7dce-160">值</span><span class="sxs-lookup"><span data-stu-id="e7dce-160">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="e7dce-161">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e7dce-161">Minimum supported client</span></span><br/> | <span data-ttu-id="e7dce-162">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7dce-162">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="e7dce-163">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e7dce-163">Minimum supported server</span></span><br/> | <span data-ttu-id="e7dce-164">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e7dce-164">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





