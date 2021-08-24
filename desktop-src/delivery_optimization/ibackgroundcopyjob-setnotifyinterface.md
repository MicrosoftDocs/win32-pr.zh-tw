---
title: 'IBackgroundCopyJob SetNotifyInterface 方法 (>deliveryoptimization .h) '
description: 識別要執行之 IBackgroundCopyCallback 介面的實作為。 您可以使用 IBackgroundCopyCallback 介面來接收作業相關事件的通知。
ms.assetid: 792211FC-440E-4D2C-A6C7-CE9EFB86571C
keywords:
- SetNotifyInterface 方法
- SetNotifyInterface 方法，IBackgroundCopyJob 介面
- IBackgroundCopyJob 介面，SetNotifyInterface 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.SetNotifyInterface
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: bd54255d87ee3f15f87d692e06b7a503e773634ab4ec30c3f388388233aab2b9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793407"
---
# <a name="ibackgroundcopyjobsetnotifyinterface-method"></a>IBackgroundCopyJob：： SetNotifyInterface 方法

識別要執行之 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面的實作為。 您可以使用 **IBackgroundCopyCallback** 介面來接收作業相關事件的通知。

## <a name="syntax"></a>語法


```C++
HRESULT SetNotifyInterface(
   IUnknown *pNotifyInterface
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNotifyInterface* 
</dt> <dd>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)介面指標。 若要移除目前的回呼介面指標，請將此參數設定為 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                              | 描述                                                     |
|------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | 已成功設定通知介面指標。<br/> |



 

## <a name="remarks"></a>備註

只有在您執行 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面時，才能呼叫這個方法。 使用 **SetNotifyInterface** 方法搭配 [**SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) 方法，以指定您想要接收的通知類型。

當您的應用程式終止時，通知介面會變成無效;請勿保存通知介面。 如此一來，應用程式的初始化程式應該在您要接收通知的現有工作上呼叫 **SetNotifyInterface** 方法。 如果您需要捕獲自上一次執行應用程式之後發生的狀態和進度資訊，請在應用程式初始化期間輪詢狀態和進度資訊。

只有作業擁有者/建立者或系統管理員可以註冊通知。

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

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> <dt>

[**IBackgroundCopyJob::GetNotifyInterface**](ibackgroundcopyjob-getnotifyinterface.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> </dl>

 

 





