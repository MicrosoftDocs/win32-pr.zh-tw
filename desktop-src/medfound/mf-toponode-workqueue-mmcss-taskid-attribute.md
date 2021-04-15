---
description: 指定 MMCSS 拓撲分支的多媒體類別排程器服務 () 工作識別碼。
ms.assetid: ccecc1e6-2d30-4e89-849f-c3acad97f312
title: 'MF_TOPONODE_WORKQUEUE_MMCSS_TASKID 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53af119c58d725d42ec5737ffd9bf96286a65ac1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512268"
---
# <a name="mf_toponode_workqueue_mmcss_taskid-attribute"></a><span data-ttu-id="bb151-103">MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID 屬性</span><span class="sxs-lookup"><span data-stu-id="bb151-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID attribute</span></span>

<span data-ttu-id="bb151-104">指定 MMCSS 拓撲分支的多媒體類別排程器服務 () 工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb151-104">Specifies a Multimedia Class Scheduler Service (MMCSS) task identifier for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="bb151-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="bb151-105">Data type</span></span>

<span data-ttu-id="bb151-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="bb151-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="bb151-107">備註</span><span class="sxs-lookup"><span data-stu-id="bb151-107">Remarks</span></span>

<span data-ttu-id="bb151-108">這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。</span><span class="sxs-lookup"><span data-stu-id="bb151-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="bb151-109">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="bb151-109">This attribute is optional.</span></span>

<span data-ttu-id="bb151-110">除非也設定了下列屬性，否則會忽略此屬性：</span><span class="sxs-lookup"><span data-stu-id="bb151-110">This attribute is ignored unless the following attributes are also set:</span></span>

-   [<span data-ttu-id="bb151-111">**MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="bb151-111">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
-   [<span data-ttu-id="bb151-112">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="bb151-112">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)

<span data-ttu-id="bb151-113">如果應用程式使用 MMCSS 註冊它自己的其中一個執行緒，您可以使用這個屬性來建立拓撲工作佇列與應用程式 MMCSS 群組的關聯。</span><span class="sxs-lookup"><span data-stu-id="bb151-113">If the application registers one of its own threads with MMCSS, you can use this attribute to associate the topology work queue with the application's MMCSS group.</span></span> <span data-ttu-id="bb151-114">將屬性值設定為等於當應用程式向 MMCSS 註冊時所收到的工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb151-114">Set the attribute value equal to the task identifier that the application received when it registered with MMCSS.</span></span> <span data-ttu-id="bb151-115"> (在 [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa)函數的 *TaskIndex* 參數中傳回工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="bb151-115">(The task identifier is returned in the *TaskIndex* parameter of the [**AvSetMmThreadCharacteristics**](/windows/win32/api/avrt/nf-avrt-avsetmmthreadcharacteristicsa) function.</span></span> <span data-ttu-id="bb151-116">如需詳細資訊，請參閱主題 [進程和執行緒函數](../procthread/process-and-thread-functions.md)。 ) </span><span class="sxs-lookup"><span data-stu-id="bb151-116">For more information, see the topic [Process and Thread Functions](../procthread/process-and-thread-functions.md).)</span></span>

<span data-ttu-id="bb151-117">如果您想要讓 MMCSS 指派拓撲的新工作識別碼，請設定 [**mf \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別**](mf-toponode-workqueue-mmcss-class-attribute.md) 屬性，但不要設定 **mf \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID** 屬性。</span><span class="sxs-lookup"><span data-stu-id="bb151-117">If you want MMCSS to assign a new task identifier for the topology, set the [**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**](mf-toponode-workqueue-mmcss-class-attribute.md) attribute, but do not set the **MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID** attribute.</span></span>

<span data-ttu-id="bb151-118">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="bb151-118">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb151-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb151-119">Requirements</span></span>



| <span data-ttu-id="bb151-120">需求</span><span class="sxs-lookup"><span data-stu-id="bb151-120">Requirement</span></span> | <span data-ttu-id="bb151-121">值</span><span class="sxs-lookup"><span data-stu-id="bb151-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="bb151-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="bb151-122">Minimum supported client</span></span><br/> | <span data-ttu-id="bb151-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb151-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="bb151-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="bb151-124">Minimum supported server</span></span><br/> | <span data-ttu-id="bb151-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="bb151-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="bb151-126">標頭</span><span class="sxs-lookup"><span data-stu-id="bb151-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="bb151-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb151-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bb151-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb151-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb151-129">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="bb151-129">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb151-130">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bb151-130">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="bb151-131">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="bb151-131">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="bb151-132">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="bb151-132">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="bb151-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="bb151-133">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="bb151-134">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="bb151-134">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="bb151-135">工作佇列</span><span class="sxs-lookup"><span data-stu-id="bb151-135">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
