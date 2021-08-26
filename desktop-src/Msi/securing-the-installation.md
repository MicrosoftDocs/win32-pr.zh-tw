---
description: 將 CustomUserAccounts 資料表中的所有密碼屬性加入至屬性工作表中的 MsiHiddenProperties 屬性。
ms.assetid: 682f534c-10a2-4260-b21d-7075d8c1620c
title: 保護安裝的安全
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 642170cc2ac4e84bebe5235e84328abe5039ede1bdb8fc2760bbd249ff5268de
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120040728"
---
# <a name="securing-the-installation"></a>保護安裝的安全

將 CustomUserAccounts 資料表中的所有密碼屬性加入至 [屬性工作表](property-table.md)中的 [**MsiHiddenProperties**](msihiddenproperties.md)屬性。 將延遲自訂動作的名稱也加入至 **MsiHiddenProperties** 屬性。 這可防止安裝程式將機密屬性值寫入 () 到記錄檔中的密碼，並確保當延遲的自訂動作使用這些值做為 CustomActionData 屬性時，不會記錄這些值。

若要讓使用者的密碼可在 Windows Installer 服務中使用，必須將 password 屬性新增至 [**SecureCustomProperties**](securecustomproperties.md)屬性。

[屬性工作表](property-table.md)



| 屬性                                                 | 值                                                        |
|----------------------------------------------------------|--------------------------------------------------------------|
| [**MsiHiddenProperties**](msihiddenproperties.md)       | TESTUSERPASSWORD;CreateAccount;RemoveAccount;RollbackAccount |
| [**SecureCustomProperties**](securecustomproperties.md) | TESTUSERPASSWORD                                             |



 

這會結束範例。

 

 



