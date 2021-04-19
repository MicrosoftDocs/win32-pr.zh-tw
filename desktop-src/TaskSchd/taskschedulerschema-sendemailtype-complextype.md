---
title: sendEmailType 複雜類型
description: 定義用來指定工作執行時將傳送電子郵件的動作類型。 此類型會定義用來建立電子郵件訊息模型的所有元素。
ms.assetid: e384971f-e7e4-4206-9d15-9555dfcbac2f
keywords:
- sendEmailType 複雜類型工作排程器
topic_type:
- apiref
api_name:
- sendEmailType
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 959e0b8f03223eb23b7a7bec69ba9b2aeea66447
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965331"
---
# <a name="sendemailtype-complex-type"></a><span data-ttu-id="27339-105">sendEmailType 複雜類型</span><span class="sxs-lookup"><span data-stu-id="27339-105">sendEmailType Complex Type</span></span>

<span data-ttu-id="27339-106">定義用來指定工作執行時將傳送電子郵件的動作類型。</span><span class="sxs-lookup"><span data-stu-id="27339-106">Defines the action type used to specify that an email will be sent when a task executes.</span></span> <span data-ttu-id="27339-107">此類型會定義用來建立電子郵件訊息模型的所有元素。</span><span class="sxs-lookup"><span data-stu-id="27339-107">This type defines all the elements used to model the email message.</span></span>

``` syntax
<xs:complexType name="sendEmailType">
    <xs:complexContent>
        <xs:extension
            base="actionBaseType"
        >
            <xs:all>
                <xs:element name="Server"
                    type="nonEmptyString"
                 />
                <xs:element name="Subject"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="To"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Cc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Bcc"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="ReplyTo"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="From"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="HeaderFields"
                    type="headerFieldsType"
                    minOccurs="0"
                 />
                <xs:element name="Body"
                    type="string"
                    minOccurs="0"
                 />
                <xs:element name="Attachments"
                    type="attachmentsType"
                    minOccurs="0"
                 />
            </xs:all>
        </xs:extension>
    </xs:complexContent>
</xs:complexType>
```

## <a name="child-elements"></a><span data-ttu-id="27339-108">子元素</span><span class="sxs-lookup"><span data-stu-id="27339-108">Child elements</span></span>



| <span data-ttu-id="27339-109">元素</span><span class="sxs-lookup"><span data-stu-id="27339-109">Element</span></span>                                                                        | <span data-ttu-id="27339-110">類型</span><span class="sxs-lookup"><span data-stu-id="27339-110">Type</span></span>                                                                         | <span data-ttu-id="27339-111">Description</span><span class="sxs-lookup"><span data-stu-id="27339-111">Description</span></span>                                                                                      |
|--------------------------------------------------------------------------------|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="27339-112">**附件**</span><span class="sxs-lookup"><span data-stu-id="27339-112">**Attachments**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md)   | [<span data-ttu-id="27339-113">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="27339-113">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md)   | <span data-ttu-id="27339-114">指定電子郵件訊息中的附件清單。</span><span class="sxs-lookup"><span data-stu-id="27339-114">Specifies a list of attachments in the email message.</span></span><br/>                                 |
| [<span data-ttu-id="27339-115">**密件副本**</span><span class="sxs-lookup"><span data-stu-id="27339-115">**Bcc**</span></span>](taskschedulerschema-bcc-sendemailtype-element.md)                   | <span data-ttu-id="27339-116">**string**</span><span class="sxs-lookup"><span data-stu-id="27339-116">**string**</span></span>                                                                   | <span data-ttu-id="27339-117">指定電子郵件訊息的 [密件副本] 行上使用的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="27339-117">Specifies the email addresses used on the Bcc line of an email message.</span></span><br/>               |
| [<span data-ttu-id="27339-118">**主體**</span><span class="sxs-lookup"><span data-stu-id="27339-118">**Body**</span></span>](taskschedulerschema-body-sendemailtype-element.md)                 | <span data-ttu-id="27339-119">**string**</span><span class="sxs-lookup"><span data-stu-id="27339-119">**string**</span></span>                                                                   | <span data-ttu-id="27339-120">指定電子郵件訊息主體中的文字。</span><span class="sxs-lookup"><span data-stu-id="27339-120">Specifies the text in the body of the email message.</span></span><br/>                                  |
| [<span data-ttu-id="27339-121">**Cc**</span><span class="sxs-lookup"><span data-stu-id="27339-121">**Cc**</span></span>](taskschedulerschema-cc-sendemailtype-element.md)                     | <span data-ttu-id="27339-122">**string**</span><span class="sxs-lookup"><span data-stu-id="27339-122">**string**</span></span>                                                                   | <span data-ttu-id="27339-123">指定電子郵件訊息之 Cc 行上使用的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="27339-123">Specifies the email addresses used on the Cc line of an email message.</span></span><br/>                |
| [<span data-ttu-id="27339-124">**寄件者**</span><span class="sxs-lookup"><span data-stu-id="27339-124">**From**</span></span>](taskschedulerschema-from-sendemailtype-element.md)                 | <span data-ttu-id="27339-125">**string**</span><span class="sxs-lookup"><span data-stu-id="27339-125">**string**</span></span>                                                                   | <span data-ttu-id="27339-126">指定寄件者的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="27339-126">Specifies the email address of the sender.</span></span><br/>                                            |
| [<span data-ttu-id="27339-127">**HeaderFields**</span><span class="sxs-lookup"><span data-stu-id="27339-127">**HeaderFields**</span></span>](taskschedulerschema-headerfields-sendemailtype-element.md) | [<span data-ttu-id="27339-128">**headerFieldsType**</span><span class="sxs-lookup"><span data-stu-id="27339-128">**headerFieldsType**</span></span>](taskschedulerschema-headerfieldstype-complextype.md) | <span data-ttu-id="27339-129">指定標頭欄位，以及在電子郵件訊息的標頭中使用的值。</span><span class="sxs-lookup"><span data-stu-id="27339-129">Specifies the header fields and their values used in the header of the email message.</span></span><br/> |
| [<span data-ttu-id="27339-130">**ReplyTo**</span><span class="sxs-lookup"><span data-stu-id="27339-130">**ReplyTo**</span></span>](taskschedulerschema-replyto-sendemailtype-element.md)           | <span data-ttu-id="27339-131">**string**</span><span class="sxs-lookup"><span data-stu-id="27339-131">**string**</span></span>                                                                   | <span data-ttu-id="27339-132">指定電子郵件訊息中要回復的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="27339-132">Specifies the email addresses that are replied to in the email message.</span></span><br/>               |
| [<span data-ttu-id="27339-133">**伺服器**</span><span class="sxs-lookup"><span data-stu-id="27339-133">**Server**</span></span>](taskschedulerschema-server-sendemailtype-element.md)             | [<span data-ttu-id="27339-134">**nonEmptyString**</span><span class="sxs-lookup"><span data-stu-id="27339-134">**nonEmptyString**</span></span>](taskschedulerschema-nonemptystring-simpletype.md)      | <span data-ttu-id="27339-135">指定用來傳送電子郵件訊息的電子郵件伺服器。</span><span class="sxs-lookup"><span data-stu-id="27339-135">Specifies the email server used to send the email message.</span></span> <br/>                           |
| [<span data-ttu-id="27339-136">**主體**</span><span class="sxs-lookup"><span data-stu-id="27339-136">**Subject**</span></span>](taskschedulerschema-subject-sendemailtype-element.md)           | <span data-ttu-id="27339-137">**string**</span><span class="sxs-lookup"><span data-stu-id="27339-137">**string**</span></span>                                                                   | <span data-ttu-id="27339-138">指定電子郵件訊息的主旨。</span><span class="sxs-lookup"><span data-stu-id="27339-138">Specifies the subject of the email message.</span></span><br/>                                           |
| [<span data-ttu-id="27339-139">**自**</span><span class="sxs-lookup"><span data-stu-id="27339-139">**To**</span></span>](taskschedulerschema-to-sendemailtype-element.md)                     | <span data-ttu-id="27339-140">**string**</span><span class="sxs-lookup"><span data-stu-id="27339-140">**string**</span></span>                                                                   | <span data-ttu-id="27339-141">指定電子郵件將傳送至其中的電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="27339-141">Specifies the email addresses to which the email will be sent.</span></span><br/>                        |



## <a name="requirements"></a><span data-ttu-id="27339-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="27339-142">Requirements</span></span>



| <span data-ttu-id="27339-143">需求</span><span class="sxs-lookup"><span data-stu-id="27339-143">Requirement</span></span> | <span data-ttu-id="27339-144">值</span><span class="sxs-lookup"><span data-stu-id="27339-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="27339-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27339-145">Minimum supported client</span></span><br/> | <span data-ttu-id="27339-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27339-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="27339-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27339-147">Minimum supported server</span></span><br/> | <span data-ttu-id="27339-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="27339-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





