---
description: 變更指派給子集區之資源的父集區資源設定。
ms.assetid: 419fca70-5f15-4593-80ac-ef2af2c3dde5
title: Msvm_ResourcePoolConfigurationService 類別的 ModifyPoolResources 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.ModifyPoolResources
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2efffdbcc34577f675556874c4153eea2670768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850955"
---
# <a name="modifypoolresources-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Msvm ResourcePoolConfigurationService 類別的 ModifyPoolResources 方法 \_

變更指派給子集區之資源的父集區資源設定。

## <a name="syntax"></a>語法


```mof
uint32 ModifyPoolResources(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ChildPool* \[在\]
</dt> <dd>

[**CIM \_ ResourcePool**](cim-resourcepool.md)類別實例的參考，代表要修改的子集區。

</dd> <dt>

*ParentPools* \[在\]
</dt> <dd>

[**CIM \_ ResourcePool**](cim-resourcepool.md)參考的陣列，代表要指派給子集區的新父集區。

</dd> <dt>

*AllocationSettings* \[在\]
</dt> <dd>

一或多個 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例的選擇性陣列，用來指定集區配置的相關設定。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**作業已完成，沒有錯誤** (0) 
</dt> <dt>

**DMTF 保留** ( .。。) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**方法保留** (4097. 32767) 
</dt> <dt>

**無法** (32768) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> <dt>

**不支援** (32770) 
</dt> <dt>

**未知** 的 (32771) 
</dt> <dt>

**Timeout** (32772) 
</dt> <dt>

**不正確參數** (32773) 
</dt> <dt>

**使用中** (32774) 
</dt> <dt>

**不正確狀態** (32775) 
</dt> <dt>

集區 (32776) **不正確的資源類型**
</dt> <dt>

**無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
</dt> <dt>

**廠商保留** (32779) 
</dt> <dt>

**資源不足** (32780) 
</dt> <dt>

**找不到物件** (32781 32787) 
</dt> <dt>

**物件存在** (32788) 
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

[**Msvm \_ ResourcePoolConfigurationService**](msvm-resourcepoolconfigurationservice.md)
</dt> </dl>

 

