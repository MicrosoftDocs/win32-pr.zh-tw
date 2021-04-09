---
title: IRDVTaskPluginNotifySink 介面
description: 工作代理程式會使用 IRDVTaskPluginNotifySink 介面來與觸發程式代理程式進行通訊。
ms.assetid: ccf19693-d3cc-4cf7-af35-947be047beeb
ms.tgt_platform: multiple
keywords:
- IRDVTaskPluginNotifySink 介面遠端桌面服務
- IRDVTaskPluginNotifySink 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IRDVTaskPluginNotifySink
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0dadaf387fcf6e8381404440e0d31dd210b9f8a6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103686050"
---
# <a name="irdvtaskpluginnotifysink-interface"></a><span data-ttu-id="717b8-105">IRDVTaskPluginNotifySink 介面</span><span class="sxs-lookup"><span data-stu-id="717b8-105">IRDVTaskPluginNotifySink interface</span></span>

<span data-ttu-id="717b8-106">工作代理程式會使用 **IRDVTaskPluginNotifySink** 介面來與觸發程式代理程式進行通訊。</span><span class="sxs-lookup"><span data-stu-id="717b8-106">The **IRDVTaskPluginNotifySink** interface is used by the task agent to communicate with the trigger agent.</span></span> <span data-ttu-id="717b8-107">這個介面的指標會傳遞至 [**IRDVTaskPlugin：： Initialize**](irdvtaskplugin-initialize.md) 方法中的工作代理程式。</span><span class="sxs-lookup"><span data-stu-id="717b8-107">A pointer to this interface is passed to the task agent in the [**IRDVTaskPlugin::Initialize**](irdvtaskplugin-initialize.md) method.</span></span>

## <a name="members"></a><span data-ttu-id="717b8-108">成員</span><span class="sxs-lookup"><span data-stu-id="717b8-108">Members</span></span>

<span data-ttu-id="717b8-109">**IRDVTaskPluginNotifySink** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="717b8-109">The **IRDVTaskPluginNotifySink** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="717b8-110">**IRDVTaskPluginNotifySink** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="717b8-110">**IRDVTaskPluginNotifySink** also has these types of members:</span></span>

-   [<span data-ttu-id="717b8-111">方法</span><span class="sxs-lookup"><span data-stu-id="717b8-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="717b8-112">方法</span><span class="sxs-lookup"><span data-stu-id="717b8-112">Methods</span></span>

<span data-ttu-id="717b8-113">**IRDVTaskPluginNotifySink** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="717b8-113">The **IRDVTaskPluginNotifySink** interface has these methods.</span></span>



| <span data-ttu-id="717b8-114">方法</span><span class="sxs-lookup"><span data-stu-id="717b8-114">Method</span></span>                                                                  | <span data-ttu-id="717b8-115">描述</span><span class="sxs-lookup"><span data-stu-id="717b8-115">Description</span></span>                                                                       |
|:------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [<span data-ttu-id="717b8-116">**DeleteSchedule**</span><span class="sxs-lookup"><span data-stu-id="717b8-116">**DeleteSchedule**</span></span>](irdvtaskpluginnotifysink-deleteschedule.md)       | <span data-ttu-id="717b8-117">由工作代理程式呼叫以刪除已排程的工作。</span><span class="sxs-lookup"><span data-stu-id="717b8-117">Called by the task agent to delete a scheduled task.</span></span><br/>                   |
| [<span data-ttu-id="717b8-118">**OnTaskStateChange**</span><span class="sxs-lookup"><span data-stu-id="717b8-118">**OnTaskStateChange**</span></span>](irdvtaskpluginnotifysink-ontaskstatechange.md) | <span data-ttu-id="717b8-119">用來通知觸發程式代理程式工作的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="717b8-119">Used to notify the trigger agent that the state of a task has changed.</span></span><br/> |
| [<span data-ttu-id="717b8-120">**OnTerminated**</span><span class="sxs-lookup"><span data-stu-id="717b8-120">**OnTerminated**</span></span>](irdvtaskpluginnotifysink-onterminated.md)           | <span data-ttu-id="717b8-121">由工作代理程式呼叫，以要求關閉工作代理程式。</span><span class="sxs-lookup"><span data-stu-id="717b8-121">Called by the task agent to request that the task agent be shut down.</span></span><br/>  |
| [<span data-ttu-id="717b8-122">**ScheduleTask**</span><span class="sxs-lookup"><span data-stu-id="717b8-122">**ScheduleTask**</span></span>](irdvtaskpluginnotifysink-scheduletask.md)           | <span data-ttu-id="717b8-123">由工作代理程式呼叫以排程工作。</span><span class="sxs-lookup"><span data-stu-id="717b8-123">Called by the task agent to schedule a task.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="717b8-124">備註</span><span class="sxs-lookup"><span data-stu-id="717b8-124">Remarks</span></span>

<span data-ttu-id="717b8-125">雖然下列需求中所識別的作業系統支援這個介面，但只有在虛擬機器裝載于 Windows Server 2012 時，才會使用此介面。</span><span class="sxs-lookup"><span data-stu-id="717b8-125">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="717b8-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="717b8-126">Requirements</span></span>



| <span data-ttu-id="717b8-127">需求</span><span class="sxs-lookup"><span data-stu-id="717b8-127">Requirement</span></span> | <span data-ttu-id="717b8-128">值</span><span class="sxs-lookup"><span data-stu-id="717b8-128">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="717b8-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="717b8-129">Minimum supported client</span></span><br/> | <span data-ttu-id="717b8-130">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="717b8-130">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="717b8-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="717b8-131">Minimum supported server</span></span><br/> | <span data-ttu-id="717b8-132">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="717b8-132">Windows Server 2008 R2</span></span><br/> |



 

