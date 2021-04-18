---
description: 設定客體作業系統內的網路介面卡。
ms.assetid: 698e0c17-f8bd-433f-b982-5481f9701ba6
title: Msvm_VirtualSystemManagementService 類別的 SetGuestNetworkAdapterConfiguration 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.SetGuestNetworkAdapterConfiguration
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 02c79df7aa08faa842e2b702b4cf18944e96bdfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104513356"
---
# <a name="setguestnetworkadapterconfiguration-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 SetGuestNetworkAdapterConfiguration 方法 \_

設定客體作業系統內的網路介面卡。 這些設定參數會在與在客體作業系統內執行的 KVP Exchange 整合元件建立通訊時立即套用。

## <a name="syntax"></a>語法


```mof
uint32 SetGuestNetworkAdapterConfiguration(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [in]  string                 NetworkConfiguration[],
  [out] CIM_ConcreteJob    REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

未進行 \[在\]
</dt> <dd>

要設定其網路介面卡之 [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-computersystem) 實例實例的參考。

</dd> <dt>

*NetworkConfiguration* \[在\]
</dt> <dd>

[**Msvm \_ GuestNetworkAdapterConfiguration**](msvm-guestnetworkadapterconfiguration.md)類別的內嵌實例陣列。 每個實例都會描述虛擬機器中其中一個網路介面卡的設定參數。 每個實例都必須指定 **DHCPEnabled** 屬性。

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

 

