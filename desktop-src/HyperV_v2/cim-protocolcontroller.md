---
description: 代表控制器的群組，這些控制器控制起始通訊協定之裝置的作業和運作。
ms.assetid: fb6b65d4-3a1a-47b1-afc7-9b10e8eeaa32
title: CIM_ProtocolController 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProtocolController
- CIM_ProtocolController.MaxUnitsControlled
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7dcd0f0ca1891914e2c4fc3fedbc0012d930dbaec99926f9db8e013435367f36
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119148505"
---
# <a name="cim_protocolcontroller-class"></a>CIM \_ ProtocolController 類別

代表控制器的群組，這些控制器控制起始通訊協定之裝置的作業和運作。

## <a name="syntax"></a>語法

``` syntax
[Abstract, Version("2.8.0"), UMLPackagePath("CIM::Device::ProtocolController"), AMENDMENT]
class CIM_ProtocolController : CIM_LogicalDevice
{
  uint32 MaxUnitsControlled;
};
```

## <a name="members"></a>成員

**CIM \_ ProtocolController** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ ProtocolController** 類別具有這些屬性。

<dl> <dt>

**MaxUnitsControlled**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

可透過通訊協定控制器控制或存取的單位數目上限。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md)
</dt> </dl>

 

 




