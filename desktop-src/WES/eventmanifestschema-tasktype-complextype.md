---
title: TaskType 複雜類型
description: 定義應用程式的元件或子元件。 |TaskType 複雜類型
ms.assetid: d117636d-6363-43b6-ac5a-52234ac7c729
keywords:
- TaskType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- TaskType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ccad6813624d0a27a093ff4baa7fc8b9a6aa8b14
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106991430"
---
# <a name="tasktype-complex-type"></a><span data-ttu-id="f0cf4-105">TaskType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="f0cf4-105">TaskType Complex Type</span></span>

<span data-ttu-id="f0cf4-106">定義應用程式的元件或子元件。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-106">Defines a component or subcomponent of an application.</span></span>

``` syntax
<xs:complexType name="TaskType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="opcodes"
            type="OpcodeListType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="QName"
        use="required"
     />
    <xs:attribute name="symbol"
        type="CSymbolType"
        use="optional"
     />
    <xs:attribute name="value"
        type="UInt16Type"
        use="required"
     />
    <xs:attribute name="eventGUID"
        type="GUIDType"
        use="optional"
     />
    <xs:attribute name="message"
        type="strTableRef"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="f0cf4-107">子元素</span><span class="sxs-lookup"><span data-stu-id="f0cf4-107">Child elements</span></span>



| <span data-ttu-id="f0cf4-108">元素</span><span class="sxs-lookup"><span data-stu-id="f0cf4-108">Element</span></span>                                                         | <span data-ttu-id="f0cf4-109">類型</span><span class="sxs-lookup"><span data-stu-id="f0cf4-109">Type</span></span>                                                                     | <span data-ttu-id="f0cf4-110">Description</span><span class="sxs-lookup"><span data-stu-id="f0cf4-110">Description</span></span>                                                                                                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0cf4-111">**碼**</span><span class="sxs-lookup"><span data-stu-id="f0cf4-111">**opcodes**</span></span>](eventmanifestschema-opcodes-tasktype-element.md) | [<span data-ttu-id="f0cf4-112">**OpcodeListType**</span><span class="sxs-lookup"><span data-stu-id="f0cf4-112">**OpcodeListType**</span></span>](eventmanifestschema-opcodelisttype-complextype.md) | <span data-ttu-id="f0cf4-113">定義工作特定作業碼的清單。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-113">Defines a list of task-specific opcodes.</span></span> <span data-ttu-id="f0cf4-114">您無法使用 Winmeta.xml 中為工作專屬的作業碼定義的 opcode 值。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-114">You cannot use the opcode values defined in Winmeta.xml for task-specific opcodes.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="f0cf4-115">屬性</span><span class="sxs-lookup"><span data-stu-id="f0cf4-115">Attributes</span></span>



| <span data-ttu-id="f0cf4-116">名稱</span><span class="sxs-lookup"><span data-stu-id="f0cf4-116">Name</span></span>      | <span data-ttu-id="f0cf4-117">類型</span><span class="sxs-lookup"><span data-stu-id="f0cf4-117">Type</span></span>                                                              | <span data-ttu-id="f0cf4-118">Description</span><span class="sxs-lookup"><span data-stu-id="f0cf4-118">Description</span></span>                                                                                                                                                                                                                                                                                                      |
|-----------|-------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f0cf4-119">eventGUID</span><span class="sxs-lookup"><span data-stu-id="f0cf4-119">eventGUID</span></span> | [<span data-ttu-id="f0cf4-120">**GUIDType**</span><span class="sxs-lookup"><span data-stu-id="f0cf4-120">**GUIDType**</span></span>](eventmanifestschema-guidtype-simpletype.md)       | <span data-ttu-id="f0cf4-121">識別工作的全域唯一識別碼（登錄格式）。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-121">A globally unique identifier, in Registry format, that identifies the task.</span></span> <span data-ttu-id="f0cf4-122">如果您使用-mof 訊息編譯器引數來產生下層支援的 MOF 類別，則需要這個屬性。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-122">This attribute is required if you use the -mof message compiler argument to generate a MOF class for downlevel support.</span></span><br/>                                                                                                   |
| <span data-ttu-id="f0cf4-123">message</span><span class="sxs-lookup"><span data-stu-id="f0cf4-123">message</span></span>   | [<span data-ttu-id="f0cf4-124">**strTableRef**</span><span class="sxs-lookup"><span data-stu-id="f0cf4-124">**strTableRef**</span></span>](eventmanifestschema-strtableref-simpletype.md) | <span data-ttu-id="f0cf4-125">工作的當地語系化顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-125">The localized display name for the task.</span></span> <span data-ttu-id="f0cf4-126">訊息字串會參考資訊清單之 [**stringTable**](eventmanifestschema-stringtable-resources-element.md) 區段中的當地語系化字串。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-126">The message string references a localized string in the [**stringTable**](eventmanifestschema-stringtable-resources-element.md) section of the manifest.</span></span> <br/>                                                                                                   |
| <span data-ttu-id="f0cf4-127">NAME</span><span class="sxs-lookup"><span data-stu-id="f0cf4-127">name</span></span>      | <span data-ttu-id="f0cf4-128">**QName**</span><span class="sxs-lookup"><span data-stu-id="f0cf4-128">**QName**</span></span>                                                         | <span data-ttu-id="f0cf4-129">工作的名稱。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-129">The name of the task.</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="f0cf4-130">符號</span><span class="sxs-lookup"><span data-stu-id="f0cf4-130">symbol</span></span>    | [<span data-ttu-id="f0cf4-131">**CSymbolType**</span><span class="sxs-lookup"><span data-stu-id="f0cf4-131">**CSymbolType**</span></span>](eventmanifestschema-csymboltype-simpletype.md) | <span data-ttu-id="f0cf4-132">用來參考應用程式中工作的符號。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-132">The symbol to use to reference the task in your application.</span></span> <span data-ttu-id="f0cf4-133">[**訊息編譯器 (MC.exe)**](message-compiler--mc-exe-.md)會使用符號，在編譯器產生的標頭檔中建立工作的常數。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-133">The [**Message Compiler (MC.exe)**](message-compiler--mc-exe-.md) uses the symbol to create a constant for the task in the header file that the compiler generates.</span></span> <span data-ttu-id="f0cf4-134">如果您未指定符號，編譯器會為您產生一個符號。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-134">If you do not specify a symbol, the compiler generates one for you.</span></span><br/> |
| <span data-ttu-id="f0cf4-135">value</span><span class="sxs-lookup"><span data-stu-id="f0cf4-135">value</span></span>     | [<span data-ttu-id="f0cf4-136">**UInt16Type**</span><span class="sxs-lookup"><span data-stu-id="f0cf4-136">**UInt16Type**</span></span>](eventmanifestschema-hexint16type-simpletype.md) | <span data-ttu-id="f0cf4-137">在提供者所定義的工作清單中，可唯一識別這項工作的數位值。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-137">A numeric value that uniquely identifies this task within the list of tasks that the provider defines.</span></span> <span data-ttu-id="f0cf4-138">值的範圍必須介於1到239之間。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-138">The value must be in the range from 1 through 239.</span></span><br/>                                                                                                                                             |



## <a name="examples"></a><span data-ttu-id="f0cf4-139">範例</span><span class="sxs-lookup"><span data-stu-id="f0cf4-139">Examples</span></span>

<span data-ttu-id="f0cf4-140">下列範例顯示如何指定工作。</span><span class="sxs-lookup"><span data-stu-id="f0cf4-140">The following example shows how to specify a task.</span></span>


```XML
<tasks>
  <task name="printspool:Disconnect" 
         symbol="PRINTSPOOL_TASK_DISCONNECT"
         value="0" 
         message="$(string.disconnect)"/>
 
  <task name="printspool:Connect" 
         symbol="PRINTSPOOL_TASK_CONNECT"
         value="1" 
         message="$(string.connect)">
       <opcodes>
          <opcode name="ReadRegistry" 
                  symbol="MYOPCODE_READ_REGISTRY" value="11"
                  message="$(string.ReadRegistry)"/>
       </opcodes>
   </task>
</tasks>
```



## <a name="requirements"></a><span data-ttu-id="f0cf4-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0cf4-141">Requirements</span></span>



| <span data-ttu-id="f0cf4-142">需求</span><span class="sxs-lookup"><span data-stu-id="f0cf4-142">Requirement</span></span> | <span data-ttu-id="f0cf4-143">值</span><span class="sxs-lookup"><span data-stu-id="f0cf4-143">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f0cf4-144">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0cf4-144">Minimum supported client</span></span><br/> | <span data-ttu-id="f0cf4-145">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0cf4-145">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f0cf4-146">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0cf4-146">Minimum supported server</span></span><br/> | <span data-ttu-id="f0cf4-147">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0cf4-147">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





