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
# <a name="audio-streams"></a>音訊串流

線上商店可從音樂伺服器以串流的形式提供音樂。 這適用于提供範例、特殊促銷專案，或讓訂用帳戶使用者無須下載內容即可享受音樂。 通常不會將資料流程的 URL 儲存為音樂目錄的一部分，而是在根據追蹤識別碼來播放之前，先解析 URL。 若要啟用這種情況，Windows Media Player 會呼叫 [IWMPContentPartner：： GetStreamingURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getstreamingurl) ，並提供串流類型 (作為 [WMPStreamingType](/previous-versions/windows/desktop/api/contentpartner/ne-contentpartner-wmpstreamingtype) 列舉值) 以及資料流程的識別碼。 外掛程式會透過 *pbstrURL* 參數傳回資料流程的 URL。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於類型1線上商店**](about-type-1-online-stores.md)
</dt> </dl>

 

 




