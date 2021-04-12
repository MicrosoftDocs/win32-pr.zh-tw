---
title: ComHandlerAction 物件
description: 代表引發處理常式之動作的腳本物件。
ms.assetid: 47ffe52f-b7b7-4486-a00d-6105395f23c0
keywords:
- COM 處理常式動作工作排程器，物件
- ComHandlerAction 物件工作排程器
- ComHandlerAction 物件工作排程器，說明
topic_type:
- apiref
api_name:
- ComHandlerAction
api_location:
- taskschd.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02d7e8371deda260c407682181fd31e29886b777
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464193"
---
# <a name="comhandleraction-object"></a><span data-ttu-id="f0200-106">ComHandlerAction 物件</span><span class="sxs-lookup"><span data-stu-id="f0200-106">ComHandlerAction object</span></span>

<span data-ttu-id="f0200-107">代表引發處理常式之動作的腳本物件。</span><span class="sxs-lookup"><span data-stu-id="f0200-107">Scripting object that represents an action that fires a handler.</span></span>

## <a name="members"></a><span data-ttu-id="f0200-108">成員</span><span class="sxs-lookup"><span data-stu-id="f0200-108">Members</span></span>

<span data-ttu-id="f0200-109">**ComHandlerAction** 物件具有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="f0200-109">The **ComHandlerAction** object has these types of members:</span></span>

-   [<span data-ttu-id="f0200-110">屬性</span><span class="sxs-lookup"><span data-stu-id="f0200-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f0200-111">屬性</span><span class="sxs-lookup"><span data-stu-id="f0200-111">Properties</span></span>

<span data-ttu-id="f0200-112">**ComHandlerAction** 物件具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="f0200-112">The **ComHandlerAction** object has these properties.</span></span>



| <span data-ttu-id="f0200-113">屬性</span><span class="sxs-lookup"><span data-stu-id="f0200-113">Property</span></span>                                               | <span data-ttu-id="f0200-114">存取類型</span><span class="sxs-lookup"><span data-stu-id="f0200-114">Access type</span></span>           | <span data-ttu-id="f0200-115">Description</span><span class="sxs-lookup"><span data-stu-id="f0200-115">Description</span></span>                                                                                               |
|:-------------------------------------------------------|:----------------------|:----------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f0200-116">**ClassId**</span><span class="sxs-lookup"><span data-stu-id="f0200-116">**ClassId**</span></span>](comhandleraction-classid.md)<br/> | <span data-ttu-id="f0200-117">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f0200-117">Read/write</span></span><br/> | <span data-ttu-id="f0200-118">取得或設定處理常式類別的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0200-118">Gets or sets the identifier of the handler class.</span></span><br/>                                              |
| [<span data-ttu-id="f0200-119">**資料**</span><span class="sxs-lookup"><span data-stu-id="f0200-119">**Data**</span></span>](comhandleraction-data.md)<br/>       | <span data-ttu-id="f0200-120">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f0200-120">Read/write</span></span><br/> | <span data-ttu-id="f0200-121">取得或設定與處理常式相關聯的其他資料。</span><span class="sxs-lookup"><span data-stu-id="f0200-121">Gets or sets additional data that is associated with the handler.</span></span><br/>                              |
| [<span data-ttu-id="f0200-122">**Id**</span><span class="sxs-lookup"><span data-stu-id="f0200-122">**Id**</span></span>](action-id.md)<br/>                     | <span data-ttu-id="f0200-123">讀取/寫入</span><span class="sxs-lookup"><span data-stu-id="f0200-123">Read/write</span></span><br/> | <span data-ttu-id="f0200-124">繼承自 [**動作**](action.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f0200-124">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="f0200-125">取得或設定動作的識別碼。</span><span class="sxs-lookup"><span data-stu-id="f0200-125">Gets or sets the identifier of the action.</span></span><br/> |
| [<span data-ttu-id="f0200-126">**類型**</span><span class="sxs-lookup"><span data-stu-id="f0200-126">**Type**</span></span>](action-type.md)<br/>                 | <span data-ttu-id="f0200-127">唯讀</span><span class="sxs-lookup"><span data-stu-id="f0200-127">Read-only</span></span><br/>  | <span data-ttu-id="f0200-128">繼承自 [**動作**](action.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="f0200-128">Inherited from the [**Action**](action.md) object.</span></span> <span data-ttu-id="f0200-129">取得動作的類型。</span><span class="sxs-lookup"><span data-stu-id="f0200-129">Gets the type of the action.</span></span><br/>               |



 

## <a name="remarks"></a><span data-ttu-id="f0200-130">備註</span><span class="sxs-lookup"><span data-stu-id="f0200-130">Remarks</span></span>

<span data-ttu-id="f0200-131">COM 處理常式必須針對工作排程器執行 [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) 介面，以啟動和停止處理常式。</span><span class="sxs-lookup"><span data-stu-id="f0200-131">COM handlers must implement the [**ITaskHandler**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandler) interface for the Task Scheduler to start and stop the handler.</span></span> <span data-ttu-id="f0200-132">接著，COM 處理常式會使用 [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) 物件的方法，將狀態傳達給工作排程器。</span><span class="sxs-lookup"><span data-stu-id="f0200-132">In turn, the COM handler uses the methods of the [**TaskHandlerStatus**](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus) object to communicate the status back to the Task Scheduler.</span></span>

<span data-ttu-id="f0200-133">讀取或寫入 XML 時，會在工作排程器架構的 [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) 元素中指定 COM 處理常式動作。</span><span class="sxs-lookup"><span data-stu-id="f0200-133">When reading or writing XML, a COM handler action is specified in the [**ComHandler**](taskschedulerschema-comhandler-actiongroup-element.md) element of the Task Scheduler schema.</span></span>

## <a name="requirements"></a><span data-ttu-id="f0200-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="f0200-134">Requirements</span></span>



| <span data-ttu-id="f0200-135">需求</span><span class="sxs-lookup"><span data-stu-id="f0200-135">Requirement</span></span> | <span data-ttu-id="f0200-136">值</span><span class="sxs-lookup"><span data-stu-id="f0200-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f0200-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f0200-137">Minimum supported client</span></span><br/> | <span data-ttu-id="f0200-138">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0200-138">Windows Vista \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="f0200-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f0200-139">Minimum supported server</span></span><br/> | <span data-ttu-id="f0200-140">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f0200-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f0200-141">類型程式庫</span><span class="sxs-lookup"><span data-stu-id="f0200-141">Type library</span></span><br/>             | <dl> <span data-ttu-id="f0200-142"><dt>Taskschd.msc .tlb</dt></span><span class="sxs-lookup"><span data-stu-id="f0200-142"><dt>Taskschd.tlb</dt></span></span> </dl> |
| <span data-ttu-id="f0200-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f0200-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f0200-144"><dt>Taskschd.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f0200-144"><dt>Taskschd.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f0200-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f0200-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f0200-146">**TaskHandlerStatus**</span><span class="sxs-lookup"><span data-stu-id="f0200-146">**TaskHandlerStatus**</span></span>](/windows/desktop/api/taskschd/nn-taskschd-itaskhandlerstatus)
</dt> <dt>

[<span data-ttu-id="f0200-147">工作排程器物件</span><span class="sxs-lookup"><span data-stu-id="f0200-147">Task Scheduler Objects</span></span>](task-scheduler-objects.md)
</dt> <dt>

[<span data-ttu-id="f0200-148">工作排程器</span><span class="sxs-lookup"><span data-stu-id="f0200-148">Task Scheduler</span></span>](task-scheduler-start-page.md)
</dt> </dl>

 

 





