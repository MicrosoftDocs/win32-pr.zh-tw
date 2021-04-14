---
description: 代表可分割 GPU。 每個 GPU 都可以分割成多個 GPU 磁碟分割，而這些分割區可指派給虛擬機器作為 vGPU。
ms.assetid: a32dfc03-6967-4fa3-ae32-bf074137740b
title: Msvm_PartitionableGpu 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_PartitionableGpu
- Msvm_PartitionableGpu.ValidPartitionCounts
- Msvm_PartitionableGpu.PartitionCount
- Msvm_PartitionableGpu.TotalVRAM
- Msvm_PartitionableGpu.AvailableVRAM
- Msvm_PartitionableGpu.MinPartitionVRAM
- Msvm_PartitionableGpu.MaxPartitionVRAM
- Msvm_PartitionableGpu.OptimalPartitionVRAM
- Msvm_PartitionableGpu.TotalEncode
- Msvm_PartitionableGpu.AvailableEncode
- Msvm_PartitionableGpu.MinPartitionEncode
- Msvm_PartitionableGpu.MaxPartitionEncode
- Msvm_PartitionableGpu.OptimalPartitionEncode
- Msvm_PartitionableGpu.TotalDecode
- Msvm_PartitionableGpu.AvailableDecode
- Msvm_PartitionableGpu.MinPartitionDecode
- Msvm_PartitionableGpu.MaxPartitionDecode
- Msvm_PartitionableGpu.OptimalPartitionDecode
- Msvm_PartitionableGpu.TotalCompute
- Msvm_PartitionableGpu.AvailableCompute
- Msvm_PartitionableGpu.MinPartitionCompute
- Msvm_PartitionableGpu.MaxPartitionCompute
- Msvm_PartitionableGpu.OptimalPartitionCompute
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7f82904608a8e2ee4dfa13942066d57d35d511f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852379"
---
# <a name="msvm_partitionablegpu-class"></a>Msvm \_ PartitionableGpu 類別

代表可分割 GPU。 每個 GPU 都可以分割成多個 GPU 磁碟分割，而這些分割區可指派給虛擬機器作為 vGPU。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_PartitionableGpu : CIM_ComputerSystem
{
  uint16 ValidPartitionCounts[];
  uint16 PartitionCount;
  uint64 TotalVRAM;
  uint64 AvailableVRAM;
  uint64 MinPartitionVRAM;
  uint64 MaxPartitionVRAM;
  uint64 OptimalPartitionVRAM;
  uint64 TotalEncode;
  uint64 AvailableEncode;
  uint64 MinPartitionEncode;
  uint64 MaxPartitionEncode;
  uint64 OptimalPartitionEncode;
  uint64 TotalDecode;
  uint64 AvailableDecode;
  uint64 MinPartitionDecode;
  uint64 MaxPartitionDecode;
  uint64 OptimalPartitionDecode;
  uint64 TotalCompute;
  uint64 AvailableCompute;
  uint64 MinPartitionCompute;
  uint64 MaxPartitionCompute;
  uint64 OptimalPartitionCompute;
};
```

## <a name="members"></a>成員

**Msvm \_ PartitionableGpu** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ PartitionableGpu** 類別具有這些屬性。

<dl> <dt>

**AvailableCompute**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的可用計算引擎數量。

</dd> <dt>

**AvailableDecode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的可用解碼引擎量。

</dd> <dt>

**AvailableEncode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的可用編碼引擎數量。

</dd> <dt>

**AvailableVRAM**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的可用 VRAM 量。

</dd> <dt>

**MaxPartitionCompute**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要出現在 GPU 磁碟分割中的計算引擎數量上限。

</dd> <dt>

**MaxPartitionDecode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要出現在 GPU 磁碟分割中的解碼引擎量上限。

</dd> <dt>

**MaxPartitionEncode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

在 GPU 磁碟分割中會出現的編碼引擎最大數量。

</dd> <dt>

**MaxPartitionVRAM**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要出現在 GPU 分割區中的最大 VRAM 數量。

</dd> <dt>

**MinPartitionCompute**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的最小計算引擎量。

</dd> <dt>

**MinPartitionDecode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的解碼引擎最小數量。

</dd> <dt>

**MinPartitionEncode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的最小編碼引擎數量。

</dd> <dt>

**MinPartitionVRAM**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

要出現在 GPU 磁碟分割中的最小 VRAM 量。

</dd> <dt>

**OptimalPartitionCompute**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的最佳計算引擎量。

</dd> <dt>

**OptimalPartitionDecode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的最佳解碼引擎量。

</dd> <dt>

**OptimalPartitionEncode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的最佳編碼引擎數量。

</dd> <dt>

**OptimalPartitionVRAM**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的最佳 VRAM 量。

</dd> <dt>

**PartitionCount**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

實體 GPU 分割成的 GPU 磁碟分割數量。

</dd> <dt>

**TotalCompute**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的計算引擎總數量。

</dd> <dt>

**TotalDecode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的解碼引擎總數量。

</dd> <dt>

**TotalEncode**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將會出現在 GPU 磁碟分割中的編碼引擎總數量。

</dd> <dt>

**TotalVRAM**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

將出現在 GPU 磁碟分割中的總 VRAM 量。

</dd> <dt>

**ValidPartitionCounts**
</dt> <dd> <dl> <dt>

資料類型： **uint16** 陣列
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

可將實體 GPU 分割成的有效 GPU 分割區選項陣列。

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

[**CIM \_ 未進行**](cim-computersystem.md)
</dt> </dl>

 

 




