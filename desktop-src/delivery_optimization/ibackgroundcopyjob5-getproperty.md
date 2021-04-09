---
title: 'IBackgroundCopyJob5 GetProperty 方法 (>deliveryoptimization .h) '
description: 取得傳遞最佳化 () 工作屬性的泛型方法。
ms.assetid: 22BA2FAB-3F24-4801-8FB7-CB6F9E8DFBB3
keywords:
- GetProperty 方法
- GetProperty 方法，IBackgroundCopyJob5 介面
- IBackgroundCopyJob5 介面，GetProperty 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyJob5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8200bb63a131db6fcab30b77f35a89fc9c943675
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934465"
---
# <a name="ibackgroundcopyjob5getproperty-method"></a>IBackgroundCopyJob5：： GetProperty 方法

取得傳遞最佳化 () 工作屬性的泛型方法。

## <a name="syntax"></a>語法


```C++
HRESULT GetProperty(
  [in]  BITS_JOB_PROPERTY_ID    PropertyId,
  [out] BITS_JOB_PROPERTY_VALUE *pPropertyValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PropertyId* \[在\]
</dt> <dd>

取得指定為 [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) 列舉值之屬性的識別碼。

</dd> <dt>

*pPropertyValue* \[擴展\]
</dt> <dd>

以 BITS_JOB_PROPERTY_VALUE 聯集傳回的屬性值。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列傳回值。



| 傳回碼                                                                          | Description        |
|--------------------------------------------------------------------------------------|--------------------|
| <dl> <dt>**S_OK**</dt> </dl> | Success<br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyJob5 定義為 E847030C-BBBA-4657-AF6D-484AA42BF1FE<br/>              |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyJob5**](ibackgroundcopyjob5.md)
</dt> <dt>

[**IBackgroundCopyJob5：： SetProperty**](ibackgroundcopyjob5-setproperty.md)
</dt> </dl>

 

 





