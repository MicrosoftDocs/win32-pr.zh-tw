---
description: 指定拓撲分支的相對執行緒優先順序。
ms.assetid: 7BCD2EE0-94FB-4438-9B6A-7B26DBFB5978
title: 'MF_TOPONODE_WORKQUEUE_MMCSS_PRIORITY 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0667c91054f8711b8825cf421a2ee565b9161f3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114020"
---
# <a name="mf_toponode_workqueue_mmcss_priority-attribute"></a><span data-ttu-id="f6eb4-103">MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ PRIORITY 屬性</span><span class="sxs-lookup"><span data-stu-id="f6eb4-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_PRIORITY attribute</span></span>

<span data-ttu-id="f6eb4-104">指定拓撲分支的相對執行緒優先順序。</span><span class="sxs-lookup"><span data-stu-id="f6eb4-104">Specifies the relative thread priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="f6eb4-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="f6eb4-105">Data type</span></span>

<span data-ttu-id="f6eb4-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="f6eb4-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="f6eb4-107">備註</span><span class="sxs-lookup"><span data-stu-id="f6eb4-107">Remarks</span></span>

<span data-ttu-id="f6eb4-108">這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。</span><span class="sxs-lookup"><span data-stu-id="f6eb4-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="f6eb4-109">屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="f6eb4-109">The attribute is optional.</span></span>

<span data-ttu-id="f6eb4-110">此屬性需要相同節點上的 [mf \_ TOPONODE \_ WORKQUEUE \_ 識別碼](mf-toponode-workqueue-id-attribute.md) 和 [mf \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別](mf-toponode-workqueue-mmcss-class-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="f6eb4-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) and [MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS](mf-toponode-workqueue-mmcss-class-attribute.md) attributes on the same node.</span></span>

<span data-ttu-id="f6eb4-111">屬性的值是此拓撲分支之工作佇列的相對執行緒優先順序。</span><span class="sxs-lookup"><span data-stu-id="f6eb4-111">The value of the attribute is the relative thread priority of the work queue for this branch of the topology.</span></span> <span data-ttu-id="f6eb4-112">[多媒體類別](../procthread/multimedia-class-scheduler-service.md)排程器服務 (MMCSS) 會在設定執行緒優先順序時使用相對優先權。</span><span class="sxs-lookup"><span data-stu-id="f6eb4-112">The [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) uses the relative priority when it sets the thread priority.</span></span> <span data-ttu-id="f6eb4-113">如需詳細資訊，請參閱 [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority)。</span><span class="sxs-lookup"><span data-stu-id="f6eb4-113">For more information, see [**AvSetMmThreadPriority**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadpriority).</span></span>

<span data-ttu-id="f6eb4-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="f6eb4-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="f6eb4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f6eb4-115">Requirements</span></span>



| <span data-ttu-id="f6eb4-116">需求</span><span class="sxs-lookup"><span data-stu-id="f6eb4-116">Requirement</span></span> | <span data-ttu-id="f6eb4-117">值</span><span class="sxs-lookup"><span data-stu-id="f6eb4-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="f6eb4-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f6eb4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="f6eb4-119">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6eb4-119">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f6eb4-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f6eb4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="f6eb4-121">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f6eb4-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="f6eb4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="f6eb4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="f6eb4-123"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f6eb4-123"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f6eb4-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f6eb4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6eb4-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="f6eb4-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6eb4-126">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="f6eb4-126">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="f6eb4-127">工作佇列和執行緒改進</span><span class="sxs-lookup"><span data-stu-id="f6eb4-127">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="f6eb4-128">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="f6eb4-128">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="f6eb4-129">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="f6eb4-129">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="f6eb4-130">**MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="f6eb4-130">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="f6eb4-131">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="f6eb4-131">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> </dl>

 

 
