---
description: 表示 Microsoft Hyper-V 平臺中的服務註冊。
ms.assetid: 706557C2-49D6-453F-9DC0-2C655888EEBE
title: Msvm_VirtualizationComponentRegistration 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponentRegistration
- Msvm_VirtualizationComponentRegistration.Component
- Msvm_VirtualizationComponentRegistration.ResourceType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c7acd111ab95f59146763e874d40c4efb411313938c94b1a4527aa1e2d08490c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118146552"
---
# <a name="msvm_virtualizationcomponentregistration-class"></a>Msvm \_ VirtualizationComponentRegistration 類別

表示 Microsoft Hyper-V 平臺中的服務註冊。

下列語法已簡化受控物件格式 (MOF) 程式碼。

## <a name="syntax"></a>語法

``` syntax
class Msvm_VirtualizationComponentRegistration
{
  Msvm_VirtualizationComponent REF Component;
  Msvm_ResourceTypeDefinition  REF ResourceType;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualizationComponentRegistration** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualizationComponentRegistration** 類別具有這些屬性。

<dl> <dt>

**元件**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)**
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

描述服務所支援之資源類型之實例的參考。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ VirtualizationComponentRegistration** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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



 

