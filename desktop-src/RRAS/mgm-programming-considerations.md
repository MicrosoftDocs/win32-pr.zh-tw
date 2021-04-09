---
title: MGM 程式設計考慮
description: 當您正在開發多播群組管理員用戶端時，請遵守下列指導方針
ms.assetid: 48451a76-81e0-4d60-acb3-c9ec55de32b4
keywords:
- 多播，程式設計考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e442de1dcb2da5a8664648587a88f05feaee970
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840388"
---
# <a name="mgm-programming-considerations"></a>MGM 程式設計考慮

當您正在開發多播群組管理員用戶端時，請遵守下列指導方針：

-   您必須在路由器進程內進行函式呼叫。 如果從另一個進程呼叫函數，其結果將無效;用戶端不會與多播群組管理員互動。
-   使用 MGM API 的用戶端必須提供自己的錯誤檢查，以確保只有有效的資料會傳遞至多播群組管理員。 MGM 函數不會傳回關於無效參數的詳細錯誤訊息;錯誤 \_ 不正確 \_ 參數值會傳回而不會有說明。
-   用戶端在呼叫 MGM 函式時，應謹慎使用鎖定。 這樣做可以防止鎖死。 呼叫 MGM 函式時，用戶端不應該保留任何可能同時在多播群組管理員回呼中保存的鎖定。

 

 




