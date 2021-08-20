---
description: 代表父乙太網路交換器擴充功能與子乙太網路交換器擴充功能之間的關聯。
ms.assetid: a0a60214-d85d-4c64-b720-1c34abc25287
title: Msvm_ParentEthernetSwitchExtension 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ParentEthernetSwitchExtension
- Msvm_ParentEthernetSwitchExtension.Antecedent
- Msvm_ParentEthernetSwitchExtension.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5cefc1560317908b647f49e0c033897cd36e3bf7661fdc0b9bd6786fbf4998ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117811208"
---
# <a name="msvm_parentethernetswitchextension-class"></a>Msvm \_ ParentEthernetSwitchExtension 類別

代表父乙太網路交換器擴充功能與子乙太網路交換器擴充功能之間的關聯。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ParentEthernetSwitchExtension : CIM_Dependency
{
  Msvm_EthernetSwitchExtension REF Antecedent;
  Msvm_EthernetSwitchExtension REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ ParentEthernetSwitchExtension** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ParentEthernetSwitchExtension** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

代表父 switch 擴充的 [**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) 類別實例的參考。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

代表子 switch 擴充的 [**Msvm \_ EthernetSwitchExtension**](msvm-ethernetswitchextension.md) 類別之實例的參考。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

