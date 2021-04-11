---
title: 音訊串流
description: 音訊串流
ms.assetid: 7bb39c48-5d0b-483d-83ee-946adfc9724f
keywords:
- Windows Media Player 線上商店、音訊串流
- 線上商店、音訊串流
- 輸入1個線上商店、音訊串流
- Windows Media Player 線上商店，來自音樂伺服器的串流
- 線上商店，來自音樂伺服器的串流
- 輸入1個線上商店、來自音樂伺服器的串流
- Windows Media Player 線上商店、音樂伺服器串流
- 線上商店、音樂伺服器串流
- 輸入1個線上商店、音樂伺服器串流
- 音訊串流
- 音樂伺服器串流
- 來自音樂伺服器的串流
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7164a703417e2efb8e32b2632890972957f7adf7
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023067"
---
# <a name="audio-streams"></a><span data-ttu-id="d068b-115">音訊串流</span><span class="sxs-lookup"><span data-stu-id="d068b-115">Audio Streams</span></span>

<span data-ttu-id="d068b-116">線上商店可從音樂伺服器以串流的形式提供音樂。</span><span class="sxs-lookup"><span data-stu-id="d068b-116">Online stores can provide music as a stream from a music server.</span></span> <span data-ttu-id="d068b-117">這適用于提供範例、特殊促銷專案，或讓訂用帳戶使用者無須下載內容即可享受音樂。</span><span class="sxs-lookup"><span data-stu-id="d068b-117">This is useful for providing samples, special promotional items, or to enable subscription users to enjoy music without having to download the content.</span></span> <span data-ttu-id="d068b-118">通常不會將資料流程的 URL 儲存為音樂目錄的一部分，而是在根據追蹤識別碼來播放之前，先解析 URL。</span><span class="sxs-lookup"><span data-stu-id="d068b-118">It is common not to store the URL of the stream as part of the music catalog, but instead to resolve the URL just before playback based upon the track ID.</span></span> <span data-ttu-id="d068b-119">若要啟用這種情況，Windows Media Player 會呼叫 [IWMPContentPartner：： GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) ，並提供串流類型 (作為 [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) 列舉值) 以及資料流程的識別碼。</span><span class="sxs-lookup"><span data-stu-id="d068b-119">To enable this, Windows Media Player calls [IWMPContentPartner::GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) and provides the streaming type (as a [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) enumeration value) and the ID for the stream.</span></span> <span data-ttu-id="d068b-120">外掛程式會透過 *pbstrURL* 參數傳回資料流程的 URL。</span><span class="sxs-lookup"><span data-stu-id="d068b-120">The plug-in returns the URL for the stream through the *pbstrURL* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d068b-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="d068b-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d068b-122">**關於類型1線上商店**</span><span class="sxs-lookup"><span data-stu-id="d068b-122">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




