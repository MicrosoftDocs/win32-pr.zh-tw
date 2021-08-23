---
description: 用於 Msvm VssService 類別中的 QueryGuestClusterInformation 方法 \_ ，以抓取 VM 所屬之來賓叢集的相關資訊。
ms.assetid: c484b38d-9137-44da-a368-a2a673b94ef8
title: Msvm_GuestClusterInformation 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GuestClusterInformation
- Msvm_GuestClusterInformation.ClusterId
- Msvm_GuestClusterInformation.ClusterSize
- Msvm_GuestClusterInformation.SharedVirtualHardDisks
- Msvm_GuestClusterInformation.SharedVirtualHardDiskPaths
- Msvm_GuestClusterInformation.IsClustered
- Msvm_GuestClusterInformation.IsOnline
- Msvm_GuestClusterInformation.IsOwned
- Msvm_GuestClusterInformation.IsActiveActive
- Msvm_GuestClusterInformation.LastResourceMoveTime
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ed353e0d9c4d3049e120b00a11bc3d1bf85e3a0b42e52deb4ed277b9bde9b96b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119523290"
---
# <a name="msvm_guestclusterinformation-class"></a>Msvm \_ GuestClusterInformation 類別

用於 [**Msvm \_ VssService**](msvm-vssservice.md)類別中的 [**QueryGuestClusterInformation**](msvm-vssservice-queryguestclusterinformation.md)方法，以抓取 VM 所屬之來賓叢集的相關資訊。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GuestClusterInformation
{
  string  ClusterId;
  uint16  ClusterSize;
  string  SharedVirtualHardDisks[];
  string  SharedVirtualHardDiskPaths[];
  boolean IsClustered[];
  boolean IsOnline[];
  boolean IsOwned[];
  boolean IsActiveActive[];
  uint64  LastResourceMoveTime;
};
```

## <a name="members"></a>成員

**Msvm \_ GuestClusterInformation** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ GuestClusterInformation** 類別具有這些屬性。

<dl> <dt>

**ClusterId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

VM 的客體作業系統所屬之容錯移轉叢集的識別碼。

</dd> <dt>

**ClusterSize**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

VM 的客體作業系統所屬叢集中的節點數目。

</dd> <dt>

**IsActiveActive**
</dt> <dd> <dl> <dt>

資料類型： **布林** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

布林值陣列，對應至每個共用虛擬硬碟，指出是否在主動/主動模式的 Vm 之間共用來賓叢集中對應的磁片資源。

</dd> <dt>

**IsClustered**
</dt> <dd> <dl> <dt>

資料類型： **布林** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

布林值陣列，對應至每個共用虛擬硬碟，指出對應的磁片是否為來賓叢集中的叢集資源。

</dd> <dt>

**IsOnline**
</dt> <dd> <dl> <dt>

資料類型： **布林** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

布林值陣列，對應至每個共用虛擬硬碟，指出來賓叢集中對應的磁片資源是否在線上。

</dd> <dt>

**IsOwned**
</dt> <dd> <dl> <dt>

資料類型： **布林** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

布林值陣列，對應至每個共用虛擬硬碟，指出來賓叢集中對應的磁片資源是否為此 VM 所擁有的目前。

</dd> <dt>

**LastResourceMoveTime**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

上次移動其中一個共用磁片資源時的時鐘滴答計數。

> [!Note]  
> 這個屬性是在 Windows 10、1703版和 Windows Server 2016 中加入的。

 

</dd> <dt>

**SharedVirtualHardDiskPaths**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

連線至 VM 的共用虛擬硬碟路徑陣列。

</dd> <dt>

**SharedVirtualHardDisks**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> <dt>

限定詞： [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ( 「已編制索引」 ) 
</dt> </dl>

資源配置設定資料 (RASD) 的陣列，代表連線至 VM 的共用虛擬硬碟。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

