---
title: 驗證層級
description: Microsoft RPC 提供多個層級的驗證。
ms.assetid: d9ed938e-4cd4-4355-8d08-830f955dd00c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c5fd25efb84b4ee2834e6f79c7fdd21dd903d55
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183456"
---
# <a name="authentication-levels"></a>驗證層級

Microsoft RPC 提供多個層級的驗證。 根據驗證層級而定，流量的來源 (傳送流量的安全性主體) 可在建立連線、用戶端啟動新的遠端程序呼叫，或在用戶端與伺服器之間的每個封包交換期間進行驗證。

即使流量的寄件者已通過驗證，但安全性仍是弱式，因為這類驗證並不確定封包未修改或損毀，而是路由;它只會驗證封包是否來自指定的主體。 為了提高安全性，分散式應用程式可以設定 RPC 執行時間程式庫，以確認未修改用戶端和伺服器之間交換的任何資料。 RPC 程式庫也可以在傳送每個封包之前加密其內容。 一般來說，想要保護其流量的應用程式應該只使用最後兩個層級：完整性和隱私權。

請注意，較高層級的驗證需要較高的計算負擔。 開發人員必須決定哪一個對您的應用程式來說更重要—速度或安全性。 大部分的開發人員會發現，有一些效能測試，它們可以達到可接受的效能層級，同時維持足夠的安全性。

分散式應用程式的用戶端和伺服器部分必須使用相同的驗證層級。 如需 RPC 驗證層級的清單，請參閱 [驗證層級常數](authentication-level-constants.md)。

 

 




