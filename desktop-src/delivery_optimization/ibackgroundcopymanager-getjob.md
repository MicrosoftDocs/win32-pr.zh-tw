---
title: 'IBackgroundCopyManager GetJob 方法 (>deliveryoptimization .h) '
description: 從傳送佇列中抓取指定的工作。 一般來說，您的應用程式會保存工作識別碼，讓您稍後可以從佇列中取得工作。
ms.assetid: ED551A6B-66C7-47E9-93DA-E231BD637522
keywords:
- GetJob 方法
- GetJob 方法，IBackgroundCopyManager 介面
- IBackgroundCopyManager 介面，GetJob 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.GetJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d8d05b496eaa0d6f1520f22efeed8a39af5eb8e4c338457e18c65a7913489472
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542286"
---
# <a name="ibackgroundcopymanagergetjob-method"></a>IBackgroundCopyManager：： GetJob 方法

從傳送佇列中抓取指定的工作。 一般來說，您的應用程式會保存工作識別碼，讓您稍後可以從佇列中取得工作。

## <a name="syntax"></a>語法


```C++
HRESULT GetJob(
  [in]  REFGUID            JobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*JobID* \[在\]
</dt> <dd>

識別要從傳送佇列中取出的作業。 [**>Batchclient.joboperations.createjob**](ibackgroundcopymanager-createjob.md)方法會傳回作業識別碼。

</dd> <dt>

*ppJob* \[擴展\]
</dt> <dd>

*JobID* 所指定之作業的 [**IBackgroundCopyJob**](ibackgroundcopyjob-.md)介面指標。 完成時，發行 *ppJob*。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                                      | Description                                                        |
|--------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>         | 已成功從傳送佇列中取出作業。<br/> |
| <dl> <dt>**DO_E_NOT_FOUND**</dt> </dl> | 在佇列中找不到作業。<br/>                     |
| <dl> <dt>**E_ACCESSDENIED**</dt> </dl>   | 使用者沒有取得工作的許可權。<br/>      |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager 定義為5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob：： GetId**](ibackgroundcopyjob-getid.md)
</dt> <dt>

[**IBackgroundCopyManager：： >batchclient.joboperations.createjob**](ibackgroundcopymanager-createjob.md)
</dt> </dl>

 

 





