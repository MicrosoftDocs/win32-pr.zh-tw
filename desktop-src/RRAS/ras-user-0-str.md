---
title: 'RAS_USER_0 結構 (Rassapi .h) '
description: '\_ \_ RasAdminUserSetInfo 和 RasAdminUserGetInfo 函數中會使用 RAS 使用者0結構來指定使用者的相關資訊。'
ms.assetid: a2d4a935-f46d-4bc2-ada8-beaa3ac74834
keywords:
- RAS_USER_0 結構 RAS
- PRAS_USER_0 結構指標 RAS
topic_type:
- apiref
api_name:
- RAS_USER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cbb4b04ddf3b81d330825b3333899e149d2f7b0d1f30c19106c6977e5291846f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789139"
---
# <a name="ras_user_0-structure"></a>RAS \_ 使用者 \_ 0 結構

\[Windows Vista 不支援這個版本的 **RAS \_ 使用者 \_ 0** 結構。 請改用 mprapi 中定義的較新 [**RAS \_ 使用者 \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_user_0) 。\]

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)和 [**RasAdminUserGetInfo**](rasadminusergetinfo.md)函數中會使用 **RAS \_ 使用者 \_ 0** 結構來指定使用者的相關資訊。

## <a name="syntax"></a>語法


```C++
typedef struct _RAS_USER_0 {
  BYTE  bfPrivilege;
  WCHAR szPhoneNumber[RASSAPI_MAX_PHONENUMBER_SIZE + 1];
} RAS_USER_0, *PRAS_USER_0;
```



## <a name="members"></a>成員

<dl> <dt>

**bfPrivilege**
</dt> <dd>

一組位旗標，指定使用者的 RAS 許可權。 這個成員可以是 RASPRIV \_ DialinPrivilege 旗標和其中一個回撥旗標的組合。 使用 RASPRIV \_ CallbackType mask 來識別提供給使用者的回撥許可權類型。 已定義下列旗標。



| 值                                                                                                                                                                                                                                         | 意義                                                                                       |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| <span id="RASPRIV_NoCallback"></span><span id="raspriv_nocallback"></span><span id="RASPRIV_NOCALLBACK"></span><dl> <dt>**RASPRIV \_ NoCallback**</dt> </dl>                             | 使用者沒有任何回撥許可權。<br/>                                               |
| <span id="RASPRIV_AdminSetCallback"></span><span id="raspriv_adminsetcallback"></span><span id="RASPRIV_ADMINSETCALLBACK"></span><dl> <dt>**RASPRIV \_ AdminSetCallback**</dt> </dl>     | 使用者帳戶已設定為讓系統管理員設定回撥號碼。<br/> |
| <span id="RASPRIV_CallerSetCallback"></span><span id="raspriv_callersetcallback"></span><span id="RASPRIV_CALLERSETCALLBACK"></span><dl> <dt>**RASPRIV \_ CallerSetCallback**</dt> </dl> | 遠端使用者可以在撥入時指定撥回電話號碼。<br/>              |
| <span id="RASPRIV_DialinPrivilege"></span><span id="raspriv_dialinprivilege"></span><span id="RASPRIV_DIALINPRIVILEGE"></span><dl> <dt>**RASPRIV \_ DialinPrivilege**</dt> </dl>         | 使用者有權撥入這部伺服器。<br/>                                 |



 

在 [**RasAdminUserSetInfo**](rasadminusersetinfo.md) 函式的呼叫中指定其中一個回呼旗標。

</dd> <dt>

**szPhoneNumber**
</dt> <dd>

以 null 結束的 Unicode 字串，指定使用者的回撥電話號碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                           |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                 |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Rassapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[遠端存取服務 (RAS) 總覽](about-remote-access-service.md)
</dt> <dt>

[RAS 伺服器管理結構](ras-server-administration-structures.md)
</dt> <dt>

[**RasAdminUserGetInfo**](rasadminusergetinfo.md)
</dt> <dt>

[**RasAdminUserSetInfo**](rasadminusersetinfo.md)
</dt> </dl>

 

 





