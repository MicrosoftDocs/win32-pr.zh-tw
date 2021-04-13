---
title: 'BG_JOB_TYPE 列舉 (>deliveryoptimization .h) '
description: BG_JOB_TYPE 列舉會定義常數值，以指定傳送作業的類型，例如 [下載]。
ms.assetid: 696A43C3-1FA2-436D-B34A-3544E7C9A66A
keywords:
- BG_JOB_TYPE 列舉
topic_type:
- apiref
api_name:
- BG_JOB_TYPE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f1f672bcf2d2538bfaa9b9573fa1dfa71ee7b9cd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464945"
---
# <a name="bg_job_type-enumeration"></a>BG_JOB_TYPE 列舉

**BG_JOB_TYPE** 列舉會定義常數值，以指定傳送作業的類型，例如 [下載]。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  BG_JOB_TYPE_DOWNLOAD
} BG_JOB_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="BG_JOB_TYPE_DOWNLOAD"></span><span id="bg_job_type_download"></span>**BG_JOB_TYPE_DOWNLOAD**
</dt> <dd>

指定作業將檔下載至用戶端。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob：： GetType**](ibackgroundcopyjob-gettype.md)
</dt> <dt>

[**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





