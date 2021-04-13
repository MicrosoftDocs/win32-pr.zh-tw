---
description: 當系統提示使用者提供登入資訊時，驗證是互動式的。 當使用者透過 GINA 使用者介面登入時， (LSA) 的「本地安全機構」會執行互動式驗證。
ms.assetid: 86a318fa-4d7c-4191-a309-d25b492dd915
title: 互動式驗證
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: afeb09044f4b34f28c02cd0f03b3358a8158af65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320200"
---
# <a name="interactive-authentication"></a>互動式驗證

當系統提示使用者提供登入資訊時，驗證是互動式的。 當使用者透過 [*GINA*](../secgloss/g-gly.md)使用者介面登入時， (LSA) 的「[*本地安全機構*](../secgloss/l-gly.md)」會執行互動式驗證。 下圖顯示一般互動式驗證的部分。

![互動式驗證](images/lsaint3.png)

使用者將 CTRL + ALT + DEL [*安全的注意順序*](../secgloss/s-gly.md) 輸入 (SAS) ，以通知系統開始登入順序。 [*Winlogon*](../secgloss/w-gly.md) 會接收 SAS 並呼叫 GINA，以顯示使用者介面並取得使用者的登入資料，例如使用者名稱和密碼。

取得登入資料之後，GINA 會呼叫 [**LsaLogonUser**](/windows/desktop/api/Ntsecapi/nf-ntsecapi-lsalogonuser) 函式來驗證使用者，指定必須使用哪個驗證套件來評估登入資料。

LSA 會呼叫指定的驗證套件，並將登入資料傳遞給它。 驗證套件會檢查資料，並判斷驗證是否成功。 驗證結果會從 lsa 傳回至 GINA。

GINA 會顯示使用者驗證成功或失敗，並將驗證的結果傳回給 Winlogon。 如果驗證成功，使用者的登入會話就會開始，並儲存一組登入 [*認證*](../secgloss/c-gly.md) 以供日後參考。

> [!Note]  
> 一般而言，撰寫自訂 GINA 以接受特殊登入資料的開發人員（例如 [*智慧卡*](../secgloss/s-gly.md) 或視網膜掃描資料）也必須撰寫負責處理該資料及判斷其真實性的驗證套件。

 

如需 Winlogon 和 Gina 的詳細資訊，請參閱 [winlogon 和 GINA](winlogon-and-gina.md)。 如需有關驗證套件的詳細資訊，請參閱 [建立自訂安全性封裝](creating-custom-security-packages.md)。

 

 
