---
title: 裝置一致性範本
description: 裝置一致性範本
ms.assetid: 5172ab39-819a-4d74-8e6e-b275b43f664c
keywords:
- Windows Media Format SDK，裝置一致性範本
- 編解碼器、裝置一致性範本
- 裝置一致性範本，關於
- 範本、裝置一致性範本
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6eccb88b372f9e0eb463d88db83d70102408a7a6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311276"
---
# <a name="device-conformance-templates"></a><span data-ttu-id="a110e-107">裝置一致性範本</span><span class="sxs-lookup"><span data-stu-id="a110e-107">Device Conformance Templates</span></span>

<span data-ttu-id="a110e-108">Windows Media 9 系列編解碼器支援裝置一致性範本，這些範本是串流設定設定和編解碼器演算法的定義範圍。</span><span class="sxs-lookup"><span data-stu-id="a110e-108">The Windows Media 9 Series codecs support device conformance templates, which are defined ranges of stream configuration settings and codec algorithms.</span></span> <span data-ttu-id="a110e-109">每個範本都會定義適用于特定裝置的值範圍。</span><span class="sxs-lookup"><span data-stu-id="a110e-109">Each template defines the ranges of values appropriate for certain devices.</span></span>

<span data-ttu-id="a110e-110">在過去，讓裝置能夠播放 ASF 檔案的硬體製造商，全都是以自己的標準運作。</span><span class="sxs-lookup"><span data-stu-id="a110e-110">In the past, the hardware manufacturers that made devices capable of playing ASF files were all working to their own standards.</span></span> <span data-ttu-id="a110e-111">如此一來，就能在今天繼續進行的類似裝置上產生範圍廣泛的功能。</span><span class="sxs-lookup"><span data-stu-id="a110e-111">This resulted in the widely disparate range of capabilities on similar devices that continues today.</span></span>

<span data-ttu-id="a110e-112">使用裝置一致性範本時，Windows Media 編解碼器會為類似的裝置建立通用的基礎。</span><span class="sxs-lookup"><span data-stu-id="a110e-112">With device conformance templates, the Windows Media codecs establish common ground for similar devices.</span></span> <span data-ttu-id="a110e-113">硬體製造商可以陳述裝置符合的範本，讓內容建立者更安心地鎖定其檔案以讀取裝置。</span><span class="sxs-lookup"><span data-stu-id="a110e-113">Hardware manufacturers can state which templates their devices conform to, enabling content creators to more confidently target their files to reading devices.</span></span> <span data-ttu-id="a110e-114">在嘗試播放檔案之前，播放程式應用程式可以更輕鬆地判斷檔案是否不適合裝置。</span><span class="sxs-lookup"><span data-stu-id="a110e-114">It is also easier for player applications to determine whether a file is inappropriate for the device before attempting to play it.</span></span>

<span data-ttu-id="a110e-115">裝置一致性範本會以字串來識別，該字串會儲存為與套用範本的資料流程相關聯的中繼資料屬性。</span><span class="sxs-lookup"><span data-stu-id="a110e-115">A device conformance template is identified by a string, which is stored as a metadata attribute associated with the stream to which the template applies.</span></span> <span data-ttu-id="a110e-116">如需範本和其字串和參數的清單，請參閱 [裝置一致性範本參數](device-conformance-template-parameters.md)。</span><span class="sxs-lookup"><span data-stu-id="a110e-116">For a list of the templates and their strings and parameters, see [Device Conformance Template Parameters](device-conformance-template-parameters.md).</span></span>

<span data-ttu-id="a110e-117">除了 Windows Media 視訊9螢幕編解碼器和 Windows Media 音訊9無失真編解碼器之外，所有 Windows Media 9 系列和更新版本的編解碼器都支援裝置一致性範本。</span><span class="sxs-lookup"><span data-stu-id="a110e-117">Device conformance templates are supported for all of the Windows Media 9 Series and later codecs except the Windows Media Video 9 Screen codec and the Windows Media Audio 9 Lossless codec.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a110e-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="a110e-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a110e-119">**編解碼器功能**</span><span class="sxs-lookup"><span data-stu-id="a110e-119">**Codec Features**</span></span>](codec-features.md)
</dt> <dt>

[<span data-ttu-id="a110e-120">**使用裝置一致性範本**</span><span class="sxs-lookup"><span data-stu-id="a110e-120">**Working with Device Conformance Templates**</span></span>](working-with-device-conformance-templates.md)
</dt> </dl>

 

 




