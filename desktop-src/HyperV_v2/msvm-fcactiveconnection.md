---
description: 將交換器埠連接到埠所連接的光纖通道端點。
ms.assetid: e2762e0c-2f78-4159-a67c-31213e311072
title: Msvm_FcActiveConnection 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_FcActiveConnection
- Msvm_FcActiveConnection.Antecedent
- Msvm_FcActiveConnection.Dependent
- Msvm_FcActiveConnection.TrafficType
- Msvm_FcActiveConnection.OtherTrafficDescription
- Msvm_FcActiveConnection.IsUnidirectional
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e29330e073266f2f2a8749ec3c70d9e26b35ff7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998251"
---
# <a name="msvm_fcactiveconnection-class"></a>Msvm \_ FcActiveConnection 類別

將交換器埠連接到埠所連接的光纖通道端點。 此物件的存在表示交換器埠和光纖通道端點會主動連線，而且與光纖通道端點相關聯的光纖通道埠可透過交換器埠與網路通訊。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_FcActiveConnection : CIM_ActiveConnection
{
  Msvm_FcEndpoint REF Antecedent;
  Msvm_FcEndpoint REF Dependent;
  uint16              TrafficType;
  string              OtherTrafficDescription;
  boolean             IsUnidirectional;
};
```

## <a name="members"></a>成員

**Msvm \_ FcActiveConnection** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ FcActiveConnection** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_ FcEndpoint**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

代表服務存取點的 [**Msvm \_ FcEndpoint**](msvm-fcendpoint.md) 類別實例的參考， (設定為通訊或正在主動與相依 SAP 進行通訊的 sap) 。 在單向連接中，此 SAP 是正在傳輸的。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **Msvm \_ FcEndpoint**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**Msvm \_ FcEndpoint**](msvm-fcendpoint.md)類別實例的參考，代表已設定為要進行通訊或正在主動與之前的 SAP 通訊的 sap。 在單向連接中，此 SAP 是接收的。

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

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

