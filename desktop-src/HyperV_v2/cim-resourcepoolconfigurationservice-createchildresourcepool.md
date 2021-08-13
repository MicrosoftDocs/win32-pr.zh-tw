---
description: 使用指定的配置設定啟動作業，以從父集區建立子集區。
ms.assetid: 9b09221a-7c4e-4648-a2a8-012df1818c3e
title: CIM_ResourcePoolConfigurationService 類別的 CreateChildResourcePool 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ResourcePoolConfigurationService.CreateChildResourcePool
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 48a43baeefcbc56707fa6327930d9c18eaa57a2442b81fbc5f5cff17633b2148
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118648150"
---
# <a name="createchildresourcepool-method-of-the-cim_resourcepoolconfigurationservice-class"></a>CIM ResourcePoolConfigurationService 類別的 CreateChildResourcePool 方法 \_

使用指定的配置設定啟動作業，以從父集區建立子集區。

## <a name="syntax"></a>語法


```mof
uint32 CreateChildResourcePool(
  [in]  string               ElementName,
  [in]  string               Settings[],
  [in]  CIM_ResourcePool REF ParentPool[],
  [out] CIM_ResourcePool REF Pool,
  [out] CIM_ConcreteJob  REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ElementName* \[在\]
</dt> <dd>

要建立之集區的終端使用者相關名稱。 如果是 **Null**，則可以使用系統提供的預設名稱。 值會儲存在所建立專案的 **ElementName** 屬性中。

</dd> <dt>

*設定* \[在\]
</dt> <dd>

字串，包含用來指定子集區設定的 [**CIM \_ SettingData**](cim-settingdata.md) 實例表示。

</dd> <dt>

*ParentPool* \[在\]
</dt> <dd>

用來建立新集區的 [**CIM \_ ResourcePool**](cim-resourcepool.md) 。

</dd> <dt>

*集* \[ 區擴展\]
</dt> <dd>

參考所產生集區的 [**CIM \_ ResourcePool**](cim-resourcepool.md) 。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業已完成) ，則作業 (的參考可能會是 null。

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

 

 




