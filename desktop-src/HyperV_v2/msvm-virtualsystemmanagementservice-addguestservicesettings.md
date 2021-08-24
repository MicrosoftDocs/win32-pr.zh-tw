---
description: 將來賓服務設定新增至虛擬系統設定。
ms.assetid: 2c8c2f2b-332a-470e-af7f-80c82e3e2caf
title: Msvm_VirtualSystemManagementService 類別的 AddGuestServiceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddGuestServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4f011a0bce545bbde57cbcc9c22861f492cbc27e71ddc717a379d82cbd27bc42
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119681138"
---
# <a name="addguestservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 AddGuestServiceSettings 方法 \_

將來賓服務設定新增至虛擬系統設定。

套用至「目前」虛擬系統設定的元件時，可能會修改作用中虛擬系統的副作用來賓服務。

## <a name="syntax"></a>語法


```mof
uint32 AddGuestServiceSettings(
  [in]  CIM_VirtualSystemSettingData REF AffectedConfiguration,
  [in]  string                           GuestServiceSettings[],
  [out] CIM_SettingData              REF ResultingGuestServiceSettings[],
  [out] CIM_ConcreteJob              REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AffectedConfiguration* \[在\]
</dt> <dd>

參考描述受影響設定的 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 。

</dd> <dt>

*GuestServiceSettings* \[在\]
</dt> <dd>

包含來賓服務設定的陣列。

</dd> <dt>

*ResultingGuestServiceSettings* \[擴展\]
</dt> <dd>

成功時，會包含 [**CIM \_ SettingData**](cim-settingdata.md) 的參考，以描述所產生的來賓服務設定。

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
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

