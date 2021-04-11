---
title: ComHandler (actionGroup) 元素
description: 指定引發處理常式的動作。
ms.assetid: 18f16873-3879-4a3b-b8f2-17cc84647e25
keywords:
- ComHandler 元素工作排程器
topic_type:
- apiref
api_name:
- ComHandler
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 2269464efb09e8c513ab2bdebb24744a6b32a671
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934831"
---
# <a name="comhandler-actiongroup-element"></a><span data-ttu-id="f6238-104">ComHandler (actionGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="f6238-104">ComHandler (actionGroup) Element</span></span>

<span data-ttu-id="f6238-105">指定引發處理常式的動作。</span><span class="sxs-lookup"><span data-stu-id="f6238-105">Specifies an action that fires a handler.</span></span>

``` syntax
<xs:element name="ComHandler"
    type="comHandlerType"
 />
```

<span data-ttu-id="f6238-106">**ComHandler** 元素是由 [**actionGroup**](taskschedulerschema-actiongroup-group.md)定義。</span><span class="sxs-lookup"><span data-stu-id="f6238-106">The **ComHandler** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="f6238-107">父元素</span><span class="sxs-lookup"><span data-stu-id="f6238-107">Parent element</span></span>



| <span data-ttu-id="f6238-108">元素</span><span class="sxs-lookup"><span data-stu-id="f6238-108">Element</span></span>                                                         | <span data-ttu-id="f6238-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="f6238-109">Derived from</span></span>                                                       | <span data-ttu-id="f6238-110">Description</span><span class="sxs-lookup"><span data-stu-id="f6238-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f6238-111">**行動**</span><span class="sxs-lookup"><span data-stu-id="f6238-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="f6238-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="f6238-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="f6238-113">包含工作所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="f6238-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="f6238-114">子元素</span><span class="sxs-lookup"><span data-stu-id="f6238-114">Child elements</span></span>



| <span data-ttu-id="f6238-115">元素</span><span class="sxs-lookup"><span data-stu-id="f6238-115">Element</span></span>                                                               | <span data-ttu-id="f6238-116">類型</span><span class="sxs-lookup"><span data-stu-id="f6238-116">Type</span></span>                                                         | <span data-ttu-id="f6238-117">Description</span><span class="sxs-lookup"><span data-stu-id="f6238-117">Description</span></span>                                                       |
|-----------------------------------------------------------------------|--------------------------------------------------------------|-------------------------------------------------------------------|
| [<span data-ttu-id="f6238-118">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="f6238-118">**ClassId**</span></span>](taskschedulerschema-classid-comhandlertype-element.md) | [<span data-ttu-id="f6238-119">**guidType**</span><span class="sxs-lookup"><span data-stu-id="f6238-119">**guidType**</span></span>](taskschedulerschema-guidtype-simpletype.md)  | <span data-ttu-id="f6238-120">指定處理常式類別的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6238-120">Specifies the identifier of the handler class.</span></span><br/>         |
| [<span data-ttu-id="f6238-121">**資料**</span><span class="sxs-lookup"><span data-stu-id="f6238-121">**Data**</span></span>](taskschedulerschema-data-comhandlertype-element.md)       | [<span data-ttu-id="f6238-122">**dataType**</span><span class="sxs-lookup"><span data-stu-id="f6238-122">**dataType**</span></span>](taskschedulerschema-datatype-complextype.md) | <span data-ttu-id="f6238-123">指定與處理常式相關聯的其他資料。</span><span class="sxs-lookup"><span data-stu-id="f6238-123">Specifies additional data associated with the handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="f6238-124">備註</span><span class="sxs-lookup"><span data-stu-id="f6238-124">Remarks</span></span>

<span data-ttu-id="f6238-125">應用程式會使用 [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) 介面來定義 COM 處理常式動作。</span><span class="sxs-lookup"><span data-stu-id="f6238-125">Applications define a COM handler action using the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

### <a name="attributes"></a><span data-ttu-id="f6238-126">屬性</span><span class="sxs-lookup"><span data-stu-id="f6238-126">Attributes</span></span>

<span data-ttu-id="f6238-127">下列屬性是由 [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="f6238-127">The following attribute is defined by the [**actionBaseType**](taskschedulerschema-actionbasetype-complextype.md) complex type.</span></span>

-   <span data-ttu-id="f6238-128">識別碼：工作所執行之動作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f6238-128">ID: Identifier of the action performed by the task.</span></span>

## <a name="examples"></a><span data-ttu-id="f6238-129">範例</span><span class="sxs-lookup"><span data-stu-id="f6238-129">Examples</span></span>

<span data-ttu-id="f6238-130">下列 XML 定義 COM 處理常式動作。</span><span class="sxs-lookup"><span data-stu-id="f6238-130">The following XML defines a COM handler action.</span></span>


```XML
<Actions>
    <ComHandler>
        <ClassId></ClassId>
        <Data></Data>
    </ComHandler>
</Actions>
```



## <a name="requirements"></a><span data-ttu-id="f6238-131">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6238-131">Requirements</span></span>



| <span data-ttu-id="f6238-132">需求</span><span class="sxs-lookup"><span data-stu-id="f6238-132">Requirement</span></span> | <span data-ttu-id="f6238-133">值</span><span class="sxs-lookup"><span data-stu-id="f6238-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f6238-134">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6238-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f6238-135">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6238-135">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="f6238-136">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6238-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f6238-137">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6238-137">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="f6238-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6238-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6238-139">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="f6238-139">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





