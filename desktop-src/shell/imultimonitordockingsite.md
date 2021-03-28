---
description: 由瀏覽器所執行。 公開管理哪些監視在多個監視器系統上包含 Windows 工作列的方法。
title: IMultiMonitorDockingSite 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMultiMonitorDockingSite
api_type:
- COM
api_location: ''
ms.assetid: af9a7a9e-bd7c-4b17-9cb6-008df5c820d8
ms.openlocfilehash: 3aa1ccb1c25fd2896ce9e18ba52ea3f46b1882af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991822"
---
# <a name="imultimonitordockingsite-interface"></a><span data-ttu-id="e0667-104">IMultiMonitorDockingSite 介面</span><span class="sxs-lookup"><span data-stu-id="e0667-104">IMultiMonitorDockingSite interface</span></span>

<span data-ttu-id="e0667-105">由瀏覽器所執行。</span><span class="sxs-lookup"><span data-stu-id="e0667-105">Implemented by the browser.</span></span> <span data-ttu-id="e0667-106">公開管理哪些監視在多個監視器系統上包含 Windows 工作列的方法。</span><span class="sxs-lookup"><span data-stu-id="e0667-106">Exposes methods that manage which monitor contains the Windows taskbar on a multiple monitor system.</span></span>

## <a name="members"></a><span data-ttu-id="e0667-107">成員</span><span class="sxs-lookup"><span data-stu-id="e0667-107">Members</span></span>

<span data-ttu-id="e0667-108">**IMultiMonitorDockingSite** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="e0667-108">The **IMultiMonitorDockingSite** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e0667-109">**IMultiMonitorDockingSite** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="e0667-109">**IMultiMonitorDockingSite** also has these types of members:</span></span>

-   [<span data-ttu-id="e0667-110">方法</span><span class="sxs-lookup"><span data-stu-id="e0667-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="e0667-111">方法</span><span class="sxs-lookup"><span data-stu-id="e0667-111">Methods</span></span>

<span data-ttu-id="e0667-112">**IMultiMonitorDockingSite** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="e0667-112">The **IMultiMonitorDockingSite** interface has these methods.</span></span>



| <span data-ttu-id="e0667-113">方法</span><span class="sxs-lookup"><span data-stu-id="e0667-113">Method</span></span>                                                            | <span data-ttu-id="e0667-114">描述</span><span class="sxs-lookup"><span data-stu-id="e0667-114">Description</span></span>                                                                                |
|:------------------------------------------------------------------|:-------------------------------------------------------------------------------------------|
| [<span data-ttu-id="e0667-115">**GetMonitor**</span><span class="sxs-lookup"><span data-stu-id="e0667-115">**GetMonitor**</span></span>](imultimonitordockingsite-getmonitor.md)         | <span data-ttu-id="e0667-116">取得目前的預設監視器。</span><span class="sxs-lookup"><span data-stu-id="e0667-116">Gets the current default monitor.</span></span><br/>                                               |
| [<span data-ttu-id="e0667-117">**RequestMonitor**</span><span class="sxs-lookup"><span data-stu-id="e0667-117">**RequestMonitor**</span></span>](imultimonitordockingsite-requestmonitor.md) | <span data-ttu-id="e0667-118">確認監視器正在使用中且可供使用。</span><span class="sxs-lookup"><span data-stu-id="e0667-118">Verifies that the monitor is active and available.</span></span><br/>                              |
| [<span data-ttu-id="e0667-119">**SetMonitor**</span><span class="sxs-lookup"><span data-stu-id="e0667-119">**SetMonitor**</span></span>](imultimonitordockingsite-setmonitor.md)         | <span data-ttu-id="e0667-120">變更用於多個監視器系統上停駐工具列的監視器。</span><span class="sxs-lookup"><span data-stu-id="e0667-120">Changes which monitor is used for docked toolbars on a multiple monitor system.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="e0667-121">備註</span><span class="sxs-lookup"><span data-stu-id="e0667-121">Remarks</span></span>

<span data-ttu-id="e0667-122">您通常不會執行 **IMultiMonitorDockingSite** 介面。</span><span class="sxs-lookup"><span data-stu-id="e0667-122">You do not typically implement the **IMultiMonitorDockingSite** interface.</span></span> <span data-ttu-id="e0667-123">Shell 瀏覽器會執行這個介面，以支援多個監視器。</span><span class="sxs-lookup"><span data-stu-id="e0667-123">The Shell browser implements this interface to support multiple monitors.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0667-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="e0667-124">Requirements</span></span>



| <span data-ttu-id="e0667-125">需求</span><span class="sxs-lookup"><span data-stu-id="e0667-125">Requirement</span></span> | <span data-ttu-id="e0667-126">值</span><span class="sxs-lookup"><span data-stu-id="e0667-126">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------|
| <span data-ttu-id="e0667-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e0667-127">Minimum supported client</span></span><br/> | <span data-ttu-id="e0667-128">僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0667-128">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="e0667-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e0667-129">Minimum supported server</span></span><br/> | <span data-ttu-id="e0667-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e0667-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                   |



 

 
