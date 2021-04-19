---
title: SendEmailType) 元素的內文 (主體
description: 包含電子郵件訊息主體中的文字。
ms.assetid: fac6ddd5-6f73-427b-b213-ab946512c87a
keywords:
- Body 元素工作排程器
topic_type:
- apiref
api_name:
- Body
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4659f2ff03f69b6bba40d9cd16e9b68515cc8889
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966512"
---
# <a name="body-sendemailtype-element"></a><span data-ttu-id="c072a-104">SendEmailType) 元素的內文 (主體</span><span class="sxs-lookup"><span data-stu-id="c072a-104">Body (sendEmailType) Element</span></span>

<span data-ttu-id="c072a-105">包含電子郵件訊息主體中的文字。</span><span class="sxs-lookup"><span data-stu-id="c072a-105">Contains the text in the body of the email message.</span></span>

``` syntax
<xs:element name="Body"
    type="string"
 />
```

<span data-ttu-id="c072a-106">**Body** 專案是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="c072a-106">The **Body** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="c072a-107">父元素</span><span class="sxs-lookup"><span data-stu-id="c072a-107">Parent element</span></span>



| <span data-ttu-id="c072a-108">元素</span><span class="sxs-lookup"><span data-stu-id="c072a-108">Element</span></span>                                                                              | <span data-ttu-id="c072a-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="c072a-109">Derived from</span></span>                                                           | <span data-ttu-id="c072a-110">Description</span><span class="sxs-lookup"><span data-stu-id="c072a-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="c072a-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="c072a-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="c072a-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="c072a-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="c072a-113">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="c072a-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="c072a-114">備註</span><span class="sxs-lookup"><span data-stu-id="c072a-114">Remarks</span></span>

<span data-ttu-id="c072a-115">針對 c + + 開發，請參閱 [**IEmailAction 的 Body 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body)。</span><span class="sxs-lookup"><span data-stu-id="c072a-115">For C++ development, see [**Body Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_body).</span></span>

<span data-ttu-id="c072a-116">如需腳本開發，請參閱 [**EmailAction。**](emailaction-body.md)</span><span class="sxs-lookup"><span data-stu-id="c072a-116">For script development, see [**EmailAction.Body**](emailaction-body.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c072a-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="c072a-117">Requirements</span></span>



| <span data-ttu-id="c072a-118">需求</span><span class="sxs-lookup"><span data-stu-id="c072a-118">Requirement</span></span> | <span data-ttu-id="c072a-119">值</span><span class="sxs-lookup"><span data-stu-id="c072a-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="c072a-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c072a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="c072a-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c072a-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="c072a-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c072a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="c072a-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c072a-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





