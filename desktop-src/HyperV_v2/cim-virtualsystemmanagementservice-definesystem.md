---
description: 定義虛擬系統。
ms.assetid: c3964e99-9227-4b98-af87-7caa59296306
title: CIM_VirtualSystemManagementService 類別的 DefineSystem 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemManagementService.DefineSystem
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 2e38111d52044ed385fdd8cd19dd9094834e794c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974627"
---
# <a name="definesystem-method-of-the-cim_virtualsystemmanagementservice-class"></a>CIM VirtualSystemManagementService 類別的 DefineSystem 方法 \_

定義虛擬系統。

未完全指定的輸入可能會以預設值填入。

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

字串，包含類別 [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) 的內嵌實例，可用來定義要建立之虛擬系統的屬性。

</dd> <dt>

*ResourceSettings* \[在\]
</dt> <dd>

字串陣列，其中每個字串都包含類別 [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) 的內嵌實例，以描述要在新虛擬系統的範圍中建立之虛擬資源的虛擬層面。

</dd> <dt>

*ReferenceConfiguration* \[在\]
</dt> <dd>

參考虛擬系統組態的最上層物件之 [**CIM \_ VirtualSystemSettingDat**](cim-virtualsystemsettingdata.md) 物件實例的參考。 如果 *SystemSettings* 和 *ResourceSettings* 參數未提供個別的資訊，則會使用參考設定來補充新虛擬系統的設定。

</dd> <dt>

*ResultingSystem* \[擴展\]
</dt> <dd>

如果已成功定義虛擬電腦系統，則會傳回代表新定義虛擬電腦 [**系統 \_ 之類別的實例的參考**](cim-computersystem.md) 。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業的執行時間很長，則可以選擇性地傳回作業。 在此情況下，會透過關聯 [**cim \_ AffectedJobElement**](cim-affectedjobelement.md)來呈現代表新虛擬系統的類別 [**cim \_**](cim-computersystem.md)系統實例，並以屬性 **AffectedElement** 參考 Cim 的新實例，**並 \_** 將屬性 **ElementEffects** 設定為 5 (建立) 。

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

 

 




