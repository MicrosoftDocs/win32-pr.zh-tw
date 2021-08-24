---
title: 'INapSystemHealthValidationRequest GetPrivateData 方法 (NapSystemHealthValidator .h) '
description: 允許 NapServer 捕獲狀態資訊。
ms.assetid: f85026ca-852b-4eb1-9a8c-7e03cd1765f2
keywords:
- GetPrivateData 方法 NAP
- GetPrivateData 方法 NAP，INapSystemHealthValidationRequest 介面
- INapSystemHealthValidationRequest 介面 NAP，GetPrivateData 方法
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest.GetPrivateData
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43ea94e3f03b3816cfb62f51263d5a5f9c67cf903b7e24991fa7a0f5d06427a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119780758"
---
# <a name="inapsystemhealthvalidationrequestgetprivatedata-method"></a>INapSystemHealthValidationRequest：： GetPrivateData 方法

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthValidationRequest：： GetPrivateData** 方法可讓 NapServer 取得狀態資訊。

## <a name="syntax"></a>語法


```C++
HRESULT GetPrivateData(
  [out] PrivateData **privateData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*privateData* \[擴展\]
</dt> <dd>

指標，指向 [**PrivateData**](/windows/win32/api/naptypes/ns-naptypes-privatedata) 包含狀態資訊之不透明資料 blob 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

也可能傳回其他 COM 特定的錯誤碼。



| 傳回碼                                                                                     | 描述                                                        |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**S \_確定**</dt> </dl>           | 作業成功。<br/>                                    |
| <dl> <dt>**E \_ACCESSDENIED**</dt> </dl> | 許可權錯誤，拒絕存取。<br/>                       |
| <dl> <dt>**E \_OUTOFMEMORY**</dt> </dl>  | 系統資源限制，無法執行操作。<br/> |



 

## <a name="remarks"></a>備註

只有 NapServer 可以解讀資料 blob。

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

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> </dl>

 

 





