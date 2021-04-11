---
description: 當網路來源使用 UDP 傳輸時，加速資料流程的最長持續時間（以毫秒為單位）。
ms.assetid: d5f3064a-b222-4f72-b889-cd88c14a239c
title: 'MFNETSOURCE_MAXUDPACCELERATEDSTREAMINGDURATION 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2621e01203ba81b54e565f86953df64304c9bd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027425"
---
# <a name="mfnetsource_maxudpacceleratedstreamingduration-property"></a><span data-ttu-id="ad4a6-103">MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION 屬性</span><span class="sxs-lookup"><span data-stu-id="ad4a6-103">MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION property</span></span>

<span data-ttu-id="ad4a6-104">當網路來源使用 UDP 傳輸時，加速資料流程的最長持續時間（以毫秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="ad4a6-104">Maximum duration of accelerated streaming, in milliseconds, when the network source uses UDP transport.</span></span>



<span data-ttu-id="ad4a6-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="ad4a6-105">Data type</span></span>

<span data-ttu-id="ad4a6-106">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="ad4a6-106">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="ad4a6-107">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="ad4a6-107">PROPVARIANT member</span></span>

<span data-ttu-id="ad4a6-108">**DWORD** (儲存為 **LONG**) </span><span class="sxs-lookup"><span data-stu-id="ad4a6-108">**DWORD** (stored as **LONG**)</span></span>

<span data-ttu-id="ad4a6-109">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="ad4a6-109">VT\_I4</span></span>

<span data-ttu-id="ad4a6-110">**lVal**</span><span class="sxs-lookup"><span data-stu-id="ad4a6-110">**lVal**</span></span>



## <a name="remarks"></a><span data-ttu-id="ad4a6-111">備註</span><span class="sxs-lookup"><span data-stu-id="ad4a6-111">Remarks</span></span>

<span data-ttu-id="ad4a6-112">常數 **MFNETSOURCE \_ MAXUDPACCELERATEDSTREAMINGDURATION** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="ad4a6-112">The constant **MFNETSOURCE\_MAXUDPACCELERATEDSTREAMINGDURATION** defines the GUID for this property key.</span></span> <span data-ttu-id="ad4a6-113"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="ad4a6-113">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="ad4a6-114">若是 UDP 傳輸，如果這個屬性的值較低，這個屬性會覆寫 [**MFNETSOURCE \_ ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="ad4a6-114">For UDP transport, this property overrides the [**MFNETSOURCE\_ACCELERATEDSTREAMINGDURATION**](mfnetsource-acceleratedstreamingduration-property.md) property if the value of this property is lower.</span></span>

<span data-ttu-id="ad4a6-115">應用程式可以使用這個屬性來設定網路來源。</span><span class="sxs-lookup"><span data-stu-id="ad4a6-115">Applications can use this property to configure the network source.</span></span> <span data-ttu-id="ad4a6-116">若要設定屬性，請將 **IPropertyStore** 指標傳遞至來源解析程式。</span><span class="sxs-lookup"><span data-stu-id="ad4a6-116">To set the property, pass an **IPropertyStore** pointer to the source resolver.</span></span> <span data-ttu-id="ad4a6-117">如需詳細資訊，請參閱設定 [媒體來源](configuring-a-media-source.md)。</span><span class="sxs-lookup"><span data-stu-id="ad4a6-117">For more information, see [Configuring a Media Source](configuring-a-media-source.md).</span></span>

<span data-ttu-id="ad4a6-118">這個屬性的預設值為8000毫秒。</span><span class="sxs-lookup"><span data-stu-id="ad4a6-118">The default value of this property is 8,000 milliseconds.</span></span>

## <a name="requirements"></a><span data-ttu-id="ad4a6-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad4a6-119">Requirements</span></span>



| <span data-ttu-id="ad4a6-120">需求</span><span class="sxs-lookup"><span data-stu-id="ad4a6-120">Requirement</span></span> | <span data-ttu-id="ad4a6-121">值</span><span class="sxs-lookup"><span data-stu-id="ad4a6-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="ad4a6-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad4a6-122">Minimum supported client</span></span><br/> | <span data-ttu-id="ad4a6-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad4a6-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="ad4a6-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad4a6-124">Minimum supported server</span></span><br/> | <span data-ttu-id="ad4a6-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ad4a6-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="ad4a6-126">標頭</span><span class="sxs-lookup"><span data-stu-id="ad4a6-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad4a6-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="ad4a6-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ad4a6-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad4a6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad4a6-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="ad4a6-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="ad4a6-130">網路來源功能</span><span class="sxs-lookup"><span data-stu-id="ad4a6-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="ad4a6-131">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="ad4a6-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




