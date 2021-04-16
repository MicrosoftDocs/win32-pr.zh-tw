---
title: ChannelPublishingType) 元素的延遲 (
description: 清除緩衝區之前等候的時間（以毫秒為單位）。
ms.assetid: 7ca6a0f8-3d4c-41e8-a998-0e34d2df4a2f
keywords:
- 延遲元素 EventLog
topic_type:
- apiref
api_name:
- latency
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d48a98f2f319ec08d2fc1325728f798c5ec96e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508284"
---
# <a name="latency-channelpublishingtype-element"></a><span data-ttu-id="ff730-104">ChannelPublishingType) 元素的延遲 (</span><span class="sxs-lookup"><span data-stu-id="ff730-104">latency (ChannelPublishingType) Element</span></span>

<span data-ttu-id="ff730-105">清除緩衝區之前等候的時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ff730-105">The time to wait before flushing the buffers, in milliseconds.</span></span>

``` syntax
<xs:element name="latency"
    type="unsignedInt"
 />
```

<span data-ttu-id="ff730-106">**延遲** 元素是由 [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="ff730-106">The **latency** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="ff730-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff730-107">Requirements</span></span>



| <span data-ttu-id="ff730-108">需求</span><span class="sxs-lookup"><span data-stu-id="ff730-108">Requirement</span></span> | <span data-ttu-id="ff730-109">值</span><span class="sxs-lookup"><span data-stu-id="ff730-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="ff730-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff730-110">Minimum supported client</span></span><br/> | <span data-ttu-id="ff730-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff730-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="ff730-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff730-112">Minimum supported server</span></span><br/> | <span data-ttu-id="ff730-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff730-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ff730-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff730-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="ff730-115">**父元素**</span><span class="sxs-lookup"><span data-stu-id="ff730-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="ff730-116">**發行 (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="ff730-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





