---
title: Waveform-Audio 裝置的對應
description: Waveform-Audio 裝置的對應
ms.assetid: e23919c9-c5fa-4406-920c-1fdbeea4821d
keywords:
- 多媒體音訊，地圖波形-音訊裝置
- 音訊、地圖波形-音訊裝置
- 音訊壓縮管理員 (的) ，對應波形-音訊裝置
- 裝置 (音訊壓縮管理員) 、地圖波形-音訊裝置
- 對應波形-音訊裝置
- 多媒體音訊，對應程式
- 音訊、對應程式
- 音訊壓縮管理員 (的) 、對應工具
- " (的音訊壓縮管理員) 、對應程式"
- mapper
- 波形音訊、地圖裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9cdd269e21eb992244dd0e5979c7e0d193ba92b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103839747"
---
# <a name="mapping-waveform-audio-devices"></a><span data-ttu-id="65eb9-114">Waveform-Audio 裝置的對應</span><span class="sxs-lookup"><span data-stu-id="65eb9-114">Mapping Waveform-Audio Devices</span></span>

<span data-ttu-id="65eb9-115">Windows 為音訊裝置提供一組標準功能。</span><span class="sxs-lookup"><span data-stu-id="65eb9-115">Windows provides a set of standard functions for audio devices.</span></span> <span data-ttu-id="65eb9-116">這些函式會發出管理硬體裝置之設備磁碟機的呼叫。</span><span class="sxs-lookup"><span data-stu-id="65eb9-116">These functions issue calls to device drivers that manage hardware devices.</span></span> <span data-ttu-id="65eb9-117">系統會使用稱為「對應工具」的模組來管理已安裝的裝置。</span><span class="sxs-lookup"><span data-stu-id="65eb9-117">The system uses a module called a "mapper" to manage installed devices.</span></span> <span data-ttu-id="65eb9-118">對應工具會在驅動程式介面中使用特殊的勾點來攔截呼叫，以及在系統與系統中安裝的驅動程式之間扮演媒介。</span><span class="sxs-lookup"><span data-stu-id="65eb9-118">The mapper uses special hooks in the driver interface to intercept calls and to act as an intermediary between the system and the drivers installed in the system.</span></span> <span data-ttu-id="65eb9-119">對應工具會負責比對應用程式對裝置存取裝置的要求，以使用可用的裝置，以及尋找符合目前應用程式之音訊需求的裝置。</span><span class="sxs-lookup"><span data-stu-id="65eb9-119">The mapper is responsible for matching an application's requests for access to a device with the available devices and for finding a device that meets the current application's audio requirements.</span></span> <span data-ttu-id="65eb9-120">系統提供標準驅動程式類型的對應程式數目：波形-音訊、MIDI (音樂檢測數位介面) 和輔助裝置。</span><span class="sxs-lookup"><span data-stu-id="65eb9-120">The system provides mappers for standard driver types: waveform-audio, MIDI (Musical Instrument Digital Interface), and auxiliary devices.</span></span>

<span data-ttu-id="65eb9-121">System.servicemodel 是基本多媒體系統的延伸模組，並安裝為對應程式。</span><span class="sxs-lookup"><span data-stu-id="65eb9-121">The ACM is an extension of the basic multimedia system and is installed as a mapper.</span></span> <span data-ttu-id="65eb9-122">這表示「磁片磁碟機」會使用波形音訊裝置的驅動程式介面對應程式攔截。</span><span class="sxs-lookup"><span data-stu-id="65eb9-122">This means the ACM uses the driver-interface mapper hooks for waveform-audio devices.</span></span> <span data-ttu-id="65eb9-123">使用這些勾點，可讓進行中的資料在波形音訊裝置磁碟機之間進行解碼或編碼。</span><span class="sxs-lookup"><span data-stu-id="65eb9-123">Using these hooks allows the ACM to decode or encode waveform-audio data before passing it to or from a waveform-audio device driver.</span></span> <span data-ttu-id="65eb9-124">「高階」和「標準系統對應工具」之間的差異在於，「高階」可以搜尋支援指定格式的波形音訊裝置，或尋找支援指定格式的波形音訊裝置與高階壓縮工具或解壓縮程式組合。</span><span class="sxs-lookup"><span data-stu-id="65eb9-124">The difference between the ACM and the standard system mapper is that the ACM can search for a waveform-audio device that supports a specified format or find a combination of a waveform-audio device and an ACM compressor or decompressor that supports a specified format.</span></span>

<span data-ttu-id="65eb9-125">當應用程式要求系統為輸入或輸出開啟波形音訊裝置時，要求會指定格式和裝置。</span><span class="sxs-lookup"><span data-stu-id="65eb9-125">When an application requests that the system open a waveform-audio device for input or output, the request specifies the format and device.</span></span> <span data-ttu-id="65eb9-126">當指定的裝置是對應工具時，對應工具必須找到支援指定格式的裝置。</span><span class="sxs-lookup"><span data-stu-id="65eb9-126">When the specified device is the mapper, the mapper must find a device that supports the specified format.</span></span> <span data-ttu-id="65eb9-127">在執行程式中執行的對應程式會搜尋支援指定格式的已安裝波形音訊裝置。</span><span class="sxs-lookup"><span data-stu-id="65eb9-127">The mapper implemented in the ACM searches for an installed waveform-audio device that supports the specified format.</span></span> <span data-ttu-id="65eb9-128">如果 [高階] 找不到這類裝置，則會搜尋波形音訊裝置，以及一起支援格式的壓縮程式或解壓縮程式。</span><span class="sxs-lookup"><span data-stu-id="65eb9-128">If the ACM cannot find such a device, it searches for a waveform-audio device and a compressor or decompressor that together support the format.</span></span> <span data-ttu-id="65eb9-129">具體而言，執行程式會搜尋壓縮程式或解壓縮程式，以將指定的格式轉換成已安裝的波形音訊裝置所支援的格式。</span><span class="sxs-lookup"><span data-stu-id="65eb9-129">Specifically, the ACM searches for a compressor or decompressor that converts the specified format into a format that is supported by an installed waveform-audio device.</span></span> <span data-ttu-id="65eb9-130">當您找到支援已轉換格式的裝置之後，就可以接受要求來播放或記錄原先要求的格式，即使沒有任何安裝的波形音訊裝置直接支援該格式也一樣。</span><span class="sxs-lookup"><span data-stu-id="65eb9-130">After the ACM finds a device that supports the converted format, it can honor requests to play or record the format originally requested, even though no installed waveform-audio device directly supports that format.</span></span>

<span data-ttu-id="65eb9-131">除了格式轉換之外，「上建」也會提供服務，以支援壓縮、解壓縮、篩選、格式選取和篩選選取專案。</span><span class="sxs-lookup"><span data-stu-id="65eb9-131">In addition to format conversion, the ACM also offers services to support compression, decompression, filtering, format selection, and filter selection.</span></span> <span data-ttu-id="65eb9-132">它會藉由呼叫本身的驅動程式來提供其支援的標準 API。</span><span class="sxs-lookup"><span data-stu-id="65eb9-132">It provides a standard API that it supports by calling its own drivers.</span></span>

 

 




