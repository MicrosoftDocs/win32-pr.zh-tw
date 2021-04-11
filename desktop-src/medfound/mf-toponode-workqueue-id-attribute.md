---
description: 指定拓撲分支的工作佇列。
ms.assetid: 5bc7e2db-cfd2-4b94-b4d6-fe2b9ea9daf8
title: 'MF_TOPONODE_WORKQUEUE_ID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f9acda95895a1812f6cebbe64cbf3cd3bcdea4eb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114021"
---
# <a name="mf_toponode_workqueue_id-attribute"></a><span data-ttu-id="eb990-103">MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼屬性</span><span class="sxs-lookup"><span data-stu-id="eb990-103">MF\_TOPONODE\_WORKQUEUE\_ID attribute</span></span>

<span data-ttu-id="eb990-104">指定拓撲分支的工作佇列。</span><span class="sxs-lookup"><span data-stu-id="eb990-104">Specifies a work queue for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="eb990-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="eb990-105">Data type</span></span>

<span data-ttu-id="eb990-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="eb990-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="eb990-107">備註</span><span class="sxs-lookup"><span data-stu-id="eb990-107">Remarks</span></span>

<span data-ttu-id="eb990-108">這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。</span><span class="sxs-lookup"><span data-stu-id="eb990-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="eb990-109">屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="eb990-109">The attribute is optional.</span></span>

<span data-ttu-id="eb990-110">屬性的值是工作佇列的應用程式定義識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb990-110">The value of the attribute is an application-defined identifier for the work queue.</span></span>

<span data-ttu-id="eb990-111">應用程式可以使用這個屬性，將工作佇列指派給拓撲的分支。</span><span class="sxs-lookup"><span data-stu-id="eb990-111">Applications can use this attribute to assign work queues to branches of the topology.</span></span> <span data-ttu-id="eb990-112">拓撲中的每個來源節點都會定義一個分支。</span><span class="sxs-lookup"><span data-stu-id="eb990-112">Each source node in the topology defines one branch.</span></span> <span data-ttu-id="eb990-113">分支包含每個從該節點接收資料的拓撲節點。</span><span class="sxs-lookup"><span data-stu-id="eb990-113">The branch includes every topology node that receives data from that node.</span></span>

<span data-ttu-id="eb990-114">如果設定此屬性，請在已解析的拓撲上呼叫 [**IMFWorkQueueServices：： BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) 方法。</span><span class="sxs-lookup"><span data-stu-id="eb990-114">If you set this attribute, call the [**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss) method on the resolved topology.</span></span> <span data-ttu-id="eb990-115">拓撲中的多個分支可以共用相同的工作佇列，而工作佇列可以跨拓撲重複使用。</span><span class="sxs-lookup"><span data-stu-id="eb990-115">Multiple branches in the topology can share the same work queue, and work queues can be re-used across topologies.</span></span>

> [!Note]  
> <span data-ttu-id="eb990-116">這個屬性的值與 [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) 函數所傳回的識別碼不同。</span><span class="sxs-lookup"><span data-stu-id="eb990-116">The value of this attribute is not the same as the identifier that is returned by the [**MFAllocateWorkQueue**](/windows/desktop/api/mfapi/nf-mfapi-mfallocateworkqueue) function.</span></span> <span data-ttu-id="eb990-117">屬性的值是應用程式定義的識別碼，可用來將拓撲分支與工作佇列產生關聯。</span><span class="sxs-lookup"><span data-stu-id="eb990-117">The value of the attribute is an application-defined identifier, and is used to associate topology branches with work queues.</span></span> <span data-ttu-id="eb990-118">當媒體會話配置新的工作佇列時，它會在內部儲存實際的工作佇列識別碼。</span><span class="sxs-lookup"><span data-stu-id="eb990-118">When the Media Session allocates a new work queue, it stores the actual work-queue identifier internally.</span></span>

 

<span data-ttu-id="eb990-119">如果設定此屬性，則應用程式也可以藉由設定 [ [**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別**](mf-toponode-workqueue-mmcss-class-attribute.md) ] 屬性，將分支指派給多媒體類別排程器服務 (MMCSS) 工作。</span><span class="sxs-lookup"><span data-stu-id="eb990-119">If this attribute it set, the application can also assign the branch to a Multimedia Class Scheduler Service (MMCSS) task, by setting the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute.</span></span>

<span data-ttu-id="eb990-120">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="eb990-120">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb990-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="eb990-121">Requirements</span></span>



| <span data-ttu-id="eb990-122">需求</span><span class="sxs-lookup"><span data-stu-id="eb990-122">Requirement</span></span> | <span data-ttu-id="eb990-123">值</span><span class="sxs-lookup"><span data-stu-id="eb990-123">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="eb990-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="eb990-124">Minimum supported client</span></span><br/> | <span data-ttu-id="eb990-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb990-125">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="eb990-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="eb990-126">Minimum supported server</span></span><br/> | <span data-ttu-id="eb990-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="eb990-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="eb990-128">標頭</span><span class="sxs-lookup"><span data-stu-id="eb990-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="eb990-129"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="eb990-129"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb990-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eb990-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb990-131">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="eb990-131">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="eb990-132">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="eb990-132">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="eb990-133">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="eb990-133">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="eb990-134">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="eb990-134">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="eb990-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="eb990-135">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="eb990-136">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="eb990-136">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)
</dt> <dt>

[<span data-ttu-id="eb990-137">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="eb990-137">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="eb990-138">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="eb990-138">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="eb990-139">工作佇列</span><span class="sxs-lookup"><span data-stu-id="eb990-139">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 




