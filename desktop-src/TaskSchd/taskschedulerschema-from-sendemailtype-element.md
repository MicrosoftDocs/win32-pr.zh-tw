---
title: 從 (sendEmailType) 元素
description: 包含電子郵件寄件者的電子郵件地址。
ms.assetid: b80733de-e050-4026-a2fe-f63833ec2660
keywords:
- From 元素工作排程器
topic_type:
- apiref
api_name:
- From
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 9f50704212fe6a4fec7ce0fc21bacd7ea33e402c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024882"
---
# <a name="from-sendemailtype-element"></a><span data-ttu-id="da2db-104">從 (sendEmailType) 元素</span><span class="sxs-lookup"><span data-stu-id="da2db-104">From (sendEmailType) Element</span></span>

<span data-ttu-id="da2db-105">包含電子郵件寄件者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="da2db-105">Contains the email address of the email sender.</span></span>

``` syntax
<xs:element name="From"
    type="string"
 />
```

<span data-ttu-id="da2db-106">**From** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="da2db-106">The **From** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="da2db-107">父元素</span><span class="sxs-lookup"><span data-stu-id="da2db-107">Parent element</span></span>



| <span data-ttu-id="da2db-108">元素</span><span class="sxs-lookup"><span data-stu-id="da2db-108">Element</span></span>                                                                              | <span data-ttu-id="da2db-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="da2db-109">Derived from</span></span>                                                           | <span data-ttu-id="da2db-110">Description</span><span class="sxs-lookup"><span data-stu-id="da2db-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="da2db-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="da2db-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="da2db-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="da2db-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="da2db-113">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="da2db-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="da2db-114">備註</span><span class="sxs-lookup"><span data-stu-id="da2db-114">Remarks</span></span>

<span data-ttu-id="da2db-115">針對 c + + 開發，請參閱 [**IEmailAction 的 From 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from)。</span><span class="sxs-lookup"><span data-stu-id="da2db-115">For C++ development, see [**From Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_from).</span></span>

<span data-ttu-id="da2db-116">如需腳本開發，請參閱 [**EmailAction。**](emailaction-from.md)</span><span class="sxs-lookup"><span data-stu-id="da2db-116">For script development, see [**EmailAction.From**](emailaction-from.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="da2db-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="da2db-117">Requirements</span></span>



| <span data-ttu-id="da2db-118">需求</span><span class="sxs-lookup"><span data-stu-id="da2db-118">Requirement</span></span> | <span data-ttu-id="da2db-119">值</span><span class="sxs-lookup"><span data-stu-id="da2db-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="da2db-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="da2db-120">Minimum supported client</span></span><br/> | <span data-ttu-id="da2db-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da2db-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="da2db-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="da2db-122">Minimum supported server</span></span><br/> | <span data-ttu-id="da2db-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="da2db-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





