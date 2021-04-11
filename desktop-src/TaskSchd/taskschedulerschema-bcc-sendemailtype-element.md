---
title: 密件副本 (sendEmailType) 元素
description: 包含電子郵件訊息的密件副本行上使用的電子郵件地址。
ms.assetid: c80407d0-3b3f-4efe-91de-7a3a7abc996f
keywords:
- 密件副本元素工作排程器
topic_type:
- apiref
api_name:
- Bcc
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: f262b8f5d74018a4622f915def85df5e16108cdb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104351"
---
# <a name="bcc-sendemailtype-element"></a><span data-ttu-id="555c4-104">密件副本 (sendEmailType) 元素</span><span class="sxs-lookup"><span data-stu-id="555c4-104">Bcc (sendEmailType) Element</span></span>

<span data-ttu-id="555c4-105">包含電子郵件訊息的密件副本行上使用的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="555c4-105">Contains the email addresses used on the Bcc line of an email message.</span></span>

``` syntax
<xs:element name="Bcc"
    type="string"
 />
```

<span data-ttu-id="555c4-106">**密件副本** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="555c4-106">The **Bcc** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="555c4-107">父元素</span><span class="sxs-lookup"><span data-stu-id="555c4-107">Parent element</span></span>



| <span data-ttu-id="555c4-108">元素</span><span class="sxs-lookup"><span data-stu-id="555c4-108">Element</span></span>                                                                              | <span data-ttu-id="555c4-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="555c4-109">Derived from</span></span>                                                           | <span data-ttu-id="555c4-110">Description</span><span class="sxs-lookup"><span data-stu-id="555c4-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="555c4-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="555c4-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="555c4-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="555c4-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="555c4-113">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="555c4-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="555c4-114">備註</span><span class="sxs-lookup"><span data-stu-id="555c4-114">Remarks</span></span>

<span data-ttu-id="555c4-115">針對 c + + 開發，請參閱 [**IEmailAction 的 [密件副本] 屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc)。</span><span class="sxs-lookup"><span data-stu-id="555c4-115">For C++ development, see [**Bcc Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_bcc).</span></span>

<span data-ttu-id="555c4-116">如需腳本開發，請參閱 [**EmailAction。**](emailaction-bcc.md)</span><span class="sxs-lookup"><span data-stu-id="555c4-116">For script development, see [**EmailAction.Bcc**](emailaction-bcc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="555c4-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="555c4-117">Requirements</span></span>



| <span data-ttu-id="555c4-118">需求</span><span class="sxs-lookup"><span data-stu-id="555c4-118">Requirement</span></span> | <span data-ttu-id="555c4-119">值</span><span class="sxs-lookup"><span data-stu-id="555c4-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="555c4-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="555c4-120">Minimum supported client</span></span><br/> | <span data-ttu-id="555c4-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="555c4-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="555c4-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="555c4-122">Minimum supported server</span></span><br/> | <span data-ttu-id="555c4-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="555c4-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





