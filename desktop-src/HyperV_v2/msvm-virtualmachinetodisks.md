---
description: 將資料設定為以陣列形式傳遞至 Msvm \_ CollectionReferencePointExportSettingData 類別。
ms.assetid: f127880f-f917-4069-a283-a6f9427c5e07
title: Msvm_VirtualMachineToDisks 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualMachineToDisks
- Msvm_VirtualMachineToDisks.VirtualMachineId
- Msvm_VirtualMachineToDisks.DisksToExport
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: cad5de9389b9cb1d5e7db0573f3a4e3fc271ba31
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847765"
---
# <a name="msvm_virtualmachinetodisks-class"></a>Msvm \_ VirtualMachineToDisks 類別

將資料設定為以陣列形式傳遞至 [**Msvm \_ CollectionReferencePointExportSettingData**](msvm-collectionreferencepointexportsettingdata.md) 類別。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_VirtualMachineToDisks
{
  string VirtualMachineId;
  string DisksToExport[];
};
```

## <a name="members"></a>成員

**Msvm \_ VirtualMachineToDisks** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ VirtualMachineToDisks** 類別具有這些屬性。

<dl> <dt>

**DisksToExport**
</dt> <dd> <dl> <dt>

資料類型： **字串** 陣列
</dt> <dt>

存取類型：唯讀
</dt> </dl>

需要匯出資料之特定虛擬機器識別碼所屬磁片的 WMI 實例識別碼。

</dd> <dt>

**VirtualMachineId**
</dt> <dd> <dl> <dt>

資料類型： **字串**
</dt> <dt>

存取類型：讀取/寫入
</dt> </dl>

與虛擬磁片相關聯的虛擬機器識別碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 10 桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



 

 




