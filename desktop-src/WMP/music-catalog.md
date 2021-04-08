---
title: 音樂類別目錄
description: 音樂類別目錄
ms.assetid: d7ebf37f-00ae-4978-a63d-9d13741724f5
keywords:
- Windows Media Player 線上商店、音樂目錄
- 線上商店、音樂目錄
- 輸入1個線上商店、音樂目錄
- Windows Media Player 線上商店，目錄編譯器
- 線上商店，目錄編譯器
- 輸入1個線上商店、目錄編譯器
- 音樂目錄
- 目錄編譯器
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479a74393ee4d853f591cb6d75eef8be741c9228
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023012"
---
# <a name="music-catalog"></a>音樂類別目錄

類型1線上商店會以一組定位鍵分隔值 (TSV) 檔案來建立其音樂目錄。 然後，線上商店會使用 Microsoft 的 [目錄](catalog-compiler-for-type-1-online-stores.md) 編譯器將 TSV 檔案編譯成可 Windows Media Player 下載的壓縮類別目錄。 Windows Media Player 可以下載完整的類別目錄檔案或目錄更新檔案。 目錄更新只包含上次目錄更新之後變更的目錄資訊。 由內容合作夥伴外掛程式決定是否要下載完整目錄或更新。 無論是哪一種情況，Windows Media Player 都會在來自外掛程式的通知時，將變更套用至目前的目錄。

如果線上商店已備妥新的目錄，此外掛程式可以藉由呼叫 [IWMPContentPartnerCallback：： notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify) 並傳遞 wmpcnNewCatalogAvailable 作為 *型* 別參數的值，來通知玩家。

當 Windows Media Player 準備好下載目錄或更新時，播放程式會呼叫 [IWMPContentPartner：： GetCatalogURL](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcatalogurl)。 這個方法會將目前目錄的相關資訊提供給外掛程式，例如目錄版本和地區設定識別碼。 外掛程式的回應方式是提供統一資源定位器 (URL) 正確的完整目錄或更新，以及更新的版本號碼和到期日。 Windows Media Player 會根據外掛程式在 **GetCatalogURL** 中提供的資訊，定期要求類別目錄更新。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於類型1線上商店**](about-type-1-online-stores.md)
</dt> <dt>

[**類型1線上商店的目錄編譯器**](catalog-compiler-for-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentPartner 介面**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> </dl>

 

 




