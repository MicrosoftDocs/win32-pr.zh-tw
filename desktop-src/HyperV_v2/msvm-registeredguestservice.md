---
description: 代表 Msvm \_ GuestServiceInterfaceComponent 實例與 Msvm GuestService 實例之間的關聯 \_ ，代表在來賓中執行的服務。
ms.assetid: 246CFAC1-7D83-4DE7-B9D3-96326511E08B
title: Msvm_RegisteredGuestService 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_RegisteredGuestService
- Msvm_RegisteredGuestService.Antecedent
- Msvm_RegisteredGuestService.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cf2e551a30f169477f9dc73e58ecd9e6c3a78b708c047eb0088f36782623da3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130438"
---
# <a name="msvm_registeredguestservice-class"></a>Msvm \_ RegisteredGuestService 類別

代表 [**Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md) 實例與 [**Msvm \_ GuestService**](msvm-guestservice.md)實例之間的關聯，代表在來賓中執行的服務。 此類別衍生自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency) 性類別。

下列語法是簡化自 MOF 程式碼，且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_RegisteredGuestService : CIM_Dependency
{
  Msvm_GuestServiceInterfaceComponent REF Antecedent;
  Msvm_GuestService                   REF Dependent;
};
```

## <a name="members"></a>成員

**Msvm \_ RegisteredGuestService** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ RegisteredGuestService** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ GuestServiceInterfaceComponent**](msvm-guestserviceinterfacecomponent.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性 \_ 。前面」 ) 
</dt> </dl>

此關聯中 guest 服務介面元件的參考。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ GuestService**](msvm-guestservice.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「CIM 相依性依存」 \_ ) 
</dt> </dl>

參考相依于 **Antecedent** 屬性的已註冊來賓服務。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ 相依性**](cim-dependency.md)
</dt> <dt>

[**CIM \_ 相依性**](/windows/desktop/CIMWin32Prov/cim-dependency)
</dt> </dl>

 

