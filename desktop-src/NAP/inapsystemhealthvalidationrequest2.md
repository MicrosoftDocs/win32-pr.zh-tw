---
title: 'INapSystemHealthValidationRequest2 介面 (NapSystemHealthValidator .h) '
description: 提供用來支援應用程式開發人員所定義之系統健全狀況驗證程式的方法。
ms.assetid: 12094203-bb6c-4028-9baf-a2a9b124ce6d
keywords:
- INapSystemHealthValidationRequest2 介面 NAP
- INapSystemHealthValidationRequest2 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthValidationRequest2
api_location:
- qshvhost.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b6438394120ecd901c6de6d7a8ccac40f742d9f73d27a36682de894d9c5a7ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118620847"
---
# <a name="inapsystemhealthvalidationrequest2-interface"></a>INapSystemHealthValidationRequest2 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthValidationRequest2** 介面提供的方法可用來支援應用程式開發人員所定義的系統健全狀況驗證程式。

> [!Note]  
> 此介面會繼承 [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md) 的所有方法，因此應該改用。

 

## <a name="members"></a>成員

**INapSystemHealthValidationRequest2** 介面繼承自 [**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)。 **INapSystemHealthValidationRequest2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapSystemHealthValidationRequest2** 介面具有這些方法。



| 方法                                                                                                    | 描述                                                        |
|:----------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------|
| [**INapSystemHealthValidationRequest2::GetConfigId**](inapsystemhealthvalidationrequest2-getconfigid.md) | 捕獲驗證要求中的設定識別碼。<br/> |



 

## <a name="remarks"></a>備註

如果 SHV 不支援 [**INapComponentConfig3**](inapcomponentconfig3.md)，則不適用此介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                               |
| 最低支援的伺服器<br/> | Windows僅限 Server 2008 R2 \[ desktop 應用程式\]<br/>                                                 |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthValidator。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapSystemHealthValidator .idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Qshvhost.dll</dt> </dl>                 |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapSystemHealthValidationRequest**](inapsystemhealthvalidationrequest.md)
</dt> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

 





