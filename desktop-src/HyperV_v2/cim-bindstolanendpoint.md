---
description: 表示 CIM \_ ServiceAccessPoint 或 cim \_ ProtocolEndpoint 物件相依于 \_ 相同系統上的基礎 CIM LANEndpoint 物件的關聯。
ms.assetid: 3c015fbd-0611-41e8-a79a-01c980eedfd3
title: CIM_BindsToLANEndpoint 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_BindsToLANEndpoint
- CIM_BindsToLANEndpoint.Antecedent
- CIM_BindsToLANEndpoint.Dependent
- CIM_BindsToLANEndpoint.FrameType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dff1cf243b54739509343d6d8958aa2a54f464b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987295"
---
# <a name="cim_bindstolanendpoint-class"></a>CIM \_ BindsToLANEndpoint 類別

表示 [**CIM \_ ServiceAccessPoint**](cim-serviceaccesspoint.md) 或 [**cim \_ ProtocolEndpoint**](cim-protocolendpoint.md) 物件相依于相同系統上的基礎 [**CIM \_ LANEndpoint**](cim-lanendpoint.md) 物件的關聯。

## <a name="syntax"></a>語法

``` syntax
[Association, Abstract, Version("2.6.0"), UMLPackagePath("CIM::Network::ProtocolEndpoints"), AMENDMENT]
class CIM_BindsToLANEndpoint : CIM_BindsTo
{
  CIM_LANEndpoint        REF Antecedent;
  CIM_ServiceAccessPoint REF Dependent;
  uint16                     FrameType;
};
```

## <a name="members"></a>成員

**CIM \_ BindsToLANEndpoint** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ BindsToLANEndpoint** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LANEndpoint**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

基礎 [**CIM \_ LANEndpoint**](cim-lanendpoint.md) 物件。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ ServiceAccessPoint**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

相依于 [**cim \_ LANEndpoint**](cim-lanendpoint.md)的 [**cim \_ ServiceAccessPoint**](cim-serviceaccesspoint.md)或 [**cim \_ ProtocolEndpoint**](cim-protocolendpoint.md)物件。

</dd> <dt>

**FrameType**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上層服務存取點或通訊協定端點的框架方法。

> [!Note]  
> 只有在使用 IPX 通訊協定時，才會知道原始802.3。

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

**Ethernet** (1) 


</dt> <dd></dd> <dt>

<span id="802.2"></span>

**802.2** (2) 


</dt> <dd></dd> <dt>

<span id="SNAP"></span><span id="snap"></span>

**貼齊** (3) 


</dt> <dd></dd> <dt>

<span id="Raw802.3"></span><span id="raw802.3"></span><span id="RAW802.3"></span>

**原始的 802.3** (4) 


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8<br/>                                                                                    |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ BindsTo**](cim-bindsto.md)
</dt> </dl>

 

