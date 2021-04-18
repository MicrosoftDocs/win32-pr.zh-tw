---
title: 專屬線上商店
description: 專屬線上商店
ms.assetid: f2b7f9a7-2299-48f4-b915-2c1a5e0d68bb
keywords:
- Windows Media Player 線上商店，獨家
- 線上商店，獨家
- 輸入1個線上商店，專屬
- 輸入2個線上商店，專屬
- 專屬線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f408a0ada0de46d637537ffccd3ec162da04e8ce
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "106965005"
---
# <a name="exclusive-online-stores"></a>專屬線上商店

在 Windows Media Player 11 中，從遠端內嵌播放機控制項的應用程式可以指定專屬的線上商店。 在此情況下，會停用 Windows Media Player 中的服務選取器，而且只有指定的線上存放區可供使用者使用。 此外，Windows Media Player 會採用專屬線上商店 ServiceInfo 檔的 **color** 元素所指定的色彩。

若要指定專屬的線上商店，應用程式必須將 ExclusiveService：*keyname* 附加至它從 [IWMPRemoteMediaServices：： GetServiceType](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpremotemediaservices-getservicetype)傳回的字串結尾。 例如，假設 Proseware 是指定給特定線上商店的索引鍵名稱。 如果 **GetServiceType** 傳回 "Remote ExclusiveService： Proseware" 字串，則 Proseware 將是遠端內嵌播放機控制項中唯一可用的線上商店。

只有當應用程式啟動時，如果 Windows Media Player 尚未執行，應用程式才可以將 Windows Media Player 限制為專屬的線上商店。 應用程式的責任是在執行應用程式之前，通知使用者必須關閉 Windows Media Player。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**Type 1 和 Type 2 線上商店的一般資訊**](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[**遠端處理 Windows Media Player 控制項**](remoting-the-windows-media-player-control.md)
</dt> </dl>

 

 




