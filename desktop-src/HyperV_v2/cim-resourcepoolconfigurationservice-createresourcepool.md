---
description: 啟動建立根 ResourcePool 的作業。 ResourcePool 的範圍會設定為與此服務相同的系統。
ms.assetid: 357880dc-125a-452c-89f5-44cd17684436
title: CIM_ResourcePoolConfigurationService 類別的 CreateResourcePool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ca339eb2e2a4ec0fb441c5ed1a657608d71248bc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690800"
---
# <a name="createresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>CIM ResourcePoolConfigurationService 類別的 CreateResourcePool 方法 \_

啟動建立根 ResourcePool 的作業。 ResourcePool 的範圍會設定為與此服務相同的系統。

## <a name="syntax"></a>語法


```mof
uint32 CreateResourcePool(
  [in]  string                ElementName,
  [in]  CIM_LogicalDevice REF HostResources[],
  [in]  string                ResourceType,
  [out] CIM_ResourcePool  REF Pool,
  [out] CIM_ConcreteJob   REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ElementName* \[在\]
</dt> <dd>

要建立之集區的終端使用者相關名稱。 如果是 **Null**，則可以使用系統提供的預設名稱。 值會儲存在所建立集區的 **ElementName** 屬性中。

</dd> <dt>

*HostResources* \[在\]
</dt> <dd>

零或多個 [**CIM \_ LogicalDevice**](cim-logicaldevice.md) 裝置的陣列，用來建立集區或修改來源延伸。 陣列中的所有元素都必須是相同的類型。

</dd> <dt>

*ResourceType* \[in\]
</dt> <dd>

所建立集區將管理的資源類型。 如果 *HostResources* 包含元素，此屬性必須符合其型別。

</dd> <dt>

*集* \[ 區擴展\]
</dt> <dd>

成功時，傳回所產生之 [**CIM \_ ResourcePool**](cim-resourcepool.md)的參考。 傳回工作時，這可能是 **Null**，在這種情況下，用戶端必須在作業完成之後，使用該作業來尋找產生的 ResourcePool。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業已完成) ，則參考代表作業 (的 [**CIM \_ ConcreteJob**](cim-concretejob.md) 可能是 null。

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

 

 




