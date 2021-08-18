---
title: 'INapServerCallback OnComplete 方法 (NapSystemHealthValidator .h) '
description: 由 Shv 用來指示非同步要求完成。
ms.assetid: 959ee4ac-7c29-4013-a174-24abc6a580c7
keywords:
- OnComplete 方法 NAP
- OnComplete 方法 NAP，INapServerCallback 介面
- INapServerCallback 介面 NAP，OnComplete 方法
topic_type:
- apiref
api_name:
- INapServerCallback.OnComplete
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16b0eb14663894eb1aac6911659eb452a1d50af59219b9c978215dc96de8a12f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012586"
---
# <a name="inapservercallbackoncomplete-method"></a>INapServerCallback：： OnComplete 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

Shv 會使用 **INapServerCallback：： OnComplete** 方法來通知非同步要求完成。

## <a name="syntax"></a>語法


```C++
HRESULT OnComplete(
  [in] INapSystemHealthValidationRequest *request,
  [in] HRESULT                           errorCode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*要求* \[在\]
</dt> <dd>

代表驗證要求之 [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) 物件的指標。

</dd> <dt>

*errorCode* \[在\]
</dt> <dd>

指出無法執行驗證之原因的 [**NAP 錯誤碼**](nap-error-constants.md) 。

> [!Note]  
> 一般而言， [**INapSystemHealthValidationRequest：： SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md) 方法的傳回值會傳遞給這個參數。 但是，如果因為重新處理失敗而無法呼叫 **SetSoHResponse** ，就會傳遞 failed 命令所傳回的值。

 

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

\_無論 **SoHRequest** 是否通過健康情況檢查，驗證程式都必須傳回 S，才能完成 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh)驗證。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthValidator。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>


</dt> <dt>

[**INapServerCallback**](inapservercallback.md)
</dt> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





