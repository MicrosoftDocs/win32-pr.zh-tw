---
description: CIM \_ DeviceConnection 關聯類別代表兩個或多個已連線的裝置。
ms.assetid: 82095cd6-1843-4db2-9fe8-3e225611bd3b
ms.tgt_platform: multiple
title: 'CIM_DeviceConnection 類別 (CIMWin32 WMI 提供者) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_DeviceConnection
- CIM_DeviceConnection.Dependent
- CIM_DeviceConnection.Antecedent
- CIM_DeviceConnection.NegotiatedDataWidth
- CIM_DeviceConnection.NegotiatedSpeed
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b8179287686439ea31c19d700a785de7fff47659
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187763"
---
# <a name="cim_deviceconnection-class-cimwin32-wmi-providers"></a>CIM_DeviceConnection 類別 (CIMWin32 WMI 提供者) 

**CIM \_ DeviceConnection** 關聯類別代表兩個或多個已連線的裝置。

> [!IMPORTANT]
> DMTF (分散式管理工作強制) CIM (通用訊息模型) 類別是用來建立 WMI 類別的父類別。 WMI 目前僅支援 [CIM 2.x 版的架構](https://dmtf.org/standards/cim/schemas)。

 

下列語法已從受管理物件格式 (MOF) 程式碼加以簡化，並包含所有繼承的屬性。 屬性會依字母順序列出，而不是依 MOF 順序列出。

## <a name="syntax"></a>語法

``` syntax
[Abstract, UUID("{8502C53C-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_DeviceConnection : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_LogicalDevice REF Antecedent;
  uint32                NegotiatedDataWidth;
  uint64                NegotiatedSpeed;
};
```

## <a name="members"></a>成員

**CIM \_ DeviceConnection** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**CIM \_ DeviceConnection** 類別具有這些屬性。

<dl> <dt>

**先行**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalDevice**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( "Antecedent" ) 
</dt> </dl>

描述邏輯裝置的 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 。

</dd> <dt>

**依賴**
</dt> <dd> <dl> <dt>

資料類型： **CIM \_ LogicalDevice**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：覆 [**寫**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「相依」 ) 
</dt> </dl>

[**CIM \_ LogicalDevice**](cim-logicaldevice.md) ，描述連接到前一個裝置的第二個邏輯裝置。

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

</dd> </dl>

## <a name="remarks"></a>備註

**Cim \_ DeviceConnection** 類別衍生自 cim 相依 [**性 \_**](cim-dependency.md)。

WMI 不會執行這個類別。 如需衍生自 **CIM \_ DeviceConnection** 之類別的詳細資訊，請參閱 [Win32 類別](win32-provider.md)。

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

[**CIM \_ 相依性**](cim-dependency.md)
</dt> </dl>

 

