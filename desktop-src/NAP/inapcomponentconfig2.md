---
title: 'INapComponentConfig2 介面 (NapCommon .h) '
description: 提供適用于系統健全狀況驗證程式的 NAP 系統組態方法 (Shv) 從遠端設定 NPS) 使用者介面的網路原則 (伺服器。
ms.assetid: 35150184-300c-4ea4-bff9-b3c33fa3156b
keywords:
- INapComponentConfig2 介面 NAP
- INapComponentConfig2 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapComponentConfig2
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29bd6fbea7696d0e4d5eacefd028ce7d33e549e0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106965708"
---
# <a name="inapcomponentconfig2-interface"></a>INapComponentConfig2 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapComponentConfig2** 介面會為系統健康狀態驗證 (SHV 提供 NAP 系統組態方法，) 在遠端 (NPS) 使用者介面設定網路原則伺服器。

> [!Note]  
> 此介面會繼承 [**INapComponentConfig**](inapcomponentconfig.md) 的所有方法，因此應該改用。

 

## <a name="members"></a>成員

**INapComponentConfig2** 介面繼承自 [**INapComponentConfig**](inapcomponentconfig.md)。 **INapComponentConfig2** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapComponentConfig2** 介面具有這些方法。



| 方法                                                                                                | 描述                                                                                                                                                                |
|:------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**INapComponentConfig2::InvokeUIForMachine**](inapcomponentconfig2-invokeuiformachine.md)           | 視需要由 Shv 所執行，以直接在指定的電腦上管理遠端設定。<br/>                                                                 |
| [**INapComponentConfig2::InvokeUIFromConfigBlob**](inapcomponentconfig2-invokeuifromconfigblob.md)   | 視需要由 Shv 所執行，以在記憶體中載入遠端電腦的設定，並顯示允許操作設定資料的 UI。<br/> |
| [**INapComponentConfig2::IsRemoteConfigSupported**](inapcomponentconfig2-isremoteconfigsupported.md) | 由 Shv 執行以指出是否支援遠端設定。<br/>                                                                                      |



 

## <a name="remarks"></a>備註

系統健康情況代理程式 (Sha) 或隔離強制用戶端 (Qec) 不應執行此介面。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>NapCommon。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>NapCommon .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**INapComponentConfig**](inapcomponentconfig.md)
</dt> <dt>

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

 





