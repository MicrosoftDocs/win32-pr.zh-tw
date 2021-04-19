---
description: 表示橋接器服務為交換器服務元件的關聯。
ms.assetid: 737d5ba1-0759-40cf-bc46-a059d19902c8
title: CIM_SwitchServiceTransparentBridging 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SwitchServiceTransparentBridging
- CIM_SwitchServiceTransparentBridging.GroupComponent
- CIM_SwitchServiceTransparentBridging.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 04bce4bf673dc029b7b3a2d2b837670b01300c73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106992026"
---
# <a name="cim_switchservicetransparentbridging-class"></a>CIM \_ SwitchServiceTransparentBridging 類別

表示橋接器服務為交換器服務元件的關聯。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::SwitchingBridging")]
class CIM_SwitchServiceTransparentBridging : CIM_ServiceComponent
{
  CIM_SwitchService              REF GroupComponent;
  CIM_TransparentBridgingService REF PartComponent;
};
```

## <a name="members"></a>成員

**CIM \_ SwitchServiceTransparentBridging** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ SwitchServiceTransparentBridging** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ SwitchService**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

Switch 服務的 [**CIM \_ SwitchService**](cim-switchservice.md) 參考。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ TransparentBridgingService**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 
</dt> </dl>

元件橋接服務的 [**CIM \_ TransparentBridgingService**](cim-transparentbridgingservice.md) 參考。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ServiceComponent**](cim-servicecomponent.md)
</dt> </dl>

 

