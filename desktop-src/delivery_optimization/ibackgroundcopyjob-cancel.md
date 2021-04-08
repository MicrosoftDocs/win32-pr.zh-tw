---
title: 'IBackgroundCopyJob Cancel 方法 (>deliveryoptimization) '
description: 從傳送佇列刪除工作，並從用戶端移除相關的暫存檔案 (下載) 和伺服器 (上傳) 。
ms.assetid: DC502DC2-1335-476F-A1B8-FDB6BA595FF1
keywords:
- Cancel 方法
- Cancel 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，Cancel 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.Cancel
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f72cdcea82ef7db30de141af295bb74594a7a630
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843456"
---
# <a name="ibackgroundcopyjobcancel-method"></a>IBackgroundCopyJob：： Cancel 方法

從傳送佇列刪除工作，並從用戶端移除相關的暫存檔案 (下載) 和伺服器 (上傳) 。

## <a name="syntax"></a>語法


```C++
HRESULT Cancel();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                                          | Description                                                                                              |
|------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl>             | 已成功取消作業。<br/>                                                                |
| <dl> <dt>**DO_E_INVALID_STATE**</dt> </dl> | 無法取消其狀態為 BG_JOB_STATE_CANCELLED 或 BG_JOB_STATE_ACKNOWLEDGED 的作業。<br/> |



 

## <a name="remarks"></a>備註

您可以隨時取消作業;不過，無法在作業取消之後復原。

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

[**IBackgroundCopyJob：： Complete**](ibackgroundcopyjob-complete.md)
</dt> <dt>

[**IBackgroundCopyJob：： Resume**](ibackgroundcopyjob-resume.md)
</dt> <dt>

[**IBackgroundCopyJob：：暫止**](ibackgroundcopyjob-suspend.md)
</dt> </dl>

 

 





