---
description: 本節說明網路封包 Exchange/Sequenced 封包 Exchange (IPX/SPX) 特有的 Winsock 擴充功能。 它也會描述基底 Winsock 函式的各個層面，這些函式需要特殊考慮或可能展現獨特的行為。
ms.assetid: 8447e063-767a-40b8-b094-724393e85be2
title: Winsock IPX/SPX 附錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 74e5a97b90dc29f577bf2335b93a15fb3fb2c87c8362e0585151e1ac8b1e3393
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051346"
---
# <a name="winsock-ipxspx-annex"></a>Winsock IPX/SPX 附錄

本節說明網路封包 Exchange/Sequenced 封包 Exchange (IPX/SPX) 特有的 Winsock 擴充功能。 它也會描述基底 Winsock 函式的各個層面，這些函式需要特殊考慮或可能展現獨特的行為。



| 元素          | 描述                                                                                                                                     |
|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| 通訊協定名稱 (s)  | IPX、SPX                                                                                                                                        |
| 描述      | 透過 IPX 網路層提供傳輸服務：適用于不可靠的資料包的 IPX、適用于可靠、以連接導向的訊息串流的 SPX。 |
| 位址系列   | AF \_ IPX                                                                                                                                         |
| 標頭檔      | Wsipx。h                                                                                                                                         |



 

本節討論如何使用 Winsock 搭配 IPX 的通訊協定系列，讓傳統的 IPX 應用程式可以移植到 Winsock。 IPX 網路的運作方式與 IP 網路本質上不同，因此使用 IPX/SPX 時必須考慮這類差異。

 

 



