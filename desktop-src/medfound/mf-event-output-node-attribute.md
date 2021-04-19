---
description: 識別資料流程接收的拓撲節點。
ms.assetid: 9aa6ca66-5122-4d05-94b9-32be194e9eb3
title: 'MF_EVENT_OUTPUT_NODE 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02c484ea55841f4057bf0855dd51b90db951acb6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998266"
---
# <a name="mf_event_output_node-attribute"></a><span data-ttu-id="fe90d-103">MF \_ 事件 \_ 輸出 \_ 節點屬性</span><span class="sxs-lookup"><span data-stu-id="fe90d-103">MF\_EVENT\_OUTPUT\_NODE attribute</span></span>

<span data-ttu-id="fe90d-104">識別資料流程接收的拓撲節點。</span><span class="sxs-lookup"><span data-stu-id="fe90d-104">Identifies the topology node for a stream sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="fe90d-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="fe90d-105">Data type</span></span>

<span data-ttu-id="fe90d-106">**UINT64**</span><span class="sxs-lookup"><span data-stu-id="fe90d-106">**UINT64**</span></span>

<span data-ttu-id="fe90d-107">視為 [**TOPOID**](topoid.md)。</span><span class="sxs-lookup"><span data-stu-id="fe90d-107">Treat as [**TOPOID**](topoid.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="fe90d-108">備註</span><span class="sxs-lookup"><span data-stu-id="fe90d-108">Remarks</span></span>

<span data-ttu-id="fe90d-109">這個屬性的值是目前拓撲上輸出節點的節點識別碼。</span><span class="sxs-lookup"><span data-stu-id="fe90d-109">The value of this attribute is a node identifier for an output node on the current topology.</span></span> <span data-ttu-id="fe90d-110">若要取得相關聯節點的指標，請在拓撲上呼叫 [**IMFTopology：： GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) 。</span><span class="sxs-lookup"><span data-stu-id="fe90d-110">To get a pointer to the associated node, call [**IMFTopology::GetNodeByID**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-getnodebyid) on the topology.</span></span>

<span data-ttu-id="fe90d-111">這個屬性會搭配下列事件使用：</span><span class="sxs-lookup"><span data-stu-id="fe90d-111">This attribute is used with the following events:</span></span>

-   [<span data-ttu-id="fe90d-112">MESessionStreamSinkFormatChanged</span><span class="sxs-lookup"><span data-stu-id="fe90d-112">MESessionStreamSinkFormatChanged</span></span>](mesessionstreamsinkformatchanged.md)
-   [<span data-ttu-id="fe90d-113">MESinkInvalidated</span><span class="sxs-lookup"><span data-stu-id="fe90d-113">MESinkInvalidated</span></span>](mesinkinvalidated.md)

<span data-ttu-id="fe90d-114">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="fe90d-114">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe90d-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="fe90d-115">Requirements</span></span>



| <span data-ttu-id="fe90d-116">需求</span><span class="sxs-lookup"><span data-stu-id="fe90d-116">Requirement</span></span> | <span data-ttu-id="fe90d-117">值</span><span class="sxs-lookup"><span data-stu-id="fe90d-117">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="fe90d-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fe90d-118">Minimum supported client</span></span><br/> | <span data-ttu-id="fe90d-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe90d-119">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="fe90d-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fe90d-120">Minimum supported server</span></span><br/> | <span data-ttu-id="fe90d-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fe90d-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="fe90d-122">標頭</span><span class="sxs-lookup"><span data-stu-id="fe90d-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="fe90d-123"><dt>Mfapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="fe90d-123"><dt>Mfapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe90d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fe90d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe90d-125">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="fe90d-125">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe90d-126">事件屬性</span><span class="sxs-lookup"><span data-stu-id="fe90d-126">Event Attributes</span></span>](event-attributes.md)
</dt> <dt>

[<span data-ttu-id="fe90d-127">**IMFAttributes::GetUINT64**</span><span class="sxs-lookup"><span data-stu-id="fe90d-127">**IMFAttributes::GetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint64)
</dt> <dt>

[<span data-ttu-id="fe90d-128">**IMFAttributes::SetUINT64**</span><span class="sxs-lookup"><span data-stu-id="fe90d-128">**IMFAttributes::SetUINT64**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint64)
</dt> </dl>

 

 




