---
description: 識別查詢類型。
ms.assetid: 575c4e71-3cab-4123-a2a5-d23b53e87111
title: 'D3DQUERYTYPE 列舉 (D3D9Types) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DQUERYTYPE
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 0778e879a6147c185964808ee4b4c302bd211ef3
ms.sourcegitcommit: bfab92e16614d4fa54b044917358261232bda81a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/08/2021
ms.locfileid: "113489692"
---
# <a name="d3dquerytype-enumeration"></a><span data-ttu-id="d93e8-103">D3DQUERYTYPE 列舉</span><span class="sxs-lookup"><span data-stu-id="d93e8-103">D3DQUERYTYPE enumeration</span></span>

<span data-ttu-id="d93e8-104">識別查詢類型。</span><span class="sxs-lookup"><span data-stu-id="d93e8-104">Identifies the query type.</span></span> <span data-ttu-id="d93e8-105">如需查詢的詳細資訊，請參閱 [ (Direct3D 9 的查詢) ](queries.md)</span><span class="sxs-lookup"><span data-stu-id="d93e8-105">For information about queries, see [Queries (Direct3D 9)](queries.md)</span></span>

## <a name="syntax"></a><span data-ttu-id="d93e8-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d93e8-106">Syntax</span></span>


```C++
typedef enum D3DQUERYTYPE { 
  D3DQUERYTYPE_VCACHE             = 4,
  D3DQUERYTYPE_RESOURCEMANAGER    = 5,
  D3DQUERYTYPE_VERTEXSTATS        = 6,
  D3DQUERYTYPE_EVENT              = 8,
  D3DQUERYTYPE_OCCLUSION          = 9,
  D3DQUERYTYPE_TIMESTAMP          = 10,
  D3DQUERYTYPE_TIMESTAMPDISJOINT  = 11,
  D3DQUERYTYPE_TIMESTAMPFREQ      = 12,
  D3DQUERYTYPE_PIPELINETIMINGS    = 13,
  D3DQUERYTYPE_INTERFACETIMINGS   = 14,
  D3DQUERYTYPE_VERTEXTIMINGS      = 15,
  D3DQUERYTYPE_PIXELTIMINGS       = 16,
  D3DQUERYTYPE_BANDWIDTHTIMINGS   = 17,
  D3DQUERYTYPE_CACHEUTILIZATION   = 18,
  D3DQUERYTYPE_MEMORYPRESSURE     = 19
} D3DQUERYTYPE, *LPD3DQUERYTYPE;
```



## <a name="constants"></a><span data-ttu-id="d93e8-107">常數</span><span class="sxs-lookup"><span data-stu-id="d93e8-107">Constants</span></span>

<dl> <dt>

<span data-ttu-id="d93e8-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE \_ VCACHE**</span><span class="sxs-lookup"><span data-stu-id="d93e8-108"><span id="D3DQUERYTYPE_VCACHE"></span><span id="d3dquerytype_vcache"></span>**D3DQUERYTYPE\_VCACHE**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-109">查詢有關頂點快取之資料配置的驅動程式提示。</span><span class="sxs-lookup"><span data-stu-id="d93e8-109">Query for driver hints about data layout for vertex caching.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE \_ ResourceManager**</span><span class="sxs-lookup"><span data-stu-id="d93e8-110"><span id="D3DQUERYTYPE_ResourceManager"></span><span id="d3dquerytype_resourcemanager"></span><span id="D3DQUERYTYPE_RESOURCEMANAGER"></span>**D3DQUERYTYPE\_ResourceManager**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-111">查詢資源管理員。</span><span class="sxs-lookup"><span data-stu-id="d93e8-111">Query the resource manager.</span></span> <span data-ttu-id="d93e8-112">針對此查詢，裝置行為旗標必須包含 [D3DCREATE \_ 停用 \_ 驅動程式 \_ 管理](d3dcreate.md)。</span><span class="sxs-lookup"><span data-stu-id="d93e8-112">For this query, the device behavior flags must include [D3DCREATE\_DISABLE\_DRIVER\_MANAGEMENT](d3dcreate.md).</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE \_ VERTEXSTATS**</span><span class="sxs-lookup"><span data-stu-id="d93e8-113"><span id="D3DQUERYTYPE_VERTEXSTATS"></span><span id="d3dquerytype_vertexstats"></span>**D3DQUERYTYPE\_VERTEXSTATS**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-114">查詢頂點統計資料。</span><span class="sxs-lookup"><span data-stu-id="d93e8-114">Query vertex statistics.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="d93e8-115"><span id="D3DQUERYTYPE_EVENT"></span><span id="d3dquerytype_event"></span>**D3DQUERYTYPE\_EVENT**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-116">查詢從 API 呼叫發出的任何和所有非同步事件。</span><span class="sxs-lookup"><span data-stu-id="d93e8-116">Query for any and all asynchronous events that have been issued from API calls.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE \_ 遮蔽**</span><span class="sxs-lookup"><span data-stu-id="d93e8-117"><span id="D3DQUERYTYPE_OCCLUSION"></span><span id="d3dquerytype_occlusion"></span>**D3DQUERYTYPE\_OCCLUSION**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-118">遮蔽查詢會傳回通過 z 測試的圖元數。</span><span class="sxs-lookup"><span data-stu-id="d93e8-118">An occlusion query returns the number of pixels that pass z-testing.</span></span> <span data-ttu-id="d93e8-119">這些圖元適用于 [**D3DISSUE \_ BEGIN**](d3dissue-begin.md) 和 [**D3DISSUE \_ END**](d3dissue-end.md)問題之間繪製的基本專案。</span><span class="sxs-lookup"><span data-stu-id="d93e8-119">These pixels are for primitives drawn between the issue of [**D3DISSUE\_BEGIN**](d3dissue-begin.md) and [**D3DISSUE\_END**](d3dissue-end.md).</span></span> <span data-ttu-id="d93e8-120">這可讓應用程式針對0檢查遮蔽結果。</span><span class="sxs-lookup"><span data-stu-id="d93e8-120">This enables an application to check the occlusion result against 0.</span></span> <span data-ttu-id="d93e8-121">零是完全 pixels occluded 的，這表示目前相機位置看不到圖元。</span><span class="sxs-lookup"><span data-stu-id="d93e8-121">Zero is fully occluded, which means the pixels are not visible from the current camera position.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE \_ 時間戳記**</span><span class="sxs-lookup"><span data-stu-id="d93e8-122"><span id="D3DQUERYTYPE_TIMESTAMP"></span><span id="d3dquerytype_timestamp"></span>**D3DQUERYTYPE\_TIMESTAMP**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-123">傳回64位的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="d93e8-123">Returns a 64-bit timestamp.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE \_ TIMESTAMPDISJOINT**</span><span class="sxs-lookup"><span data-stu-id="d93e8-124"><span id="D3DQUERYTYPE_TIMESTAMPDISJOINT"></span><span id="d3dquerytype_timestampdisjoint"></span>**D3DQUERYTYPE\_TIMESTAMPDISJOINT**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-125">如果計數器頻率已從 D3DQUERYTYPE 時間戳記變更，請使用此查詢來通知應用程式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="d93e8-125">Use this query to notify an application if the counter frequency has changed from the D3DQUERYTYPE\_TIMESTAMP.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE \_ TIMESTAMPFREQ**</span><span class="sxs-lookup"><span data-stu-id="d93e8-126"><span id="D3DQUERYTYPE_TIMESTAMPFREQ"></span><span id="d3dquerytype_timestampfreq"></span>**D3DQUERYTYPE\_TIMESTAMPFREQ**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-127">如果 D3DQUERYTYPE 時間戳記查詢中的值在 \_ D3DQUERYTYPE TIMESTAMPDISJOINT 查詢的整個持續期間無法保證是連續的，則此查詢結果為 TRUE \_ 。</span><span class="sxs-lookup"><span data-stu-id="d93e8-127">This query result is **TRUE** if the values from D3DQUERYTYPE\_TIMESTAMP queries cannot be guaranteed to be continuous throughout the duration of the D3DQUERYTYPE\_TIMESTAMPDISJOINT query.</span></span> <span data-ttu-id="d93e8-128">否則，查詢結果會是 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="d93e8-128">Otherwise, the query result is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE \_ PIPELINETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="d93e8-129"><span id="D3DQUERYTYPE_PIPELINETIMINGS"></span><span id="d3dquerytype_pipelinetimings"></span>**D3DQUERYTYPE\_PIPELINETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-130">處理管線資料的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="d93e8-130">Percent of time processing pipeline data.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE \_ INTERFACETIMINGS**</span><span class="sxs-lookup"><span data-stu-id="d93e8-131"><span id="D3DQUERYTYPE_INTERFACETIMINGS"></span><span id="d3dquerytype_interfacetimings"></span>**D3DQUERYTYPE\_INTERFACETIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-132">驅動程式中處理資料的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="d93e8-132">Percent of time processing data in the driver.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE \_ VERTEXTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="d93e8-133"><span id="D3DQUERYTYPE_VERTEXTIMINGS"></span><span id="d3dquerytype_vertextimings"></span>**D3DQUERYTYPE\_VERTEXTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-134">處理頂點著色器資料的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="d93e8-134">Percent of time processing vertex shader data.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE \_ PIXELTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="d93e8-135"><span id="D3DQUERYTYPE_PIXELTIMINGS"></span><span id="d3dquerytype_pixeltimings"></span>**D3DQUERYTYPE\_PIXELTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-136">處理圖元著色器資料的時間百分比。</span><span class="sxs-lookup"><span data-stu-id="d93e8-136">Percent of time processing pixel shader data.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE \_ BANDWIDTHTIMINGS**</span><span class="sxs-lookup"><span data-stu-id="d93e8-137"><span id="D3DQUERYTYPE_BANDWIDTHTIMINGS"></span><span id="d3dquerytype_bandwidthtimings"></span>**D3DQUERYTYPE\_BANDWIDTHTIMINGS**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-138">協助您瞭解應用程式效能的輸送量度量比較。</span><span class="sxs-lookup"><span data-stu-id="d93e8-138">Throughput measurement comparisons for help in understanding the performance of an application.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE \_ CACHEUTILIZATION**</span><span class="sxs-lookup"><span data-stu-id="d93e8-139"><span id="D3DQUERYTYPE_CACHEUTILIZATION"></span><span id="d3dquerytype_cacheutilization"></span>**D3DQUERYTYPE\_CACHEUTILIZATION**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-140">測量紋理和索引頂點的快取點擊率效能。</span><span class="sxs-lookup"><span data-stu-id="d93e8-140">Measure the cache hit-rate performance for textures and indexed vertices.</span></span>

</dd> <dt>

<span data-ttu-id="d93e8-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE \_ MEMORYPRESSURE**</span><span class="sxs-lookup"><span data-stu-id="d93e8-141"><span id="D3DQUERYTYPE_MEMORYPRESSURE"></span><span id="d3dquerytype_memorypressure"></span>**D3DQUERYTYPE\_MEMORYPRESSURE**</span></span>
</dt> <dd>

<span data-ttu-id="d93e8-142">包含在 [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) 結構中的記憶體配置效率。</span><span class="sxs-lookup"><span data-stu-id="d93e8-142">Efficiency of memory allocation contained in a [**D3DMEMORYPRESSURE**](d3dmemorypressure.md) structure.</span></span>

<span data-ttu-id="d93e8-143">Direct3D 9 與 Direct3D 9Ex 之間的差異：</span><span class="sxs-lookup"><span data-stu-id="d93e8-143">Differences between Direct3D 9 and Direct3D 9Ex:</span></span>

- <span data-ttu-id="d93e8-144">D3DQUERYTYPE \_ MEMORYPRESSURE 僅適用于 Windows 7 (或更多目前作業系統) 上執行的 Direct3D9Ex。</span><span class="sxs-lookup"><span data-stu-id="d93e8-144">D3DQUERYTYPE\_MEMORYPRESSURE is only available in Direct3D9Ex running on Windows 7 (or more current operating system).</span></span>



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d93e8-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="d93e8-145">Requirements</span></span>



| <span data-ttu-id="d93e8-146">需求</span><span class="sxs-lookup"><span data-stu-id="d93e8-146">Requirement</span></span> | <span data-ttu-id="d93e8-147">值</span><span class="sxs-lookup"><span data-stu-id="d93e8-147">Value</span></span> |
|-------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d93e8-148">標頭</span><span class="sxs-lookup"><span data-stu-id="d93e8-148">Header</span></span><br/> | <dl> <span data-ttu-id="d93e8-149"><dt>D3D9Types。h</dt></span><span class="sxs-lookup"><span data-stu-id="d93e8-149"><dt>D3D9Types.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d93e8-150">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d93e8-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d93e8-151">Direct3D 列舉</span><span class="sxs-lookup"><span data-stu-id="d93e8-151">Direct3D Enumerations</span></span>](dx9-graphics-reference-d3d-enums.md)
</dt> <dt>

[<span data-ttu-id="d93e8-152">**IDirect3DDevice9：： CreateQuery**</span><span class="sxs-lookup"><span data-stu-id="d93e8-152">**IDirect3DDevice9::CreateQuery**</span></span>](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createquery)
</dt> </dl>

 

 
