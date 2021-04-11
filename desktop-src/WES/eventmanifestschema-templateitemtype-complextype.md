---
title: TemplateItemType 複雜類型
description: 此範本會定義要包含在事件中的資料。 |TemplateItemType 複雜類型
ms.assetid: 1681af7d-03ef-47bc-bc02-ce1a9903fb44
keywords:
- TemplateItemType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- TemplateItemType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 94ae108ceed3285fe7e57461611d94b1147d94e7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "104196014"
---
# <a name="templateitemtype-complex-type"></a><span data-ttu-id="3701a-105">TemplateItemType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="3701a-105">TemplateItemType Complex Type</span></span>

<span data-ttu-id="3701a-106">此範本會定義要包含在事件中的資料。</span><span class="sxs-lookup"><span data-stu-id="3701a-106">A template that defines the data to include with an event.</span></span>

``` syntax
<xs:complexType name="TemplateItemType">
    <xs:sequence
        maxOccurs="unbounded"
    >
        <xs:choice
            maxOccurs="unbounded"
            minOccurs="0"
        >
            <xs:element name="data"
                type="DataDefinitionType"
             />
            <xs:element name="struct"
                type="StructDefinitionType"
             />
        </xs:choice>
        <xs:element name="binary"
            minOccurs="0"
        >
            <xs:complexType>
                <xs:attribute name="name"
                    type="string"
                    use="optional"
                 />
            </xs:complexType>
        </xs:element>
        <xs:element name="UserData"
            type="XmlType"
            minOccurs="0"
         />
    </xs:sequence>
    <xs:attribute name="tid"
        type="token"
        use="required"
     />
    <xs:attribute name="name"
        type="string"
        use="optional"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="3701a-107">子元素</span><span class="sxs-lookup"><span data-stu-id="3701a-107">Child elements</span></span>



| <span data-ttu-id="3701a-108">元素</span><span class="sxs-lookup"><span data-stu-id="3701a-108">Element</span></span>                                                                   | <span data-ttu-id="3701a-109">類型</span><span class="sxs-lookup"><span data-stu-id="3701a-109">Type</span></span>                                                                                 | <span data-ttu-id="3701a-110">Description</span><span class="sxs-lookup"><span data-stu-id="3701a-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="3701a-111">**二 進 制**</span><span class="sxs-lookup"><span data-stu-id="3701a-111">**binary**</span></span>](eventmanifestschema-binary-templateitemtype-element.md)     |                                                                                      | <span data-ttu-id="3701a-112">已保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="3701a-112">Reserved for internal use only.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="3701a-113">**資料**</span><span class="sxs-lookup"><span data-stu-id="3701a-113">**data**</span></span>](eventmanifestschema-data-templateitemtype-element.md)         | [<span data-ttu-id="3701a-114">**DataDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="3701a-114">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md)     | <span data-ttu-id="3701a-115">定義您想要包含在事件中的資料項目。</span><span class="sxs-lookup"><span data-stu-id="3701a-115">Defines a data item that you want to include with the event.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| [<span data-ttu-id="3701a-116">**結構**</span><span class="sxs-lookup"><span data-stu-id="3701a-116">**struct**</span></span>](eventmanifestschema-struct-templateitemtype-element.md)     | [<span data-ttu-id="3701a-117">**StructDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="3701a-117">**StructDefinitionType**</span></span>](eventmanifestschema-structdefinitiontype-complextype.md) | <span data-ttu-id="3701a-118">定義結構，其中包含一個或多個您想要包含在事件中的資料項目。</span><span class="sxs-lookup"><span data-stu-id="3701a-118">Defines a structure that includes one or more data items that you want to include with the event.</span></span> <span data-ttu-id="3701a-119">提供者會將結構撰寫為 blob，而不是結構的個別成員。</span><span class="sxs-lookup"><span data-stu-id="3701a-119">Providers write the structure as a blob and not as individual members of the structure.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| [<span data-ttu-id="3701a-120">**UserData**</span><span class="sxs-lookup"><span data-stu-id="3701a-120">**UserData**</span></span>](eventmanifestschema-userdata-templateitemtype-element.md) | [<span data-ttu-id="3701a-121">**XmlType**</span><span class="sxs-lookup"><span data-stu-id="3701a-121">**XmlType**</span></span>](eventmanifestschema-xmltype-complextype.md)                           | <span data-ttu-id="3701a-122">用來呈現事件資料的 XML 片段。</span><span class="sxs-lookup"><span data-stu-id="3701a-122">An XML fragment that is used to render the event data.</span></span> <span data-ttu-id="3701a-123">如果您未包含片段，則會以範本中定義資料項目的順序轉譯事件資料。</span><span class="sxs-lookup"><span data-stu-id="3701a-123">If you do not include the fragment, the event data is rendered in the order that the data items are defined in the template.</span></span> <span data-ttu-id="3701a-124">此元素的內容是任何有效的 XML 片段。</span><span class="sxs-lookup"><span data-stu-id="3701a-124">The contents of this element is any valid XML fragment.</span></span> <span data-ttu-id="3701a-125">片段必須只包含一個最上層節點，而且最上層節點必須指定它自己的命名空間。</span><span class="sxs-lookup"><span data-stu-id="3701a-125">The fragment must contain only one top-level node and the top-level node must specify its own namespace.</span></span> <br/> <span data-ttu-id="3701a-126">若要參考片段中的資料項目，請將片段中節點的文字主體設定為%*n*，其中 *n* 是資料項目清單中最上層資料項目的單一索引， (您無法參考結構) 的成員。</span><span class="sxs-lookup"><span data-stu-id="3701a-126">To reference a data item in the fragment, set the text body for a node in the fragment to %*n*, where *n* is the one-based index of the top-level data items in the list of data items (you cannot reference members of a structure).</span></span> <span data-ttu-id="3701a-127">您指定的索引值不得大於範本中最上層資料項目的數目。</span><span class="sxs-lookup"><span data-stu-id="3701a-127">The index value that you specify must not be greater than the number of top-level data items in the template.</span></span><br/> <span data-ttu-id="3701a-128">這個元素會遵循所有 **資料** 和 **結構** 元素。</span><span class="sxs-lookup"><span data-stu-id="3701a-128">This element follows all **data** and **struct** elements.</span></span> <br/> |



## <a name="attributes"></a><span data-ttu-id="3701a-129">屬性</span><span class="sxs-lookup"><span data-stu-id="3701a-129">Attributes</span></span>



| <span data-ttu-id="3701a-130">名稱</span><span class="sxs-lookup"><span data-stu-id="3701a-130">Name</span></span> | <span data-ttu-id="3701a-131">類型</span><span class="sxs-lookup"><span data-stu-id="3701a-131">Type</span></span>   | <span data-ttu-id="3701a-132">描述</span><span class="sxs-lookup"><span data-stu-id="3701a-132">Description</span></span>                                                                                                                                                                                           |
|------|--------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3701a-133">NAME</span><span class="sxs-lookup"><span data-stu-id="3701a-133">name</span></span> | <span data-ttu-id="3701a-134">字串</span><span class="sxs-lookup"><span data-stu-id="3701a-134">string</span></span> | <span data-ttu-id="3701a-135">已保留供內部使用。</span><span class="sxs-lookup"><span data-stu-id="3701a-135">Reserved for internal use only.</span></span><br/>                                                                                                                                                            |
| <span data-ttu-id="3701a-136">NAME</span><span class="sxs-lookup"><span data-stu-id="3701a-136">name</span></span> | <span data-ttu-id="3701a-137">字串</span><span class="sxs-lookup"><span data-stu-id="3701a-137">string</span></span> | <span data-ttu-id="3701a-138">範本名稱。</span><span class="sxs-lookup"><span data-stu-id="3701a-138">The name of the template.</span></span><br/>                                                                                                                                                                  |
| <span data-ttu-id="3701a-139">tid</span><span class="sxs-lookup"><span data-stu-id="3701a-139">tid</span></span>  | <span data-ttu-id="3701a-140">token</span><span class="sxs-lookup"><span data-stu-id="3701a-140">token</span></span>  | <span data-ttu-id="3701a-141">唯一識別提供者所定義之範本清單內範本的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3701a-141">An identifier that uniquely identifies the template within the list of templates that the provider defines.</span></span> <span data-ttu-id="3701a-142">當您定義事件定義時，請使用這個名稱來參考範本。</span><span class="sxs-lookup"><span data-stu-id="3701a-142">Use this name to reference the template when you define your event definition.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="3701a-143">備註</span><span class="sxs-lookup"><span data-stu-id="3701a-143">Remarks</span></span>

<span data-ttu-id="3701a-144">範本定義必須至少有一個資料或結構子項目。</span><span class="sxs-lookup"><span data-stu-id="3701a-144">The template definition must have at least one data or struct child element.</span></span> <span data-ttu-id="3701a-145">提供者必須以範本中定義之資料項目的順序來寫入事件資料。</span><span class="sxs-lookup"><span data-stu-id="3701a-145">The provider must write the event data in the order of the data items defined in the template.</span></span>

<span data-ttu-id="3701a-146">範本中所有資料項目的大小必須小於 64 KB。</span><span class="sxs-lookup"><span data-stu-id="3701a-146">The size of all the data items in the template must be less than 64 KB.</span></span>

## <a name="examples"></a><span data-ttu-id="3701a-147">範例</span><span class="sxs-lookup"><span data-stu-id="3701a-147">Examples</span></span>

<span data-ttu-id="3701a-148">下列範例顯示如何建立範本定義。</span><span class="sxs-lookup"><span data-stu-id="3701a-148">The following example shows how to create a template definition.</span></span>


```XML
<templates>
   <template tid="T1">
       <data name="PrinterName" intype="win:UnicodeString" />
       <UserData>
          <PrinterConnectionFailure 
              xmlns="schemas.microsoft.com/schemas/event/Microsoft.Windows.PrintSpooler/1.0.1.0/6382e26fc390d748">
              <PrinterName>%1</PrinterName>
          </PrinterConnectionFailure>
       </xml>
   </template>
</templates>
```



## <a name="requirements"></a><span data-ttu-id="3701a-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="3701a-149">Requirements</span></span>



| <span data-ttu-id="3701a-150">需求</span><span class="sxs-lookup"><span data-stu-id="3701a-150">Requirement</span></span> | <span data-ttu-id="3701a-151">值</span><span class="sxs-lookup"><span data-stu-id="3701a-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="3701a-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3701a-152">Minimum supported client</span></span><br/> | <span data-ttu-id="3701a-153">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3701a-153">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="3701a-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3701a-154">Minimum supported server</span></span><br/> | <span data-ttu-id="3701a-155">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3701a-155">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





