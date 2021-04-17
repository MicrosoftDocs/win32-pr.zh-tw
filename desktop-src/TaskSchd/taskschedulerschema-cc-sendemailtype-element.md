---
title: Cc (sendEmailType) 元素
description: 包含電子郵件訊息之 Cc 行上使用的電子郵件地址。
ms.assetid: cb8bc5b3-c352-43e3-bf28-d2090a519c7f
keywords:
- Cc 元素工作排程器
topic_type:
- apiref
api_name:
- Cc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bc49f2d7eebc2fbb1b5818fee2efa0e54f579a8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466025"
---
# <a name="cc-sendemailtype-element"></a><span data-ttu-id="f5c0d-104">Cc (sendEmailType) 元素</span><span class="sxs-lookup"><span data-stu-id="f5c0d-104">Cc (sendEmailType) Element</span></span>

<span data-ttu-id="f5c0d-105">包含電子郵件訊息之 Cc 行上使用的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="f5c0d-105">Contains the email addresses used on the Cc line of an email message.</span></span>

``` syntax
<xs:element name="Cc"
    type="string"
 />
```

<span data-ttu-id="f5c0d-106">**Cc** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="f5c0d-106">The **Cc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="f5c0d-107">父元素</span><span class="sxs-lookup"><span data-stu-id="f5c0d-107">Parent element</span></span>



| <span data-ttu-id="f5c0d-108">元素</span><span class="sxs-lookup"><span data-stu-id="f5c0d-108">Element</span></span>                                                                              | <span data-ttu-id="f5c0d-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="f5c0d-109">Derived from</span></span>                                                           | <span data-ttu-id="f5c0d-110">Description</span><span class="sxs-lookup"><span data-stu-id="f5c0d-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="f5c0d-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="f5c0d-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="f5c0d-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="f5c0d-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="f5c0d-113">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="f5c0d-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f5c0d-114">備註</span><span class="sxs-lookup"><span data-stu-id="f5c0d-114">Remarks</span></span>

<span data-ttu-id="f5c0d-115">針對 c + + 開發，請參閱 [**IEmailAction 的 Cc 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc)。</span><span class="sxs-lookup"><span data-stu-id="f5c0d-115">For C++ development, see [**Cc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_cc).</span></span>

<span data-ttu-id="f5c0d-116">如需腳本開發，請參閱 [**EmailAction.Cc**](emailaction-cc.md)。</span><span class="sxs-lookup"><span data-stu-id="f5c0d-116">For script development, see [**EmailAction.Cc**](emailaction-cc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f5c0d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5c0d-117">Requirements</span></span>



| <span data-ttu-id="f5c0d-118">需求</span><span class="sxs-lookup"><span data-stu-id="f5c0d-118">Requirement</span></span> | <span data-ttu-id="f5c0d-119">值</span><span class="sxs-lookup"><span data-stu-id="f5c0d-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f5c0d-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5c0d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="f5c0d-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5c0d-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f5c0d-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5c0d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="f5c0d-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5c0d-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





