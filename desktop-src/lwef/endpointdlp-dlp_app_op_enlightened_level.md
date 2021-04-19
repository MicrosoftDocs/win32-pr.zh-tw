---
description: 使端點資料遺失防止 (DLP) 動作與強制等級產生關聯。
title: 'DLP_APP_OP_ENLIGHTENED_LEVEL 結構 (endpointdlp .h) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DLP_APP_OP_ENLIGHTENED_LEVEL
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: 2d9c1aa8335078cad71832c6090cada1669641cb
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495545"
---
# <a name="dlp_app_op_enlightened_level-structure"></a>DLP_APP_OP_ENLIGHTENED_LEVEL 結構

使端點資料遺失防止 (DLP) 動作與強制等級產生關聯。

## <a name="syntax"></a>語法


```C++
typedef struct _DLP_APP_OP_ENLIGHTENED_LEVEL{
    DlpActionType Operation;
    DlpAppEnforceLevel AppEnforcementLevel;
}DLP_APP_OP_ENLIGHTENED_LEVEL, *PDLP_APP_OP_ENLIGHTENED_LEVEL;
```


## <a name="members"></a>成員

<dl> <dt>

*操作* \[在\]
</dt> <dd>

[DlpActionType](endpointdlp-dlpactiontype.md)列舉中的值，指定端點 DLP 動作類型。

</dd> </dl>

<dl> <dt>

*AppEnforcementLevel* \[在\]
</dt> <dd>

[DlpAppEnforceLevel](endpointdlp-dlpappenforcelevel.md)中的值，指定相關聯之端點 DLP 動作類型的強制執行層級。

</dd> </dl>





## <a name="remarks"></a>備註

將這些結構的陣列傳遞至 [DlpInitializeEnforcementMode](endpointdlp-dlpinitializeenforcementmode.md) ，以設定一組端點 DLP 作業的強制模式。

## <a name="requirements"></a>規格需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |

