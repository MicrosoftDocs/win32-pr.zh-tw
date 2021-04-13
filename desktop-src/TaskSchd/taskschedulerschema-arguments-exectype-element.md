---
title: 引數 (execType) 元素
description: 指定與命令列操作相關聯的引數。
ms.assetid: 37207c4f-941c-4cbf-9a81-5876b224a7c1
keywords:
- Arguments 元素工作排程器
topic_type:
- apiref
api_name:
- Arguments
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ff35465fbad1de82d096b583499ea6cdafe93ca7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508852"
---
# <a name="arguments-exectype-element"></a><span data-ttu-id="51b8e-104">引數 (execType) 元素</span><span class="sxs-lookup"><span data-stu-id="51b8e-104">Arguments (execType) Element</span></span>

<span data-ttu-id="51b8e-105">指定與命令列操作相關聯的引數。</span><span class="sxs-lookup"><span data-stu-id="51b8e-105">Specifies the arguments associated with the command-line operation.</span></span>

``` syntax
<xs:element name="Arguments"
    type="string"
 />
```

<span data-ttu-id="51b8e-106">**引數** 元素是由 [**execType**](taskschedulerschema-exectype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="51b8e-106">The **Arguments** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="51b8e-107">父元素</span><span class="sxs-lookup"><span data-stu-id="51b8e-107">Parent element</span></span>



| <span data-ttu-id="51b8e-108">元素</span><span class="sxs-lookup"><span data-stu-id="51b8e-108">Element</span></span>                                                      | <span data-ttu-id="51b8e-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="51b8e-109">Derived from</span></span>                                                 | <span data-ttu-id="51b8e-110">Description</span><span class="sxs-lookup"><span data-stu-id="51b8e-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="51b8e-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="51b8e-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="51b8e-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="51b8e-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="51b8e-113">指定執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="51b8e-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="51b8e-114">備註</span><span class="sxs-lookup"><span data-stu-id="51b8e-114">Remarks</span></span>

<span data-ttu-id="51b8e-115">針對 c + + 開發，請參閱 [**IExecAction 的引數屬性**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)。</span><span class="sxs-lookup"><span data-stu-id="51b8e-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="51b8e-116">如需腳本開發，請參閱 [**ExecAction。**](execaction-arguments.md)</span><span class="sxs-lookup"><span data-stu-id="51b8e-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="51b8e-117">範例</span><span class="sxs-lookup"><span data-stu-id="51b8e-117">Examples</span></span>

<span data-ttu-id="51b8e-118">如需使用可執行動作之工作的 XML 完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="51b8e-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51b8e-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="51b8e-119">Requirements</span></span>



| <span data-ttu-id="51b8e-120">需求</span><span class="sxs-lookup"><span data-stu-id="51b8e-120">Requirement</span></span> | <span data-ttu-id="51b8e-121">值</span><span class="sxs-lookup"><span data-stu-id="51b8e-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="51b8e-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51b8e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="51b8e-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51b8e-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="51b8e-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51b8e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="51b8e-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51b8e-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51b8e-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="51b8e-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51b8e-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="51b8e-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





