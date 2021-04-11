---
description: 選擇影片編解碼器
ms.assetid: 3a4b925a-4fb4-4189-a571-8083454fed0e
title: '選擇影片編解碼器 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9186c7e7e60f5822ec2e50e3e5c7e16e96b91839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191083"
---
# <a name="choosing-a-video-codec-microsoft-media-foundation"></a><span data-ttu-id="8ec14-103">選擇影片編解碼器 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="8ec14-103">Choosing a Video Codec (Microsoft Media Foundation)</span></span>

<span data-ttu-id="8ec14-104">Windows Media 視訊9編碼器支援三種編碼輸出類別：主要設定檔、Advanced Profile 和 Image。</span><span class="sxs-lookup"><span data-stu-id="8ec14-104">The Windows Media Video 9 Encoder supports three categories of encoded output: Main Profile, Advanced Profile, and Image.</span></span> <span data-ttu-id="8ec14-105">主要設定檔類別提供複雜影片內容的一般影片壓縮，例如電影或音樂影片。</span><span class="sxs-lookup"><span data-stu-id="8ec14-105">The Main Profile category provides general video compression for complex video content, such as movies or music videos.</span></span> <span data-ttu-id="8ec14-106">主要設定檔的功能提供各式各樣的編碼設定。</span><span class="sxs-lookup"><span data-stu-id="8ec14-106">The features of the Main Profile provide for a wide range of encoding settings.</span></span> <span data-ttu-id="8ec14-107">您可以使用主要設定檔以非常低的位元速率來建立可在掌上型裝置上傳遞的影片，或在色譜的另一端使用它來建立數位影院的高定義影片。</span><span class="sxs-lookup"><span data-stu-id="8ec14-107">You can use the Main Profile to create video with very low bit rates for delivery on handheld devices or, at the other end of the spectrum, you can use it to create high-definition video for digital cinema.</span></span>

<span data-ttu-id="8ec14-108">主要設定檔中編碼演算法的重點在於動態影片內容，但也適用于其他影片內容。</span><span class="sxs-lookup"><span data-stu-id="8ec14-108">The emphasis of the encoding algorithms in the Main Profile is on dynamic video content, but they are suitable for other video content as well.</span></span> <span data-ttu-id="8ec14-109">主要設定檔應該是影片內容的預設類別。</span><span class="sxs-lookup"><span data-stu-id="8ec14-109">The Main Profile should be your default category for video content.</span></span> <span data-ttu-id="8ec14-110">若要符合特定需求，您可以使用 Advanced Profile 類別、影像類別或個別的編碼器，稱為 Windows Media 視訊9螢幕編碼器。</span><span class="sxs-lookup"><span data-stu-id="8ec14-110">To meet specific needs, you can use the Advanced Profile category, the Image category, or a separate encoder called the Windows Media Video 9 Screen encoder.</span></span> <span data-ttu-id="8ec14-111">下表列出四個選項。</span><span class="sxs-lookup"><span data-stu-id="8ec14-111">The following table lists the four options.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="8ec14-112">目的</span><span class="sxs-lookup"><span data-stu-id="8ec14-112">Purpose</span></span></th>
<th><span data-ttu-id="8ec14-113">轉碼器</span><span class="sxs-lookup"><span data-stu-id="8ec14-113">Codec</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8ec14-114">一般用途的影片編碼</span><span class="sxs-lookup"><span data-stu-id="8ec14-114">General-purpose video encoding</span></span></td>
<td><span data-ttu-id="8ec14-115"><a href="windowsmediavideo9encoder.md">Windows Media 視訊9編碼器</a></span><span class="sxs-lookup"><span data-stu-id="8ec14-115"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="8ec14-116">主要設定檔</span><span class="sxs-lookup"><span data-stu-id="8ec14-116">Main Profile</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ec14-117">編碼符合 VC 1 Advanced Profile SMPTE 標準的高定義影片或影片</span><span class="sxs-lookup"><span data-stu-id="8ec14-117">Encoding high definition video or video that conforms to the VC-1 Advanced Profile SMPTE standard</span></span></td>
<td><span data-ttu-id="8ec14-118"><a href="windowsmediavideo9encoder.md">Windows Media 視訊9編碼器</a></span><span class="sxs-lookup"><span data-stu-id="8ec14-118"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="8ec14-119">Advanced Profile</span><span class="sxs-lookup"><span data-stu-id="8ec14-119">Advanced Profile</span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8ec14-120">將點陣圖影像轉換成動態影片</span><span class="sxs-lookup"><span data-stu-id="8ec14-120">Converting bitmapped images to dynamic video</span></span></td>
<td><span data-ttu-id="8ec14-121"><a href="windowsmediavideo9encoder.md">Windows Media 視訊9編碼器</a></span><span class="sxs-lookup"><span data-stu-id="8ec14-121"><a href="windowsmediavideo9encoder.md">Windows Media Video 9 Encoder</a></span></span><dl> <span data-ttu-id="8ec14-122">Image</span><span class="sxs-lookup"><span data-stu-id="8ec14-122">Image</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8ec14-123">編碼電腦-應用程式影片 (螢幕擷取畫面) 或其他高度靜態的影片</span><span class="sxs-lookup"><span data-stu-id="8ec14-123">Encoding computer-application video (screen capture) or other highly static video</span></span></td>
<td><span data-ttu-id="8ec14-124"><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media 視訊9螢幕編碼器</strong></a></span><span class="sxs-lookup"><span data-stu-id="8ec14-124"><a href="windowsmediavideo9screenencoder.md"><strong>Windows Media Video 9 Screen Encoder</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8ec14-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="8ec14-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8ec14-126">使用影片</span><span class="sxs-lookup"><span data-stu-id="8ec14-126">Working with Video</span></span>](workingwithvideo.md)
</dt> </dl>

 

 



