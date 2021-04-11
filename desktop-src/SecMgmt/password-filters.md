---
description: 密碼篩選
ms.assetid: 777edb4d-1fb4-4269-8382-8fe73c0c3b23
title: 密碼篩選
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 14f76aad9bb2bb722fe7f84b13dc6b5a6bdb7eb0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194922"
---
# <a name="password-filters"></a>密碼篩選

密碼篩選器提供一種方式，讓您能夠執行密碼原則和變更通知。

進行密碼變更要求時，「 [*本地安全機構*](/windows/desktop/SecGloss/l-gly) 」 (LSA) 會呼叫在系統上註冊的密碼篩選。 每個密碼篩選器都會呼叫兩次：先驗證新密碼，然後在所有篩選準則驗證新密碼之後，通知篩選已進行變更。 下圖顯示這項程序。

![密碼變更要求](images/pswdfilte.png)

密碼變更通知是用來同步處理外部帳戶資料庫的密碼變更。

密碼篩選器用來強制執行密碼原則。 篩選準則會驗證新的密碼，並指出新的密碼是否符合已實行的密碼原則。

如需使用密碼篩選的總覽，請參閱 [使用密碼篩選器](using-password-filters.md)。

如需密碼篩選函數的清單，請參閱 [密碼篩選](management-functions.md)函式。

下列主題提供有關密碼篩選的詳細資訊：

-   [密碼篩選程式設計考慮](password-filter-programming-considerations.md)
-   [強式密碼強制執行和 Passfilt.dll](strong-password-enforcement-and-passfilt-dll.md)

 

 
