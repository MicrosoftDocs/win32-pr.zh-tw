---
description: 方法來執行前置檢查，以判斷虛擬系統是否可能成功地遷移至網路名稱或 IP 位址所指定的目標主機。
ms.assetid: bfcd4063-30fe-4d18-9df9-7b84a680814c
title: CIM_VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToHost 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemMigrationService.CheckVirtualSystemIsMigratableToHost
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5769691a792b8f74225b640b0058ad4bd0e27c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "107001704"
---
# <a name="checkvirtualsystemismigratabletohost-method-of-the-cim_virtualsystemmigrationservice-class"></a>CIM VirtualSystemMigrationService 類別的 CheckVirtualSystemIsMigratableToHost 方法 \_

方法來執行前置檢查，以判斷虛擬系統是否可能成功地遷移至網路名稱或 IP 位址所指定的目標主機。 這種方法不保證後續的遷移一律會成功，因為動態資源可用性。

傳回碼描述：

注意：此方法只是要在叢集支援的模型可供使用時，才會成為過渡解決方案。

## <a name="syntax"></a>語法


```mof
uint32 CheckVirtualSystemIsMigratableToHost(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 DestinationHost,
  [in]  string                 MigrationSettingData,
  [in]  string                 NewSystemSettingData,
  [in]  string                 NewResourceSettingData[],
  [out] boolean                IsMigratable
);
```



## <a name="parameters"></a>參數

<dl> <dt>

未進行 \[在\]
</dt> <dd>

要遷移的來源虛擬電腦系統的 CIM 系統可參考。 [**\_**](cim-computersystem.md)

</dd> <dt>

*DestinationHost* \[在\]
</dt> <dd>

遷移的目標主機系統。

此參數可接受的格式，是透過 \[ \] [**cim \_ ElementCapabilities**](cim-elementcapabilities.md)關聯所關聯之 [**cim \_ VirtualSystemMigrationCapabilities**](cim-virtualsystemmigrationcapabilities.md)的實例中，DestinationHostFormatsSupported 陣列屬性的元素值來傳達。

</dd> <dt>

*MigrationSettingData* \[在\]
</dt> <dd>

字串，包含 [**CIM \_ VirtualSystemMigrationSettingData**](cim-virtualsystemmigrationsettingdata.md) 類別的內嵌實例，代表適用于遷移作業的遷移設定。

</dd> <dt>

*NewSystemSettingData* \[在\]
</dt> <dd>

字串，包含 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 類別的內嵌實例，代表在遷移之後適用于虛擬系統的新屬性。

</dd> <dt>

*NewResourceSettingData* \[在\]
</dt> <dd>

字串陣列，其中每個字串都包含 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 類別的內嵌實例，代表在遷移之後，虛擬系統範圍中適用于虛擬資源的新屬性。

</dd> <dt>

*IsMigratable* \[擴展\]
</dt> <dd>

表示是否可以成功遷移虛擬系統的遷移檢查結果。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。



| 傳回碼/值                                                                                                                                                | Description                                                                                                                                                                                                                                                                                                                                                                            |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**已完成，沒有錯誤**</dt> <dt>0</dt> </dl>    | 檢查已執行;透過 \[ Out \] *IsMigratable* 參數值回報的結果。<br/>                                                                                                                                                                                                                                                                                 |
| <dl> <dt>**不支援**</dt> <dt>1</dt> </dl>              | 實作為不支援的方法。 沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。<br/>                                                                                                                                                                                                                                                       |
| <dl> <dt>**失敗**</dt> <dt>2</dt> </dl>                     | 檢查失敗的原因不明。 沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。<br/>                                                                                                                                                                                                                                                         |
| <dl> <dt>**Timeout**</dt> <dt>3</dt> </dl>                    | 檢查超時。沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。<br/>                                                                                                                                                                                                                                                                              |
| <dl> <dt>**不正確參數**</dt> <dt>4</dt> </dl>          | 一或多個參數正式無效。 例如，您可以使用不支援的格式來指定 *DestinationHost* 參數的值。 沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。<br/>                                                                                                                                    |
| <dl> <dt>**狀態**</dt> <dt>5</dt>無效 </dl>              | 來源虛擬系統、來源主機系統或目標主機系統處於允許起始要求的虛擬系統移轉的狀態;這可能是暫時性的狀況。 沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。<br/>                                                                                           |
| <dl> <dt>**不相容的參數**</dt> <dt>6</dt> </dl>    | 一或多個輸入參數與一組或目標主機不相容。 例如， *MigrationNewSettingData* 參數的值包含由 *DestinationHost* 參數的值所識別的目標主機系統不支援的屬性。 沒有透過 \[ Out \] *IsMigratable* 參數值回報的結果。<br/> |
| <dl> 已 <dt>**保留 DMTF**</dt> <dt></dt> </dl>             |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**方法保留**</dt>的 <dt>4097。</dt> </dl>  |                                                                                                                                                                                                                                                                                                                                                                                        |
| <dl> <dt>**廠商**</dt>專屬 <dt>的 32768. 65535</dt> </dl> |                                                                                                                                                                                                                                                                                                                                                                                        |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ VirtualSystemMigrationService**](cim-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




