---
title: 'IBackgroundCopyJob5 SetProperty 方法 (>deliveryoptimization .h) '
description: 設定傳遞最佳化 (的泛型方法會) 作業屬性。
ms.assetid: 9A8CCE04-B3EB-43CC-A135-7054EC40ABEC
keywords:
- SetProperty 方法
- SetProperty 方法，IBackgroundCopyJob5 介面
- IBackgroundCopyJob5 介面，SetProperty 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.SetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: f9b7dab17780572a59e12dde9905c3d8db23895e6564aac47cb6eb2d984bfaf3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118542681"
---
# <a name="ibackgroundcopyjob5setproperty-method"></a>IBackgroundCopyJob5：： SetProperty 方法

設定傳遞最佳化 (的泛型方法會) 作業屬性。

## <a name="syntax"></a>語法


```C++
HRESULT SetProperty(
  [in] BITS_JOB_PROPERTY_ID    PropertyId,
  [in] BITS_JOB_PROPERTY_VALUE PropertyValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PropertyId* \[在\]
</dt> <dd>

要設定為 [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) 列舉值之屬性的識別碼。

</dd> <dt>

*PropertyValue* \[在\]
</dt> <dd>

正在設定之屬性的值。 為了保留型別適合屬性的值，這個值是透過由所有已知屬性型別所組成的 [**BITS_JOB_PROPERTY_VALUE**](bits-job-property-value-.md) 聯集來指定。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列傳回值。



| 傳回碼                                                                          | 描述        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Success<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | WindowsServer， \[ 僅限1709版桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>Deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 定義為 E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5：： GetProperty**](ibackgroundcopyjob5-getproperty.md)
</dt> </dl>

 

 





