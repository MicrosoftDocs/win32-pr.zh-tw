---
title: 'IBackgroundCopyFile5 GetProperty 方法 (>deliveryoptimization .h) '
description: 取得傳遞最佳化的泛型屬性 (是否) 檔案傳輸。
ms.assetid: E2E96A0F-5670-4DE7-9DF8-A215AFAD0E8A
keywords:
- GetProperty 方法
- GetProperty 方法，IBackgroundCopyFile5 介面
- IBackgroundCopyFile5 介面，GetProperty 方法
topic_type:
- apiref
api_name:
- IBackgroundCopyFile5.GetProperty
api_location:
- dosvc.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 84c6a9f96fc332bda940573bde78d7dd05efeeb1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104094456"
---
# <a name="ibackgroundcopyfile5getproperty-method"></a>IBackgroundCopyFile5：： GetProperty 方法

取得傳遞最佳化的泛型屬性 (是否) 檔案傳輸。

## <a name="syntax"></a>語法


```C++
HRESULT GetProperty(
  [in]  BITS_FILE_PROPERTY_ID    PropertyId,
  [out] BITS_FILE_PROPERTY_VALUE *PropertyValue
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PropertyId* \[在\]
</dt> <dd>

指定要抓取其值的檔案屬性。

</dd> <dt>

*PropertyValue* \[擴展\]
</dt> <dd>

傳回做為 BITS_FILE_PROPERTY_VALUE 聯集之指標的屬性值。 使用適用于所傳入屬性識別碼值的聯集欄位。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果這個方法成功，它會傳回 **S_OK**。 否則，它會傳回 **HRESULT** 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1709版桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server，版本 1709 \[ 桌面應用程式\]<br/>                                       |
| 標頭<br/>                   | <dl> <dt>>deliveryoptimization。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>>deliveryoptimization .idl</dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Dosvc .lib</dt> </dl>                |
| DLL<br/>                      | <dl> <dt>Dosvc.dll</dt> </dl>                |
| IID<br/>                      | IID_IBackgroundCopyFile5 定義為85C1657F-DAFC-40E8-8834-DF18EA25717E<br/>             |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5.md)
</dt> <dt>

[**IBackgroundCopyFile5**](ibackgroundcopyfile5-setproperty.md)
</dt> </dl>

 

 





