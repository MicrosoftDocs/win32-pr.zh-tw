---
title: " (comHandlerType) 元素的 ClassId"
description: 指定處理常式類別的識別碼。
ms.assetid: 38ebcc39-85f2-4f61-8cb6-556c242a63d9
keywords:
- 工作排程器的 ClassId 元素
topic_type:
- apiref
api_name:
- ClassId
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c89af2f39ae6a4a529fe7a728cf4b821245aa034
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466989"
---
# <a name="classid-comhandlertype-element"></a><span data-ttu-id="b0d47-104"> (comHandlerType) 元素的 ClassId</span><span class="sxs-lookup"><span data-stu-id="b0d47-104">ClassId (comHandlerType) Element</span></span>

<span data-ttu-id="b0d47-105">指定處理常式類別的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0d47-105">Specifies the identifier of the handler class.</span></span>

``` syntax
<xs:element name="ClassId"
    type="guidType"
 />
```

<span data-ttu-id="b0d47-106">**ClassId** 元素是由 [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="b0d47-106">The **ClassId** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="b0d47-107">父元素</span><span class="sxs-lookup"><span data-stu-id="b0d47-107">Parent element</span></span>



| <span data-ttu-id="b0d47-108">元素</span><span class="sxs-lookup"><span data-stu-id="b0d47-108">Element</span></span>                                                                  | <span data-ttu-id="b0d47-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="b0d47-109">Derived from</span></span>                                                             | <span data-ttu-id="b0d47-110">Description</span><span class="sxs-lookup"><span data-stu-id="b0d47-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="b0d47-111">**ComHandler**</span><span class="sxs-lookup"><span data-stu-id="b0d47-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="b0d47-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="b0d47-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="b0d47-113">指定引發處理常式的動作。</span><span class="sxs-lookup"><span data-stu-id="b0d47-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="b0d47-114">備註</span><span class="sxs-lookup"><span data-stu-id="b0d47-114">Remarks</span></span>

<span data-ttu-id="b0d47-115">應用程式會使用 [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)介面的 [**ClassId**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid)屬性來定義類別識別碼。</span><span class="sxs-lookup"><span data-stu-id="b0d47-115">Applications define the class identifier using the [**ClassId**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_classid) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="b0d47-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="b0d47-116">Requirements</span></span>



| <span data-ttu-id="b0d47-117">需求</span><span class="sxs-lookup"><span data-stu-id="b0d47-117">Requirement</span></span> | <span data-ttu-id="b0d47-118">值</span><span class="sxs-lookup"><span data-stu-id="b0d47-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="b0d47-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b0d47-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0d47-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0d47-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="b0d47-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b0d47-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0d47-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="b0d47-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b0d47-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b0d47-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0d47-124">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="b0d47-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





