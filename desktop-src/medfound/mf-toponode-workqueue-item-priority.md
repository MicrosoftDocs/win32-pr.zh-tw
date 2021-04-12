---
description: 指定拓撲分支的工作專案優先順序。
ms.assetid: B2FA1151-08D3-46F9-A38D-AC8908EFA6A2
title: 'MF_TOPONODE_WORKQUEUE_ITEM_PRIORITY 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec5f7df6630e41a32eeb069c2a07b8030da79929
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191626"
---
# <a name="mf_toponode_workqueue_item_priority-attribute"></a><span data-ttu-id="57ce3-103">MF \_ TOPONODE \_ WORKQUEUE \_ 專案 \_ 優先順序屬性</span><span class="sxs-lookup"><span data-stu-id="57ce3-103">MF\_TOPONODE\_WORKQUEUE\_ITEM\_PRIORITY attribute</span></span>

<span data-ttu-id="57ce3-104">指定拓撲分支的工作專案優先順序。</span><span class="sxs-lookup"><span data-stu-id="57ce3-104">Specifies the work-item priority for a branch of the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="57ce3-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="57ce3-105">Data type</span></span>

<span data-ttu-id="57ce3-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="57ce3-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="57ce3-107">備註</span><span class="sxs-lookup"><span data-stu-id="57ce3-107">Remarks</span></span>

<span data-ttu-id="57ce3-108">這個屬性會套用至 (**MF \_ 拓撲 \_ SOURCESTREAM \_ 節點**) 的來源節點。</span><span class="sxs-lookup"><span data-stu-id="57ce3-108">This attribute applies to source nodes (**MF\_TOPOLOGY\_SOURCESTREAM\_NODE**).</span></span> <span data-ttu-id="57ce3-109">屬性是選擇性的。</span><span class="sxs-lookup"><span data-stu-id="57ce3-109">The attribute is optional.</span></span>

<span data-ttu-id="57ce3-110">此屬性需要相同節點上的 [MF \_ TOPONODE \_ WORKQUEUE \_ ID](mf-toponode-workqueue-id-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="57ce3-110">This attribute requires the [MF\_TOPONODE\_WORKQUEUE\_ID](mf-toponode-workqueue-id-attribute.md) attribute on the same node.</span></span>

<span data-ttu-id="57ce3-111">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="57ce3-111">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="57ce3-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="57ce3-112">Requirements</span></span>



| <span data-ttu-id="57ce3-113">需求</span><span class="sxs-lookup"><span data-stu-id="57ce3-113">Requirement</span></span> | <span data-ttu-id="57ce3-114">值</span><span class="sxs-lookup"><span data-stu-id="57ce3-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="57ce3-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="57ce3-115">Minimum supported client</span></span><br/> | <span data-ttu-id="57ce3-116">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57ce3-116">Windows 8 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="57ce3-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="57ce3-117">Minimum supported server</span></span><br/> | <span data-ttu-id="57ce3-118">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="57ce3-118">Windows Server 2012 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="57ce3-119">標頭</span><span class="sxs-lookup"><span data-stu-id="57ce3-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="57ce3-120"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="57ce3-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57ce3-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57ce3-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57ce3-122">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="57ce3-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="57ce3-123">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="57ce3-123">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="57ce3-124">工作佇列和執行緒改進</span><span class="sxs-lookup"><span data-stu-id="57ce3-124">Work Queue and Threading Improvements</span></span>](media-foundation-work-queue-and-threading-improvements.md)
</dt> <dt>

[<span data-ttu-id="57ce3-125">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="57ce3-125">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="57ce3-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span><span class="sxs-lookup"><span data-stu-id="57ce3-126">**IMFWorkQueueServices::BeginRegisterTopologyWorkQueuesWithMMCSS**</span></span>](/windows/desktop/api/mfidl/nf-mfidl-imfworkqueueservices-beginregistertopologyworkqueueswithmmcss)
</dt> <dt>

[<span data-ttu-id="57ce3-127">**MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="57ce3-127">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)
</dt> </dl>

 

 




