---
description: 包含呼叫 GetPrintExecutionData 之印表機驅動程式的執行內容。
ms.assetid: 1fd25ed9-6f28-48f9-8132-d48fffc956ec
title: 'PRINT_EXECUTION_DATA 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINT_EXECUTION_DATA
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: e67b43089c275baf59295f15e84d9bf38d1a3a5ff6e2adfaf2d270b02e2ad967
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447138"
---
# <a name="print_execution_data-structure"></a>列印 \_ 執行 \_ 資料結構

包含呼叫 [**GetPrintExecutionData**](getprintexecutiondata.md)之印表機驅動程式的執行內容。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINT_EXECUTION_DATA {
  PRINT_EXECUTION_CONTEXT  context;
  DWORD                    clientAppPID;
} PRINT_EXECUTION_DATA;
```



## <a name="members"></a>成員

<dl> <dt>

**內容**
</dt> <dd>

[**列印 \_ 執行 \_ 內容**](print-execution-context.md)值，代表印表機驅動程式的目前執行內容。

</dd> <dt>

**clientAppPID**
</dt> <dd>

如果 **coNtext** 的值是 **列印 \_ 執行 \_ 內容 \_ WOW64**， **clientAppPID** 會識別代表 splwow64.exe 進程載入印表機驅動程式的用戶端應用程式。 如果 **內容** 的值不是 **列印 \_ 執行 \_ 內容 \_ WOW64**，則 **clientAppPID** 為零。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅 Windows 7 \[ 桌面應用程式\]<br/>                                                                |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                   |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetPrintExecutionData**](getprintexecutiondata.md)
</dt> <dt>

[**列印 \_ 執行 \_ 內容**](print-execution-context.md)
</dt> </dl>

 

 




