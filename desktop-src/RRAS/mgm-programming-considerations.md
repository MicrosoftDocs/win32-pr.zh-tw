---
title: MGM 程式設計考慮
description: 當您正在開發多播群組管理員用戶端時，請遵守下列指導方針
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- 多播，程式設計考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 76a749406384068cc7dce54fab237c261926149aaf9b2fbdca23327c7b75f3d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120029621"
---
# <a name="mgm-programming-considerations"></a>MGM 程式設計考慮

當您正在開發多播群組管理員用戶端時，請遵守下列指導方針：

-   您必須在路由器進程內進行函式呼叫。 如果從另一個進程呼叫函數，其結果將無效;用戶端不會與多播群組管理員互動。
-   使用 MGM API 的用戶端必須提供自己的錯誤檢查，以確保只有有效的資料會傳遞至多播群組管理員。 MGM 函數不會傳回關於無效參數的詳細錯誤訊息;錯誤 \_ 不正確 \_ 參數值會傳回而不會有說明。
-   用戶端在呼叫 MGM 函式時，應謹慎使用鎖定。 這樣做可以防止鎖死。 呼叫 MGM 函式時，用戶端不應該保留任何可能同時在多播群組管理員回呼中保存的鎖定。

 

 




