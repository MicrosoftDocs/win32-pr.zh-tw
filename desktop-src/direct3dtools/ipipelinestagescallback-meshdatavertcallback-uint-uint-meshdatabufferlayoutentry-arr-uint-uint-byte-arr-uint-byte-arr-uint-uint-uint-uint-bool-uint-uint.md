---
description: 回呼，會通知主機 assocaited 要求所傳回的管線階段網格資訊。
MS-HAID: vspixengine.IPipeLineStagesCallback\_MeshDataVertCallback\_UINT\_UINT\_MeshDataBufferLayoutEntry\_arr\_UINT\_UINT\_BYTE\_arr\_UINT\_BYTE\_arr\_UINT\_UINT\_UINT\_UINT\_BOOL\_UINT\_UINT
MSHAttr:
- PreferredSiteName:MSDN
- PreferredLib:/library/windows/desktop
title: IPipeLineStagesCallback：： MeshDataVertCallback 方法
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: E75EDE35-AC8E-4452-B79B-860C39B156F0
api_name:
- IPipeLineStagesCallback.MeshDataVertCallback
api_type:
- COM
api_location:
- vspixengine.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3c878851b0c3cfe32128d766f4dcb35a7437579d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510008"
---
# <a name="span-idvspixengineipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uintspanipipelinestagescallbackmeshdatavertcallback-method"></a><span data-ttu-id="72e69-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback：： MeshDataVertCallback 方法</span><span class="sxs-lookup"><span data-stu-id="72e69-103"><span id="vspixengine.ipipelinestagescallback_meshdatavertcallback_uint_uint_meshdatabufferlayoutentry_arr_uint_uint_byte_arr_uint_byte_arr_uint_uint_uint_uint_bool_uint_uint"></span>IPipeLineStagesCallback::MeshDataVertCallback method</span></span>

<span data-ttu-id="72e69-104">回呼，會通知主機 assocaited 要求所傳回的管線階段網格資訊。</span><span class="sxs-lookup"><span data-stu-id="72e69-104">A callback that notifies the host of pipeline stages mesh information returned by the assocaited request.</span></span>

## <a name="syntax"></a><span data-ttu-id="72e69-105">語法</span><span class="sxs-lookup"><span data-stu-id="72e69-105">Syntax</span></span>


```C++
HRESULT MeshDataVertCallback(
   UINT                         numVertices,
   UINT                         numBufferLayoutEntries,
   MeshDataBufferLayoutEntry [] count1_entries,
   UINT                         stride,
   UINT                         numVBBytes,
   BYTE []                      count4_pVBData,
   UINT                         numIBBytes,
   BYTE []                      count6_pIBData,
   UINT                         indexSize,
   UINT                         IBOffset,
   UINT                         baseVertex,
   UINT                         minVertex,
   BOOL                         IBIndexesVB,
   UINT                         numIndices,
   UINT                         topology
);
```

## <a name="parameters"></a><span data-ttu-id="72e69-106">參數</span><span class="sxs-lookup"><span data-stu-id="72e69-106">Parameters</span></span>

<span data-ttu-id="72e69-107">*numVertices* </span><span class="sxs-lookup"><span data-stu-id="72e69-107">*numVertices* </span></span>  
<span data-ttu-id="72e69-108">結果中的頂點數目。</span><span class="sxs-lookup"><span data-stu-id="72e69-108">The number of vertices in the results.</span></span>

<span data-ttu-id="72e69-109">*numBufferLayoutEntries* </span><span class="sxs-lookup"><span data-stu-id="72e69-109">*numBufferLayoutEntries* </span></span>  
<span data-ttu-id="72e69-110">結果中的緩衝區版面設定項目數目。</span><span class="sxs-lookup"><span data-stu-id="72e69-110">The number of buffer layout entries in the results.</span></span>

<span data-ttu-id="72e69-111">*count1 \_ 專案* </span><span class="sxs-lookup"><span data-stu-id="72e69-111">*count1\_entries* </span></span>  
<span data-ttu-id="72e69-112">緩衝區版面配置 entires。</span><span class="sxs-lookup"><span data-stu-id="72e69-112">The buffer layout entires.</span></span> <span data-ttu-id="72e69-113">這些描述著色器輸出簽章。</span><span class="sxs-lookup"><span data-stu-id="72e69-113">These describe the shader output signature.</span></span>

<span data-ttu-id="72e69-114">*大步* </span><span class="sxs-lookup"><span data-stu-id="72e69-114">*stride* </span></span>  
<span data-ttu-id="72e69-115">整個輸出區塊 (stride) 的大小。</span><span class="sxs-lookup"><span data-stu-id="72e69-115">The size (stride) of an entire output chunk.</span></span>

<span data-ttu-id="72e69-116">*numVBBytes* </span><span class="sxs-lookup"><span data-stu-id="72e69-116">*numVBBytes* </span></span>  
<span data-ttu-id="72e69-117">頂點緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="72e69-117">The size of the vertex buffer in bytes.</span></span>

<span data-ttu-id="72e69-118">*count4 \_ pVBData* </span><span class="sxs-lookup"><span data-stu-id="72e69-118">*count4\_pVBData* </span></span>  
<span data-ttu-id="72e69-119">頂點緩衝區。</span><span class="sxs-lookup"><span data-stu-id="72e69-119">The vertex buffer.</span></span>

<span data-ttu-id="72e69-120">*numIBBytes* </span><span class="sxs-lookup"><span data-stu-id="72e69-120">*numIBBytes* </span></span>  
<span data-ttu-id="72e69-121">索引緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="72e69-121">The size of the index buffer in bytes.</span></span>

<span data-ttu-id="72e69-122">*count6 \_ pIBData* </span><span class="sxs-lookup"><span data-stu-id="72e69-122">*count6\_pIBData* </span></span>  
<span data-ttu-id="72e69-123">索引緩衝區。</span><span class="sxs-lookup"><span data-stu-id="72e69-123">The index buffer.</span></span>

<span data-ttu-id="72e69-124">*indexSize* </span><span class="sxs-lookup"><span data-stu-id="72e69-124">*indexSize* </span></span>  
<span data-ttu-id="72e69-125">每個索引的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="72e69-125">The size of each index in bytes.</span></span>

<span data-ttu-id="72e69-126">*IBOffset* </span><span class="sxs-lookup"><span data-stu-id="72e69-126">*IBOffset* </span></span>  
<span data-ttu-id="72e69-127">索引緩衝區中的位移，指定要開始使用索引的位置。</span><span class="sxs-lookup"><span data-stu-id="72e69-127">An offset into the index buffer that specifies where indices should start being used.</span></span>

<span data-ttu-id="72e69-128">*baseVertex* </span><span class="sxs-lookup"><span data-stu-id="72e69-128">*baseVertex* </span></span>  
<span data-ttu-id="72e69-129">頂點緩衝區中的位移，指定應該開始使用頂點的位置。</span><span class="sxs-lookup"><span data-stu-id="72e69-129">An offset into the vertex buffer that specifies where vertices should start being used.</span></span>

<span data-ttu-id="72e69-130">*minVertex*</span><span class="sxs-lookup"><span data-stu-id="72e69-130">*minVertex*</span></span>   

<span data-ttu-id="72e69-131">*IBIndexesVB* </span><span class="sxs-lookup"><span data-stu-id="72e69-131">*IBIndexesVB* </span></span>  
<span data-ttu-id="72e69-132">如果使用索引緩衝區，則為 true;否則為 false。</span><span class="sxs-lookup"><span data-stu-id="72e69-132">true when the index buffer is used; otherwise false.</span></span>

<span data-ttu-id="72e69-133">*numIndices* </span><span class="sxs-lookup"><span data-stu-id="72e69-133">*numIndices* </span></span>  
<span data-ttu-id="72e69-134">使用的索引數目。</span><span class="sxs-lookup"><span data-stu-id="72e69-134">The number of indices used.</span></span>

<span data-ttu-id="72e69-135">*拓撲* </span><span class="sxs-lookup"><span data-stu-id="72e69-135">*topology* </span></span>  
<span data-ttu-id="72e69-136">著色器的 topolology。</span><span class="sxs-lookup"><span data-stu-id="72e69-136">The topolology of the shader.</span></span> <span data-ttu-id="72e69-137">這與關聯繪製呼叫的拓撲不一定相同。</span><span class="sxs-lookup"><span data-stu-id="72e69-137">This is not necessarily the same as the topology of the associated draw call.</span></span>

## <a name="return-value"></a><span data-ttu-id="72e69-138">傳回值</span><span class="sxs-lookup"><span data-stu-id="72e69-138">Return value</span></span>

<span data-ttu-id="72e69-139">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="72e69-139">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72e69-140">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="72e69-140">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="72e69-141">規格需求</span><span class="sxs-lookup"><span data-stu-id="72e69-141">Requirements</span></span>

<table><colgroup><col style="width: 50%" /><col style="width: 50%" /></colgroup><tbody><tr class="odd"><td><p><span data-ttu-id="72e69-142">標頭</span><span class="sxs-lookup"><span data-stu-id="72e69-142">Header</span></span></p></td><td><span data-ttu-id="72e69-143">Vspixengine。h</span><span class="sxs-lookup"><span data-stu-id="72e69-143">Vspixengine.h</span></span></td></tr></tbody></table>

## <a name="span-idsee_alsospansee-also"></a><span data-ttu-id="72e69-144"><span id="see_also"></span>另請參閱</span><span class="sxs-lookup"><span data-stu-id="72e69-144"><span id="see_also"></span>See also</span></span>

[<span data-ttu-id="72e69-145">**IPipeLineStagesCallback**</span><span class="sxs-lookup"><span data-stu-id="72e69-145">**IPipeLineStagesCallback**</span></span>](/windows/desktop/direct3dtools/ipipelinestagescallback)

 

 
