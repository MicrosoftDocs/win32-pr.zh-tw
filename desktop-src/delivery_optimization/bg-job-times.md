---
title: 'BG_JOB_TIMES 結構 (>deliveryoptimization .h) '
description: BG_JOB_TIMES 結構會提供作業相關的時間戳記。
ms.assetid: 0147478F-C850-4B66-AB15-042C1A81D6B5
keywords:
- BG_JOB_TIMES 結構
topic_type:
- apiref
api_name:
- BG_JOB_TIMES
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0a2d4e56bb616254537e26fc1ba0fdf5b9e251a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103685613"
---
# <a name="bg_job_times-structure"></a>BG_JOB_TIMES 結構

**BG_JOB_TIMES** 結構會提供作業相關的時間戳記。

## <a name="syntax"></a>語法


```C++
typedef struct _BG_JOB_TIMES {
  FILETIME CreationTime;
  FILETIME ModificationTime;
  FILETIME TransferCompletionTime;
} BG_JOB_TIMES;
```



## <a name="members"></a>成員

<dl> <dt>

**CreationTime**
</dt> <dd>

建立作業的時間。 時間會指定為 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)。

</dd> <dt>

**ModificationTime**
</dt> <dd>

上次修改作業或傳輸位元組的時間。 在 [ * *IBackgroundCopyJob \** _](/previous-versions//mt811348(v=vs.85))介面中新增檔案或呼叫任何 set 方法會變更此值。 此外，變更作業的狀態以及呼叫 [_ *暫* *](ibackgroundcopyjob-suspend.md)止、[**繼續**](ibackgroundcopyjob-resume.md)、[**取消**](ibackgroundcopyjob-cancel.md)和 [**完成**](ibackgroundcopyjob-complete.md)方法會變更此值。 時間會指定為 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)。

</dd> <dt>

**TransferCompletionTime**
</dt> <dd>

工作進入 BG_JOB_STATE_TRANSFERRED 狀態的時間。 時間會指定為 [FILETIME](/windows/win32/api/minwinbase/ns-minwinbase-filetime)。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob::GetTimes**](ibackgroundcopyjob-gettimes.md)
</dt> </dl>

 

