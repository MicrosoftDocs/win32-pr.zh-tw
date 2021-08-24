---
title: RAS 使用者帳戶管理
description: Windows NT 4.0 RAS 伺服器使用包含一組使用者帳戶相關資訊的使用者帳戶資料庫。
ms.assetid: 653307f8-3b14-474a-9094-03a2d4c89092
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6254a2d4066c6b4b4e1f1167ec842cd86c07d8122b0683c985cbea0a8ca7f2f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028728"
---
# <a name="ras-user-account-administration"></a>RAS 使用者帳戶管理

Windows NT 4.0 RAS 伺服器使用包含一組使用者帳戶相關資訊的使用者帳戶資料庫。 此資訊包含使用者的 RAS 許可權，這是一組位旗標，可決定當使用者呼叫以連接時，RAS 伺服器的回應方式。 RAS 伺服器管理功能可讓您找出使用者帳戶資料庫，以及取得和設定使用者帳戶的 RAS 許可權。

Windows NT 4.0 的 RAS 伺服器可以是 Windows NT/Windows 2000 網域的一部分，也可以是獨立的 Windows NT 伺服器或不屬於網域的工作站。 若是屬於網域的伺服器，使用者帳戶資料庫會儲存在伺服器上，也就是主域控制站 (PDC) 。 獨立伺服器會儲存自己的本機使用者帳戶資料庫。 若要取得儲存指定的 RAS 伺服器所使用的使用者帳戶資料庫之伺服器的名稱，您可以呼叫 [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) 函數。 然後，您可以在 [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) 函式的呼叫中使用使用者帳戶伺服器的名稱，以列舉使用者帳戶資料庫中的使用者。 您也可以在 [**RasAdminUserGetInfo**](rasadminusergetinfo.md) 和 [**RasAdminUserSetInfo**](rasadminusersetinfo.md) 函式的呼叫中使用伺服器名稱，以取得並設定所指定使用者帳戶的 RAS 許可權。

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)和 [**RasAdminUserSetInfo**](rasadminusersetinfo.md)函式會使用 [**ras \_ 使用者 \_ 0**](ras-user-0-str.md)結構來指定使用者的 RAS 許可權和回撥電話號碼。 RAS 許可權會指出下列資訊：

-   使用者是否可以對伺服器或伺服器所屬的網域進行遠端連線。
-   使用者是否可以透過回呼來建立連線，RAS 伺服器會在該伺服器上掛斷，然後再回呼給使用者以建立連線。

每個使用者帳戶會指定下列其中一個旗標，以指出使用者的回呼許可權。



| 值                      | 意義                                                                                                                                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ NoCallback        | RAS 伺服器不會回呼使用者以建立連線。                                                                                                                                                                                        |
| RASPRIV \_ AdminSetCallback  | 當使用者呼叫時，RAS 伺服器會停止回應，並呼叫儲存在使用者帳戶資料庫中的預設回撥電話號碼。 [**RAS \_ USER \_ 0**](ras-user-0-str.md)結構的 **szPhoneNumber** 成員包含使用者的回撥電話號碼。 |
| RASPRIV \_ CallerSetCallback | 當使用者呼叫時，RAS 伺服器會提供指定回撥電話號碼的選項。 使用者也可以選擇立即連接，而不需要回呼。 **SzPhoneNumber** 成員包含使用者可覆寫的預設數位。      |



 

 

 