---
description: 建立子資源集區。
ms.assetid: 30a70231-f1b7-4f0e-ac47-cf5a79ddb8ab
title: Msvm_ResourcePoolConfigurationService 類別的 >batchclient.pooloperations.createpool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ResourcePoolConfigurationService.CreatePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fb29a4b5a47d88232a6b0df6a828d482030b3f1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978023"
---
# <a name="createpool-method-of-the-msvm_resourcepoolconfigurationservice-class"></a>Msvm ResourcePoolConfigurationService 類別的 >batchclient.pooloperations.createpool 方法 \_

建立子資源集區。 資源集區的範圍將設定為與此服務相同的系統。 產生的集區將會是子集區。

## <a name="syntax"></a>語法


```mof
uint32 CreatePool(
  [in]  string               PoolSettings,
  [in]  CIM_ResourcePool REF ParentPools[],
  [in]  string               AllocationSettings[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*PoolSettings* \[在\]
</dt> <dd>

[**Msvm \_ ResourcePoolSettingData**](msvm-resourcepoolsettingdata.md)類別的內嵌實例，可用來指定非配置相關的集區設定。

</dd> <dt>

*ParentPools* \[在\]
</dt> <dd>

[**Msvm \_ ResourcePool**](msvm-resourcepool.md)參考的陣列，代表要在其中建立新集區的集區或集區。

</dd> <dt>

*AllocationSettings* \[在\]
</dt> <dd>

一或多個 [**Msvm \_ ResourceAllocationSettingData**](msvm-resourceallocationsettingdata.md) 類別的內嵌實例陣列，用來指定集區配置的相關設定。 這個陣列必須針對 *ParentPools* 陣列中的每個元素，或只包含一個元素。 如果這個陣列包含一個元素，而 *ParentPools* 包含一個以上的元素，則 *AlllocationSettings* 會指定可由任何父集區滿足的共用容量配置。

這是用來將可從子系配置給集區的資源，限制為低於其父系所提供之匯總容量的限制。 並非所有資源類型都支援此選項。 如果資源類型不支援共用容量配置，這個方法將會傳回 32770 (不支援) 。

</dd> <dt>

*集* \[ 區擴展\]
</dt> <dd>

所產生集區的參考。

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

 

