---
title: RAS 使用者管理
description: RAS 伺服器使用包含一組使用者帳戶相關資訊的使用者帳戶資料庫。
ms.assetid: b58767b0-9b76-4d43-953a-ea772643745e
keywords:
- RAS 系統管理 RRAS，使用者管理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7860e4916a9cf6138ebb6c201e9301feacbe332649036e7eb18075df621512a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120028638"
---
# <a name="ras-user-administration"></a>RAS 使用者管理

RAS 伺服器使用包含一組使用者帳戶相關資訊的使用者帳戶資料庫。 此資訊包含使用者的 RAS 許可權，這是一組位旗標，可決定當使用者呼叫以連接時，RAS 伺服器的回應方式。 RAS 伺服器管理功能會找出使用者帳戶資料庫，並取得並設定使用者帳戶的 RAS 許可權。

RAS 伺服器可以是作業系統網域的一部分，也可以是執行伺服器或專業版作業系統的獨立電腦。 若是屬於網域的伺服器，使用者帳戶資料庫會儲存在伺服器上，也就是主域控制站 (PDC) 。 獨立伺服器會儲存自己的本機使用者帳戶資料庫。 若要取得儲存指定的 RAS 伺服器所使用的使用者帳戶資料庫之伺服器的名稱，您可以呼叫 [**MprAdminGetPDCServer**](/windows/desktop/api/Mprapi/nf-mprapi-mpradmingetpdcserver) 函數。 然後，您可以在 [**NetQueryDisplayInformation**](/windows/win32/api/lmaccess/nf-lmaccess-netquerydisplayinformation) 函式的呼叫中使用使用者帳戶伺服器的名稱，以列舉使用者帳戶資料庫中的使用者。 您也可以在 [**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo) 和 [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo) 函式的呼叫中使用伺服器名稱，以取得並設定所指定使用者帳戶的 RAS 許可權。

[**MprAdminUserGetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusergetinfo)和 [**MprAdminUserSetInfo**](/windows/desktop/api/Mprapi/nf-mprapi-mpradminusersetinfo)函式會使用 [**ras \_ 使用者 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0)結構來指定使用者的 RAS 許可權和回撥電話號碼。 RAS 許可權會指出下列資訊：

-   使用者是否可以對伺服器或伺服器所屬的網域進行遠端連線。
-   使用者是否透過回呼來建立連線，RAS 伺服器會在該伺服器上停止回應，然後再回呼給使用者以建立連接。

每個使用者帳戶會指定下列其中一個旗標，以指出使用者的回呼許可權。



| 值                      | 意義                                                                                                                                                                                                                                                                        |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| RASPRIV \_ NoCallback        | RAS 伺服器不會回呼使用者以建立連線。                                                                                                                                                                                                          |
| RASPRIV \_ AdminSetCallback  | 當使用者呼叫時，RAS 伺服器會停止回應，並呼叫儲存在使用者帳戶資料庫中的預設回撥電話號碼。 [**RAS \_ USER \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0)結構的 **szPhoneNumber** 成員包含使用者的回撥電話號碼。                       |
| RASPRIV \_ CallerSetCallback | 當使用者呼叫時，RAS 伺服器會提供選項來指定回呼使用者的電話號碼。 使用者也可以選擇立即連接，而不需要回呼。 **SzPhoneNumber** 成員包含使用者可覆寫的預設數位。 |



 

 

 