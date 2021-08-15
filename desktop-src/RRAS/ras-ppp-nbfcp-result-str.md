---
title: 'RAS_PPP_NBFCP_RESULT 結構 (Rassapi .h) '
description: RAS \_ ppp \_ NBFCP \_ 結果結構是用來報告通訊埠的 PPP NETBEUI Framer (NBF) 投影作業的結果。
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS_PPP_NBFCP_RESULT 結構 RAS
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e415e6aea75dcf78d19d776e4df0a6edf704db473eacf0c8ddbb366ffbf65947
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117789592"
---
# <a name="ras_ppp_nbfcp_result-structure"></a>RAS \_ PPP \_ NBFCP \_ 結果結構

\[Windows Vista 不支援 **RAS \_ PPP \_ NBFCP \_ 結果** 結構。\]

**RAS \_ ppp \_ NBFCP \_ 結果** 結構是用來報告通訊埠的 PPP NetBEUI Framer (NBF) 投影作業的結果。

## <a name="syntax"></a>語法


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a>成員

<dl> <dt>

**dwError**
</dt> <dd>

表示 NBF 投射作業的結果。 沒有錯誤的值 \_ 表示成功，在這種情況下， **wszWksta** 成員會包含遠端電腦的名稱。 如果投射作業不成功，則 **dwError** 是 winerror.h .H 或 Raserror 的錯誤碼。

</dd> <dt>

**dwNetBiosError**
</dt> <dd>

忽略伺服器上的這個成員;它只與用戶端相關。

</dd> <dt>

**szName**
</dt> <dd>

忽略伺服器上的這個成員;它只與用戶端相關。

</dd> <dt>

**wszWksta**
</dt> <dd>

以 null 結束的 Unicode 字串，指定 RAS 用戶端工作站的 NetBIOS 名稱。

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

[**RAS \_ 埠 \_ 1**](ras-port-1-str.md)
</dt> <dt>

[**RAS \_ PPP \_ 投射 \_ 結果**](ras-ppp-projection-result-str.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





