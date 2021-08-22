---
description: 表示系統元件關聯的特製化，該關聯會建立資源集區是在系統的內容中定義的。
ms.assetid: 72b68687-2b5f-4fef-bdca-a5c0bbfa3564
title: Msvm_HostedResourcePool 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_HostedResourcePool
- Msvm_HostedResourcePool.GroupComponent
- Msvm_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ce61d5ee2c0b676e9c4ab6099bd592533e7821ae5cd529499c111f4c5349221e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119531278"
---
# <a name="msvm_hostedresourcepool-class"></a>Msvm \_ HostedResourcePool 類別

表示系統元件關聯的特製化，該關聯會建立資源集區是在系統的內容中定義的。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Composition, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_HostedResourcePool : CIM_SystemComponent
{
  Msvm_ComputerSystem REF GroupComponent;
  CIM_ResourcePool    REF PartComponent;
};
```

## <a name="members"></a>成員

**Msvm \_ HostedResourcePool** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ HostedResourcePool** 類別具有這些屬性。

<dl> <dt>

**GroupComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_**](msvm-computersystem.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "GroupComponent" ) 、 [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

關聯中的父系統。

</dd> <dt>

**PartComponent**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85))**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "PartComponent" ) 
</dt> </dl>

系統元件的資源集區。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

