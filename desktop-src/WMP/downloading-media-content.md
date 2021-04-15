---
title: 下載媒體內容
description: 下載媒體內容
ms.assetid: 0a057e13-6e0c-4a8f-9cab-051183e6b222
keywords:
- Windows Media Player 線上商店下載媒體內容
- 線上商店，下載媒體內容
- 輸入1個線上商店，下載媒體內容
- Windows Media Player 線上商店、媒體內容下載
- 線上商店、媒體內容下載
- 輸入1個線上商店、媒體內容下載
- 媒體內容，下載
- 下載媒體內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00efe44f2bac25a9eeda86f6adcc78b34beea7cd
ms.sourcegitcommit: b04e152a7f51618fc174ffa872654623fe088db2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/21/2020
ms.locfileid: "104374777"
---
# <a name="downloading-media-content"></a><span data-ttu-id="9a19d-111">下載媒體內容</span><span class="sxs-lookup"><span data-stu-id="9a19d-111">Downloading Media Content</span></span>

<span data-ttu-id="9a19d-112">Windows Media Player 處理線上商店的音樂檔案下載。</span><span class="sxs-lookup"><span data-stu-id="9a19d-112">Windows Media Player handles music file downloads for the online store.</span></span> <span data-ttu-id="9a19d-113">當探索頁面呼叫外部時，可以起始下載 [。](external-download.md) 當使用者在播放程式中選擇時，可以下載一組曲目。</span><span class="sxs-lookup"><span data-stu-id="9a19d-113">A download can be initiated when the discovery page calls [External.download](external-download.md) or when the user chooses, in the Player, to download a set of tracks.</span></span> <span data-ttu-id="9a19d-114">無論是哪一種情況，Windows Media Player 都會呼叫 [IWMPContentPartner：:D 下載 o) ](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)，傳遞內容容器清單來描述要下載的一組曲目，以及代表下載交易的 cookie。</span><span class="sxs-lookup"><span data-stu-id="9a19d-114">In either case, Windows Media Player calls [IWMPContentPartner::Download](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download), passing a content container list that describes the set of tracks to be downloaded and a cookie that represents the download transaction.</span></span> <span data-ttu-id="9a19d-115">然後，內容合作夥伴外掛程式必須針對集合中的每個追蹤，呼叫 [IWMPContentPartnerCallback：:D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) 一次。</span><span class="sxs-lookup"><span data-stu-id="9a19d-115">The content partner plug-in must then call [IWMPContentPartnerCallback::DownloadTrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) once for each track in the set.</span></span> <span data-ttu-id="9a19d-116">當外掛程式呼叫 **DownloadTrack** 時，它會在 *hrDownload* 參數中傳遞 **HRESULT** 。</span><span class="sxs-lookup"><span data-stu-id="9a19d-116">When the plug-in calls **DownloadTrack**, it passes an **HRESULT** in the *hrDownload* parameter.</span></span> <span data-ttu-id="9a19d-117">如果外掛程式在 *hrDownload* 中傳遞了成功的程式碼，Windows Media Player 會下載該曲目。如果外掛程式在 *hrDownload* 中傳遞失敗碼，播放程式就不會下載曲目。針對每個要 **下載** 的呼叫，外掛程式都必須提供交易 cookie 和有問題之追蹤的識別碼。</span><span class="sxs-lookup"><span data-stu-id="9a19d-117">If the plug-in passes a success code in *hrDownload*, Windows Media Player downloads the track. If the plug-in passes a failure code in *hrDownload*, the Player does not download the track. For each call to **Download**, the plug-in must supply the transaction cookie and the ID of the track in question.</span></span> <span data-ttu-id="9a19d-118">針對將會實際下載的曲目，此外掛程式也必須提供該播放軌的 URL。</span><span class="sxs-lookup"><span data-stu-id="9a19d-118">For tracks that will actually be downloaded, the plug-in must also supply the URL of the track.</span></span>

<span data-ttu-id="9a19d-119">下載檔案之後，Windows Media Player 會自動更新程式庫，以反映新購買的音樂。</span><span class="sxs-lookup"><span data-stu-id="9a19d-119">After a file is downloaded, Windows Media Player automatically updates the library to reflect the newly purchased music.</span></span> <span data-ttu-id="9a19d-120">播放程式會藉由呼叫 [IWMPContentPartner：:D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete)，提供有關下載作業之外掛程式的狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="9a19d-120">The Player provides status information to the plug-in about the download operation by calling [IWMPContentPartner::DownloadTrackComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete).</span></span> <span data-ttu-id="9a19d-121">在這個方法中，播放程式會提供 **HRESULT** ，指出下載的成功或失敗、追蹤識別碼，以及線上商店在呼叫 **DownloadTrack** 時所提供的自訂參數字串。</span><span class="sxs-lookup"><span data-stu-id="9a19d-121">In this method, the Player provides an **HRESULT** to indicate success or failure of the download, the track ID, and the custom parameters string that the online store provided when it called **DownloadTrack**.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9a19d-122">相關主題</span><span class="sxs-lookup"><span data-stu-id="9a19d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9a19d-123">**類型1線上商店的程式設計指南**</span><span class="sxs-lookup"><span data-stu-id="9a19d-123">**Programming Guide for Type 1 Online Stores**</span></span>](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




