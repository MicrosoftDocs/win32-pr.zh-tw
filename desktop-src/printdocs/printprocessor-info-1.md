---
description: PRINTPROCESSOR \_ INFO \_ 1 結構會指定已安裝的列印處理器名稱。
ms.assetid: 49b272c8-156b-4996-b3fd-92cde831f4ae
title: 'PRINTPROCESSOR_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PRINTPROCESSOR_INFO_1
- _PRINTPROCESSOR_INFO_1A
- _PRINTPROCESSOR_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 5ac35f85e904e9a80d9f244a1421b54fd0994a43
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106985683"
---
# <a name="printprocessor_info_1-structure"></a>PRINTPROCESSOR \_ INFO \_ 1 結構

**PRINTPROCESSOR \_ INFO \_ 1** 結構會指定已安裝的列印處理器名稱。

## <a name="syntax"></a>語法


```C++
typedef struct _PRINTPROCESSOR_INFO_1 {
  LPTSTR pName;
} PRINTPROCESSOR_INFO_1, *PPRINTPROCESSOR_INFO_1;
```



## <a name="members"></a>成員

<dl> <dt>

**pName**
</dt> <dd>

指定已安裝之列印處理器名稱的以 null 結束的字串指標。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ PRINTPROCESSOR \_ Info \_ 1W** (Unicode) 和 **\_ PRINTPROCESSOR \_ info \_ 1a** (ANSI) <br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumPrintProcessors**](enumprintprocessors.md)
</dt> </dl>

 

 




