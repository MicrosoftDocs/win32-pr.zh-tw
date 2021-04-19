---
title: HeaderField (headerFieldsType) 元素
description: 在電子郵件訊息中包含標頭的欄位。
ms.assetid: ec6fc593-8798-4dd0-b589-48657b7cdeb1
keywords:
- HeaderField 元素工作排程器
topic_type:
- apiref
api_name:
- HeaderField
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 1f7ac79a16bb0464f6e81d90eba38384a3c2b483
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970463"
---
# <a name="headerfield-headerfieldstype-element"></a><span data-ttu-id="678bd-104">HeaderField (headerFieldsType) 元素</span><span class="sxs-lookup"><span data-stu-id="678bd-104">HeaderField (headerFieldsType) Element</span></span>

<span data-ttu-id="678bd-105">在電子郵件訊息中包含標頭的欄位。</span><span class="sxs-lookup"><span data-stu-id="678bd-105">Contains a field for a header in an email message.</span></span>

``` syntax
<xs:element name="HeaderField"
    type="headerFieldType"
 />
```

<span data-ttu-id="678bd-106">**HeaderField** 元素是由 [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="678bd-106">The **HeaderField** element is defined by the [**headerFieldsType**](taskschedulerschema-headerfieldstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="678bd-107">父元素</span><span class="sxs-lookup"><span data-stu-id="678bd-107">Parent element</span></span>



| <span data-ttu-id="678bd-108">元素</span><span class="sxs-lookup"><span data-stu-id="678bd-108">Element</span></span>                                                                        | <span data-ttu-id="678bd-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="678bd-109">Derived from</span></span>                                                                 | <span data-ttu-id="678bd-110">Description</span><span class="sxs-lookup"><span data-stu-id="678bd-110">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="678bd-111">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="678bd-111">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="678bd-112">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="678bd-112">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="678bd-113">指定標頭欄位，以及在電子郵件訊息的標頭中使用的值。</span><span class="sxs-lookup"><span data-stu-id="678bd-113">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="678bd-114">子元素</span><span class="sxs-lookup"><span data-stu-id="678bd-114">Child elements</span></span>



| <span data-ttu-id="678bd-115">元素</span><span class="sxs-lookup"><span data-stu-id="678bd-115">Element</span></span>                                                            | <span data-ttu-id="678bd-116">類型</span><span class="sxs-lookup"><span data-stu-id="678bd-116">Type</span></span>                                                                    | <span data-ttu-id="678bd-117">Description</span><span class="sxs-lookup"><span data-stu-id="678bd-117">Description</span></span>                                                            |
|--------------------------------------------------------------------|-------------------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="678bd-118">**Name**</span><span class="sxs-lookup"><span data-stu-id="678bd-118">**Name**</span></span>](taskschedulerschema-name-headerfieldtype-element.md)   | [<span data-ttu-id="678bd-119">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="678bd-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="678bd-120">在電子郵件訊息中指定標頭欄位的名稱。</span><span class="sxs-lookup"><span data-stu-id="678bd-120">Specifies the name of the header field in an email message.</span></span><br/> |
| [<span data-ttu-id="678bd-121">**值**</span><span class="sxs-lookup"><span data-stu-id="678bd-121">**Value**</span></span>](taskschedulerschema-value-headerfieldtype-element.md) | <span data-ttu-id="678bd-122">**string**</span><span class="sxs-lookup"><span data-stu-id="678bd-122">**string**</span></span>                                                              | <span data-ttu-id="678bd-123">指定電子郵件訊息中標頭欄位的值。</span><span class="sxs-lookup"><span data-stu-id="678bd-123">Specifies the value of a header field in an email message.</span></span><br/>  |



## <a name="remarks"></a><span data-ttu-id="678bd-124">備註</span><span class="sxs-lookup"><span data-stu-id="678bd-124">Remarks</span></span>

<span data-ttu-id="678bd-125">針對 c + + 開發，請參閱 [**IEmailAction 的 HeaderFields 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields)。</span><span class="sxs-lookup"><span data-stu-id="678bd-125">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="678bd-126">如需腳本開發，請參閱 [**EmailAction. HeaderFields**](emailaction-headerfields.md)。</span><span class="sxs-lookup"><span data-stu-id="678bd-126">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="678bd-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="678bd-127">Requirements</span></span>



| <span data-ttu-id="678bd-128">需求</span><span class="sxs-lookup"><span data-stu-id="678bd-128">Requirement</span></span> | <span data-ttu-id="678bd-129">值</span><span class="sxs-lookup"><span data-stu-id="678bd-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="678bd-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="678bd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="678bd-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="678bd-131">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="678bd-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="678bd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="678bd-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="678bd-133">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





