---
title: 重新整理具有 PlaysForSure 標誌之商店的授權
description: 重新整理具有 PlaysForSure 標誌之商店的授權
ms.assetid: d08d6b6e-937e-4dec-b7ca-376cdad069f9
keywords:
- Windows Media Player 線上商店，重新整理授權
- 線上商店、授權重新整理
- Windows Media Player 線上商店、授權重新整理
- 線上商店，重新整理授權
- Windows Media Player 線上商店，PlaysForSure 標誌
- 線上商店，PlaysForSure 標誌
- 重新整理授權
- 授權，重新整理
- PlaysForSure
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42e48a3ddfd2b0670e3720f7c71587d0330a69a7
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/20/2020
ms.locfileid: "104092556"
---
# <a name="refreshing-licenses-for-stores-that-have-the-playsforsure-logo"></a>重新整理具有 PlaysForSure 標誌之商店的授權

某些線上音樂商店具有 PlaysForSure 標誌，但未與 Windows Media Player 11 整合。 這些存放區必須提供 ServiceInfo 檔和輕量元件，讓 Windows Media Player 11 可以取得並更新其內容的授權。

下列範例說明授權更新程式的運作方式。

1.  使用者從 Proseware online store 取得50音樂曲目。 每個曲目都是副檔名為 .wma 的檔案。 除了曲目之外，使用者還會取得用來播放曲目的授權。
2.  使用者將50軌複製到已安裝 Windows Media Player 11 的新電腦，並將這些曲目新增至 Windows Media Player 程式庫。
3.  在稍後的時間，授權重新整理模組 (LRM) （Windows Media Player 11 的一部分）會檢查50追蹤中的中繼資料，並判斷 Proseware 是否為內容提供者。
    > [!Note]  
    > Windows Media Player 可以藉由檢查媒體檔案中的 **ContentDistributor** 屬性來識別內容提供者。 如果有 PlaysForSure 標誌的線上商店提供的媒體檔案使用 Windows Media 數位 Rights Management (WMDRM) ，線上商店必須將 **ContentDistributor** 屬性放置在媒體檔案中。 如需詳細資訊，請參閱 Windows Media Player SDK 中的新增內容散發者屬性。

     

4.  LRM 會查閱 Proseware 的 ServiceInfo 檔的 URL、下載檔案，以及檢查檔的 **Install** 元素，以取得 LRM 可用於安裝 Proseware 元件的封裝 url。 LRM 會安裝並載入元件。
5.  針對每個50曲目，LRM 會呼叫 Proseware 元件的 [IWMPSubscriptionService：： allowPlay](/previous-versions/windows/desktop/api/subscriptionservices/nf-subscriptionservices-iwmpsubscriptionservice-allowplay) 方法。 **AllowPlay** 方法會在新電腦上放置個別曲目的授權，並在 *pfAllowPlay* 參數中傳回 **TRUE** 。
    > [!Note]  
    > Proseware 元件必須提供播放個別播放軌所需的所有授權。也就是說，元件必須提供根授權和分葉授權（如有需要）。

     

    在第一次呼叫 **allowPlay** 方法時，Proseware 元件必須顯示對話方塊，以確認目前的使用者具有 Proseware 帳戶，且具有播放播放軌的許可權。在後續呼叫 **allowPlay** 時，元件可以使用第一次呼叫中取得的認證，確認使用者有權播放其餘的曲目。

線上商店所撰寫的元件必須執行 **IWMPSubscriptionService** 介面的 **allowPlay** 方法。 元件必須 \_ 從其他三個方法傳回 E >notimpl： **allowCDBurn**、 **allowPDATransfer** 和 **startBackgroundProcessing**。 此外，元件還必須將 **功能** 登錄專案的值設為 1;也就是說， \_ \_ 必須設定訂用帳戶端點 ALLOWPLAY 功能旗標，且必須清除所有其他功能旗標。 如需註冊元件的詳細資訊，請參閱 [類型2線上商店的登錄機碼和專案](registry-keys-and-entries-for-a-type-2-online-store.md)。

如需建立可執行 **IWMPSubscriptionService** 介面之元件的詳細資訊，請參閱 [建立類型2線上商店的外掛程式](building-the-plug-in-for-a-type-2-online-store.md)。

如需提供 Microsoft ServiceInfo 檔的相關資訊，請將電子郵件傳送給 Windows Media Player 的虛擬服務小組。 小組的電子郵件地址為 mpsvctm@microsoft.com 。

如需使用各種 Windows Media Sdk 來建立提供授權數位媒體內容的服務的技術指引，請前往 [Microsoft Windows Media 開發人員中心](https://msdn.microsoft.com/windowsmedia/default.aspx) ，並搜尋「建立 Windows Media Player 10 訂閱線上商店」。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ServiceInfo 檔**](serviceinfo-document.md)
</dt> <dt>

[**Windows Media Player 線上商店**](windows-media-player-online-stores.md)
</dt> </dl>

 

 




