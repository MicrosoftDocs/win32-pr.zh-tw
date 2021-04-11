---
title: 'RAS_PARAMS_VALUE 聯集 (Rassapi .h) '
description: Ras \_ \_ 參數值 UNION 在 ras 參數結構中用 \_ 來儲存與媒體特定參數相關聯的資料。
ms.assetid: 43284ee4-9bd4-4019-860f-0fb7ff3f38ee
keywords:
- RAS_PARAMS_VALUE 聯集 RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_VALUE
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b6f8cc6d693b32b1bbe6f05e8d32ca31a48cfb29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104093780"
---
# <a name="ras_params_value-union"></a>RAS \_ PARAMS \_ 值聯集

\[Windows Vista 不支援 **RAS \_ PARAMS \_ 值** 聯集。\]

Ras **參數 \_ \_ 值** union 在 [**ras \_ 參數**](ras-parameters-str.md) 結構中用來儲存與媒體特定參數相關聯的資料。 **Ras \_ 參數** 結構的 **P \_ 類型** 成員會使用 [**ras \_ params \_ 格式**](ras-params-format-str.md)列舉的值，來指出目前儲存在 **ras \_ 參數 \_ 值** 中的數值型別。

## <a name="syntax"></a>語法


```C++
typedef union RAS_PARAMS_VALUE {
  DWORD  Number;
  struct {
    DWORD Length;
    PCHAR Data;
  } String;
} RAS_PARAMS_VALUE;
```



## <a name="members"></a>成員

<dl> <dt>

**Number**
</dt> <dd>

如果 [**RAS \_ 參數**](ras-parameters-str.md)結構的 **P \_ 類型** 成員是 ParamNumber，則 **數位** 成員會包含媒體專用參數的值。 例如，MAXCONNECTBPS 參數的類型是 ParamNumber，而值可能是19200。

如果 [**RAS \_ 參數**](ras-parameters-str.md)結構的 **P \_ 類型** 成員是 ParamNumber，則 **數位** 成員會包含媒體專用參數的值。 例如，MAXCONNECTBPS 參數的類型是 ParamNumber，而值可能是19200。

</dd> <dt>

**String**
</dt> <dd>

如果 [**RAS \_ 參數**](ras-parameters-str.md)結構的 **P \_ 類型** 成員是 ParamString，則 **字串** 成員會包含媒體專用參數的值。

<dl> <dt>

**長度**
</dt> <dd>

指定 **資料** 成員所指向之字串的長度（以字元為單位）。

</dd> <dt>

**資料**
</dt> <dd>

緩衝區的指標，此緩衝區包含媒體特定參數的字串值。

</dd> </dl> </dd> </dl>

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

[RAS 伺服器管理聯集](ras-server-administration-union.md)
</dt> <dt>

[**RAS \_ 參數**](ras-parameters-str.md)
</dt> <dt>

[**RAS \_ 參數 \_ 格式**](ras-params-format-str.md)
</dt> </dl>

 

 





