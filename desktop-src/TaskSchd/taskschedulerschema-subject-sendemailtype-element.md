---
title: Subject (sendEmailType) 元素
description: 包含電子郵件訊息的主旨。
ms.assetid: 2ccaa983-4dca-4e45-ba8d-2a93e23f7e8c
keywords:
- Subject 元素工作排程器
topic_type:
- apiref
api_name:
- Subject
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b3b4871f8d61603ea77c7699a9993d29e2fc0187
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104509442"
---
# <a name="subject-sendemailtype-element"></a><span data-ttu-id="566c5-104">Subject (sendEmailType) 元素</span><span class="sxs-lookup"><span data-stu-id="566c5-104">Subject (sendEmailType) Element</span></span>

<span data-ttu-id="566c5-105">包含電子郵件訊息的主旨。</span><span class="sxs-lookup"><span data-stu-id="566c5-105">Contains the subject of the email message.</span></span>

``` syntax
<xs:element name="Subject"
    type="string"
 />
```

<span data-ttu-id="566c5-106">**Subject** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="566c5-106">The **Subject** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="566c5-107">父元素</span><span class="sxs-lookup"><span data-stu-id="566c5-107">Parent element</span></span>



| <span data-ttu-id="566c5-108">元素</span><span class="sxs-lookup"><span data-stu-id="566c5-108">Element</span></span>                                                                              | <span data-ttu-id="566c5-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="566c5-109">Derived from</span></span>                                                           | <span data-ttu-id="566c5-110">Description</span><span class="sxs-lookup"><span data-stu-id="566c5-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="566c5-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="566c5-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="566c5-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="566c5-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="566c5-113">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="566c5-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="566c5-114">備註</span><span class="sxs-lookup"><span data-stu-id="566c5-114">Remarks</span></span>

<span data-ttu-id="566c5-115">針對 c + + 開發，請參閱 [**IEmailAction 的 Subject 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject)。</span><span class="sxs-lookup"><span data-stu-id="566c5-115">For C++ development, see [**Subject Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_subject).</span></span>

<span data-ttu-id="566c5-116">如需腳本開發，請參閱 [**EmailAction。**](emailaction-subject.md)</span><span class="sxs-lookup"><span data-stu-id="566c5-116">For script development, see [**EmailAction.Subject**](emailaction-subject.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="566c5-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="566c5-117">Requirements</span></span>



| <span data-ttu-id="566c5-118">需求</span><span class="sxs-lookup"><span data-stu-id="566c5-118">Requirement</span></span> | <span data-ttu-id="566c5-119">值</span><span class="sxs-lookup"><span data-stu-id="566c5-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="566c5-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="566c5-120">Minimum supported client</span></span><br/> | <span data-ttu-id="566c5-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="566c5-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="566c5-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="566c5-122">Minimum supported server</span></span><br/> | <span data-ttu-id="566c5-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="566c5-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





