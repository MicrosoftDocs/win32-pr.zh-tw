---
title: ITsSbTaskPluginNotifySink 方法
description: ITsSbTaskPluginNotifySink 介面會公開下列方法。
ms.assetid: D22C72A3-E71B-4F00-85BA-0BAE3EFABEE4
ms.tgt_platform: multiple
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b2fcf8617efc64194952fad8e273decae2209a7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301763"
---
# <a name="itssbtaskpluginnotifysink-methods"></a><span data-ttu-id="3ddb3-103">ITsSbTaskPluginNotifySink 方法</span><span class="sxs-lookup"><span data-stu-id="3ddb3-103">ITsSbTaskPluginNotifySink Methods</span></span>

<span data-ttu-id="3ddb3-104">[**ITsSbTaskPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink)介面會公開下列方法。</span><span class="sxs-lookup"><span data-stu-id="3ddb3-104">The [**ITsSbTaskPluginNotifySink**](/windows/desktop/api/sbtsv/nn-sbtsv-itssbtaskpluginnotifysink) interfaces exposes the following methods.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="3ddb3-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="3ddb3-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="3ddb3-106">**OnDeleteTaskTime 方法**</span><span class="sxs-lookup"><span data-stu-id="3ddb3-106">**OnDeleteTaskTime method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskpluginnotifysink-ondeletetasktime)
</dt> <dd>

<span data-ttu-id="3ddb3-107">通知遠端桌面連線代理人 (RD 連線代理人) 已從佇列中移除工作。</span><span class="sxs-lookup"><span data-stu-id="3ddb3-107">Notifies Remote Desktop Connection Broker (RD Connection Broker) that a task has been removed from the queue.</span></span>

</dd> <dt>

[<span data-ttu-id="3ddb3-108">**OnReportTasks 方法**</span><span class="sxs-lookup"><span data-stu-id="3ddb3-108">**OnReportTasks method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskpluginnotifysink-onreporttasks)
</dt> <dd>

<span data-ttu-id="3ddb3-109">通知 RD 連線代理人新的工作報表。</span><span class="sxs-lookup"><span data-stu-id="3ddb3-109">Notifies RD Connection Broker of a new task report.</span></span>

</dd> <dt>

[<span data-ttu-id="3ddb3-110">**OnSetTaskTime 方法**</span><span class="sxs-lookup"><span data-stu-id="3ddb3-110">**OnSetTaskTime method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskpluginnotifysink-onsettasktime)
</dt> <dd>

<span data-ttu-id="3ddb3-111">通知 RD 連線代理人已排程工作。</span><span class="sxs-lookup"><span data-stu-id="3ddb3-111">Notifies RD Connection Broker that a task has been scheduled.</span></span>

</dd> <dt>

[<span data-ttu-id="3ddb3-112">**OnUpdateTaskStatus 方法**</span><span class="sxs-lookup"><span data-stu-id="3ddb3-112">**OnUpdateTaskStatus method**</span></span>](/windows/desktop/api/sbtsv/nf-sbtsv-itssbtaskpluginnotifysink-onupdatetaskstatus)
</dt> <dd>

<span data-ttu-id="3ddb3-113">通知 RD 連線代理人工作的狀態已變更。</span><span class="sxs-lookup"><span data-stu-id="3ddb3-113">Notifies RD Connection Broker that the status of a task has changed.</span></span>

</dd> </dl>

 

 




