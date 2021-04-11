---
description: 作業 \_ 資訊 \_ 3 結構是用來將一組列印工作連結在一起。
ms.assetid: a110f555-dc33-450c-ae77-ea26f0f69448
title: 'JOB_INFO_3 結構 (Winspool.drv .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- JOB_INFO_3
api_type:
- HeaderDef
api_location:
- Winspool.h
ms.openlocfilehash: c76cbb6c019878d9c392d21caa40c604df3a5f12
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194962"
---
# <a name="job_info_3-structure"></a>作業 \_ 資訊 \_ 3 結構

**作業 \_ 資訊 \_ 3** 結構是用來將一組列印工作連結在一起。

## <a name="syntax"></a>語法


```C++
typedef struct _JOB_INFO_3 {
  DWORD JobId;
  DWORD NextJobId;
  DWORD Reserved;
} JOB_INFO_3, *PJOB_INFO_3;
```



## <a name="members"></a>成員

<dl> <dt>

**JobId**
</dt> <dd>

列印工作識別碼。

</dd> <dt>

**NextJobId**
</dt> <dd>

在一組連結的列印工作中，下一個列印工作的列印工作識別碼。

</dd> <dt>

**已保留**
</dt> <dd>

這個值已保留供未來使用 您必須將它設定為零。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                      |
| 標頭<br/>                   | <dl> <dt>Winspool.drv (包含) 的 Windows。h </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[列印](printdocs-printing.md)
</dt> <dt>

[列印多工緩衝處理器 API 結構](printing-and-print-spooler-structures.md)
</dt> <dt>

[**EnumJobs**](enumjobs.md)
</dt> <dt>

[**GetJob**](getjob.md)
</dt> <dt>

[**SetJob**](setjob.md)
</dt> </dl>

 

 




