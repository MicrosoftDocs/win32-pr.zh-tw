---
title: ShowMessage (actionGroup) 元素
description: 表示顯示訊息方塊的動作。
ms.assetid: 33c6e437-b993-4b5e-b75a-fb3fda9b24df
keywords:
- ShowMessage 元素工作排程器
topic_type:
- apiref
api_name:
- ShowMessage
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a1344aadfa5fe67e411048bac2a83330ea704c50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104317175"
---
# <a name="showmessage-actiongroup-element"></a><span data-ttu-id="4bb83-104">ShowMessage (actionGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="4bb83-104">ShowMessage (actionGroup) Element</span></span>

<span data-ttu-id="4bb83-105">表示顯示訊息方塊的動作。</span><span class="sxs-lookup"><span data-stu-id="4bb83-105">Represents an action that shows a message box.</span></span>

``` syntax
<xs:element name="ShowMessage"
    type="showMessageType"
 />
```

<span data-ttu-id="4bb83-106">**ShowMessage** 元素是由 [**actionGroup**](taskschedulerschema-actiongroup-group.md)定義。</span><span class="sxs-lookup"><span data-stu-id="4bb83-106">The **ShowMessage** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="4bb83-107">父元素</span><span class="sxs-lookup"><span data-stu-id="4bb83-107">Parent element</span></span>



| <span data-ttu-id="4bb83-108">元素</span><span class="sxs-lookup"><span data-stu-id="4bb83-108">Element</span></span>                                                                    | <span data-ttu-id="4bb83-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="4bb83-109">Derived from</span></span>                                                       | <span data-ttu-id="4bb83-110">Description</span><span class="sxs-lookup"><span data-stu-id="4bb83-110">Description</span></span>                                            |
|----------------------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="4bb83-111">**動作 (taskType)**</span><span class="sxs-lookup"><span data-stu-id="4bb83-111">**Actions (taskType)**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="4bb83-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="4bb83-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="4bb83-113">包含工作所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="4bb83-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="4bb83-114">子元素</span><span class="sxs-lookup"><span data-stu-id="4bb83-114">Child elements</span></span>



| <span data-ttu-id="4bb83-115">元素</span><span class="sxs-lookup"><span data-stu-id="4bb83-115">Element</span></span>                                                            | <span data-ttu-id="4bb83-116">類型</span><span class="sxs-lookup"><span data-stu-id="4bb83-116">Type</span></span>           | <span data-ttu-id="4bb83-117">Description</span><span class="sxs-lookup"><span data-stu-id="4bb83-117">Description</span></span>                                                               |
|--------------------------------------------------------------------|----------------|---------------------------------------------------------------------------|
| [<span data-ttu-id="4bb83-118">**本文**</span><span class="sxs-lookup"><span data-stu-id="4bb83-118">**Body**</span></span>](taskschedulerschema-body-showmessagetype-element.md)   | <span data-ttu-id="4bb83-119">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="4bb83-119">nonEmptyString</span></span> | <span data-ttu-id="4bb83-120">指定要顯示在訊息方塊主體中的文字。</span><span class="sxs-lookup"><span data-stu-id="4bb83-120">Specifies the text to display in the body of the message box.</span></span> <br/> |
| [<span data-ttu-id="4bb83-121">**標題**</span><span class="sxs-lookup"><span data-stu-id="4bb83-121">**Title**</span></span>](taskschedulerschema-title-showmessagetype-element.md) | <span data-ttu-id="4bb83-122">nonEmptyString</span><span class="sxs-lookup"><span data-stu-id="4bb83-122">nonEmptyString</span></span> | <span data-ttu-id="4bb83-123">指定訊息方塊的標題。</span><span class="sxs-lookup"><span data-stu-id="4bb83-123">Specifies the title of the message box.</span></span> <br/>                       |



## <a name="remarks"></a><span data-ttu-id="4bb83-124">備註</span><span class="sxs-lookup"><span data-stu-id="4bb83-124">Remarks</span></span>

<span data-ttu-id="4bb83-125">針對開發腳本，會使用 [**ShowMessageAction**](showmessageaction.md) 物件來指定訊息方塊動作。</span><span class="sxs-lookup"><span data-stu-id="4bb83-125">For scripting development, a message box action is specified using the [**ShowMessageAction**](showmessageaction.md) object.</span></span>

<span data-ttu-id="4bb83-126">針對 c + + 開發，會使用 [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) 介面指定訊息方塊動作。</span><span class="sxs-lookup"><span data-stu-id="4bb83-126">For C++ development, a message box action is specified using the [**IShowMessageAction**](/windows/desktop/api/taskschd/nn-taskschd-ishowmessageaction) interface.</span></span>

<span data-ttu-id="4bb83-127">**Windows 8 和 Windows Server 2012：** 已移除這個元素。</span><span class="sxs-lookup"><span data-stu-id="4bb83-127">**Windows 8 and Windows Server 2012:** This element has been removed.</span></span> <span data-ttu-id="4bb83-128">您可以使用 IExecAction 搭配 Windows 腳本 [**MsgBox 函數**](/previous-versions/sfw6660x(v=vs.80)) ，在使用者會話中顯示訊息。</span><span class="sxs-lookup"><span data-stu-id="4bb83-128">You can use IExecAction with the Windows scripting [**MsgBox function**](/previous-versions/sfw6660x(v=vs.80)) to show a message in the user session.</span></span>

## <a name="examples"></a><span data-ttu-id="4bb83-129">範例</span><span class="sxs-lookup"><span data-stu-id="4bb83-129">Examples</span></span>

<span data-ttu-id="4bb83-130">如需使用訊息方塊動作之工作的 XML 完整範例，請參閱 [ (xml) 的訊息方塊範例 ](/previous-versions//aa381917(v=vs.85))。</span><span class="sxs-lookup"><span data-stu-id="4bb83-130">For a complete example of the XML for a task that uses a message box action, see [Message Box Example (XML)](/previous-versions//aa381917(v=vs.85)).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bb83-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bb83-131">Requirements</span></span>



| <span data-ttu-id="4bb83-132">需求</span><span class="sxs-lookup"><span data-stu-id="4bb83-132">Requirement</span></span> | <span data-ttu-id="4bb83-133">值</span><span class="sxs-lookup"><span data-stu-id="4bb83-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4bb83-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bb83-134">Minimum supported client</span></span><br/> | <span data-ttu-id="4bb83-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bb83-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4bb83-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bb83-136">Minimum supported server</span></span><br/> | <span data-ttu-id="4bb83-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bb83-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="4bb83-138">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="4bb83-138">End of client support</span></span><br/>    | <span data-ttu-id="4bb83-139">Windows 7</span><span class="sxs-lookup"><span data-stu-id="4bb83-139">Windows 7</span></span><br/>                                 |
| <span data-ttu-id="4bb83-140">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="4bb83-140">End of server support</span></span><br/>    | <span data-ttu-id="4bb83-141">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="4bb83-141">Windows Server 2008 R2</span></span><br/>                    |



 

