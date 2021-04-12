---
title: File (attachmentsType) 元素
description: 包含以電子郵件訊息中的附件形式傳送之檔案的路徑。
ms.assetid: a53f591b-ac59-43b4-8cc2-661e76d307cc
keywords:
- File 元素工作排程器
topic_type:
- apiref
api_name:
- File
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ed07d4b31f9054f6caefcff0585d9683faa90c7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384362"
---
# <a name="file-attachmentstype-element"></a><span data-ttu-id="91bb3-104">File (attachmentsType) 元素</span><span class="sxs-lookup"><span data-stu-id="91bb3-104">File (attachmentsType) Element</span></span>

<span data-ttu-id="91bb3-105">包含以電子郵件訊息中的附件形式傳送之檔案的路徑。</span><span class="sxs-lookup"><span data-stu-id="91bb3-105">Contains the path to a file sent as an attachment in an email message.</span></span>

``` syntax
<xs:element name="File"
    type="nonEmptyString"
 />
```

<span data-ttu-id="91bb3-106">**File** 元素是由 [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="91bb3-106">The **File** element is defined by the [**attachmentsType**](taskschedulerschema-attachmentstype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="91bb3-107">父元素</span><span class="sxs-lookup"><span data-stu-id="91bb3-107">Parent element</span></span>



| <span data-ttu-id="91bb3-108">元素</span><span class="sxs-lookup"><span data-stu-id="91bb3-108">Element</span></span>                                                                                      | <span data-ttu-id="91bb3-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="91bb3-109">Derived from</span></span>                                                               | <span data-ttu-id="91bb3-110">Description</span><span class="sxs-lookup"><span data-stu-id="91bb3-110">Description</span></span>                                                     |
|----------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="91bb3-111">**附件 (sendEmailType)**</span><span class="sxs-lookup"><span data-stu-id="91bb3-111">**Attachments (sendEmailType)**</span></span>](taskschedulerschema-attachments-sendemailtype-element.md) | [<span data-ttu-id="91bb3-112">**attachmentsType**</span><span class="sxs-lookup"><span data-stu-id="91bb3-112">**attachmentsType**</span></span>](taskschedulerschema-attachmentstype-complextype.md) | <span data-ttu-id="91bb3-113">包含電子郵件訊息中的附件清單。</span><span class="sxs-lookup"><span data-stu-id="91bb3-113">Contains a list of attachments in the email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="91bb3-114">備註</span><span class="sxs-lookup"><span data-stu-id="91bb3-114">Remarks</span></span>

<span data-ttu-id="91bb3-115">針對 c + + 開發，請參閱 [**IEmailAction 的附件屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments)。</span><span class="sxs-lookup"><span data-stu-id="91bb3-115">For C++ development, see [**Attachments Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_attachments).</span></span>

<span data-ttu-id="91bb3-116">如需腳本開發，請參閱 [**EmailAction。**](emailaction-attachments.md)</span><span class="sxs-lookup"><span data-stu-id="91bb3-116">For script development, see [**EmailAction.Attachments**](emailaction-attachments.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="91bb3-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="91bb3-117">Requirements</span></span>



| <span data-ttu-id="91bb3-118">需求</span><span class="sxs-lookup"><span data-stu-id="91bb3-118">Requirement</span></span> | <span data-ttu-id="91bb3-119">值</span><span class="sxs-lookup"><span data-stu-id="91bb3-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="91bb3-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91bb3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="91bb3-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91bb3-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="91bb3-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91bb3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="91bb3-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91bb3-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





