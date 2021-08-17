---
description: 將交換器埠連接到埠所連接的 LAN 端點。
ms.assetid: 963EC004-6A67-4F75-BD93-1BCD17F32490
title: Msvm_ActiveConnection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ActiveConnection
- Msvm_ActiveConnection.Antecedent
- Msvm_ActiveConnection.Dependent
- Msvm_ActiveConnection.TrafficType
- Msvm_ActiveConnection.OtherTrafficDescription
- Msvm_ActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2f8326fe50d3fef4e7776fa865afdd730416cb38fccd6347b4b27f0079966501
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693608"
---
# <a name="msvm_activeconnection-class"></a>Msvm \_ ActiveConnection 類別

將交換器埠連接到埠所連接的 LAN 端點。 此物件的存在表示交換器埠和 LAN 端點會主動連線，而且與 LAN 端點相關聯的乙太網路埠可透過交換器埠與網路通訊。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ActiveConnection : CIM_ActiveConnection
{
  Msvm_LANEndpoint REF Antecedent;
  CIM_LANEndpoint  REF Dependent;
  uint16               TrafficType;
  string               OtherTrafficDescription;
  boolean              IsUnidirectional;
};
```

## <a name="members"></a>成員

**Msvm \_ ActiveConnection** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ActiveConnection** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **[ **Msvm \_ LANEndpoint**](msvm-lanendpoint.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

代表服務存取點的 [**Msvm \_ LANEndpoint**](msvm-lanendpoint.md) 類別實例的參考， (設定為通訊或正在主動與相依 SAP 進行通訊的 sap) 。 在單向連接中，此 SAP 是正在傳輸的。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **[ **CIM \_ LANEndpoint**](cim-lanendpoint.md)**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**Msvm \_ LANEndpoint**](cim-lanendpoint.md)類別實例的參考，代表已設定為要進行通訊或正在主動與之前的 SAP 通訊的 sap。 在單向連接中，此 SAP 是接收的。

</dd> <dt>

**IsUnidirectional**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果這個屬性為 **True**，則這個連接是單向的。否則，此連接是雙向的。 當連接為單向時，「說話者」應定義為前一個 **參考。** 在雙向連接中，所選存取點是否為 **Antecedent** 或 **相依** 的，並不重要。 這個屬性繼承自 [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))。

</dd> <dt>

**OtherTrafficDescription**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))，但不會使用它。

</dd> <dt>

**TrafficType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性繼承自 [**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))，但不會使用它。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ ActiveConnection** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

## <a name="examples"></a>範例

請參閱 [查詢網路物件](querying-networking-objects.md)。

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

[**CIM \_ ActiveConnection**](cim-activeconnection.md)
</dt> <dt>

[**CIM \_ ActiveConnection**](/previous-versions//cc136779(v=vs.85))
</dt> </dl>

 

