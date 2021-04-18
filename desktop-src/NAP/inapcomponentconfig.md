---
title: 'INapComponentConfig 介面 (NapCommon .h) '
description: 針對 (Shv) 的系統健全狀況驗證程式提供 NAP 系統組態方法。
ms.assetid: 979b5c34-8efe-4c48-8236-53fbd25d4249
keywords:
- INapComponentConfig 介面 NAP
- INapComponentConfig 介面 NAP，描述
topic_type:
- apiref
api_name:
- INapComponentConfig
api_location:
- NapCommon.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 63a13ae74ba1de79803ff4a2d3716eec7fe934a1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104384390"
---
# <a name="inapcomponentconfig-interface"></a>INapComponentConfig 介面

> [!Note]  
> 從 Windows 10 開始，無法使用網路存取保護平臺

 

**INapComponentConfig** 介面會為 (shv) 的系統健全狀況驗證程式提供 NAP 系統組態方法。

> [!Note]  
> [**INapComponentConfig2**](inapcomponentconfig2.md) 和 [**INapComponentConfig3**](inapcomponentconfig3.md) 會繼承此介面的所有方法，因此應該改用。

 

## <a name="members"></a>成員

**INapComponentConfig** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **INapComponentConfig** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**INapComponentConfig** 介面具有這些方法。



| 方法                                                                          | 描述                                                                          |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------|
| [**INapComponentConfig::GetConfig**](inapcomponentconfig-getconfig.md)         | 捕獲 SHV 元件設定。<br/>                                |
| [**INapComponentConfig::InvokeUI**](inapcomponentconfig-invokeui.md)           | 啟動 SHV 元件的自訂使用者介面。<br/>              |
| [**INapComponentConfig::IsUISupported**](inapcomponentconfig-isuisupported.md) | 指定 SHV 元件是否支援自訂的使用者介面。<br/> |
| [**INapComponentConfig::SetConfig**](inapcomponentconfig-setconfig.md)         | 設定 SHV 元件設定。<br/>                                     |



 

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

[NAP 介面](nap-interfaces.md)
</dt> <dt>

[NAP 參考](nap-reference.md)
</dt> </dl>

 

