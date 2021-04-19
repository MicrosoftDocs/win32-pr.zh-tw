---
description: 使用指定的配置設定開始作業，以變更父集區。
ms.assetid: 2eea1a60-fbf0-49a7-8f79-52c62c295316
title: CIM_ResourcePoolConfigurationService 類別的 ChangeParentResourcePool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.ChangeParentResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 6ef852d6af8f0973b6b3f29fca5fcd90e9ce726a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973092"
---
# <a name="changeparentresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>CIM ResourcePoolConfigurationService 類別的 ChangeParentResourcePool 方法 \_

使用指定的配置設定開始作業，以變更父集區。

## <a name="syntax"></a>語法


```mof
uint32 ChangeParentResourcePool(
  [in]  CIM_ResourcePool REF ChildPool,
  [in]  CIM_ResourcePool REF ParentPool[],
  [in]  string               Settings[],
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ChildPool* \[在\]
</dt> <dd>

參考子集區的 [**CIM \_ ResourcePool**](cim-resourcepool.md) 。

</dd> <dt>

*ParentPool* \[在\]
</dt> <dd>

 (s) 參考父集區的 [**CIM \_ ResourcePool**](cim-resourcepool.md) 陣列。

</dd> <dt>

*設定* \[在\]
</dt> <dd>

選擇性字串，其中包含用來指定父集區設定的 [**CIM \_ SettingData**](cim-settingdata.md) 實例標記法。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業已完成) ，則參考作業 (的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 可能會是 **null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

<dl> <dt>

**作業已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**未知** 的 (2) 
</dt> <dt>

**Timeout** (3) 
</dt> <dt>

**失敗** (4) 
</dt> <dt>

**不正確參數** (5) 
</dt> <dt>

**使用** (6) 
</dt> <dt>

集區的 ResourceType (7) **不正確**
</dt> <dt>

**資源不足** (8) 
</dt> <dt>

**DMTF 保留** ( .。。) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

 (4097) **不支援的大小**
</dt> <dt>

**方法保留** (4098. 32767) 
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

[**CIM \_ ResourcePoolConfigurationService**](cim-resourcepoolconfigurationservice.md)
</dt> </dl>

 

 




