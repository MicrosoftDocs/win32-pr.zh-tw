---
description: 在其他情況下，可以使用少於所要求的字元數來完成讀取或寫入作業，即使尚未發生超時時間也一樣。
ms.assetid: 05f84661-34ff-4e1f-9ec8-e4682138dfee
title: 通訊錯誤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e946d5cb97122c35a5ec09978508e86724290307e514576482f535b1f3493418
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119874588"
---
# <a name="communications-errors"></a>通訊錯誤

在其他情況下，可以使用少於所要求的字元數來完成讀取或寫入作業，即使尚未發生超時時間也一樣。 下列是一些範例：

-   有些驅動程式支援使用特殊字元，這項作業會立即完成讀取作業，只使用收到的字元數。
-   您可以呼叫 [**PurgeComm**](/windows/desktop/api/Winbase/nf-winbase-purgecomm) 函數，以提前終止暫止的讀取或寫入作業。 此函數也可以刪除輸出或輸入緩衝區的內容，或兩者。
-   如果在讀取或寫入作業期間發生通訊錯誤，則會終止通訊資源上的所有 i/o 作業。 中斷條件、同位檢查錯誤或框架錯誤都是這類錯誤的範例。 發生錯誤時，處理常式必須呼叫 [**ClearCommError**](/windows/desktop/api/Winbase/nf-winbase-clearcommerror) 函式來清除錯誤旗標，然後才能開始其他 i/o 作業。 **ClearCommError** 會報告發生的特定錯誤，以及裝置的目前狀態。

 

 



