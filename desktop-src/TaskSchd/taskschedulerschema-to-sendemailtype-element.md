---
title: " (sendEmailType) 元素"
description: 包含要將電子郵件傳送至其中的電子郵件地址。
ms.assetid: bf3aa878-967b-4ebd-9397-a2a499686a9f
keywords:
- To 元素工作排程器
topic_type:
- apiref
api_name:
- To
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b9e0643220915ecb1c8f2cd1fe842e0dc3f21d8f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106995576"
---
# <a name="to-sendemailtype-element"></a><span data-ttu-id="2eb1f-104"> (sendEmailType) 元素</span><span class="sxs-lookup"><span data-stu-id="2eb1f-104">To (sendEmailType) Element</span></span>

<span data-ttu-id="2eb1f-105">包含要將電子郵件傳送至其中的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="2eb1f-105">Contains the email addresses to which the email will be sent.</span></span>

``` syntax
<xs:element name="To"
    type="string"
 />
```

<span data-ttu-id="2eb1f-106">**To** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="2eb1f-106">The **To** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2eb1f-107">父元素</span><span class="sxs-lookup"><span data-stu-id="2eb1f-107">Parent element</span></span>



| <span data-ttu-id="2eb1f-108">元素</span><span class="sxs-lookup"><span data-stu-id="2eb1f-108">Element</span></span>                                                                              | <span data-ttu-id="2eb1f-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="2eb1f-109">Derived from</span></span>                                                           | <span data-ttu-id="2eb1f-110">Description</span><span class="sxs-lookup"><span data-stu-id="2eb1f-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="2eb1f-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="2eb1f-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="2eb1f-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="2eb1f-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="2eb1f-113">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="2eb1f-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2eb1f-114">備註</span><span class="sxs-lookup"><span data-stu-id="2eb1f-114">Remarks</span></span>

<span data-ttu-id="2eb1f-115">針對 c + + 開發，請參閱 [**IEmailAction 的屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to)。</span><span class="sxs-lookup"><span data-stu-id="2eb1f-115">For C++ development, see [**To Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_to).</span></span>

<span data-ttu-id="2eb1f-116">如需腳本開發，請參閱 [**EmailAction.To**](emailaction-to.md)。</span><span class="sxs-lookup"><span data-stu-id="2eb1f-116">For script development, see [**EmailAction.To**](emailaction-to.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2eb1f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="2eb1f-117">Requirements</span></span>



| <span data-ttu-id="2eb1f-118">需求</span><span class="sxs-lookup"><span data-stu-id="2eb1f-118">Requirement</span></span> | <span data-ttu-id="2eb1f-119">值</span><span class="sxs-lookup"><span data-stu-id="2eb1f-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2eb1f-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2eb1f-120">Minimum supported client</span></span><br/> | <span data-ttu-id="2eb1f-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eb1f-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2eb1f-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2eb1f-122">Minimum supported server</span></span><br/> | <span data-ttu-id="2eb1f-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2eb1f-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





