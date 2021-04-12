---
description: 指定拓撲載入器是否列舉媒體來源所提供的媒體類型。
ms.assetid: 2675ef16-2018-47e8-bb22-2fc0d62e6681
title: 'MF_TOPOLOGY_ENUMERATE_SOURCE_TYPES 屬性 (Mfidl) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015042bbf9994f81058c621239224196e6ec9ac8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318300"
---
# <a name="mf_topology_enumerate_source_types-attribute"></a><span data-ttu-id="97eca-103">MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型屬性</span><span class="sxs-lookup"><span data-stu-id="97eca-103">MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute</span></span>

<span data-ttu-id="97eca-104">指定拓撲載入器是否列舉媒體來源所提供的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="97eca-104">Specifies whether the topology loader enumerates the media types provided by the media source.</span></span>

## <a name="data-type"></a><span data-ttu-id="97eca-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="97eca-105">Data type</span></span>

<span data-ttu-id="97eca-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="97eca-106">**UINT32**</span></span>

<span data-ttu-id="97eca-107">使用下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="97eca-107">Use one of the following values.</span></span>



| <span data-ttu-id="97eca-108">值</span><span class="sxs-lookup"><span data-stu-id="97eca-108">Value</span></span>                                                                                                                                    | <span data-ttu-id="97eca-109">意義</span><span class="sxs-lookup"><span data-stu-id="97eca-109">Meaning</span></span>                                             |
|------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="FALSE"></span><span id="false"></span><dl> <span data-ttu-id="97eca-110"><dt>FALSE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="97eca-110"><dt>\*\*\*\*FALSE\*\*\*\*</dt></span></span> </dl> | <span data-ttu-id="97eca-111">請勿列舉來源媒體類型。</span><span class="sxs-lookup"><span data-stu-id="97eca-111">Do not enumerate the source media types.</span></span><br/> |
| <span id="TRUE"></span><span id="true"></span><dl> <span data-ttu-id="97eca-112"><dt>TRUE \* \* \* \*</dt></span><span class="sxs-lookup"><span data-stu-id="97eca-112"><dt>\*\*\*\*TRUE\*\*\*\*</dt></span></span> </dl>    | <span data-ttu-id="97eca-113">列舉來源媒體類型。</span><span class="sxs-lookup"><span data-stu-id="97eca-113">Enumerate the source media types.</span></span><br/>        |



 

## <a name="getset"></a><span data-ttu-id="97eca-114">取得/設定</span><span class="sxs-lookup"><span data-stu-id="97eca-114">Get/set</span></span>

<span data-ttu-id="97eca-115">若要取得這個屬性，請呼叫 [**IMFAttributes：： GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32)。</span><span class="sxs-lookup"><span data-stu-id="97eca-115">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="97eca-116">若要設定這個屬性，請呼叫 [**IMFAttributes：： SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32)。</span><span class="sxs-lookup"><span data-stu-id="97eca-116">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="applies-to"></a><span data-ttu-id="97eca-117">適用於</span><span class="sxs-lookup"><span data-stu-id="97eca-117">Applies to</span></span>

[<span data-ttu-id="97eca-118">**IMFTopology**</span><span class="sxs-lookup"><span data-stu-id="97eca-118">**IMFTopology**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopology)

## <a name="remarks"></a><span data-ttu-id="97eca-119">備註</span><span class="sxs-lookup"><span data-stu-id="97eca-119">Remarks</span></span>

<span data-ttu-id="97eca-120">媒體來源上的每個串流都可以提供一種以上的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="97eca-120">Each stream on a media source can offer more than one media type.</span></span> <span data-ttu-id="97eca-121">類型清單是透過資料流程描述項上的 [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) 介面來列舉。</span><span class="sxs-lookup"><span data-stu-id="97eca-121">The list of types is enumerated through the [**IMFMediaTypeHandler**](/windows/desktop/api/mfidl/nn-mfidl-imfmediatypehandler) interface on the stream descriptor.</span></span>

<span data-ttu-id="97eca-122">拓撲載入器嘗試媒體來源媒體類型的順序是由兩個屬性所控制：</span><span class="sxs-lookup"><span data-stu-id="97eca-122">The order in which the topology loader tries a media source's media types is controlled by two attributes:</span></span>

-   <span data-ttu-id="97eca-123">MF \_ 拓撲 \_ 列舉 \_ 拓撲上的來源 \_ 類型屬性。</span><span class="sxs-lookup"><span data-stu-id="97eca-123">The MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute on the topology.</span></span>
-   <span data-ttu-id="97eca-124">來源節點上的 [**MF \_ TOPONODE \_ CONNECT \_ METHOD**](mf-toponode-connect-method-attribute.md) 屬性。</span><span class="sxs-lookup"><span data-stu-id="97eca-124">The [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node.</span></span>

<span data-ttu-id="97eca-125">如果 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型屬性為 **FALSE** 或未設定，拓撲載入器會使用資料流程目前的媒體類型。</span><span class="sxs-lookup"><span data-stu-id="97eca-125">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **FALSE** or not set, the topology loader uses the stream's current media type.</span></span> <span data-ttu-id="97eca-126">它不會列舉可能類型的清單。</span><span class="sxs-lookup"><span data-stu-id="97eca-126">It does not enumerate the list of possible types.</span></span> <span data-ttu-id="97eca-127">如果目前的媒體類型與下游拓撲節點不相容，而且找不到任何的解碼器/轉換器組合，拓撲解析就會失敗。</span><span class="sxs-lookup"><span data-stu-id="97eca-127">If the current media type is incompatible with the downstream topology node, and no combination of decoders/converters can be found, topology resolution fails.</span></span>

<span data-ttu-id="97eca-128">如果 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型屬性為 **TRUE**，拓撲載入器會列舉來源的媒體類型，直到找到相容的類型。</span><span class="sxs-lookup"><span data-stu-id="97eca-128">If the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute is **TRUE**, the topology loader enumerates the source's media types until it finds a compatible type.</span></span> <span data-ttu-id="97eca-129">在此情況下，作業的確切順序取決於來源節點上的 [**mf \_ TOPONODE \_ CONNECT \_ METHOD**](mf-toponode-connect-method-attribute.md) 屬性是否包含 **mf \_ connect \_ 解析 \_ 獨立 \_ OUTPUTTYPES** 旗標。</span><span class="sxs-lookup"><span data-stu-id="97eca-129">In that case, the exact order of operations depends on the whether the [**MF\_TOPONODE\_CONNECT\_METHOD**](mf-toponode-connect-method-attribute.md) attribute on the source node includes the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span>

<span data-ttu-id="97eca-130">如果 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型為 **TRUE** ，且已設定 **mf \_ CONNECT \_ 解析 \_ 獨立 \_ OUTPUTTYPES** 旗標，拓撲載入器會在移至下一個媒體類型之前耗盡每個媒體類型，如下所示：</span><span class="sxs-lookup"><span data-stu-id="97eca-130">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** and the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set, the topology loader exhausts each media type before moving to the next, as follows:</span></span>

``` syntax
foreach media type T
    connect directly using T
    if failed, connect with converters using T
    if failed, connect with decoders using T
```

<span data-ttu-id="97eca-131">如果 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型為 **TRUE** ，但未設定 **mf \_ CONNECT \_ 解析 \_ 獨立 \_ OUTPUTTYPES** ，拓撲載入器會嘗試與每個媒體類型的直接連線，然後使用轉換器來嘗試每個媒體類型，最後嘗試每個媒體類型使用以下的解碼器：</span><span class="sxs-lookup"><span data-stu-id="97eca-131">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **TRUE** but **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** is not set, the topology loader tries a direct connection with each media type, then tries each media type with converters, and finally tries each media type with decoders:</span></span>

``` syntax
foreach media type T
    connect directly using T
if failed,
    foreach media type T
        connect with converters using T
if failed
    foreach media type T
        connect with decoders using T
```

<span data-ttu-id="97eca-132">如果 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型為 **FALSE**，則會忽略 **mf \_ CONNECT \_ 解析 \_ 獨立 \_ OUTPUTTYPES** 旗標。</span><span class="sxs-lookup"><span data-stu-id="97eca-132">If MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is ignored.</span></span>

<span data-ttu-id="97eca-133">基於 \_ \_ \_ \_ 與現有應用程式的相容性，MF 拓撲列舉來源類型的預設值為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="97eca-133">The default value of MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES is **FALSE**, for compatibility with existing applications.</span></span>

<span data-ttu-id="97eca-134">這個屬性的 GUID 常數是從 mfuuid 匯出。</span><span class="sxs-lookup"><span data-stu-id="97eca-134">The GUID constant for this attribute is exported from mfuuid.lib.</span></span>

### <a name="example"></a><span data-ttu-id="97eca-135">範例</span><span class="sxs-lookup"><span data-stu-id="97eca-135">Example</span></span>

<span data-ttu-id="97eca-136">以下是說明 **MF \_ CONNECT \_ 解析 \_ 獨立 \_ OUTPUTTYPES** 旗標的範例。</span><span class="sxs-lookup"><span data-stu-id="97eca-136">Here is an example that illustrates the **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag.</span></span> <span data-ttu-id="97eca-137">假設拓撲的 MF \_ 拓撲 \_ 列舉 \_ 來源 \_ 類型屬性設為 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="97eca-137">Assume the topology has the MF\_TOPOLOGY\_ENUMERATE\_SOURCE\_TYPES attribute set to **TRUE**.</span></span>

<span data-ttu-id="97eca-138">媒體來源提供下列類型：</span><span class="sxs-lookup"><span data-stu-id="97eca-138">The media source offers the following types:</span></span>

-   <span data-ttu-id="97eca-139">T1、T2、T3</span><span class="sxs-lookup"><span data-stu-id="97eca-139">T1, T2, T3</span></span>

<span data-ttu-id="97eca-140">媒體接收接受下列類型：</span><span class="sxs-lookup"><span data-stu-id="97eca-140">The media sink accepts the following types:</span></span>

-   <span data-ttu-id="97eca-141">T3，T4</span><span class="sxs-lookup"><span data-stu-id="97eca-141">T3, T4</span></span>

<span data-ttu-id="97eca-142">案例1：已設定 **MF \_ CONNECT \_ 解析 \_ 獨立 \_ OUTPUTTYPES** 旗標。</span><span class="sxs-lookup"><span data-stu-id="97eca-142">Case 1: The **MF\_CONNECT\_RESOLVE\_INDEPENDENT\_OUTPUTTYPES** flag is set.</span></span>

1.  <span data-ttu-id="97eca-143">拓撲載入器會嘗試與 T1 的直接連接。</span><span class="sxs-lookup"><span data-stu-id="97eca-143">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="97eca-144">接收會拒絕 T1。</span><span class="sxs-lookup"><span data-stu-id="97eca-144">The sink rejects T1.</span></span>
2.  <span data-ttu-id="97eca-145">拓撲載入器會插入接受 T1 和輸出 T4 的解碼器。</span><span class="sxs-lookup"><span data-stu-id="97eca-145">The topology loader inserts a decoder that accepts T1 and outputs T4.</span></span> <span data-ttu-id="97eca-146">接收會接受 T4。</span><span class="sxs-lookup"><span data-stu-id="97eca-146">The sink accepts T4.</span></span>
3.  <span data-ttu-id="97eca-147">最終拓撲包含：媒體來源→解碼器→媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="97eca-147">The final topology contains: media source → decoder → media sink.</span></span>

<span data-ttu-id="97eca-148">案例2：未設定旗標。</span><span class="sxs-lookup"><span data-stu-id="97eca-148">Case 2: The flag is not set.</span></span>

1.  <span data-ttu-id="97eca-149">拓撲載入器會嘗試與 T1 的直接連接。</span><span class="sxs-lookup"><span data-stu-id="97eca-149">The topology loader tries a direct connection with T1.</span></span> <span data-ttu-id="97eca-150">接收會拒絕 T1。</span><span class="sxs-lookup"><span data-stu-id="97eca-150">The sink rejects T1.</span></span>
2.  <span data-ttu-id="97eca-151">拓撲載入器會嘗試與 T2 的直接連接。</span><span class="sxs-lookup"><span data-stu-id="97eca-151">The topology loader tries a direct connection with T2.</span></span> <span data-ttu-id="97eca-152">接收會拒絕 T2。</span><span class="sxs-lookup"><span data-stu-id="97eca-152">The sink rejects T2.</span></span>
3.  <span data-ttu-id="97eca-153">拓撲載入器會嘗試與 T3 的直接連接。</span><span class="sxs-lookup"><span data-stu-id="97eca-153">The topology loader tries a direct connection with T3.</span></span> <span data-ttu-id="97eca-154">接收會接受 T3。</span><span class="sxs-lookup"><span data-stu-id="97eca-154">The sink accepts T3.</span></span>
4.  <span data-ttu-id="97eca-155">最終拓撲包含：媒體來源→媒體接收器。</span><span class="sxs-lookup"><span data-stu-id="97eca-155">The final topology contains: media source → media sink.</span></span>

## <a name="requirements"></a><span data-ttu-id="97eca-156">規格需求</span><span class="sxs-lookup"><span data-stu-id="97eca-156">Requirements</span></span>



| <span data-ttu-id="97eca-157">需求</span><span class="sxs-lookup"><span data-stu-id="97eca-157">Requirement</span></span> | <span data-ttu-id="97eca-158">值</span><span class="sxs-lookup"><span data-stu-id="97eca-158">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="97eca-159">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="97eca-159">Minimum supported client</span></span><br/> | <span data-ttu-id="97eca-160">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97eca-160">Windows 7 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="97eca-161">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="97eca-161">Minimum supported server</span></span><br/> | <span data-ttu-id="97eca-162">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="97eca-162">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="97eca-163">標頭</span><span class="sxs-lookup"><span data-stu-id="97eca-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="97eca-164"><dt>Mfidl。h</dt></span><span class="sxs-lookup"><span data-stu-id="97eca-164"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="97eca-165">另請參閱</span><span class="sxs-lookup"><span data-stu-id="97eca-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="97eca-166">依字母順序排列的媒體基礎屬性清單</span><span class="sxs-lookup"><span data-stu-id="97eca-166">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="97eca-167">拓撲屬性</span><span class="sxs-lookup"><span data-stu-id="97eca-167">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 




