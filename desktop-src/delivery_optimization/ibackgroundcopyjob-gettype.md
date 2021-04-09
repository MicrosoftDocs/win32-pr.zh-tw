---
title: 'IBackgroundCopyJob GetType 方法 (>deliveryoptimization .h) '
description: 抓取正在執行的傳輸類型，例如檔案下載或上傳。
ms.assetid: F543A601-9385-4A73-A4E2-DE61433E84D3
keywords:
- GetType 方法
- GetType 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetType 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetType
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 5b0a09a3c7387b5b911bf6731921e7ed4e9b9163
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024741"
---
# <a name="ibackgroundcopyjobgettype-method"></a>IBackgroundCopyJob：： GetType 方法

抓取正在執行的傳輸類型，例如檔案下載或上傳。

## <a name="syntax"></a>語法


```C++
HRESULT GetType(
  [out] BG_JOB_TYPE *pJobType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pJobType* \[擴展\]
</dt> <dd>

要執行的傳輸類型。 如需傳輸類型的清單，請參閱 [**BG_JOB_TYPE**](bg-job-type.md) 列舉。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                              | Description                                          |
|------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | 已成功取出傳輸類型。<br/> |



 

## <a name="remarks"></a>備註

指定建立作業時的傳輸類型。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob 定義為37668D37-507E-4160-9316-26306D150B12<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**BG_JOB_TYPE**](bg-job-type.md)
</dt> <dt>

[**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





