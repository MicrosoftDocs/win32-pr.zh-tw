---
description: 建立新的虛擬交換器。
ms.assetid: de7495e9-48c5-427a-b9bb-0821b53a9b09
title: Msvm_VirtualEthernetSwitchManagementService 類別的 DefineSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: bd6e2dfb7d9cf7e64fb76c35f6f3c3b8457d69d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850960"
---
# <a name="definesystem-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a>Msvm VirtualEthernetSwitchManagementService 類別的 DefineSystem 方法 \_

建立新的虛擬交換器。 未指定的屬性將會填入預設值。

## <a name="syntax"></a>語法


```mof
uint32 DefineSystem(
  [in]  string                           SystemSettings,
  [in]  string                           ResourceSettings[],
  [in]  CIM_VirtualSystemSettingData REF ReferenceConfiguration,
  [out] CIM_ComputerSystem           REF ResultingSystem,
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*SystemSettings* \[在\]
</dt> <dd>

[**Msvm \_ VirtualEthernetSwitchSettingData**](msvm-virtualethernetswitchsettingdata.md)類別的內嵌實例，可用來定義要建立之虛擬交換器的屬性。 此為必要參數。

</dd> <dt>

*ResourceSettings* \[在\]
</dt> <dd>

[**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md)類別的內嵌實例陣列，描述要在新虛擬交換器範圍中建立之交換器埠的設定。 如果指定 **Null** ，則不會建立任何資源 (的虛擬交換器，亦即沒有任何交換器埠) 。

</dd> <dt>

*ReferenceConfiguration* \[在\]
</dt> <dd>

不使用這個參數。

</dd> <dt>

*ResultingSystem* \[擴展\]
</dt> <dd>

如果已成功建立虛擬交換器，則為代表新定義虛擬交換器之 [**Msvm \_ VirtualEthernetSwitch**](msvm-virtualethernetswitch.md) 類別實例的參考。

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

**不支援** (1) 
</dt> <dt>

**失敗** (2) 
</dt> <dt>

**Timeout** (3) 
</dt> <dt>

**不正確參數** (4) 
</dt> <dt>

**DMTF 保留** ( .。。) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**方法保留** (4097. 32767) 
</dt> <dt>

**廠商特定** (32768. 65535) 
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

[**Msvm \_ VirtualEthernetSwitchManagementService**](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

