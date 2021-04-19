---
description: 指定網路來源偵測到的封包配對頻寬和執行時間頻寬。
ms.assetid: 430de7fc-fe62-4b89-b3fc-7cd956e40892
title: 'MFNETSOURCE_PPBANDWIDTH 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae0f23f289f68e46bba726a4391023ce9001e2ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979758"
---
# <a name="mfnetsource_ppbandwidth-property"></a><span data-ttu-id="e826c-103">MFNETSOURCE \_ PPBANDWIDTH 屬性</span><span class="sxs-lookup"><span data-stu-id="e826c-103">MFNETSOURCE\_PPBANDWIDTH property</span></span>

<span data-ttu-id="e826c-104">指定網路來源偵測到的封包配對頻寬和執行時間頻寬。</span><span class="sxs-lookup"><span data-stu-id="e826c-104">Specifies the packet-pair bandwidth and run-time bandwidth detected by the network source.</span></span> <span data-ttu-id="e826c-105">屬性值是兩個值的陣列：</span><span class="sxs-lookup"><span data-stu-id="e826c-105">The property value is a array of two values:</span></span>

-   <span data-ttu-id="e826c-106">封包配對頻寬（以每秒位數為單位）。</span><span class="sxs-lookup"><span data-stu-id="e826c-106">Packet-pair bandwidth, in bits per second.</span></span>
-   <span data-ttu-id="e826c-107">執行時間頻寬（以位/秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="e826c-107">Run-time bandwidth, in bits per second.</span></span>



<span data-ttu-id="e826c-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="e826c-108">Data type</span></span>

<span data-ttu-id="e826c-109">PROPVARIANT 類型 (vt) </span><span class="sxs-lookup"><span data-stu-id="e826c-109">PROPVARIANT type (vt)</span></span>

<span data-ttu-id="e826c-110">PROPVARIANT 成員</span><span class="sxs-lookup"><span data-stu-id="e826c-110">PROPVARIANT member</span></span>

<span data-ttu-id="e826c-111">**ULONG** 值的陣列 (**CAUL**) </span><span class="sxs-lookup"><span data-stu-id="e826c-111">Array of **ULONG** values (**CAUL**)</span></span>

<span data-ttu-id="e826c-112">VT \_ 向量 \| vt \_ UI4</span><span class="sxs-lookup"><span data-stu-id="e826c-112">VT\_VECTOR \| VT\_UI4</span></span>

<span data-ttu-id="e826c-113">**科爾**</span><span class="sxs-lookup"><span data-stu-id="e826c-113">**caul**</span></span>



## <a name="remarks"></a><span data-ttu-id="e826c-114">備註</span><span class="sxs-lookup"><span data-stu-id="e826c-114">Remarks</span></span>

<span data-ttu-id="e826c-115">常數 **MFNETSOURCE \_ PPBANDWIDTH** 會定義此屬性索引鍵的 GUID。</span><span class="sxs-lookup"><span data-stu-id="e826c-115">The constant **MFNETSOURCE\_PPBANDWIDTH** defines the GUID for this property key.</span></span> <span data-ttu-id="e826c-116"> (PID) 的屬性識別碼為零。</span><span class="sxs-lookup"><span data-stu-id="e826c-116">The property identifier (PID) is zero.</span></span>

<span data-ttu-id="e826c-117">這是唯讀的屬性。</span><span class="sxs-lookup"><span data-stu-id="e826c-117">This property is read-only.</span></span> <span data-ttu-id="e826c-118">若要取得這個屬性，請查詢 **IPropertyStore** 介面的網路來源，然後呼叫 **IPropertyStore：： GetValue**。</span><span class="sxs-lookup"><span data-stu-id="e826c-118">To retrieve this property, query the network source for the **IPropertyStore** interface and call **IPropertyStore::GetValue**.</span></span>

## <a name="requirements"></a><span data-ttu-id="e826c-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="e826c-119">Requirements</span></span>



| <span data-ttu-id="e826c-120">需求</span><span class="sxs-lookup"><span data-stu-id="e826c-120">Requirement</span></span> | <span data-ttu-id="e826c-121">值</span><span class="sxs-lookup"><span data-stu-id="e826c-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="e826c-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e826c-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e826c-123">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e826c-123">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="e826c-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e826c-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e826c-125">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e826c-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="e826c-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e826c-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e826c-127"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="e826c-127"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e826c-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e826c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e826c-129">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="e826c-129">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> <dt>

[<span data-ttu-id="e826c-130">網路來源功能</span><span class="sxs-lookup"><span data-stu-id="e826c-130">Network Source Features</span></span>](network-source-features.md)
</dt> <dt>

[<span data-ttu-id="e826c-131">媒體基礎中的網路功能</span><span class="sxs-lookup"><span data-stu-id="e826c-131">Networking in Media Foundation</span></span>](networking-in-media-foundation.md)
</dt> </dl>

 

 




