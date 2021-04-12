---
title: 命令 (execType) 元素
description: 指定要執行的可執行檔或檔。
ms.assetid: dedf8627-926c-43c6-8add-21ff298d697a
keywords:
- 命令元素工作排程器
topic_type:
- apiref
api_name:
- Command
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: c9d27eb5b40d652035882efc311d9735bcbdd23e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385077"
---
# <a name="command-exectype-element"></a><span data-ttu-id="8c170-104">命令 (execType) 元素</span><span class="sxs-lookup"><span data-stu-id="8c170-104">Command (execType) Element</span></span>

<span data-ttu-id="8c170-105">指定要執行的可執行檔或檔。</span><span class="sxs-lookup"><span data-stu-id="8c170-105">Specifies the executable file or document to be run.</span></span>

``` syntax
<xs:element name="Command"
    type="pathType"
 />
```

<span data-ttu-id="8c170-106">**Command** 元素是由 [**execType**](taskschedulerschema-exectype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="8c170-106">The **Command** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="8c170-107">父元素</span><span class="sxs-lookup"><span data-stu-id="8c170-107">Parent element</span></span>



| <span data-ttu-id="8c170-108">元素</span><span class="sxs-lookup"><span data-stu-id="8c170-108">Element</span></span>                                                      | <span data-ttu-id="8c170-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="8c170-109">Derived from</span></span>                                                 | <span data-ttu-id="8c170-110">Description</span><span class="sxs-lookup"><span data-stu-id="8c170-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="8c170-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="8c170-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="8c170-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="8c170-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="8c170-113">指定執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="8c170-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="8c170-114">備註</span><span class="sxs-lookup"><span data-stu-id="8c170-114">Remarks</span></span>

<span data-ttu-id="8c170-115">針對 c + + 開發，請參閱 [**IExecAction 的引數屬性**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments)。</span><span class="sxs-lookup"><span data-stu-id="8c170-115">For C++ development, see the [**Arguments property of IExecAction**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_arguments).</span></span>

<span data-ttu-id="8c170-116">如需腳本開發，請參閱 [**ExecAction。**](execaction-arguments.md)</span><span class="sxs-lookup"><span data-stu-id="8c170-116">For script development, see [**ExecAction.Arguments**](execaction-arguments.md).</span></span>

## <a name="examples"></a><span data-ttu-id="8c170-117">範例</span><span class="sxs-lookup"><span data-stu-id="8c170-117">Examples</span></span>

<span data-ttu-id="8c170-118">如需使用可執行動作之工作的 XML 完整範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="8c170-118">For a complete example of the XML for a task that uses an executable action, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8c170-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="8c170-119">Requirements</span></span>



| <span data-ttu-id="8c170-120">需求</span><span class="sxs-lookup"><span data-stu-id="8c170-120">Requirement</span></span> | <span data-ttu-id="8c170-121">值</span><span class="sxs-lookup"><span data-stu-id="8c170-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="8c170-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="8c170-122">Minimum supported client</span></span><br/> | <span data-ttu-id="8c170-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c170-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="8c170-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="8c170-124">Minimum supported server</span></span><br/> | <span data-ttu-id="8c170-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="8c170-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8c170-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8c170-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c170-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="8c170-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





