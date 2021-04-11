---
description: 拓撲節點屬性
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: 拓撲節點屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943865"
---
# <a name="topology-node-attributes"></a><span data-ttu-id="bc83d-103">拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-103">Topology Node Attributes</span></span>

<span data-ttu-id="bc83d-104">下列屬性適用于拓撲節點。</span><span class="sxs-lookup"><span data-stu-id="bc83d-104">The following attributes apply to topology nodes.</span></span>

## <a name="general-topology-node-attributes"></a><span data-ttu-id="bc83d-105">一般拓撲節點屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-105">General Topology Node Attributes</span></span>



| <span data-ttu-id="bc83d-106">屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-106">Attribute</span></span>                                                                       | <span data-ttu-id="bc83d-107">描述</span><span class="sxs-lookup"><span data-stu-id="bc83d-107">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc83d-108">**MF \_ TOPONODE \_ CONNECT \_ 方法**</span><span class="sxs-lookup"><span data-stu-id="bc83d-108">**MF\_TOPONODE\_CONNECT\_METHOD**</span></span>](mf-toponode-connect-method-attribute.md)   | <span data-ttu-id="bc83d-109">指定拓撲載入器如何連接此拓撲節點，以及此節點是否為選擇性節點。</span><span class="sxs-lookup"><span data-stu-id="bc83d-109">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>                                                        |
| [<span data-ttu-id="bc83d-110">**MF \_ TOPONODE \_ 解碼器**</span><span class="sxs-lookup"><span data-stu-id="bc83d-110">**MF\_TOPONODE\_DECODER**</span></span>](mf-toponode-decoder-attribute.md)                  | <span data-ttu-id="bc83d-111">指定拓撲節點的物件是否為解碼器。</span><span class="sxs-lookup"><span data-stu-id="bc83d-111">Specifies whether a toplogy node's object is a decoder.</span></span>                                                                                                  |
| [<span data-ttu-id="bc83d-112">**MF \_ TOPONODE \_ 解密器**</span><span class="sxs-lookup"><span data-stu-id="bc83d-112">**MF\_TOPONODE\_DECRYPTOR**</span></span>](mf-toponode-decryptor-attribute.md)              | <span data-ttu-id="bc83d-113">指定拓撲節點的基礎物件是否為解密程式。</span><span class="sxs-lookup"><span data-stu-id="bc83d-113">Specifies whether a toplogy node's underlying object is a decryptor.</span></span>                                                                                     |
| [<span data-ttu-id="bc83d-114">**MF \_ TOPONODE \_ DISCARDABLE**</span><span class="sxs-lookup"><span data-stu-id="bc83d-114">**MF\_TOPONODE\_DISCARDABLE**</span></span>](mf-toponode-discardable-attribute.md)          | <span data-ttu-id="bc83d-115">指定管線是否可以從拓撲節點卸載範例。</span><span class="sxs-lookup"><span data-stu-id="bc83d-115">Specifies whether the pipeline can drop samples from a topology node.</span></span>                                                                                    |
| [<span data-ttu-id="bc83d-116">**MF \_ TOPONODE \_ 錯誤 \_ MAJORTYPE**</span><span class="sxs-lookup"><span data-stu-id="bc83d-116">**MF\_TOPONODE\_ERROR\_MAJORTYPE**</span></span>](mf-toponode-error-majortype-attribute.md) | <span data-ttu-id="bc83d-117">包含拓撲節點的主要媒體類型。</span><span class="sxs-lookup"><span data-stu-id="bc83d-117">Contains the major media type for a topology node.</span></span> <span data-ttu-id="bc83d-118">因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="bc83d-118">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span> |
| [<span data-ttu-id="bc83d-119">**MF \_ TOPONODE \_ 錯誤 \_ 子類型**</span><span class="sxs-lookup"><span data-stu-id="bc83d-119">**MF\_TOPONODE\_ERROR\_SUBTYPE**</span></span>](mf-toponode-error-subtype-attribute.md)     | <span data-ttu-id="bc83d-120">包含拓撲節點的媒體子類型。</span><span class="sxs-lookup"><span data-stu-id="bc83d-120">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="bc83d-121">因為找不到正確的解碼器，所以拓撲無法載入時，就會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="bc83d-121">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>    |
| [<span data-ttu-id="bc83d-122">**MF \_ TOPONODE \_ ERRORCODE**</span><span class="sxs-lookup"><span data-stu-id="bc83d-122">**MF\_TOPONODE\_ERRORCODE**</span></span>](mf-toponode-errorcode-attribute.md)              | <span data-ttu-id="bc83d-123">包含此拓撲節點最近連接失敗的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="bc83d-123">Contains the error code from the most recent connection failure for this topology node.</span></span>                                                                  |
| [<span data-ttu-id="bc83d-124">**已 \_ 鎖定 MF TOPONODE \_**</span><span class="sxs-lookup"><span data-stu-id="bc83d-124">**MF\_TOPONODE\_LOCKED**</span></span>](mf-toponode-locked-attribute.md)                    | <span data-ttu-id="bc83d-125">指定是否可在此拓撲節點上變更媒體類型。</span><span class="sxs-lookup"><span data-stu-id="bc83d-125">Specifies whether the media types can be changed on this topology node.</span></span>                                                                                  |
| [<span data-ttu-id="bc83d-126">**MF \_ TOPONODE \_ MARKIN \_ 這裡**</span><span class="sxs-lookup"><span data-stu-id="bc83d-126">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)         | <span data-ttu-id="bc83d-127">指定管線是否在此節點套用標記。</span><span class="sxs-lookup"><span data-stu-id="bc83d-127">Specifies whether the pipeline applies mark-in at this node.</span></span>                                                                                             |
| [<span data-ttu-id="bc83d-128">**MF \_ TOPONODE \_ MARKOUT \_ 這裡**</span><span class="sxs-lookup"><span data-stu-id="bc83d-128">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)       | <span data-ttu-id="bc83d-129">指定管線是否在此節點套用標記。</span><span class="sxs-lookup"><span data-stu-id="bc83d-129">Specifies whether the pipeline applies mark-out at this node.</span></span>                                                                                            |



 

## <a name="source-node-attributes"></a><span data-ttu-id="bc83d-130">來源節點屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-130">Source Node Attributes</span></span>



| <span data-ttu-id="bc83d-131">屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-131">Attribute</span></span>                                                                                       | <span data-ttu-id="bc83d-132">描述</span><span class="sxs-lookup"><span data-stu-id="bc83d-132">Description</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc83d-133">**MF \_ TOPONODE \_ MEDIASTART**</span><span class="sxs-lookup"><span data-stu-id="bc83d-133">**MF\_TOPONODE\_MEDIASTART**</span></span>](mf-toponode-mediastart-attribute.md)                            | <span data-ttu-id="bc83d-134">指定簡報的開始時間（相對於啟動媒體來源檔案），以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="bc83d-134">Specifies the start time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="bc83d-135">**MF \_ TOPONODE \_ MEDIASTOP**</span><span class="sxs-lookup"><span data-stu-id="bc83d-135">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)                              | <span data-ttu-id="bc83d-136">指定簡報的停止時間，相對於啟動媒體來源檔案，以 100-毫微秒單位表示。</span><span class="sxs-lookup"><span data-stu-id="bc83d-136">Specifies the stop time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span>  |
| [<span data-ttu-id="bc83d-137">**MF \_ TOPONODE \_ 展示 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="bc83d-137">**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**</span></span>](mf-toponode-presentation-descriptor-attribute.md) | <span data-ttu-id="bc83d-138">包含媒體來源之展示描述項的指標。</span><span class="sxs-lookup"><span data-stu-id="bc83d-138">Contains a pointer to the presentation descriptor for the media source.</span></span>                                           |
| [<span data-ttu-id="bc83d-139">**MF \_ TOPONODE \_ 序列 \_ ELEMENTID**</span><span class="sxs-lookup"><span data-stu-id="bc83d-139">**MF\_TOPONODE\_SEQUENCE\_ELEMENTID**</span></span>](mf-toponode-sequence-elementid-attribute.md)           | <span data-ttu-id="bc83d-140">指定包含來源節點的元素。</span><span class="sxs-lookup"><span data-stu-id="bc83d-140">Specifies the element that contains a source node.</span></span>                                                                |
| [<span data-ttu-id="bc83d-141">**MF \_ TOPONODE \_ 來源**</span><span class="sxs-lookup"><span data-stu-id="bc83d-141">**MF\_TOPONODE\_SOURCE**</span></span>](mf-toponode-source-attribute.md)                                    | <span data-ttu-id="bc83d-142">包含與拓撲節點相關聯之媒體來源的指標。</span><span class="sxs-lookup"><span data-stu-id="bc83d-142">Contains a pointer to the media source associated with a topology node.</span></span>                                           |
| [<span data-ttu-id="bc83d-143">**MF \_ TOPONODE \_ 串流 \_ 描述項**</span><span class="sxs-lookup"><span data-stu-id="bc83d-143">**MF\_TOPONODE\_STREAM\_DESCRIPTOR**</span></span>](mf-toponode-stream-descriptor-attribute.md)             | <span data-ttu-id="bc83d-144">包含媒體來源的資料流程描述元指標。</span><span class="sxs-lookup"><span data-stu-id="bc83d-144">Contains a pointer to the stream descriptor for the media source.</span></span>                                                 |
| [<span data-ttu-id="bc83d-145">**MF \_ TOPONODE \_ WORKQUEUE \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="bc83d-145">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)                       | <span data-ttu-id="bc83d-146">指定拓撲節點的工作佇列。</span><span class="sxs-lookup"><span data-stu-id="bc83d-146">Specifies a work queue for a topology node.</span></span>                                                                       |
| [<span data-ttu-id="bc83d-147">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ 類別**</span><span class="sxs-lookup"><span data-stu-id="bc83d-147">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)    | <span data-ttu-id="bc83d-148">指定 MMCSS 拓撲節點的多媒體類別排程器服務 () 工作。</span><span class="sxs-lookup"><span data-stu-id="bc83d-148">Specifies a Multimedia Class Scheduler Service (MMCSS) task for a topology node.</span></span>                                  |
| [<span data-ttu-id="bc83d-149">**MF \_ TOPONODE \_ WORKQUEUE \_ MMCSS \_ TASKID**</span><span class="sxs-lookup"><span data-stu-id="bc83d-149">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | <span data-ttu-id="bc83d-150">指定拓撲節點的 MMCSS 工作識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc83d-150">Specifies a MMCSS task identifier for a topology node.</span></span>                                                            |



 

## <a name="transform-node-attributes"></a><span data-ttu-id="bc83d-151">轉換節點屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-151">Transform Node Attributes</span></span>



| <span data-ttu-id="bc83d-152">屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-152">Attribute</span></span>                                                                             | <span data-ttu-id="bc83d-153">描述</span><span class="sxs-lookup"><span data-stu-id="bc83d-153">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc83d-154">**MF \_ TOPONODE \_ D3DAWARE**</span><span class="sxs-lookup"><span data-stu-id="bc83d-154">**MF\_TOPONODE\_D3DAWARE**</span></span>](mf-toponode-d3daware-attribute.md)                      | <span data-ttu-id="bc83d-155">指定與拓撲節點相關聯的轉換是否支援 (DXVA 的 DirectX Video 加速) </span><span class="sxs-lookup"><span data-stu-id="bc83d-155">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA)</span></span> |
| [<span data-ttu-id="bc83d-156">**MF \_ TOPONODE \_ 清空**</span><span class="sxs-lookup"><span data-stu-id="bc83d-156">**MF\_TOPONODE\_DRAIN**</span></span>](mf-toponode-drain-attribute.md)                            | <span data-ttu-id="bc83d-157">指定何時清空轉換。</span><span class="sxs-lookup"><span data-stu-id="bc83d-157">Specifies when a transform is drained.</span></span>                                                                     |
| [<span data-ttu-id="bc83d-158">**MF \_ TOPONODE \_ FLUSH**</span><span class="sxs-lookup"><span data-stu-id="bc83d-158">**MF\_TOPONODE\_FLUSH**</span></span>](mf-toponode-flush-attribute.md)                            | <span data-ttu-id="bc83d-159">指定何時清除轉換。</span><span class="sxs-lookup"><span data-stu-id="bc83d-159">Specifies when a transform is flushed.</span></span>                                                                     |
| [<span data-ttu-id="bc83d-160">**MF \_ TOPONODE \_ 轉換 \_ OBJECTID**</span><span class="sxs-lookup"><span data-stu-id="bc83d-160">**MF\_TOPONODE\_TRANSFORM\_OBJECTID**</span></span>](mf-toponode-transform-objectid-attribute.md) | <span data-ttu-id="bc83d-161">類別識別碼 (與此拓撲節點相關聯之轉換的 CLSID) 。</span><span class="sxs-lookup"><span data-stu-id="bc83d-161">The class identifier (CLSID) of the transform associated with this topology node.</span></span>                          |



 

## <a name="output-node-attributes"></a><span data-ttu-id="bc83d-162">輸出節點屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-162">Output Node Attributes</span></span>



| <span data-ttu-id="bc83d-163">屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-163">Attribute</span></span>                                                                                  | <span data-ttu-id="bc83d-164">描述</span><span class="sxs-lookup"><span data-stu-id="bc83d-164">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="bc83d-165">**MF \_ TOPONODE \_ 停用預先進行 \_**</span><span class="sxs-lookup"><span data-stu-id="bc83d-165">**MF\_TOPONODE\_DISABLE\_PREROLL**</span></span>](mf-toponode-disable-preroll-attribute.md)            | <span data-ttu-id="bc83d-166">指定媒體會話是否在此拓撲節點所代表的媒體接收器上使用預先進行。</span><span class="sxs-lookup"><span data-stu-id="bc83d-166">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>            |
| [<span data-ttu-id="bc83d-167">**\_ \_ \_ 移除時的 MF TOPONODE NOSHUTDOWN \_**</span><span class="sxs-lookup"><span data-stu-id="bc83d-167">**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**</span></span>](mf-toponode-noshutdown-on-remove-attribute.md) | <span data-ttu-id="bc83d-168">指定當輸出節點從拓撲中移除時，媒體會話是否會關閉媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="bc83d-168">Specifies whether the Media Session shuts down the media sink when the output node is removed from the topology.</span></span> |
| [<span data-ttu-id="bc83d-169">**MF \_ TOPONODE \_ RATELESS**</span><span class="sxs-lookup"><span data-stu-id="bc83d-169">**MF\_TOPONODE\_RATELESS**</span></span>](mf-toponode-rateless-attribute.md)                           | <span data-ttu-id="bc83d-170">指定與此拓撲節點相關聯的媒體接收器是否 rateless。</span><span class="sxs-lookup"><span data-stu-id="bc83d-170">Specifies whether the media sink associated with this topology node is rateless.</span></span>                                 |
| [<span data-ttu-id="bc83d-171">**MF \_ TOPONODE \_ STREAMID**</span><span class="sxs-lookup"><span data-stu-id="bc83d-171">**MF\_TOPONODE\_STREAMID**</span></span>](mf-toponode-streamid-attribute.md)                           | <span data-ttu-id="bc83d-172">與此拓撲節點相關聯之資料流程接收的資料流程識別碼。</span><span class="sxs-lookup"><span data-stu-id="bc83d-172">The stream identifier of the stream sink associated with this topology node.</span></span>                                     |



 

## <a name="tee-node-attributes"></a><span data-ttu-id="bc83d-173">T 節點屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-173">Tee Node Attributes</span></span>



| <span data-ttu-id="bc83d-174">屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-174">Attribute</span></span>                                                                  | <span data-ttu-id="bc83d-175">描述</span><span class="sxs-lookup"><span data-stu-id="bc83d-175">Description</span></span>                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="bc83d-176">**MF \_ TOPONODE \_ PRIMARYOUTPUT**</span><span class="sxs-lookup"><span data-stu-id="bc83d-176">**MF\_TOPONODE\_PRIMARYOUTPUT**</span></span>](mf-toponode-primaryoutput-attribute.md) | <span data-ttu-id="bc83d-177">指出哪些輸出是 t 節點上的主要輸出。</span><span class="sxs-lookup"><span data-stu-id="bc83d-177">Indicates which output is the primary output on a tee node.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="bc83d-178">相關主題</span><span class="sxs-lookup"><span data-stu-id="bc83d-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bc83d-179">**IMFTopologyNode**</span><span class="sxs-lookup"><span data-stu-id="bc83d-179">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="bc83d-180">媒體基礎屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-180">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="bc83d-181">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="bc83d-181">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 



