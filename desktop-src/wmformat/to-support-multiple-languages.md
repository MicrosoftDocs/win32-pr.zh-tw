---
title: 支援多種語言
description: 支援多種語言
ms.assetid: b0061de4-d725-455f-9d9b-5bd0dbe8ff53
keywords:
- Windows Media Format SDK，支援多種語言
- Windows Media Format SDK，多重語言支援
- Windows Media Format SDK，語言支援
- Advanced Systems Format (ASF) ，支援多種語言
- ASF (Advanced Systems Format) ，支援多種語言
- Advanced Systems Format (ASF) 、多重語言支援
- ASF (Advanced Systems Format) 、多重語言支援
- Advanced Systems Format (ASF) ，語言支援
- ASF (Advanced Systems Format) ，語言支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bc070bda1cc25c6b7fd0fa583a8ac63a55fa603
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "103933006"
---
# <a name="to-support-multiple-languages"></a><span data-ttu-id="41ab0-112">支援多種語言</span><span class="sxs-lookup"><span data-stu-id="41ab0-112">To Support Multiple Languages</span></span>

<span data-ttu-id="41ab0-113">您可以在資料流程和中繼資料中支援多種語言。</span><span class="sxs-lookup"><span data-stu-id="41ab0-113">You can support multiple languages both in streams and in metadata.</span></span> <span data-ttu-id="41ab0-114">Windows Media 格式 SDK 中的多語言支援核心是 [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) 介面，可維護所支援的語言清單。</span><span class="sxs-lookup"><span data-stu-id="41ab0-114">The core of multiple language support in the Windows Media Format SDK is the [**IWMLanguageList**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist) interface, which maintains a list of the languages supported.</span></span> <span data-ttu-id="41ab0-115">語言清單會為每個支援的語言提供一個索引，此索引會在處理多種語言時用於 SDK 中的各種物件。</span><span class="sxs-lookup"><span data-stu-id="41ab0-115">The language list gives each supported language an index, which is used in various objects in the SDK when dealing with the multiple languages.</span></span>

<span data-ttu-id="41ab0-116">[**IWMLanguageList：： AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string)方法會將語言新增至清單。</span><span class="sxs-lookup"><span data-stu-id="41ab0-116">The [**IWMLanguageList::AddLanguageByRFC1766String**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-addlanguagebyrfc1766string) method adds a language to the list.</span></span> <span data-ttu-id="41ab0-117">您可以使用 [**IWMLanguageList：： GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) 取得語言的總數量，然後針對每個語言逐一查看呼叫 [**IWMLanguageList：： GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) 的語言，以識別已在清單中的語言。</span><span class="sxs-lookup"><span data-stu-id="41ab0-117">You can identify the languages already in the list by obtaining the total number of languages with [**IWMLanguageList::GetLanguageCount**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagecount) and then looping through the languages calling [**IWMLanguageList::GetLanguageDetails**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmlanguagelist-getlanguagedetails) for each.</span></span> <span data-ttu-id="41ab0-118">語言索引是以零為基底。</span><span class="sxs-lookup"><span data-stu-id="41ab0-118">The language index is zero based.</span></span>

## <a name="to-configure-mutual-exclusion-by-language"></a><span data-ttu-id="41ab0-119">依語言設定相互排除</span><span class="sxs-lookup"><span data-stu-id="41ab0-119">To Configure Mutual Exclusion by Language</span></span>

<span data-ttu-id="41ab0-120">依語言設定簡單的互斥物件非常簡單。</span><span class="sxs-lookup"><span data-stu-id="41ab0-120">Configuring a simple mutual exclusion object by language is very simple.</span></span> <span data-ttu-id="41ab0-121">每個資料流程現在都與語言相關聯。</span><span class="sxs-lookup"><span data-stu-id="41ab0-121">Each stream is now associated with a language.</span></span> <span data-ttu-id="41ab0-122">您可以使用 [**IWMStreamConfig3：： SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage)來設定與資料流程相關聯的語言。</span><span class="sxs-lookup"><span data-stu-id="41ab0-122">The language associated with a stream can be set using [**IWMStreamConfig3::SetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmstreamconfig3-setlanguage).</span></span> <span data-ttu-id="41ab0-123">設定所有互斥資料流程之後，只要建立相互排除的物件，就像任何其他類型一樣。</span><span class="sxs-lookup"><span data-stu-id="41ab0-123">After all of the mutually exclusive streams are configured, simply create a mutual exclusion object as you would for any other type.</span></span> <span data-ttu-id="41ab0-124">然後呼叫 [**IWMMutualExclusion：： >advanced.field.settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) 傳遞 CLSID \_ WMMUTEX \_ Language 作為型別。</span><span class="sxs-lookup"><span data-stu-id="41ab0-124">Then call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) passing CLSID\_WMMUTEX\_Language for the type.</span></span>

<span data-ttu-id="41ab0-125">當專有資料流程也以位元速率互斥時，語言互斥的資料流程會變得更複雜。</span><span class="sxs-lookup"><span data-stu-id="41ab0-125">Streams that are mutually exclusive by language become more complicated when the exclusive streams are also mutually exclusive by bit rate.</span></span> <span data-ttu-id="41ab0-126">在此情況下，您必須執行下列步驟來使用互斥記錄：</span><span class="sxs-lookup"><span data-stu-id="41ab0-126">In this case you must use mutually exclusive records, by performing the following steps:</span></span>

1.  <span data-ttu-id="41ab0-127">為每種語言的不同位速率資料流程建立相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="41ab0-127">Create a mutual exclusion object for the streams of differing bit rates in each language.</span></span> <span data-ttu-id="41ab0-128">如需以位元速率建立相互排除物件的詳細資訊，請參閱 [使用多位元率互斥](using-multiple-bit-rate-mutual-exclusion.md)。</span><span class="sxs-lookup"><span data-stu-id="41ab0-128">For more information about creating a mutual exclusion object by bit rate, see [Using Multiple Bit Rate Mutual Exclusion](using-multiple-bit-rate-mutual-exclusion.md).</span></span>
2.  <span data-ttu-id="41ab0-129">建立相互排除物件。</span><span class="sxs-lookup"><span data-stu-id="41ab0-129">Create a mutual exclusion object.</span></span> <span data-ttu-id="41ab0-130">呼叫 [**IWMMutualExclusion：： >advanced.field.settype**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) 並傳遞 CLSID \_ WMMUTEX \_ 語言，以指定獨佔性 by language。</span><span class="sxs-lookup"><span data-stu-id="41ab0-130">Call [**IWMMutualExclusion::SetType**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion-settype) and pass CLSID\_WMMUTEX\_Language to specify exclusivity by language.</span></span>
3.  <span data-ttu-id="41ab0-131">藉由呼叫 [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)的 **QueryInterface** 方法，取得在步驟2中建立之相互排除物件的 [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)介面指標。</span><span class="sxs-lookup"><span data-stu-id="41ab0-131">Obtain a pointer to the [**IWMMutualExclusion2**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2) interface of the mutual exclusion object created in step 2 by calling the **QueryInterface** method of [**IWMMutualExclusion**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion).</span></span>
4.  <span data-ttu-id="41ab0-132">針對每個語言呼叫 [**IWMMutualExclusion2：： AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) 方法一次，以建立將會互斥的資料流程記錄。</span><span class="sxs-lookup"><span data-stu-id="41ab0-132">Call the [**IWMMutualExclusion2::AddRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addrecord) method once for each language, to create stream records that will be mutually exclusive.</span></span>
5.  <span data-ttu-id="41ab0-133">針對在步驟4中建立的每一筆記錄，使用 [**IWMMutualExclusion2：： AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord)的呼叫新增適當語言的資料流程。</span><span class="sxs-lookup"><span data-stu-id="41ab0-133">For each record created in step 4, add the streams of the appropriate language with calls to [**IWMMutualExclusion2::AddStreamForRecord**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmmutualexclusion2-addstreamforrecord).</span></span>

## <a name="to-read-files-with-multiple-languages"></a><span data-ttu-id="41ab0-134">讀取具有多種語言的檔案</span><span class="sxs-lookup"><span data-stu-id="41ab0-134">To Read Files with Multiple Languages</span></span>

<span data-ttu-id="41ab0-135">Reader 物件提供方法，以識別檔案中資料流程的可用語言。</span><span class="sxs-lookup"><span data-stu-id="41ab0-135">The reader object provides methods to identify the available languages of streams in a file.</span></span> <span data-ttu-id="41ab0-136">您可以藉由呼叫 [**IWMReaderAdvanced4：： GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount)，來取得輸出的支援語言數目。</span><span class="sxs-lookup"><span data-stu-id="41ab0-136">You can retrieve the number of supported languages for an output by calling [**IWMReaderAdvanced4::GetLanguageCount**](/previous-versions/windows/desktop/api/wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguagecount).</span></span> <span data-ttu-id="41ab0-137">然後，您可以呼叫 [**IWMReaderAdvanced4：： GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage)來取得每個語言的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="41ab0-137">You can then retrieve details about each language with calls to [**IWMReaderAdvanced4::GetLanguage**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced4-getlanguage).</span></span>

<span data-ttu-id="41ab0-138">您可以藉由呼叫 [**IWMReaderAdvanced2：： SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting)，將該語言的索引傳遞給讀取器，以指定要播放的語言。</span><span class="sxs-lookup"><span data-stu-id="41ab0-138">You can specify the language to play by passing the index of that language to the reader with a call to [**IWMReaderAdvanced2::SetOutputSetting**](/previous-versions/windows/desktop/api/Wmsdkidl/nf-wmsdkidl-iwmreaderadvanced2-setoutputsetting).</span></span> <span data-ttu-id="41ab0-139">這會選取指定的語言，同時為檔案中的任何其他互斥物件維持自動資料流程選取。</span><span class="sxs-lookup"><span data-stu-id="41ab0-139">This will select the specified language while maintaining automatic stream selection for any other mutual exclusion objects in the file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="41ab0-140">相關主題</span><span class="sxs-lookup"><span data-stu-id="41ab0-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="41ab0-141">**Advanced 主題**</span><span class="sxs-lookup"><span data-stu-id="41ab0-141">**Advanced Topics**</span></span>](advanced-topics.md)
</dt> <dt>

[<span data-ttu-id="41ab0-142">**IWMLanguageList 介面**</span><span class="sxs-lookup"><span data-stu-id="41ab0-142">**IWMLanguageList Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmlanguagelist)
</dt> <dt>

[<span data-ttu-id="41ab0-143">**IWMMutualExclusion 介面**</span><span class="sxs-lookup"><span data-stu-id="41ab0-143">**IWMMutualExclusion Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion)
</dt> <dt>

[<span data-ttu-id="41ab0-144">**IWMMutualExclusion2 介面**</span><span class="sxs-lookup"><span data-stu-id="41ab0-144">**IWMMutualExclusion2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmmutualexclusion2)
</dt> <dt>

[<span data-ttu-id="41ab0-145">**IWMReaderAdvanced2 介面**</span><span class="sxs-lookup"><span data-stu-id="41ab0-145">**IWMReaderAdvanced2 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced2)
</dt> <dt>

[<span data-ttu-id="41ab0-146">**IWMReaderAdvanced4 介面**</span><span class="sxs-lookup"><span data-stu-id="41ab0-146">**IWMReaderAdvanced4 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmreaderadvanced4)
</dt> <dt>

[<span data-ttu-id="41ab0-147">**IWMStreamConfig3 介面**</span><span class="sxs-lookup"><span data-stu-id="41ab0-147">**IWMStreamConfig3 Interface**</span></span>](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmstreamconfig3)
</dt> </dl>

 

 




