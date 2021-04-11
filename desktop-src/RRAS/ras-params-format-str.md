---
title: 'RAS_PARAMS_FORMAT 列舉 (Rassapi .h) '
description: Ras \_ \_ 參數格式列舉型別會在 ras \_ 參數結構中用來指出與媒體特定索引鍵相關聯的資料類型。
ms.assetid: dd2c0110-1f27-4a8f-bc61-f15588ebc4ca
keywords:
- RAS_PARAMS_FORMAT 列舉 RAS
topic_type:
- apiref
api_name:
- RAS_PARAMS_FORMAT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00065f3781fd2ada420f67367e84e0863fe3b446
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104393"
---
# <a name="ras_params_format-enumeration"></a>RAS \_ 參數 \_ 格式列舉

\[Windows Vista 不支援 **RAS \_ PARAMS \_ 格式** 列舉。\]

Ras **參數 \_ \_ 格式** 列舉型別會在 [**ras \_ 參數**](ras-parameters-str.md) 結構中用來指出與媒體特定索引鍵相關聯的資料類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum RAS_PARAMS_FORMAT { 
  ParamNumber  = 0,
  ParamString  = 1
} RAS_PARAMS_FORMAT;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="ParamNumber"></span><span id="paramnumber"></span><span id="PARAMNUMBER"></span>**ParamNumber**
</dt> <dd>

指出與索引鍵相關聯的資料是數位。

</dd> <dt>

<span id="ParamString"></span><span id="paramstring"></span><span id="PARAMSTRING"></span>**ParamString**
</dt> <dd>

表示與索引鍵相關聯的資料為字串。

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

[RAS 伺服器管理列舉](ras-server-administration-enumerations.md)
</dt> <dt>

[**RAS \_ 參數**](ras-parameters-str.md)
</dt> </dl>

 

 





