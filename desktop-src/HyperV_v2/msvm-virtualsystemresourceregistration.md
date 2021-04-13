---
description: 註冊可提供虛擬機器特定資源相關物件的服務。
ms.assetid: 85782C4D-E0A3-4EED-9A26-7928862C559B
title: Msvm_VirtualSystemResourceRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceRegistration
- Msvm_VirtualSystemResourceRegistration.ResourceType
- Msvm_VirtualSystemResourceRegistration.Component
- Msvm_VirtualSystemResourceRegistration.IsRootDevice
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7cef3699de973bd22985215a64100c594f223be9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510991"
---
# <a name="msvm_virtualsystemresourceregistration-class"></a>Msvm \_ VirtualSystemResourceRegistration 類別

註冊可提供虛擬機器特定資源相關物件的服務。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Msvm_VirtualSystemResourceRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition         REF ResourceType;
  Msvm_VirtualSystemResourceComponent REF Component;
  boolean                                 IsRootDevice = False;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualSystemResourceRegistration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualSystemResourceRegistration** 類別具有這些屬性。

<dl> <dt>

**元件**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ VirtualSystemResourceComponent**](msvm-virtualsystemresourcecomponent.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

實例的參考，該實例描述實此類別的 COM 物件。

</dd> <dt>

**IsRootDevice**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果這個註冊指出指定的資源類型是此服務的根 (或不是父系的) 裝置，則為 **True** ;否則 **為 False**。 當 **IsRootDevice** 設定為 **True** 時，只有一個註冊可以存在。 否則，此註冊代表子裝置的對應。 此屬性一律設為 **False**。

</dd> <dt>

**ResourceType**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ ResourceTypeDefinition**](msvm-resourcetypedefinition.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述服務所支援之資源類型之實例的參考。 這個屬性繼承自 [**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ VirtualSystemResourceRegistration** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 用戶端支援結束<br/>    | Windows 8.1<br/>                                                                                  |
| 伺服器支援結束<br/>    | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualizationComponentRegistration**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponentregistration)
</dt> <dt>

[**Msvm \_ VirtualizationComponentRegistration**](msvm-virtualizationcomponentregistration.md)
</dt> </dl>

 

