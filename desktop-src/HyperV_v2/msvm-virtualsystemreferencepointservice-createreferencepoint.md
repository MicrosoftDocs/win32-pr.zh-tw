---
description: 建立虛擬系統的參考點。
ms.assetid: 9cc7665a-9562-4267-bcd0-3162e426fbad
title: Msvm_VirtualSystemReferencePointService 類別的 CreateReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.CreateReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: fdcf4680ff10bdc8135fae4ec3bb9f81d53c26092e7196e73965ee4f4d87991f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014476"
---
# <a name="createreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Msvm VirtualSystemReferencePointService 類別的 CreateReferencePoint 方法 \_

建立虛擬系統的參考點。

## <a name="syntax"></a>語法


```mof
uint32 CreateReferencePoint(
  [in]      Msvm_ComputerSystem              REF AffectedSystem,
  [in]      string                               ReferencePointSettings,
  [in]      uint16                               ReferencePointType,
  [in, out] Msvm_VirtualSystemReferencePoint REF ResultingReferencePoint,
  [out]     CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*AffectedSystem* \[在\]
</dt> <dd>

參考受影響之虛擬系統的 [**Msvm \_**](msvm-computersystem.md) 系統。

</dd> <dt>

*ReferencePointSettings* \[在\]
</dt> <dd>

包含參數設定。

</dd> <dt>

*ReferencePointType* \[在\]
</dt> <dd>

要求的參考點類型：

<dt>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>

<span id="Log_based"></span><span id="log_based"></span><span id="LOG_BASED"></span>以 **記錄為基礎** 的 (0) 


</dt> <dd>

以 Hyper-v 複本記錄檔追蹤為基礎。

</dd> <dt>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>

<span id="RCT_based"></span><span id="rct_based"></span><span id="RCT_BASED"></span>**依** (1) 的 .rct


</dt> <dd>

以虛擬磁片的復原變更追蹤為基礎。

</dd> </dl> </dd> <dt>

*ResultingReferencePoint* \[in、out\]
</dt> <dd>

產生的虛擬系統參考點

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業的執行時間很長，則可以選擇性地傳回作業。 在此情況下， [**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md) 類別的實例（代表新的虛擬系統參考點）會透過 [**CIM \_ AffectedJobElement**](cim-affectedjobelement.md) 關聯來呈現，而 **AffectedElement** 屬性的值則是參考 **Msvm \_ VirtualSystemReferencePoint** 類別的新實例，代表虛擬系統參考點，而 **ElementEffects** 的值設定為 5 (建立) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，會傳回 0;否則，會傳回錯誤。

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

**不正確狀態** (5) 
</dt> <dt>

**不正確類型** (6) 
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

[**Msvm \_ VirtualSystemReferencePointService**](msvm-virtualsystemreferencepointservice.md)
</dt> </dl>

 

 




