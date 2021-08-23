---
description: Msvm \_ EthernetSwitchPort 類別的實例與 Msvm EthernetPortData 類別的實例之間的關聯 \_ ，代表由交換器擴充功能所收集之埠的資料。
ms.assetid: 08677914-af09-47b7-9d4d-406696e1f504
title: Msvm_EthernetPortInfo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_EthernetPortInfo
- Msvm_EthernetPortInfo.Antecedent
- Msvm_EthernetPortInfo.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 3ef8f8f4ab7191400cfead94d20c4f601b97e48d46ee160d31c7b26b8e567b92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119524888"
---
# <a name="msvm_ethernetportinfo-class"></a>Msvm \_ EthernetPortInfo 類別

[**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md)類別的實例與 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md)類別的實例之間的關聯，代表由交換器擴充功能所收集之埠的資料。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_EthernetPortInfo : CIM_Dependency
{
  Msvm_EthernetSwitchPort REF Antecedent;
  Msvm_EthernetPortData   REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ EthernetPortInfo** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ EthernetPortInfo** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_ EthernetSwitchPort**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性 \_ 。前面」 ) 
</dt> </dl>

代表切換埠之 [**Msvm \_ EthernetSwitchPort**](msvm-ethernetswitchport.md) 類別的實例。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_ EthernetPortData**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性依存」 \_ ) 
</dt> </dl>

表示埠資料之 [**Msvm \_ EthernetPortData**](msvm-ethernetportdata.md) 類別的實例。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

