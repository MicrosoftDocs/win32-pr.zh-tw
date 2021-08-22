---
title: 'IBackgroundCopyJob >getstate 方法 (>deliveryoptimization .h) '
description: 捕獲作業的狀態。
ms.assetid: 975AF0FB-37AE-4CE8-9EC1-35A972E422D8
keywords:
- '>getstate 方法'
- '>getstate 方法，IBackgroundCopyJob 介面'
- IBackgroundCopyJob 介面，>getstate 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob.GetState
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 64a26d1cc301230a9bb8330b9a2b2daf3178b1538ec95f593cd5e3f4d3099d7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755298"
---
# <a name="ibackgroundcopyjobgetstate-method"></a>IBackgroundCopyJob：： >getstate 方法

捕獲作業的狀態。

## <a name="syntax"></a>語法


```C++
HRESULT GetState(
  [out] BG_JOB_STATE *pJobState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pJobState* \[擴展\]
</dt> <dd>

作業的狀態。 例如，此狀態會反映作業是錯誤、傳送資料還是暫停。 如需作業狀態的清單，請參閱 [**BG_JOB_STATE**](bg-job-state-.md) 列舉。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列 **HRESULT** 值，以及其他值。



| 傳回碼                                                                              | 描述                                                 |
|------------------------------------------------------------------------------------------|-------------------------------------------------------------|
| <dl> <dt>S_OK * * * *</dt> </dl> | 已成功抓取作業的狀態。<br/> |



 

## <a name="remarks"></a>備註

如果您想要知道作業發生錯誤或已傳送作業中的所有檔案，您可以使用這個方法來輪詢作業的狀態，或您可以註冊在事件發生時收到通知。 如需註冊以接收事件通知的詳細資訊，請參閱 [**IBackgroundCopyCallback**](ibackgroundcopycallback.md) 介面。

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

[**BG_JOB_STATE**](bg-job-state-.md)
</dt> <dt>

[**IBackgroundCopyCallback**](ibackgroundcopycallback.md)
</dt> </dl>

 

 





