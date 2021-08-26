---
title: 'IBackgroundCopyCallback 介面 (>deliveryoptimization .h) '
description: 執行 IBackgroundCopyCallback 介面，以接收作業已完成、已修改或發生錯誤的通知。 用戶端會使用此介面，而不是輪詢作業的狀態。
ms.assetid: CF85D852-1B4E-4BC2-B6A6-0035ED3C439C
keywords:
- IBackgroundCopyCallback 介面
- IBackgroundCopyCallback 介面，說明
topic_type:
- apiref
api_name:
- IBackgroundCopyCallback
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 165a1edcdb6bd70de8fad379fcc89d5afc36776348fd7751277614229a23377e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119953638"
---
# <a name="ibackgroundcopycallback-interface"></a>IBackgroundCopyCallback 介面

執行 **IBackgroundCopyCallback** 介面，以接收作業已完成、已修改或發生錯誤的通知。 用戶端會使用此介面，而不是輪詢作業的狀態。

## <a name="members"></a>成員

**IBackgroundCopyCallback** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IBackgroundCopyCallback** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IBackgroundCopyCallback** 介面具有這些方法。



| 方法                                                                    | 描述                                                                       |
|:--------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| [**JobError**](ibackgroundcopycallback-joberror-method.md)               | 發生錯誤時呼叫。<br/>                                           |
| [**JobModification**](ibackgroundcopycallback-jobmodification-method.md) | 在修改作業時呼叫。<br/>                                         |
| [**JobTransferred**](ibackgroundcopycallback-jobtransferred.md)          | 當作業中的所有檔案都已成功傳送時呼叫。<br/> |



 

## <a name="remarks"></a>備註

若要接收通知，請呼叫 [**IBackgroundCopyJob：： SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) 方法，以指定 **IBackgroundCopyCallback** 執行的介面指標。 若要指定您要接收的通知，請呼叫 [**IBackgroundCopyJob：： SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md) 方法。

只要介面指標有效，就會呼叫您的回呼。 當您的應用程式終止時，通知介面不再有效;請勿保存通知介面。 如此一來，應用程式的初始化程式應該在您要接收通知的現有工作上呼叫 [**SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyCallback 定義為97EA99C7-0186-4AD4-8DF9-C5B4E0ED6B22<br/>          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob**](ibackgroundcopyjob-.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyFlags**](ibackgroundcopyjob-setnotifyflags.md)
</dt> <dt>

[**IBackgroundCopyJob::SetNotifyInterface**](ibackgroundcopyjob-setnotifyinterface.md)
</dt> </dl>

 

