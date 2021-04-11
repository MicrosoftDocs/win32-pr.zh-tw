---
title: 'IBackgroundCopyManager >batchclient.joboperations.createjob 方法 (>deliveryoptimization .h) '
description: 建立作業。
ms.assetid: BDE5BE4D-9AE9-463D-B900-850D255EAB58
keywords:
- '>batchclient.joboperations.createjob 方法'
- '>batchclient.joboperations.createjob 方法，IBackgroundCopyManager 介面'
- IBackgroundCopyManager 介面，>batchclient.joboperations.createjob 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyManager.CreateJob
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: de7f0b61cdbc5d5776039c3bf13b83ca0a6f8fdc
ms.sourcegitcommit: ea73413ee4f69fa573ee0cd4422f20d17bd42e1f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/27/2021
ms.locfileid: "104027609"
---
# <a name="ibackgroundcopymanagercreatejob-method"></a>IBackgroundCopyManager：： >batchclient.joboperations.createjob 方法

建立作業。

## <a name="syntax"></a>語法


```C++
HRESULT CreateJob(
  [in]  LPCWSTR            pDisplayName,
  [in]  BG_JOB_TYPE        Type,
  [out] GUID               *pJobID,
  [out] IBackgroundCopyJob **ppJob
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDisplayName* \[在\]
</dt> <dd>

以 Null 終止的字串，其中包含作業的顯示名稱。 通常，顯示名稱會用來識別使用者介面中的作業。 請注意，有一個以上的作業可能會有相同的顯示名稱。 不得為 **Null**。 名稱限制為256個字元，不包括 null 結束字元。

</dd> <dt>

*類型* \[在\]
</dt> <dd>

傳送作業的類型，例如 BG_JOB_TYPE_DOWNLOAD。 如需傳輸類型的清單，請參閱 [**BG_JOB_TYPE**](bg-job-type.md) 列舉。

</dd> <dt>

*pJobID* \[擴展\]
</dt> <dd>

可唯一識別佇列中的作業。 當您呼叫 [**IBackgroundCopyManager：： GetJob**](ibackgroundcopymanager-getjob.md) 方法以從佇列取得工作時，請使用此識別碼。

</dd> <dt>

*ppJob* \[擴展\]
</dt> <dd>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)介面指標，可讓您用來修改作業的屬性，並指定要傳送的檔案。 若要啟動佇列中的作業，請呼叫 [**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md) 方法。 完成時釋放 *ppJob* 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                              | Description                                    |
|------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | 已成功產生新的作業。<br/> |



 

## <a name="remarks"></a>備註

只有建立作業的使用者或具有系統管理員許可權的使用者可以 [將檔案新增至作業](https://www.bing.com/search?q=add+files+to+the+job) ，並 [變更作業的屬性](https://www.bing.com/search?q=change+the+job's+properties)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyManager 定義為5CE34C0D-0DC9-4C1F-897C-DAA1B78CEE7C<br/>           |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyManager**](ibackgroundcopymanager.md)
</dt> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md)
</dt> </dl>
