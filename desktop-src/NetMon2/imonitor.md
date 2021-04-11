---
description: IMonitor 介面提供控制監視作業的方法。 監視器控制服務會呼叫這些方法 (MCSVC) 。
ms.assetid: 53140e7d-c3a1-45cd-aaa4-c6f5021a6102
title: 'IMonitor 介面 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMonitor
api_type:
- COM
api_location:
- Netmon.h
ms.openlocfilehash: 1b6ba91860905010fd14a46cd4608eaee3da80fa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848367"
---
# <a name="imonitor-interface"></a><span data-ttu-id="685a3-104">IMonitor 介面</span><span class="sxs-lookup"><span data-stu-id="685a3-104">IMonitor interface</span></span>

<span data-ttu-id="685a3-105">**IMonitor** 介面提供控制監視作業的方法。</span><span class="sxs-lookup"><span data-stu-id="685a3-105">The **IMonitor** interface provides methods that control monitor operation.</span></span> <span data-ttu-id="685a3-106">[*監視器控制服務*](m.md)會呼叫這些方法 (MCSVC) 。</span><span class="sxs-lookup"><span data-stu-id="685a3-106">These methods are called by the [*Monitor Control Service*](m.md) (MCSVC).</span></span>

## <a name="members"></a><span data-ttu-id="685a3-107">成員</span><span class="sxs-lookup"><span data-stu-id="685a3-107">Members</span></span>

<span data-ttu-id="685a3-108">**IMonitor** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="685a3-108">The **IMonitor** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="685a3-109">**IMonitor** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="685a3-109">**IMonitor** also has these types of members:</span></span>

-   [<span data-ttu-id="685a3-110">方法</span><span class="sxs-lookup"><span data-stu-id="685a3-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="685a3-111">方法</span><span class="sxs-lookup"><span data-stu-id="685a3-111">Methods</span></span>

<span data-ttu-id="685a3-112">**IMonitor** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="685a3-112">The **IMonitor** interface has these methods.</span></span>



| <span data-ttu-id="685a3-113">方法</span><span class="sxs-lookup"><span data-stu-id="685a3-113">Method</span></span>                                        | <span data-ttu-id="685a3-114">描述</span><span class="sxs-lookup"><span data-stu-id="685a3-114">Description</span></span>                                                                                                         |
|:----------------------------------------------|:--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="685a3-115">**DoConfigure**</span><span class="sxs-lookup"><span data-stu-id="685a3-115">**DoConfigure**</span></span>](imonitor-doconfigure.md)   | <span data-ttu-id="685a3-116">更新監視設定。</span><span class="sxs-lookup"><span data-stu-id="685a3-116">Updates monitor configuration.</span></span><br/>                                                                           |
| [<span data-ttu-id="685a3-117">**DoInitialize**</span><span class="sxs-lookup"><span data-stu-id="685a3-117">**DoInitialize**</span></span>](imonitor-doinitialize.md) | <span data-ttu-id="685a3-118">初始化監視器。</span><span class="sxs-lookup"><span data-stu-id="685a3-118">Initializes a monitor.</span></span><br/>                                                                                   |
| [<span data-ttu-id="685a3-119">**OnFrames**</span><span class="sxs-lookup"><span data-stu-id="685a3-119">**OnFrames**</span></span>](imonitor-onframes.md)         | <span data-ttu-id="685a3-120">指出框架事件的狀態。</span><span class="sxs-lookup"><span data-stu-id="685a3-120">Indicates the status of a frame event.</span></span><br/>                                                                   |
| [<span data-ttu-id="685a3-121">**OnStart**</span><span class="sxs-lookup"><span data-stu-id="685a3-121">**OnStart**</span></span>](imonitor-onstart.md)           | <span data-ttu-id="685a3-122">表示已成功設定監視，且資料捕捉即將開始。</span><span class="sxs-lookup"><span data-stu-id="685a3-122">Indicates that the monitor has been configured successfully and that the data capture is about to begin.</span></span><br/> |
| [<span data-ttu-id="685a3-123">**OnStatus**</span><span class="sxs-lookup"><span data-stu-id="685a3-123">**OnStatus**</span></span>](imonitor-onstatus.md)         | <span data-ttu-id="685a3-124">表示 NPP 狀態事件。</span><span class="sxs-lookup"><span data-stu-id="685a3-124">Indicates an NPP status event.</span></span><br/>                                                                           |
| [<span data-ttu-id="685a3-125">**S**</span><span class="sxs-lookup"><span data-stu-id="685a3-125">**OnStop**</span></span>](imonitor-onstop.md)             | <span data-ttu-id="685a3-126">表示資料捕獲完成。</span><span class="sxs-lookup"><span data-stu-id="685a3-126">Indicates data capture completion.</span></span><br/>                                                                       |



 

## <a name="requirements"></a><span data-ttu-id="685a3-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="685a3-127">Requirements</span></span>



| <span data-ttu-id="685a3-128">需求</span><span class="sxs-lookup"><span data-stu-id="685a3-128">Requirement</span></span> | <span data-ttu-id="685a3-129">值</span><span class="sxs-lookup"><span data-stu-id="685a3-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="685a3-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="685a3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="685a3-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="685a3-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="685a3-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="685a3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="685a3-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="685a3-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="685a3-134">標頭</span><span class="sxs-lookup"><span data-stu-id="685a3-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="685a3-135"><dt>Netmon</dt></span><span class="sxs-lookup"><span data-stu-id="685a3-135"><dt>Netmon.h</dt></span></span> </dl> |



 

