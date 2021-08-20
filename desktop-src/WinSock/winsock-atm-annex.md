---
description: ATM 適用于 LAN 和 WAN 環境。
ms.assetid: 532a876c-9b31-410e-9331-5e8aa98ccaee
title: Winsock ATM 附錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f55c71b830fa8a5f27f083af0263c62766e7b037e433c04b73bfea5ba12960
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118822444"
---
# <a name="winsock-atm-annex"></a>Winsock ATM 附錄

ATM 適用于 LAN 和 WAN 環境。 ATM 網路同時傳輸了各式各樣的網路流量，包括語音、資料、影像和影片。 它會在每個虛擬通道上為使用者提供保證的服務品質 (VC) 基礎。



| 元素          | 描述                                                                                                                                                 |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 通訊協定名稱 (s)  | ATMPROTO \_ AAL5、ATMPROTO \_ AALUSER                                                                                                                           |
| 描述      | ATM AAL5 會提供以連接為導向的傳輸服務、保留的訊息界限，以及保證的 QOS。 ATMPROTO \_ AALUSER 是使用者定義的 AAL。 |
| 位址系列   | AF \_ ATM                                                                                                                                                     |
| 標頭檔      | Ws2atm。h                                                                                                                                                    |



 

本節說明 (ATM) 專屬延伸模組所需的非同步傳輸模式，以支援在 ATM 論壇使用者網路介面中公開和指定的原生 ATM 服務 (單一) 規格版本 3.x (3.0 和 3.1) 。 本檔支援 AAL 類型 5 (訊息模式) 和使用者定義 AAL。 本檔的未來版本將支援其他類型的 AAL 以及單向4.0。

 

 



