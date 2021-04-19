---
description: 表示 Microsoft Windows Hyper-v 平臺的資源集區元素。
ms.assetid: DF48E8A6-240F-44E9-9DA3-1E6694396F10
title: Msvm_ResourcePoolComponent 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolComponent
- Msvm_ResourcePoolComponent.CLSID
- Msvm_ResourcePoolComponent.Context
- Msvm_ResourcePoolComponent.Enabled
- Msvm_ResourcePoolComponent.Name
- Msvm_ResourcePoolComponent.AllocationCapabilitiesClassName
- Msvm_ResourcePoolComponent.ResourcePoolClassName
- Msvm_ResourcePoolComponent.ResourcePoolSettingDataClassName
- Msvm_ResourcePoolComponent.PhysicalDeviceClassName
- Msvm_ResourcePoolComponent.WmiFactoryCLSID
- Msvm_ResourcePoolComponent.MaxParentPools
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a0cf64a9e01d904aa4e6c6ec263fdeec92eb7c94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106992056"
---
# <a name="msvm_resourcepoolcomponent-class"></a>Msvm \_ ResourcePoolComponent 類別

表示 Microsoft Windows Hyper-v 平臺的資源集區元素。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
class Msvm_ResourcePoolComponent : Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
  string  AllocationCapabilitiesClassName;
  string  ResourcePoolClassName;
  string  ResourcePoolSettingDataClassName = "Msvm_ResourcePoolSettingData";
  string  PhysicalDeviceClassName;
  string  WmiFactoryCLSID;
  uint8   MaxParentPools = 0;
};
```

## <a name="members"></a>成員

**Msvm \_ ResourcePoolComponent** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ ResourcePoolComponent** 類別具有這些屬性。

<dl> <dt>

**AllocationCapabilitiesClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

衍生自 [**CIM \_ AllocationCapabilities**](/previous-versions/windows/desktop/clushyperv/cim-allocationcapabilities) 的類別名稱，可描述此資源集區的配置功能。

</dd> <dt>

**Clsid**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**GUID** ，表示服務 COM 物件的類別識別碼。 這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)。

</dd> <dt>

**內容**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

新建立的物件將在其中執行的內容。 此值會在 *dwClsCoNtext* 參數中傳遞至 **CoCreateInstance**。 這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)，而且一律設定為1。

</dd> <dt>

**Enabled**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

如果這個實例已啟用，而且可以用來完成用戶端要求，則為 **True** 。否則 **為 False**。 這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)，而且一律設定為 **True**。

</dd> <dt>

**MaxParentPools**
</dt> <dd> <dl> <dt>

資料類型： **uint8**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

子集區支援的父資源集區數目上限。

</dd> <dt>

**名稱**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞：索引 **鍵**
</dt> </dl>

特定語言的字串，可唯一識別元素。 建議採用下列格式來防止命名衝突：「廠商 \| 元件 \| 版本」。 例如，此名稱代表 Microsoft 模擬網路埠元件的1.0 版：「Microsoft EmulatedNetworkPortComponent v1.0 \| 」 \| 。 這個屬性繼承自 [**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)。

</dd> <dt>

**PhysicalDeviceClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

衍生自 [**CIM \_ LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) 的類別名稱，這個類別會從這個集區配置資源的實體裝置。 如果配置自這個集區的虛擬裝置類別與實體裝置類別相同，則此屬性可以是 **Null** 。

</dd> <dt>

**ResourcePoolClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

從執行資源集區之 [**CIM \_ ResourcePool**](/previous-versions//cc136903(v=vs.85)) 衍生的類別名稱。

</dd> <dt>

**ResourcePoolSettingDataClassName**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

衍生自 [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) 的類別名稱，此名稱會描述資源集區的非配置相關設定。

</dd> <dt>

**WmiFactoryCLSID**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

**GUID** ，表示元件之 WMI 物件 factory 的類別識別碼。

</dd> </dl>

## <a name="remarks"></a>備註

存取 **Msvm \_ ResourcePoolComponent** 類別可能受 UAC 篩選所限制。 如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi)。

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

[**Msvm \_ VirtualizationComponent**](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[**Msvm \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)
</dt> </dl>

 

