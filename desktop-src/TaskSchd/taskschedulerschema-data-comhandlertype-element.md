---
title: 資料 (comHandlerType) 元素
description: 指定與處理常式相關聯的其他資料。
ms.assetid: 352cb92b-54bb-4bb0-8a43-123c88c80962
keywords:
- 工作排程器的資料元素
topic_type:
- apiref
api_name:
- Data
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d009005dc2bb889c8bd9e34e84d853665310330a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934830"
---
# <a name="data-comhandlertype-element"></a><span data-ttu-id="2c307-104">資料 (comHandlerType) 元素</span><span class="sxs-lookup"><span data-stu-id="2c307-104">Data (comHandlerType) Element</span></span>

<span data-ttu-id="2c307-105">指定與處理常式相關聯的其他資料。</span><span class="sxs-lookup"><span data-stu-id="2c307-105">Specifies additional data associated with the handler.</span></span>

``` syntax
<xs:element name="Data"
    type="dataType"
 />
```

<span data-ttu-id="2c307-106">**資料** 元素是由 [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="2c307-106">The **Data** element is defined by the [**comHandlerType**](taskschedulerschema-comhandlertype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="2c307-107">父元素</span><span class="sxs-lookup"><span data-stu-id="2c307-107">Parent element</span></span>



| <span data-ttu-id="2c307-108">元素</span><span class="sxs-lookup"><span data-stu-id="2c307-108">Element</span></span>                                                                  | <span data-ttu-id="2c307-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="2c307-109">Derived from</span></span>                                                             | <span data-ttu-id="2c307-110">Description</span><span class="sxs-lookup"><span data-stu-id="2c307-110">Description</span></span>                                          |
|--------------------------------------------------------------------------|--------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="2c307-111">**ComHandler**</span><span class="sxs-lookup"><span data-stu-id="2c307-111">**ComHandler**</span></span>](taskschedulerschema-comhandler-actiongroup-element.md) | [<span data-ttu-id="2c307-112">**comHandlerType**</span><span class="sxs-lookup"><span data-stu-id="2c307-112">**comHandlerType**</span></span>](taskschedulerschema-comhandlertype-complextype.md) | <span data-ttu-id="2c307-113">指定引發處理常式的動作。</span><span class="sxs-lookup"><span data-stu-id="2c307-113">Specifies an action that fires a handler.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="2c307-114">備註</span><span class="sxs-lookup"><span data-stu-id="2c307-114">Remarks</span></span>

<span data-ttu-id="2c307-115">應用程式會使用 [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction)介面的 [**data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data)屬性來定義處理常式資料。</span><span class="sxs-lookup"><span data-stu-id="2c307-115">Applications define the handler data using the [**Data**](/windows/desktop/api/taskschd/nf-taskschd-icomhandleraction-get_data) property of the [**IComHandlerAction**](/windows/desktop/api/taskschd/nn-taskschd-icomhandleraction) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="2c307-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="2c307-116">Requirements</span></span>



| <span data-ttu-id="2c307-117">需求</span><span class="sxs-lookup"><span data-stu-id="2c307-117">Requirement</span></span> | <span data-ttu-id="2c307-118">值</span><span class="sxs-lookup"><span data-stu-id="2c307-118">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="2c307-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="2c307-119">Minimum supported client</span></span><br/> | <span data-ttu-id="2c307-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c307-120">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="2c307-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="2c307-121">Minimum supported server</span></span><br/> | <span data-ttu-id="2c307-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="2c307-122">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="2c307-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2c307-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2c307-124">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="2c307-124">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





