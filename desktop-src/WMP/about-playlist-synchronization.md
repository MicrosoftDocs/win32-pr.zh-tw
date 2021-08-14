---
title: 關於播放清單同步處理
description: 關於播放清單同步處理
ms.assetid: bc7d52e0-7906-4b5b-82e6-a84e9c4f0ff0
keywords:
- Windows Media Player，播放清單同步處理
- Windows Media Player 物件模型，播放清單同步處理
- 物件模型，播放清單同步處理
- Windows Media Player ActiveX 控制項、播放清單同步處理
- ActiveX 控制項，播放清單同步處理
- Windows Media PlayerMobile ActiveX 控制項，播放清單同步處理
- Windows Media Player行動、播放清單同步處理
- 同步處理裝置、播放清單
- 裝置同步處理，播放清單
- 播放清單，同步處理
- Windows媒體中繼檔播放清單，同步處理
- 中繼檔播放清單，同步處理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe54bef188fea2baee64da962dabf4eb8f700b72407772d591d73f52be2d4289
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119956868"
---
# <a name="about-playlist-synchronization"></a>關於播放清單同步處理

Windows Media Player 10 或更新版本是設計來使用播放清單同步處理模型，將數位媒體內容同步處理至裝置。 這表示預定要複製到裝置的內容必須是播放清單的一部分。 當使用者選擇將個人的數位媒體內容從電腦傳送到裝置時，Windows Media Player 會將內容新增至預設播放清單以供複製。

Windows Media Player 裝置同步處理 api 的設計，也像這樣。 如同 Windows Media Player，您的程式可以向使用者顯示其定義的播放清單清單。 然後，您可以讓使用者選擇要與特定裝置同步處理的播放清單，並設定同步處理常式的優先順序。

因為可攜式裝置的儲存容量有限，所以使用者可以選擇同步處理比裝置可儲存更多的數位媒體內容。 Windows Media Player 會以優先權順序同步處理內容。 使用者可以使用可從 [ **裝置** ] 功能存取的對話方塊來定義優先權順序。 若要回應使用者對您程式的輸入，您可以變更特定播放清單屬性的值，以程式設計方式變更優先順序順序。 這些屬性統稱為 *同步* 屬性。

媒體櫃中的每個播放清單都有16個同步處理屬性： **Sync01** 至 **Sync16**。 每個屬性都代表具有對應合作關係索引的裝置。 每個屬性的值會告訴您兩個事項：

-   是否應將播放清單與裝置同步處理。
-   播放清單的優先順序值。

值為零表示 Windows Media Player 不應嘗試與裝置同步播放播放清單。 任何其他值都是優先順序號碼。 較低的值在同步處理期間會獲得較高的優先順序。

播放清單也有 **>synconly** 屬性，指出播放清單是否僅適用于同步處理。

數位媒體內容的個別專案也包含同步處理的相關中繼資料。 當您從程式庫取出 **媒體** 物件時，您可以檢查 **SyncState** 屬性的值。 這個屬性會提供有關內容是否已成功複製到裝置的擴充資訊，或是因為無法容納內容而導致複製內容失敗的相關資訊。

> [!Note]  
> 您應該避免提供使用者介面元素，讓使用者能夠從所有程式庫內容建立播放清單，以進行同步處理。

 

為了優化效能，Windows Media Player 會強制執行一組規則來建立同步播放清單。 您的程式應該只針對您提供的內容建立同步播放清單。 允許 Windows Media Player 為使用者從其他來源新增至程式庫的內容建立同步播放清單。

除了建立您自己的播放清單使用者介面之外，您還可以使用預設對話方塊來顯示使用者，以選擇播放清單及管理裝置的合作關係。 若要這樣做，請呼叫 [IWMPSyncDevice：： showSettings](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-showsettings)。 當您叫用此方法時，Windows Media Player 會顯示它的 [同步處理設定] 對話方塊。 當使用者關閉對話方塊時，Windows Media Player 會自動回到先前的停駐狀態，並將控制權傳遞回您的遠端程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於裝置同步處理**](about-device-synchronization.md)
</dt> <dt>

[**管理同步播放清單**](managing-synchronization-playlists.md)
</dt> <dt>

[**播放清單屬性**](playlist-attributes.md)
</dt> </dl>

 

 




