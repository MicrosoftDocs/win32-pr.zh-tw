---
title: 持續性物件狀態
description: 持續性物件狀態
ms.assetid: 731fef03-d204-48e7-b33a-801e97a9d2c2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c08d4dd1175b5a7681f79fa9049772af245a031
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300368"
---
# <a name="persistent-object-state"></a>持續性物件狀態

某些 COM 物件可能會在用戶端要求您這麼做時，儲存其內部狀態。

COM 會定義標準，讓用戶端可以要求將物件初始化、載入及儲存至資料存放區， (例如一般檔案、結構化儲存體或記憶體) 。 用戶端負責管理物件的持續性資料的儲存位置，而非資料的格式。 遵守這些標準的 COM 物件稱為持續性 *物件*。

如需詳細資訊，請參閱下列主題：

-   [持續性物件介面](persistent-object-interfaces.md)
-   [初始化持續性物件](initializing-persistent-objects.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM 用戶端和伺服器](com-clients-and-servers.md)
</dt> </dl>

 

 




