---
title: 關於 CD 燒錄
description: 關於 CD 燒錄
ms.assetid: 1ecc73ed-c49d-4190-baa9-93162f075a4c
keywords:
- Windows Media Player、CD 燒錄
- Windows Media Player 物件模型，CD 燒錄
- 物件模型，CD 燒錄
- Windows Media Player ActiveX 控制項、CD 燒錄
- ActiveX 控制項，CD 燒錄
- Windows Media PlayerMobile ActiveX control、CD 燒錄
- Windows Media Player行動電話、CD 燒錄
- CD 燒錄，關於
- 燒錄 Cd，關於
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c784765a09b601da2f0ec75434a37f55a75ff7e6ab6d737f7912daab8f197c07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119957138"
---
# <a name="about-cd-burning"></a>關於 CD 燒錄

Windows Media Player 11 SDK 引進了建立 cd 的新功能。 此進程稱為「 *燒錄*」。

若要列舉使用者電腦上的 CD 磁片磁碟機，請使用 **IWMPCdromCollection** 介面。 您可以藉由呼叫 [IWMPCore：： get \_ cdromCollection](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcore-get_cdromcollection)，來取得這個介面的指標。 藉由使用 **count** 和 **item** 方法，您可以逐一查看集合，以取得使用者電腦上每個 CD 光碟機的 **IWMPCdrom** 介面指標。 **IWMPCdrom** 介面代表個別的 CD 光碟機。

開始燒錄 CD 之前，您必須先透過 **IWMPCdrom** 指標呼叫 **QueryInterface** ，以取得 **IWMPCdromBurn** 介面的指標。 藉由使用 **isAvailable** 方法，您可以判斷特定的 cd 光碟機是否可以燒錄 cd、磁片磁碟機中是否有光碟片，以及如何使用 cd。

若要指定要燒錄到 CD 的專案，您必須建立播放清單。 Windows Media Player 使用 **IWMPPlaylist** 介面表示播放清單。 您可以用任何想要的方式建立此播放清單。 例如，您可以藉由呼叫 [IWMPMediaCollection：： getByAlbum](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpmediacollection-getbyalbum)，直接從程式庫取出播放清單。 建立要燒錄到 CD 的播放清單之後，您必須呼叫 [IWMPCdromBurn：:p \_ burnPlaylist](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnplaylist) 方法，並將播放清單指標當作引數傳遞。 這會將您的播放清單設定為 Windows Media Player 將複製到 CD 的播放清單。

如果您從媒體櫃取出播放清單，則對播放清單所做的任何變更都會反映在使用者的程式庫中。 若要避免這種情況，請呼叫 [IWMPPlaylist：： setItemInfo](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpplaylist-setiteminfo)，並傳遞屬性名稱 "暫時性" 和值 "true"。 這會將您的播放清單實例轉換成暫時播放清單，而不需要變更原始播放清單即可進行編輯。

每次您設定要燒錄的新播放清單，或對現有的燒錄播放清單進行變更時，都必須呼叫 [IWMPCdromBurn：： refreshStatus](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-refreshstatus) 來更新狀態資訊。 這可確保 Windows Media Player 會執行必要的處理，以提供正確的 CD 燒錄操作狀態資訊。

若要指定要燒錄的 CD 類型，請呼叫 [IWMPCdromBurn：:p 的 \_ burnFormat](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_burnformat)。 Windows Media Player 可讓您燒錄兩種類型的 cd：音訊 cd 和資料 cd。 [WMPBurnFormat](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnformat)列舉會定義 CD 類型。

您可以藉由呼叫 [IWMPCdromBurn：:p 內容卷 \_ 標](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-put_label)來指定 CD 的磁片區標籤。

當您準備好開始燒錄 CD 時，請呼叫 [IWMPCdromBurn：： startBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-startburn)。 您可以定期呼叫 [IWMPCdromBurn：： get \_ burnProgress](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-get_burnprogress)來監視燒錄作業的進度。 這個方法會抓取整個燒錄作業的進度值。 抓取的值是代表燒錄完成百分比的數位。 您可以藉由處理 [IWMPEvents3：： CdromBurnStateChange](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnstatechange) 事件來監視燒錄作業的狀態，它會使用 [WMPBurnState](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpburnstate) 列舉來指出目前的狀態。 您應該小心將事件) 所提供的 **IWMPCdromBurn** 指標 (與代表您的燒錄作業的指標進行比較，以確保您的作業會引發事件。 您可以藉由呼叫 [IWMPCdromBurn：： stopBurn](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpcdromburn-stopburn)來停止燒錄操作。

您可以處理兩個事件，以接收有關燒錄作業的錯誤通知。 發生泛型錯誤時，就會引發 [IWMPEvents3：： CdromBurnError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnerror) 事件。 當特定媒體專案在燒錄期間造成錯誤時，就會引發[IWMPEvents3：： CdromBurnMediaError](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpevents3-cdromburnmediaerror) 。 如同 **CdromBurnStateChange** 事件，每個事件都提供 **IWMPCdromBurn** 指標，代表引發事件的燒錄作業。 **CdromBurnMediaError** 事件提供代表引發事件之媒體專案的 **IDispatch** 指標。 您可以透過這個指標呼叫 **QueryInterface** 來取出 **IWMPMedia** 指標。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Player 物件模型**](about-the-player-object-model.md)
</dt> <dt>

[**IWMPCdrom 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdrom)
</dt> <dt>

[**IWMPCdromBurn 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromburn)
</dt> <dt>

[**IWMPCdromCollection 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpcdromcollection)
</dt> <dt>

[**IWMPEvents3 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents3)
</dt> <dt>

[**IWMPMedia 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpmedia)
</dt> <dt>

[**IWMPPlaylist 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpplaylist)
</dt> <dt>

[**暫存屬性**](temporary-attribute.md)
</dt> </dl>

 

 




