---
description: 指定拓撲分支 (MMCSS) 工作的多媒體類別排程器服務。
ms.assetid: 8668d0f1-9d54-4c56-bb19-09498252bec4
title: 'MF_TOPONODE_WORKQUEUE_MMCSS_CLASS 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 824c9dbdc9b12bbc8fead9ab6ae722fca1e6643a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999863"
---
# <a name="mf_toponode_workqueue_mmcss_class-attribute"></a><span data-ttu-id="596c3-103">MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別屬性</span><span class="sxs-lookup"><span data-stu-id="596c3-103">MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS attribute</span></span>

<span data-ttu-id="596c3-104">指定拓撲分支 (MMCSS) 工作的 [多媒體類別](../procthread/multimedia-class-scheduler-service.md) 排程器服務。</span><span class="sxs-lookup"><span data-stu-id="596c3-104">Specifies a [Multimedia Class Scheduler Service](../procthread/multimedia-class-scheduler-service.md) (MMCSS) task for a topology branch.</span></span>

## <a name="data-type"></a><span data-ttu-id="596c3-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="596c3-105">Data type</span></span>

<span data-ttu-id="596c3-106">寬字元字串</span><span class="sxs-lookup"><span data-stu-id="596c3-106">Wide-character string</span></span>

## <a name="remarks"></a><span data-ttu-id="596c3-107">備註</span><span class="sxs-lookup"><span data-stu-id="596c3-107">Remarks</span></span>

<span data-ttu-id="596c3-108">這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。</span><span class="sxs-lookup"><span data-stu-id="596c3-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="596c3-109">此屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="596c3-109">This attribute is optional.</span></span>

<span data-ttu-id="596c3-110">此屬性需要 [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="596c3-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute.</span></span> <span data-ttu-id="596c3-111">如果您設定此屬性，也請在相同的節點上設定 [ **MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼** ] 屬性。</span><span class="sxs-lookup"><span data-stu-id="596c3-111">If you set this attribute, also set the **MF\_TOPONODE\_WORKQUEUE\_ID** attribute is set on the same node.</span></span>

<span data-ttu-id="596c3-112">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="596c3-112">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="596c3-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="596c3-113">Requirements</span></span>



| <span data-ttu-id="596c3-114">需求</span><span class="sxs-lookup"><span data-stu-id="596c3-114">Requirement</span></span> | <span data-ttu-id="596c3-115">值</span><span class="sxs-lookup"><span data-stu-id="596c3-115">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="596c3-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="596c3-116">Minimum supported client</span></span><br/> | <span data-ttu-id="596c3-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="596c3-117">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="596c3-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="596c3-118">Minimum supported server</span></span><br/> | <span data-ttu-id="596c3-119">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="596c3-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="596c3-120">標頭</span><span class="sxs-lookup"><span data-stu-id="596c3-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="596c3-121"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="596c3-121"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="596c3-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="596c3-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="596c3-123">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="596c3-123">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="596c3-124">**IMFAttributes：： GetString**</span><span class="sxs-lookup"><span data-stu-id="596c3-124">**IMFAttributes::GetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getstring)
</dt> <dt>

[<span data-ttu-id="596c3-125">**IMFAttributes：： SetString**</span><span class="sxs-lookup"><span data-stu-id="596c3-125">**IMFAttributes::SetString**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setstring)
</dt> <dt>

[<span data-ttu-id="596c3-126">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="596c3-126">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="596c3-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="596c3-127">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="596c3-128">**MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="596c3-128">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> <dt>

[<span data-ttu-id="596c3-129">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="596c3-129">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)
</dt> <dt>

[<span data-ttu-id="596c3-130">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="596c3-130">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="596c3-131">工作佇列</span><span class="sxs-lookup"><span data-stu-id="596c3-131">Work Queues</span></span>](work-queues.md)
</dt> </dl>

 

 
