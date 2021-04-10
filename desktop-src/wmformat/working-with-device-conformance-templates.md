---
title: 使用裝置一致性範本
description: 使用裝置一致性範本
ms.assetid: 230744d2-7c0f-4a14-8018-da88b5285add
keywords:
- 設定檔，裝置一致性範本
- 設定檔，一致性範本
- 編解碼器、裝置一致性範本
- 編解碼器，一致性範本
- 裝置一致性範本，關於
- 一致性範本
- 範本、裝置一致性範本
- Advanced Systems Format (ASF) 、裝置一致性範本
- ASF (Advanced Systems Format) 、裝置一致性範本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036d304aa43c0dce5fe4d5302dccc32484657155
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104092536"
---
# <a name="working-with-device-conformance-templates"></a><span data-ttu-id="fdb6a-112">使用裝置一致性範本</span><span class="sxs-lookup"><span data-stu-id="fdb6a-112">Working with Device Conformance Templates</span></span>

<span data-ttu-id="fdb6a-113">由於 ASF 檔案有很大的彈性，因此通常很難判斷檔案是否適合在特定裝置上播放。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-113">Because of the great flexibility of ASF files, it is often difficult to determine whether a file is appropriate for playback on a specific device.</span></span> <span data-ttu-id="fdb6a-114">例如，在桌上型電腦上針對本機播放所撰寫的檔案，並不適合用於掌上型裝置。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-114">For example, files written for local playback on desktop computers are not optimal for use on handheld devices.</span></span> <span data-ttu-id="fdb6a-115">裝置一致性範本可讓應用程式快速識別檔案預定的播放裝置類型。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-115">Device conformance templates enable applications to quickly identify the type of playback device for which a file was intended.</span></span> <span data-ttu-id="fdb6a-116">如果裝置一致性範本與裝置不符，應用程式可以通知使用者該檔案對裝置而言是不正確的。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-116">If the device conformance template does not match the device, the application can inform the user that the file is inappropriate for the device.</span></span> <span data-ttu-id="fdb6a-117">如此一來，使用者就能獲得更好的播放體驗。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-117">In this way, the user can be assured of a better playback experience.</span></span>

<span data-ttu-id="fdb6a-118">如果您要以獨佔方式寫入個人電腦上的檔案，則在建立設定檔時，裝置一致性範本將不會有許多因素。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-118">If you are writing files exclusively for use on personal computers, device conformance templates will not be as much of a factor in creating profiles.</span></span> <span data-ttu-id="fdb6a-119">這些範本的主要用途是確保為了與特殊硬體一起使用而建立的檔案，與整個裝置（而不只是單一裝置）相容。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-119">The main purpose of these templates is to ensure that files created for use with special hardware are compatible with a whole range of devices and not just a single device.</span></span>

<span data-ttu-id="fdb6a-120">裝置一致性範本是一個判斷提示，表示 ASF 檔案包含在特定參數內編碼的資料。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-120">A device conformance template is an assertion that an ASF file contains data encoded within certain parameters.</span></span> <span data-ttu-id="fdb6a-121">如需個別範本適用設定的詳細資訊，請參閱 [裝置一致性範本參數](device-conformance-template-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-121">For more information about the settings appropriate to the individual templates, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="fdb6a-122">下列編解碼器支援裝置一致性範本：</span><span class="sxs-lookup"><span data-stu-id="fdb6a-122">The following codecs support device conformance templates:</span></span>

-   <span data-ttu-id="fdb6a-123">Windows Media 視訊9</span><span class="sxs-lookup"><span data-stu-id="fdb6a-123">Windows Media Video 9</span></span>
-   <span data-ttu-id="fdb6a-124">Windows Media 音訊9和更新版本</span><span class="sxs-lookup"><span data-stu-id="fdb6a-124">Windows Media Audio 9 and later</span></span>
-   <span data-ttu-id="fdb6a-125">Windows Media 音訊 9 Professional 和更新版本</span><span class="sxs-lookup"><span data-stu-id="fdb6a-125">Windows Media Audio 9 Professional and later</span></span>
-   <span data-ttu-id="fdb6a-126">Windows Media 音訊9語音</span><span class="sxs-lookup"><span data-stu-id="fdb6a-126">Windows Media Audio 9 Voice</span></span>

<span data-ttu-id="fdb6a-127">您不需要採取任何特殊步驟就能使用裝置一致性範本。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-127">You do not need to take any special steps to use device conformance templates.</span></span> <span data-ttu-id="fdb6a-128">編解碼器會自動為檔案中的每個適當串流寫入範本字串。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-128">The codec automatically writes a template string for each appropriate stream in the file.</span></span> <span data-ttu-id="fdb6a-129">編解碼器會根據設定檔中的串流設定，決定要使用的範本。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-129">The codec will decide which template to use, based on the stream configuration settings in the profile.</span></span> <span data-ttu-id="fdb6a-130">裝置一致性範本參數中有一些重迭，因此您可能會想要要求特定的範本，而不是讓編解碼器為您指派一個範本。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-130">There is some overlap in device conformance template parameters, so you may want to request a specific template instead of letting the codec assign one for you.</span></span> <span data-ttu-id="fdb6a-131">您可以 \_ 使用適當串流設定物件的 [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) 介面方法來設定 g wszDecoderComplexityRequested 屬性，以指定您想要的範本。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-131">You can specify which template you want by setting the g\_wszDecoderComplexityRequested property with the methods of the [**IWMPropertyVault**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmpropertyvault) interface of the appropriate stream configuration object.</span></span>

<span data-ttu-id="fdb6a-132">寫入 ASF 檔案時，每個資料流程的實際裝置一致性範本會設定為編解碼器傳遞給寫入器的值。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-132">When an ASF file is written, the actual device conformance template for each stream is set to the value passed to the writer by the codec.</span></span> <span data-ttu-id="fdb6a-133">開啟要讀取的檔案時，您可以使用 [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) 介面的方法來取出 g \_ wszDeviceConformanceTemplate 資料流程層級屬性，以找出檔案資料流程符合的範本。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-133">When opening a file for reading, you can find out which template the streams of the file conform to by using the methods of the [**IWMHeaderInfo3**](/previous-versions/windows/desktop/api/wmsdkidl/nn-wmsdkidl-iwmheaderinfo3) interface to retrieve the g\_wszDeviceConformanceTemplate stream-level attribute.</span></span> <span data-ttu-id="fdb6a-134">如需屬性的詳細資訊，請參閱 [使用中繼資料](working-with-metadata.md)。</span><span class="sxs-lookup"><span data-stu-id="fdb6a-134">For more information about attributes, see [Working with Metadata](working-with-metadata.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="fdb6a-135">相關主題</span><span class="sxs-lookup"><span data-stu-id="fdb6a-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fdb6a-136">**設計設定檔**</span><span class="sxs-lookup"><span data-stu-id="fdb6a-136">**Designing Profiles**</span></span>](designing-profiles.md)
</dt> <dt>

[<span data-ttu-id="fdb6a-137">**裝置一致性範本參數**</span><span class="sxs-lookup"><span data-stu-id="fdb6a-137">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> </dl>

 

 




