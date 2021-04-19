---
description: 指定端點資料遺失防止 (DLP) 作業的強制等級。
title: 'DlpAppEnforceLevel 列舉 (endpointdlp) '
ms.topic: reference
ms.date: 03/18/2021
topic_type:
- APIRef
- kbSyntax
api_name:
- DlpAppEnforceLevel
api_type:
- COM
api_location:
- endpointdlp.h
ms.openlocfilehash: d0ccc8d0d39bc4022899deaeb9e8a81eae1f720f
ms.sourcegitcommit: 91110c16e4713ed82d7fb80562d3ddf40b5d76b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2021
ms.locfileid: "107495537"
---
# <a name="dlpappenforcelevel-enumeration"></a>DlpAppEnforceLevel 列舉

指定端點資料遺失防止 (DLP) 作業的強制等級。

## <a name="syntax"></a>Syntax


```C++
typedef enum _DlpAppEnforceLevel {
    DlpAppEnforceLevelNone = 0, 
    DlpAppEnforceLevelNotify,   
    DlpAppEnforceLevelPrevent,   
    DlpAppEnforceLevelFull, 
    DlpAppEnforceLevelCount,
}DlpAppEnforceLevel;
```


## <a name="constants"></a>常數

<dl> <dt>

*DlpAppEnforceLevelNone* \[在\]
</dt> <dd>

應用程式不會強制執行。 DLP 系統將會強制執行此作業。

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelNotify* \[在\]
</dt> <dd>

Tne 應用程式會使用 DLP Api 來通知 DLP 系統有關作業的資訊。 DLP 系統將會強制執行此作業。

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelPrevent* \[在\]
</dt> <dd>

目前的版本不支援。

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelFull* \[在\]
</dt> <dd>

目前的版本不支援。

</dd> </dl>

<dl> <dt>

*DlpAppEnforceLevelCount* \[在\]
</dt> <dd>

列舉的最大值。

</dd> </dl>



## <a name="remarks"></a>備註

[DLP_APP_OP_ENLIGHTENED_LEVEL](endpointdlp-dlp_app_op_enlightened_level.md)結構會使用這個列舉的值。


## <a name="requirements"></a>規格需求



| 需求          |    值                   |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 版本 1809 (10.0;組建 17763)            |

