---
description: 將虛擬機器或虛擬機器的快照集匯出到檔案。
ms.assetid: b88712e4-a1a6-4188-8082-f4973f89018d
title: Msvm_VirtualSystemManagementService 類別的 ExportSystemDefinition 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ExportSystemDefinition
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9f6b6dc5728a4275965ccd482d851601ecd1c6e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689496"
---
# <a name="exportsystemdefinition-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 ExportSystemDefinition 方法 \_

將虛擬機器或虛擬機器的快照集匯出到檔案。 虛擬機器必須處於「已關閉電源」或「已儲存」狀態才能匯出。 虛擬機器、其相關聯的設定設定，以及其相關聯的資源設定將會保留在產生的檔案中。

## <a name="syntax"></a>語法


```mof
uint32 ExportSystemDefinition(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 ExportDirectory,
  [in]  string                 ExportSettingData,
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

未進行 \[在\]
</dt> <dd>

CIM 電腦的參考 [**， \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 代表要匯出的虛擬機器。

</dd> <dt>

*ExportDirectory* \[在\]
</dt> <dd>

要匯出虛擬機器之目錄的完整路徑。 如果 *ExportSettingData* 參數中 [**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)類別的 **CreateVmExportSubdirectory** 屬性設定為 **True**，則可以重複使用此目錄來匯出多部虛擬機器，而此方法會將每個虛擬機器定義放在此路徑底下的個別子目錄中。

</dd> <dt>

*ExportSettingData* \[在\]
</dt> <dd>

[**Msvm \_ VirtualSystemExportSettingData**](msvm-virtualsystemexportsettingdata.md)類別的內嵌實例，表示匯出作業的設定。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**無法** (32768) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> <dt>

**不支援** (32770) 
</dt> <dt>

**狀態未知** (32771) 
</dt> <dt>

**Timeout** (32772) 
</dt> <dt>

**不正確參數** (32773) 
</dt> <dt>

**系統正在使用中** (32774) 
</dt> <dt>

**此操作的狀態無效** (32775) 
</dt> <dt>

**不正確的資料類型** (32776) 
</dt> <dt>

**系統無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

