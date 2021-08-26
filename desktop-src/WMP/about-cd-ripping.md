---
title: 關於 CD 翻錄
description: 關於 CD 翻錄
ms.assetid: 1a179284-2909-4fc0-82be-996794ee4f31
keywords:
- Windows Media Player、CD 翻錄
- Windows Media Player 物件模型，CD 翻錄
- 物件模型、CD 翻錄
- Windows Media Player ActiveX 控制項、CD 翻錄
- ActiveX 控制項，CD 翻錄
- Windows Media PlayerMobile ActiveX control、CD 翻錄
- Windows Media Player行動電話、CD 翻錄
- CD 翻錄，關於
- 翻錄 Cd、關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0efab14a97f9cc24c4137e5d939bc9562b1fc073cd551bd83388de4ba1de0b65
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903598"
---
# <a name="about-cd-ripping"></a>關於 CD 翻錄

Windows Media Player 11 SDK 引進了新功能，可將音訊曲目從 cd 複製到使用者的電腦。 此進程稱為「 *翻錄*」。

當您使用 Windows Media Player SDK 介面來翻錄音訊播放軌時，會使用使用者在 [Windows Media Player **選項**] 對話方塊中定義的設定來建立所產生的音樂曲目。

若要列舉使用者電腦上的 CD 磁片磁碟機，請使用 **IWMPCdromCollection** 介面。 您可以藉由呼叫 [IWMPCore：： get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)，來取得這個介面的指標。 藉由使用 **count** 和 **item** 方法，您可以逐一查看集合，以取得使用者電腦上每個 CD 光碟機的 **IWMPCdrom** 介面指標。 **IWMPCdrom** 介面代表個別的 CD 光碟機。 開始將 CD 翻錄之前，您必須先透過 **IWMPCdrom** 指標呼叫 **QueryInterface** ，以取得 **IWMPCdromRip** 介面的指標。

若要開始進行翻錄作業，只要呼叫 [IWMPCdromRip：： startRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-startrip)即可。 您可以定期呼叫 [IWMPCdromRip：： get \_ ripProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripprogress)來監視翻錄作業的進度。 這個方法會抓取整個翻錄作業的進度值。 抓取的值是表示完成的完成百分比的數位。 您可以定期呼叫 [IWMPCdromRip：： get \_ ripState](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-get_ripstate)來監視翻錄作業的狀態。 這個方法會抓取 [WMPRipState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpripstate) 列舉值，這個值表示作業正在進行中或已停止。 您也可以藉由處理 [IWMPEvents3：： CdromRipStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripstatechange) 事件，來監視「翻錄」作業的狀態。 請小心將事件) 所提供的 **IWMPCdromRip** 指標 (與代表您的翻錄作業的指標進行比較，以確保您的作業會引發事件。 您可以藉由呼叫 [IWMPCdromRip：： stopRip](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromrip-stoprip)來停止翻錄作業。

若要接收有關翻錄作業的錯誤通知，您可以處理 [IWMPEvents3：： CdromRipMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromripmediaerror) 事件。 如同 **CdromRipStateChange**，這個事件提供 **IWMPCdromRip** 介面指標，代表引發事件的翻錄作業。 此事件也會提供代表引發事件之媒體專案的 **IDispatch** 指標。 您可以透過這個指標呼叫 **QueryInterface** 來取出 **IWMPMedia** 指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Player 物件模型**](about-the-player-object-model.md)
</dt> </dl>

 

 




