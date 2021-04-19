---
title: StructDefinitionType 複雜類型
description: 定義結構，其中包含一個或多個您想要包含在事件中的資料項目。 |StructDefinitionType 複雜類型
ms.assetid: eb6b3682-1035-472b-8027-583d43c31748
keywords:
- StructDefinitionType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- StructDefinitionType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 01e739077d38dec94c0a407e5779bec90369ffb9
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "106997344"
---
# <a name="structdefinitiontype-complex-type"></a><span data-ttu-id="a54ef-105">StructDefinitionType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="a54ef-105">StructDefinitionType Complex Type</span></span>

<span data-ttu-id="a54ef-106">定義結構，其中包含一個或多個您想要包含在事件中的資料項目。</span><span class="sxs-lookup"><span data-stu-id="a54ef-106">Defines a structure that includes one or more data items that you want to include with the event.</span></span>

``` syntax
<xs:complexType name="StructDefinitionType"
    mixed="true"
>
    <xs:sequence>
        <xs:element name="data"
            type="DataDefinitionType"
            maxOccurs="unbounded"
         />
    </xs:sequence>
    <xs:attribute name="name"
        type="string"
        use="required"
     />
    <xs:attribute name="length"
        type="LengthType"
        use="optional"
     />
    <xs:attribute name="count"
        type="CountType"
        use="optional"
     />
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="a54ef-107">子元素</span><span class="sxs-lookup"><span data-stu-id="a54ef-107">Child elements</span></span>



| <span data-ttu-id="a54ef-108">元素</span><span class="sxs-lookup"><span data-stu-id="a54ef-108">Element</span></span>                                                               | <span data-ttu-id="a54ef-109">類型</span><span class="sxs-lookup"><span data-stu-id="a54ef-109">Type</span></span>                                                                             | <span data-ttu-id="a54ef-110">Description</span><span class="sxs-lookup"><span data-stu-id="a54ef-110">Description</span></span>                                                               |
|-----------------------------------------------------------------------|----------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="a54ef-111">**資料**</span><span class="sxs-lookup"><span data-stu-id="a54ef-111">**data**</span></span>](eventmanifestschema-data-structdefinitiontype-element.md) | [<span data-ttu-id="a54ef-112">**DataDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="a54ef-112">**DataDefinitionType**</span></span>](eventmanifestschema-datadefinitiontype-complextype.md) | <span data-ttu-id="a54ef-113">定義您想要包含在結構中的資料項目。</span><span class="sxs-lookup"><span data-stu-id="a54ef-113">Defines a data item that you want to include in the structure.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="a54ef-114">屬性</span><span class="sxs-lookup"><span data-stu-id="a54ef-114">Attributes</span></span>



| <span data-ttu-id="a54ef-115">名稱</span><span class="sxs-lookup"><span data-stu-id="a54ef-115">Name</span></span>   | <span data-ttu-id="a54ef-116">類型</span><span class="sxs-lookup"><span data-stu-id="a54ef-116">Type</span></span>                                                            | <span data-ttu-id="a54ef-117">描述</span><span class="sxs-lookup"><span data-stu-id="a54ef-117">Description</span></span>                                                                                                                                                                                                                                                                               |
|--------|-----------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a54ef-118">count</span><span class="sxs-lookup"><span data-stu-id="a54ef-118">count</span></span>  | [<span data-ttu-id="a54ef-119">**CountType**</span><span class="sxs-lookup"><span data-stu-id="a54ef-119">**CountType**</span></span>](eventmanifestschema-counttype-simpletype.md)   | <span data-ttu-id="a54ef-120">結構陣列中的元素數目。</span><span class="sxs-lookup"><span data-stu-id="a54ef-120">The number of elements in an array of structures.</span></span> <span data-ttu-id="a54ef-121">這個屬性指出結構正在定義結構的陣列。</span><span class="sxs-lookup"><span data-stu-id="a54ef-121">This attribute indicates that the structure is defining an array of structures.</span></span> <span data-ttu-id="a54ef-122">您可以指定包含計數之結構外部的實際計數或資料項目目名稱。</span><span class="sxs-lookup"><span data-stu-id="a54ef-122">You can specify the actual count or the name of a data item outside of the structure that contains the count.</span></span> <br/>                               |
| <span data-ttu-id="a54ef-123">長度</span><span class="sxs-lookup"><span data-stu-id="a54ef-123">length</span></span> | [<span data-ttu-id="a54ef-124">**LengthType**</span><span class="sxs-lookup"><span data-stu-id="a54ef-124">**LengthType**</span></span>](eventmanifestschema-lengthtype-simpletype.md) | <span data-ttu-id="a54ef-125">不適用。</span><span class="sxs-lookup"><span data-stu-id="a54ef-125">Not available.</span></span><br/> <span data-ttu-id="a54ef-126">**Windows Server 2008 和 Windows Vista：** 此結構的長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a54ef-126">**Windows Server 2008 and Windows Vista:** The length of this structure, in bytes.</span></span> <span data-ttu-id="a54ef-127">從 Windows 7 開始無法使用。</span><span class="sxs-lookup"><span data-stu-id="a54ef-127">Not available starting with Windows 7.</span></span><br/>                                                                                                                            |
| <span data-ttu-id="a54ef-128">NAME</span><span class="sxs-lookup"><span data-stu-id="a54ef-128">name</span></span>   | <span data-ttu-id="a54ef-129">字串</span><span class="sxs-lookup"><span data-stu-id="a54ef-129">string</span></span>                                                          | <span data-ttu-id="a54ef-130">結構的名稱。</span><span class="sxs-lookup"><span data-stu-id="a54ef-130">The name to the structure.</span></span> <span data-ttu-id="a54ef-131">如果您在範本中指定 [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) 區段，您可以使用名稱來參考 XML 片段中的資料項目。</span><span class="sxs-lookup"><span data-stu-id="a54ef-131">You can use the name to reference the data item in your XML fragment if you specify a [**UserData**](eventmanifestschema-userdata-templateitemtype-element.md) section in your template.</span></span><br/> <span data-ttu-id="a54ef-132">**Windows Vista：** 這個屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="a54ef-132">**Windows Vista:** This attribute is optional.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="a54ef-133">備註</span><span class="sxs-lookup"><span data-stu-id="a54ef-133">Remarks</span></span>

<span data-ttu-id="a54ef-134">提供者會將結構撰寫為 blob，而不是結構的個別成員。</span><span class="sxs-lookup"><span data-stu-id="a54ef-134">Providers write the structure as a blob and not as individual members of the structure.</span></span> <span data-ttu-id="a54ef-135">如果您所撰寫的 C 結構包含指標 (例如，型別 LPWSTR) 的指標，事件資料將會包含指標值，而不是已取值的資料。</span><span class="sxs-lookup"><span data-stu-id="a54ef-135">If the C structure that you are writing contains pointers (for example, a pointer of type LPWSTR), the event data will contain the pointer value, not the dereferenced data.</span></span>

<span data-ttu-id="a54ef-136">您不應該使用結構，而應該改為針對每個成員定義資料項目，然後個別撰寫這些資料項目。</span><span class="sxs-lookup"><span data-stu-id="a54ef-136">You should not use structures but instead should define data items for each member and write them separately.</span></span> <span data-ttu-id="a54ef-137">如果您決定要使用結構，則結構只應包含整數類資料類型，而您必須確保結構的成員符合8位元組的界限。</span><span class="sxs-lookup"><span data-stu-id="a54ef-137">If you decide to use structure, the structure should contain only integral types and you must ensure that the members of the structure align to an 8-byte boundary.</span></span> <span data-ttu-id="a54ef-138">如果不這麼做，當您嘗試存取資料時，可能會收到對齊錯誤。</span><span class="sxs-lookup"><span data-stu-id="a54ef-138">If you do not, you will likely receive alignment errors when you try to access the data.</span></span> <span data-ttu-id="a54ef-139">請考慮使用 \# pragma pack () 指示詞來強制在8位元組的界限上對齊。</span><span class="sxs-lookup"><span data-stu-id="a54ef-139">Consider using the \#pragma pack() directive to force alignment on an 8-byte boundary.</span></span>

## <a name="requirements"></a><span data-ttu-id="a54ef-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="a54ef-140">Requirements</span></span>



| <span data-ttu-id="a54ef-141">需求</span><span class="sxs-lookup"><span data-stu-id="a54ef-141">Requirement</span></span> | <span data-ttu-id="a54ef-142">值</span><span class="sxs-lookup"><span data-stu-id="a54ef-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a54ef-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a54ef-143">Minimum supported client</span></span><br/> | <span data-ttu-id="a54ef-144">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a54ef-144">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="a54ef-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a54ef-145">Minimum supported server</span></span><br/> | <span data-ttu-id="a54ef-146">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a54ef-146">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





