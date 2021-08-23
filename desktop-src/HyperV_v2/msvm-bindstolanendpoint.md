---
description: 此關聯會 (SAP) 來建立服務存取點，做為通訊協定端點的通訊協定服務要求者。
ms.assetid: 14edefd8-d59b-4925-8b78-a979fb9a975f
title: Msvm_BindsToLANEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_BindsToLANEndpoint
- Msvm_BindsToLANEndpoint.Antecedent
- Msvm_BindsToLANEndpoint.Dependent
- Msvm_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 44dc8d88475b23d8d7ac12ec36eba96376cf19b7d4d3168556519597d445c73d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119870401"
---
# <a name="msvm_bindstolanendpoint-class"></a>Msvm \_ BindsToLANEndpoint 類別

此關聯會 (SAP) 來建立服務存取點，做為通訊協定端點的通訊協定服務要求者。 此關聯通常會在單一系統上的 Sap 和端點之間執行。 因為通訊協定端點是一種 SAP，所以這個系結可用來建立兩個通訊協定的分層，其中的上層層是由 **相依** 性和較低 **層所表示。**

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_BindsToLANEndpoint : CIM_BindsToLANEndpoint
{
  Msvm_LANEndpoint  REF Antecedent;
  Msvm_VLANEndpoint REF Dependent;
  uint16                FrameType;
};
```

## <a name="members"></a>成員

**Msvm \_ BindsToLANEndpoint** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ BindsToLANEndpoint** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

代表切換埠之 [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) 類別的參考。 這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

與切換埠相關聯之 [**Msvm \_ VLANEndpoint**](msvm-vlanendpoint.md) 的參考。 這個屬性繼承自 [**CIM 相依 \_**](/windows/desktop/CIMWin32Prov/cim-dependency)性。

</dd> <dt>

**FrameType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

描述系結至 LAN 端點的上層 SAP 或端點的框架方法。 這個屬性繼承自 **CIM \_ BindsToLANEndpoint**，而且一律設定為 **Null**。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

