---
title: ReplyTo (sendEmailType) 元素
description: 包含在電子郵件訊息中回復的電子郵件地址。
ms.assetid: c09b72f6-de2c-41dc-942c-d6184863e33c
keywords:
- ReplyTo 元素工作排程器
topic_type:
- apiref
api_name:
- ReplyTo
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 02055539d4557a60f182981f0d9cd7d3e1a63ca4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106356"
---
# <a name="replyto-sendemailtype-element"></a><span data-ttu-id="f0f6a-104">ReplyTo (sendEmailType) 元素</span><span class="sxs-lookup"><span data-stu-id="f0f6a-104">ReplyTo (sendEmailType) Element</span></span>

<span data-ttu-id="f0f6a-105">包含在電子郵件訊息中回復的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="f0f6a-105">Contains the email addresses that are replied to in the email message.</span></span>

``` syntax
<xs:element name="ReplyTo"
    type="string"
 />
```

<span data-ttu-id="f0f6a-106">**ReplyTo** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="f0f6a-106">The **ReplyTo** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f0f6a-107">父元素</span><span class="sxs-lookup"><span data-stu-id="f0f6a-107">Parent element</span></span>



| <span data-ttu-id="f0f6a-108">元素</span><span class="sxs-lookup"><span data-stu-id="f0f6a-108">Element</span></span>                                                                              | <span data-ttu-id="f0f6a-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="f0f6a-109">Derived from</span></span>                                                           | <span data-ttu-id="f0f6a-110">Description</span><span class="sxs-lookup"><span data-stu-id="f0f6a-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="f0f6a-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="f0f6a-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="f0f6a-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="f0f6a-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="f0f6a-113">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="f0f6a-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f0f6a-114">備註</span><span class="sxs-lookup"><span data-stu-id="f0f6a-114">Remarks</span></span>

<span data-ttu-id="f0f6a-115">針對 c + + 開發，請參閱 [**IEmailAction 的 ReplyTo 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto)。</span><span class="sxs-lookup"><span data-stu-id="f0f6a-115">For C++ development, see [**ReplyTo Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_replyto).</span></span>

<span data-ttu-id="f0f6a-116">如需腳本開發，請參閱 [**EmailAction。**](emailaction-replyto.md)</span><span class="sxs-lookup"><span data-stu-id="f0f6a-116">For script development, see [**EmailAction.ReplyTo**](emailaction-replyto.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f0f6a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0f6a-117">Requirements</span></span>



| <span data-ttu-id="f0f6a-118">需求</span><span class="sxs-lookup"><span data-stu-id="f0f6a-118">Requirement</span></span> | <span data-ttu-id="f0f6a-119">值</span><span class="sxs-lookup"><span data-stu-id="f0f6a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f0f6a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0f6a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f0f6a-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0f6a-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f0f6a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0f6a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f0f6a-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0f6a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





