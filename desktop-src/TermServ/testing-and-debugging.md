---
title: 測試和偵錯
description: 有 \ 0034; echo \ 0034;由遠端桌面連線 (RDC) 用戶端所執行的接聽程式，一律存在並接聽連入連線。
ms.assetid: ae14af04-7d19-406b-998e-a0579cfe73eb
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d9028ccf0eea97a8651392baba094ac6dcda242f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965564"
---
# <a name="testing-and-debugging"></a>測試和偵錯

有一個由遠端桌面連線 (RDC) 用戶端所執行的「echo」接聽程式，其一律存在並接聽連入連線。 當您撰寫動態虛擬通道的伺服器端 (DVC) 模組時，若要快速測試，您可以開啟名為 "ECHO" 的端點。 從這個端點具現化之通道的任何寫入，都會導致收到相同的資料。

您可以使用這項技術來測試伺服器端模組的輸入/輸出 (i/o) 執行、測量遠端桌面連線 (RDC) 用戶端外掛程式的回應時間，或測量遠端桌面連線 (RDC) 用戶端的網路延遲。 可透過此通道傳送的資料量沒有任何限制。

 

 




