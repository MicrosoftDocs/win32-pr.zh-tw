---
title: 'RAS_PARAMETERS 結構 (Rassapi .h) '
description: RasAdminPortGetInfo 函 \_ 式會使用 ras 參數結構，傳回與 RAS 伺服器上端口相關聯之媒體特定參數的名稱和值。
ms.assetid: b46b6176-9a0c-4d9b-b961-b20fdc41653b
keywords:
- RAS_PARAMETERS 結構 RAS
topic_type:
- apiref
api_name:
- RAS_PARAMETERS
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e38ec1a8febbca4319a9c098eafee3705fe59602af81b3ec94e4e974892be771
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119909668"
---
# <a name="ras_parameters-structure"></a>RAS \_ 參數結構

\[Windows Vista 不支援 **RAS \_ 參數** 結構。\]

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)函式會使用 **ras \_ 參數** 結構，傳回與 RAS 伺服器上端口相關聯之媒體特定參數的名稱和值。

## <a name="syntax"></a>語法


```C++
typedef struct RAS_PARAMETERS {
  CHAR              P_Key[RASSAPI_MAX_PARAM_KEY_SIZE];
  RAS_PARAMS_FORMAT P_Type;
  BYTE              P_Attributes;
  RAS_PARAMS_VALUE  P_Value;
} RAS_PARAMETERS;
```



## <a name="members"></a>成員

<dl> <dt>

**P \_ 鍵**
</dt> <dd>

指定代表媒體特定參數的索引鍵名稱，例如 MAXCONNECTBPS。

</dd> <dt>

**P \_ 類型**
</dt> <dd>

識別與參數相關聯的資料類型。 這個成員可以是下列其中一個 [**RAS \_ PARAMS \_ 格式**](ras-params-format-str.md) 列舉值的值。



| 值                                                                                                                                                                                | 意義                                                                 |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span><dl> <dt>**ParamNumber**</dt> </dl> | 指出與索引鍵相關聯的資料是數位。<br/> |
| <span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span><dl> <dt>**ParamString**</dt> </dl> | 表示與索引鍵相關聯的資料為字串。<br/> |



 

</dd> <dt>

**P \_ 屬性**
</dt> <dd>

保留的。

</dd> <dt>

**P \_ 值**
</dt> <dd>

指定與參數相關聯的值。 這個成員是 [**RAS \_ PARAMS \_ 值**](ras-params-value-str.md) 聯集。 如果 **P \_ 類型** 成員是 ParamNumber，等位的 **數位** 成員就會包含此值。 如果 **P \_ 類型** 是 ParamString，等位的 **字串** 成員就會包含值。

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

[**RasAdminAcceptNewConnection**](rasadminacceptnewconnection.md)
</dt> <dt>

[**RasAdminConnectionHangupNotification**](rasadminconnectionhangupnotification.md)
</dt> <dt>

[**RasAdminPortGetInfo**](rasadminportgetinfo.md)
</dt> </dl>

 

 





