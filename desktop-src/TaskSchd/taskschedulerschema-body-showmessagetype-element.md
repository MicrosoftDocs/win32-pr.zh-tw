---
title: ShowMessageType) 元素的內文 (主體
description: 包含要顯示在訊息方塊主體中的文字。
ms.assetid: 69ea872a-7ca1-4464-9380-b35f74c9cb8e
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
ms.openlocfilehash: 3486601153f8e9dd7dac14f83800dae00a79a9f8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465809"
---
# <a name="body-showmessagetype-element"></a><span data-ttu-id="8f442-104">ShowMessageType) 元素的內文 (主體</span><span class="sxs-lookup"><span data-stu-id="8f442-104">Body (showMessageType) Element</span></span>

<span data-ttu-id="8f442-105">包含要顯示在訊息方塊主體中的文字。</span><span class="sxs-lookup"><span data-stu-id="8f442-105">Contains the text to display in the body of the message box.</span></span>

``` syntax
<xs:element name="Body"
    type="nonEmptyString"
 />
```

<span data-ttu-id="8f442-106">**Body** 專案是由 [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="8f442-106">The **Body** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8f442-107">父元素</span><span class="sxs-lookup"><span data-stu-id="8f442-107">Parent element</span></span>



| <span data-ttu-id="8f442-108">元素</span><span class="sxs-lookup"><span data-stu-id="8f442-108">Element</span></span>                                                                                  | <span data-ttu-id="8f442-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="8f442-109">Derived from</span></span>                                                               | <span data-ttu-id="8f442-110">Description</span><span class="sxs-lookup"><span data-stu-id="8f442-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="8f442-111">**ShowMessage (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="8f442-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="8f442-112">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="8f442-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="8f442-113">表示顯示訊息方塊的動作。</span><span class="sxs-lookup"><span data-stu-id="8f442-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8f442-114">備註</span><span class="sxs-lookup"><span data-stu-id="8f442-114">Remarks</span></span>

<span data-ttu-id="8f442-115">針對 c + + 開發，請參閱 [**IShowMessageAction 的 MessageBody 屬性**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody)。</span><span class="sxs-lookup"><span data-stu-id="8f442-115">For C++ development, see [**MessageBody Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_messagebody).</span></span>

<span data-ttu-id="8f442-116">如需腳本開發，請參閱 [**ShowMessageAction. MessageBody**](showmessageaction-messagebody.md)。</span><span class="sxs-lookup"><span data-stu-id="8f442-116">For script development, see [**ShowMessageAction.MessageBody**](showmessageaction-messagebody.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f442-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f442-117">Requirements</span></span>



| <span data-ttu-id="8f442-118">需求</span><span class="sxs-lookup"><span data-stu-id="8f442-118">Requirement</span></span> | <span data-ttu-id="8f442-119">值</span><span class="sxs-lookup"><span data-stu-id="8f442-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8f442-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8f442-120">Minimum supported client</span></span><br/> | <span data-ttu-id="8f442-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f442-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8f442-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8f442-122">Minimum supported server</span></span><br/> | <span data-ttu-id="8f442-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8f442-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





