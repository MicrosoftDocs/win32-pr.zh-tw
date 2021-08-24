---
description: 註冊提供全域資源集區相關物件的服務。
ms.assetid: B602F6E1-2889-43CF-AAF1-40F339231DB4
title: Msvm_ResourcePoolRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolRegistration
- Msvm_ResourcePoolRegistration.ResourceType
- Msvm_ResourcePoolRegistration.Component
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bbcb0f2e3d5b0dfad884572c90f889d28e47fcffaf328b39d78f02d4c2baa3a6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119535468"
---
# <a name="msvm_resourcepoolregistration-class"></a>Msvm \_ ResourcePoolRegistration 類別

註冊提供全域資源集區相關物件的服務。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Msvm_ResourcePoolRegistration : Msvm_VirtualizationComponentRegistration
{
  Msvm_ResourceTypeDefinition REF ResourceType;
  Msvm_ResourcePoolComponent  REF Component;
};
```

## <a name="members"></a>成員

**Msvm \_ ResourcePoolRegistration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ResourcePoolRegistration** 類別具有這些屬性。

<dl> <dt>

**元件**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ ResourcePoolComponent**](msvm-resourcepoolcomponent.md)**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

實例的參考，該實例描述實此類別的 COM 物件。

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

存取 **Msvm \_ ResourcePoolRegistration** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
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

 

