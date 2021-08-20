---
description: 群組參數
ms.assetid: 088156f7-fb75-4fcf-b928-87e97b13bdab
title: 群組參數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3083c3a7ad0971d6d3334303cf9eaf4c0313c4482825c3623a04a12ae046b665
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018366"
---
# <a name="grouping-parameters"></a>群組參數

群組參數會識別一組 [音訊會話](audio-sessions.md) ，這些會話全都由系統音量控制程式 Sndvol 中的單一音量控制所控制。 群組參數是 GUID，可唯一識別電腦範圍內的集合。

群組參數的用途類似于跨進程會話的會話 GUID。 也就是說，群組參數可讓使用者從任意數目的進程，以單一單位來控制資料流程的集合。 不過，在跨進程會話無法提供解決方案的情況下，群組參數會有此用途。

如果有數個用戶端將各自的串流指派給個別的會話，但指派相同的群組參數給所有會話，Sndvol 會顯示這些會話的單一磁片區控制項。 若要提供群組參數的支援，Sndvol 或任何類似的磁片區控制應用程式都必須執行下列動作：

-   在顯示磁片區控制項之前，請檢查所有使用中會話的群組參數。 將所有具有相同群組參數的會話組合在同一個磁片區下。
-   當使用者變更特定群組參數之磁片區控制項的設定時，請更新共用該群組參數之所有會話的磁片區層級。

群組參數有助於減少 Sndvol 所顯示的音量控制項數目。 如果 Sndvol clutters 顯示的控制項太多，使用者可能會混淆。 如果不支援群組參數，Sndvol 一律會針對每個會話顯示個別的音量控制項，這在所有情況下可能都不適用。 此外，群組參數提供便利的方式，以確保包含類似音訊內容類型的會話可以輕鬆地設定為相同的磁片區層級。

如先前所述，較高層級的音訊 Api 通常會將它們的串流指派給預設的進程特定會話， (由會話 GUID 值 GUID \_ Null) 識別。 此預設值可讓 Sndvol 針對每個用戶端應用程式進程顯示個別的音量控制項，這通常是想要的行為。 此外，如果同一個用戶端的多個實例在不同的進程中執行，但需要單一的共用磁片區控制，則用戶端可以直接將它們的串流指派給相同的跨進程會話。 這兩種情況都不需要使用群組參數。 不過，Microsoft Internet Explorer 所查詢示的一個重要案例，需要使用群組參數來達成所需的行為。

Internet Explorer 可讓使用者開啟多個瀏覽器視窗，而且這些視窗可能不會在相同的進程中執行。 如果 Sndvol 針對每個應用程式實例顯示個別的音量控制項，而且它們都有相同的標籤「Internet Explorer」，則使用者可能會混淆。 在此情況下，跨進程會話不是可行的解決方案。如果 Internet Explorer 的多個實例在不同的進程中執行，它們可能無法將其所有音訊串流指派給單一跨進程會話。 原因是 Internet Explorer 的 windows 可能正在執行 Windows Media Player 的實例，或其他使用較高層級音訊 API 來播放其音訊串流的多媒體外掛程式。 這些 Api 通常會將進程中的串流指派給預設的進程特定會話。 Internet Explorer 無法控制這些資料流程的指派給會話。

WASAPI 藉由啟用 Internet Explorer 的每個實例，以存取其預設、進程特定會話的會話控制項，以及將群組參數指派給該會話，來解決這個問題。 如果 Internet Explorer 的所有實例指派相同的群組參數給所有的音訊會話，Sndvol 就會顯示這些會話的單一音量控制。

依預設，會話不屬於任何群組。 如果用戶端未明確指派會話至群組，則 Sndvol 會顯示該會話的專用磁片區控制項。 群組參數值 GUID \_ Null 表示會話不屬於任何群組。 如果沒有用戶端明確指派會話的群組參數，則該會話的群組參數值預設為 GUID \_ Null。

用戶端可以動態變更指派給會話的群組。

群組可以包含 [音訊端點裝置](audio-endpoint-devices.md)上跨進程會話和進程特定會話的任何組合。

Sndvol 使用者介面可讓使用者一次只顯示一個音訊端點裝置的音量控制項。 當使用者調整特定裝置的音量控制項時，連接到其他裝置的會話音量層級不會受到影響。 尤其是，特定群組參數的磁片區控制項只會影響共用群組參數的會話，並連接到目前選取的裝置。 具有相同群組參數但連接至另一部裝置的會話不會受到影響。

如先前所述，Sndvol 會以顯示名稱和圖示來標記所顯示的每個磁片區控制項。 在群組的磁片區控制項的案例中，Sndvol 會任意選取群組中的其中一個會話，作為顯示名稱的來源，以及它與音量控制項一起顯示的圖示。 因此，為了確保 Sndvol 一律會顯示相同的群組顯示名稱和圖示，將會話指派給該群組的所有應用程式實例都應確定其各自的會話具有相同的顯示名稱和圖示。 如需有關顯示名稱和圖示的詳細資訊，請參閱 [音訊會話](audio-sessions.md)。

應用程式（例如 Sndvol）可以在會話的群組參數變更時註冊自己，以接收通知。 如果應用程式將會話指派的相關資訊快取到群組參數，這類通知可能很有用。 通知會通知應用程式，快取的資訊可能不再有效。

若要將群組參數指派給會話，請呼叫 [**IAudioSessionControl：： SetGroupingParam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-setgroupingparam) 方法。 若要取得指派給會話的群組參數，請呼叫 [**IAudioSessionControl：： GetGroupingParam**](/windows/desktop/api/Audiopolicy/nf-audiopolicy-iaudiosessioncontrol-getgroupingparam) 方法。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[音訊會話](audio-sessions.md)
</dt> </dl>

 

 



