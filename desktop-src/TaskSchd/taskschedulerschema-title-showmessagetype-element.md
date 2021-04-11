---
title: 標題 (showMessageType) 元素
description: 包含訊息方塊的標題。
ms.assetid: 089d2043-41ed-4050-b794-af24ab7ac8b9
keywords:
- Title 元素工作排程器
topic_type:
- apiref
api_name:
- Title
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ca5baa7135579ff673ba9b01a672a126924d1d49
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094059"
---
# <a name="title-showmessagetype-element"></a><span data-ttu-id="ab707-104">標題 (showMessageType) 元素</span><span class="sxs-lookup"><span data-stu-id="ab707-104">Title (showMessageType) Element</span></span>

<span data-ttu-id="ab707-105">包含訊息方塊的標題。</span><span class="sxs-lookup"><span data-stu-id="ab707-105">Contains the title of the message box.</span></span>

``` syntax
<xs:element name="Title"
    type="nonEmptyString"
 />
```

<span data-ttu-id="ab707-106">**Title** 元素是由 [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="ab707-106">The **Title** element is defined by the [**showMessageType**](taskschedulerschema-showmessagetype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="ab707-107">父元素</span><span class="sxs-lookup"><span data-stu-id="ab707-107">Parent element</span></span>



| <span data-ttu-id="ab707-108">元素</span><span class="sxs-lookup"><span data-stu-id="ab707-108">Element</span></span>                                                                                  | <span data-ttu-id="ab707-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="ab707-109">Derived from</span></span>                                                               | <span data-ttu-id="ab707-110">Description</span><span class="sxs-lookup"><span data-stu-id="ab707-110">Description</span></span>                                               |
|------------------------------------------------------------------------------------------|----------------------------------------------------------------------------|-----------------------------------------------------------|
| [<span data-ttu-id="ab707-111">**ShowMessage (actionGroup)**</span><span class="sxs-lookup"><span data-stu-id="ab707-111">**ShowMessage (actionGroup)**</span></span>](taskschedulerschema-showmessage-actiongroup-element.md) | [<span data-ttu-id="ab707-112">**showMessageType**</span><span class="sxs-lookup"><span data-stu-id="ab707-112">**showMessageType**</span></span>](taskschedulerschema-showmessagetype-complextype.md) | <span data-ttu-id="ab707-113">表示顯示訊息方塊的動作。</span><span class="sxs-lookup"><span data-stu-id="ab707-113">Represents an action that shows a message box.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ab707-114">備註</span><span class="sxs-lookup"><span data-stu-id="ab707-114">Remarks</span></span>

<span data-ttu-id="ab707-115">針對 c + + 開發，請參閱 [**IShowMessageAction 的 Title 屬性**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title)。</span><span class="sxs-lookup"><span data-stu-id="ab707-115">For C++ development, see [**Title Property of IShowMessageAction**](/windows/desktop/api/taskschd/nf-taskschd-ishowmessageaction-get_title).</span></span>

<span data-ttu-id="ab707-116">如需腳本開發，請參閱 [**ShowMessageAction。**](showmessageaction-title.md)</span><span class="sxs-lookup"><span data-stu-id="ab707-116">For script development, see [**ShowMessageAction.Title**](showmessageaction-title.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ab707-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab707-117">Requirements</span></span>



| <span data-ttu-id="ab707-118">需求</span><span class="sxs-lookup"><span data-stu-id="ab707-118">Requirement</span></span> | <span data-ttu-id="ab707-119">值</span><span class="sxs-lookup"><span data-stu-id="ab707-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ab707-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab707-120">Minimum supported client</span></span><br/> | <span data-ttu-id="ab707-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab707-121">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ab707-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab707-122">Minimum supported server</span></span><br/> | <span data-ttu-id="ab707-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab707-123">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



 

 





