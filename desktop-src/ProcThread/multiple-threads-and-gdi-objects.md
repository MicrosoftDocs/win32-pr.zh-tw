---
description: 為了增強效能，圖形裝置介面 (GDI) 物件 (例如，調色板、裝置內容、區域和類似的) 都不會序列化。
ms.assetid: aefb6a0b-ca00-4951-a173-8d7806b5d4e7
title: 多執行緒和 GDI 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3a17c7edcf32341eb9b1eaff3546fbe7be219b5f924a85d4a1db1d584a0a5922
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120032328"
---
# <a name="multiple-threads-and-gdi-objects"></a>多執行緒和 GDI 物件

為了增強效能，圖形裝置介面 (GDI) 物件 (例如，調色板、裝置內容、區域和類似的) 都不會序列化。 如果有多個執行緒共用這些物件的進程，這會造成潛在的危險。 例如，如果某個執行緒在另一個執行緒正在使用 GDI 物件時刪除該物件，則結果為無法預期的結果。 您可以避免這種危險，只是不共用 GDI 物件。 如果無法避免共用 (或希望) ，應用程式必須提供自己的機制來同步存取。 如需同步處理存取的詳細資訊，請參閱 [同步處理多執行緒的執行](synchronizing-execution-of-multiple-threads.md)。

 

 



