---
description: CIM \_ USBControllerHasHub 類別定義了 USB 控制器下游的中樞。
ms.assetid: 38bc0342-3ff0-42c8-9c1e-ea5a5822e1d3
ms.tgt_platform: multiple
title: CIM_USBControllerHasHub 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_USBControllerHasHub
- CIM_USBControllerHasHub.NegotiatedDataWidth
- CIM_USBControllerHasHub.NegotiatedSpeed
- CIM_USBControllerHasHub.AccessState
- CIM_USBControllerHasHub.NumberOfHardResets
- CIM_USBControllerHasHub.NumberOfSoftResets
- CIM_USBControllerHasHub.Dependent
- CIM_USBControllerHasHub.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ba0f6d9a618a194faa8d16f9b2f53c6ce10653cf
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104110052"
---
# <a name="cim_usbcontrollerhashub-class"></a>CIM \_ USBControllerHasHub 類別

**CIM \_ USBControllerHasHub** 類別定義了 USB 控制器下游的中樞。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class CIM_USBControllerHasHub : CIM_ControlledBy
{
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
  uint16                AccessState;
  uint32                NumberOfHardResets;
  uint32                NumberOfSoftResets;
  CIM_USBHub        REF Dependent;
  CIM_USBController REF Antecedent;
};
```

## <a name="members"></a>成員

**CIM \_ USBControllerHasHub** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ USBControllerHasHub** 類別具有這些屬性。

<dl> <dt>

**AccessState**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指出控制器是否正在主動命令或存取裝置。 當邏輯裝置可透過多個控制器來發出或存取時，這項資訊是必要的。

這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**未知** 的 (0) 


</dt> <dd></dd> <dt>

<span id="Active"></span><span id="active"></span><span id="ACTIVE"></span>

**Active** (1) 


</dt> <dd></dd> <dt>

<span id="Inactive"></span><span id="inactive"></span><span id="INACTIVE"></span>

**非** 使用中 (2) 


</dt> <dd></dd> </dl>

</dd> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ USBController**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 、 [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 、 [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

描述 USBController 的 [**CIM \_ USBController**](cim-usbcontroller.md) 。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ USBHub**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) ， [**最小**](/windows/desktop/WmiSdk/standard-qualifiers) (1) 
</dt> </dl>

[**CIM \_ USBHub**](cim-usbhub.md) ，描述與控制器相關聯的 USBHub。

</dd> <dt>

**NegotiatedDataWidth**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( "bits" ) 
</dt> </dl>

當有數個匯流排或連接資料寬度時，此屬性會定義裝置之間使用的資料寬度。 資料寬度的指定單位為位。 如果資料寬度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。

這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。

</dd> <dt>

**NegotiatedSpeed**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**單位**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「每秒位數」 ) 
</dt> </dl>

當可能有數個匯流排或連線速度時，此屬性會定義要在裝置之間使用的速率。 以每秒位數指定速度。 如果連線或匯流排速度未經過協商，或此資訊不適用於裝置管理，則應該將屬性設定為 0 (零) 。

如需在腳本中使用 **uint64** 值的詳細資訊，請參閱 [WMI 中的腳本](/windows/desktop/WmiSdk/creating-a-wmi-script)。

這個屬性繼承自 [**CIM \_ DeviceConnection**](cim-deviceconnection.md)。

</dd> <dt>

**NumberOfHardResets**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制器發出的硬重設數目。 硬重設會將裝置傳回到其初始化或啟動狀態。 所有內部裝置狀態資訊和資料都會遺失。

這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。

</dd> <dt>

**NumberOfSoftResets**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

控制器發出的軟重設數目。 軟重設並不會完全清除目前的裝置狀態和資料。 確切的語法取決於裝置，以及用來與其通訊的通訊協定和機制。

這個屬性繼承自 [**CIM \_ ControlledBy**](cim-controlledby.md)。

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ USBControllerHasHub** 類別衍生自 [**cim \_ ControlledBy**](cim-controlledby.md)。

WMI 不會執行這個類別。 針對衍生自 **CIM \_ USBCONTROLLERHASHUB** 的 WMI 類別，請參閱 [Win32 類別](win32-provider.md)。

此檔衍生自 DMTF 所發佈的 CIM 類別描述。 Microsoft 可能已進行變更，以更正次要錯誤、符合 Microsoft SDK 檔標準，或提供詳細資訊。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>                                                                |
| 最低支援的伺服器<br/> | Windows Server 2008<br/>                                                          |
| 命名空間<br/>                | 根 \\ CIMV2<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32 mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ControlledBy**](cim-controlledby.md)
</dt> </dl>

 

