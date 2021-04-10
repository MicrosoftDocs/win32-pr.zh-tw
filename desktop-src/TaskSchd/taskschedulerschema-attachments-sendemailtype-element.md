---
title: 附件 (sendEmailType) 元素
description: 包含電子郵件訊息中的附件清單。
ms.assetid: 5ae22481-af70-42eb-a964-e63d800be17d
keywords:
- 附件元素工作排程器
topic_type:
- apiref
api_name:
- Attachments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 67eed8f82f0caa27f44070bd109d4fa4560472eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686225"
---
# <a name="attachments-sendemailtype-element"></a><span data-ttu-id="5e688-104">附件 (sendEmailType) 元素</span><span class="sxs-lookup"><span data-stu-id="5e688-104">Attachments (sendEmailType) Element</span></span>

<span data-ttu-id="5e688-105">包含電子郵件訊息中的附件清單。</span><span class="sxs-lookup"><span data-stu-id="5e688-105">Contains a list of attachments in the email message.</span></span>

``` syntax
<xs:element name="Attachments"
    type="attachmentsType"
 />
```

<span data-ttu-id="5e688-106">**附件** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="5e688-106">The **Attachments** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="5e688-107">父元素</span><span class="sxs-lookup"><span data-stu-id="5e688-107">Parent element</span></span>



| <span data-ttu-id="5e688-108">元素</span><span class="sxs-lookup"><span data-stu-id="5e688-108">Element</span></span>                                                                              | <span data-ttu-id="5e688-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="5e688-109">Derived from</span></span>                                                           | <span data-ttu-id="5e688-110">Description</span><span class="sxs-lookup"><span data-stu-id="5e688-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="5e688-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="5e688-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="5e688-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="5e688-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="5e688-113">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="5e688-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="5e688-114">子元素</span><span class="sxs-lookup"><span data-stu-id="5e688-114">Child elements</span></span>



| <span data-ttu-id="5e688-115">元素</span><span class="sxs-lookup"><span data-stu-id="5e688-115">Element</span></span>                                                          | <span data-ttu-id="5e688-116">類型</span><span class="sxs-lookup"><span data-stu-id="5e688-116">Type</span></span>                                                                    | <span data-ttu-id="5e688-117">Description</span><span class="sxs-lookup"><span data-stu-id="5e688-117">Description</span></span>                                                                                |
|------------------------------------------------------------------|-------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="5e688-118">**檔案**</span><span class="sxs-lookup"><span data-stu-id="5e688-118">**File**</span></span>](taskschedulerschema-file-attachmentstype-element.md) | [<span data-ttu-id="5e688-119">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="5e688-119">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md) | <span data-ttu-id="5e688-120">指定以電子郵件訊息中的附件形式傳送之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="5e688-120">Specifies the path to a file that is sent as an attachment in an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="5e688-121">備註</span><span class="sxs-lookup"><span data-stu-id="5e688-121">Remarks</span></span>

<span data-ttu-id="5e688-122">針對 c + + 開發，請參閱 [**IEmailAction 的附件屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments)。</span><span class="sxs-lookup"><span data-stu-id="5e688-122">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="5e688-123">如需腳本開發，請參閱 [**EmailAction。**](emailaction-attachments.md)</span><span class="sxs-lookup"><span data-stu-id="5e688-123">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5e688-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5e688-124">Requirements</span></span>



| <span data-ttu-id="5e688-125">需求</span><span class="sxs-lookup"><span data-stu-id="5e688-125">Requirement</span></span> | <span data-ttu-id="5e688-126">值</span><span class="sxs-lookup"><span data-stu-id="5e688-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="5e688-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5e688-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5e688-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e688-128">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="5e688-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5e688-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5e688-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5e688-130">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





