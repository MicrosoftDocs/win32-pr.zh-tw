---
title: DirectShow QASF 參考
description: DirectShow QASF 參考
ms.assetid: 66f483b5-3886-48b4-bc43-7c3517abd20d
keywords:
- Windows Media Format SDK、QASF
- Windows Media Format SDK、DirectShow
- DirectShow、QASF 參考
- QASF 篩選準則，參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c509030f676b83a84f67590a242aea623656a514
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104375953"
---
# <a name="directshow-qasf-reference"></a><span data-ttu-id="f6a17-107">DirectShow QASF 參考</span><span class="sxs-lookup"><span data-stu-id="f6a17-107">DirectShow QASF Reference</span></span>

<span data-ttu-id="f6a17-108">本章節包含下列 DirectShow QASF 篩選器、介面和列舉的程式設計參考。</span><span class="sxs-lookup"><span data-stu-id="f6a17-108">This section contains programming references for the following DirectShow QASF filters, interfaces and enumerations.</span></span> <span data-ttu-id="f6a17-109">DirectShow SDK 檔包含這些篩選器所公開的其他泛型介面（例如 **IBaseFilter** 和 **IPin**），以及舊版 QASF 元件的參考和程式設計指南材質。</span><span class="sxs-lookup"><span data-stu-id="f6a17-109">The DirectShow SDK documentation contains reference and programming guide materials for additional generic interfaces exposed by these filters, such as **IBaseFilter** and **IPin**, and for earlier versions of the QASF components.</span></span>

<span data-ttu-id="f6a17-110">如需 QASF 名稱的說明，請參閱 [關於 DirectShow](about-directshow.md)。</span><span class="sxs-lookup"><span data-stu-id="f6a17-110">For an explanation of the QASF name, see [About DirectShow](about-directshow.md).</span></span>

<span data-ttu-id="f6a17-111">DirectShow QASF 元件包含下列篩選。</span><span class="sxs-lookup"><span data-stu-id="f6a17-111">The following filters are included with the DirectShow QASF components.</span></span>



| <span data-ttu-id="f6a17-112">篩選</span><span class="sxs-lookup"><span data-stu-id="f6a17-112">Filter</span></span>                                           | <span data-ttu-id="f6a17-113">Description</span><span class="sxs-lookup"><span data-stu-id="f6a17-113">Description</span></span>                                                      |
|--------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="f6a17-114">WM ASF 讀取器篩選器</span><span class="sxs-lookup"><span data-stu-id="f6a17-114">WM ASF Reader Filter</span></span>](wm-asf-reader-filter.md) | <span data-ttu-id="f6a17-115">讀取及剖析本機或遠端 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="f6a17-115">Reads and parses local or remote ASF files.</span></span>                      |
| [<span data-ttu-id="f6a17-116">WM ASF 寫入器篩選器</span><span class="sxs-lookup"><span data-stu-id="f6a17-116">WM ASF Writer Filter</span></span>](wm-asf-writer-filter.md) | <span data-ttu-id="f6a17-117">從壓縮或未壓縮的輸入資料流程建立 ASF 檔案。</span><span class="sxs-lookup"><span data-stu-id="f6a17-117">Creates ASF files from compressed or uncompressed input streams.</span></span> |



 

<span data-ttu-id="f6a17-118">下列介面是為了與 DirectShow QASF 元件搭配使用而定義的。</span><span class="sxs-lookup"><span data-stu-id="f6a17-118">The following interfaces are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="f6a17-119">介面</span><span class="sxs-lookup"><span data-stu-id="f6a17-119">Interface</span></span>                                                  | <span data-ttu-id="f6a17-120">描述</span><span class="sxs-lookup"><span data-stu-id="f6a17-120">Description</span></span>                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6a17-121">**IAMWMBufferPass**</span><span class="sxs-lookup"><span data-stu-id="f6a17-121">**IAMWMBufferPass**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpass)                 | <span data-ttu-id="f6a17-122">提供一種方法，可讓應用程式從 [WM Asf 寫入](wm-asf-writer-filter.md) 器的輸入 Pin 或 [wm asf 讀取](wm-asf-reader-filter.md) 器篩選器的輸出圖釘註冊回呼。</span><span class="sxs-lookup"><span data-stu-id="f6a17-122">Provides a method that enables applications to register for callbacks from the input pins of the [WM ASF Writer](wm-asf-writer-filter.md) or the output pins of the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span> <span data-ttu-id="f6a17-123">用於索引編制和新增資料單位延伸模組時。</span><span class="sxs-lookup"><span data-stu-id="f6a17-123">Used in indexing and when adding data unit extensions.</span></span> |
| [<span data-ttu-id="f6a17-124">**IAMWMBufferPassCallback**</span><span class="sxs-lookup"><span data-stu-id="f6a17-124">**IAMWMBufferPassCallback**</span></span>](/previous-versions/windows/desktop/api/dshowasf/nn-dshowasf-iamwmbufferpasscallback) | <span data-ttu-id="f6a17-125">由應用程式執行，並由篩選準則呼叫。</span><span class="sxs-lookup"><span data-stu-id="f6a17-125">Implemented by applications and called by the filters.</span></span> <span data-ttu-id="f6a17-126">應用程式會在此介面上使用一個方法，以取得資料流程中個別範例的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="f6a17-126">Applications use the one method on this interface to obtain information about individual samples in the stream.</span></span> <span data-ttu-id="f6a17-127">用於索引編制和新增資料單位延伸模組時。</span><span class="sxs-lookup"><span data-stu-id="f6a17-127">Used in indexing and when adding data unit extensions.</span></span>                                                 |
| <span data-ttu-id="f6a17-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6a17-128">[**IConfigAsfWriter**](/previous-versions/windows/desktop/legacy/dd743205(v=vs.85))</span></span>               | <span data-ttu-id="f6a17-129">在 WM ASF 寫入器上執行。</span><span class="sxs-lookup"><span data-stu-id="f6a17-129">Implemented on the WM ASF Writer.</span></span> <span data-ttu-id="f6a17-130">由應用程式用來指定檔案的設定檔和索引參數。</span><span class="sxs-lookup"><span data-stu-id="f6a17-130">Used by applications to specify profiles and indexing parameters for the file.</span></span>                                                                                                                                                              |
| <span data-ttu-id="f6a17-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6a17-131">[**IConfigAsfWriter2**](/previous-versions/windows/desktop/legacy/dd743206(v=vs.85))</span></span>             | <span data-ttu-id="f6a17-132">在 WM ASF 寫入器上提供額外的設定函數。</span><span class="sxs-lookup"><span data-stu-id="f6a17-132">Provides additional configuration functions on the WM ASF Writer.</span></span>                                                                                                                                                                                                             |



 

<span data-ttu-id="f6a17-133">已定義下列列舉、結構和事件以搭配 DirectShow QASF 元件使用。</span><span class="sxs-lookup"><span data-stu-id="f6a17-133">The following enumeration, structure, and events are defined for use with the DirectShow QASF components.</span></span>



| <span data-ttu-id="f6a17-134">列舉型別</span><span class="sxs-lookup"><span data-stu-id="f6a17-134">Enumeration</span></span>                                                               | <span data-ttu-id="f6a17-135">描述</span><span class="sxs-lookup"><span data-stu-id="f6a17-135">Description</span></span>                                                                                                                                                                       |
|---------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6a17-136">[\_AM \_ ASFWRITERCONFIG \_ PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f6a17-136">[\_AM\_ASFWRITERCONFIG\_PARAM](/previous-versions/windows/desktop/legacy/dd758054(v=vs.85))</span></span> | <span data-ttu-id="f6a17-137">定義 [**IConfigAsfWriter2：： GetParam**](iconfigasfwriter2-getparam.md) 和 [**SetParam**](iconfigasfwriter2-setparam.md) 方法中所使用的篩選設定參數。</span><span class="sxs-lookup"><span data-stu-id="f6a17-137">Defines filter configuration parameters used in the [**IConfigAsfWriter2::GetParam**](iconfigasfwriter2-getparam.md) and [**SetParam**](iconfigasfwriter2-setparam.md) methods.</span></span> |



 



| <span data-ttu-id="f6a17-138">結構</span><span class="sxs-lookup"><span data-stu-id="f6a17-138">Structure</span></span>                                         | <span data-ttu-id="f6a17-139">Description</span><span class="sxs-lookup"><span data-stu-id="f6a17-139">Description</span></span>                                                                                                                                           |
|---------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6a17-140">**\_WMT \_ 事件 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="f6a17-140">**AM\_WMT\_EVENT\_DATA**</span></span>](/previous-versions/windows/desktop/api/evcode/ns-evcode-am_wmt_event_data) | <span data-ttu-id="f6a17-141">包含與 [**WMT \_ 狀態**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) 事件有關的資訊，以及 WINDOWS Media 格式 SDK 所傳回的相關狀態碼。</span><span class="sxs-lookup"><span data-stu-id="f6a17-141">Contains information pertaining to a [**WMT\_STATUS**](/previous-versions/windows/desktop/api/Wmsdkidl/ne-wmsdkidl-wmt_status) event and the associated status code returned by the Windows Media Format SDK.</span></span> |



 



| <span data-ttu-id="f6a17-142">事件</span><span class="sxs-lookup"><span data-stu-id="f6a17-142">Event</span></span>                                           | <span data-ttu-id="f6a17-143">描述</span><span class="sxs-lookup"><span data-stu-id="f6a17-143">Description</span></span>                                                                                                     |
|-------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f6a17-144">EC \_ WMT \_ 活動</span><span class="sxs-lookup"><span data-stu-id="f6a17-144">EC\_WMT\_EVENT</span></span>](ec-wmt-event.md)              | <span data-ttu-id="f6a17-145">從 Windows Media 格式 SDK 轉送的事件。</span><span class="sxs-lookup"><span data-stu-id="f6a17-145">Event forwarded from the Windows Media Format SDK.</span></span>                                                              |
| [<span data-ttu-id="f6a17-146">EC \_ WMT \_ 索引 \_ 事件</span><span class="sxs-lookup"><span data-stu-id="f6a17-146">EC\_WMT\_INDEX\_EVENT</span></span>](ec-wmt-index-event.md) | <span data-ttu-id="f6a17-147">當應用程式使用 [WM ASF 寫入器](wm-asf-writer-filter.md) 來編制 Windows Media 視訊檔案的索引時傳送。</span><span class="sxs-lookup"><span data-stu-id="f6a17-147">Sent when an application uses the [WM ASF Writer](wm-asf-writer-filter.md) to index Windows Media Video files.</span></span> |



 

 

 