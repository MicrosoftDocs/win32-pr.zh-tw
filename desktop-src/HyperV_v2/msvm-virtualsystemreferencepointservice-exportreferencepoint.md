---
description: 匯出虛擬系統的參考點。
ms.assetid: e4d80404-6b1b-4153-9ab2-aebab18c331a
title: Msvm_VirtualSystemReferencePointService 類別的 ExportReferencePoint 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointService.ExportReferencePoint
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 3273c4781858b02e60b632ae491b1694068a32f5feaddea885576dade6876989
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119147951"
---
# <a name="exportreferencepoint-method-of-the-msvm_virtualsystemreferencepointservice-class"></a>Msvm VirtualSystemReferencePointService 類別的 ExportReferencePoint 方法 \_

匯出虛擬系統的參考點。

## <a name="syntax"></a>語法


```mof
uint32 ExportReferencePoint(
  [in]  Msvm_VirtualSystemReferencePoint REF ReferencePoint,
  [in]  string                               ExportDirectory,
  [in]  string                               ExportSettingData,
  [out] CIM_ConcreteJob                  REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ReferencePoint* \[在\]
</dt> <dd>

[**Msvm \_ VirtualSystemReferencePoint**](msvm-virtualsystemreferencepoint.md)實例的參考，代表要匯出的參考點。

</dd> <dt>

*ExportDirectory* \[在\]
</dt> <dd>

要匯出參考點之目錄的完整路徑。

</dd> <dt>

*ExportSettingData* \[在\]
</dt> <dd>

[**Msvm \_ VirtualSystemReferencePointExportSettingData**](msvm-virtualsystemreferencepointexportsettingdata.md)的實例，表示匯出作業的設定。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

用於監視作業進度的選擇性參數，如果無法同步執行方法，就會使用此參數。 如果作業是以非同步方式執行，則傳回值為4096。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時，會傳回 0 (完成，沒有錯誤) ，或 4096 (作業已啟動) ;否則，會傳回錯誤。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**無法** (32768) 
</dt> <dt>

**拒絕存取** (32769) 
</dt> <dt>

**不支援** (32770) 
</dt> <dt>

**狀態未知** (32771) 
</dt> <dt>

**Timeout** (32772) 
</dt> <dt>

**不正確參數** (32773) 
</dt> <dt>

**系統正在使用中** (32774) 
</dt> <dt>

**此操作的狀態無效** (32775) 
</dt> <dt>

**不正確的資料類型** (32776) 
</dt> <dt>

**系統無法使用** (32777) 
</dt> <dt>

**記憶體不足** (32778) 
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

 

 




