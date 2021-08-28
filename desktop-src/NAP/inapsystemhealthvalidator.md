---
title: 'INapSystemHealthValidator 介面 (NapSystemHealthValidator .h) '
description: 必須由 SHV 開發人員執行，才能讓 NAP 系統與 SHV 進行通訊。
ms.assetid: 0366d919-39b9-4961-9b8b-c4313448391f
keywords:
- INapSystemHealthValidator 介面 NAP
- INapSystemHealthValidator 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapSystemHealthValidator
api_location:
- NapSystemHealthValidator.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7310afe1c61dd61344bd1ed355f78735dc7785f9016bbcbb702073b2a06feba0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119686058"
---
# <a name="inapsystemhealthvalidator-interface"></a>INapSystemHealthValidator 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapSystemHealthValidator** 提供的方法必須由 SHV 開發人員執行，才能讓 NAP 系統與 shv 進行通訊。

## <a name="members"></a>成員

**INapSystemHealthValidator** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapSystemHealthValidator** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapSystemHealthValidator** 介面具有這些方法。



| 方法                                                                                   | 描述                                                                                                                               |
|:-----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapSystemHealthValidator：： Validate**](inapsystemhealthvalidator-validate-method.md) | NAP 系統會呼叫此應用程式定義的方法，以驗證從用戶端接收的 [**SoHRequest**](/windows/win32/api/naptypes/ns-naptypes-soh) 。 <br/> |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                               |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                                    |
| 標頭<br/>                   | <dl> <dt>NapSystemHealthValidator。h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>NapSystemHealthValidator .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

