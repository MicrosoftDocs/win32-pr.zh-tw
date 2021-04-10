---
title: bufferSize (ChannelPublishingType) 元素
description: 包含配置給會話緩衝區的記憶體數量（以 kb 為單位）。
ms.assetid: 05f38251-648a-48a2-a0f6-bac5ace7f02b
keywords:
- bufferSize 元素 EventLog
topic_type:
- apiref
api_name:
- bufferSize
api_type:
- Schema
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: af609db6fb81417e81b2981ed351dc8b2954371f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025483"
---
# <a name="buffersize-channelpublishingtype-element"></a><span data-ttu-id="02440-104">bufferSize (ChannelPublishingType) 元素</span><span class="sxs-lookup"><span data-stu-id="02440-104">bufferSize (ChannelPublishingType) Element</span></span>

<span data-ttu-id="02440-105">包含配置給會話緩衝區的記憶體數量（以 kb 為單位）。</span><span class="sxs-lookup"><span data-stu-id="02440-105">Contains the amount of memory, in kilobytes, allocated for the session buffers.</span></span>

``` syntax
<xs:element name="bufferSize"
    type="unsignedInt"
 />
```

<span data-ttu-id="02440-106">**BufferSize** 元素是由 [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md)複雜型別定義。</span><span class="sxs-lookup"><span data-stu-id="02440-106">The **bufferSize** element is defined by the [**ChannelPublishingType**](eventmanifestschema-channelpublishingtype-complextype.md) complex type.</span></span>

## <a name="requirements"></a><span data-ttu-id="02440-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="02440-107">Requirements</span></span>



| <span data-ttu-id="02440-108">需求</span><span class="sxs-lookup"><span data-stu-id="02440-108">Requirement</span></span> | <span data-ttu-id="02440-109">值</span><span class="sxs-lookup"><span data-stu-id="02440-109">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="02440-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="02440-110">Minimum supported client</span></span><br/> | <span data-ttu-id="02440-111">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02440-111">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="02440-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="02440-112">Minimum supported server</span></span><br/> | <span data-ttu-id="02440-113">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="02440-113">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="02440-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="02440-114">See also</span></span>

<dl> <dt>

<span data-ttu-id="02440-115">**父元素**</span><span class="sxs-lookup"><span data-stu-id="02440-115">**Parent element**</span></span>
</dt> <dt>

[<span data-ttu-id="02440-116">**發行 (ChannelType)**</span><span class="sxs-lookup"><span data-stu-id="02440-116">**publishing (ChannelType)**</span></span>](eventmanifestschema-publishing-channeltype-element.md)
</dt> </dl>

 

 





