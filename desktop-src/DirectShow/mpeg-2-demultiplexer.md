---
description: 此篩選器會 demultiplexes 以推送模式傳遞的 MPEG-2 傳輸和程式串流。
ms.assetid: 99bfc55d-6519-4e85-98ce-cad27bd71ffb
title: MPEG-2 信號信號
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3ea71727dc273bd0dc5d65ac49b28385b4898067
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "107001646"
---
# <a name="mpeg-2-demultiplexer"></a><span data-ttu-id="10f1b-103">MPEG-2 信號信號</span><span class="sxs-lookup"><span data-stu-id="10f1b-103">MPEG-2 Demultiplexer</span></span>

<span data-ttu-id="10f1b-104">此篩選器會 demultiplexes 以推送模式傳遞的 MPEG-2 傳輸和程式串流。</span><span class="sxs-lookup"><span data-stu-id="10f1b-104">This filter demultiplexes MPEG-2 transport and program streams that are delivered in push-mode.</span></span> <span data-ttu-id="10f1b-105">從 Windows XP 開始，此篩選器也支援提取模式的程式資料流程， (檔案播放) 。</span><span class="sxs-lookup"><span data-stu-id="10f1b-105">Starting in Windows XP, this filter also supports program streams in pull mode (file playback).</span></span> <span data-ttu-id="10f1b-106">在舊版平臺上，請在提取模式中使用程式資料流程的 [Mpeg-2 分隔](mpeg-2-splitter.md) 器篩選器。</span><span class="sxs-lookup"><span data-stu-id="10f1b-106">On earlier platforms, use the [MPEG-2 Splitter](mpeg-2-splitter.md) filter for program streams in pull mode.</span></span> <span data-ttu-id="10f1b-107">此篩選器可以在任何類型的篩選圖形中使用，包括 BDA 數位電視濾波器圖形。</span><span class="sxs-lookup"><span data-stu-id="10f1b-107">This filter can be used in any type of filter graph, including a BDA digital TV filter graph.</span></span>

> [!Note]  
> <span data-ttu-id="10f1b-108">MPEG-2 信號信號不支援框架正確的搜尋。</span><span class="sxs-lookup"><span data-stu-id="10f1b-108">The MPEG-2 Demultiplexer does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="10f1b-109">篩選介面</span><span class="sxs-lookup"><span data-stu-id="10f1b-109">Filter Interfaces</span></span></td>
<td><span data-ttu-id="10f1b-110">所有模式：</span><span class="sxs-lookup"><span data-stu-id="10f1b-110">All modes:</span></span><br/>
<ul>
<li><span data-ttu-id="10f1b-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="10f1b-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></li>
<li><span data-ttu-id="10f1b-112"><strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="10f1b-112"><strong>ISpecifyPropertyPages</strong></span></span></li>
</ul>
<span data-ttu-id="10f1b-113">僅限推送模式：</span><span class="sxs-lookup"><span data-stu-id="10f1b-113">Push mode only:</span></span><br/>
<ul>
<li><span data-ttu-id="10f1b-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span><span class="sxs-lookup"><span data-stu-id="10f1b-114"><a href="/windows/desktop/api/Strmif/nn-strmif-iamfiltermiscflags"><strong>IAMFilterMiscFlags</strong></a></span></span></li>
<li><span data-ttu-id="10f1b-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span><span class="sxs-lookup"><span data-stu-id="10f1b-115"><a href="/windows/desktop/api/Strmif/nn-strmif-impeg2demultiplexer"><strong>IMpeg2Demultiplexer</strong></a></span></span></li>
<li><span data-ttu-id="10f1b-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span><span class="sxs-lookup"><span data-stu-id="10f1b-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ireferenceclock"><strong>IReferenceClock</strong></a></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10f1b-117">輸入 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="10f1b-117">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="10f1b-118">主要類型： MEDIATYPE_STREAM</span><span class="sxs-lookup"><span data-stu-id="10f1b-118">Major type: MEDIATYPE_STREAM</span></span><br/> <span data-ttu-id="10f1b-119">亞：</span><span class="sxs-lookup"><span data-stu-id="10f1b-119">Subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="10f1b-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="10f1b-120">KSDATAFORMAT_SUBTYPE_BDA_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="10f1b-121">MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="10f1b-121">MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="10f1b-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span><span class="sxs-lookup"><span data-stu-id="10f1b-122">MEDIASUBTYPE_MPEG2_TRANSPORT</span></span></li>
<li><span data-ttu-id="10f1b-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span><span class="sxs-lookup"><span data-stu-id="10f1b-123">MEDIASUBTYPE_MPEG2_TRANSPORT_STRIDE</span></span></li>
</ul>
<span data-ttu-id="10f1b-124">如需詳細資訊，請參閱 <a href="mpeg-2-demultiplexer-media-types.md"><strong>Mpeg-2 信號的媒體類型</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="10f1b-124">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10f1b-125">輸入 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="10f1b-125">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="10f1b-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="10f1b-126"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10f1b-127">輸出 Pin 媒體類型</span><span class="sxs-lookup"><span data-stu-id="10f1b-127">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="10f1b-128">音訊和影片的基本資料流程必須有主要類型的 MEDIATYPE_Audio 或 MEDIATYPE_Video。</span><span class="sxs-lookup"><span data-stu-id="10f1b-128">Audio and video elementary streams must have a major type of MEDIATYPE_Audio or MEDIATYPE_Video.</span></span><br/> <span data-ttu-id="10f1b-129">如需詳細資訊，請參閱 <a href="mpeg-2-demultiplexer-media-types.md"><strong>Mpeg-2 信號的媒體類型</strong></a>。</span><span class="sxs-lookup"><span data-stu-id="10f1b-129">For more information, see <a href="mpeg-2-demultiplexer-media-types.md"><strong>MPEG-2 Demultiplexer Media Types</strong></a>.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10f1b-130">輸出 Pin 介面</span><span class="sxs-lookup"><span data-stu-id="10f1b-130">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="10f1b-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>，僅限 <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>Push 模式： <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>、 <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>、 <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span><span class="sxs-lookup"><span data-stu-id="10f1b-131"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a>Push mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-iampushsource"><strong>IAMPushSource</strong></a>, <a href="/previous-versions/windows/desktop/api/Bdaiface/nn-bdaiface-impeg2pidmap"><strong>IMPEG2PIDMap</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-impeg2streamidmap"><strong>IMPEG2StreamIdMap</strong></a></span></span><br/> <span data-ttu-id="10f1b-132">僅提取模式： <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="10f1b-132">Pull mode only: <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10f1b-133">篩選 CLSID</span><span class="sxs-lookup"><span data-stu-id="10f1b-133">Filter CLSID</span></span></td>
<td><span data-ttu-id="10f1b-134">CLSID_MPEG2Demultiplexer</span><span class="sxs-lookup"><span data-stu-id="10f1b-134">CLSID_MPEG2Demultiplexer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10f1b-135">屬性頁 CLSID</span><span class="sxs-lookup"><span data-stu-id="10f1b-135">Property Page CLSID</span></span></td>
<td><span data-ttu-id="10f1b-136">僅供測試之用。</span><span class="sxs-lookup"><span data-stu-id="10f1b-136">Available for testing only.</span></span> <span data-ttu-id="10f1b-137">使用 <strong>ISpecifyPropertyPages</strong> 介面存取屬性頁</span><span class="sxs-lookup"><span data-stu-id="10f1b-137">Use the <strong>ISpecifyPropertyPages</strong> interface to access the property pages</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10f1b-138">可執行檔</span><span class="sxs-lookup"><span data-stu-id="10f1b-138">Executable</span></span></td>
<td><span data-ttu-id="10f1b-139">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="10f1b-139">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="10f1b-140"><a href="merit.md">優點</a></span><span class="sxs-lookup"><span data-stu-id="10f1b-140"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="10f1b-141">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="10f1b-141">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="10f1b-142"><a href="filter-categories.md">篩選準則分類</a></span><span class="sxs-lookup"><span data-stu-id="10f1b-142"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="10f1b-143">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="10f1b-143">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="10f1b-144">備註</span><span class="sxs-lookup"><span data-stu-id="10f1b-144">Remarks</span></span>

<span data-ttu-id="10f1b-145">若要輸出音訊和影片的基本資料流程，demux 必須接收 PCR 和 SCR 資料流程。</span><span class="sxs-lookup"><span data-stu-id="10f1b-145">To output audio and video elementary streams, the demux must receive the PCR and SCR streams.</span></span> <span data-ttu-id="10f1b-146">在輸入端，這表示傳輸資料流程必須包含定義 PCR 資料流程之 PID 的 PAT 和 PMT 資料表;和程式資料流程必須包含至少一個套件標頭。</span><span class="sxs-lookup"><span data-stu-id="10f1b-146">On the input side, this means a transport stream must contain the PAT and PMT tables that define the PID for the PCR stream; and program streams must contain at least one pack header.</span></span>

## <a name="requirements"></a><span data-ttu-id="10f1b-147">規格需求</span><span class="sxs-lookup"><span data-stu-id="10f1b-147">Requirements</span></span>



| <span data-ttu-id="10f1b-148">需求</span><span class="sxs-lookup"><span data-stu-id="10f1b-148">Requirement</span></span> | <span data-ttu-id="10f1b-149">值</span><span class="sxs-lookup"><span data-stu-id="10f1b-149">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="10f1b-150">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="10f1b-150">Minimum supported client</span></span><br/> | <span data-ttu-id="10f1b-151">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10f1b-151">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="10f1b-152">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="10f1b-152">Minimum supported server</span></span><br/> | <span data-ttu-id="10f1b-153">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="10f1b-153">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="10f1b-154">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="10f1b-154">End of server support</span></span><br/>    | <span data-ttu-id="10f1b-155">Windows Server 2003 R2</span><span class="sxs-lookup"><span data-stu-id="10f1b-155">Windows Server 2003 R2</span></span><br/>                          |



## <a name="see-also"></a><span data-ttu-id="10f1b-156">另請參閱</span><span class="sxs-lookup"><span data-stu-id="10f1b-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="10f1b-157">DirectShow 篩選</span><span class="sxs-lookup"><span data-stu-id="10f1b-157">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="10f1b-158">使用 MPEG-2 信號信號</span><span class="sxs-lookup"><span data-stu-id="10f1b-158">Using the MPEG-2 Demultiplexer</span></span>](using-the-mpeg-2-demultiplexer.md)
</dt> </dl>

 

 




