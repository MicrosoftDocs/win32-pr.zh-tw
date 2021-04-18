---
title: WorkingDirectory (execType) 元素
description: 指定可執行檔或可執行檔所使用的檔案所在的目錄。
ms.assetid: 09e53748-6d21-42df-bbdd-f0fd9693aab0
keywords:
- WorkingDirectory 元素工作排程器
topic_type:
- apiref
api_name:
- WorkingDirectory
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e8c382d0e60b16d85fbc86f7579a0e700d3dd30b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965532"
---
# <a name="workingdirectory-exectype-element"></a><span data-ttu-id="1ed07-104">WorkingDirectory (execType) 元素</span><span class="sxs-lookup"><span data-stu-id="1ed07-104">WorkingDirectory (execType) Element</span></span>

<span data-ttu-id="1ed07-105">指定可執行檔或可執行檔所使用的檔案所在的目錄。</span><span class="sxs-lookup"><span data-stu-id="1ed07-105">Specifies the directory where either the executable or those files used by the executable exists.</span></span>

``` syntax
<xs:element name="WorkingDirectory"
    type="pathType"
 />
```

<span data-ttu-id="1ed07-106">**WorkingDirectory** 元素是由 [**execType**](taskschedulerschema-exectype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="1ed07-106">The **WorkingDirectory** element is defined by the [**execType**](taskschedulerschema-exectype-complextype.md) complex type.</span></span>

## <a name="parent-element"></a><span data-ttu-id="1ed07-107">父元素</span><span class="sxs-lookup"><span data-stu-id="1ed07-107">Parent element</span></span>



| <span data-ttu-id="1ed07-108">元素</span><span class="sxs-lookup"><span data-stu-id="1ed07-108">Element</span></span>                                                      | <span data-ttu-id="1ed07-109">衍生自</span><span class="sxs-lookup"><span data-stu-id="1ed07-109">Derived from</span></span>                                                 | <span data-ttu-id="1ed07-110">Description</span><span class="sxs-lookup"><span data-stu-id="1ed07-110">Description</span></span>                                                            |
|--------------------------------------------------------------|--------------------------------------------------------------|------------------------------------------------------------------------|
| [<span data-ttu-id="1ed07-111">**Exec**</span><span class="sxs-lookup"><span data-stu-id="1ed07-111">**Exec**</span></span>](taskschedulerschema-exec-actiongroup-element.md) | [<span data-ttu-id="1ed07-112">**execType**</span><span class="sxs-lookup"><span data-stu-id="1ed07-112">**execType**</span></span>](taskschedulerschema-exectype-complextype.md) | <span data-ttu-id="1ed07-113">指定執行命令列操作的動作。</span><span class="sxs-lookup"><span data-stu-id="1ed07-113">Specifies an action that executes a command-line operation.</span></span><br/> |



## <a name="remarks"></a><span data-ttu-id="1ed07-114">備註</span><span class="sxs-lookup"><span data-stu-id="1ed07-114">Remarks</span></span>

<span data-ttu-id="1ed07-115">針對腳本開發，工作目錄是由 [**ExecAction. WorkingDirectory**](execaction-workingdirectory.md) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="1ed07-115">For script development, the working directory is specified by the [**ExecAction.WorkingDirectory**](execaction-workingdirectory.md) property.</span></span>

<span data-ttu-id="1ed07-116">針對 c + + 開發，工作目錄是由 [**IExecAction：： WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) 屬性所指定。</span><span class="sxs-lookup"><span data-stu-id="1ed07-116">For C++ development, the working directory is specified by the [**IExecAction::WorkingDirectory**](/windows/desktop/api/taskschd/nf-taskschd-iexecaction-get_workingdirectory) property.</span></span>

## <a name="examples"></a><span data-ttu-id="1ed07-117">範例</span><span class="sxs-lookup"><span data-stu-id="1ed07-117">Examples</span></span>

<span data-ttu-id="1ed07-118">下列 XML 會定義執行動作。</span><span class="sxs-lookup"><span data-stu-id="1ed07-118">The following XML defines a execution action.</span></span>


```XML
<Exec>
    <Command></Command>
    <Arguments></Arguments>
    <WorkingDirectory></WorkingDirectory>
</ServiceResume>
```



## <a name="requirements"></a><span data-ttu-id="1ed07-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="1ed07-119">Requirements</span></span>



| <span data-ttu-id="1ed07-120">需求</span><span class="sxs-lookup"><span data-stu-id="1ed07-120">Requirement</span></span> | <span data-ttu-id="1ed07-121">值</span><span class="sxs-lookup"><span data-stu-id="1ed07-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="1ed07-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="1ed07-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1ed07-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ed07-123">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="1ed07-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="1ed07-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1ed07-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="1ed07-125">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="1ed07-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1ed07-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ed07-127">工作排程器架構元素</span><span class="sxs-lookup"><span data-stu-id="1ed07-127">Task Scheduler Schema Elements</span></span>](task-scheduler-schema-elements.md)
</dt> <dt>

[<span data-ttu-id="1ed07-128">工作排程器</span><span class="sxs-lookup"><span data-stu-id="1ed07-128">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





