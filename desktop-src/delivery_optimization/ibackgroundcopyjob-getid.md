---
title: 'IBackgroundCopyJob GetId 方法 (>deliveryoptimization .h) '
description: 抓取用來識別佇列中之作業的識別碼。
ms.assetid: 05CE5420-22F8-4CFE-BC40-3A29C775854B
keywords:
- GetId 方法
- GetId 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，GetId 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetId
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01c696985b4b632223318675fd63f842b85ed6e27297ff1befebbac1b3fa9bce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755498"
---
# <a name="ibackgroundcopyjobgetid-method"></a>IBackgroundCopyJob：： GetId 方法

抓取用來識別佇列中之作業的識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetId(
  [out] GUID *pJobID
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pJobID* \[擴展\]
</dt> <dd>

識別 DO 佇列內作業的 GUID。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會在成功時傳回 **S_OK** ，或在發生錯誤時傳回其中一個標準 COM **HRESULT** 值。

## <a name="remarks"></a>備註

當您 [建立](ibackgroundcopymanager-createjob.md) 作業時，服務會產生識別碼。 若要使用識別碼來取得作業的 [**IBackgroundCopyJob**](ibackgroundcopyjob-.md) 介面指標，請呼叫 [**IBackgroundCopyManager：： GetJob**](ibackgroundcopymanager-getjob.md) 方法。

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

[**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](ibackgroundcopymanager-createjob.md)
</dt> <dt>

[**IBackgroundCopyManager::GetJob**](ibackgroundcopymanager-getjob.md)
</dt> </dl>

 

 





