---
description: 表示虛擬系統的儲存特定設定。
ms.assetid: 0b3fcd78-7e9a-4a94-ad18-0ca72b3cfd73
title: Msvm_StorageSettingData 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageSettingData
- Msvm_StorageSettingData.VirtualProcessorsPerChannel
- Msvm_StorageSettingData.DisableInterruptBatching
- Msvm_StorageSettingData.ThreadCountPerChannel
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: db061d048ce45a4d6fa076a5b0367e794cdf16e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998909"
---
# <a name="msvm_storagesettingdata-class"></a>Msvm \_ StorageSettingData 類別

表示虛擬系統的儲存特定設定。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_StorageSettingData : Msvm_SystemComponentSettingData
{
  uint16  VirtualProcessorsPerChannel;
  boolean DisableInterruptBatching;
  uint16  ThreadCountPerChannel;
};
```

## <a name="members"></a>成員

**Msvm \_ StorageSettingData** 類別具有下列類型的成員：

-   [屬性](#properties)

### <a name="properties"></a>屬性

**Msvm \_ StorageSettingData** 類別具有這些屬性。

<dl> <dt>

**DisableInterruptBatching**
</dt> <dd> <dl> <dt>

資料類型： **布林值**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

指定是否應該停用中斷批次處理。

這是唯讀屬性，但是可以使用 Wmi [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)方法來變更。

</dd> <dt>

**ThreadCountPerChannel**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

處理 IO 的每個儲存通道執行緒數目。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)方法來變更。

<dt>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>

<span id="Default"></span><span id="default"></span><span id="DEFAULT"></span>**預設** (0) 


</dt> <dd>

預設行為

</dd> <dt>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>

<span id="Low"></span><span id="low"></span><span id="LOW"></span>**低** (1) 


</dt> <dd>

每個儲存體通道的執行緒數目下限。

</dd> <dt>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>

<span id="Medium"></span><span id="medium"></span><span id="MEDIUM"></span>**中型** (2) 


</dt> <dd>

每個儲存體通道的執行緒數目。

</dd> <dt>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>

<span id="High"></span><span id="high"></span><span id="HIGH"></span>**高** (3) 


</dt> <dd>

每個儲存體通道有大量的執行緒。

</dd> </dl>

</dd> <dt>

**VirtualProcessorsPerChannel**
</dt> <dd> <dl> <dt>

資料類型： **uint16**
</dt> <dt>

存取類型：唯讀
</dt> </dl>

每個儲存體通道的處理器數目。 要開啟的通道數目是由主機/**VirtualProcessorsPerChannel**) 上的 (邏輯處理器計數所指定。

這是唯讀屬性，但是可以使用 [**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)類別的 [**ModifySystemComponentSettings**](msvm-virtualsystemmanagementservice-modifysystemcomponentsettings.md)方法來變更。

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

[**Msvm \_ SystemComponentSettingData**](msvm-systemcomponentsettingdata.md)
</dt> </dl>

 

 




