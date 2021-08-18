---
title: 'IBackgroundCopyJob SetPriority 方法 (>deliveryoptimization .h) '
description: 指定作業的優先權層級。 優先權層級會決定您的作業相對於傳送佇列中其他作業的處理時間。
ms.assetid: DC943093-CA1D-4840-B7AC-29710764D4E5
keywords:
- SetPriority 方法
- SetPriority 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，SetPriority 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetPriority
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4ed1852d6990b94a000ac6affcec6020d266aaac5fae4611c3985a6f5c203aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542869"
---
# <a name="ibackgroundcopyjobsetpriority-method"></a>IBackgroundCopyJob：： SetPriority 方法

指定作業的優先權層級。 優先權層級會決定您的作業相對於傳送佇列中其他作業的處理時間。

## <a name="syntax"></a>語法


```C++
HRESULT SetPriority(
  [in] BG_JOB_PRIORITY Priority
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*優先順序* \[在\]
</dt> <dd>

指定作業相對於傳送佇列中其他作業的優先權層級。 預設值為 BG_JOB_PRIORITY_NORMAL。 如需優先權層級的清單，請參閱 [**BG_JOB_PRIORITY**](bg-job-priority-.md) 列舉。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                              | Description                                   |
|------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | 已成功設定作業優先順序。<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**BG_JOB_PRIORITY**](bg-job-priority-.md)
</dt> <dt>

[**IBackgroundCopyJob：： GetPriority**](ibackgroundcopyjob-getpriority.md)
</dt> </dl>

 

 





