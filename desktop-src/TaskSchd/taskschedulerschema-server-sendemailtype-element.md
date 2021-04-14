---
title: 伺服器 (sendEmailType) 元素
description: 包含用來傳送電子郵件訊息的電子郵件伺服器。
ms.assetid: 4c6084d1-70c5-4d8b-8fcb-ab4cd8aab441
keywords:
- Server 元素工作排程器
topic_type:
- apiref
api_name:
- Server
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 5fc57ddf5deee52ff9b118a8267eec4069108030
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384097"
---
# <a name="server-sendemailtype-element"></a><span data-ttu-id="bcbc7-104">伺服器 (sendEmailType) 元素</span><span class="sxs-lookup"><span data-stu-id="bcbc7-104">Server (sendEmailType) Element</span></span>

<span data-ttu-id="bcbc7-105">包含用來傳送電子郵件訊息的電子郵件伺服器。</span><span class="sxs-lookup"><span data-stu-id="bcbc7-105">Contains the email server used to send the email message.</span></span>

``` syntax
<xs:element name="Server"
    type="nonEmptyString"
 />
```

<span data-ttu-id="bcbc7-106">**Server** 元素是由 [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="bcbc7-106">The **Server** element is defined by the [**sendEmailType**](taskschedulerschema-sendemailtype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="bcbc7-107">父元素</span><span class="sxs-lookup"><span data-stu-id="bcbc7-107">Parent element</span></span>



| <span data-ttu-id="bcbc7-108">元素</span><span class="sxs-lookup"><span data-stu-id="bcbc7-108">Element</span></span>                                                                              | <span data-ttu-id="bcbc7-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="bcbc7-109">Derived from</span></span>                                                           | <span data-ttu-id="bcbc7-110">Description</span><span class="sxs-lookup"><span data-stu-id="bcbc7-110">Description</span></span>                                                  |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="bcbc7-111">**SendEmail (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="bcbc7-111">**SendEmail (actionGroup)**</span></span>](taskschedulerschema-sendemail-actiongroup-element.md) | [<span data-ttu-id="bcbc7-112">**sendEMailType**</span><span class="sxs-lookup"><span data-stu-id="bcbc7-112">**sendEMailType**</span></span>](taskschedulerschema-sendemailtype-complextype.md) | <span data-ttu-id="bcbc7-113">表示傳送電子郵件訊息的動作。</span><span class="sxs-lookup"><span data-stu-id="bcbc7-113">Represents an action that sends an email message.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="bcbc7-114">備註</span><span class="sxs-lookup"><span data-stu-id="bcbc7-114">Remarks</span></span>

<span data-ttu-id="bcbc7-115">針對 c + + 開發，請參閱 [**IEmailAction 的伺服器屬性**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server)。</span><span class="sxs-lookup"><span data-stu-id="bcbc7-115">For C++ development, see [**Server Property of IEmailAction**](/windows/desktop/api/taskschd/nf-taskschd-iemailaction-get_server).</span></span>

<span data-ttu-id="bcbc7-116">如需腳本開發，請參閱 [**EmailAction。**](emailaction-server.md)</span><span class="sxs-lookup"><span data-stu-id="bcbc7-116">For script development, see [**EmailAction.Server**](emailaction-server.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcbc7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="bcbc7-117">Requirements</span></span>



| <span data-ttu-id="bcbc7-118">需求</span><span class="sxs-lookup"><span data-stu-id="bcbc7-118">Requirement</span></span> | <span data-ttu-id="bcbc7-119">值</span><span class="sxs-lookup"><span data-stu-id="bcbc7-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="bcbc7-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bcbc7-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bcbc7-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcbc7-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="bcbc7-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bcbc7-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bcbc7-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bcbc7-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





