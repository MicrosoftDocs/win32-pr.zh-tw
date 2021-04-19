---
description: 指定媒體會話如何關閉拓撲中的物件。
ms.assetid: 53b4faba-860f-4d6c-a145-09ea4ae63b8b
title: 'MF_TOPONODE_NOSHUTDOWN_ON_REMOVE 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6bec06d2190491167d978250270503e5e6506d58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106993000"
---
# <a name="mf_toponode_noshutdown_on_remove-attribute"></a><span data-ttu-id="c9293-103">\_ \_ \_ 移除屬性上的 MF TOPONODE NOSHUTDOWN \_</span><span class="sxs-lookup"><span data-stu-id="c9293-103">MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE attribute</span></span>

<span data-ttu-id="c9293-104">指定媒體會話如何關閉拓撲中的物件。</span><span class="sxs-lookup"><span data-stu-id="c9293-104">Specifies how the Media Session shuts down an object in the topology.</span></span>

## <a name="data-type"></a><span data-ttu-id="c9293-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="c9293-105">Data type</span></span>

<span data-ttu-id="c9293-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="c9293-106">**UINT32**</span></span>

<span data-ttu-id="c9293-107">視為布林值。</span><span class="sxs-lookup"><span data-stu-id="c9293-107">Treat as a Boolean value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c9293-108">備註</span><span class="sxs-lookup"><span data-stu-id="c9293-108">Remarks</span></span>

<span data-ttu-id="c9293-109">這個屬性會套用至下列類型的拓撲節點：</span><span class="sxs-lookup"><span data-stu-id="c9293-109">This attribute applies to the following types of toplogy node:</span></span>

-   <span data-ttu-id="c9293-110">輸出節點</span><span class="sxs-lookup"><span data-stu-id="c9293-110">Output nodes</span></span>
-   <span data-ttu-id="c9293-111">任何包含 *非同步* 媒體基礎轉換 (MFT) 的轉換節點。</span><span class="sxs-lookup"><span data-stu-id="c9293-111">Any transform node that contains an *asynchronous* Media Foundation transform (MFT).</span></span>

<span data-ttu-id="c9293-112">屬性可以具有下列值：</span><span class="sxs-lookup"><span data-stu-id="c9293-112">The attribute can have the following values:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c9293-113">值</span><span class="sxs-lookup"><span data-stu-id="c9293-113">Value</span></span></th>
<th><span data-ttu-id="c9293-114">描述</span><span class="sxs-lookup"><span data-stu-id="c9293-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="c9293-115"><strong>TRUE</strong></span><span class="sxs-lookup"><span data-stu-id="c9293-115"><strong>TRUE</strong></span></span></td>
<td><span data-ttu-id="c9293-116">當媒體會話切換至新拓撲或清除目前的拓撲時，不會關閉屬於此拓撲節點的物件。</span><span class="sxs-lookup"><span data-stu-id="c9293-116">When the Media Session switches to a new topology or clears the current topology, it does not shut down the object that belongs to this topology node.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="c9293-117"><strong>FALSE</strong></span><span class="sxs-lookup"><span data-stu-id="c9293-117"><strong>FALSE</strong></span></span></td>
<td><span data-ttu-id="c9293-118">當媒體會話切換至新拓撲或清除目前的拓撲時，它會關閉節點物件，如下所示：</span><span class="sxs-lookup"><span data-stu-id="c9293-118">When the Media Session switches to a new topology or clears the current topology, it shuts down the node object, as follows:</span></span>
<ul>
<li><span data-ttu-id="c9293-119">輸出節點：會話會呼叫媒體接收器上的 <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink：： Shutdown</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="c9293-119">Output nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasink-shutdown"><strong>IMFMediaSink::Shutdown</strong></a> on the media sink.</span></span></li>
<li><span data-ttu-id="c9293-120">轉換節點：會話會呼叫 MFT 上的 <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown：： Shutdown</strong></a> 。</span><span class="sxs-lookup"><span data-stu-id="c9293-120">Transform nodes: The session calls <a href="/windows/desktop/api/mfidl/nf-mfidl-imfshutdown-shutdown"><strong>IMFShutdown::Shutdown</strong></a> on the MFT.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="c9293-121">預設值為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c9293-121">The default value is **TRUE**.</span></span>

<span data-ttu-id="c9293-122">如果您的應用程式將多個拓撲排入佇列，最好將此屬性設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="c9293-122">If your application queues multiple topologies, it is a good idea to set this attribute to **FALSE**.</span></span> <span data-ttu-id="c9293-123">否則，拓撲中的物件可能無法正確地關閉。</span><span class="sxs-lookup"><span data-stu-id="c9293-123">Otherwise, objects in the topology might not be shut down correctly.</span></span>

<span data-ttu-id="c9293-124">當應用程式透過呼叫 [**IMFMediaSession：： Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown)關閉媒體會話時，不會套用此屬性。</span><span class="sxs-lookup"><span data-stu-id="c9293-124">This attribute does not apply when the application shuts down the Media Session by calling [**IMFMediaSession::Shutdown**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-shutdown).</span></span> <span data-ttu-id="c9293-125">當媒體會話關閉時，它一律會關閉目前拓撲中的媒體接收器和非同步 MFTs。</span><span class="sxs-lookup"><span data-stu-id="c9293-125">When the Media Session shuts down, it always shuts down the media sinks and asynchronous MFTs in the current topology.</span></span>

<span data-ttu-id="c9293-126">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="c9293-126">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9293-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="c9293-127">Requirements</span></span>



| <span data-ttu-id="c9293-128">需求</span><span class="sxs-lookup"><span data-stu-id="c9293-128">Requirement</span></span> | <span data-ttu-id="c9293-129">值</span><span class="sxs-lookup"><span data-stu-id="c9293-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="c9293-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c9293-130">Minimum supported client</span></span><br/> | <span data-ttu-id="c9293-131">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9293-131">Windows Vista \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="c9293-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c9293-132">Minimum supported server</span></span><br/> | <span data-ttu-id="c9293-133">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c9293-133">Windows Server 2008 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="c9293-134">標頭</span><span class="sxs-lookup"><span data-stu-id="c9293-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="c9293-135"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="c9293-135"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9293-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c9293-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9293-137">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="c9293-137">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9293-138">非同步 MFTs</span><span class="sxs-lookup"><span data-stu-id="c9293-138">Asynchronous MFTs</span></span>](asynchronous-mfts.md)
</dt> <dt>

[<span data-ttu-id="c9293-139">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="c9293-139">Topology Node Attributes</span></span>](topology-node-attributes.md)
</dt> <dt>

[<span data-ttu-id="c9293-140">**IMFAttributes：： GetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c9293-140">**IMFAttributes::GetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)
</dt> <dt>

[<span data-ttu-id="c9293-141">**IMFAttributes：： SetUINT32**</span><span class="sxs-lookup"><span data-stu-id="c9293-141">**IMFAttributes::SetUINT32**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)
</dt> <dt>

[<span data-ttu-id="c9293-142">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="c9293-142">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 




