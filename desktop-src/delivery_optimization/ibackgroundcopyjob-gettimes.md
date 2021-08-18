---
title: 'IBackgroundCopyJob GetTimes 方法 (>deliveryoptimization .h) '
description: 抓取作業相關的時間戳記，例如作業的建立時間或上次修改時間。
ms.assetid: 9002FB8D-08CB-4878-980F-15FE0DC952A6
keywords:
- GetTimes 方法
- GetTimes 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetTimes 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetTimes
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 3179342630fe932dd55efc4e75e15cd06a879d6cdc93005981cc7e0ebca7e05c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755208"
---
# <a name="ibackgroundcopyjobgettimes-method"></a>IBackgroundCopyJob：： GetTimes 方法

抓取作業相關的時間戳記，例如作業的建立時間或上次修改時間。

## <a name="syntax"></a>語法


```C++
HRESULT GetTimes(
  [out] BG_JOB_TIMES *pTimes
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pTimes* \[擴展\]
</dt> <dd>

包含作業相關的時間戳記。 如需可用的時間戳記，請參閱 [**BG_JOB_TIMES**](bg-job-times.md) 結構。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                              | 描述                                         |
|------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | 已成功取出時間戳記。<br/> |



 

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

[**BG_JOB_TIMES**](bg-job-times.md)
</dt> </dl>

 

 





