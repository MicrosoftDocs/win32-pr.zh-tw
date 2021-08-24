---
description: 提供現有虛擬硬碟映射的狀態資訊。
ms.assetid: b0177906-71dc-4be8-b351-97d7ef427acd
title: Msvm_VirtualHardDiskState 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualHardDiskState
- Msvm_VirtualHardDiskState.FileSize
- Msvm_VirtualHardDiskState.InUse
- Msvm_VirtualHardDiskState.MinInternalSize
- Msvm_VirtualHardDiskState.PhysicalSectorSize
- Msvm_VirtualHardDiskState.Alignment
- Msvm_VirtualHardDiskState.FragmentationPercentage
- Msvm_VirtualHardDiskState.Timestamp
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c5896e8b19d2897084997bd01b65bbb0d6e80e0ca15f662fff38871bdc0b6755
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119426308"
---
# <a name="msvm_virtualharddiskstate-class"></a>Msvm \_ VirtualHardDiskState 類別

提供現有虛擬硬碟映射的狀態資訊。

下列語法已簡化受控物件格式 (MOF) 程式碼，並且包含所有繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[AMENDMENT]
class Msvm_VirtualHardDiskState
{
  uint64   FileSize;
  boolean  InUse;
  uint64   MinInternalSize;
  uint32   PhysicalSectorSize;
  uint32   Alignment;
  uint32   FragmentationPercentage;
  DATETIME Timestamp;
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualHardDiskState** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualHardDiskState** 類別具有這些屬性。

<dl> <dt>

**對齊**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定虛擬硬碟的對齊類型。 這會是下列其中一個值。



| 值                                                                        | 意義                        |
|------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>0</dt> </dl> | 512位元組對齊。<br/> |
| <dl> <dt>1</dt> </dl> | 4 KB 對齊。<br/>     |



 

</dd> <dt>

**FileSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬硬碟檔案的大小 (檔案) 所耗用的實際儲存體量（以位元組為單位）。

</dd> <dt>

**FragmentationPercentage**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬硬碟檔案中分散的虛擬磁片區塊百分比近似值。

</dd> <dt>

**InUse**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

這個屬性保留給未來的版本使用。

</dd> <dt>

**MinInternalSize**
</dt> <dd> <dl> <dt>

資料類型： **uint64**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

可以壓縮虛擬硬碟的大小下限（以位元組為單位）。 此大小會進位到磁區大小的下一個最大倍數。

</dd> <dt>

**PhysicalSectorSize**
</dt> <dd> <dl> <dt>

資料類型： **uint32**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

基礎實體磁片所使用的實體磁區大小（以位元組為單位）。

</dd> <dt>

**Timestamp**
</dt> <dd> <dl> <dt>

資料類型： **DATETIME**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

虛擬硬碟的時間戳記

> [!Note]  
> 加入 Windows 10 和 Windows Server 2016。

 

</dd> </dl>

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

[**GetVirtualHardDiskState**](getvirtualharddiskstate-msvm-imagemanagementservice.md)
</dt> </dl>

 

 




