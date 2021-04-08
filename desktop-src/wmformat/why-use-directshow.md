---
title: 為何要使用 DirectShow
description: 為何要使用 DirectShow
ms.assetid: 0ab33526-73d0-425e-a03f-29c74555f578
keywords:
- Windows Media Format SDK、DirectShow
- Windows Media Format SDK，硬體
- 'Windows Media Format SDK、Windows Driver Model (WDM) '
- Advanced Systems Format (ASF) 、DirectShow
- ASF (Advanced Systems Format) ，DirectShow
- Advanced Systems Format (ASF) 、硬體
- ASF (Advanced Systems Format) ，硬體
- 'Advanced Systems Format (ASF) 、Windows Driver Model (WDM) '
- 'ASF (Advanced Systems Format) 、Windows Driver Model (WDM) '
- DirectShow，關於
- DirectShow，硬體
- 'DirectShow，Windows Driver Model (WDM) '
- 'Windows Driver Model (WDM) '
- 'WDM (Windows Driver Model) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f90fa1de01a7b136b938f9b09cc7fb2b3c229fad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103673115"
---
# <a name="why-use-directshow"></a><span data-ttu-id="8adc8-117">為何要使用 DirectShow？</span><span class="sxs-lookup"><span data-stu-id="8adc8-117">Why Use DirectShow?</span></span>

<span data-ttu-id="8adc8-118">應用程式可能會直接使用 DirectShow 而非 Windows Media 格式 SDK 的主要原因有兩種：適用于 DirectShow 串流架構的便利性，以及硬體的存取。</span><span class="sxs-lookup"><span data-stu-id="8adc8-118">There are two main reasons why an application might use DirectShow rather than the Windows Media Format SDK directly: for the convenience of the DirectShow streaming architecture, and for access to hardware.</span></span>

## <a name="convenience"></a><span data-ttu-id="8adc8-119">便利</span><span class="sxs-lookup"><span data-stu-id="8adc8-119">Convenience</span></span>

<span data-ttu-id="8adc8-120">使用 DirectShow 串流架構，只需要幾個方法呼叫來播放 Windows Media 音訊或 Windows Media 視訊的檔案。</span><span class="sxs-lookup"><span data-stu-id="8adc8-120">With DirectShow streaming architecture, it takes only a few method calls to play Windows Media Audio or Windows Media Video files.</span></span> <span data-ttu-id="8adc8-121">也簡化了建立檔案的程式。</span><span class="sxs-lookup"><span data-stu-id="8adc8-121">Creating files is also simplified.</span></span> <span data-ttu-id="8adc8-122">您只需使用篩選上的 **IConfigAsfWriter** 介面來指定設定檔，而 DirectShow 會自動載入轉譯或寫入資料流程所需的元件，並提供傳輸和同步處理媒體資料流程程的機制。</span><span class="sxs-lookup"><span data-stu-id="8adc8-122">You simply specify a profile using the **IConfigAsfWriter** interface on the filter, and DirectShow automatically loads the required components for rendering or writing the streams, and provides the mechanisms for transferring and synchronizing the flow of media data.</span></span> <span data-ttu-id="8adc8-123">當您將內容從各種格式轉換成 Windows Media 格式時，DirectShow 特別有用。</span><span class="sxs-lookup"><span data-stu-id="8adc8-123">DirectShow is especially useful when converting content from varied formats into Windows Media Format.</span></span> <span data-ttu-id="8adc8-124">您可以建立可解碼各種不同檔案和壓縮類型的 DirectShow 篩選圖形，然後將已解碼的資料流程饋送到 [WM ASF 寫入](wm-asf-writer-filter.md) 器篩選器中。</span><span class="sxs-lookup"><span data-stu-id="8adc8-124">You can create DirectShow filter graphs that decode a wide variety of file and compression types, and then feed the decoded streams into the [WM ASF Writer](wm-asf-writer-filter.md) filter.</span></span> <span data-ttu-id="8adc8-125">相較之下，此 SDK 中的 UncompAVItoWMV 範例只適用于未壓縮的 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="8adc8-125">By comparison, the UncompAVItoWMV sample in this SDK works only with uncompressed AVI files.</span></span> <span data-ttu-id="8adc8-126">文字資料流程和任意資料流程也可以透過 DirectShow 來建立和/或轉譯，但這可能需要您建立自訂的 DirectShow 篩選器來處理這些資料流程。</span><span class="sxs-lookup"><span data-stu-id="8adc8-126">Text streams and arbitrary data streams can also be created and/or rendered through DirectShow, but this might require you to create custom DirectShow filters for processing those streams.</span></span>

## <a name="access-to-hardware"></a><span data-ttu-id="8adc8-127">存取硬體</span><span class="sxs-lookup"><span data-stu-id="8adc8-127">Access to Hardware</span></span>

<span data-ttu-id="8adc8-128">DirectShow 是應用程式程式碼存取 Windows Driver Model (WDM) 型硬體裝置（例如 1394 DV 攝影機、電視調諧器和 USB 網路攝影機）的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="8adc8-128">DirectShow is the only way for application code to access Windows Driver Model (WDM)–based hardware devices such as 1394 DV cameras, TV tuners, and USB webcams.</span></span> <span data-ttu-id="8adc8-129">如果您的應用程式必須直接從以 WDM 為基礎的硬體裝置來捕捉資料，並將它轉碼為 Windows Media 格式，而且 Windows Media 編碼器 SDK 不符合您的需求，則 [DirectShow] 是唯一的替代方案。</span><span class="sxs-lookup"><span data-stu-id="8adc8-129">If your application must capture data directly from a WDM-based hardware device and transcode it to Windows Media Format, and the Windows Media Encoder SDK does not suit your needs, then DirectShow is the only alternative.</span></span> <span data-ttu-id="8adc8-130">DirectShow 也可以用來根據適用于 Windows 的影片來存取舊版裝置。</span><span class="sxs-lookup"><span data-stu-id="8adc8-130">DirectShow can also be used to access legacy devices based on Video for Windows.</span></span>

 

 




