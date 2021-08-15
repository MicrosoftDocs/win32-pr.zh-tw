---
description: 傳回指定之虛擬機器定義檔的虛擬機器摘要資訊。
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Msvm_VirtualSystemManagementService 類別的 GetDefinitionFileSummaryInformation 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 7c6d3da6ef920488edb7fde723880b9f53768cfd246e91d287390bb6fb02fb17
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117995295"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 GetDefinitionFileSummaryInformation 方法 \_

傳回指定之虛擬機器定義檔的虛擬機器摘要資訊。

## <a name="syntax"></a>語法


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*DefinitionFiles* \[在\]
</dt> <dd>

要傳回摘要資訊之 XML 設定檔的路徑陣列。

</dd> <dt>

*SummaryInformation* \[擴展\]
</dt> <dd>

[**Msvm \_ SummaryInformationBase**](msvm-summaryinformation.md)實例的陣列，其中包含 *DefinitionFiles* 陣列中所指定之虛擬機器和（或）快照的要求資訊。 只會傳回 **Name**、 **ElementName**、 **CreationTime** 和 **Notes** 屬性，其他所有屬性都是 **Null**。

> [!Note]  

 

在 Windows 10 之前，版本1703，datatype 是 [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

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
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                                              |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                                                    |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




