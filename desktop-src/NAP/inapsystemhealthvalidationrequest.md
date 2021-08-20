---
title: 'INapSystemHealthValidationRequest 介面 (NapSystemHealthValidator .h) '
description: 用來支援應用程式開發人員所定義的系統健康狀態驗證。
ms.assetid: faa91ff5-49f5-4aec-81d7-02ec59274f23
keywords:
- INapSystemHealthValidationRequest 介面 NAP
- INapSystemHealthValidationRequest 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e7b6b2fdc0da8757ddd29b963445c0b984c45d19955c093270cf397fcac14b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118133473"
---
# <a name="inapsystemhealthvalidationrequest-interface"></a>INapSystemHealthValidationRequest 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthValidationRequest** 介面提供的方法可用來支援應用程式開發人員所定義的系統健全狀況驗證程式。

> [!Note]  
> [**INapSystemHealthValidationRequest2**](inapsystemhealthvalidationrequest2.md) 會繼承此介面的所有方法，因此應該改用。

 

## <a name="members"></a>成員

**INapSystemHealthValidationRequest** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapSystemHealthValidationRequest** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapSystemHealthValidationRequest** 介面具有這些方法。



| 方法                                                                                                                               | 描述                                                                                                           |
|:-------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest::GetCorrelationId**](inapsystemhealthvalidationrequest-getcorrelationid-method.md)             | 由驗證程式用來取出相互關聯識別碼。 然後，驗證程式必須記錄這些資訊。<br/>           |
| [**INapSystemHealthValidationRequest::GetMachineName**](inapsystemhealthvalidationrequest-getmachinename-method.md)                 | 由驗證程式用來取得電腦名稱稱。 然後，驗證程式必須記錄這些資訊。<br/>             |
| [**INapSystemHealthValidationRequest::GetPrivateData**](inapsystemhealthvalidationrequest-getprivatedata-method.md)                 | 允許 NapServer 捕獲狀態資訊。<br/>                                                        |
| [**INapSystemHealthValidationRequest::GetSoHRequest**](inapsystemhealthvalidationrequest-getsohrequest-method.md)                   | 允許驗證程式取出並驗證 SoHRequest 資訊。<br/>                                     |
| [**INapSystemHealthValidationRequest::GetSoHResponse**](inapsystemhealthvalidationrequest-getsohresponse-method.md)                 | 取得 SoHResponse 物件。<br/>                                                                               |
| [**INapSystemHealthValidationRequest::GetStringCorrelationId**](inapsystemhealthvalidationrequest-getstringcorrelationid-method.md) | 由驗證程式用來取出唯一的交換識別碼。 然後，驗證程式必須記錄這些資訊。<br/> |
| [**INapSystemHealthValidationRequest::SetPrivateData**](inapsystemhealthvalidationrequest-setprivatedata-method.md)                 | 允許 NapServer 儲存狀態資訊。<br/>                                                           |
| [**INapSystemHealthValidationRequest::SetSoHResponse**](inapsystemhealthvalidationrequest-setsohresponse-method.md)                 | 允許驗證程式設定 SoHResponse。<br/>                                                                  |



 

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

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

