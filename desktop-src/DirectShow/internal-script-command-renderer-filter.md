---
description: 內部指令碼命令轉譯器篩選
ms.assetid: 264cc7c3-987c-4832-85a2-087278a4d024
title: 內部指令碼命令轉譯器篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b241643d991e9348015dc51ea5b2f1c4875f079d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104510060"
---
# <a name="internal-script-command-renderer-filter"></a><span data-ttu-id="f16c8-103">內部指令碼命令轉譯器篩選</span><span class="sxs-lookup"><span data-stu-id="f16c8-103">Internal Script Command Renderer Filter</span></span>

<span data-ttu-id="f16c8-104">接收指令碼命令，並將它們分派至應用程式。</span><span class="sxs-lookup"><span data-stu-id="f16c8-104">Receives script commands and dispatches them to the application.</span></span>

<span data-ttu-id="f16c8-105">此篩選器會以下列兩種格式之一接受指令碼命令：</span><span class="sxs-lookup"><span data-stu-id="f16c8-105">This filter accepts script commands in one of two formats:</span></span>

-   <span data-ttu-id="f16c8-106">媒體 \_ 型文字：每個媒體範例都包含一個 ANSI 文字字串。</span><span class="sxs-lookup"><span data-stu-id="f16c8-106">MEDIATYPE\_Text: Each media sample contains an ANSI text string.</span></span>
-   <span data-ttu-id="f16c8-107">媒體 \_ 型 ScriptCommand：每個媒體範例都包含兩個以 Null 終止的 Unicode 字串，串連在一起。</span><span class="sxs-lookup"><span data-stu-id="f16c8-107">MEDIATYPE\_ScriptCommand: Each media sample contains two NULL-terminated Unicode strings, concatenated together.</span></span> <span data-ttu-id="f16c8-108">第一個字串描述命令類型，而第二個字串則是指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="f16c8-108">The first string describes the command type and the second string is the script command.</span></span>

    <span data-ttu-id="f16c8-109">當篩選準則收到範例時，它會傳送 [**EC \_ OLE \_ 事件**](ec-ole-event.md) 事件通知。</span><span class="sxs-lookup"><span data-stu-id="f16c8-109">When the filter receives a sample, it sends an [**EC\_OLE\_EVENT**](ec-ole-event.md) event notification.</span></span> <span data-ttu-id="f16c8-110">第一個事件參數是具有命令類型的 **BSTR** ，或 `Text` 如果格式為媒體文字，則為 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f16c8-110">The first event parameter is a **BSTR** with the command type, or `Text` if the format is MEDIATYPE\_Text.</span></span> <span data-ttu-id="f16c8-111">第二個事件參數是具有指令碼命令的 **BSTR** 。</span><span class="sxs-lookup"><span data-stu-id="f16c8-111">The second event parameter is a **BSTR** with the script command.</span></span> <span data-ttu-id="f16c8-112">應用程式可以取出事件並回應指令碼命令。</span><span class="sxs-lookup"><span data-stu-id="f16c8-112">The application can retrieve the event and respond to the script command.</span></span>

<span data-ttu-id="f16c8-113">如需如何使用此篩選準則的範例，請參閱 [薩米文 (CC) ](sami--cc--parser-filter.md)剖析器。</span><span class="sxs-lookup"><span data-stu-id="f16c8-113">For an example of how to use this filter, see [SAMI (CC) Parser](sami--cc--parser-filter.md).</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="f16c8-114">篩選介面</span><span class="sxs-lookup"><span data-stu-id="f16c8-114">Filter Interfaces</span></span></td>
<td><span data-ttu-id="f16c8-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>、 <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16c8-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f16c8-116">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="f16c8-116">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="f16c8-117">MEDIATYPE_ScriptCommand，MEDIASUBTYPE_Null</span><span class="sxs-lookup"><span data-stu-id="f16c8-117">MEDIATYPE_ScriptCommand, MEDIASUBTYPE_NULL</span></span></li>
<li><span data-ttu-id="f16c8-118">MEDIATYPE_Text，MEDIASUBTYPE_Null</span><span class="sxs-lookup"><span data-stu-id="f16c8-118">MEDIATYPE_Text, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f16c8-119">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="f16c8-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="f16c8-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="f16c8-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f16c8-121">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="f16c8-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="f16c8-122">不適用</span><span class="sxs-lookup"><span data-stu-id="f16c8-122">Not applicable</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f16c8-123">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="f16c8-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="f16c8-124">不適用</span><span class="sxs-lookup"><span data-stu-id="f16c8-124">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f16c8-125">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="f16c8-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="f16c8-126">{48025243-2D39-11CE-875D-00608CB78066}</span><span class="sxs-lookup"><span data-stu-id="f16c8-126">{48025243-2D39-11CE-875D-00608CB78066}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f16c8-127">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="f16c8-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="f16c8-128">沒有屬性頁</span><span class="sxs-lookup"><span data-stu-id="f16c8-128">No property page</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f16c8-129">可執行檔</span><span class="sxs-lookup"><span data-stu-id="f16c8-129">Executable</span></span></td>
<td><span data-ttu-id="f16c8-130">Quartz.dll</span><span class="sxs-lookup"><span data-stu-id="f16c8-130">Quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="f16c8-131"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="f16c8-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="f16c8-132">MERIT_PREFERRED + 1</span><span class="sxs-lookup"><span data-stu-id="f16c8-132">MERIT_PREFERRED + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="f16c8-133"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="f16c8-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="f16c8-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="f16c8-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="f16c8-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="f16c8-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f16c8-136">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="f16c8-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



