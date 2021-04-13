---
title: HeaderFields (sendEmailType) 元素
description: 指定標頭欄位，以及在電子郵件訊息的標頭中使用的值。
ms.assetid: 6261f32e-3012-4ce7-b407-699374596333
keywords:
- HeaderFields 元素工作排程器
topic_type:
- apiref
api_name:
- HeaderFields
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9d108f1c31b8253046ccdbf09312df4f54c7335d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508851"
---
# <a name="headerfields-sendemailtype-element"></a><span data-ttu-id="853ed-104">HeaderFields (sendEmailType) 元素</span><span class="sxs-lookup"><span data-stu-id="853ed-104">HeaderFields (sendEmailType) Element</span></span>

<span data-ttu-id="853ed-105">指定標頭欄位，以及在電子郵件訊息的標頭中使用的值。</span><span class="sxs-lookup"><span data-stu-id="853ed-105">Specifies the header fields and their values used in the header of the email message.</span></span>

``` syntax
<xs:element name="HeaderFields"
    type="headerFieldsType"
 />
```

<span data-ttu-id="853ed-106">**HeaderFields** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="853ed-106">The **HeaderFields** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="853ed-107">父元素</span><span class="sxs-lookup"><span data-stu-id="853ed-107">Parent element</span></span>



| <span data-ttu-id="853ed-108">元素</span><span class="sxs-lookup"><span data-stu-id="853ed-108">Element</span></span>                                                                              | <span data-ttu-id="853ed-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="853ed-109">Derived from</span></span>                                                           | <span data-ttu-id="853ed-110">Description</span><span class="sxs-lookup"><span data-stu-id="853ed-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="853ed-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="853ed-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="853ed-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="853ed-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="853ed-113">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="853ed-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="853ed-114">子元素</span><span class="sxs-lookup"><span data-stu-id="853ed-114">Child elements</span></span>



| <span data-ttu-id="853ed-115">元素</span><span class="sxs-lookup"><span data-stu-id="853ed-115">Element</span></span>                                                                         | <span data-ttu-id="853ed-116">類型</span><span class="sxs-lookup"><span data-stu-id="853ed-116">Type</span></span>                                                                       | <span data-ttu-id="853ed-117">Description</span><span class="sxs-lookup"><span data-stu-id="853ed-117">Description</span></span>                                                    |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------|----------------------------------------------------------------|
| [<span data-ttu-id="853ed-118">**HeaderField**</span><span class="sxs-lookup"><span data-stu-id="853ed-118">**HeaderField**</span></span>](taskschedulerschema-headerfield-headerfieldstype-element.md) | [<span data-ttu-id="853ed-119">**headerFieldType**</span><span class="sxs-lookup"><span data-stu-id="853ed-119">**headerFieldType**</span></span>](taskschedulerschema-headerfieldtype-complextype.md) | <span data-ttu-id="853ed-120">在電子郵件訊息中包含標頭的欄位。</span><span class="sxs-lookup"><span data-stu-id="853ed-120">Contains a field for a header in an email message.</span></span> <br/> |



## <a name="remarks"></a><span data-ttu-id="853ed-121">備註</span><span class="sxs-lookup"><span data-stu-id="853ed-121">Remarks</span></span>

<span data-ttu-id="853ed-122">針對 c + + 開發，請參閱 [**IEmailAction 的 HeaderFields 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields)。</span><span class="sxs-lookup"><span data-stu-id="853ed-122">For C++ development, see [**HeaderFields Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_headerfields).</span></span>

<span data-ttu-id="853ed-123">如需腳本開發，請參閱 [**EmailAction. HeaderFields**](emailaction-headerfields.md)。</span><span class="sxs-lookup"><span data-stu-id="853ed-123">For script development, see [**EmailAction.HeaderFields**](emailaction-headerfields.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="853ed-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="853ed-124">Requirements</span></span>



| <span data-ttu-id="853ed-125">需求</span><span class="sxs-lookup"><span data-stu-id="853ed-125">Requirement</span></span> | <span data-ttu-id="853ed-126">值</span><span class="sxs-lookup"><span data-stu-id="853ed-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="853ed-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="853ed-127">Minimum supported client</span></span><br/> | <span data-ttu-id="853ed-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="853ed-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="853ed-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="853ed-129">Minimum supported server</span></span><br/> | <span data-ttu-id="853ed-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="853ed-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





