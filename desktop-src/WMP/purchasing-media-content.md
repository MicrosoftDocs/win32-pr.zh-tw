---
title: 購買媒體內容
description: 購買媒體內容
ms.assetid: df4a3152-f9e3-4a97-b021-6d5e8de9c184
keywords:
- Windows Media Player 線上商店、購買媒體內容
- 線上商店、購買媒體內容
- 輸入1個線上商店、購買媒體內容
- Windows Media Player 線上商店、媒體內容購買
- 線上商店、媒體內容購買
- 輸入1個線上商店、媒體內容購買
- 媒體內容，購買
- 購買媒體內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e420f1dce607e1c596c48490d10bbe8a2a5a5f61
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "103932913"
---
# <a name="purchasing-media-content"></a>購買媒體內容

當 Windows Media Player 在文件庫樹狀檢視中顯示音樂內容時，使用者介面會包含使用者可以按一下以購買內容的元素。 例如，使用者可能會按一下按鈕來購買個別的歌曲，或購買整個專輯。

如果使用中的線上商店是類型1存放區，Windows Media Player 可以存取線上商店目錄中的追蹤、專輯和清單價格。 目錄中的價格是只有線上商店才能瞭解格式的字串。 Windows Media Player 不會解讀價格字串;它只會顯示在使用者介面專案中，例如購買按鈕。

當 Windows Media Player 設定一組媒體專案的購買專案時，它會呼叫 [IWMPContentPartner：： CanBuySilent](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-canbuysilent)，將媒體專案的識別碼和價格傳遞給內容合作夥伴外掛程式。 屆時，外掛程式可以檢查玩家所提供的價格。 這些是使用者預期支付的價格;也就是播放程式向使用者顯示的價格。 根據播放程式所提供的媒體識別碼和價格，外掛程式會計算總價格，並在 *bstrTotalPrice* 參數中返回播放程式。 播放程式傳遞給 **CanBuySilent** 的價格會提供外掛程式資訊，但不會商都必須外掛程式以傳回特定的總價。 外掛程式可以計算出合適的總價格。

除了計算購買的總價格之外， **CanBuySilent** 還會判斷 purchace 是否能以無訊息方式繼續進行;也就是說，不會顯示對話方塊。 如果 **CanBuySilent** 傳回 **True**，Windows Media Player 只會變更 [購買] 按鈕上的文字，以提示使用者確認購買。 如果 **CanBuySilent** 傳回 **False**，Windows Media Player 會顯示一個對話方塊，提示使用者確認購買。 對話方塊會提供使用者資訊，以摘要列出購買的資訊，例如專輯數量、個別曲目數目，以及外掛程式) 所傳回的總價格 (。

使用者確認購買之後，Player 會撥打 [IWMPContentPartner：：](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-buy)purchase。 這個方法呼叫會提供外掛程式與 **CanBuySilent** 相同的內容容器清單。 **通話時**，Windows Media Player 也會提供 cookie (單純的 **DWORD** 值，也就是可供外掛程式用來識別交易的會話) 唯一的。 當交易完成時，外掛程式必須呼叫 [IWMPContentPartnerCallback：： BuyComplete](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-buycomplete)，傳遞 *dwBuyCookie* 參數的原始 cookie 值，以通知播放程式交易已完成。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型1線上商店的程式設計指南**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




