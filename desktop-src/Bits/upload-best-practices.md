---
title: 上傳最佳作法
description: Highloads 可能會導致各種伺服器超時狀況，而這可能會在用戶端重試時增加負載。
ms.assetid: 8210f849-2aae-497b-b5dd-af25f6f4b8bf
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b95a229ff1e229c41fde8fd377e347f91cf43010
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020895"
---
# <a name="upload-best-practices"></a>上傳最佳作法

Highloads 可能會導致各種伺服器超時狀況，而這可能會在用戶端重試時增加負載。 此外，大量未完成的連接將會耗用更多的伺服器資源，讓情況更糟。 最重要的是，如果後端應用程式未撰寫來處理高負載狀況，可能會損毀或不正確的行為。 應用程式應該執行下列步驟來限制後端的負載。

如果未撰寫伺服器應用程式來處理大量磁片區，則可能會發生 timeout 狀況，而這可能會在用戶端重試時增加負載。 此外，大量未完成的連接將會耗用更多的伺服器資源。

測試您的伺服器應用程式時，盡可能測試最高的負載。 您應使用多部用戶端電腦，每個都有數個並行的前景位作業，並測量後端的最大輸送量。 如果您無法測量輸送量，就必須估計輸送量。

伺服器應用程式應該位於與上傳 URL 不同的 URL (查看 BITS IIS 屬性 **BITSServerNotificationURL**) 。

最好的作法是根據經證實的輸送量值限制應用程式伺服器上的負載。 您應使用 IIS 屬性（ **MaxBandwidth** 和 **MaxConnections**）來限制應用程式伺服器上的負載。

 

 




