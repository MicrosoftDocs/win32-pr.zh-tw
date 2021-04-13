---
title: WMPDVD 通訊協定
description: WMPDVD 通訊協定
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows Media Player，通訊協定
- Windows Media Player 物件模型，通訊協定
- 物件模型，通訊協定
- Windows Media Player ActiveX 控制項，物件模型的通訊協定
- ActiveX 控制項，物件模型的通訊協定
- Windows Media Player 的行動 ActiveX 控制項、物件模型的通訊協定
- Windows Media Player 行動裝置、物件模型的通訊協定
- 通訊協定，Windows Media Player 物件模型
- 通訊協定，WMPDVD
- WMPDVD 通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc4d3949c18a268ea6a2fffc196081ba466b5758
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300711"
---
# <a name="wmpdvd-protocol"></a><span data-ttu-id="96ea9-113">WMPDVD 通訊協定</span><span class="sxs-lookup"><span data-stu-id="96ea9-113">WMPDVD Protocol</span></span>

<span data-ttu-id="96ea9-114">WMPDVD 通訊協定可讓您使用 URL 語法，指定 DVD 中的媒體。</span><span class="sxs-lookup"><span data-stu-id="96ea9-114">The WMPDVD protocol enables you to specify media from a DVD using URL syntax.</span></span> <span data-ttu-id="96ea9-115">這是通訊協定的一般形式：</span><span class="sxs-lookup"><span data-stu-id="96ea9-115">This is the general form of the protocol:</span></span>


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



<span data-ttu-id="96ea9-116">*磁片磁碟機* 區段是 DVD 光碟機的字母;它不包含通常搭配磁片磁碟機規範使用的冒號。</span><span class="sxs-lookup"><span data-stu-id="96ea9-116">The *drive* segment is the letter of the DVD drive; it does not include the colon typically used with drive specifiers.</span></span> <span data-ttu-id="96ea9-117">此區段一律為必要項。</span><span class="sxs-lookup"><span data-stu-id="96ea9-117">This segment is always required.</span></span>

<span data-ttu-id="96ea9-118">*標題* 區段是要播放的標題編號。</span><span class="sxs-lookup"><span data-stu-id="96ea9-118">The *title* segment is the number of the title to play.</span></span> <span data-ttu-id="96ea9-119">除非您想要在特定標題或特定標題的特定章節上開始播放，否則不需要此專案。</span><span class="sxs-lookup"><span data-stu-id="96ea9-119">It is not required unless you want to start playback at a specific title or at a specific chapter of a specific title.</span></span>

<span data-ttu-id="96ea9-120">*章節* 區段是要播放的章節編號。</span><span class="sxs-lookup"><span data-stu-id="96ea9-120">The *chapter* segment is the number of the chapter to play.</span></span> <span data-ttu-id="96ea9-121">除非您想要在特定標題的特定章節上開始播放，否則不需要此專案。</span><span class="sxs-lookup"><span data-stu-id="96ea9-121">It is not required unless you want to start playback at a specific chapter of a specific title.</span></span>

<span data-ttu-id="96ea9-122">Contentdir 引數是影片 TS 的路徑 \_ 。IFO 檔案，可能位於本機儲存體或網路共用上。</span><span class="sxs-lookup"><span data-stu-id="96ea9-122">The contentdir argument is the path to a VIDEO\_TS.IFO file, which may be in local storage or on a network share.</span></span> <span data-ttu-id="96ea9-123">如果您包含此區段，則會忽略 *磁片磁碟機* 區段，不過它仍然是必要的。</span><span class="sxs-lookup"><span data-stu-id="96ea9-123">If you include this segment, then the *drive* segment is ignored although it is still required.</span></span> <span data-ttu-id="96ea9-124">如果您也包含 *標題* 區段或 *標題* 和 *章節* 區段，則會相對於 contentdir 區段中指定的 DVD 內容，而不是 *磁片磁碟機* 區段。</span><span class="sxs-lookup"><span data-stu-id="96ea9-124">If you also include the *title* segment or both the *title* and *chapter* segments then they are relative to the DVD content specified in the contentdir segment, not the *drive* segment.</span></span>

<span data-ttu-id="96ea9-125">下列範例會使用 WMPDVD 通訊協定，從頭開始播放 DVD，就像是自動啟動一樣。</span><span class="sxs-lookup"><span data-stu-id="96ea9-125">The following example uses the WMPDVD protocol to play the DVD from the beginning, as if it were starting automatically.</span></span>


```C++
player.url = "wmpdvd://F";
```



<span data-ttu-id="96ea9-126">下列範例會使用 WMPDVD 通訊協定，從指定標題的開頭播放 DVD。</span><span class="sxs-lookup"><span data-stu-id="96ea9-126">The following example uses the WMPDVD protocol to play the DVD from the beginning of the specified title.</span></span>


```C++
player.url = "wmpdvd://F/2";
```



<span data-ttu-id="96ea9-127">下列範例會使用 WMPDVD 通訊協定，從指定的章節播放 DVD。</span><span class="sxs-lookup"><span data-stu-id="96ea9-127">The following example uses the WMPDVD protocol to play the DVD from the specified chapter.</span></span>


```C++
player.url = "wmpdvd://F/2/4";
```



<span data-ttu-id="96ea9-128">下列範例會使用 WMPDVD 通訊協定，從本機儲存體播放 DVD 內容。</span><span class="sxs-lookup"><span data-stu-id="96ea9-128">The following example uses the WMPDVD protocol to play DVD content from local storage.</span></span> <span data-ttu-id="96ea9-129">*路徑* 字串的結尾是包含影片 TS 的資料夾 \_ 。IFO 檔案;它不包含檔案名。</span><span class="sxs-lookup"><span data-stu-id="96ea9-129">The *path* string ends with the folder that contains the VIDEO\_TS.IFO file; it does not include the file name.</span></span> <span data-ttu-id="96ea9-130">在此範例中， *磁片磁碟機* 區段的值不會有任何作用，雖然它是必要的，而且會從標題2的第4章開始播放。</span><span class="sxs-lookup"><span data-stu-id="96ea9-130">In this example, the value of the *drive* segment has no effect although it is required, and playback begins in chapter 4 of title 2.</span></span>


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



<span data-ttu-id="96ea9-131">將 WMPDVD 字串指派給 **url** 屬性需要 Windows Media Player 9 系列或更新版本。</span><span class="sxs-lookup"><span data-stu-id="96ea9-131">Assigning a WMPDVD string to the **url** property requires Windows Media Player 9 Series or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96ea9-132">相關主題</span><span class="sxs-lookup"><span data-stu-id="96ea9-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96ea9-133">**支援的通訊協定和檔案類型**</span><span class="sxs-lookup"><span data-stu-id="96ea9-133">**Supported Protocols and File Types**</span></span>](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




