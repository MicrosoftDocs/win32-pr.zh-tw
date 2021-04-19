---
title: Exec (actionGroup) 元素
description: 指定執行命令列操作的動作。
ms.assetid: 84bdd1ec-4279-4282-b44a-4b5ad30503eb
keywords:
- Exec 元素工作排程器
topic_type:
- apiref
api_name:
- Exec
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b29ba66be8f2d3aefaec4f437359f2af5275d2f0
ms.sourcegitcommit: 628fda3e63fd1d513ce9a5f55be8bbc4af4b2a4b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106975603"
---
# <a name="exec-actiongroup-element"></a><span data-ttu-id="ac40b-104">Exec (actionGroup) 元素</span><span class="sxs-lookup"><span data-stu-id="ac40b-104">Exec (actionGroup) Element</span></span>

<span data-ttu-id="ac40b-105">指定執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="ac40b-105">Specifies an action that executes a command-line operation.</span></span>

``` syntax
<xs:element name="Exec"
    type="execType"
 />
```

<span data-ttu-id="ac40b-106">**Exec** 元素是由 [**actionGroup**](taskschedulerschema-actiongroup-group.md)所定義。</span><span class="sxs-lookup"><span data-stu-id="ac40b-106">The **Exec** element is defined by the [**actionGroup**](taskschedulerschema-actiongroup-group.md) .</span></span>

## <a name="parent-element"></a><span data-ttu-id="ac40b-107">父元素</span><span class="sxs-lookup"><span data-stu-id="ac40b-107">Parent element</span></span>



| <span data-ttu-id="ac40b-108">元素</span><span class="sxs-lookup"><span data-stu-id="ac40b-108">Element</span></span>                                                         | <span data-ttu-id="ac40b-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="ac40b-109">Derived from</span></span>                                                       | <span data-ttu-id="ac40b-110">Description</span><span class="sxs-lookup"><span data-stu-id="ac40b-110">Description</span></span>                                            |
|-----------------------------------------------------------------|--------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="ac40b-111">**行動**</span><span class="sxs-lookup"><span data-stu-id="ac40b-111">**Actions**</span></span>](taskschedulerschema-actions-tasktype-element.md) | [<span data-ttu-id="ac40b-112">**actionsType**</span><span class="sxs-lookup"><span data-stu-id="ac40b-112">**actionsType**</span></span>](taskschedulerschema-actionstype-complextype.md) | <span data-ttu-id="ac40b-113">包含工作所執行的動作。</span><span class="sxs-lookup"><span data-stu-id="ac40b-113">Contains the actions performed by the task.</span></span><br/> |



## <a name="child-elements"></a><span data-ttu-id="ac40b-114">子元素</span><span class="sxs-lookup"><span data-stu-id="ac40b-114">Child elements</span></span>



| <span data-ttu-id="ac40b-115">元素</span><span class="sxs-lookup"><span data-stu-id="ac40b-115">Element</span></span>                                                                           | <span data-ttu-id="ac40b-116">類型</span><span class="sxs-lookup"><span data-stu-id="ac40b-116">Type</span></span>       | <span data-ttu-id="ac40b-117">Description</span><span class="sxs-lookup"><span data-stu-id="ac40b-117">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------------------|------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ac40b-118">**引數**</span><span class="sxs-lookup"><span data-stu-id="ac40b-118">**Arguments**</span></span>](taskschedulerschema-arguments-exectype-element.md)               | <span data-ttu-id="ac40b-119">**string**</span><span class="sxs-lookup"><span data-stu-id="ac40b-119">**string**</span></span> | <span data-ttu-id="ac40b-120">指定與命令列操作相關聯的引數。</span><span class="sxs-lookup"><span data-stu-id="ac40b-120">Specifies the arguments associated with the command-line operation.</span></span><br/>                               |
| [<span data-ttu-id="ac40b-121">**命令**</span><span class="sxs-lookup"><span data-stu-id="ac40b-121">**Command**</span></span>](taskschedulerschema-command-exectype-element.md)                   | <span data-ttu-id="ac40b-122">**string**</span><span class="sxs-lookup"><span data-stu-id="ac40b-122">**string**</span></span> | <span data-ttu-id="ac40b-123">指定要執行的可執行檔或檔。</span><span class="sxs-lookup"><span data-stu-id="ac40b-123">Specifies the executable file or document to be run.</span></span><br/>                                              |
| [<span data-ttu-id="ac40b-124">**WorkingDirectory**</span><span class="sxs-lookup"><span data-stu-id="ac40b-124">**WorkingDirectory**</span></span>](taskschedulerschema-workingdirectory-exectype-element.md) | <span data-ttu-id="ac40b-125">字串</span><span class="sxs-lookup"><span data-stu-id="ac40b-125">string</span></span>     | <span data-ttu-id="ac40b-126">指定可執行檔或可執行檔所使用的檔案所在的目錄。</span><span class="sxs-lookup"><span data-stu-id="ac40b-126">Specifies the directory where either the executable or those files used by the executable exists.</span></span><br/> |



## <a name="attributes"></a><span data-ttu-id="ac40b-127">屬性</span><span class="sxs-lookup"><span data-stu-id="ac40b-127">Attributes</span></span>



| <span data-ttu-id="ac40b-128">名稱</span><span class="sxs-lookup"><span data-stu-id="ac40b-128">Name</span></span> | <span data-ttu-id="ac40b-129">類型</span><span class="sxs-lookup"><span data-stu-id="ac40b-129">Type</span></span>       | <span data-ttu-id="ac40b-130">描述</span><span class="sxs-lookup"><span data-stu-id="ac40b-130">Description</span></span>                                                    |
|------|------------|----------------------------------------------------------------|
| <span data-ttu-id="ac40b-131">id</span><span class="sxs-lookup"><span data-stu-id="ac40b-131">id</span></span>   | <span data-ttu-id="ac40b-132">**string**</span><span class="sxs-lookup"><span data-stu-id="ac40b-132">**string**</span></span> | <span data-ttu-id="ac40b-133">工作所執行之動作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="ac40b-133">The identifier of the action performed by the task.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="ac40b-134">備註</span><span class="sxs-lookup"><span data-stu-id="ac40b-134">Remarks</span></span>

<span data-ttu-id="ac40b-135">上方所列的子專案是由 [**execType**](taskschedulerschema-exectype-complextype.md) 複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="ac40b-135">The child elements listed above are defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

<span data-ttu-id="ac40b-136">針對腳本開發，執行動作是由 [**ExecAction**](execaction.md) 物件定義。</span><span class="sxs-lookup"><span data-stu-id="ac40b-136">For script development, an execution action is defined by the [**ExecAction**](execaction.md) object.</span></span>

<span data-ttu-id="ac40b-137">針對 c + + 開發，執行動作是由 [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) 介面所定義。</span><span class="sxs-lookup"><span data-stu-id="ac40b-137">For C++ development, an execution action is defined by the [**IExecAction**](/windows/desktop/api/taskschd/nn-taskschd-iexecaction) interface.</span></span>

<span data-ttu-id="ac40b-138">如果在 [**命令**](taskschedulerschema-command-exectype-element.md)、 [**引數**](taskschedulerschema-arguments-exectype-element.md)或 [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) 元素中使用環境變數，則會快取環境變數的值，並在啟動工作引擎)  (Taskeng.exe 時使用。</span><span class="sxs-lookup"><span data-stu-id="ac40b-138">If environment variables are used in the [**Command**](taskschedulerschema-command-exectype-element.md), [**Arguments**](taskschedulerschema-arguments-exectype-element.md), or [**WorkingDirectory**](taskschedulerschema-workingdirectory-exectype-element.md) elements, then the values of the environment variables are cached and used when the Taskeng.exe (the task engine) is launched.</span></span> <span data-ttu-id="ac40b-139">工作引擎啟動後所發生的環境變數變更將不會由工作引擎使用。</span><span class="sxs-lookup"><span data-stu-id="ac40b-139">Changes to the environment variables that occur after the task engine is launched will not be used by the task engine.</span></span>

## <a name="examples"></a><span data-ttu-id="ac40b-140">範例</span><span class="sxs-lookup"><span data-stu-id="ac40b-140">Examples</span></span>

<span data-ttu-id="ac40b-141">如需使用事件觸發程式之工作的完整 XML 範例，請參閱 [時間觸發程式範例 (xml) ](time-trigger-example--xml-.md)。</span><span class="sxs-lookup"><span data-stu-id="ac40b-141">For a complete example of the XML for a task that uses an event trigger, see [Time Trigger Example (XML)](time-trigger-example--xml-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ac40b-142">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac40b-142">Requirements</span></span>



| <span data-ttu-id="ac40b-143">需求</span><span class="sxs-lookup"><span data-stu-id="ac40b-143">Requirement</span></span> | <span data-ttu-id="ac40b-144">值</span><span class="sxs-lookup"><span data-stu-id="ac40b-144">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ac40b-145">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ac40b-145">Minimum supported client</span></span><br/> | <span data-ttu-id="ac40b-146">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac40b-146">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ac40b-147">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ac40b-147">Minimum supported server</span></span><br/> | <span data-ttu-id="ac40b-148">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ac40b-148">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ac40b-149">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac40b-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac40b-150">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="ac40b-150">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> </dl>

 

 





