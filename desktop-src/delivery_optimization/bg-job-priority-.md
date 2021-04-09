---
title: 'BG_JOB_PRIORITY 列舉 (>deliveryoptimization .h) '
description: BG_JOB_PRIORITY 列舉會定義常數值，以指定工作的優先權層級。
ms.assetid: AF1F1F6D-473A-49E5-B24D-644A70DF304C
keywords:
- BG_JOB_PRIORITY 列舉
- BG_JOB_PRIORITY 列舉
topic_type:
- apiref
api_name:
- BG_JOB_PRIORITY
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 45b1f0f3029cc6157f2f100b3324165cfac1b03b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024961"
---
# <a name="bg_job_priority-enumeration"></a>BG_JOB_PRIORITY 列舉

**BG_JOB_PRIORITY** 列舉會定義常數值，以指定工作的優先權層級。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BG_JOB_PRIORITY_FOREGROUND,
  BG_JOB_PRIORITY_HIGH,
  BG_JOB_PRIORITY_NORMAL,
  BG_JOB_PRIORITY_LOW
} BG_JOB_PRIORITY;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="BG_JOB_PRIORITY_FOREGROUND"></span><span id="bg_job_priority_foreground"></span>**BG_JOB_PRIORITY_FOREGROUND**
</dt> <dd>

在前景中傳送工作。 前景傳輸會與其他應用程式競爭網路頻寬，這可能會妨礙使用者的網路體驗。 這是最高的優先權層級。

</dd> <dt>

<span id="BG_JOB_PRIORITY_HIGH"></span><span id="bg_job_priority_high"></span>**BG_JOB_PRIORITY_HIGH**
</dt> <dd>

在背景中傳送作業。 背景傳輸使用的是較小的網路頻寬百分比。

</dd> <dt>

<span id="BG_JOB_PRIORITY_NORMAL"></span><span id="bg_job_priority_normal"></span>**BG_JOB_PRIORITY_NORMAL**
</dt> <dd>

所有非前景作業的行為都相同。 如需詳細資訊，請參閱 BG_JOB_PRIORITY_HIGH 中的批註。

</dd> <dt>

<span id="BG_JOB_PRIORITY_LOW"></span><span id="bg_job_priority_low"></span>**BG_JOB_PRIORITY_LOW**
</dt> <dd>

所有非前景作業的行為都相同。 如需詳細資訊，請參閱 BG_JOB_PRIORITY_HIGH 中的批註。

</dd> </dl>

## <a name="remarks"></a>備註

您可以同時進行多個前景和背景傳輸。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob：： GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> <dt>

[**IBackgroundCopyJob：： SetPriority**](ibackgroundcopyjob-setpriority.md)
</dt> </dl>

 

 





