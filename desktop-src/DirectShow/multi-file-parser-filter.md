---
description: 多重檔案剖析器篩選
ms.assetid: 8ef06f49-fda4-49e2-9b07-70453a2e897c
title: 多重檔案剖析器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44fc83a56bb12c307b85be875a3a2e7e73b744d9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972312"
---
# <a name="multi-file-parser-filter"></a><span data-ttu-id="435e5-103">多重檔案剖析器篩選</span><span class="sxs-lookup"><span data-stu-id="435e5-103">Multi-File Parser Filter</span></span>

<span data-ttu-id="435e5-104">多重檔案剖析器篩選器會剖析簡單的檔案格式，讓您可以指定多個檔案名，就好像它們是一個檔案一樣。</span><span class="sxs-lookup"><span data-stu-id="435e5-104">The Multi-File Parser filter parses a simple file format that enables multiple file names to be specified as though they were one file.</span></span> <span data-ttu-id="435e5-105">這些檔案的格式如下範例所示：</span><span class="sxs-lookup"><span data-stu-id="435e5-105">These files have the format shown in the following example:</span></span>


```C++
;MULTI
https://server/share/video.mpg
https://server/share/captions.smi
```



<span data-ttu-id="435e5-106">此篩選器的使用已被取代。</span><span class="sxs-lookup"><span data-stu-id="435e5-106">The use of this filter is deprecated.</span></span> <span data-ttu-id="435e5-107">若要在相同的篩選圖形中轉譯多個檔案，應用程式應該只呼叫 **RenderFile** 或 **AddSourceFilter** 多次。</span><span class="sxs-lookup"><span data-stu-id="435e5-107">To render multiple files within the same filter graph, the application should simply call **RenderFile** or **AddSourceFilter** multiple times.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="435e5-108">篩選介面</span><span class="sxs-lookup"><span data-stu-id="435e5-108">Filter interfaces</span></span></td>
<td><span data-ttu-id="435e5-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="435e5-109"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="435e5-110">輸入 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="435e5-110">Input pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="435e5-111">主要類型： MEDIATYPE_Stream</span><span class="sxs-lookup"><span data-stu-id="435e5-111">Major type: MEDIATYPE_Stream</span></span></li>
<li><span data-ttu-id="435e5-112">子類型： CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="435e5-112">Subtype: CLSID_MultFile</span></span></li>
<li><span data-ttu-id="435e5-113">格式類型： GUID_Null</span><span class="sxs-lookup"><span data-stu-id="435e5-113">Format type: GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="435e5-114">輸入 pin 介面</span><span class="sxs-lookup"><span data-stu-id="435e5-114">Input pin interfaces</span></span></td>
<td><span data-ttu-id="435e5-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="435e5-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="435e5-116">輸出 pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="435e5-116">Output pin media types</span></span></td>
<td><ul>
<li><span data-ttu-id="435e5-117">主要類型： MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="435e5-117">Major type: MEDIATYPE_File</span></span></li>
<li><span data-ttu-id="435e5-118">子類型： GUID_Null</span><span class="sxs-lookup"><span data-stu-id="435e5-118">Subtype: GUID_NULL</span></span></li>
<li><span data-ttu-id="435e5-119">格式類型： MEDIATYPE_File</span><span class="sxs-lookup"><span data-stu-id="435e5-119">Format type: MEDIATYPE_File</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="435e5-120">輸出 pin 介面</span><span class="sxs-lookup"><span data-stu-id="435e5-120">Output pin interfaces</span></span></td>
<td><span data-ttu-id="435e5-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="435e5-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="435e5-122">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="435e5-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="435e5-123">CLSID_MultFile</span><span class="sxs-lookup"><span data-stu-id="435e5-123">CLSID_MultFile</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="435e5-124">可執行檔</span><span class="sxs-lookup"><span data-stu-id="435e5-124">Executable</span></span></td>
<td><span data-ttu-id="435e5-125">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="435e5-125">Quartz.dll</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="435e5-126"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="435e5-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="435e5-127">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="435e5-127">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="435e5-128"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="435e5-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="435e5-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="435e5-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="435e5-130">備註</span><span class="sxs-lookup"><span data-stu-id="435e5-130">Remarks</span></span>

<span data-ttu-id="435e5-131">此篩選會針對原始程式檔中所列的每個檔案建立一個輸出圖釘。</span><span class="sxs-lookup"><span data-stu-id="435e5-131">The filter creates one output pin for each file listed in the source file.</span></span> <span data-ttu-id="435e5-132">輸出類型為「媒體類型」 \_ ，而輸出類型的格式區塊是包含檔案名的寬字元字串。</span><span class="sxs-lookup"><span data-stu-id="435e5-132">The output type is MEDIATYPE\_File, and the format block for the output type is a wide-character string that contains the file name.</span></span> <span data-ttu-id="435e5-133">每個釘選都會連接到檔案 [資料流程](file-stream-renderer-filter.md) 轉譯器篩選準則的實例。</span><span class="sxs-lookup"><span data-stu-id="435e5-133">Each pin connects to an instance of the [File Stream Renderer](file-stream-renderer-filter.md) filter.</span></span> <span data-ttu-id="435e5-134">檔案資料流程轉譯器篩選器會建立一個輸出圖釘，以公開 [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) 介面。</span><span class="sxs-lookup"><span data-stu-id="435e5-134">The File Stream Renderer filter creates one output pin, which exposes the [**IStreamBuilder**](/windows/desktop/api/Strmif/nn-strmif-istreambuilder) interface.</span></span> <span data-ttu-id="435e5-135">輸出圖釘會轉譯指定的檔案。</span><span class="sxs-lookup"><span data-stu-id="435e5-135">The output pin renders the specified file.</span></span> <span data-ttu-id="435e5-136">在多檔案剖析器和檔案資料流程轉譯器之間，不會有媒體資料的移動。</span><span class="sxs-lookup"><span data-stu-id="435e5-136">No media data travels between the Multi-File Parser and the File Stream Renderer.</span></span>

<span data-ttu-id="435e5-137">篩選的 CLSID 未定義于 Uuid. h 中。</span><span class="sxs-lookup"><span data-stu-id="435e5-137">The filter's CLSID is not defined in Uuids.h.</span></span> <span data-ttu-id="435e5-138">在您自己的標頭檔中使用此宏：</span><span class="sxs-lookup"><span data-stu-id="435e5-138">Use this macro in your own header file:</span></span>


```C++
// {D51BD5A3-7548-11cf-A520-0080C77EF58A}
DEFINE_GUID(CLSID_MultFile,
0xd51bd5a3, 0x7548, 0x11cf, 0xa5, 0x20, 0x0, 0x80, 0xc7, 0x7e, 0xf5, 0x8a);
```



## <a name="related-topics"></a><span data-ttu-id="435e5-139">相關主題</span><span class="sxs-lookup"><span data-stu-id="435e5-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="435e5-140">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="435e5-140">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



