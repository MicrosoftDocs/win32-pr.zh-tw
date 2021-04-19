---
description: 將資源新增至虛擬系統設定。
ms.assetid: c2541571-74f0-48f8-997c-56c152980eea
title: CIM_VirtualSystemManagementService 類別的 AddResourceSettings 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.AddResourceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 9563b1e8421dfa6724971450b117780435f6f39e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974396"
---
# <a name="addresourcesettings-method-of-the-cim_virtualsystemmanagementservice-class"></a>CIM VirtualSystemManagementService 類別的 AddResourceSettings 方法 \_

將資源新增至虛擬系統設定。

當套用至「狀態」虛擬系統設定時，將會在作用中的虛擬系統中加入副作用資源。

## <a name="syntax"></a>語法


```mof
uint32 AddResourceSettings(
  [in]  CIM_VirtualSystemSettingData      REF AffectedConfiguration,
  [in]  string                                ResourceSettings[],
  [out] CIM_ResourceAllocationSettingData REF ResultingResourceSettings[],
  [out] CIM_ConcreteJob                   REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AffectedConfiguration* \[在\]
</dt> <dd>

受影響之虛擬系統組態的 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 參考。

</dd> <dt>

*ResourceSettings* \[在\]
</dt> <dd>

字串陣列，其中每個字串都包含一個類別 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 的內嵌實例，以描述要新增至虛擬系統的虛擬資源的虛擬層面。

</dd> <dt>

*ResultingResourceSettings* \[擴展\]
</dt> <dd>

類別 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 實例的參考陣列，代表已新增之虛擬資源的虛擬層面。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業的執行時間很長，則可以選擇性地傳回作業。 在此情況下，可透過代表受影響之虛擬系統設定的 [**cim \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md)類別實例，透過關聯 **cim \_ ConreteComponent** ，取得代表新增資源設定的類別 [**cim \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md)實例。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

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
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ VirtualSystemManagementService**](cim-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




