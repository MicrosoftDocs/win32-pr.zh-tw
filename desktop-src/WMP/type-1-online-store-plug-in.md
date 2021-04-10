---
title: 輸入1線上商店外掛程式
description: 輸入1線上商店外掛程式
ms.assetid: 3aa74282-522b-4240-8d72-73bd3015abeb
keywords:
- Windows Media Player 線上商店、外掛程式
- 線上商店、外掛程式
- 輸入1個線上商店、外掛程式
- Windows Media Player 線上商店、IWMPContentPartner 介面
- 線上商店、IWMPContentPartner 介面
- 輸入1個線上商店、IWMPContentPartner 介面
- 外掛程式，Windows Media Player 線上商店
- 外掛程式，線上商店
- 外掛程式，請輸入1個線上商店
- 外掛程式，IWMPContentPartner 介面
- Windows Media Player 外掛程式，請輸入1個線上商店
- Windows Media Player 外掛程式，線上商店
- Windows Media Player 外掛程式，Windows Media Player 線上商店
- Windows Media Player 外掛程式、IWMPContentPartner 介面
- IWMPContentPartner
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fe42095d08262520734603a5418ac6831ce6685
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/25/2020
ms.locfileid: "104023176"
---
# <a name="type-1-online-store-plug-in"></a>輸入1線上商店外掛程式

若要利用程式庫整合功能，請輸入1線上商店提供者必須建立可執行 [IWMPContentPartner](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner) 介面的外掛程式。 這個介面會提供 Windows Media Player 呼叫的方法，以通知線上商店有關播放程式中發生的活動，以及抓取有關線上商店內容、目錄或商店本身的特定資訊。

在 Windows Media Player 具現化外掛程式之後，Player 會呼叫 [IWMPContentPartner：： SetCallback](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-setcallback)，並提供 **IWMPContentPartnerCallback** 介面的指標。 此介面可讓線上商店利用方法來呼叫 Windows Media Player，以提供狀態資訊或起始特定進程，例如下載音樂播放軌。

Windows Media Player 和外掛程式是在不同的進程中執行。 外掛程式是在預設 DLL 代理 dllhost.exe 中執行的同進程伺服器。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於類型1線上商店**](about-type-1-online-stores.md)
</dt> <dt>

[**IWMPContentPartner 介面**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)
</dt> <dt>

[**IWMPContentPartnerCallback 介面**](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)
</dt> </dl>

 

 




