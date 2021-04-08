---
title: BITS 要求封包
description: BITS 要求封包
ms.assetid: 4d8fd5f3-7621-438f-926f-38ece7a52f52
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6738f77477342f1329818ae7c2ffb5c010b074c3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931963"
---
# <a name="bits-request-packets"></a>BITS 要求封包

要求封包會描述用戶端要求。 在任何指定的時間，都只能有一個未處理的要求;傳送另一個要求之前，您必須先從伺服器接收目前要求的 [Ack](bits-response-packets.md) 。

下表列出針對上傳和上傳-回復作業傳送至 BITS 伺服器的要求封包。 資料表會列出傳送至伺服器的一般順序中的封包。



| 要求封包                       | 目的                                                                                                                                                        |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [坪](ping.md)                     | 建立連接並與伺服器協商安全性。                                                                                              |
| [建立-會話](create-session.md) | 要求 BITS 伺服器的上傳會話。                                                                                                               |
| [片段](fragment.md)             | 將檔案的片段傳送至 BITS 伺服器。 傳送的片段要求數目取決於您所選擇的片段大小和上傳檔案的大小。 |
| [關閉會話](close-session.md)   | 結束與 BITS 伺服器的檔案上傳會話。                                                                                                             |
| [取消-會話](cancel-session.md) | 結束與 BITS 伺服器的檔案上傳會話。 一般而言，如果使用者取消作業，您會傳送 Cancel-Session 封包。                                 |



 

Ping 封包是選擇性的。 您可以使用 Create-Session 封包來建立連線並協商安全性，而不是傳送 Ping 封包。 不過，針對此目的使用 Ping 封包較有效率。

 

 




