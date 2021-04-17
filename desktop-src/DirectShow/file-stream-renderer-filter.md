---
description: 檔案資料流程轉譯器篩選
ms.assetid: e26462bb-e67f-4522-bec2-88378c4ff442
title: 檔案資料流程轉譯器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a64c8d8a0c87dab3aa811c8246be24ded8ee04dc
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510240"
---
# <a name="file-stream-renderer-filter"></a><span data-ttu-id="cf459-103">檔案資料流程轉譯器篩選</span><span class="sxs-lookup"><span data-stu-id="cf459-103">File Stream Renderer Filter</span></span>

<span data-ttu-id="cf459-104">檔案資料流程轉譯器篩選器會轉譯由 [多](multi-file-parser-filter.md) 檔案剖析器篩選器剖析的檔案名。</span><span class="sxs-lookup"><span data-stu-id="cf459-104">The File Stream Renderer filter renders file names that are parsed by the [Multi-File Parser](multi-file-parser-filter.md) filter.</span></span> <span data-ttu-id="cf459-105">如需詳細資訊，請參閱該篩選器的檔。</span><span class="sxs-lookup"><span data-stu-id="cf459-105">For more information, see the documentation for that filter.</span></span>

<span data-ttu-id="cf459-106">此篩選器的使用已被取代。</span><span class="sxs-lookup"><span data-stu-id="cf459-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="cf459-107">若要在相同的篩選圖形中轉譯多個檔案，應用程式應該只呼叫 **RenderFile** 或 **AddSourceFilter** 多次。</span><span class="sxs-lookup"><span data-stu-id="cf459-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf459-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="cf459-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="cf459-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf459-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf459-110">輸入 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="cf459-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="cf459-111">主要類型： MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="cf459-111">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="cf459-112">子類型： GUID_Null</span><span class="sxs-lookup"><span data-stu-id="cf459-112">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="cf459-113">格式類型： MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="cf459-113">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf459-114">輸入 pin 介面</span><span class="sxs-lookup"><span data-stu-id="cf459-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="cf459-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf459-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf459-116">輸出 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="cf459-116">Output pin media types</span></span></td>
<td><span data-ttu-id="cf459-117">無</span><span class="sxs-lookup"><span data-stu-id="cf459-117">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf459-118">輸出 pin 介面</span><span class="sxs-lookup"><span data-stu-id="cf459-118">Output pin interfaces</span></span></td>
<td><span data-ttu-id="cf459-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf459-119"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-istreambuilder"><strong>IStreamBuilder</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf459-120">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="cf459-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="cf459-121">CLSID_FileRend</span><span class="sxs-lookup"><span data-stu-id="cf459-121">CLSID_FileRend</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf459-122">可執行檔</span><span class="sxs-lookup"><span data-stu-id="cf459-122">Executable</span></span></td>
<td><span data-ttu-id="cf459-123">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="cf459-123">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf459-124"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="cf459-124"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="cf459-125">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="cf459-125">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf459-126"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="cf459-126"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="cf459-127">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="cf459-127">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="cf459-128">備註</span><span class="sxs-lookup"><span data-stu-id="cf459-128">Remarks</span></span>

<span data-ttu-id="cf459-129">篩選的 CLSID 未定義于 Uuid. h 中。</span><span class="sxs-lookup"><span data-stu-id="cf459-129">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="cf459-130">在您自己的標頭檔中使用此宏：</span><span class="sxs-lookup"><span data-stu-id="cf459-130">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A5-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_FileRend,
0xd51bd5A5, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="cf459-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="cf459-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf459-132">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="cf459-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



