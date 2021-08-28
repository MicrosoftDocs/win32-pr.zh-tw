---
description: 代表 GPU 磁碟分割裝置的設定狀態。
ms.assetid: 33ec4ea2-4e79-4c84-8abe-da8308ad6702
title: Msvm_GpuPartitionSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_GpuPartitionSettingData
- Msvm_GpuPartitionSettingData.MinPartitionVRAM
- Msvm_GpuPartitionSettingData.MaxPartitionVRAM
- Msvm_GpuPartitionSettingData.OptimalPartitionVRAM
- Msvm_GpuPartitionSettingData.MinPartitionEncode
- Msvm_GpuPartitionSettingData.MaxPartitionEncode
- Msvm_GpuPartitionSettingData.OptimalPartitionEncode
- Msvm_GpuPartitionSettingData.MinPartitionDecode
- Msvm_GpuPartitionSettingData.MaxPartitionDecode
- Msvm_GpuPartitionSettingData.OptimalPartitionDecode
- Msvm_GpuPartitionSettingData.MinPartitionCompute
- Msvm_GpuPartitionSettingData.MaxPartitionCompute
- Msvm_GpuPartitionSettingData.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 39fe0f5a794875c25cf844c39df2217fae04d1b791a5a5174358fa0ea70150ab
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014526"
---
# <a name="msvm_gpupartitionsettingdata-class"></a>Msvm \_ GpuPartitionSettingData 類別

代表 GPU 磁碟分割裝置的設定狀態。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_GpuPartitionSettingData : CIM_ResourceAllocationSettingData
{
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a>成員

**Msvm \_ GpuPartitionSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ GpuPartitionSettingData** 類別具有這些屬性。

<dl> <dt>

**MaxPartitionCompute**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

要出現在 GPU 磁碟分割中的計算引擎數量上限。

</dd> <dt>

**MaxPartitionDecode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

要出現在 GPU 磁碟分割中的解碼引擎量上限。

</dd> <dt>

**MaxPartitionEncode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

在 GPU 磁碟分割中會出現的編碼引擎最大數量。

</dd> <dt>

**MaxPartitionVRAM**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

要出現在 GPU 分割區中的最大 VRAM 數量。

</dd> <dt>

**MinPartitionCompute**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

將會出現在 GPU 磁碟分割中的最小計算引擎量。

</dd> <dt>

**MinPartitionDecode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

將會出現在 GPU 磁碟分割中的解碼引擎最小數量。

</dd> <dt>

**MinPartitionEncode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

將會出現在 GPU 磁碟分割中的編碼引擎最小數量。

</dd> <dt>

**MinPartitionVRAM**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

要出現在 GPU 磁碟分割中的最小 VRAM 量。

</dd> <dt>

**OptimalPartitionCompute**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

將會出現在 GPU 磁碟分割中的最佳計算引擎量。

</dd> <dt>

**OptimalPartitionDecode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

將會出現在 GPU 磁碟分割中的最佳解碼引擎量。

</dd> <dt>

**OptimalPartitionEncode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

將會出現在 GPU 磁碟分割中的最佳編碼引擎數量。

</dd> <dt>

**OptimalPartitionVRAM**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

將會出現在 GPU 磁碟分割中的最佳 VRAM 量。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

 




