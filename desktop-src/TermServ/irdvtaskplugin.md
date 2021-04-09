---
title: IRDVTaskPlugin 介面
description: IRDVTaskPlugin 介面是由虛擬機器更新工作代理程式所執行，可讓工作代理程式管理虛擬機器的系統更新。
ms.assetid: e06eb707-be78-4d1f-96d3-21526b167e61
ms.tgt_platform: multiple
keywords:
- IRDVTaskPlugin 介面遠端桌面服務
- IRDVTaskPlugin 介面遠端桌面服務，說明
topic_type:
- apiref
api_name:
- IRDVTaskPlugin
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 59e90e899e8084f7fbc6b0b6f11067061eaa807b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935061"
---
# <a name="irdvtaskplugin-interface"></a><span data-ttu-id="909ea-105">IRDVTaskPlugin 介面</span><span class="sxs-lookup"><span data-stu-id="909ea-105">IRDVTaskPlugin interface</span></span>

<span data-ttu-id="909ea-106">**IRDVTaskPlugin** 介面是由虛擬機器更新工作 *代理程式* 所執行，可讓工作代理程式管理虛擬機器的系統更新。</span><span class="sxs-lookup"><span data-stu-id="909ea-106">The **IRDVTaskPlugin** interface is implemented by a virtual machine update *task agent* to allow the task agent to manage system updates for a virtual machine.</span></span> <span data-ttu-id="909ea-107">此介面是由主機系統所執行的 *觸發程式代理程式* 所使用。</span><span class="sxs-lookup"><span data-stu-id="909ea-107">This interface is used by the *trigger agent*, which is implemented by the host system.</span></span>

## <a name="members"></a><span data-ttu-id="909ea-108">成員</span><span class="sxs-lookup"><span data-stu-id="909ea-108">Members</span></span>

<span data-ttu-id="909ea-109">**IRDVTaskPlugin** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="909ea-109">The **IRDVTaskPlugin** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="909ea-110">**IRDVTaskPlugin** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="909ea-110">**IRDVTaskPlugin** also has these types of members:</span></span>

-   [<span data-ttu-id="909ea-111">方法</span><span class="sxs-lookup"><span data-stu-id="909ea-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="909ea-112">屬性</span><span class="sxs-lookup"><span data-stu-id="909ea-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="909ea-113">方法</span><span class="sxs-lookup"><span data-stu-id="909ea-113">Methods</span></span>

<span data-ttu-id="909ea-114">**IRDVTaskPlugin** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="909ea-114">The **IRDVTaskPlugin** interface has these methods.</span></span>



| <span data-ttu-id="909ea-115">方法</span><span class="sxs-lookup"><span data-stu-id="909ea-115">Method</span></span>                                          | <span data-ttu-id="909ea-116">描述</span><span class="sxs-lookup"><span data-stu-id="909ea-116">Description</span></span>                                                        |
|:------------------------------------------------|:-------------------------------------------------------------------|
| [<span data-ttu-id="909ea-117">**初始化**</span><span class="sxs-lookup"><span data-stu-id="909ea-117">**Initialize**</span></span>](irdvtaskplugin-initialize.md) | <span data-ttu-id="909ea-118">呼叫以初始化工作代理程式。</span><span class="sxs-lookup"><span data-stu-id="909ea-118">Called to initialize the task agent.</span></span><br/>                    |
| [<span data-ttu-id="909ea-119">**StartTask**</span><span class="sxs-lookup"><span data-stu-id="909ea-119">**StartTask**</span></span>](irdvtaskplugin-starttask.md)   | <span data-ttu-id="909ea-120">呼叫以啟動虛擬機器上的更新工作。</span><span class="sxs-lookup"><span data-stu-id="909ea-120">Called to start the update task on the virtual machine.</span></span><br/> |
| [<span data-ttu-id="909ea-121">**終止**</span><span class="sxs-lookup"><span data-stu-id="909ea-121">**Terminate**</span></span>](irdvtaskplugin-terminate.md)   | <span data-ttu-id="909ea-122">在工作代理程式關閉時呼叫。</span><span class="sxs-lookup"><span data-stu-id="909ea-122">Called when the task agent is being shut down.</span></span><br/>          |



 

### <a name="properties"></a><span data-ttu-id="909ea-123">屬性</span><span class="sxs-lookup"><span data-stu-id="909ea-123">Properties</span></span>

<span data-ttu-id="909ea-124">**IRDVTaskPlugin** 介面具有這些屬性。</span><span class="sxs-lookup"><span data-stu-id="909ea-124">The **IRDVTaskPlugin** interface has these properties.</span></span>



| <span data-ttu-id="909ea-125">屬性</span><span class="sxs-lookup"><span data-stu-id="909ea-125">Property</span></span>                                                   | <span data-ttu-id="909ea-126">存取類型</span><span class="sxs-lookup"><span data-stu-id="909ea-126">Access type</span></span>          | <span data-ttu-id="909ea-127">Description</span><span class="sxs-lookup"><span data-stu-id="909ea-127">Description</span></span>                                             |
|:-----------------------------------------------------------|:---------------------|:--------------------------------------------------------|
| [<span data-ttu-id="909ea-128">**PluginName**</span><span class="sxs-lookup"><span data-stu-id="909ea-128">**PluginName**</span></span>](irdvtaskplugin-pluginname.md)<br/> | <span data-ttu-id="909ea-129">唯讀</span><span class="sxs-lookup"><span data-stu-id="909ea-129">Read-only</span></span><br/> | <span data-ttu-id="909ea-130">包含工作代理程式的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="909ea-130">Contains the display name of the task agent.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="909ea-131">備註</span><span class="sxs-lookup"><span data-stu-id="909ea-131">Remarks</span></span>

<span data-ttu-id="909ea-132">當虛擬機器已排程進行系統更新時，就會在虛擬機器上執行工作代理程式。</span><span class="sxs-lookup"><span data-stu-id="909ea-132">The task agent is run on the virtual machine when that virtual machine is scheduled for a system update.</span></span> <span data-ttu-id="909ea-133">當呼叫 [**StartTask**](irdvtaskplugin-starttask.md) 方法時，工作代理程式會更新虛擬機器。</span><span class="sxs-lookup"><span data-stu-id="909ea-133">The task agent updates the virtual machine when the [**StartTask**](irdvtaskplugin-starttask.md) method is called.</span></span>

<span data-ttu-id="909ea-134">若要註冊工作代理程式，請將下列機碼新增至虛擬機器的登錄：</span><span class="sxs-lookup"><span data-stu-id="909ea-134">To register the task agent, add the following key to the registry of the virtual machine:</span></span>

<span data-ttu-id="909ea-135">**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **Microsoft** \\ **Windows NT** \\ **CurrentVersion** \\ **Terminal Server** \\ **Task** \\ **外掛程式** \\ **TaskAgentName**</span><span class="sxs-lookup"><span data-stu-id="909ea-135">**HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Windows NT**\\**CurrentVersion**\\**Terminal Server**\\**Task**\\**Plugins**\\**TaskAgentName**</span></span>

<span data-ttu-id="909ea-136">在此登錄機碼底下，新增下列值：</span><span class="sxs-lookup"><span data-stu-id="909ea-136">Under this registry key, add the following values:</span></span>



| <span data-ttu-id="909ea-137">名稱</span><span class="sxs-lookup"><span data-stu-id="909ea-137">Name</span></span>                     | <span data-ttu-id="909ea-138">類型</span><span class="sxs-lookup"><span data-stu-id="909ea-138">Type</span></span>                      | <span data-ttu-id="909ea-139">Description</span><span class="sxs-lookup"><span data-stu-id="909ea-139">Description</span></span>                                                                   |
|--------------------------|---------------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="909ea-140">**Clsid**</span><span class="sxs-lookup"><span data-stu-id="909ea-140">**CLSID**</span></span><br/>     | <span data-ttu-id="909ea-141">**REG \_ SZ**</span><span class="sxs-lookup"><span data-stu-id="909ea-141">**REG\_SZ**</span></span><br/>    | <span data-ttu-id="909ea-142">表示工作代理程式 **CLSID** 的字串。</span><span class="sxs-lookup"><span data-stu-id="909ea-142">A string that represents the **CLSID** of the task agent.</span></span><br/>          |
| <span data-ttu-id="909ea-143">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="909ea-143">**IsEnabled**</span></span><br/> | <span data-ttu-id="909ea-144">**REG \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="909ea-144">**REG\_DWORD**</span></span><br/> | <span data-ttu-id="909ea-145">如果工作代理程式已停用，則為 0; 如果工作代理程式已啟用，則為1。</span><span class="sxs-lookup"><span data-stu-id="909ea-145">0 if the task agent is disabled or 1 if the task agent is enabled.</span></span><br/> |



 

> [!Note]  
> <span data-ttu-id="909ea-146">您可以註冊一個以上的工作代理程式，但只會使用一個工作代理程式。</span><span class="sxs-lookup"><span data-stu-id="909ea-146">More than one task agent can be registered, but only one task agent will be used.</span></span> <span data-ttu-id="909ea-147">如果啟用多個工作代理程式，則只會使用找到的第一個工作代理程式。</span><span class="sxs-lookup"><span data-stu-id="909ea-147">If more than one task agent is enabled, only the first one found will be used.</span></span>

 

<span data-ttu-id="909ea-148">雖然下列需求中所識別的作業系統支援這個介面，但只有在虛擬機器裝載于 Windows Server 2012 時，才會使用此介面。</span><span class="sxs-lookup"><span data-stu-id="909ea-148">Although this interface is supported on the operating systems identified in the Requirements below, it will only be used if the virtual machine is hosted on Windows Server 2012.</span></span>

## <a name="requirements"></a><span data-ttu-id="909ea-149">規格需求</span><span class="sxs-lookup"><span data-stu-id="909ea-149">Requirements</span></span>



| <span data-ttu-id="909ea-150">需求</span><span class="sxs-lookup"><span data-stu-id="909ea-150">Requirement</span></span> | <span data-ttu-id="909ea-151">值</span><span class="sxs-lookup"><span data-stu-id="909ea-151">Value</span></span> |
|-------------------------------------|-----------------------------------|
| <span data-ttu-id="909ea-152">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="909ea-152">Minimum supported client</span></span><br/> | <span data-ttu-id="909ea-153">Windows 7 Enterprise</span><span class="sxs-lookup"><span data-stu-id="909ea-153">Windows 7 Enterprise</span></span><br/>   |
| <span data-ttu-id="909ea-154">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="909ea-154">Minimum supported server</span></span><br/> | <span data-ttu-id="909ea-155">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="909ea-155">Windows Server 2008 R2</span></span><br/> |



 

