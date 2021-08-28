---
description: SYSTEM.PRINTING.PRINTQUEUE.ADDJOB \_ INFO \_ 1 結構會識別列印工作，以及應用程式可以儲存該作業的目錄和檔案。
ms.assetid: de915932-11a7-47e8-9be9-edab76d94189
title: 'ADDJOB_INFO_1 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ADDJOB_INFO_1
- _ADDJOB_INFO_1A
- _ADDJOB_INFO_1W
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: 6a0abcd2d9d09b65e8b4d5dd27e01532859a8060eda7847f0c1b7888a3c9714f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119950758"
---
# <a name="addjob_info_1-structure"></a>SYSTEM.PRINTING.PRINTQUEUE.ADDJOB \_ INFO \_ 1 結構

**System.printing.printqueue.addjob \_ INFO \_ 1** 結構會識別列印工作，以及應用程式可以儲存該作業的目錄和檔案。

## <a name="syntax"></a>語法


```C++
typedef struct _ADDJOB_INFO_1 {
  LPTSTR Path;
  DWORD  JobId;
} ADDJOB_INFO_1, *PADDJOB_INFO_1;
```



## <a name="members"></a>成員

<dl> <dt>

**路徑**
</dt> <dd>

以 null 結束的字串指標，其中包含應用程式可以用來儲存列印工作的路徑和檔案名。

</dd> <dt>

**JobId**
</dt> <dd>

列印工作的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>winspool.drv (包含 Windows .h) </dt> </dl> |
| Unicode 與 ANSI 名稱<br/>   | **\_ System.printing.printqueue.addjob \_ Info \_ 1W** (Unicode) 和 **\_ system.printing.printqueue.addjob \_ info \_ 1a** (ANSI) <br/>                             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**System.printing.printqueue.addjob**](addjob.md)
</dt> </dl>

 

 




