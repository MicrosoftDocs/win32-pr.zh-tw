---
description: 您可以透過兩種方式從封包中解壓縮檔案。 第一個最簡單的方式是利用內建于安裝函式的自動封包處理。
ms.assetid: 113333c8-28d1-4b0e-8da4-0c94389d8038
title: 從封包解壓縮檔案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfd7f41d4951e43bb58fac6efb9b1fd11895373398643e7c8c9cc00821dd72d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118887249"
---
# <a name="extracting-files-from-cabinets"></a>從封包解壓縮檔案

您可以透過兩種方式從封包中解壓縮檔案。 第一個最簡單的方式是利用內建于安裝函式的自動封包處理。

安裝功能（例如 [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)、 [**SetupInstallFile**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfilea)和 [**SetupInstallFromInfSection**](/windows/desktop/api/Setupapi/nf-setupapi-setupinstallfrominfsectiona)）會檢查每個檔案的壓縮。 如果檔案位於封包中，則函式會先在封包外搜尋該名稱的檔案。 如果找到，則函式會安裝外部檔案，並忽略封包內的檔案。 這可讓您更新封包內的單一檔案，而不需要重建封包。

安裝函式也會追蹤封包中的哪些檔案已被抓取，因此檔案只會解壓縮一次，即使已安裝多次。

從封包解壓縮檔案的第二種方式是使用 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta)。 此函式會逐一查看封包中的每個檔案，將通知傳送給找到的每個檔案的回呼常式。 回呼常式接著會傳回值，指出是否應該解壓縮或略過檔案。

> [!Note]  
> 安裝程式 API 不提供預設回呼常式來處理封包通知。 如果您明確地呼叫 [**SetupIterateCabinet**](/windows/desktop/api/Setupapi/nf-setupapi-setupiteratecabineta) ，您必須提供回呼常式來處理函式傳回的封包通知。

 

 

 



