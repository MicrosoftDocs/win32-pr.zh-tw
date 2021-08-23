---
description: 連接虛擬交換器服務與透明橋接服務的關聯。
ms.assetid: 4DFD73CA-38F0-4C06-BEBE-C684590E50E8
title: Msvm_HostedSwitchService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedSwitchService
- Msvm_HostedSwitchService.Antecedent
- Msvm_HostedSwitchService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 634cff066c602cc4eb684bd7e1a016f9f9c925f19db25a0556fd37cc1e27c5f8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531268"
---
# <a name="msvm_hostedswitchservice-class"></a>Msvm \_ HostedSwitchService 類別

連接虛擬交換器服務與透明橋接服務的關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedSwitchService : CIM_HostedService
{
  Msvm_VirtualEthernetSwitch REF Antecedent;
  CIM_Service                REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ HostedSwitchService** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ HostedSwitchService** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 
</dt> </dl>

代表虛擬交換器之 [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) 類別實例的參考。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ 服務**](/windows/desktop/CIMWin32Prov/cim-service)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 
</dt> </dl>

代表橋接服務之 [**Msvm \_ TransparentBridgingService**](msvm-transparentbridgingservice.md) 類別實例的參考。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ HostedSwitchService** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ HostedService**](cim-hostedservice.md)
</dt> <dt>

[**CIM \_ HostedService**](/windows/desktop/CIMWin32Prov/cim-hostedservice)
</dt> </dl>

 

