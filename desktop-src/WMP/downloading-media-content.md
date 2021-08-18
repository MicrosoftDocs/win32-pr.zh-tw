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
ms.openlocfilehash: 6a314dc4b59966fd779660a2c1ab26fc2b37d413e4add068f936a6109acd423a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997028"
---
# <a name="downloading-media-content"></a>下載媒體內容

Windows Media Player 處理線上商店的音樂檔案下載。 當探索頁面呼叫外部時，可以起始下載 [。](external-download.md) 當使用者在播放程式中選擇時，可以下載一組曲目。 無論是哪一種情況，Windows Media Player 都會呼叫[IWMPContentPartner：:D 下載 o) ](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-download)，傳遞內容容器清單來描述要下載的一組曲目，以及代表下載交易的 cookie。 然後，內容合作夥伴外掛程式必須針對集合中的每個追蹤，呼叫 [IWMPContentPartnerCallback：:D ownloadtrack](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-downloadtrack) 一次。 當外掛程式呼叫 **DownloadTrack** 時，它會在 *hrDownload* 參數中傳遞 **HRESULT** 。 如果外掛程式在 *hrDownload* 中傳遞了成功的程式碼，Windows Media Player 會下載該曲目。如果外掛程式在 *hrDownload* 中傳遞失敗碼，播放程式就不會下載曲目。針對每個要 **下載** 的呼叫，外掛程式都必須提供交易 cookie 和有問題之追蹤的識別碼。 針對將會實際下載的曲目，此外掛程式也必須提供該播放軌的 URL。

下載檔案之後，Windows Media Player 會自動更新程式庫，以反映新購買的音樂。 播放程式會藉由呼叫 [IWMPContentPartner：:D ownloadtrackcomplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-downloadtrackcomplete)，提供有關下載作業之外掛程式的狀態資訊。 在這個方法中，播放程式會提供 **HRESULT** ，指出下載的成功或失敗、追蹤識別碼，以及線上商店在呼叫 **DownloadTrack** 時所提供的自訂參數字串。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型1線上商店的程式設計指南**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




