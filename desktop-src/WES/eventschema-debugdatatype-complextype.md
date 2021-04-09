---
title: DebugDataType 複雜類型
description: 定義可以針對 Windows 軟體追蹤預處理器 (的 WPP) 事件記錄的資料。
ms.assetid: 75638e0f-7a26-473e-a0c4-bd8972ac171f
keywords:
- DebugDataType 複雜類型 EventLog
topic_type:
- apiref
api_name:
- DebugDataType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c190d3b2b0e870ac249fed03485828685d5dc770
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024521"
---
# <a name="debugdatatype-complex-type"></a><span data-ttu-id="31391-104">DebugDataType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="31391-104">DebugDataType Complex Type</span></span>

<span data-ttu-id="31391-105">定義可以針對 Windows 軟體追蹤預處理器 (的 WPP) 事件記錄的資料。</span><span class="sxs-lookup"><span data-stu-id="31391-105">Defines the data that can be logged for Windows software trace preprocessor (WPP) events.</span></span>

``` syntax
<xs:complexType name="DebugDataType">
    <xs:sequence>
        <xs:element name="SequenceNumber"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="FlagsName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="LevelName"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Component"
            type="string"
         />
        <xs:element name="SubComponent"
            type="string"
            minOccurs="0"
         />
        <xs:element name="FileLine"
            type="string"
            minOccurs="0"
         />
        <xs:element name="Function"
            type="unsignedInt"
            minOccurs="0"
         />
        <xs:element name="Message"
            type="string"
         />
        <xs:any
            minOccurs="0"
            maxOccurs="unbounded"
            processContents="lax"
            namespace="##other"
         />
    </xs:sequence>
    <xs:anyAttribute
        processContents="lax"
        namespace="##other"
     />
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="31391-106">子元素</span><span class="sxs-lookup"><span data-stu-id="31391-106">Child elements</span></span>



| <span data-ttu-id="31391-107">元素</span><span class="sxs-lookup"><span data-stu-id="31391-107">Element</span></span>                                                                    | <span data-ttu-id="31391-108">類型</span><span class="sxs-lookup"><span data-stu-id="31391-108">Type</span></span>        | <span data-ttu-id="31391-109">Description</span><span class="sxs-lookup"><span data-stu-id="31391-109">Description</span></span>                                                                                                        |
|----------------------------------------------------------------------------|-------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="31391-110">**元件**</span><span class="sxs-lookup"><span data-stu-id="31391-110">**Component**</span></span>](eventschema-component-debugdatatype-element.md)           | <span data-ttu-id="31391-111">字串</span><span class="sxs-lookup"><span data-stu-id="31391-111">string</span></span>      | <span data-ttu-id="31391-112">記錄追蹤訊息的元件名稱。</span><span class="sxs-lookup"><span data-stu-id="31391-112">The name of the component that logged the trace message.</span></span><br/>                                                |
| [<span data-ttu-id="31391-113">**FileLine**</span><span class="sxs-lookup"><span data-stu-id="31391-113">**FileLine**</span></span>](eventschema-fileline-debugdatatype-element.md)             | <span data-ttu-id="31391-114">字串</span><span class="sxs-lookup"><span data-stu-id="31391-114">string</span></span>      | <span data-ttu-id="31391-115">來源檔案的名稱，以及記錄追蹤訊息之原始程式檔內的行。</span><span class="sxs-lookup"><span data-stu-id="31391-115">The name of the source file and the line within the source file that logged the trace message.</span></span><br/>          |
| [<span data-ttu-id="31391-116">**FlagsName**</span><span class="sxs-lookup"><span data-stu-id="31391-116">**FlagsName**</span></span>](eventschema-flagname-debugdatatype-element.md)            | <span data-ttu-id="31391-117">字串</span><span class="sxs-lookup"><span data-stu-id="31391-117">string</span></span>      | <span data-ttu-id="31391-118">啟用時傳遞給提供者的旗標值。</span><span class="sxs-lookup"><span data-stu-id="31391-118">The flag value passed to the provider when it was enabled.</span></span><br/>                                              |
| [<span data-ttu-id="31391-119">**功能**</span><span class="sxs-lookup"><span data-stu-id="31391-119">**Function**</span></span>](eventschema-function-debugdatatype-element.md)             | <span data-ttu-id="31391-120">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="31391-120">unsignedInt</span></span> | <span data-ttu-id="31391-121">記錄追蹤訊息的函數名稱。</span><span class="sxs-lookup"><span data-stu-id="31391-121">The name of the function that logged the trace message.</span></span><br/>                                                 |
| [<span data-ttu-id="31391-122">**LevelName**</span><span class="sxs-lookup"><span data-stu-id="31391-122">**LevelName**</span></span>](eventschema-levelname-debugdatatype-element.md)           | <span data-ttu-id="31391-123">字串</span><span class="sxs-lookup"><span data-stu-id="31391-123">string</span></span>      | <span data-ttu-id="31391-124">啟用時傳遞給提供者的層級值。</span><span class="sxs-lookup"><span data-stu-id="31391-124">The level value passed to the provider when it was enabled.</span></span><br/>                                             |
| [<span data-ttu-id="31391-125">**消息**</span><span class="sxs-lookup"><span data-stu-id="31391-125">**Message**</span></span>](eventschema-message-debugdatatype-element.md)               | <span data-ttu-id="31391-126">字串</span><span class="sxs-lookup"><span data-stu-id="31391-126">string</span></span>      | <span data-ttu-id="31391-127">訊息字串。</span><span class="sxs-lookup"><span data-stu-id="31391-127">The message string.</span></span> <span data-ttu-id="31391-128">如果 WPP 事件指定了 FormattedString 欄位，XML 就會包含這個元素。</span><span class="sxs-lookup"><span data-stu-id="31391-128">The XML contains this element if the WPP event specified the FormattedString field.</span></span><br/> |
| [<span data-ttu-id="31391-129">**SequenceNumber**</span><span class="sxs-lookup"><span data-stu-id="31391-129">**SequenceNumber**</span></span>](eventschema-sequencenumber-debugdatatype-element.md) | <span data-ttu-id="31391-130">unsignedInt</span><span class="sxs-lookup"><span data-stu-id="31391-130">unsignedInt</span></span> | <span data-ttu-id="31391-131">追蹤訊息的本機或全域序號。</span><span class="sxs-lookup"><span data-stu-id="31391-131">The local or global sequence number of the trace message.</span></span><br/>                                               |
| [<span data-ttu-id="31391-132">**子元件**</span><span class="sxs-lookup"><span data-stu-id="31391-132">**SubComponent**</span></span>](eventschema-subcomponent-debugdatatype-element.md)     | <span data-ttu-id="31391-133">字串</span><span class="sxs-lookup"><span data-stu-id="31391-133">string</span></span>      | <span data-ttu-id="31391-134">記錄追蹤訊息的子元件名稱。</span><span class="sxs-lookup"><span data-stu-id="31391-134">The name of the subcomponent that logged the trace message.</span></span><br/>                                             |



## <a name="remarks"></a><span data-ttu-id="31391-135">備註</span><span class="sxs-lookup"><span data-stu-id="31391-135">Remarks</span></span>

<span data-ttu-id="31391-136">只有在提供者將% TRACE \_ 格式 \_ 前置詞% 環境變數設定為包含這些專案時，才會包含這些元素。</span><span class="sxs-lookup"><span data-stu-id="31391-136">The elements are included only if the provider set the %TRACE\_FORMAT\_PREFIX% environment variable to include them.</span></span> <span data-ttu-id="31391-137">如需這些元素的詳細資訊，請參閱追蹤訊息前置詞。</span><span class="sxs-lookup"><span data-stu-id="31391-137">For details on these elements, see Trace Message Prefix.</span></span>

## <a name="requirements"></a><span data-ttu-id="31391-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="31391-138">Requirements</span></span>



| <span data-ttu-id="31391-139">需求</span><span class="sxs-lookup"><span data-stu-id="31391-139">Requirement</span></span> | <span data-ttu-id="31391-140">值</span><span class="sxs-lookup"><span data-stu-id="31391-140">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="31391-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="31391-141">Minimum supported client</span></span><br/> | <span data-ttu-id="31391-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31391-142">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="31391-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="31391-143">Minimum supported server</span></span><br/> | <span data-ttu-id="31391-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="31391-144">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





