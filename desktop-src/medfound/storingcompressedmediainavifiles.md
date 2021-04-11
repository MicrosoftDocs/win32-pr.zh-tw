---
description: 說明如何將 Windows Media 資料儲存在 AVI 檔案中。
ms.assetid: f2a9d9ff-4876-4f24-b96a-5d89e42fa3d5
title: '將壓縮的媒體儲存在 AVI 檔案中 (Microsoft 媒體基礎) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 080524a47b4295517d50705f6aeb125d085a8346
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "104321575"
---
# <a name="storing-compressed-media-in-avi-files-microsoft-media-foundation"></a><span data-ttu-id="b56a5-103">將壓縮的媒體儲存在 AVI 檔案中 (Microsoft 媒體基礎) </span><span class="sxs-lookup"><span data-stu-id="b56a5-103">Storing Compressed Media in AVI Files (Microsoft Media Foundation)</span></span>

<span data-ttu-id="b56a5-104">您使用 Windows Media 音訊和影片編解碼器壓縮的任何內容，都必須以某些容器格式放置。</span><span class="sxs-lookup"><span data-stu-id="b56a5-104">Any of the content that you compress using the Windows Media Audio and Video codecs must be put in some container format.</span></span> <span data-ttu-id="b56a5-105">其中一種最受歡迎的格式是音訊影片交錯或 AVI。</span><span class="sxs-lookup"><span data-stu-id="b56a5-105">One of the most popular formats is Audio Video Interleave, or AVI.</span></span> <span data-ttu-id="b56a5-106">您可以使用適用于 Windows (VfW) 或 Microsoft DirectShow 的 Microsoft 影片來建立 AVI 檔案。</span><span class="sxs-lookup"><span data-stu-id="b56a5-106">You can use Microsoft Video for Windows (VfW) or Microsoft DirectShow to create AVI files.</span></span> <span data-ttu-id="b56a5-107">如需有關使用 Windows 或 DirectShow 影片的詳細資訊，請參閱 MSDN 上的產品檔。</span><span class="sxs-lookup"><span data-stu-id="b56a5-107">For more information about using Video for Windows or DirectShow, refer to the product documentation on MSDN.</span></span>

<span data-ttu-id="b56a5-108">已開發 Windows Media 音訊和影片編解碼器，以使用 Advanced Systems 格式的屬性 (ASF) ，也就是 Windows Media 所使用的容器。</span><span class="sxs-lookup"><span data-stu-id="b56a5-108">The Windows Media Audio and Video codecs have been developed to use the properties of the Advanced Systems Format (ASF), which is the container used by Windows Media.</span></span> <span data-ttu-id="b56a5-109">由於 AVI 和 ASF 儲存內容的方式不同，因此將以 Windows Media 音訊和視頻編解碼器壓縮的內容儲存在 AVI 檔案中時，會發生一些問題。</span><span class="sxs-lookup"><span data-stu-id="b56a5-109">Because AVI and ASF store content differently, some difficulties arise when storing content compressed with the Windows Media Audio and Video codecs in an AVI file.</span></span>

<span data-ttu-id="b56a5-110">Windows Media 音訊編解碼器會壓縮音訊內容，使其無法正確解壓縮，而不會有個別樣本的時間戳記。</span><span class="sxs-lookup"><span data-stu-id="b56a5-110">The Windows Media Audio codecs compress audio content in such a way that it cannot be properly decompressed without time stamps for the individual samples.</span></span> <span data-ttu-id="b56a5-111">這可讓壓縮的媒體進行一些優化。</span><span class="sxs-lookup"><span data-stu-id="b56a5-111">This enables some optimization in the compressed media.</span></span> <span data-ttu-id="b56a5-112">因為 ASF 容器會將時間戳記與所有範例保持在一起，所以音訊演算法的這個特性一直都是正常運作。</span><span class="sxs-lookup"><span data-stu-id="b56a5-112">Because the ASF container keeps time stamps with all samples, this characteristic of the audio algorithms has always worked well.</span></span>

<span data-ttu-id="b56a5-113">不過，AVI 檔案並不會保留時間戳與範例。</span><span class="sxs-lookup"><span data-stu-id="b56a5-113">AVI files, however, do not keep time stamps with samples.</span></span> <span data-ttu-id="b56a5-114">這表示，當儲存在 AVI 檔案時，Windows Media 音訊內容無法正確解壓縮。</span><span class="sxs-lookup"><span data-stu-id="b56a5-114">This means that Windows Media Audio content cannot be decompressed properly when stored in an AVI file.</span></span> <span data-ttu-id="b56a5-115">Windows Media 視訊內容沒有此限制，而且可以包含在 AVI 檔案中。</span><span class="sxs-lookup"><span data-stu-id="b56a5-115">Windows Media Video content does not have this limitation, and can be included in AVI files.</span></span> <span data-ttu-id="b56a5-116">若要使用同步處理的音效將 Windows Media 視訊內容編碼為 AVI 檔案，您必須使用另一個音訊編解碼器。</span><span class="sxs-lookup"><span data-stu-id="b56a5-116">To encode Windows Media Video content to an AVI file with synchronized sound, you must use another audio codec.</span></span>

<span data-ttu-id="b56a5-117">使用 AVI 檔案作為 Windows Media 容器的另一個問題，就是使用低位速率的影片。</span><span class="sxs-lookup"><span data-stu-id="b56a5-117">The other issue with using an AVI file as a container for Windows Media concerns low-bit-rate video.</span></span> <span data-ttu-id="b56a5-118">Windows Media 視訊編解碼器為低位費率產生影片內容的其中一種方式，是卸載重複的畫面格。</span><span class="sxs-lookup"><span data-stu-id="b56a5-118">One of the ways in which the Windows Media Video codecs produce video content for low bit rates is by dropping duplicate frames.</span></span> <span data-ttu-id="b56a5-119">如果您想要將 Windows Media 視訊內容放在 ASF 檔案中，您需要設定編碼器，以提供重複畫面格的虛擬框架 (將 [MFPKEY \_ PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) 設定為 VARIANT \_ TRUE) ，以便在檔案中表示每個畫面格。</span><span class="sxs-lookup"><span data-stu-id="b56a5-119">If you want to put Windows Media Video content in an ASF file, you need to set the encoder to deliver dummy frames for duplicate frames (set [MFPKEY\_PRODUCEDUMMYFRAMES](mfpkey-producedummyframesproperty.md) to VARIANT\_TRUE) so that every frame is represented in the file.</span></span> <span data-ttu-id="b56a5-120">編解碼器所產生的虛擬框架大小為8個位元組。</span><span class="sxs-lookup"><span data-stu-id="b56a5-120">The dummy frames produced by the codec are 8 bytes in size.</span></span> <span data-ttu-id="b56a5-121">不過，AVI 多工器寫入檔案的框架可能會大為數百個位元組，並填滿亂數據。</span><span class="sxs-lookup"><span data-stu-id="b56a5-121">However, the frame written to file by the AVI multiplexer can be hundreds of bytes larger, and filled with random data.</span></span> <span data-ttu-id="b56a5-122">以這種方式建立的 AVI 檔案仍可供播放，但會比預期更大。</span><span class="sxs-lookup"><span data-stu-id="b56a5-122">An AVI file made in this way will still be playable, but it will be much larger than expected.</span></span> <span data-ttu-id="b56a5-123">您可以使用較高的位元速率來編碼儲存在 AVI 檔案中的影片，以避免這個問題。</span><span class="sxs-lookup"><span data-stu-id="b56a5-123">You can avoid this problem by using higher bit rates when encoding video for storage in AVI files.</span></span>

## <a name="related-topics"></a><span data-ttu-id="b56a5-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="b56a5-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b56a5-125">Windows Media 轉碼器</span><span class="sxs-lookup"><span data-stu-id="b56a5-125">Windows Media Codecs</span></span>](windows-media-codecs.md)
</dt> </dl>

 

 



