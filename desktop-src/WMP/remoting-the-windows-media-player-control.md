---
title: 遠端處理 Windows Media Player 控制項
description: 遠端處理 Windows Media Player 控制項
ms.assetid: d543b2a0-a2cb-47e2-b50e-4513fc061b46
keywords:
- Windows Media Player 嵌入 ActiveX 控制項
- Windows Media Player 物件模型，嵌入 ActiveX 控制項
- 物件模型，嵌入 ActiveX 控制項
- Windows Media Player 行動裝置，內嵌 ActiveX 控制項
- Windows Media Player ActiveX 控制項，內嵌
- Windows Media Player 的行動 ActiveX 控制項，內嵌
- ActiveX 控制項，嵌入
- Windows Media Player，遠端 ActiveX 控制項
- Windows Media Player 物件模型，遠端 ActiveX 控制項
- 物件模型、遠端處理 ActiveX 控制項
- Windows Media Player 行動裝置、遠端處理 ActiveX 控制項
- Windows Media Player ActiveX 控制項，遠端處理
- Windows Media Player 行動 ActiveX 控制項，遠端處理
- ActiveX 控制項，遠端處理
- 遠端 Windows Media Player ActiveX 控制項
- 內嵌、遠端處理 ActiveX 控制項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 615d3d31535abea098939af65ea67c13acbf8f6c
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023167"
---
# <a name="remoting-the-windows-media-player-control"></a>遠端處理 Windows Media Player 控制項

當您在 c + + 程式中內嵌 Windows Media Player 控制項時，您可以使用它做為播放程式完整模式的遠端延伸。 這稱為「遠端」 Windows Media Player 控制項，可讓您提供完整模式播放程式的所有功能，而不需自行執行。

當您從遠端控制時，它會與播放程式的完整模式共用相同的播放引擎，而您的使用者可以在內嵌模式 (「停駐」) 狀態時來回切換，而「停駐」狀態 (「未移動」狀態) 而數位媒體播放會繼續不中斷。

## <a name="enabling-remote-embedding"></a>啟用遠端內嵌

若要啟用 Windows Media Player 控制項的遠端內嵌，您的程式必須執行 **IServiceProvider** 和 [IWMPRemoteMediaServices](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpremotemediaservices) 介面。 **IServiceProvider** 是一種標準元件物件模型， (COM) 介面和單一方法，稱為 **QueryService**。 Windows Media Player 會呼叫這個方法，以取得 **IWMPRemoteMediaServices** 介面的指標。

**IWMPRemoteMediaServices** 有數個方法，但其中只有兩個是直接與遠端相關的。 在 [GetApplicationName](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getapplicationname)中，您會傳回程序的名稱，Windows Media Player 加入至 [ **View** ] 功能表上的 [其他程式清單] 中的 [**切換到其他程式** 清單]。 在 [GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype)中，您可以藉由傳回 "Remote" 或 "Local" 的值，來指出控制項的內嵌模式。 如果成功建立遠端連線， [IWMPPlayer4](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer4)介面的[get \_ isRemote](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_isremote)方法會傳回 true。

## <a name="specifying-an-exclusive-online-store"></a>指定專屬的線上商店

在 Windows Media Player 11 中，從遠端內嵌播放機控制項的應用程式可以指定專屬的線上商店。 在此情況下，會停用 Windows Media Player 中的服務選取器，而且只有指定的線上存放區可供使用者使用。 如需有關如何指定專屬線上商店的詳細資訊，請參閱 [專屬的線上商店](exclusive-online-stores.md)。

## <a name="docking-and-undocking"></a>銜接和移除

**IWMPPlayer4** 介面也會透過 [get \_ playerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayer4-get_playerapplication)方法提供 [IWMPPlayerApplication](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayerapplication)介面的存取權。 使用 **IWMPPlayerApplication** 在停駐和取消停駐狀態之間切換，以及決定影片或視覺效果顯示的目前停駐狀態和位置。

[IWMPPlayerApplication：： switchToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtoplayerapplication)方法會開啟 Windows Media Player 的完整模式，並將影片或視覺效果顯示傳送至 [**立即播放**] 窗格，以將控制項取消停靠。 [IWMPPlayerApplication：： switchToControl](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-switchtocontrol)方法會將影片或視覺效果顯示傳送至您的程式，並關閉播放程式的完整模式（如果已開啟），藉此將控制項停駐。 您也可以從 **切換至其他程式** 清單中選取程式，或藉由關閉播放程式的完整模式，來停駐控制項。 在這兩種情況下，任何現正播放的數位媒體都會繼續不中斷。

## <a name="transferring-the-video-or-visualization-display"></a>傳送影片或視覺效果顯示

當有多個具有內嵌、遠端 Windows Media Player 控制項的程式同時執行時，所有的控制項都會共用相同的播放引擎。 它們也會在未移除的狀態下，共用播放程式完整模式的相同實例。 不過，在停駐狀態中，只有一個控制項可以顯示影片或視覺效果。 在未移除的狀態下，只有播放程式的完整模式會顯示影片或視覺效果。 **SwitchToControl** 方法會在停駐和取消停駐的狀態中運作，並將影片或視覺效果顯示傳送給任何程式呼叫它。

停駐和取消停駐狀態之間的唯一差異，在於是否有 Windows Media Player 的完整模式，以及其影片或視覺效果顯示的擁有權。 在未停用的狀態中，所有目前執行中的內嵌、遠端控制仍會顯示，而且其使用者介面仍可完全正常運作。 但是，如果有影片或視覺效果視窗，則會是空的。 在停駐狀態中，只有一個內嵌的遠端控制項擁有顯示，但是所有的使用者介面仍繼續運作。

## <a name="hiding-or-changing-the-control-in-the-undocked-state"></a>隱藏或變更未移除狀態的控制項

如果您想要在未移除的狀態中隱藏或更改內嵌控制項的使用者介面，或是當程式未擁有顯示時，您必須提供自己的實作為。 當您停駐和取消停駐控制項時，您可以進行這些變更，也可以讓它們回應 Windows Media Player 的事件。 因為播放機可透過 [ **切換至其他程式** ] 功能表選項來停駐，所以通常最好提供這項功能來回應事件。

您可以針對 [SwitchedToPlayerApplication](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtoplayerapplication) 和 [SwitchedToControl](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-switchedtocontrol) 事件執行事件處理常式，也可以針對 [PlayerDockedStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerdockedstatechange) 事件執行單一事件處理常式。 在後者的情況下，您可以藉由呼叫 [IWMPPlayerApplication：： get \_ playerDocked](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_playerdocked)來判斷停駐的狀態。 在這兩種情況下，請使用 [IWMPPlayerApplication：： get \_ hasDisplay](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplayerapplication-get_hasdisplay) 來判斷您的程式是否擁有影片或視覺效果顯示。

## <a name="re-establishing-a-remote-connection"></a>重新建立遠端連線

在某些情況下，遠端、內嵌控制項和獨立播放機之間的連線將會失敗，並使您的 Windows Media Player 介面指標失效。 Windows Media Player 會自動嘗試重新連線，而且會引發 [PlayerReconnect](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents-playerreconnect) 事件以表示這次嘗試。 雖然重新連接是自動的，但如果您想要釋出不正確指標，並取得新的指標，讓您可以透過新的連接存取獨立的播放程式，則必須為此事件提供事件處理常式。

## <a name="controlling-the-undocked-player"></a>控制未移除的播放玩家

無論停駐的狀態為何，Windows Media Player 控制項的所有遠端實例都可以操作播放程式的完整模式。 但是，在停駐 Windows Media Player 控制項之前，將會忽略與播放程式完整模式沒有關聯的功能。 這包括 [IWMPPlayer](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplayer) 和衍生介面的屬性，例如 **enabled**、 **enableCoNtextMenu**、 **uiMode** 和 **windowlessVideo**。

## <a name="error-dialog-boxes"></a>錯誤對話方塊

從遠端 Windows Media Player 控制項實例， *設定*。**enableErrorDialogs** 屬性以特定方式運作。 適用的規則如下：

-   當 Windows Media Player 取消停駐時 (Windows Media Player UI 可見) ， **enableErrorDialogs** 屬性會被忽略，而播放程式會處理錯誤對話方塊。
-   當 Windows Media Player 停駐時， **enableErrorDialogs** 控制項的每個遠端實例所指定的值只會套用至個別控制項實例。 也就是說，如果特定控制項實例針對 **enableErrorDialogs** 指定 "true" 的值，則當控制項的所有其他實例都指定 "false" 值時，只有該實例會顯示對話方塊。

## <a name="remoting-in-the-background"></a>背景中的遠端處理

您應該避免在控制項未使用時，將播放程式的遠端實例保留在背景中執行。 由於「遠端播放機控制項」實例會以完整模式播放機共用其播放引擎，讓背景實例保持執行可能會導致非預期的行為。 例如，使用者可能會在檔案播放時關閉完整模式播放機。 使用者預期播放程式關閉時，檔案播放會完全停止，但因為播放引擎仍在使用中，所以音訊可能會繼續播放。

## <a name="samples"></a>範例

Windows Media Player SDK 安裝程式套件會安裝示範遠端處理的範例。 如需詳細資訊，請參閱 RemoteSkin 和 WMPML 範例。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**範例**](samples.md)
</dt> <dt>

[**在 c + + 程式中使用 Windows Media Player 控制項**](using-the-windows-media-player-control-in-a-c---program.md)
</dt> </dl>

 

 




